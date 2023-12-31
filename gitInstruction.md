# Инструкция по работе с контролем версий Git

## Что такое Git и зачем он нужен?
Git - это консольная утилита, для отслеживания и ведения истории изменения файлов, в вашем проекте. Чаще всего его используют для кода, но можно и для других файлов. Например, для картинок - полезно для дизайнеров.

С помощью Git-a вы можете откатить свой проект до более старой версии, сравнивать, анализировать или сливать свои изменения в репозиторий.

Репозиторием называют хранилище вашего кода и историю его изменений. Git работает локально и все ваши репозитории хранятся в определенных папках на жестком диске.

Так же ваши репозитории можно хранить и в интернете. Обычно для этого используют три сервиса:

- GitHub

- Bitbucket

- GitLab

Каждая точка сохранения вашего проекта носит название коммит (commit). У каждого commit-a есть hash (уникальный id) и комментарий. Из таких commit-ов собирается ветка. Ветка - это история изменений. У каждой ветки есть свое название. Репозиторий может содержать в себе несколько веток, которые создаются из других веток или вливаются в них.

## Установка
Основой интерфейс для работы с Git-ом является консоль/терминал. Это не совсем удобно, тем более для новичков.

Установим сам Git.

* Windows. Проходим по ссылке, выбираем под вашу ОС (32 или 64 битную), скачиваем и устанавливаем.

* Для Mac OS. Открываем терминал и пишем:

#Если установлен Homebrew
brew install git

#Если нет, то вводим эту команду. 
git --version
#После этого появится окно, где предложит установить Command Line Tools (CLT).
#Соглашаемся и ждем установки. Вместе с CLT установиться и git

* Linux. Открываем терминал и вводим следующую команду.

#Debian или Ubuntu
sudo apt install git

#CentOS
sudo yum install git

## Настройка
Вы установили себе Git и можете им пользоваться. Давайте теперь его настроим, чтобы когда вы создавали commit, указывался автор, кто его создал.

Открываем терминал (Linux и MacOS) или консоль (Windows) и вводим следующие команды.

## Установим имя для вашего пользователя

#Вместо <ваше_имя> можно ввести, например, Grisha_Popov
#Кавычки оставляем
git config --global user.name "<ваше_имя>"

## Теперь установим email. 
Принцип тот же.
git config --global user.email "<адрес_почты@email.com>"

## Создание репозитория
Теперь вы готовы к работе с Git локально на компьютере.

Создадим наш первый репозиторий. Для этого пройдите в папку вашего проекта.
#Для Linux и MacOS путь может выглядеть так /Users/UserName/Desktop/MyProject
#Для Windows например С://MyProject
cd <путь_к_вашему_проекту>

Инициализация/создание репозитория
- git init

Теперь Git отслеживает изменения файлов вашего проекта. Но, так как вы только создали репозиторий в нем нет вашего кода. Для этого необходимо создать commit.

## Добавим все файлы проекта в нам будующий commit
git add .
## Или так
git add --all

## Если хотим добавить конкретный файл то можно так
git add <имя_файла> 

## Теперь создаем commit. Обязательно указываем комментарий.
## И не забываем про кавычки
git commit -m "<комментарий>"

Отлично. Вы создали свой первый репозиторий и заполнили его первым commit.

## Процесс работы с Git
Не стоит после каждого изменения файла делать commit. Чаще всего их создают, когда:

- Создан новый функционал

- Добавлен новый блок на верстке

- Исправлены ошибки по коду

- Вы завершили рабочий день и хотите сохранить код


Это поможет держать вашу ветки в чистоте и порядке. Тем самым, вы будете видеть историю изменений по каждому нововведению в вашем проекте, а не по каждому файлу.

## Итог
Это первая вводная статья по утилите Git. Здесь мы рассмотрели:

- Как его устанавливать

- Как его настраивать

- Как инициализировать репозиторий и создать commit через консоль

Существует ещё множество команд, например:

git help # справка по всем командам
git clone
git status
git branch
git checkout
git merge
git remote
git fetch
git push
git pull


Для облегчения обучения, оставлю вам ссылку на бесплатный тренажер по Git.

https://learngitbranching.js.org/

## Работа с удаленными репозиториями (GitHub)

Чтобы сделать это, войдите в личный кабинет GitHub и найдите кнопку Create repository. Если у вас уже есть готовый репозиторий на локальном компьютере, его можно импортировать на платформу. Сделать это поможет кнопка Import repository .


