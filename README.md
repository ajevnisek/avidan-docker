# avidan-docker
Avidan Lab Docker Cheatsheet

# Setup
Create a directory shared with the docker
```bash
mkdir from_container
```
# Build docker Image
```bash
docker image build -t ajevnisek/avidan-container-demo .
```


# Run docker Container
```bash
docker run --rm --name container-demo -dit -v ~/Desktop/sandbox/avidan-docker/from_container:/results ajevnisek/avidan-container-demo bash
```
## Debug
### watch logs
```bash
docker logs container-demo -f
```

### bash to the container
```bash
docker exec -it container-demo bash
```


# Misc
Clear all docker cache:
```bash
docker system prune -a
```

# Run this image with run:ai:
```bash
runai submit -g 1 --name avidan-container-demo -i ajevnisek/avidan-docker-cuda-ubuntu-16.04-conda -v ~/Desktop/sandbox/avidan-docker/from_container:/results --pvc=storage:/storage
```