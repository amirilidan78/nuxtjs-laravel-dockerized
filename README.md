# Laravel, Nuxtjs Dockerized 

### Project structure

#### services folder 
services folder contains Mongo, Mysql, Nginx ,Redis ,Supervisor docker files and config files.

#### src folder 
src folder contains Laravel and Nuxt js applications . 


### Services 
Nginx config service nginx.conf is located at /services/nginx, Laravel application is served on api.example-domain.com ,Nuxt application is served on example-domain.com, You can access laravel application via example-domain.com/api-proxy for cors policy. 
You can change Mongo db configs from .env file in /services/mongo folder.
You can change Mysql db configs from .env file in /services/mysql folder.
Redis dockerfile is located at /services/redis you can set password and change configs for security purpose.
Supervisor runs artisan schedule:work & artisan queue:work , it`s config file are located at /services/supervisor/conf.d.

### Src
Nuxt js dockerfile is located at /src/nuxt, Node:14 image is used for creating image.
Laravel dockerfile is located at /src/laravel, Php:8 image is used for creating image.