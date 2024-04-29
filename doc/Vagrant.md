### Vagrant
Vagrant дает быстрое развертывание среды разработки

Алексей Медов

(Vagrant - простой пример создания виртуальной машины в Virtualbox)[https://www.youtube.com/watch?v=-A0rwMtHdVo]

Утилита для автоматического поднятия серверов в вируальной машине с помощью конфигурационного файла, который называется Vagrantfile. Работает с VirtualBox VmWare Ansible и другими провайдерами. Box - преднастроенный образ операционной системы например: ubuntu/trusty64.

#### Создание и запуск

`vagrant init ubuntu/trusty64`
`vagrant up`
`vagrant provision #на ранее установленном боксе устанавливает ПО`


#### Подключение к созданной ВМ
`vagrant ssh-config #посмотреть параметры VS должна быть запущена`
`vagrant ssh default #подключиться к виртуальной машине`
можно устанавливать необходимые програмы через `sudo apt-get install`

`exit #закрыть подключение к ВМ`

#### Уничтожение ВМ
Находясь в папке с Vagrantfile пишем
`vagrant destroy`
`vagrant destroy -f #удаляет без подтверждения. Останавливает и удаляет`


(Vagrant)[https://app.vagrantup.com/ubuntu/boxes/trusty64]

(A Virtual Machine for Ruby on Rails Core Development)[https://github.com/rails/rails-dev-box]
(Using Vagrant for Rails Development)[https://gorails.com/guides/using-vagrant-for-rails-development]

---

### Для инициализации Varrant проекта

` vagrant init ubuntu/trusty64 #в корне проекта создается Vagrant file`

`rm -rf app #удалить папку app рекурсивно`

#### Сохранение виртуальной машины 

Виртуальную машину можно поместить в ждущий режим.  `vagrant suspend` (возобновление работы — `vagrant up`).
#### Выключение ВМ
Выключить виртуальную машину можно с помощью `vagrant halt`.

#### Удаление ВМ
 `vagrant destroy -f`.

 ### Установка rbenv
 `sudo apt install rbenv`

 (How to Create and Manage Virtual Machines with the Vagrant Command Line Tool)[https://www.freecodecamp.org/news/create-and-manage-virtual-machines-with-vagrant/]

 ### Как установить libvips-dev в Ubuntu / Debian

 `sudo apt update`
 `sudo apt install libvips-dev`