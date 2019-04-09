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

if you want to install **PE**, **EE**, **ERP** module or the **B2B** module copy your credentials to the auth.json file

* run `docker-compose up -d` to start the container stack

* to keep track of the shop installation enter the following command 
`docker-compose logs -f php`

* open `http://localhost/` in your browser


**OXID admin credentials**

> User: `admin`

> Password: `admin`

**data persistence**

all data (_www_ and _mysql_) will be stored in the _data_ directory in your project folder

**XDEBUG**

set Debug Port in PHPStorm to 9001

Preferences -> Languages & Frameworks -> PHP -> Debug -> xdebug


**Unit tests**

How to execute the Unit tests.

Starting point of each action is the shop root directory. The shop root directory is the place where are the folders source/ and vendor/ are located.  
Be aware to execute the tests in the context of the container.

1. Adapting the test configuration file
    1. Open _test_config.yml_
    1. Search for: `shop_tests_path: tests`
    1. Replace with: `shop_tests_path: vendor/oxid-esales/oxideshop-ce/tests`

1. Restore the directory Setup
    1. Rename the folder `_Setup` to `Setup`.

1. Executing the tests
    1. Navigate into the _vendor/bin_ directory
    1. execute the command: `php runtests`
