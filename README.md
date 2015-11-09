# Python docker image for development environment

A Docker Python image with some useful packages for development environments.
Do not use it for production.


## Configuration

Installed modules

 * pudb
 * ipython


## Common usage

### Launching a python console

The default command launch a Python 2 console:

    # Classic console
    $ docker run -it alexisno/python-dev
    # IPython console
    $ docker run -it alexisno/python-dev ipython

To launch a Python 3 console:

    # Classic console
    $ docker run -it alexisno/python-dev python3
    # IPython console
    $ docker run -it alexisno/python-dev ipython3


### Using it as a base image for a project

This image should be used as a basic image for any project.

* Create a Dockerfile based on this image and add your project dependencies.
* Create you own image with `docker build` or `docker-compose build`.

Run your new image with a command similar to this:

    docker run -d -p 80:80 -v /path/to/your/project/sources:/var/www/project-name
