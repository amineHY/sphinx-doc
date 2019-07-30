# sphinx-doc
This repository contains information about docker image to run sphinx for building documentation
Link to docker hub: https://hub.docker.com/r/aminehy/sphinx-doc

## Compile the documentation with sphinx
`docker run -it -v $(pwd):/workspace -e USER_ID=$UID aminehy/sphinx-doc:v2.1.2  make html`


## Command for Building the docker image
`docker build -t aminehy/sphinx-doc:v2.1.2 .`
`docker push aminehy/sphinx-doc:v2.1.2`


## Login to docker hub and push the image to docker hub
`docker login`
`docker push aminehy/sphinx-doc:v2.1.2`
