Hастройка логина в GitHub через SSH Key на Linux
1. ssh-keygen
2. cat <путь/название публичного ключа>
3. Копируем ключ и вставляем в гитхаб.

---
git remote -v  узнать сейчас подключен удаленный репозиторий по https или по ssh

git remote set-url origin git@github.com:galichy79/Memory.git перенастроить подключение на ssh

### Общая информация по подключению через ssh

МЫ рекомендуем вам создать ключи SSH и передать ваш публичный ключ любой системе, доступ к которой вам нужен. Это более безопасно и поможет сэкономить время в долгосрочной перспективе.
[Настройка ключей SSH](https://www.digitalocean.com/community/tutorials/how-to-set-up-ssh-keys-on-ubuntu-20-04)


https://www.youtube.com/watch?v=OwWZ5JgJneQ&t=201s

---

Запушить существующий репозиторий


…or push an existing repository from the command line SSH

git remote add origin git@github.com:galichy79/gal.git

git branch -M main

git push -u origin main 

---

git merge origin/main

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

[Создание нового ssh ключа и добавление его в ssh-agent](https://docs-github-com.translate.goog/en/authentication/connecting-to-github-with-ssh/generating-a-new-ssh-key-and-adding-it-to-the-ssh-agent?platform=linux&_x_tr_sl=auto&_x_tr_tl=ru&_x_tr_hl=ru)






[google/docsy](https://github.com/google/docsy)

[Docsy](https://www.docsy.dev/about/)

[rubyschool урок 20 установка и работа с Git
установка Ungit на Windows]()

[3.1 Ветвление в Git официальная справка](https://git-scm.com/book/ru/v2/%D0%92%D0%B5%D1%82%D0%B2%D0%BB%D0%B5%D0%BD%D0%B8%D0%B5-%D0%B2-Git-%D0%9E-%D0%B2%D0%B5%D1%82%D0%B2%D0%BB%D0%B5%D0%BD%D0%B8%D0%B8-%D0%B2-%D0%B4%D0%B2%D1%83%D1%85-%D1%81%D0%BB%D0%BE%D0%B2%D0%B0%D1%85)

[Gitnuro Git multiplatform client ](https://github.com/JetpackDuba/Gitnuro)