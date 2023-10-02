#Урок 10. Структура приложения с пользовательским интерфейсом и базой данных (паттерн Repository)
# Блок 1 (семинар 10)

### **Задание:**

a. Спроектировать пользовательский интерфейс (web-SPA, native mobile), основные компоненты (подключение робота, управление помещениями, расписание работы, сервисное обслуживание робота, история уборок), https://www.figma.com/  или https://app.diagrams.net/.

b. Спроектировать доменную модель, в виде текста Домен – атрибуты.

c. Спроектировать сценарии (Use case)(подключение, выбор помещения, программы уборки, настройка расписания, просмотр статистики..), в виде Актор – Прецедент (из первой лекции).

d. Спроектировать слой  API Gateway (mobile, web), сформировать REST запросы: GET, POST, PUT, DELETE ([https://swagger.io](https://swagger.io/)).

* (дополнительно, по желанию) Разработать REST контракты API между компонентами и сгенерировавать (автоматически на ресурсе [https://swagger.io](https://swagger.io/)) код на разных языках программирования.

e. Спроектировать компоненты бизнес-логики и связать их API Gateway с применением паттерна BFF https://app.diagrams.net/.

f. Определить состав информации для кеширования на уровне приложения пользователя, API Gateway, уровня бизнес-логики и уровня репозитория. Список.

g. Спроектировать ER модель (https://www.dbdesigner.net/), запросы в БД и уровень хранения данных (СУБД).

### Домашнее задание:

Доработать пункты задания Блока 1: a, b, c, d, e, f, g.

Инструменты:

- **https://www.figma.com/**
- **https://app.diagrams.net/**
- **https://www.dbdesigner.net/**
- **[https://swagger.io](https://swagger.io/)**

**Текст задания**

На семинаре с преподавателем проектируется приложение управления роботом пылесосом. Задание разбито на 3 части. На 10 семинаре разбирается UI приложения (пример приведен снизу). UserCase диаграмма и структура данных. Студент должен сформировать документы, согласно разобранных схем. Приветствуется добавление деталей или кейсов(решаемых задач).

![Снимок экрана 2022-12-06 в 17.35.01.png](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/809097fd-dbf0-4b32-8159-248667289038/%D0%A1%D0%BD%D0%B8%D0%BC%D0%BE%D0%BA_%D1%8D%D0%BA%D1%80%D0%B0%D0%BD%D0%B0_2022-12-06_%D0%B2_17.35.01.png)

Задание выполняется для приложения управления роботом пылесосом(подробно разбирается на семинаре)

Задание 1. Разработать полную ERD домена сервера в https://www.dbdesigner.net/.

Задание 2. Сделать графический интерфейс для мобильного приложения и десктоп( WEB)(разобрано на семинаре)

Задание 3. Разработать USERCASE диаграмму управления роботом пылесосом

Задание 4. Сформировать REST запросы: GET, POST, DELETE. Инструмент проектирования API контракта [https://swagger.io](https://swagger.io/).

**Критерии оценивания домашнего задания**

Основная цель семинара обобщить полученные знания и навыки. Сформировать максимальный пакет документов для разработки системы управления роботом пылесосом.

**Оценка “Отлично”-** разработана подробная ERD диаграмма с полным погружением в тематику. Логичный интерфейс приложения. Разработано API для связи клиента, сервера и робота. Подробная USERCASE диаграмма. Работа обязательно сдана через GitHub.

**Оценка “Хорошо” –** диаграмма содержит мелкие недочеты. Отсутствует информация, которая должна быть (нет данных о модели робота или владельце). Интерфейс явно реализует не все функции доступные роботу пылесосу. Отсутствует один из документов: ERD, UI, USERCASE.

**Оценка “Удовлетворительно” –** диаграмма слишком простая и не содержит связей. Диаграммы явно не отражают суть решаемой задачи. Отсутствуют два документа из трех(USERCASE, ERD, UI).

**Оценка “Не сдано” -** сдано что-то другое (ДЗ для другого урока, непонятно что, заглушка, просьба отсрочить проверку работы и т.п. без кода)

**Пример идеального решения домашнего задания**

USERCASE диаграмма

![Снимок экрана 2022-12-06 в 17.35.12.png](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/65628cae-ef00-4f1b-85d5-96996e2cb232/%D0%A1%D0%BD%D0%B8%D0%BC%D0%BE%D0%BA_%D1%8D%D0%BA%D1%80%D0%B0%D0%BD%D0%B0_2022-12-06_%D0%B2_17.35.12.png)

ERD диаграмма

![Снимок экрана 2022-12-06 в 17.35.20.png](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/0f10c27b-cbd6-49f6-910a-1bb3eb5d9d05/%D0%A1%D0%BD%D0%B8%D0%BC%D0%BE%D0%BA_%D1%8D%D0%BA%D1%80%D0%B0%D0%BD%D0%B0_2022-12-06_%D0%B2_17.35.20.png)

UI

![Снимок экрана 2022-12-06 в 17.35.40.png](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/934863e6-7466-49ca-8107-d9d4cc2ea5e4/%D0%A1%D0%BD%D0%B8%D0%BC%D0%BE%D0%BA_%D1%8D%D0%BA%D1%80%D0%B0%D0%BD%D0%B0_2022-12-06_%D0%B2_17.35.40.png)

![Снимок экрана 2022-12-06 в 17.36.38.png](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/79cd784f-6380-4e08-b611-b00a268045a6/%D0%A1%D0%BD%D0%B8%D0%BC%D0%BE%D0%BA_%D1%8D%D0%BA%D1%80%D0%B0%D0%BD%D0%B0_2022-12-06_%D0%B2_17.36.38.png)

API
