Installation

On the remote

Make sure the firewall leaves open the registry port

Create the directory
```
mkdir -p ~/dev/docker/registries/registry
```

On the local

Copy the a file
```
scp ~/dev/docker/registries/registry/docker-compose.yml stephane@149.28.60.185:~/dev/docker/registries/registry/
```

On the remote

Start the registry
```
cd ~/dev/docker/registries/registry/;
docker stack deploy --compose-file docker-compose.yml registry
```

