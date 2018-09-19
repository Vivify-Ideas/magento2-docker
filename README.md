![Magento 2](https://cdn.rawgit.com/rafaelstz/magento2-snippets-visualstudio/master/images/icon.png)

#  Magento 2 Docker to Development

### Apache 2.4 + PHP 7.1 + OPCache +  Redis + Varnish Cache + MariaDB + ElasticSearch +  SendMail + N98 Magerun 2 + XDebug

[![Build Status](https://travis-ci.org/TerrorSquad/clean-docker.svg?branch=master)](https://travis-ci.org/TerrorSquad/clean-docker)
[![Docker Build](https://img.shields.io/docker/build/gninkovic/clean-docker.svg)](https://hub.docker.com/r/gninkovic/clean-docker/)
[![Docker Pulls](https://img.shields.io/docker/pulls/gninkovic/clean-docker.svg)](https://hub.docker.com/r/gninkovic/clean-docker/)
[![Docker Starts](https://img.shields.io/docker/stars/gninkovic/clean-docker.svg)](https://hub.docker.com/r/gninkovic/clean-docker/)
[![Build Status](https://images.microbadger.com/badges/image/gninkovic/clean-docker.svg)](https://microbadger.com/images/gninkovic/clean-docker)
[![Releases](https://img.shields.io/github/release/TerrorSquad/clean-docker.svg)](https://github.com/TerrorSquad/clean-docker/releases)

### Requirements

**MacOS:**

Install [Docker](https://docs.docker.com/docker-for-mac/install/), [Docker-compose](https://docs.docker.com/compose/install/#install-compose) and [Docker-sync](https://github.com/EugenMayer/docker-sync/wiki/docker-sync-on-OSX).

**Windows:**

Install [Docker](https://docs.docker.com/docker-for-windows/install/), [Docker-compose](https://docs.docker.com/compose/install/#install-compose) and [Docker-sync](https://github.com/EugenMayer/docker-sync/wiki/docker-sync-on-Windows).

**Linux:**

Install [Docker](https://docs.docker.com/engine/installation/linux/docker-ce/ubuntu/) and [Docker-compose](https://docs.docker.com/compose/install/#install-compose).

### How to use

Execute in your terminal, change the *MYMAGENTO2* to use the name of your project:

```
curl -s https://raw.githubusercontent.com/TerrorSquad/clean-docker/master/init | bash -s MYMAGENTO2 clone
```

If you want to install the Magento 2, use like that:

```
cd MYMAGENTO2
./shell
rm index.php
install-magento2
```

You can specify the version that want install (e.g. `install-magento2 2.2`).

### Panels

Enjoy your new panels!

**Web server:** http://localhost:8080/

**Varnish cache:** http://localhost

**Elastic search:** http://localhost:9200

**PHPMyAdmin:** http://localhost:8081

**Local emails:** http://localhost:8025

### Features commands

| Commands  | Description  | Options & Examples |
|---|---|---|
| `./init`  | If you didn't use the CURL setup command above, please use this command changing the name of the project.  | `./init MYMAGENTO2` |
| `./start`  | If you continuing not using the CURL you can start your container manually  | |
| `./stop`  | Stop your project containers  | |
| `./kill`  | Stops containers and removes containers, networks, volumes, and images created to the specific project  | |
| `./shell`  | Access your container  | `./shell root` | |
| `./magento`  | Use the power of the Magento CLI  | |
| `./n98`  | Use the Magerun commands as you want | |
| `./grunt-init`  | Prepare to use Grunt  | |
| `./grunt`  | Use Grunt specifically in your theme or completely, it'll do the deploy and the watcher.  | `./grunt luma` |
| `./xdebug`  |  Enable / Disable the XDebug | |
| `./composer`  |  Use Composer commands | `./composer update` |
