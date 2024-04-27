### Vagrant
Vagrant дает быстрое развертывание среды разработки

Алексей Медов

(Видеоролики)[https://www.youtube.com/@medov.alexey/videos]

Программа для автоматического поднятия серверов в вируальной машине с помощью конфигурационного файла, который называется Vagrantfile. Работает с VirtualBox VmWare Ansible и другими провайдерами. Box - преднастроенный образ операционной системы например: ubuntu/trusty64.

#### Создание и запуск

`vagrant init ubuntu/trusty64`
`vagrant up`
`vagrant provision #на ранее установленном боксе устанавливает ПО`


#### Подключение к созданной ВМ
`vagrant ssh-config #посмотреть параметры VS должна быть запущена`
`vagrant ssh default`
`exit #закрыть подключение к ВМ`

#### Уничтожение ВМ
Находясь в папке с Vagrantfile пишем
`vagrant destroy`
`vagrant destroy -f #удаляет без подтверждения. Останавливает и удаляет`


(Vagrant)[https://app.vagrantup.com/ubuntu/boxes/trusty64]

(A Virtual Machine for Ruby on Rails Core Development)[https://github.com/rails/rails-dev-box]
(Using Vagrant for Rails Development)[https://gorails.com/guides/using-vagrant-for-rails-development]