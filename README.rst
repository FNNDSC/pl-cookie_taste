pl-cookie_taste
================================

.. image:: https://img.shields.io/docker/v/fnndsc/pl-cookie_taste?sort=semver
    :target: https://hub.docker.com/r/fnndsc/pl-cookie_taste

.. image:: https://img.shields.io/github/license/fnndsc/pl-cookie_taste
    :target: https://github.com/FNNDSC/pl-cookie_taste/blob/master/LICENSE

.. image:: https://github.com/FNNDSC/pl-cookie_taste/workflows/ci/badge.svg
    :target: https://github.com/FNNDSC/pl-cookie_taste/actions


.. contents:: Table of Contents


Abstract
--------

A simple plugin to demonstrate a working plugin from cookiecutter-chrisapp


Description
-----------


``cookie_taste`` is a *ChRIS fs-type* application that produces ... by ...


Usage
-----

.. code::

    docker run --rm fnndsc/pl-cookie_taste cookie_taste
        [-h|--help]
        [--json] [--man] [--meta]
        [--savejson <DIR>]
        [-v|--verbosity <level>]
        [--version]
        <inputDir> <outputDir>


Arguments
~~~~~~~~~

.. code::

    [-h] [--help]
    If specified, show help message and exit.
    
    [--json]
    If specified, show json representation of app and exit.
    
    [--man]
    If specified, print (this) man page and exit.

    [--meta]
    If specified, print plugin meta data and exit.
    
    [--savejson <DIR>] 
    If specified, save json representation file to DIR and exit. 
    
    [-v <level>] [--verbosity <level>]
    Verbosity level for app. Not used currently.
    
    [--version]
    If specified, print version number and exit. 


Getting inline help is:

.. code:: bash

    docker run --rm fnndsc/pl-cookie_taste cookie_taste --man

Run
~~~

You need to specify input and output directories using the `-v` flag to `docker run`.


.. code:: bash

    docker run --rm -u $(id -u)                             \
        -v $(pwd)/in:/incoming -v $(pwd)/out:/outgoing      \
        fnndsc/pl-cookie_taste cookie_taste                        \
        /incoming /outgoing


Development
-----------

Build the Docker container:

.. code:: bash

    docker build -t local/pl-cookie_taste .

Run unit tests:

.. code:: bash

    docker run --rm local/pl-cookie_taste nosetests

Examples
--------

Put some examples here!


.. image:: https://raw.githubusercontent.com/FNNDSC/cookiecutter-chrisapp/master/doc/assets/badge/light.png
    :target: https://chrisstore.co
