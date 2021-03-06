# Docker

Docker is an open platform for developing, shipping, and running applications.

- Deliver software quickly and consistently as enables you to separate your apps from your infrastructure, which benefits on your apps running always on the same environment and sandbox your projects.

- With Docker, you can manage your infrastructure in the same ways you manage your applications.

- Docker provides tooling and a platform to manage the lifecycle of your app components via the containers.

## Terminology

### Container

A container is the Docker's component that packs and run your application in a isolated fashion. It becomes as the unit for distributing and testing your application.

- Run multiple instances of a container on a given host.

- Run directly within the host machine's kernel, they don't load any hypervisor, so that the process become faster to run.

- In the contrary of virtual machines, you can run more instances of containers on a given hardware combination.

- Deploy your app as a container or orchestrated service, whether you production environment is a local laptop, physical or virtual machines in a data center, a cloud provider or a mixture of environments.

- Containers are great for continuous integration and continuous delivery (CI/CD) workflows.

- A container is a runnable instance of an image. You can create, start, stop, move, or delete a container using the Docker API or CLI. You can connect a container to one or more networks, attach storage to it, or even create a new image based on its current state.

- By default, a container is relatively well isolated from other containers and its host machine. You can control how isolated a container’s network, storage, or other underlying subsystems are from other containers or from the host machine.

- When a container is removed, any changes to its local state that are not stored in persistent storage disappear.

#### Virtual machine vs Container

![Virtual Machine vs container](https://monosnap.com/image/TSj7FG6m3fhk8HWD9N8Ofb8Pva2dCV.png)

### Images

An image is a read-only template with instructions for creating a Docker container. An image is based on another image, with some additional customization.

To build your own image, you create a Dockerfile with a simple syntax for defining the steps needed to create the image and run it.

Each instruction in a Dockerfile creates a layer in the image. When you change the Dockerfile and rebuild the image, only those layers which have changed are rebuilt. This is part of what makes images so lightweight, small, and fast, when compared to other virtualization technologies.

![Image](https://monosnap.com/image/gbdxcUl0jOz3J0rdFeAJsdwQBpwq4t.png)

![Image flow](https://monosnap.com/image/deLJ9kxFSLMAqxJ55EboR56wtKGjgf.png)

![Container vs Images](https://monosnap.com/image/aqnG6q9bjoXfKexwxWwTb2LyAlYBxo.png)

### Services

Services allow you to scale containers across multiple Docker daemons, which all work together as a swarm with multiple managers and workers. Each member of a swarm is a Docker daemon, and the daemons all communicate using the Docker API. A service allows you to define the desired state, such as the number of replicas of the service that must be available at any given time. By default, the service is load-balanced across all worker nodes.

### Daemon

The server is a long-running program called a daemon proccess, `dockerd` command. Can run on the same system or be external.

### REST API

A REST API which specify an interface that programs can use to talk with the damon and instruct what to do.

### Client

A CLI on the client, the `docker` command. It comunicates to the docker daemon through the REST API over UNIX sockets or a network interface. The Docker client can communicate with more than one daemon.

### Registry

A Docker registry stores Docker images. Docker Hub and Docker Cloud are public registries that anyone can use, and Docker is configured to look for images on Docker Hub by default.

- When you use the `docker pull` or `docker run` commands, the required images are pulled from your configured registry.

- When you use the `docker push` command, your image is pushed to your configured registry.

- Images are distributed and versioned. You can upgrade the application by pulling the new version of the image and redeploying the containers.

### Namespaces

Docker uses a technology called namespaces to provide the isolated workspace called the container. When you run a container, Docker creates a set of namespaces for that container.

The pid namespace: Process isolation (PID: Process ID).
The net namespace: Managing network interfaces (NET: Networking).
The ipc namespace: Managing access to IPC resources (IPC: InterProcess Communication).
The mnt namespace: Managing filesystem mount points (MNT: Mount).
The uts namespace: Isolating kernel and version identifiers. (UTS: Unix Timesharing System).

### Control Groups

Docker Engine on Linux also relies on another technology called control groups (cgroups). A cgroup limits an application to a specific set of resources.

### Union file systems

Union file systems, or UnionFS, are file systems that operate by creating layers, making them very lightweight and fast. Docker Engine uses UnionFS to provide the building blocks for containers.

### Container format

Docker Engine combines the namespaces, control groups, and UnionFS into a wrapper called a container format. The default container format is libcontainer

### Docker Engine

The docker engine is a client-sever app.

![Docker Engine](https://docs.docker.com/engine/images/engine-components-flow.png)

### Docker Architecture

![Docker architecture](https://docs.docker.com/engine/images/architecture.svg)

### Docker Compose

A facility to write in a single file and run all the container instances to run due to developing several services.

## References

- Check out: [Docker overview](https://docs.docker.com/engine/docker-overview/#control-groups)

- Watch: [First Docker course of basics](https://www.youtube.com/watch?v=YFl2mCHdv24), [Docker compose](https://www.youtube.com/watch?v=Qw9zlE3t8Ko) and [Deploy Docker containers with Docker Cloud](https://www.youtube.com/watch?v=F82K07NmRpk)

- Watch: [Execute containers and commands within the running containers](https://www.youtube.com/watch?v=_cSn1HcykYY&index=10&list=PLn5IkU1ZhgiZl4EH7AFkqs-pqF6ZUz_iS), [List stopped containers](https://www.youtube.com/watch?v=INqmK7rSaH8&list=PLn5IkU1ZhgiZl4EH7AFkqs-pqF6ZUz_iS&index=13), [Interactive containers](https://www.youtube.com/watch?v=NZdH12tFN6A&list=PLn5IkU1ZhgiZl4EH7AFkqs-pqF6ZUz_iS&index=14) and [Exit without stopping container and attach to running containers](https://www.youtube.com/watch?v=FnANuSh1syI&index=16&list=PLn5IkU1ZhgiZl4EH7AFkqs-pqF6ZUz_iS).

- Play: [Interactive tutorial to manage containers lifecycle](https://play.instruqt.com/public/tracks/docker-container-lifecycle)

- Read: [Use docker-compose](https://docs.docker.com/compose/gettingstarted/#where-to-go-next)

- Print: [Cheatsheet for Docker CLI](https://www.docker.com/sites/default/files/Docker_CheatSheet_08.09.2016_0.pdf), [Another cheatsheet for Docker CLI](http://files.zeroturnaround.com/pdf/zt_docker_cheat_sheet.pdf), [Cheatsheet for Dockerfile](https://kapeli.com/cheat_sheets/Dockerfile.docset/Contents/Resources/Documents/index) and [Cheatsheet for docker-compose](https://devhints.io/docker-compose)
