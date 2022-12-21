# Docker-WP(LATEST)-MariaDB-Adminer

> Simple docker env, for local development.

## About build:

- composer (insert plugins in mount drive plugins)
- docker-compose hold all wp (themes and plugins external) and db files localy on your host mashine
- example 'env/files' config for wp and db services

## How start

> Before run you should install docker on your PC.

> [How install docker](https://docs.docker.com/get-docker/), official docs

Checkout docker already installed, just run in terminal and you get docker version info

```
docker -v
```

So if you solve docker install problems you can run this build in your ide or terminal:

```
docker-compose up -d
```

And now checkout in browser:

[Adminer](http://localhost:8080)

[Wodpress Installation: Default Port](http://localhost:80)

> MariaDB, you should wait few seconds after run, check log messages.

> Before wordpress installation checkout db access with Adminer.

---

## How unlock permission

You can add root access for your user

```
sudo chown -R [user-name]:www-data /path/to/your/local/folder
```

> Add full permission for your user, use command as root (sudo).

> -R flag (recursive run).

> Warning it breaks workflow as admin in cms.

---

## How return default permission

```
sudo chown -R www-data /path/to/your/local/folder
```

> This will return all back, use command as root (sudo).

> -R flag (recursive run).

---

## But for better permission config use security plugins:

[All In One WP Security & Firewall](https://wordpress.org/plugins/all-in-one-wp-security-and-firewall/), official wordpress plugin

> Already include in composer.json
