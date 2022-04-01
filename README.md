## Quick Start
Copy .env.example to .env, and execute following commands.
~~~
docker-compose up -d
docker-compose exec api.z3 composer install
docker-compose exec api.z3 php artisan key:generate
docker-compose exec api.z3 php artisan migrate
docker-compose exec api.z3 php artisan storage:link
~~~


## Cautions

Nginx operates within the directory, so if you can't cd to that directory from the nginx user then it will fail 