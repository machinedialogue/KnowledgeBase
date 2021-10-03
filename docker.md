docker-compose
 - https://codeburst.io/replicate-kubernetes-ingress-locally-with-docker-compose-2872e650af6b
 - https://scotch.io/tutorials/create-a-mean-app-with-angular-2-and-docker-compose

Awesome Compose 
 - https://github.com/docker/awesome-compose

On Windows:
- https://hub.docker.com/editions/community/docker-ce-desktop-windows
- https://hub.docker.com/search?q=&type=edition&offering=community&sort=updated_at&order=desc

https://scotch.io/tutorials/create-a-mean-app-with-angular-2-and-docker-compose

https://github.com/Microsoft/dotnet-framework-docker

<b>Develop with containers in Visual Studio</b>

https://docs.microsoft.com/en-us/visualstudio/containers/?view=vs-2017

<b>Dockerizing .NET Apps with Microsoft's Build Images on Docker Hub</b>

https://blog.sixeyed.com/dockerizing-net-apps-with-microsofts-build-images-on-docker-hub/

How to containerize the .NET Framework web apps with Windows Containers and Docker

https://github.com/dotnet-architecture/eShopModernizing/wiki/02.-How-to-containerize-the-.NET-Framework-web-apps-with-Windows-Containers-and-Docker

<b>SQL Server 2016</b>

https://github.com/Microsoft/mssql-docker/tree/master/windows

docker run -d -p 1533:1533 -e sa_password=<SA_PASSWORD> -e ACCEPT_EULA=Y microsoft/mssql-server-windows-developer:2016-sp1

<b>Reading Q:</b>

https://docs.microsoft.com/en-us/dotnet/standard/microservices-architecture/docker-application-development-process/docker-app-development-workflow


<b>Considerations for air-gapped registries</b>

https://docs.docker.com/registry/deploying/#considerations-for-air-gapped-registries

<b>How To Build Your Containerization Strategy</b>

https://dockercon2018.hubs.vidyard.com/watch/X43ys6KF3BmHdLtYN7zb8N

Build Tools 2015

https://github.com/Microsoft/dotnet-framework-docker/issues/23


<b>cmds: </b>

Display the running processes of a container
 - docker container top CONTAINER [ps OPTIONS]

Get Environment Variable from Docker Container
 - docker exec container env

Image from tar file : 
docker load --input node.tar

sudo docker run -it --rm -v `pwd`:`pwd` -w `pwd` node bash

<b>Ref: </b>

https://stackoverflow.com/questions/24309526/how-to-change-the-docker-image-installation-directory

https://stackoverflow.com/questions/19234831/where-are-docker-images-stored-on-the-host-machine

https://docs.docker.com/registry/deploying/

<b>Troubleshooting:</b>

Docker Networking Disabled: WARNING: IPv4 forwarding is disabled. Networking will not work
 - https://stackoverflow.com/questions/41453263/docker-networking-disabled-warning-ipv4-forwarding-is-disabled-networking-wil
 - 

