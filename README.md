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
or simply use command:
```bash
cp .env.example .env
```

3. Starting & Stopping Sail

Before starting Sail, you should ensure that no other web servers or databases are running on your local computer. To start all of the Docker containers defined in your application's docker-compose.yml file, you should execute the up command:

```bash
./vendor/bin/sail up
```
However, instead of repeatedly typing `./vendor/bin/sail` to execute Sail commands, you may wish to configure a Bash alias that allows you to execute Sail's commands more easily:

```bash
alias sail='[ -f sail ] && bash sail || bash vendor/bin/sail'
```

To start all of the Docker containers in the background, you may start Sail in "detached" mode:
```bash
sail up -d
```
To stop all of the containers, you may simply press Control + C to stop the container's execution. Or, if the containers are running in the background, you may use the stop command:
```bash
sail stop
```
Form more information about how Laravel Sail is interacting with Docker environment visit [Laravel Sail](https://laravel.com/docs/8.x/sail) official documentation

# Usage

Once the application's Docker containers have been started, you can access the application in your web browser at: http://localhost

On localhost development mode if u want to make some changes into JS files you should run yarn to install node_modules:

```bash
sail yarn
```

# Support

If u stuck and can't run all this commands properly contact: [vati@redberry.ge](mailto:vati@redberry.ge)