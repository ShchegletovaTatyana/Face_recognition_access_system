﻿# Face Control

Проект **"Face control"** выполнен студентами группы _18МАГ ИАД_ в рамках курса "Проекты ИАД", магистерская программа "Интеллектуальный анализ данных", Факультет Информатики, Математики и Компьютерных наук, Высшая школа экономики. &copy;2020

### **Состав участников:**
* _Масленникова Елизавета_
* _Канатов Николай_
* _Горская Ксения_
* _Корнева Татьяна_
* _Коробков Никита_
* _Кузнецова Екатерина_

#### Преподаватель: 

**Михаил Владимирович Бацын**, 

_кандидат физико-математических наук, доцент кафедры прикладной математики и информатики, ведущий научный сотрудник Лаборатории Алгоритмов и Технологий Анализа Сетевых Структур_

# Описание проекта

Текущие способы контроля сотрудников на большом предприятии имеют несколько недостатков: 
* Бумажный документооборот;
* «Тяжелое» обновление известной базы данных;
* Сложности с привлечением новых сотрудников;
* Большие временные затраты;
* Слабый контроль сторонних работников (outsourcing)
 
**Цель нашего проекта:** создание масштабируемого решения контроля доступов сотрудника на промышленных предприятиях с гибким интерфейсом для работы с базой данных. 

В результаты работы нашей команды мы планируем создать **Web-приложение** с простым масштабируемым интерфейсом для легкого обновления базы сотрудников **с возможностью детектирования и идентификации сотрудников по изображению лица** при помощи специальной системы видеонаблюдения.

**Камеры**, находящиеся на территории всего предприятия **в режиме онлайн идентифицируют и отслеживают всех людей в конкретной зоне**. Планируется, что если система заметит посторонних или сотрудников без доступа к данной территории, или вообще не сможет идентифицировать лицо – **автоматически поднимается тревога на пульт охраны**.
Дополнительно система ведет статистику и записывает перемещения всех сотрудников для облегчения процесса мониторинга. 
Также **web-приложение** позволяет быстро и легко добавлять новых или же заводить сторонних сотрудников в систему.


### Распределение работы внутри команды:
* Масленникова Елизавета – ответственная за **систему идентифицирования сотрудников** на видео-трансляции в режиме онлайн; разработка, ревью кода и поддержка части проекта на **Python**.

* Коробков Никита – разработка **системы идентифицирования сотрудников**; разработка, ревью кода и поддержка части проекта на **Python**; помощь в разработке **backend-а для web-приложения**.

* Корнева Татьяна - разработка, ревью кода и поддержка части проекта на **Python**; помощь в разработке **дизайна для frontend-а**; ответственная за **еженедельные отчеты**.

* Канатов Николай – ответственный за **web-приложение**; разработка, ревью кода и поддержка **web-интерфейса приложения**.

* Горская Ксения - разработка, ревью кода и поддержка **web-интерфейса приложения**; разработка **дизайна для frontend-а**.

* Кузнецова Екатерина - разработка, ревью кода и поддержка **web-интерфейса приложения**; ответственная за **структуру и наполнение БД сотрудников**.


### План работы

| **Дата** | | | | |
|:-------------:|:------------------:|:-----:|:-----:|:-----:|
| _22.01.2020_ | Выбор проекта | Краткое описание проекта | Определение цели и задач | Создание общего репозитория |
| _29.01.2020_ | Определение стека технологий | Исследование и выбор технологии детектирования лиц | Выбор подходящего проекта для backend части |  |
| _5.02.2020; 12.02.2020_ | **Python:** реализация детектирования лица и корпуса человека онлайн по видеостриму и слежение за ним | **Backend:** создание api проекта, настройка инфраструктуры проекта | **Frontend:** создание начального проекта, настройка взаимодействия с сервером | **БД:** Определение схемы используемой базы данных, заполнение тестовыми данными |
| _19.02.2020; 26.02.2020; 04.03.2020_ | **Python:** добавление персонализации человека по базе, создание интерфейса по добавлению, изменению и удалению человека для детектирования | **Backend:** основная разработка | **Frontend:** основная разработка | |
| _11.03.2020_ | **Python:** добавление логирования при детектировании, передача сигналов на бэкенд | Соединение и подключение всех частей проекта | | |
| _18.03.2020_ | Тестирование проекта | Косметические улучшения | | |
| _25.03.2020_ | Итоговая демонстрация готового продукта | | | |


### Недельный отчет 

В течение **1-ой недели** работы наша команда: 
* определилась с итоговым проектом, сформулировала основные цели и задачи работы, обосновали актуальность и необходимость проекта; 
* определила основные части итогового проекта; 
* распределила «зоны ответственности» между участниками;
* составила первоначальный план работы над проектом; 
* подготовила необходимую инфраструктуру – создали общий репозиторий с доступом всех участников команды, выложили всю необходимую информацию по проекту, договорились о правилах разработки, коммитах и ревью кода

