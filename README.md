# rstudio-isb-ngchm-demo
This repository contains a docker-compose file for extending the
ISB CGC RStudio example image with tools for creating
[Next-Generation Clustered Heat Maps (NG-CHMs)](http://bioinformatics.mdanderson.org/main/NG-CHM:Overview).
The docker-compose file extends the ISB image with the
[NGCHM R package](https://github.com/bmbroom/NGCHMR) and
[a small package (ISB-CGC-utils)](https://github.com/bmbroom/ISB-CGC-utils)
containing example functions for creating NG-CHMs using data obtained from the ISB CGC cloud pilot.

This system is designed to run on on any machine running
[Docker](https://www.docker.com/) and [Docker Compose](https://docs.docker.com/compose/).
The machine concerned can be local to your environment or in
any cloud environment that supports Docker (including but not limited to the
[Google Compute Engine](https://cloud.google.com/compute/)).
It is not designed for the Google Container engine.

## Usage

Clone this repository to a machine running [Docker](https://www.docker.com/) version 10 or higher and [Docker Compose](https://docs.docker.com/compose/) version 1.6.2 or higher.

The system uses a named docker volume to store RStudio data:
```bash
$ docker volume create --name=rstudioData
```

Cd into the repository and start the docker containers:
```bash
$ cd rstudio-isb-ngchm-demo
$ docker-compose up -d
```
The container will publish the rstudio interface on port 8787.

In a cloud environment you might need to enable access to that port.

## NG-CHM Server

This system must be used in conjunction with one or more NG-CHM systems.

The [ngchm-system-one repository](https://github.com/bmbroom/ngchm-system-one) contains a
docker-compose file for creating a ready-to-use NG-CHM system.

Once up and running, the home page for that server will provide instructions for connecting it with
this RStudio system.
The [R package](https://github.com/bmbroom/ISB-CGC-utils) documents how to
create NG-CHMs.
