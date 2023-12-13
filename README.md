# NOTER APP

### Dockerizing simple nodejs app

This repo consists of simple node js app which print `THIS IS NOTER VERSION 2`

### RUN

To build a docker image from the docker file:

`$ docker build -t <your-dockerhub-id>/noterapp:<version-tag> .`

The above command will build your docker image.

To run the docker image

`$ docker run -d -p 80:3000 <your-dockerhub-id>/noterapp:<version-tag>`

To push this image to the docker hub

`$ docker login`

(provide your username and password)

`$ docker push <your-dockerhub-id>/noterapp:<version-tag>`


### Modify container

To modify the content of the containers

`$ docker ps (will give running container-id)`

`$ docker exec -it <running container id> bash`

Then modify index.js

Exit the container.

To save images

`$ docker commit <running container id>`

After committing, we need to add a tag to new image

`$ docker tag -t <your-dockerhub-id>/noterapp:<version-tag> <docker image id>`

Then push the new version to docker hub

`$ docker push <your-dockerhub-id>/noterapp:<version-tag>`


### Docker compose

To run the node js app using docker-compose

`$ docker-compose up`




