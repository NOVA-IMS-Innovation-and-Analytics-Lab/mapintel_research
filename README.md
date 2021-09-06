# Mapintel Experiments

This is the Experiments module of the Mapintel project. This module is composed mainly of notebooks. 

In the *notebooks folder* you can find various jupyter notebooks, each with an experimental purpose described in the first cell of each file.

This module is independent of the UI application and therefore should not be deployed. Its only objective is to perform experiments by making use of the Open Distro for Elasticsearch instance.

## Usage

### Option 1: Container

Just run
```
docker-compose --profile experiments up
``` 
in the root folder of the Mapintel repository. This will start two containers (Open Distro for Elasticsearch and Experiments container).
The Experiments container will run a jupyter notebook server which can be accessed at `https://localhost:9999`. 

For security reasons, jupyter notebook requires an authentication token which can be acquired in the terminal logs or by running 
```
docker exec mapintel_experiments_1 /usr/local/bin/jupyter notebook list
```

### Option 2: Local

Execute in this folder:
```
jupyter notebook ..
```

**Requirements**: This expects a running Open Distro for Elasticsearch instance at `https://localhost:9200`. Also, all python and system dependencies must be satisfied.