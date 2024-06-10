# Ansible

## Обновите конфигурацию ssh

Измените файл `~/.ssh/config` добавив следующуюконфигурацию:
```Host vagrant-vm
  HostName 127.0.0.1
  User vagrant
  Port 2222
  IdentityFile /home/yu/Vagrant/.vagrant/machines/default/virtualbox/private_key
  UserKnownHostsFile /dev/null
  StrictHostKeyChecking no
  IdentitiesOnly yes
  LogLevel FATAL
  PubkeyAcceptedKeyTypes +ssh-rsa
  HostKeyAlgorithms +ssh-rsa
  KexAlgorithms +diffie-hellman-group1-sha1
```
После обновления `~/.ssh/config`, подключайтесь с помощью:

```
ssh vagrant-vm
```


### Запускаем плейбук при помощи утилиты `ansible-playbook`
```
ansible-playbook install_ruby_with_openssl.yml
```

##### 1 Делаем инвентори файл hosts.txt

``` # hosts.txt
[default]
linux1 ansible_host=127.0.0.1 ansible_user=vagrant ansible_ssh_private_key_file=/home/yu/Vagrant/.vagrant/machines/default/virtualbox/private_key  
```

##### 2 Делаем пинг
```
ansible -i hosts.txt default -m ping
```
##### Подтвердить изменение ключа хоста:
```
ssh-keygen -f "/home/yu/.ssh/known_hosts" -R "[127.0.0.1]:2222"
```
#### Создаем конфиг файл
`ansible --version`
`mkfile ansible.cfg`
``` # ansible.cfg
[defaults]
host_key_checking = false # все эти параметры брать на сайте ансибл
inventory         = ./hosts.txt
```
Теперь при вводе команды не надо писать -i
##### Новая команда для вызова Ansible ping
```
ansible all -m ping
```
### Если inventory указан в конфигурационном файле Ansible то его не нужно указывать при запуске плейбука
```
ansible-playbook install_yarn.yml

### Плейбук для установки nvm
---
- name: Install NVM (Node Version Manager)
  hosts: all
  become: yes
  tasks:
    - name: Ensure curl is installed
      package:
        name: curl
        state: present

    - name: Download NVM installation script
      get_url:
        url: "https://raw.githubusercontent.com/nvm-sh/nvm/master/install.sh"
        dest: "/tmp/install_nvm.sh"

    - name: Run NVM installation script
      command: "/bin/bash /tmp/install_nvm.sh"
      args:
        creates: "{{ ansible_user_dir }}/.nvm"  # Проверяем, что NVM не установлено

    - name: Source NVM script in bashrc
      lineinfile:
        dest: "{{ ansible_env.HOME }}/.bashrc"
        line: "source $HOME/.nvm/nvm.sh"
        state: present
      when: ansible_shell_type is defined and ansible_shell_type == 'bash'  # Проверяем, что используется оболочка bash

    - name: Source .bashrc to activate NVM
      command: "source $HOME/.bashrc"
      args:
        executable: "/bin/bash"
      when: ansible_shell_type is defined and ansible_shell_type == 'bash'  # Проверяем, что используется оболочка bash

###  Плейбук для установки Ярн

---
- name: Install Yarn
  hosts: all
  become: yes
  tasks:
    - name: Download Yarn key
      shell: "curl -sS https://dl.yarnpkg.com/debian/pubkey.gpg | sudo apt-key add -"
      become_user: root

    - name: Add Yarn repository
      apt_repository:
        repo: "deb https://dl.yarnpkg.com/debian/ stable main"
        state: present
      become_user: root

    - name: Update apt package cache
      apt:
        update_cache: yes

    - name: Install Yarn package
      apt:
        name: yarn
        state: present