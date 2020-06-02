# Hadoop on AARCH64

This documents my process of deploying Hadoop and friends on aarch64 system.

## Environment
1. Ubuntu 20.04
1. Raspberry Pi 4 4GB

## Package Versions
1. Hadoop 2.10.0
1. Hive 1.2.2
1. OpenJDK 8

## Process

### Hadoop

#### Building native extensions

1. Need to build protobuf 2.5

##### Protobuf

1. Protobuf 2.5 does not support building on aarch64
1. Apply the following patch to workaround
1. https://gist.github.com/BennettSmith/7111094

#### Configuration

1. Copy the configuration files into place

### Hive

1. Need MySQL 5.7 as metastore

#### MySQL 5.7

1. Ubuntu 20.04 apt only has MySQL 8.0
1. Install via Docker
1. https://scito.ch/content/mysql-57-docker-container-raspberry-pi-using-debian-sid

# References
1. https://qiita.com/thashi/items/f8884b78df3faa5ff887
1. https://scito.ch/content/mysql-57-docker-container-raspberry-pi-using-debian-sid
1. https://www.linode.com/docs/databases/hadoop/how-to-install-and-set-up-hadoop-cluster/#architecture-of-a-hadoop-cluster
