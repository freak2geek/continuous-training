# Docker

Docker is an open platform for developing, shipping, and running applications

- Deliver software quickly and consistently as enables you to separate your apps from your infrastructure.

- With Docker, you can manage your infrastructure in the same ways you manage your applications.

- Docker provides tooling and a platform to manage the lifecycle of your app components via the containers.

## Terminology

### Container

A container is the Docker's component that packs and run your application in a isolated fashion. It becomes as the unit for distributing and testing your application.

- Run multiple instances of a container on a given host.

- Run directly within the host machine's kernel, they don't load any hypervisor, so that the process become faster to run.

- In the contrary of virtual machines, you can run more instances of containers on a given hardware combination.

- Deploy your app as a container or orchestrated service, whether you production environment is a local laptop, phisical or virtual machines in a data center, a cloud provider or a mixture of environments.

- Containers are great for continuous integration and continuous delivery (CI/CD) workflows.

- A container is a runnable instance of an image. You can create, start, stop, move, or delete a container using the Docker API or CLI. You can connect a container to one or more networks, attach storage to it, or even create a new image based on its current state.

- By default, a container is relatively well isolated from other containers and its host machine. You can control how isolated a container’s network, storage, or other underlying subsystems are from other containers or from the host machine.

- When a container is removed, any changes to its local state that are not stored in persistent storage disappear.

#### Images

An image is a read-only template with instructions for creating a Docker container. An image is based on another image, with some additional customization.

To build your own image, you create a Dockerfile with a simple syntax for defining the steps needed to create the image and run it.

Each instruction in a Dockerfile creates a layer in the image. When you change the Dockerfile and rebuild the image, only those layers which have changed are rebuilt. This is part of what makes images so lightweight, small, and fast, when compared to other virtualization technologies.

### Services

Services allow you to scale containers across multiple Docker daemons, which all work together as a swarm with multiple managers and workers. Each member of a swarm is a Docker daemon, and the daemons all communicate using the Docker API. A service allows you to define the desired state, such as the number of replicas of the service that must be available at any given time. By default, the service is load-balanced across all worker nodes.

### Docker Engine

The docker engine is a client-sever app.

#### Daemon

The server is a long-running program called a daemon proccess, `dockerd` command. Can run on the same system or be external.

#### REST API

A REST API which specify an interface that programs can use to talk with the damon and instruct what to do.

#### Client

A CLI on the client, the `docker` command. It comunicates to the docker daemon through the REST API over UNIX sockets or a network interface. The Docker client can communicate with more than one daemon.

#### Registry

A Docker registry stores Docker images. Docker Hub and Docker Cloud are public registries that anyone can use, and Docker is configured to look for images on Docker Hub by default.

- When you use the `docker pull` or `docker run` commands, the required images are pulled from your configured registry.

- When you use the `docker push` command, your image is pushed to your configured registry.

- Images are distributed and versioned. You can upgrade the application by pulling the new version of the image and redeploying the containers.

#### Namespaces

Docker uses a technology called namespaces to provide the isolated workspace called the container. When you run a container, Docker creates a set of namespaces for that container.

The pid namespace: Process isolation (PID: Process ID).
The net namespace: Managing network interfaces (NET: Networking).
The ipc namespace: Managing access to IPC resources (IPC: InterProcess Communication).
The mnt namespace: Managing filesystem mount points (MNT: Mount).
The uts namespace: Isolating kernel and version identifiers. (UTS: Unix Timesharing System).

#### Control Groups

Docker Engine on Linux also relies on another technology called control groups (cgroups). A cgroup limits an application to a specific set of resources.

#### Union file systems

Union file systems, or UnionFS, are file systems that operate by creating layers, making them very lightweight and fast. Docker Engine uses UnionFS to provide the building blocks for containers.

#### Container format

Docker Engine combines the namespaces, control groups, and UnionFS into a wrapper called a container format. The default container format is libcontainer

![Docker Engine](https://docs.docker.com/engine/images/engine-components-flow.png)

![Docker architecture](https://docs.docker.com/engine/images/architecture.svg)

## References

- Check out: [Docker overview](https://docs.docker.com/engine/docker-overview/#control-groups)
