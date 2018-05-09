# VirtualBox Base Image

This base image contains the pre-requisites to get started with Docker on CentOS/RHEL 7.

### Commands that have been run:
```sh
$ yum install -y yum-utils device-mapper-persistent-data lvm2
$ yum-config-manager --add-repo https://download.docker.com/linux/centos/docker-ce.repo
$ yum update
$ yum install docker-ce

$ systemctl enable docker
$ systemctl start docker
```

### Users
| Username        | Password           | Groups |
| ------------- | ------------- | ----- |
| root | root | root |
| vagrant | vagrant | vagrant, wheel |
| john | john | docker |
| jane | jane | docker |

### Connecting to the machine
```sh
$ ssh -p 2222 vagrant@127.0.0.1
```

## Artifacts
- **docker-ce-stable.ova:**  The exported virtualbox appliance


## Packing and testing the appliance for Vagrant
```sh
$ vagrant package --base docker-ce-stable --output docker-ce.box
$ vagrant box add --name docker-ce-stable docker-ce.box
$ vagrant init docker-ce-stable
$ vagrant up
```