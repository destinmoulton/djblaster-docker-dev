### djblaster-docker
====================
Set of docker containers for running djblaster.


### Folder Structure
====================
This should be cloned into a folder parallel to the main DJBlaster folder.

* parent_dir
.* djblaster
..* Main DJBlaster repo cloned here.
.* docker
..* This repo cloned here.

The local volumes will be stored in the "docker" folder. This includes a local volume for the mysql container so that there is data persistence while testing.

You can of course use whatever structure you prefer, but you will need to alter the docker-compose.yml to reflect these path changes.


### Docker Commands
============

Start the docker containers:
$ docker-compose up -d

Stop and remove the docker containers:
$ docker-compose down

List the running docker processes:
$ docker ps

Start a shell in one of the containers:
$ docker exec -i -t container_name /bin/sh


### Port Notes
===================

