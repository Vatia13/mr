# Project

Project "Moveretail" is using Laravel 8.65 that requires PHP "8.1" or you can chose one from your ./docker directory, changing docker-compose.yml under build -> context: "path" (8.1 recommended)

## Installation

1. Install Composer Dependencies

```bash
docker run --rm \
    -u "$(id -u):$(id -g)" \
    -v $(pwd):/opt \
    -w /opt \
    laravelsail/php80-composer:latest \
    composer install --ignore-platform-reqs
```
2. Environment variables .env
In project directory make copy of .env.example file and rename it to .env

3. Starting & Stopping Sail

Before starting Sail, you should ensure that no other web servers or databases are running on your local computer. To start all of the Docker containers defined in your application's docker-compose.yml file, you should execute the up command:

```bash
./vendor/bin/sail up
```
To start all of the Docker containers in the background, you may start Sail in "detached" mode:
```bash
./vendor/bin/sail up -d
```
To stop all of the containers, you may simply press Control + C to stop the container's execution. Or, if the containers are running in the background, you may use the stop command:
```bash
./vendor/bin/sail stop
```
Form more information about how Laravel Sail is interacting with Docker environment visit [Laravel Sail](https://laravel.com/docs/8.x/sail) official documentation