По кнопке Create repository вы попадете на страницу создания репозитория. Здесь нужно ввести его название и дать краткое описание. Также важно выбрать, будет ли ваш репозиторий доступен другим пользователям GitHub. Публичные могут видеть все, а приватные — только их создатели и члены команды. Но что бы вы ни выбрали, помните: изменить настройки приватности можно будет и позже.

Также сервис предложит вам создать репозиторий с README-файлом.

README-файл — это технический документ с подробным описанием вашего проекта.
Добавить его особенно важно тем, кто хочет сделать IT-проект публичным. Именно README — первое, что читают другие пользователи в чужих репозиториях, поэтому его стоит написать.

Еще среди пунктов можно выбрать тип лицензии. Он помогает разработчикам защитить свои права и показать, в каких целях другие пользователи могут пользоваться их кодом на GitHub. Сегодня мы создаем пробный репозиторий, поэтому лицензия не нужна.


Когда вы заполните все пункты и проставите нужные галочки, жмите Create repository. Дальше вы попадете на страницу готового репозитория. Первый шаг сделан — можно начать работу с проектом на GitHub!

## Разбираемся в функциях GitHub
Теперь наполним репозиторий файлами, а заодно узнаем, как пользоваться базовыми возможностями GitHub. Чтобы добавить документы в репозиторий, кликните Add file на его странице. Здесь можно сразу создать файл или загрузить его с локального компьютера.


Заранее создаем нужный файл (или серию файлов) и выбираем его после клика по кнопке Choose your files на следующей странице. В полях ниже можно прописать название файла и дать краткий комментарий. По умолчанию сервис предложит добавить все это в главную ветку — main.

Ветка (branch) — это история работы над проектом со всеми изменениями и версиями.
Также вы можете переставить галочку и создать новую ветку.


После этого нажимаем Commit changes внизу. Теперь ваши файлы появятся в репозитории. Чтобы просмотреть их, теперь не нужно ничего скачивать. Достаточно просто кликнуть по названию файла в репозитории, и вы увидите его содержимое. Это удобно, когда нужно быстро посмотреть код в ветке.

Предположим, вы загрузили первую простенькую версию приложения. Чтобы работать над ней дальше и улучшать IT-проект, нужно будет редактировать файлы с кодом и загружать изменения на GitHub. Платформа позволяет делать это с помощью коммитов.

Коммит (commit) — это изменения в репозитории и его файлах.
Любые изменения в добавленных файлах, новые файлы, а также их удаление — все это коммиты. Давайте отредактируем наш первый загруженный файл, чтобы посмотреть, как все это работает в GitHub. Просто кликаем на него в репозитории, а дальше меняем наполнение прямо на странице. Ниже описываем изменения и жмем Commit changes.


Возвращаемся в репозиторий. На первый взгляд, мы просто сохранили наш первый файл в его новой версии, но при этом мы в любой момент можем посмотреть все старые. Для этого кликните по документу и найдите кнопку History сверху. Она покажет вам историю коммитов в файле с предыдущими версиями.


Чтобы посмотреть на конкретные изменения, кликните по номеру коммита справа — он выглядит как набор букв и цифр. Тогда программа подсветит то, что конкретно поменялось в коде по сравнению с последней версией.


При этом во время разработки вы, скорее всего, не обойдетесь одной веткой. Вторая может пригодиться, чтобы параллельно разрабатывать на облачной платформе другую версию приложения. Или вести совместную разработку с другими программистами.

Давайте создадим новую ветку. Это просто: на странице репозитория находим кнопку с названием основной ветки, кликаем и в строке поиска набираем имя новой ветки. Если такого названия еще не было, GitHub предложит создать ветку. Делаем это и получаем копию ветки main.


Переключимся на новую ветку — у нас это beta1. А потом снова зайдем в документ Первый файл.txt и создадим новый коммит. Теперь ветки main и beta1 отличаются — GitHub сразу сообщает об этом и предлагает сравнить их, а потом слить вместе.

На этом моменте вы можете продолжить параллельную разработку версий приложения или сделать Pull request.

Пул-реквест (pull request) — это слияние двух веток c различным наполнением. Если выполнить его, все изменения «перетекут» в главную ветку.
Предположим, что мы тестировали новый подход и поняли, что его можно добавлять в публичную версию IT-проекта, то есть ветку main. Тогда кликаем по кнопке Compare & pull request в уведомлении. На новой странице сверху можно будет выбрать ветки, которые вы хотите сравнить. Если они одинаковые, создать pull request будет нельзя.

В нашем случае ветки main и beta1 отличаются. А значит, составляем описание для запроса в окошке и жмем Create pull request.


