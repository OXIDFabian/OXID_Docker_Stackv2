**_OXID Docker Stack_**
---
_THIS IS A PRIVATE PROJECT AND NOT OFFICALY SUPPORTED BY OXID ESALES_

**Stack overview**

* Webserver container (httpd or nginx)
* PHP container (7.0 - 7.3)
* DB container (MySQL or MariaDB)
* Memcached container
* Mailhog container (default port: 8025)
* Adminer container (default port: 8080)

**Quickstart**

install docker and docker-compose

download or git clone this repository

customize the .env file

* run `docker-compose up -d` to start the container stack

* open `http://localhost/` in your browser



**data persistence**

all data (_www_ and _mysql_) will be stored in the _data_ directory in your project folder

**XDEBUG**

set Debug Port in PHPStorm to 9001

Preferences -> Languages & Frameworks -> PHP -> Debug -> xdebug
