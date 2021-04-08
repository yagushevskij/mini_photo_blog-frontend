# Сервис микроблогов v0.0.2

## Описание
Pet проект, созданный для закрепления навыков разработки с использованием нативного JavaScript.
Галерея самых рейтинговых фото зарегистрированных пользователей, а так же возможность создания личной страницы с уникальным URL.

![alt tag](https://imgur.com/D6zNytA "Скриншот главной страницы приложения")​
![alt tag](https://imgur.com/m8hSpHk "Скриншот пользовательской страницы")​
Демо: [https://mesto.turbomegapro.ru/](https://mesto.turbomegapro.ru/)

## Особенности
- Приложения на одной странице (SPA);
- Работа с REST API (https://github.com/yagushevskij/mini_photo_blog-api);
- Модульный ES6 JavaScript код с использованием классов;
- Асинхронная обработка запросов c помощью promice и async/await;
- Сборка проекта с использованием webpack;

## Основные функции
- Фотогалерея на основе grid masonry layout в стиле pinterest. Размеры превью изображений рассчитываются на основе пропорций и рейтинга элемента с ровной интерполяцией исходя из настроек;
- Страницы пользователей имеют собственные уникальные url вида http://site.ru/user/username (http://localhost:8080/?user=username для dev сборки)
- Валидация пользовательских данных с выводом кастомных сообщений;
- Асинхронная загрузка изображений с выводом прелоадера во время загрузки и обработкой ошибок;
- Регистрация/авторизация на сайте с использованием cookies;
- Добавление/удаление карточек пользователями и голосование;
- Настраиваемая пагинация (по скроллу или по клику);

## Требования к системе
- Node.js;
- менеджер пакетов NPM;
- nginx или apache с модулем mod_rewrite для корректной работы функции пользовательских страниц в режиме production. Пример конфигурации для nginx:
> rewrite ^/user/(.*)$ /?username=$1 last;

## Установка
1) Скопируйте репозиторий;
2) Установите модули командой
>npm install
3) Для запуска локального сервера в режиме develop с поддержкой hot reload:
>npm run dev
Для сборки проекта в режиме production:
>npm run build

## Используемые технологии
Git, Webpack, JavaScript, html, css, BEM, nginx