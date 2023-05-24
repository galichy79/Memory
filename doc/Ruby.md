

[Конспект курса по руби Романа Пушкина](https://github.com/krdprog/rubyschool-notes/blob/master/one-by-one/lesson-01.md)
---

- [Узнайте бандлер получше. Показана графическая схема зависимостей.](https://habr.com/ru/company/engineyard/blog/172807/)

require - Этот метод подгружает руби-код из внешнего источника. require ищет по абсолютному пути, ему обяательно надо указать, относительно чего искать:

[В чем разница между require и require_relative. Справочник по руби](http://ruby.qkspace.com/ruby-v-chem-raznitsa-mezhdu-require-i-require_relative)

Последняя конструкция слишком громоздкая (дополнительная переменная, пара строк кода) и некрасивая (точки, слеши, склейка строк) . Поэтому придумали reuquire_relative. Он делает то же самое: ищет файл для подключения относительно той папки, в которой лежит основная программа (а не той, в которой мы программу запускаем):

[How To Install Ruby on Rails version 7 on Manjaro Linux with RVM](https://medium.com/@faturr/how-to-install-ruby-on-rails-version-7-on-manjaro-linux-with-rvm-7a0cde49f415)