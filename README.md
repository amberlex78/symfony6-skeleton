# Symfony 6 Skeleton Application

Only for DEV, not for production!

**Docker + PHP 8.1 + MySQL 8 + Nginx + XDebug 3.1.2 + Symfony 6 + Bootstrap 5 + Adminer**

## Setup

See hostnames in the `.env` file.

Add to `/etc/hosts` file lines:
```
127.0.0.1 symfony6-skeleton.test
127.0.0.1 adminer.test
```

Clone and run the `docker-compose`:
```
git clone https://github.com/amberlex78/symfony6-skeleton
cd symfony6-skeleton
cp project/.env project/.env.local
make init
make setup
sudo chown -R $USER:$USER project/
```

### Database

See database connection parameters in the `.env` file.

Database connection in the `project/.env.local` file:
```
DATABASE_URL="mysql://symfony:symfony@mysql:3306/symfony?serverVersion=8.0"
```

### Seed
If you want to populate the database with data, run the command:
```
make db-dul
```
(schema:drop, schema:update, fixtures:load)
## Docker

### Up

Docker up `docker-compose up -d` or:
```
make up
```

### Down

Docker down `docker-compose down --remove-orphans` or:
```
make down
```

See all command in `Makefile` file.

## Access to site

Front:
```
http://symfony6-skeleton.test
```
