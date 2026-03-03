University: [ITMO University](https://itmo.ru/ru/)  
Faculty: [FICT](https://fict.itmo.ru)  
Course: [Введение в веб технологии](https://itmo-ict-faculty.github.io/introduction-in-web-tech/)  
Year: 2025/2026  
Group: U4125  
Author: Tkachenko Elizaveta Andreevna  
Lab: Lab2  
Date of create: 03.03.2026  
Date of finished:  

Лабораторная работа №2
"CI/CD для Docker приложения"
Описание
Это вторая лабораторная работа по настройке CI/CD пайплайна для автоматической сборки, публикации и деплоя Docker образа из первой лабораторной работы.

Ход работы:  
Настройка CI/CD пайплайна с GitHub Actions:  
1. Подготовка проекта:  
- Скопировала файлы из первой лабораторной (app.py, requirements.txt, Dockerfile)  
- Создала аккаунт на Docker Hub  
- Создала новый репозиторий на Docker Hub  
2. Настройка GitHub Actions:  
- Создала папку .github/workflows/ в корне проекта  
- Создала файл docker-build.yml с пайплайном  
3. Настройка секретов:  
- В настройках GitHub репозитория добавила секреты:  
DOCKER_USERNAME - мой логин на Docker Hub (elizavetatk)  
DOCKER_PASSWORD - мой токен доступа Docker Hub (здесь сначала возникла ошибка из-за того, что выбрала не тот вариант при создании токена - нужен "Read & Write")  
4. Тестирование пайплайна:  
- Сделала коммит и пуш в main ветку  
- Проверила выполнение пайплайна в разделе Actions  
сначала возникла ошибка из-за некорректности отступов в файле yml, исправила и сделала новый  
- Убедилась, что образ появился в Docker Hub  
- Проверила логи выполнения каждого шага  

Все скриншоты приложу в папку
