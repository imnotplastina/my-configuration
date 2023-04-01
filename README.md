### For local dev:
* Make directory for docker
```
mkdir ./storage/docker
```
* Copy .env.example
```
cp .env.example .env
```
* Add host user to .env
```
echo UID=$(id -u) >> .env
echo GID=$(id -u) >> .env
```
* Run docker services
```
docker-compose up -d --build
```
* Install composer dependencies
```
docker-compose exec app composer install
```
* Install npm dependencies
```
npm i
```
* Run artisan serve
```
docker-compose exec app php artisan serve --host 127.0.0.1 --port 8876
```
* Migrate database
```
docker-compose exec app php artisan migrate --seed
```

