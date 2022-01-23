# Requirements

## Hardware

Web DL is developed to run on a [Raspberry Pi 4 (2 GB+)](https://www.raspberrypi.org/products/raspberry-pi-4-model-b/). Running on it on any other arm device should also be possible, although this hasn't been tested. For storage, it's recommended to make use of an external USB drive or hard disk (not recommended for Raspberry Pi). 

Web DL is currently developed on Apple macOS with an Apple Silicon (ARM) processor. In order to run the stack on x86 small modifications should be made to the _docker-compose.yml_ and _Dockerfile_ files of the API repository in order to run the containers. You can refer to these files to see what changes are required.

### Recommended requirements

* ARMv7+ processor 
* 2 GB memory or more
* 1 GB of free disk space
* Additional disk space for requests

###  Minimum requirements

* ARMv7/x86 processor
* 1.2 GB memory
* 1 GB of free disk space
* Additional disk space for requests

## Operating System

* Debian-based Linux distributions, such as [Raspberry Pi OS](https://www.raspberrypi.org/software/operating-systems/), [Ubuntu](https://ubuntu.com/raspberry-pi) and others
* Apple macOS Mojave 10.14 or higher
* Microsoft Windows 10 Home/Pro 2004 (build 19041), Enterprise/Education 1909 (build 18363) or higher (64-bit)

## Software

* [Git](https://git-scm.com/downloads)
* [Docker Desktop](https://www.docker.com/products/docker-desktop)<sup>[1]</sup>
* [Microsoft Visual Code](https://code.visualstudio.com/)<sup>[2]</sup>

### Minimum runtime environment

* Docker 18.09.2 or higher
* Docker Compose 1.23.2 or higher

<sup>[1]</sup>: On lower versions of macOS, Windows, or on Linux, the
[Docker Engine](https://hub.docker.com/search?offering=community&operating_system=linux&q=&type=edition)
can be installed as a valid substitute.

<sup>[2]</sup>: A file editor is required in order to edit hidden dot files. Any other file editor capable of this should also suffice.

## Development

For development the Web DL Website requires the following software to be installed:

* [Node.js](https://nodejs.org/en) (LTS)
* [Yarn](https://classic.yarnpkg.com/en/docs/install/#mac-stable) (Classic stable)
* Several additional packages installed via Yarn
