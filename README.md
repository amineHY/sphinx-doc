<!-- TOC -->

- [Description](#description)
    - [Compile the documentation website](#compile-the-documentation-website)
    - [Login to Docker Hub](#login-to-docker-hub)
    - [(Re)Build docker image](#rebuild-docker-image)
    - [Push the image to Docker Hub](#push-the-image-to-docker-hub)

<!-- /TOC -->

# Description
This repository contains information about docker image to run sphinx for building documentation

Link to docker hub: https://hub.docker.com/r/aminehy/sphinx-doc

## Compile the documentation website
`docker run -it -v $(pwd):/workspace -e USER_ID=$UID aminehy/sphinx-doc:v2.1.2  make html`



## Login to Docker Hub
`docker login`

## (Re)Build docker image
`docker build -t aminehy/sphinx-doc:v2.1.2 .`
`docker push aminehy/sphinx-doc:v2.1.2`


## Push the image to Docker Hub
`docker push aminehy/sphinx-doc:v2.1.2`
