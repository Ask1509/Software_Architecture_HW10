
# Архитектура ПО. Семинар 10. Структура приложения с пользовательским интерфейсом и базой данных

## Разработка архитектуры мессенджера
С приложением будут работать два типа пользователей: администратор, запускающий и останавливающий сервер, и некоторое количество людей, подключающихся к этому серверу, пишущих сообщения, и завершающих работу с сервером, отключившись от него.

По факту будет даже не одно приложение, а два (сервер и клиент), взаимодействующие друг с другом.

![Usecase diagram](/img/page01.png)


На следующей иллюстрации отображен полный цикл работы приложений:

![Flow diagram](/img/page02.png)


Клиентскую и серверную части реализуем по модели MVC: это будет удобно для дальней разработки, например переходу от использования JFrame в UI к более продвинутым инструментам проектирования пользовательского интерфейса.

Обе части соеденим посредством Socket.

И при написании кода воспользуемся развернутой диаграммой классов, которая, если не считать деталей реализации, практически полностью описывает наши приложения:

![Class diagram](/img/page03.png)


## Работа с приложением
Администратор запускает сервер (файл `Server`), указывая его адрес и порт, который он будет слушать.

![Administrator screen](/img/server01.png)

К серверу подключаются пользователи (в том числе и сам Администратор может выступать в двух ролях), при помощи клиентской части (файл `Client`), работают с программой:

![First client screen](/img/client01.png)

![Second client screen](/img/client02.png)



Отключаются от сервера:

![First client screen](/img/client04.png")

![Second client screen](/img/client03.png)

![Administrator screen](/img/server02.png)

Администратор останавливает сервер, завершив работу приложения.

## Возможные улучшения
Подключение приложения к базе данных на сервере для регистрации/авторизации пользователей, а также хранения истории сообщений.
Переход в UI от JFrame к JavaFX, или связке HTML, CSS, Typescript.
Или даже реализация на другом языке, но это будет уже совсем другая история…

![Class diagram from future](/img/BigScreen.png)
