`gem install rails`
`rails new myapp`
`cd myapp`
`bin/rails s`
`rails generate controller home index`

# Создание приложения Rails

### Prerequisites
- Ryby
- SQLite3
- Nose.js
- [Yarn](https://classic.yarnpkg.com/lang/en/docs/install/#debian-stable)

- [https://guides.rubyonrails.org/](https://guides.rubyonrails.org/)

- rbenv
- [https://github.com/nodejs/node-gyp](https://github.com/nodejs/node-gyp)
- [https://rubygems.org/](https://rubygems.org/)

```
gem update --system
```
```
rails new AskIt -T -j webpack --css bootstrap --skip-hotwire
```
### Запускаем приложение

```
bin/dev
```
### Глава 2
[Мини приложение](https://www.softcover.io/read/db8803f7/ruby_on_rails_tutorial_3rd_edition_russian/toy_app)

---

REST-архитектуры, предпочитаемой Rails.

миниатюрное будет состоять из пользователей и связанных с ними микросообщений (like a Twitter).



---

- [Аутентификация в rails-приложениях через facebook, vkontakte](https://habr.com/ru/articles/142128/)

- [Irwi — Wiki в Rails-приложениях](https://habr.com/ru/articles/68235/)

-[Организация верстки в rails приложении с помощью гема rails_ui_kit](https://habr.com/ru/articles/254463/)

- [Стартап Glide для создания мобильных приложений из Google-таблиц](https://habr.com/ru/companies/vdsina/articles/520238/)

- [Разработка Rails приложений с использованием Hotwire](https://habr.com/ru/articles/681266/)

- [Аутентификация в Rails-приложениях с помощью Devise. Часть 1: базовая настройка](https://habr.com/ru/articles/208056/)
- [devise](https://github.com/heartcombo/devise)

- [Ловушка CMS](https://habr.com/ru/articles/229099/)

- [Stimulus 1.0: скромный JavaScript фреймворк для HTML, который у вас уже есть](https://habr.com/ru/articles/346132/)

### Установка ninja

`ninja --version`

`sudo apt-get install ninja-build`

### Rails-style-guide

[Rails-style-guide(RU)](https://github.com/arbox/rails-style-guide/blob/master/README-ruRU.md)

[https://sustainable-rails.com/](https://sustainable-rails.com/)

[gem dotenv how to use video](https://www.youtube.com/watch?v=JvhIoQjezRs)

[как создать приложение на старых рельсах](https://www.youtube.com/watch?v=1hoLN25sfJk)


[Rails для продвинутых: организация кода (Иван Немытченко)](https://www.youtube.com/watch?v=Ae19vpQ14jw)

[Environment Variables with Ruby on Rails](https://www.youtube.com/watch?v=O-aDLsuNTRY&t=440s)

[Ruby on Rails #33 Gem Dotenv - alternative to Rails credentials](https://www.youtube.com/watch?v=AFdd3VdKA8o&t=381s)

[Learn Ruby on Rails - Full Course](https://www.youtube.com/watch?v=fmyvWz5TUWg&t=262s)

[Ruby on Rails 6.* - Урок 11. Аутентификация через социальные сети. OAUTH. Часть 1.](https://www.youtube.com/watch?v=YvGxAt9OVeE)

[Environment Variables (.env) with Ruby](https://www.youtube.com/watch?v=KRzt_vTZaLQ)

[Конфигурация веб-приложения. Новый подход](https://www.youtube.com/watch?v=lUo5z1HhwcY)

[Ruby on Rails Tutorial (3-е издание)](https://www.softcover.io/read/db8803f7/ruby_on_rails_tutorial_3rd_edition_russian/beginning)

[Фронтенд на рельсах (почти) без JS](https://habr.com/ru/articles/590381/)

Hotwire является собирательным названием для семейства библиотек.
На октябрь 2021 года было всего две библиотеки: Turbo и Stimulus.

Turbo заменит уже существующую Turbolinks.
Библиотека Turbo разделена на несколько частей, где каждая служит единой цели - доставить в ваше приложение HTML, отрисованный на сервере, с разницей в том, когда и как это делается:

    Turbo Drive - тот старый добрый Turbolinks, с которым мы знакомы. 

    Turbo Frames - “отдельные” фреймы, которые могут быть загружены асинхронно и обновлены, когда сервер возвращает фрейм с тем же id. 

    Turbo Streams - другой тип фреймов, который обновляется в результате HTTP запроса или с помощью сервера через Websocket. 

    Turbo Native - обёртка вашего “турбированного” веб-приложения, которая интегрирует его в мобильное приложение.


[500+ вопросов на собеседовании по Ruby](https://itvdn.com/ru/blog/article/ruby-500-questions)

[Співбесіда з Ruby. 500+ запитань для Junior, Middle, Senior](https://dou.ua/lenta/articles/interview-questions-ruby-developer/)

```
bundle install
yarn install
```

[The Asset Pipeline](https://guides.rubyonrails.org/asset_pipeline.html)

[Dart Sass for Rails](https://github.com/rails/dartsass-rails)

---

[Поиск по сайту](https://pagefind.app/)

[Adding search to a static Jekyll site using pagefind ](https://jay.gooby.org/2023/07/04/adding-search-to-a-static-site-using-pagefind)

[Conner Jensen](https://www.youtube.com/@connerjensen8170/videos)

---

[clearbnb](https://www.youtube.com/playlist?list=PLS6F722u-R6LoD3UN0EE_cKtHVG2EWn0t)


# Заметки
`bin/webpack-dev-server`

#### Обновить зависимости
Если в package.json имеется сторока 
"dependencies": {

}, то используется npm

`npm update`




# Методы оплаты 

[pay](https://github.com/pay-rails/pay) Есть Fake processor used for generic trials without cards, free subscriptions, testing, etc.