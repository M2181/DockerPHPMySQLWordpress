# DockerPHPMySQLWordpress

Wordpress structured to work on two Virtual Machines.
- Virtualization envirovement is VirtualBox.
- Virtual Machines are Ubuntu Server 20.10 with preinstalled Docker.
- Networking is on bridge mode.
- First VM contains Docker with php:7.4.15-apache-buster
- Second VM contains Docker with mysql:latest

Containers are launched with commands:

**sudo docker run -v config-file.cnf:/etc/mysql/conf.d -v ~/test/wp:/var/lib/mysql --env-file=env -p 3306:3306 testi5**

**sudo docker run -p 80:80 -v ~/test/wordpress:/var/www/html --env-file=env testi7**