В течение **2-ой недели** наша команда активно работала над *разработкой основной концепции проекта, выбором используемого стека технологий, сервисов и фреймворков*. 

* **Николай** занимался исследованием и подбором варианта проекта для написания серверной части приложения. По итогу его работы команда остановилась на **«.Net Core 2.2»**, так как это позволит работать и на Windows, и на Linux, что увеличить масштабность проекта. 
* **Екатерина** изучала сервисы для обмена данными между серверной частью приложения и камерами (программой распознавания на Python). Выбор был сделан в пользу сервиса **RabbitMq**. Екатерина также изучила основы работы с этим сервисом и его интеграции в проект.
* **Ксения** подбирала подходящий вариант реализации клиентской части приложения. В итоге был выбран фреймворк **«React.js»**, так как он является одним из самых популярных фреймворков, который постоянно поддерживается разработчиками и достаточно простой в реализации.
* **Никита** исследовал возможность применения классификатора на основе **«Каскадов Хаара»** (реализация из Python-OpenCV). Библиотека предоставляет уже обученные классификаторы для обнаружения лица и отдельных его черт. Для идентификации самого человека необходимо дообучить классификатор по некоторому исходному набору данных – датасету лиц людей. Но эксперименты показали плохую точность модели. При наличии в исходном датасете 2-х людей точность распознавания примерно 56%, а если люди похожи – то модель постоянно путается. Увеличение исходных фотографий каждого человека, добавления разных ракурсов только путает модель еще больше. При увеличении количества человек точность модели падает в разы. 
* **Елизавета** исследовала возможности библиотеки **face_recognition** на Python. Библиотека работает с использованием алгоритмов машинного обучения из **dlib**, написанных на С++. Для распознавания лиц используется **гистограмма направленных градиентов (HOG)**. Затем на каждом лице определяются основные опорные точки (face landmark estimation), по которым затем происходит его выравнивание (если на исходном изображении лицо как-то повернуто). Для идентификации лица далее используется предобученная нейронная сеть, которая переводит изображение в специальный эмбеддинг и находит наиболее близкое из всех имеющихся в базе. При тестировании модель показала высокую точность и быстродействие, поэтому команда приняла решение остановиться именно на ней.
* **Татьяна** изучала инструменты и их возможности для обработки потока видео-стрима. Выбор был сделан в пользу библиотеки **OpenCV**, так как она предоставляет простой интерфейс при использования его как для получения изображения, так и для дорисовки необходимых элементов на видео («квадратик» вокруг распознанных объектов). Также Татьяна изучала модели для распознавания человека (целиком). В итоге было принято решение использовать **TensorFlow Object Detection API**, так как их модели показывают высокую точность по детектированию объектов и при этом является достаточно простым в использовании. 

В течение 3-ей недели наша команда начала активно работать в направлении **разработки проекта, его составных частей, написания кода**. А именно:
* **Николай** создал темплейты проектов для серверной части, добавил базовые модели, а также принимал участие в разработке структуры базы данных для сотрудников.
* **Екатерина** добавила темплейт проекта для реализации бизнес логики и продолжает изучение библиотеки **RabbitMQ**, принципов ее использования и внедрения внутрь проекта на **C#**, а также принимала участие в разработке структуры базы данных для сотрудников.
* **Ксения** разработала **структуру базы данных** для сотрудников, добавила реализацию проекта бизнес логики и проекта для работы с самой базой данных.
* **Татьяна** реализовала интерфейс для приема видео потока с веб-камеры и добавила распознование облика человека при помощи **TensorFlow Object Detection API**. Код уже прошел ревью и доступен в бранче "python".
* **Елизавета** вместе с **Никитой** начали реализацию кода для распознования и идентификации лица человека при помощи **face_recognition** библиотеки. На данный момент готово рсапознование лица и слежение за ним в режиме онлайн по приходящему видеопотоку. Также **Елизавета и Никита** разрабатывают схему хранения банка фотографий людей для распознования, а также интерфейс для его обновления.

В качестве дальнейшей работы **Елизавета, Татьяна и Никита** продолжат работать над разработкой программы идентификации конкретного человека по известной базе на видео-потоке в режиме онлайн; **Николай** продолжит разработку backend части приложения; **Екатерина** подготовит заготовку кода для подключения сервиса **RabbitMQ** к проекту; **Ксения** займется созданием базы данных для проекта и ее заполнением тестовыми примерами.

P.S. Дефолтная **master** бранча создана для реализации уже собранных воедино компонентов программы. Пока же разработка кода происходит в отдельных бранчах:
* **develop/python** - распознование и идентификация человека на видео;
* **develop/backend** и **develop/frontend** - соответственно, для frontend и backend частей;
* **develop** - бранча для предварительной сборки проекта.

Также внутри всех бранчей установлены негласные правила между участниками команды по порядку прохождения ревью кода и мержинга.
