# MMDVM Hotspot

A Dockerized MMDVM Hotspot

## Running

#### Prerequisites:
* [Docker](https://www.docker.com)
* [docker-compose](https://docs.docker.com/compose/install/)

#### Quick-Start:
1. Install the prerequisites.
2. Edit the default config files in `data/` and rename them.
3. Start the updater: `docker-compose up -d updater`
4. Populate data volume: `docker cp data $(docker ps -f name=updater -q):/`
5. Bring up the rest: `docker-compose up -d`

