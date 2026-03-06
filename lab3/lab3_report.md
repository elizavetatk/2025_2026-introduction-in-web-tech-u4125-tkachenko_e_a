University: [ITMO University](https://itmo.ru/ru/)  
Faculty: [FICT](https://fict.itmo.ru)  
Course: [Введение в веб технологии](https://itmo-ict-faculty.github.io/introduction-in-web-tech/)  
Year: 2025/2026  
Group: U4125  
Author: Tkachenko Elizaveta Andreevna  
Lab: Lab3  
Date of create: 05.03.2026  
Date of finished:  

## Лабораторная работа №3  

## Ход работы:

Настройка мониторинга с Prometheus и Grafana:

1. Создание конфигурации Prometheus:
- Соpдать папку prometheus для конфигурации
- Создать файл prometheus/prometheus.yml 

2. Запуск Node Exporterscrape_configs:
- Запустить контейнер Node Exporter для сбора системных метрик:
- Проверить работу: curl http://localhost:9100/metrics

3. Запуск Prometheus:

- Создать том для данных Prometheus:

*docker volume create prometheus-data*  
*docker network create monitoring*  

- Выйти на папку выше в консоли, убедиться что вы находитесь над уровнем папки prometheus. Запустить контейнер Prometheus:
- Проверить работу: открыть http://localhost:9090 в браузере

4. Запуск Grafana:
- Создать том для данных Grafana:
*docker volume create grafana-data*
- Запустить контейнер Grafana:
- Проверить работу: открыть http://localhost:3000 в браузере

5. Настройка Grafana:
- Войти в Grafana
- **Добавить источник данных Prometheus:**
* Configuration → Data Sources → Add data source
* Выбрать Prometheus
* URL: http://prometheus:9090
* Save & Test
- **Создать дашборд:**
* Create → Dashboard → Add visualization
* Выбрать источник данных Prometheus
* Добавить метрику: node_cpu_seconds_total
* Сохранить дашборд

На последнем этапе добавления метрики node_cpu_seconds_total у меня возникала ошибка (никаких данных не было).  
Я перепроверила Prometheus и нашла там проблему, что данные не собирались.  
Исправила! Оказалось, что проблема была в том, что Node Exporter был запущен до создания сети monitoring и не был в нее добавлен. 
Также потребовалось сделать docker restart prometheus. После этого все получилось (на скринах также прикладываю проблемы возникшие.

6. Тестирование системы:
- Проверить все контейнеры: docker ps
- Открыть Prometheus и убедиться, что метрики собираются
- Открыть Grafana и проверить отображение графиков
- Создать несколько графиков для разных метрик  

Выбрала такие метрики и добавила их графики:  
Память: node_memory_MemTotal_bytes    
Диск: node_filesystem_size_bytes  
