# Ubuntu Container Administration using Docker

## Project Overview

This project demonstrates hands-on Ubuntu 24.04 container administration using Docker. The objective was to create and manage an isolated Linux environment for basic system administration and troubleshooting activities.

## Technologies Used

- Docker
- Ubuntu 24.04
- Linux
- Windows PowerShell

## Project Implementation

1. Pulled the Ubuntu 24.04 Docker image.
2. Created and ran an interactive Ubuntu container.
3. Created a Linux user named `supportuser`.
4. Installed essential utilities such as curl and vim.
5. Created `/opt/troubleshooting` directory.
6. Restarted the container and verified persistence.

## Commands Used

```bash
docker pull ubuntu:24.04

docker run -it --name ubuntu ubuntu:24.04

apt update

adduser supportuser

apt install curl vim -y

mkdir -p /opt/troubleshooting

exit

docker start -ai ubuntu
```

## Verification

```bash
docker ps -a

docker exec ubuntu id supportuser

docker exec ubuntu dpkg -l curl vim

docker exec ubuntu ls -ld /opt/troubleshooting
```

## Key Learnings

- Docker image and container management
- Linux user administration
- Package installation
- Directory management
- Container lifecycle management
- Data persistence across container restarts

## Project Outcome

Successfully created and administered an Ubuntu container using Docker, gaining practical experience in Linux administration and containerization.

