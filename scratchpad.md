docker build . -t custom-nginx-docker

docker run -p 1935:1935 custom-nginx-docker
