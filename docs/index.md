---
hide:
- navigation
---

# Getting Started

## MangaDB Api

MangaDB API is a powerful RESTful API designed to provide comprehensive data and metadata about manga volumes, series, staff, and publishers. With MangaDB API, you can collect and curate manga-related data, making it easier to build powerful applications and services for manga enthusiasts.

## How to access the API

If you want to use our live API, you can do so by accessing it at [https://api.manga-db.com].

Alternatively, if you want to contribute to our project's source code, follow the installation
guide below. You can also experiment with our endpoints by using our sandbox API URL,
[https://sandbox.manga-db.com], before diving into the code.

## Setting up the API on your machine

### Prerequisites
Before proceeding with the installation, ensure that you have Docker installed in your system.
You can install the latest version of Docker by following the instructions given in [the official Docker documentation][docker-docs].

### Setup
To set up the project, follow the steps below:

1. Clone the repository.

```bash
$ git clone https://github.com/g3ru1a/mangadb-api
```

2. Install the composer dependencies using the following command in your terminal:
```bash
$ docker run --rm \
-u "$(id -u):$(id -g)" \
-v $(pwd):/var/www/html \
-w /var/www/html \
laravelsail/php81-composer:latest \
composer install --ignore-platform-reqs
```

3. Copy `.env.example` to `.env`.

```bash
$ cp .env.example .env
```

4. Set the `WWWGROUP` and `WWWUSER` to your user ID, if it's not `1000`, in the `.env` file.

```text
WWWGROUP=1000
WWWUSER=1000
```

5. Set the database name, user, and password you want in the `.env` file.

```text
DB_DATABASE=laravel
DB_USERNAME=sail
DB_PASSWORD=password
```

6. Add your S3 information in the `.env` file.

```text
AWS_ACCESS_KEY_ID=<your-access-key>
AWS_SECRET_ACCESS_KEY=<your-secret-access-key>
AWS_DEFAULT_REGION=<your-region>
AWS_BUCKET=<your-bucket>
```

7. Set your image_cdn URL in the `.env` file.

```text
IMAGE_CDN_URL="https://cdn.yourwebsite.com/"
```

8. Run Sail using the following command:

```bash
$ ./vendor/bin/sail up
```
Run migrations using the following command:
```bash
$ php artisan migrate:fresh
```
If you want to run migrations using Docker, use the following command:

```bash
$ docker exec -d <container_name> php artisan migrate:fresh
```

That's it, you should be all set to play around with the api.

### Troubleshooting

Below is a list of common issues:

- If you encounter permission issues for the logs folder, check [this issue on StackOverflow][stackoverflow-issue].


[docker-docs]: https://docs.docker.com/get-docker/
[stackoverflow-issue]: https://stackoverflow.com/questions/50552970/laravel-docker-the-stream-or-file-var-www-html-storage-logs-laravel-log-co
[https://api.manga-db.com]: https://api.manga-db.com
[https://sandbox.manga-db.com]: https://sandbox.manga-db.com