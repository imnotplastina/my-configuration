# Laravel & Docker 
Basic docker configuration for Laravel project :v:

## TODO
- [ ] Make makefile 
- [ ] Configuration for production

## Usage
### Development
1. Make directory for docker `mkdir ./storage/docker`
2. Copy .env.example `cp .env.example .env`
3. Run docker services `docker-compose up -d --build`
4. Install composer dependencies `docker-compose exec app composer install`

> Make sure that everything works
1. Run artisan serve `docker-compose exec app php artisan serve --port 8876`
2. Migrate database `docker-compose exec app php artisan migrate --seed`

### Production

soon... :shipit:
