# Docker Tutorial
## 1. Docker Flow
1. List of images: `docker images`
2. List of containers: `docker ps`
3. All containers: `docker ps -a`
4. Last container: `docker ps -l`
5. Image to container: `docker run <image>` e.g: `docker run --ti ubuntu:latest bash`
6. Container to image: `docker commit <container>`
7. Tag image: `docker commit <container> <tag>`

## 2. Docker Run
1. Run and remove container after done: `docker run --rm -ti ubuntu <cmd>` e.g. `docker run --rm -ti ubuntu sleep 5`
2. Run and do multiple command: `docker run -ti ubuntu bash -c "sleep 5; echo all done"`
3. Detach container: `docker run -d -ti ubuntu bash`
4. Attach container: `docker attach <container>`
5. Detach container after attaching: `ctrl+p` > `ctrl+q`
6. Add another process: `docker exec -ti <container> <cmd>`

## 3. Container Output
1. Logs: `docker logs <container>`

## 4. Kill and Stop Container
1. Terminate: `docker kill <container>`
2. Delete: `docker rm <container>`
3. Memory limit: `docker run --memory maximum-allowed-memory image-name <cmd>`
4. CPU Limit: `docker run --cpu-shares` or `docker run --cpu-quota`