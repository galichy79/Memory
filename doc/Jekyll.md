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

[jelyllrb.com](https://jekyllrb.com/)

[kiviok site](http://kiviok.github.io/2016/09/16/using-webstorm-for-jekyll/)

[kivi ok video про сайт на Jekyll](https://robotkang-cc.translate.goog/19620.html?_x_tr_sl=auto&_x_tr_tl=ru&_x_tr_hl=ru)

Сайт на Jekyll. #1 Рисование каркаса сайта
___
[Создание статических сайтов с Jekyll Andrew Burgess](https://code.tutsplus.com/ru/articles/building-static-sites-with-jekyll--net-22211)

[Веб хостинг AWS](https://aws.amazon.com/ru/websites/)

[Размещение статического сайта на AWS](https://aws.amazon.com/ru/getting-started/hands-on/host-static-website/)

[netlify хостинг первый месяц бесплатно](https://www.netlify.com/)

- [Bundler](https://bundler.io/v2.4/man/bundle-exec.1.html)



[Skeleton](http://getskeleton.com/)

Material disign google

[Параметры конфигурации Jekyll](https://jekyllrb-com.translate.goog/docs/configuration/options/?_x_tr_sl=auto&_x_tr_tl=ru&_x_tr_hl=ru)

[Liquid](https://shopify.github.io/liquid/)

Посмотреть примеры с ликвид.

[Темы в Jekyll](https://jekyllrb-com.translate.goog/docs/themes/?_x_tr_sl=auto&_x_tr_tl=ru&_x_tr_hl=ru)

[Гитхаб репозиторий к статьям kiviok](https://github.com/kiviok/jekyllcosmo)


[Список блогов на Jekyll](https://github.com/jekyll/jekyll/wiki/Sites)
---
