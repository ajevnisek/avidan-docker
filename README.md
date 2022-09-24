# avidan-docker
Avidan Lab Docker Cheatsheet

# Setup
Create a directory shared with the docker
```bash
mkdir from_container
```
# Build docker Image
```bash
docker image build -t avidan-container .
```


# Run docker Container
```bash
docker run --rm --name avidan-container-demo -dit -v ~/Desktop/sandbox/avidan-docker/from_container:/results avidan-container bash
```
## Debug
### watch logs
```bash
docker logs avidan-container-demo -f
```

### bash to the container
```bash
docker exec -it our-demo bash
```


# Misc
Clear all docker cache:
```bash
docker system prune -a
```

