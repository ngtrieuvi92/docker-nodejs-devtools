# Node.js w/ Bower, Grunt & Gulp
## This Docker image has been setup to avoid permission issues when using Docker Volumes, implement from this tutorial [HANDLING PERMISSIONS WITH DOCKER VOLUMES](https://denibertovic.com/posts/handling-permissions-with-docker-volumes/)

It can run with UID of current user in your machine to avoid permission issue, default UID is 1000, not root user
Example:`docker run -it -e LOCAL_USER_ID=`id -u $USER` ngtrieuvi92/nodejs-devtools`

This repository contains a **Dockerfile** of [Node.js](http://nodejs.org/) w/ [Bower](http://bower.io/) & [Grunt](http://gruntjs.com/) for [automated builds](https://hub.docker.com/r/ngtrieuvi92/nodejs-devtools/) published to the public [Docker Hub Registry](https://hub.docker.com/).

### Base Docker Image

* [library/node](https://hub.docker.com/r/library/node/)

### Supported tags and respective `Dockerfile` links
* [`latest`](https://github.com/ngtrieuvi92/nodejs-devtools/blob/master/Dockerfile)

### Installation

1. Install [Docker](https://www.docker.com/).

2. Download an [automated build](https://github.com/ngtrieuvi92/nodejs-devtools) from public the [Docker Hub Registry](https://hub.docker.com/): `docker pull ngtrieuvi92/nodejs-devtools`

### Usage

    docker run -it -e LOCAL_USER_ID=`id -u $USER` --rm ngtrieuvi92/nodejs-devtools

#### Run `node`

    docker run -it -e LOCAL_USER_ID=`id -u $USER` --rm ngtrieuvi92/nodejs-devtools node

#### Run `npm`

    docker run -it -e LOCAL_USER_ID=`id -u $USER` --rm ngtrieuvi92/nodejs-devtools npm

#### Run `bower`

    docker run -it -e LOCAL_USER_ID=`id -u $USER` --rm ngtrieuvi92/nodejs-devtools bower

#### Run `grunt`

    docker run -it -e LOCAL_USER_ID=`id -u $USER` --rm ngtrieuvi92/nodejs-devtools grunt

#### Run `gulp`

    docker run -it -e LOCAL_USER_ID=`id -u $USER` --rm ngtrieuvi92/nodejs-devtools gulp
