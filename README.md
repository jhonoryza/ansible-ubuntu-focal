# Ansible Ubuntu Focal Fossa (20.04) LTS #

## Requirement

* Install ansible di local pc.
* Update host file : ``/hosts`` ini untuk konfigurasi ip address server yang akan digunakan dan user yg digunakan
* Update alokasi resource ``vars/allocation.yml`` dan ``vars/global.yml``
* Tambahkan local's public key ``~/.ssh/id_rsa.pub`` ke dalam remote server's di folder: ``~/.ssh/authorized_keys``
* Jalankan command di remote server : ``sudo apt-get install python3-minimal aptitude python-apt``

## Cara Pakai

``ansible-playbook -i hosts <role>.yml``

Kumpulan list role yang bisa digunakan :
* common
* nginx
* php
* mysql
* redis

contoh:
``ansible-playbook -i hosts nginx.yml``

or ``ansible-playbook -i hosts lemp.yml`` untuk install semua role.

## Versi yang Terinstall

| Software   | Version |
| ---------- | ------- |
| nginx      | 1.17.10 |
| MySQL      | 8.0     |
| PHP        | 8.0     |
| redis      | latest  |
| phpmyadmin | 5.2.0   |

## akses phpmyadmin
buka browser [http://ip-address/MySQL_DB/phpMyAdmin/](http://ip-address/MySQL_DB/phpMyAdmin/)
