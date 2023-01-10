

[far2l  установил отсюда](https://github.com/elfmz/far2l)

[Видеоинструкция по установке far2l](https://www.youtube.com/watch?v=ropU_mXYbg4&t=118s)
---

Опиши этапы устновки программ в линукс на примере far2l

[far2l-deb](https://github.com/unxed/far2l-deb)

Удобно когда ты одним и тем же файловым менеджером пользуешься и на виндовз и на линукс

Nano
---
Ctrl + O - записать файл
Ctrl + X - выйти из редактора

[XnView скриншот части экрана в линукс](https://www.xnview.com/en/xnviewmp/)

[Видео о XnView time 3.39](https://www.youtube.com/watch?v=j-0vaRqF4xU)

![](/images/20230103_102743.jpg)

[Signal official site](https://signal.org/download/linux/)

Установить Signal
---

# 1. Install our official public software signing key
wget -O- https://updates.signal.org/desktop/apt/keys.asc | sudo apt-key add -

# 2. Add our repository to your list of repositories
echo 'deb [arch=amd64 signed-by=/usr/share/keyrings/signal-desktop-keyring.gpg] https://updates.signal.org/desktop/apt xenial main' |\
  sudo tee -a /etc/apt/sources.list.d/signal-xenial.list

# 3. Update your package database and install signal
sudo apt update && sudo apt install signal-desktop

[Как добавить изображение в маркдаун](https://denshub.com/ru/hugo-post-insert-image/)

Установить make
___

sudo apt update

sudo apt install make

[Подробная информация о пакете make утилита для управления компиляцией](https://www.gnu.org/software/make/)

[Gnu Make документация на русском](http://linux.yaroslavl.ru/docs/prog/gnu_make_3-79_russian_manual.html)

[Работа с компилятором GCC C++ в линукс](https://www.youtube.com/watch?v=IqCQOlci6mE)





