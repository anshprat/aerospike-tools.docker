## Aerospike Tools Dockerfile

This repository contains the Dockerfile for [Aerospike Tools](http://www.aerospike.com/docs/tools/). 

### Dependencies

- [ubuntu:14.04](https://registry.hub.docker.com/_/ubuntu/)

### Installation

1. Install [Docker](https://www.docker.io/).

2. Build an image from Dockerfile:_
   
		docker build -t="aerospike/aerospike-tools" github.com/aerospike/aerospike-tools.docker

### Usage

1. The following will run `asd` with all the exposed ports forward to the host machine.

	docker run -ti --name aerospike-tools aerospike/aerospike-tools <Aerospike Tool>

Example:

```
# docker run -ti aerospike/aerospike-tools asmonitor -e "asinfo -v statistics" -h host1.example.aerospike.com 
```
	
2. Available tools:

- asmonitor -h SEED_HOST

- asinfo -h SEED_HOST

- asadm -h SEED_HOST

- asloglatency -h SEED_HOST

- cli -h SEED_HOST

- ascli -h SEED_HOST

- aql -h SEED_HOST

- asbackup -h SEED_HOST

- asrestore -h SEED_HOST


Addtional info on using our tools can be found [here](http://www.aerospike.com/docs/tools/)




