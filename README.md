# Simple Python Flask Dockerized Application#

Build the image using the following command
docker build -t pythonweb:latest .

Run the Docker container using the command shown below.
docker run -d -p 8080:8080 pythonweb:latest
docker run --name webapp -p 8080:8080 pythonweb:latest
docker run --name webapp -p 8080:8080 --rm pythonweb:latest
docker run -p 8080:8080 pythonweb:latest

Local Directory Mounts
docker run --name app --mount type=bind,source=`pwd`,target=/app,readonly -p 8080:8080 pythonweb:latest
docker run --name app --mount type=bind,source=`pwd`,target=/app,readonly -p 8080:8080 --rm pythonweb:latest

docker exec -it webapp "/bin/bash"



----------------------------
skaffold dev
skaffold run