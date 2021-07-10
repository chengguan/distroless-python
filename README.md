# distroless-python (debugging turned on)

# Building
docker build -t hello-debug . 

# Running as daemon
docker run -d -p 80:80 hello-debug

# Starting container with busybox shell
docker run -p 80:80 --entrypoint=sh -ti hello-debug

# Hop onto busybox shell of a running container
docker exec -ti <container id> sh 

# Inspect the layout of a docker image
docker image inspect d8e988f73df4
