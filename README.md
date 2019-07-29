# sphinx-doc
This repository contains information about docker image to run sphinx for building documentation


## Compile the documentation with sphinx
sudo docker run -it -v $(pwd):/workspace -e USER_ID=$UID aminehy/sphinx-doc:v2.0.0  make html


## Command for Building the docker image
docker build -t aminehy/sphinx-doc:v2.0.0 .
docker push aminehy/sphinx-doc:v2.0.0



## Login to docker hub and push the image to docker hub
docker login
docker push aminehy/sphinx-doc:v2.0.0
