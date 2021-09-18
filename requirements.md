# Requirements

## Hardware

Web DL is developed to run on a [Raspberry Pi 4 (2GB+)](https://www.raspberrypi.org/products/raspberry-pi-4-model-b/). Running on it on any other arm device should also be possible, although this hasn't been tested. For storage it's recommended to make use of an external USB drive or hard disk (not recommended for Raspberry Pi). 

Web DL is developed on apple macOS, although small modifications have been made to the docker-compose.yml and Dockerfile files. You can refer to these files in the API repository to see what's required.

### Recommended requirements

* ARMv7 processor
* 2GB memory or more
* 1 GB of free disk space
* Additional disk space for requests

###  Minimum requirements

* ARMv7 processor
* 1.5GB memory
* 1 GB of free disk space
* Additional disk space for requests

## Operating System

* Debian-based linux distributions, such as [Raspberry Pi OS](https://www.raspberrypi.org/software/operating-systems/), [Ubuntu](https://ubuntu.com/raspberry-pi) and others
* Apple macOS Mojave 10.14 or higher (Intel chip)<sup>[1]</sup>
* Microsoft Windows 10 Home/Pro 2004 (build 19041), Enterprise/Education 1909 (build 18363) or higher (64-bit)

## Software

* [Git](https://git-scm.com/downloads)
* [Docker Desktop](https://www.docker.com/products/docker-desktop)
* [Microsoft Visual Code](https://code.visualstudio.com/)<sup>[3]</sup>

### Minimum runtime environment

* Docker 18.09.2 or higher
* Docker Compose 1.23.2 or higher

<sup>[1]</sup>: Docker Desktop for Mac on Apple Silicon is available but requires a
[manual install of Rosetta 2](https://docs.docker.com/docker-for-mac/apple-silicon/#system-requirements).

<sup>[2]</sup>: On lower versions of macOS, Windows, or on Linux, the
[Docker Engine](https://hub.docker.com/search?offering=community&operating_system=linux&q=&type=edition)
can be installed as a valid substitute.

<sup>[3]</sup>: A file editor is required in order to edit hidden dot files. Any other file editor capable of this should also suffice.