Запрос отправлен. Теперь его должен посмотреть и принять владелец ветки main. Если права на нее у вас, вы получите уведомление во вкладке Pull requests. На странице запроса его можно принять или отклонить.


Для примера нажмем Merge pull request и Confirm merge, чтобы принять изменения. Теперь ветки слиты — об этом говорит фиолетовая отметка с надписью Merged. Если ветка beta1 больше не нужна, ее можно сразу удалить.

Также владелец репозитория с правами на основную ветку может заблокировать ее от изменений. Обычно, если ветка не закрыта, GitHub сам подсказывает об этом и предлагает защитить ее. Для этого просто жмем на кнопку Protect this branch и выставляем нужные галочки. Наша, например, теперь всегда будет требовать Pull request перед слиянием. Но вы можете и вовсе закрыть ее от изменений, оставить только чтение.


Но и это еще не все. Мы уже подключались к аккаунту GitHub через локальный клиент Git. Важно помнить, что через него можно продолжать работать над репозиторием. Например, с помощью пушей.

Пуш (Push) — это функция Git, которая позволяет отправлять изменения через локальный клиент в удаленный репозиторий.
Также пользователь может создать полную копию репозитория с GitHub, чтобы скачать ее себе на компьютер. Эта функция так и называется — Clone.

Клон (Clone) — это копирование удаленного репозитория на локальный компьютер.
Чтобы клонировать репозиторий, зайдите на его страницу и найдите вверху зеленую кнопку Code. По клику на нее вы откроете меню копирования. Здесь можно скачать и zip-файл, но нас интересует полная копия. Поэтому выбираем нужный способ (HTML, ключ SSH или GitHub CLI) и копируем URL. Он скоро пригодится.

Дальше нужно открыть консоль Git Bash. Если вы еще не скачали программу, сделайте это по инструкции. А после введите в строку команду ниже:

- git clone <URL репозитория>

Вместо <URL репозитория> вставьте скопированный URL безо всяких скобочек. А после жмите Enter. Готово! Теперь вы можете работать с копией на локальном компьютере.


Рано или поздно ваш IT-проект будет готов увидеть свет. Когда это случится, вы сможете выпустить его первую рабочую версию — релиз.

Релиз (release) — это готовое приложение и одноименная страница с его исходным кодом на GitHub.
Чтобы создать релиз, зайдите на страницу репозитория и найдите Create a release справа. На новой странице можно будет указать его заголовок и описание, а также выбрать ветку, которую вы представите как готовое приложение. Дальше останется только нажать Publish release и сохранить все это.


Готово! Теперь вы умеете пользоваться всеми базовыми функциями GitHub :)

## Изучаем открытые проекты
GitHub нужен не только для работы со своими проектами. Эта платформа — отличный инструмент, чтобы анализировать проекты других разработчиков и учиться у них. Например, изучить код известных приложений. На GitHub вы найдете и VK, и Telegram, и Avito, и еще много других популярных сервисов.

Серфить по поиску GitHub просто. Найдите строку вверху сайта и введите ключевое слово. Например, название приложения, которое вы хотите поискать. В выпадающем меню выберите настройки поиска All GitHub. И не забудьте отсортировать результаты — это поможет сохранить время.

Советуем отмечать через Star проекты, которые вам нравятся. Это поможет GitHub создать для вас ленту рекомендаций в разделе Explore, где вы будете чаще встречать интересные репозитории.

Иногда разработчики находят интересные репозитории и пользуются наработками в них, чтобы создать свой IT-проект на базе уже готового кода. В этом случае им помогает функция Fork.

Форк (Fork) — это копирование чужого репозитория в свой.
С помощью форка разработчик может клонировать чужой проект, чтобы разрабатывать его дальше отдельно от родительского. Также многие «форкают» проекты, потому что хотят предложить изменения его владельцу. Тогда разработчик копирует проект, вносит правки и отправляет запрос на слияние.

Чтобы «позаимствовать» репозиторий, он должен быть открытым и доступным для Fork. Если вы нашли такой, зайдите на его страницу и кликните по кнопке Fork в верхнем правом углу.

Обратите внимание: не все проекты доступны для этой функции — владелец может закрыть свой репозиторий от форка, даже если тот относится к публичным. 

Описание инструкции взял с ресурса https://habr.com/ru/articles/541258/

# Домашнее задание №2

Для домашнего задания необходимо было создать 4 разные ветки, сделать в кждой по 4 комита и конфликт при merge.

Скрин конфликта:
![![DomZadanie_conflict.jpg](DomZadanie_conflict.jpg)]

Изменение на гитхабе

