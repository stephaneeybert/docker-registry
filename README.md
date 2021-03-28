Installation

Go to the registries directory
```
cd ~/dev/docker/registries
```
Clone the repository
```
git clone git@github.com:stephaneeybert/docker-registry.git
```
Rename the directory
```
mv docker-registry/ docker
```


On the local

Copy the a file
```
scp ~/dev/docker/registries/docker/docker-compose.yml stephane@...:~/dev/docker/registries/docker/
```

On the remote

Make sure the firewall leaves open the registry port

Create the directory
```
mkdir -p ~/dev/docker/registries/docker
```

Start the registry
```
cd ~/dev/docker/registries/docker/;
docker stack deploy --compose-file docker-compose.yml docker-registry
```

Stopping the registry
```
docker stack rm docker-registry
```

