To build both docker images:

  * docker-compose --x-networking build

The --x-networking option is a new feature of docker-compose that replaces links. It setups up networks so that containers can communicate with one another.

To bring up the stack in development mode:

  * docker-compose --x-networking -f docker-compose.yml -f docker-compose-dev.yml

To bring up the stack in production mode:

  * docker-compose --x-networking -f docker-compose.yml

NOTE: The order of the configuration files supplied by -f is important. The configuration is updated as each file is parsed.
