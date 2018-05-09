# 00 - Prerequisites

During the workshop basic knowledge of Linux, Git and networking is required.

### Steps:

1. Download & install [VirtualBox 5.2.10](https://www.virtualbox.org/wiki/Downloads)
1. Download & install [Vagrant 2.0.1](https://www.vagrantup.com/downloads.html) or higher.
1. Clone this repository
1. Open a terminal/command prompt session and navigate to this repo.
1. run `vagrant up`

**Note:** You may see an error like `Warning: Connection reset. Retrying... Warning: Remote connection disconnect. Retrying...` You can ignore this error since the SSH has to be started. Connection will succeed after 30 sec or so.

## Connect to the Docker hosts
```sh
$ ssh -p 2222 root@127.0.0.1 # to connect to node-1
$ ssh -p 2200 root@127.0.0.1 # to connect to node-2
$ ssh -p 2201 root@127.0.0.1 # to connect to manager-1
$ ssh -p 2202 root@127.0.0.1 # to connect to manager-2
$ ssh -p 2203 root@127.0.0.1 # to connect to manager-3
```
For an overview of the available user credentials see [](../Vagrant-Base)

