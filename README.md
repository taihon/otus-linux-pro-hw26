## OTUS Administrator Linux. Professional ДЗ №26: Динамический веб

**Задание**

Для выполнения домашнего задания используйте методичку
https://docs.google.com/document/d/1Q5Hqwq8dqsdRSDWA_bQKc1GsCx4wxi1c/edit?usp=share_link&ouid=104106368295333385634&rtpof=true&sd=true

Варианты стенда:

- nginx + php-fpm (laravel/wordpress) + python (flask/django) + js(react/angular);
- nginx + java (tomcat/jetty/netty) + go + ruby;
  можно свои комбинации.

Реализации на выбор:

- на хостовой системе через конфиги в /etc;
- деплой через docker-compose.

Для усложнения можно попросить проекты у коллег с курсов по разработке

К сдаче принимается:

- vagrant стэнд с проброшенными на локалхост портами
- каждый порт на свой сайт
- через нжинкс

Формат сдачи: Vagrantfile + ansible

**_Решение_**

Для развёртывания инфраструктуры используется vagrant, ansible и docker. Выбран вариант с пробросом портов 8081-8083 на хост-машину. Стенд построен из nginx+wordpress-fpm, node.js, django. Nginx осуществляет проксирование соединений на дополнительные веб-приложения.
Для запуска необходимо выполнить команды:
```
vagrant up
ansible-playbook playbook.yml
```