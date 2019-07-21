# Docker-Nextcloud

## Introduction

This repository is a customized version of the official Nextcloud docker-compose example. To view the official example visit:
https://github.com/nextcloud/docker/tree/master/.examples/docker-compose/with-nginx-proxy-self-signed-ssl/mariadb/fpm

The files are configured to serve Nextcloud behind a reverse proxy on the same machine as this application.

This template includes the following services:
- Nextcloud
- MariaDB
- Redis
- Collabora-Online
- PhpMyAdmin

## Getting started

Start by cloning or downloading this repository.
```
git clone https://github.com/r00tusrDE/docker-nextcloud.git
```

Every environment variable that needs to be set is marked with ```{changeme}```.
You need to edit the following files:
- docker-compose.yml
- app.env
- db.env

## Additional Information

If you don't need phpmyadmin or collabora-online just delete the particular section in docker-compose.yml

I'm using Nextcloud behind a reverse proxy so all ports are only published to localhost. Change this if needed in docker-compose.yml

Apache reverse proxy config for Nextcloud: https://github.com/r00tusrDE/apache-reverse-proxy-templates/blob/master/nextcloud

Apache reverse proxy config for Collabora-Online: https://github.com/r00tusrDE/apache-reverse-proxy-templates/blob/master/collabora-online

For more information about Nextcloud environment variables and Nextcloud with docker visit the official nextcloud docker repository:
https://github.com/nextcloud/docker
