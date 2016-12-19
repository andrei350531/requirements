
## Andrei Kozyakov, group 350531. Business-requirements.

<a href="#Диаграммы">Смотреть диаграммы</a>

# Глоссарий
<table>
    <tr>
        <td>Термин</td>
        <td>Описание</td>
    </tr>
    <tr>
        <td name="fzLink">ФЗ</td>
        <td>Сокращение на: Фитнес-зал "Здоровак"</td>
    </tr>
    <tr>
        <td>Сайт</td>
        <td>Информационная система, предоставляющая пользователям сети Интернет доступ к своему содержимому и функционалу в виде упорядоченного набора взаимосвязанных HTML-страниц</td>
    </tr>
    <tr>
        <td>Пользователь</td>
        <td>Любой посититель сайта ФЗ</td>
    </tr>
    <tr>
        <td>Клиент</td>
        <td>Зарегестрированный и авторизированный на сайте ФЗ пользователь</td>
    </tr>
    <tr>
        <td>NodeJS</td>
        <td>Программная платформа, основанная на движке V8 (транслирующем JavaScript в машинный код), превращающая JavaScript из узкоспециализированного языка в язык общего назначения</td>
    </tr>
</table>

# 1. Введение
### &nbsp;&nbsp;&nbsp;&nbsp;Предметом разработки является сайт фитнес-зала "Здоровяк"(далее ФЗ) с системой онлайн-покупки абонементов и записи на занятия в зале.
Назначение сайта:
+ Предоставление информации о деятельности ФЗ;
+ Предоставление информации об услугах ФЗ;
+ Предоставление информации обо всех залах ФЗ, где проводятся зянятия;
+ Предоставление возможности регистрации клиентов
+ Предоставление возможности онлайн-покупки абонементов клиентами
+ Предоставление возможности онлайн-записи на занятия клиентами

Цель создания сайта:
+ Упростить работу с клиентами ФЗ
+ Предоставить информацию о ФЗ всем пользователями сети Интернет
+ Увеличение клиентской базы <a href="#user-content-fzLink">ФЗ</a>


# 2. Требования пользователя
## 2.1 Программные интерфейсы
&nbsp;&nbsp;&nbsp;&nbsp;Приложение должно иметь клиент-сервеную архитектуру. Верстка страниц, их стили и логика должны быть реализованы на HTML5, TypeScript и CSS. Серверная часть должна быть реализована на NodeJS. Для хранения данных должна использоваться база данных MySQL. Для безопасности данных пользователя сайт должен работать по протоколу HTTP2.0 и иметь доверенный SSL-сертификат.
Покупка абонементов пользователями должна быть реализована через систему `"WEBPAY.BY"`.

## 2.2 Интерфейс пользователя

#### Главная страница сайта
![Main Page](https://github.com/andrei350531/requirements/blob/master/images/mainPage.png?raw=true)
#### Страница авторизации клиента
![Login Page](https://github.com/andrei350531/requirements/blob/master/images/login.png?raw=true)
#### Страница регистрации клиента
![Registration Page](https://github.com/andrei350531/requirements/blob/master/images/registration.png?raw=true)
#### Страница галереи
![Gelery Page](https://github.com/andrei350531/requirements/blob/master/images/geleryUser.png?raw=true)
#### Страница услуг
![Services Page](https://github.com/andrei350531/requirements/blob/master/images/serviceUser.png?raw=true)
#### Страница услуг для клинета
![Services Client Page](https://github.com/andrei350531/requirements/blob/master/images/serviceClient.png?raw=true)
#### Страница контактов
![Contacts Page](https://github.com/andrei350531/requirements/blob/master/images/contacts.png?raw=true)
#### Страница профиля клиента
![Profile Page](https://github.com/andrei350531/requirements/blob/master/images/profile.png?raw=true)

## 2.3 Характеристики пользователя
&nbsp;&nbsp;&nbsp;&nbsp;Данный сайт будет подходить всем группам людей, желающим узнать о ФЗ или стать его клиентами, независимо от их образования, опыта и технической грамотности.

## 2.4 Предположения и зависимости
&nbsp;&nbsp;&nbsp;&nbsp; Приложение фукнцианирует при стабилоной работе сети Интернет у пользователя.

# 3. Системные требования
## 3.1 Функциональные требования
* Должно быть реализовано 8 страниц:
    * Главная страница;
    * Станица авторизации;
    * Страница регистрации;
    * Страница с галереей;
    * Станица с контактами;
    * Страница с услугами;
    * Страница профиля клиета;
    * Страница записи клинета на занятие;
* Главная страница должна содержать:
    * Ссылки на все страницы сайта;
    * Краткую информацию о ФЗ;
    * Небольшую часть изображений из галереи;
    * Контактную информацию;
    * Краткое описание самых популярных услуг
* Страница авторизации должна содержать:
    * Поля для авторизации клиента;
    * Ссылку на станицу регистрации;
* Страница регистрации должна содержать:
    * Поля для ввода информации о новом клинете;
* Страница с галереей должны содержать изображения всех залов ФЗ с краткой информацией о них
* Страница с контактами должна содержать:
    * Адрес и контактную информацию ФЗ;
    * Карту с расположеним ФЗ в виде метки
* Страница с услугами должна содержать информации о всех предоставляемых ФЗ услугах и ценах на них
* На странице услуг клинеты должны иметь ссылку на покупку абонемента на любую услугу через систему "WEBPAY.BY"
* Страница профиля должна быть доступна только клинетам ФЗ
* Страница профиля должна содержать:
    * Информацию о клинете;
    * Информацию о купленных абонементах;
    * Инофрмацию о записях на занятия;
    * Информацию об оставшемся количестве занятий по каждому из абонементов;
    * Ссылку на страницу записи на занятие
* Клинет должен иметь возможность отменить запись на занятие
* Страница записи на занятие должна быть доступна только клиентам.
* Страница для записи на занятие должна содержать:
    * Поле для выбора даты и времени занятия
    * Поле для выбора абонемента клинета
    * Залы ФЗ свободные для записи на выбранную дату и абонемент
* Пользователь должен получать информацию о любых ошибках сайта в виде сообщений
* Главная страница сайта должна всегда быть доступна к загрузке из кеша браузера пользователя

## 3.2 Нефункциональные требования
### 3.2.1 Атрибуты качества
* Загрузка сайта не должна занимать больше пяти секунд
* Графический дизайн должен быть отзывчивым как для мобильных, так и для десктопных устройств
* Запросы к базе данных должны заниматься не больше одной секунды




# <span name="diagrams">Диаграммы</span>

## Диаграмма классов
![Classes diagram](https://github.com/andrei350531/requirements/blob/master/schemas/classes.jpg?raw=true)


## Диаграмма последовательности (Переключение между страницами сайта)
![Sequence diagram](https://github.com/andrei350531/requirements/blob/master/schemas/sequence.jpg?raw=true)


## Диаграмма состояний (Запись клиента на занятие)
![States diagram](https://github.com/andrei350531/requirements/blob/master/schemas/states.jpg?raw=true)


## Диаграмма использования №1
![States diagram](https://github.com/andrei350531/requirements/blob/master/schemas/useCase1.jpg?raw=true)


## Диаграмма использования №2
![States diagram](https://github.com/andrei350531/requirements/blob/master/schemas/useCase2.jpg?raw=true)


## Диаграмма деятельности
![States diagram](https://github.com/andrei350531/requirements/blob/master/schemas/activity.jpg?raw=true)