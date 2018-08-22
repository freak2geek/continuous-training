# To Build App

To build the app, F2G's projects use [Docker](https://www.docker.com/). Docker encapsulates the project infrastructure, including OS and app dependencies, in an unique image, which can be instantiated and run. On run the instances, all app code and database data is linked, so live and persisted changes are supported.

## Build image

- Run `build`

## Run development

- Run `start-development`/`start`

## Run production

- Run `start-production`

## Rebuild images

F2G's scripts use `docker-compose up` to build and run smartly the docker images on any change on the Dockerfile. However, sometimes you may be needed to rebuild it. Using `build` will force a rebuild.

## Run custom commands on the containers

On start the app, a virtual environment is run to allocate the app processes. If it's needed to install new app dependency or run any bash command in such environment:

- Run `bash`. It opens a bash instance within the container process for the app.

- Run any command you want.

Alternatively, to force install of new dependencies within `package.json` file, use `install` command.
