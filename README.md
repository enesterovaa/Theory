# Theory
## Что такое клиент-серверная архитектура ##

Клиент – локальный компьютер на стороне виртуального пользователя, который выполняет отправку запроса к серверу для возможности предоставления данных или выполнения определенной группы системных действий.

Сервер – очень мощный компьютер или специальное системное оборудование, которое предназначается для разрешения определенного круга задач по процессу выполнения программных кодов. Он выполняет работы сервисного обслуживания по клиентским запросам, предоставляет пользователям доступ к определенным системным ресурсам, сохраняет данные или БД.

База данных (БД) — это совокупность данных, которая включает в себя определённые правила, принципы хранения, описания и управления данными. Эти данные относятся к какой-то предметной области и позволяют решать множество конкретных задач.

Клиент-серверная архитектура - это взаимодействие двух программных продуктов между собой, один из которых выступает в качестве сервера, а другой соответственно в качестве клиента. Клиент посылает запрос, а сервер отвечает ему. Сервер запрашивает данные в базе данных

## Что такое HTTP и HTTPS ##

Это протоколы передачи данных. HTTPS не является отдельным протоколом передачи данных, а представляет собой расширение протокола HTTP с надстройкой шифрования; передаваемые по протоколу HTTP данные не защищены, HTTPS обеспечивает конфиденциальность информации путем ее шифрования; HTTP использует порт 80, HTTPS — порт 443.

Аббревиатура HTTP расшифровывается как HyperText Transfer Protocol, "протокол передачи гипертекста". По сути, он является набором правил, которые знает клиент и знает сервер и они между собой общаются по этим правилам.

HTTP - широко распространнеый протокол передачи данных, изначально предназначенный для гипертекстовых документов, то есть документов, которые могут содержать ссылки, позволяющие организовать переход к другим документам.
 
	
  Модель TCP/IP.
		1 уровень - канальный (link layer)
		2 уровень - межсетевой (internet layer). Протокол IP работает здесь.
		3 уровень - транспортный (transport layer). Протокол TCP работает здесь. А также UDP.
		4 уровень - прикладной (application layer). Протокол HTTP работает здесь. А также FTP, NTP, DHCP, PING, Telnet.

Client = User agent. Клиентами могут быть: браузер, Postman, Jmeter, Java app, Soap UI.

## HTTP методы ##

Метод HTTP - последовательность из любых символов, кроме управляющих и разделителей, указывающая на основную операцию над ресурсом. Обычно метод представляет собой короткое английское  слово, записанное заглавными буквами. Название метоода чувствительно к регистру.

Сервер может использовать любые методы, не существует обязательных методов для сервера или клиента. 
	
	GET - запрашивает представление ресурса. Запросы с использованием этого метода могут 
	
	только извлекать данные.
	
	HEAD - запрашивает ресурс так же, как и метод GET, но без тела ответа.
	
	POST - используется для отправки сущностей к определенному ресурсу. Часто вызывает 
	
	изменение состояния или какие-то побочные эффекты на сервере.
	
	PUT - заменяет все текущие представления ресурса данными запроса.
	
	DELETE - удаляет указанный ресурс.
	
	CONNECT - устанавливает "туннель" к серверу, определенному по ресурсу.
	
	OPTIONS - используется для описания параметров соединения с ресурсом.
	
	TRACE - выполняет вызов возвращаемого тестового сообщения с ресурса.
	
	PATCH - используется для частичного изменения ресурса.


## HTTP статус коды сервера ##

Код ответа (состояния) HTTP показывает, был ли успешно выполнен определенный HTTP запрос. Коды сгруппированы в 5 классов:

	1. 100-199 Информационные, которые не несут особо никакой полезной нагрузки.
	
	2. 200-299 Успешные. Например, отправляя GET запрос, 200 код в ответе говорит о том, 
	
	что запрос прошел и все хорошо, после числа 200 идет OK. 
	
		Отправляя POST запрос, мы в ответе увидим 201 и после этого сообщение CREATED и это бы говорило, 
		
		что все успешно создано.
		
	3. 300-399 Перенаправленные. Например, если мы увидим 300 код, это будет означать, что URL, по которому 
	
	мы делаем запрос, был изменен навсегда и теперь нужно идти по другому URL.
	
	4. 400-499 Клиентские ошибки. Означают, что на стороне клиента что-то было сделано не так.
	
		400 - имеет сообщение BAD REQUEST, означает, что что-то в запросе вы написали не так, 
		
		нужно что-то исправить. 
		
		401 код будет указывать, что вам нужно будет выполнить аутентификацию перед тем, 
		
		как получить доступ к ресурсу.
		
		404 NOT FOUND. Говорит, что там, куда вы пытаетесь обратиться, нет ресурса. Скорее всего, 
		
		вы неправильно указали путь до ресурса.
		
		405 говорит о том, что вы использовали неверный метод, например, отправили GET запрос вместо POST, 
		
		а POST там не обслуживается.
		
	5. 500-599 Серверные ошибки. 
	
		500 - что-то на сервере произошло, из-за чего ваш запрос был некорректно обработан или 
		
		что-то на сервере поломалось.
		
		504 - говорит о том, что есть тайм-аут. То есть сервер очень долго обрабатывал информацию 
		
		и вы не получили ответа в какие-то разумные строки.


## Что такое ядро браузера ##

Ядро браузера можно разделить на две части: движок рендеринга (инженер макета или движок рендеринга) и движок JS. 

Он отвечает за получение содержимого веб-страницы (HTML, XML, изображения и тд), организацию инфрмации 

(направление, добавление CSS и тд) и расчет режима отображения веб-страницы, а затем вывод ее на монитор и принтер. 

Разница в ядре браузера будет по-разному интерпретировать синтаксис веб-страницы, поэтому эффект рендеринга 
	
будет другим. Ядра браузера можно разделить на пять типов: Trident, Gecko, Presto, Webkit, Blink.


## Какие браузеры какие ядра используют ##

Trider - проприетарный движок Microsoft Internet Explorer.

EdgeHTML - движок от компании Microsoft для ее браузера Microsoft Edge.Является ответвлением Trident.

Blink - движок браузера  Chromium, браузера Google Chrome с 28 версии, Microsoft Edge с 79 версии, 

Opera с 15 версии и Vivaldi. Он является ответвлением WebKit.

Gecko - открытый движок проекта Mozilla; используется в большом числе программ, основанных на коде Mozilla 

(браузер Firefox, почтовом клиенте Thuderbird, наборе программ SeaMonkey)

WebKit - движок для браузера Apple Safari, включенного в операционную систему Mac OS X, и браузера 

Google Chrome (до 2013). Встроен в библиотеку Qt (начиная с Qt 5.6 признан устаревшим).

KHTML - разработан в рамках проекта KDE, используется в браузере Konqueror и послужил основой для WebKit


## Что такое API ##

## Что такое эндпоинты ##

## URL (URI, URL, URN) ##

## Идемпотентные HTTP методы ##

## Безопасные HTTP методы ##

12. Идентификация, аутентификация, авторизация

13. Что такое IP

14. Что такое октеты в DNS

15. Что такое порт, сколько портов у Linux сервера

16. Уровни OSI

17. Хедеры HTTP запросов
