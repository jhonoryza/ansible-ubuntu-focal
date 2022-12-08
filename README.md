# Ansible Ubuntu Focal Fossa (20.04) LTS #

## Requirement

* Install ansible di local pc. [cara install](https://docs.ansible.com/ansible/latest/installation_guide/intro_installation.html).
* Update host file : ``hosts`` ini untuk konfigurasi ip address server yang akan digunakan dan user yg digunakan
* Tambahkan local's public key ``~/.ssh/id_rsa.pub`` ke dalam remote server's di folder: ``~/.ssh/authorized_keys``
* Update variable yang terdapat di folder vars jika diperlukan.

## Cara Pakai

run command di local:
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
| phpmyadmin | latest   |

## akses phpmyadmin
buka browser [http://ip-address/phpmyadmin](http://ip-address/phpmyadmin)

## akses adminer
buka browser [http://ip-address/adminer](http://ip-address/adminer)
