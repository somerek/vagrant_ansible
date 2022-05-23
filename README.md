# Vagrand and ansible work
1.	Установить VirtualBox.
2.	Установить Vagrant.
3.	Создать виртуальную машину с помощью Vagrant'а со следующими характеристиками: CPU - 2 / RAM - 2 GB / HDD - 10 GB / OS - Debian 8/9.
4.	Настроить виртуальную машину через Vagrant provisioner ( Ansible ). Установить следующие пакеты:
-	Vim
-	Wget
-	Htop
-	Tmux
-	Php5.6
-	Nginx (Любая версия. Должен работать на 80 порту)
-	Apache2 (Должен работать на порту 8888)
5.	Написать скрипт на php. Достаточно вывода фразы "Hello World!", но можно и сложнее.
6.	Написать playbook для обновления php5.6 до php7.2.
7.	Создать публичный репозиторий на GitLab или GitHub. В репозиторий положить конфиг Vagrant'а и playbook provisioner'а, все прочие скрипты.
8.	Прислать ссылку на репозиторий.


May be need run
ansible-galaxy collection install community.general
