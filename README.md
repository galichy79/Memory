
Лучше когда база знаний будет в виде сайта.
---

[Д.С. Кулябов](https://yamadharma.github.io/ru/)
---


[github утилиты командной строки](https://yamadharma.github.io/ru/post/2021/08/04/github-command-line-utilities/)

sudo snap install gh

To authenticate, please run `gh auth login`.



Я склонировал репозиторий через фар. И открыл в руби майн.

config


Host github.com
        User git
        Hostname github.com
        PreferredAuthentications publickey
        IdentityFile /home/user/.ssh/id_rsa




[Hugo](https://gohugo.io/)

[Смотреть как огранизовано хранилище у Фернандо](https://github.com/android10
)

[Создание нового ssh ключа и добавление его в ssh-agent](https://docs-github-com.translate.goog/en/authentication/connecting-to-github-with-ssh/generating-a-new-ssh-key-and-adding-it-to-the-ssh-agent?platform=linux&_x_tr_sl=auto&_x_tr_tl=ru&_x_tr_hl=ru)

[Linux](/doc/Linux_mint.md)
=======

[Юриспруденция](/doc/%D0%AE%D1%80%D0%B8%D1%81%D0%BF%D1%80%D1%83%D0%B4%D0%B5%D0%BD%D1%86%D0%B8%D1%8F/%D0%AE%D1%80%D0%B8%D1%81%D0%BF%D1%80%D1%83%D0%B4%D0%B5%D0%BD%D1%86%D0%B8%D1%8F.md)
===

[Все разом](/doc/vse/vse.md)
===

Jekyll
---

Чтобы не ставить/обновлять гемы по-одиночке каджый раз используется бандлер(который сам является гемом). Работает это так: в Gemfile ты описываешь какие гемы тебе нужны. После чего запускаешь bundle install. Бандлер проходится по твоему Gemfile и устанавливает с помощью утилиты gem. Нужные гемы. А также сойдает файл Gemfile.lock, в котором описывает что, откуда и почему он поставил. Если сказать bundle update, то бандлер заглянет в файлы Gemfile b Gemfile.lock, проверит версии и установит гем последней доступной версии. Не обновит, а поставит новый. Старая версия тоже останется. 
bundle exec означает выполнить нечто с помощью гема из файа Gemfile.lock/ В рельсе все следует запускать через bundle.exec. Это исключит конфликт версий.

Про Gem:
Gem это есмъ библиотека, скомпанованная определённым образом. То есть это набор кода (модули, классы и тд), которые решают некоторую задачу.
Утилита gem занимается тем, что управляет этими библиотеками. Например 'gem install colorize' скачает с интернета библиотеку (далее "гем") в каталог, доступный для твоих программ (конкретное место зависит от настроек и способа установки Рубина). После чего ты сможешь в своём коде написать require 'colorize' и пользоваться методами, которые данный гем предоставляет. Гем может требовать для установки другие гемы.

Про Bandler:
Чтобы не ставить/обновлять гемы по-одиночке каждый раз, люди написали Бандлер (который сам является гемом). Работает это так: в Gemfile ты описываешь какие гемы тебе нужны (каких версий, где взять и прочее...). После чего запускаешь bundle install Бандлер проходит по твоему Gemfile и устанавливает (с помощью утилиты gem) нужные гемы, а также создаёт файл Gemfile.lock, в котором описывает что, откуда и почему он поставил. Это важный файл! храни его в репозитории.
Если сказать bundle update, то бандлер заглянет в файлы Gemfile и Gemfile.lock, проверит версии и установит гем последней доступной версии. Внимание! не обновит, а поставит новый! То есть старая версия останется.
Здесь мы приходим к команде bundle exec. Эта команда означает: выполнить нечто с помощью гема из файла Gemfile.lock. Внимание! в рельсе всё (пока не взматереешь) следует запускать через bundle exec! Это исключит конфликт версий. Например: bundle exec rspec, bundle exec rails db:migrate и тд.

Про Рельсу:
Посмотри в каком-либо рельсовом проекте bin/rails, там обычный рубиновый код: require_relative '../config/boot'
Смотрим в config/boot.rb: require 'bundler/setup' Вот тут подключается гем Bundler и далее (можно посмотреть по исходникам) вызывается Bundler.setup, который, в свою очередь, смотрит в файлы Gemfile и Gemfile.lock и подключает указанные библиотеки (с помощью require), после чего методы оных библиотек становятся доступны в проекте. Кстати, Рельса сама является гемом, точнее набором гемов.

[Смотреть как организована система хранения у него](https://github.com/android10)

[Bundler](https://bundler.io/v2.4/man/bundle-exec.1.html)
---

[Узнайте бандлер получше. Показана графическая схема зависимостей.](https://habr.com/ru/company/engineyard/blog/172807/)

require - Этот метод подгружает руби-код из внешнего источника. require ищет по абсолютному пути, ему обяательно надо указать, относительно чего искать:

[В чем разница между require и require_relative. Справочник по руби](http://ruby.qkspace.com/ruby-v-chem-raznitsa-mezhdu-require-i-require_relative)

Последняя конструкция слишком громоздкая (дополнительная переменная, пара строк кода) и некрасивая (точки, слеши, склейка строк) . Поэтому придумали reuquire_relative. Он делает то же самое: ищет файл для подключения относительно той папки, в которой лежит основная программа (а не той, в которой мы программу запускаем):

sudo apt-get update 

[jelyllrb.com](https://jekyllrb.com/)

[kiviok site](http://kiviok.github.io/2016/09/16/using-webstorm-for-jekyll/)

[kivi ok video про сайт на Jekyll](https://robotkang-cc.translate.goog/19620.html?_x_tr_sl=auto&_x_tr_tl=ru&_x_tr_hl=ru)

Сайт на Jekyll. #1 Рисование каркаса сайта
___
[Создание статических сайтов с Jekyll Andrew Burgess](https://code.tutsplus.com/ru/articles/building-static-sites-with-jekyll--net-22211)

[Веб хостинг AWS](https://aws.amazon.com/ru/websites/)

[Размещение статического сайта на AWS](https://aws.amazon.com/ru/getting-started/hands-on/host-static-website/)

[netlify хостинг первый месяц бесплатно](https://www.netlify.com/)



[Skeleton](http://getskeleton.com/)

Material disign google

[Параметры конфигурации Jekyll](https://jekyllrb-com.translate.goog/docs/configuration/options/?_x_tr_sl=auto&_x_tr_tl=ru&_x_tr_hl=ru)

[Liquid](https://shopify.github.io/liquid/)

Посмотреть примеры с ликвид.

[Темы в Jekyll](https://jekyllrb-com.translate.goog/docs/themes/?_x_tr_sl=auto&_x_tr_tl=ru&_x_tr_hl=ru)

[Гитхаб репозиторий к статьям kiviok](https://github.com/kiviok/jekyllcosmo)

[Работа с компилятором GCC C++ в линукс](https://www.youtube.com/watch?v=IqCQOlci6mE)


___



[Как настроить VS Code для увеличеия продуктивности](https://techrocks.ru/2019/03/31/vs-code-customization/)




Вы можете использовать средство миграции Sass для автоматического обновления ваших таблиц стилей для использования math.div()и  list.slash().

sudo apt install npm

sudo npm install -g sass-migrator

sudo sass-migrator division **/*.scss



Писать сайт для Проявки на базе Bootstrap верстка современного сайта за 45 минут


[Що таке є гривня та які її перспективи в У](https://economics.novyny.live/finance/chto-takoe-e-grivna-i-kakovy-ee-perspektivy-v-ukraine-66700.html)

Смотреть Джордана Питерсона

为自由开路者，不可使其困顿于荆棘。 ...…

Пусть не запутается в терниях тот, кто прокладывает путь к свободе. ... 
---

[Сайт китайца откуда взята эта цитата](https://robotkang-cc.translate.goog/19620.html?_x_tr_sl=auto&_x_tr_tl=ru&_x_tr_hl=ru)

Создание документов в маркдаун

[Bootstrap](https://getbootstrap.com/)

[Bootstrap верстка современного сайта за 45 минут!](https://www.youtube.com/watch?v=46q2eB7xvXA&t=99s)

[Конспект курса по руби Романа Пушкина](https://github.com/krdprog/rubyschool-notes/blob/master/one-by-one/lesson-01.md)
---

[Трудові відносини під час воєнного стану](https://ua.korrespondent.net/articles/4550159-bez-vlasnoho-bazhannia-trudovi-vidnosyny-pid-chas-voiennoho-stanu)



