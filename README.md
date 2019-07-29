# sphinx-doc
This repository contains information about docker image to run sphinx for building documentation


# Content of the Dopcker file
FROM alpine:latest


RUN apk --no-cache add make py3-pip python3-dev && \
    pip3 install --upgrade pip &&\
    pip3 install sphinx==2.1.2 && \
    pip3 install sphinx_rtd_theme && \
    pip3 install sphinx-autobuild && \
    pip3 install pygments-markdown-lexer && \
    pip3 install recommonmark && \
    pip3 install sphinxcontrib-mermaid

WORKDIR /workspace


# Compile the documentation with sphinx
sudo docker run -it -v $(pwd):/workspace -e USER_ID=$UID aminehy/sphinx-doc:v2.1.2  make html


# Command for Building the docker image
docker build -t aminehy/sphinx-doc:v2.1.2 .
docker push aminehy/sphinx-doc:v2.1.2 


