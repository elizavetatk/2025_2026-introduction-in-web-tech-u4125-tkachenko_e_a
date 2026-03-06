University: [ITMO University](https://itmo.ru/ru/)  
Faculty: [FICT](https://fict.itmo.ru)  
Course: [Введение в веб технологии](https://itmo-ict-faculty.github.io/introduction-in-web-tech/)  
Year: 2025/2026  
Group: U4125  
Author: Tkachenko Elizaveta Andreevna  
Lab: Coursework  
Date of create: 05.03.2026  
Date of finished:  


# Отчет по курсовой работе: "Создание персонального сайта с использованием MkDocs"

## Ход работы  

**Этап 1: Подготовка и установка**
- Установка MkDocs, Python, тему Material  
- Создание нового проекта: my-personal-site

**Этап 2: Настройка конфигурации (mkdocs.yml)**

- Настроены site_name, site_description, site_author, site_url
- Добавлена тема Material с features
- Выбрана цветовая схема: primary indigo, accent pink
- Настроена навигация по разделам: Главная, О себе, Проекты, Контакты, Достижения

**Этап 3: Создание контента**
Созданы 5 страниц в папке docs
1. index.md - Главная  
2. about.md - О себе  
3. projects.md - Проекты  
4. contacts.md - Контакты  
5. achievements.md - Достижения  

**Этапы 4 и 5**
1. Добавлено изображение на страницу Главная  
2. Протестирована функция поиска  
3. Настроена цветовая палитра  
4. Настроен футер в mkdocs.yml (добавлены copyright, иконки соцсетей и ссылки)  
5. Для оформления проектов и контактов используется admonition (!!!tip "" и другие)  

**Этап 6: Публикация**

- Локальное тестирование: `mkdocs serve`
- Сборка статических файлов: `mkdocs build`
- Настройка GitHub Actions для автоматической публикации
- Сайт опубликован на GitHub Pages

Сайт: https://elizavetatk.github.io/2025_2026-introduction-in-web-tech-u4125-tkachenko_e_a/
