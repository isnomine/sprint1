**Задание 1**


*Уровень 1. Проектирование*

После анализа исходного приложения, видно, что это простое SPA приложение, разработанное на react.
Приложение предоставляет функционал загрузки, просмотра и оценки изображений. Авторизации пользователя, а так-же управление его профилем.


Так как приложение достаточно простое и использует один фреймворк то подходящим решением для разбивки на микрофронтенды будет - Module Federation.

*Уровень 2. Планирование изменений*

Исходный фронтенд был разделен на 4 микрофронтенда исходя из их бизнес логики

* auth - мифкрофронтенд отвечающий за регистрацию и авторизацию пользователя
* main - основвной микрофронтенд который подгружает другие. Содержит общие компоненты интерфейса
* profile - микрофронтенд отвечающий за профиль пользователя и его редактирование
* photos - микрофронтенд отвечающий за работу с фотографиями (загрузка, редактирование, оценка)

├───auth                        
│   └───src                     
│       ├───blocks              
│       │   ├───auth-form       
│       │   │   ├───__button    
│       │   │   ├───__form      
│       │   │   ├───__input     
│       │   │   ├───__link      
│       │   │   ├───__text      
│       │   │   ├───__textfield
│       │   │   └───__title     
│       │   └───login
│       ├───components
│       └───utils
├───main
│   └───src
│       ├───blocks
│       │   ├───content
│       │   ├───footer
│       │   │   └───__copyright
│       │   └───header
│       │       ├───__auth-link
│       │       ├───__logo
│       │       ├───__logout
│       │       ├───__user
│       │       └───__wrapper
│       ├───components
│       ├───contexts
│       ├───images
│       ├───public
│       ├───utils
│       └───vendor
│           └───fonts
├───profile
│   └───src
│       ├───blocks
│       │   └───profile
│       │       ├───__add-button
│       │       ├───__description
│       │       ├───__edit-button
│       │       ├───__image
│       │       ├───__info
│       │       └───__title
│       ├───components
│       └───utils
└───photos
    └───src
        ├───blocks
        │   ├───card
        │   │   ├───__delete-button
        │   │   │   ├───_hidden
        │   │   │   └───_visible
        │   │   ├───__description
        │   │   ├───__image
        │   │   ├───__like-button
        │   │   │   └───_is-active
        │   │   ├───__like-count
        │   │   └───__title
        │   ├───components
        │   ├───page
        │   │   ├───__content
        │   │   └───__section
        │   ├───places
        │   │   ├───__item
        │   │   └───__list
        │   └───popup
        │       ├───_is-opened
        │       ├───_type
        │       ├───__button
        │       │   └───_disabled
        │       ├───__caption
        │       ├───__close
        │       ├───__content
        │       │   └───_content
        │       ├───__error
        │       │   └───_visible
        │       ├───__form
        │       ├───__icon
        │       ├───__image
        │       ├───__input
        │       │   └───_type
        │       ├───__label
        │       ├───__status-message
        │       └───__title
        └───utils



**Задание 2**

https://drive.google.com/file/d/16EBxdBrPlmW4zqdCg0Q_DGIbxOGWSthS/view?usp=drive_link