# rtde-dev-docker

Docker Compose configs for RTDE development and demoing on Jackie's laptop.

## Jupyter Notebook

The `jupyter` directory of this repository contains a Docker Compose configuration file that allows you run the [Jupyter Data Science Notebook](https://github.com/jupyter/docker-stacks/tree/master/datascience-notebook) container.  The container provides Jupyter notebook, and common data science Python libraries (pandas, matplotlib, etc).

### Starting a Jupyter Notebook Server ###

To start the server, open a terminal, navigate to the directory that contains the `docker-compose.yml` file and run `docker-compose up -d`.  For example, on my machine, I would run:

```
cd /home/jeffrey/github.com/jlym/rtde-dev-docker/jupyter
docker-compose up -d  
```

### Accessing Jupyter Notebook ###

You can access Jupyter by running a browser on the VM and navigating to [http://localhost:8888](http://localhost:8888) .

### Stopping the Server ###

To stop the server, open a terminal and navigate to the directory that contains the `docker-compose.yml` file and run `docker-compose down`.  For example, on my machine, I would run:

```
cd /home/jeffrey/github.com/jlym/rtde-dev-docker/jupyter
docker-compose down
```

### Files ###

Jupyter has a directory named `work` that gets mapped to the `work-volume` directory on the host machine (your VM).  This means that you can access files that you create in the `work` directory on Jupyter by looking in the `work-volume` directory on your VM.
