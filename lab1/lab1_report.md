University: [ITMO University](https://itmo.ru/ru/)  
Faculty: [FICT](https://fict.itmo.ru)  
Course: [Введение в веб технологии](https://itmo-ict-faculty.github.io/introduction-in-web-tech/)  
Year: 2025/2026  
Group: U4125  
Author: Tkachenko Elizaveta Andreevna  
Lab: Lab1  
Date of create: 03.03.2026  
Date of finished:  

Лабораторная работа №1 "Основы работы с Docker"

Ход работы
1. Установка Docker (скриншоты 1.1, 1.2, 1.3)  
Чтобы не писать везде sudo добавила выполнила команду sudo usermod -aG docker $USER и перезапуск newgrp docker  
2. Работа с готовыми образами (скриншоты 1.3, 2.1)  
3. Запуск веб-сервера nginx (скриншоты 3.1, 3.2 - в браузере, 3.3)  
4. Управление контейнерами (скриншоты 4.1, 4.2 - в браузере после удаления образа rmi)  
5. Работа с томами (volumes): скриншоты 5.1, 5.2  
через команду cat /data/test.txt читала содержимое созданного файла  

В результате работы я научилась на базовом уровне работать с Docker: устанавливать, создавать Dockerfile, собирать образы, запускать контейнеры и управлять ими.

Лабораторная работа со звездочкой - Создание Dockerfile по заданным условиям:
1. Создала файл проекта app.py с соответствующим содержанием
2. Создала файл requirements.txt со следующим содержанием (так как возникла ошибка версий в процессе):  
Flask==2.0.1  
Werkzeug==2.0.3  
Jinja2==3.0.3  
itsdangerous==2.0.1  
click==8.0.4  
3. Создала Dockerfile с соответствующими условиями (на скрине img cat_Dockerfile)  
4. Проверила работу, все получилось!  
Собрать образ: docker build -t my-flask-app .  
Запустить контейнер: docker run -d -p 5000:5000 --name flask-container my-flask-app  
Проверить работу: curl http://localhost:5000
