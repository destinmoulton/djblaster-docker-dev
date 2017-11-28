### djblaster-docker
----
Set of docker containers for testing and running [DJBlaster](https://github.com/destinmoulton/djblasterbundle).

Includes:
* MySQL DB
* nginx
* php-fpm (5.6)
* phpMyAdmin

The images are derived from Alpine distros.

### Requirements
----
* docker
* docker-compose

### Getting Started
----
Start the docker containers:
`$ docker-compose up -d`

DJBlaster: http://djblaster.lcl:88

phpMyAdmin: http://djblaster.lcl:8888

### Folder Structure
----
This should be cloned into a folder parallel to the main DJBlaster folder.

* parent_dir
  * djblaster
    * symfony_installation
      * src/djblaster
        * Where the DJ Blaster bundle should be cloned.
  * docker
    * This repo cloned here.

The local volumes will be stored in the "docker" folder under "volumes". This includes a local volume for the mysql container so that there is data persistence while testing.

You can of course use whatever structure you prefer, but you will need to alter the docker-compose.yml to reflect these path changes.


### Docker Commands
----

Start the docker containers:
`$ docker-compose up -d`

Stop and remove the docker containers:
`$ docker-compose down`

Rebuild the docker containers:
`$ docker-compose build`

List the running docker processes:
`$ docker ps`

Start a shell in one of the containers:
`$ docker exec -i -t container_name /bin/sh`

### License
----
[MIT](https://github.com/destinmoulton/djblaster-docker-dev/blob/master/LICENSE)