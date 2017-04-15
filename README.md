# Kiliman

Pinnackl **Kiliman** is an *open-source realtime database stack* based on the [RehtinkDB](https://www.rethinkdb.com/) and [Horizon](http://horizon.io/) projects.

It's basicaly a *realtime relational database* coupled with a *web socket application*.

## Getting Started

Kiliman is using **docker compose** to facilitate the deployement of the database environement.

    Note: If you are new to Docker, you can find the documentation here: https://www.docker.com/

Clone this project, and duplicate the `.hz/config.toml.example` in .`hz/config.toml`
Replace the application name `# project_name = "PROJECT_NAME"` in the config file

Run the following command in the Kiliman directory

```bash
$ docker-compose up -d
```

## Administration

### RethinkDB Administrator console

*RethinkDB* offer an administraion tool to monitor your database server. It's basicaly available on your RethinkDB _**CONTAINER_IP**_ on port _**8080**_

    Note: By default the binding of 8080 to the host has been disabled, if your want to access it from localhost, you need to uncomment the ports section in the docker-compose.yml file. Otherwise, you'll be able to connect to the direct IP address using tools as Portainer.

### Chateau

The *RethinkDB* administrator console can be a little hard to work with, so you might want to use a proper data explorer.

[Chateau](https://github.com/neumino/chateau) is a *phpmyadmin* like for RethinkDB.

Install *Chateau* via **npm**

```bash
$ npm install -g chateau
```

Duplicate the `config.js.example` in `config.js` and edit it to mathch your configuration

Run the following command in the Kiliman directory

```bash
$ chateau
```

The Data explorer will be available on the defined address in the *config.js*. The default will be _**localhost:9001**_.
