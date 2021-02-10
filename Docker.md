# Introduction to Docker
Docker is an open platform for developing, shipping, and running applications. The whole idea of Docker is for developers to easily develop applications, ship them into containers which can then be deployed anywhere. Docker enables you to separate your applications from your infrastructure, so you can deliver software quickly. With Docker, you can manage your infrastructure in the same ways you manage your applications.
# Docker platform
Docker provides the ability to package and run an application in a loosely isolated environment called a *container*. The isolation and security allow you to run many containers simultaneously on a given host. *Containers* are lightweight because they don’t need the extra load of a hypervisor, but run directly within the host machine’s kernel. This means you can run more containers on a given hardware combination than if you were using virtual machines. 

## Docker architecture
Docker uses a client-server architecture. The Docker client talks to the Docker daemon, which does the heavy lifting of building, running, and distributing your Docker containers. The Docker client and daemon can run on the same system, or you can connect a Docker client to a remote Docker daemon. The Docker client and daemon communicate using a REST API, over UNIX sockets or a network interface.

![Docker architecture](https://docs.docker.com/engine/images/architecture.svg)

# Why do we use Docker?
1. Docker containers provide a way to get a grip on software. You can use Docker to wrap up an application in such a way that its deployment and runtime issues—how to expose it on a network, how to manage its use of storage and memory and I/O, how to control access permissions—are handled outside of the application itself, and in a way that is consistent across all “containerized” apps. You can run your Docker container on any OS-compatible host (Linux or Windows) that has the Docker runtime installed.

2. *Portability*: Since a Docker container can easily be sent to another machine, you can set up everything on your own computer and then run the analyses on example: a more powerful machine.
*Sharability*: You can send the Docker container to anyone (who knows how to work with Docker).

3. It also allows them to get a head start by using one of thousands of programs already designed to run in a Docker container as a part of their application.

Reasons to use Docker:
1. *Fast, consistent delivery of your applications*

2. *Responsive deployment and scaling*

3. *Running more workloads on the same hardware*

## Docker Tutorial
Here are the lists of some Docker Tutorials available online:

[Docker-Overview](https://docs.docker.com/get-started/overview/)

[Tutorials Point](https://www.tutorialspoint.com/docker/index.htm)

[Docker blog](https://www.docker.com/blog/whats-in-a-container-platform/)

 [opensource.com](https://opensource.com/resources/what-docker)
 


