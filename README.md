# laravel-nginx-fpm-mariadb-docker

- Laravel 7
- PHP 7.4
- MariaDb
- Docker

## Setup
###1. Add Repository
        
    git clone git@github.com:coliveira-ptc/laravel-nginx-fpm-mariadb-docker.git NameOfTheProject

###2. Change the name of the database, in these files:
docker-compose.yml

    MYSQL_DATABASE: laravel-nginx-fpm-mariadb-docker
      
.env 
    
    DB_DATABASE=laravel-nginx-fpm-mariadb-docker

##3. Run docker-compose
    docker-compose build && docker-compose up -d

##4. Give some permissions
sudo chgrp -R www-data storage bootstrap/cache
sudo chmod -R ug+rwx storage bootstrap/cache


###Test: http://localhost:7001/
