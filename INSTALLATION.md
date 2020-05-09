Installation

On the remote

Make sure the firewall leaves open the registry port

Create the directory
```
mkdir -p ~/dev/docker/registries/docker
```

On the local

Copy the a file
```
scp ~/dev/docker/registries/docker/docker-compose.yml stephane@149.28.60.185:~/dev/docker/registries/docker/
```

On the remote

Start the registry
```
cd ~/dev/docker/registries/docker/;
docker stack deploy --compose-file docker-compose.yml docker-registry
```

