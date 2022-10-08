# Requirements

## Hardware

Web DL is developed to run on a [Raspberry Pi 4 (2 GB+)](https://www.raspberrypi.org/products/raspberry-pi-4-model-b/). Running it on any other armv7+ device should also be possible, although this hasn't been tested. For storage, it's recommended to make use of an external USB drive (for Raspberry Pi's) or hard disk. 

Web DL is currently developed on Apple macOS with an Apple Silicon (ARM64) processor. In order to run the stack on ARM64 or x86 small modifications should be made to the [_Dockerfile_](https://github.com/web-dl-tools/api/blob/master/compose/selenium/Dockerfile) file of the API repository in order to run the containers. You can refer to this file to see what changes are required.

### Recommended requirements

* ARMv8 processor (64-bit)
* 2 GB memory or more
* 500 MB of free disk space
* Additional disk space for requests

###  Minimum requirements

* ARMv7+ processor (64-bit)
* 1.2 GB memory
* 200 MB of free disk space
* Additional disk space for requests

## Operating System (64-bit)

* Debian-based Linux distributions, such as [Raspberry Pi OS](https://www.raspberrypi.org/software/operating-systems/)<sup>[1]</sup>, [Ubuntu](https://ubuntu.com/raspberry-pi) and others
* Apple macOS Mojave 10.15 or higher
* Microsoft Windows 11 Home/Pro/Enterprise/Education version 21H2 or higher
* Microsoft Windows 10 Home/Pro version 21H1 or higher, Enterprise/Education version 20H2 or higher.

## Software

* [Git](https://git-scm.com/downloads)
* [Docker Desktop](https://www.docker.com/products/docker-desktop)<sup>[2]</sup>
* [Microsoft Visual Code](https://code.visualstudio.com/)<sup>[3]</sup>

### Minimum runtime environment

* Docker 18.09.2 or higher
* Docker Compose 1.23.2 or higher

### Development

For development the Web DL Website requires the following software to be installed:

* [Node.js](https://nodejs.org/en) (LTS)
* [Yarn](https://classic.yarnpkg.com/en/docs/install/#mac-stable) (Classic stable)
* Several additional packages installed via Yarn

<sup>[1]</sup>: Raspberry Pi promotes their 32-bit image higher on the page and in the image tool. Make sure you download/select the 64-bit image.

<sup>[2]</sup>: On lower versions of macOS, Windows, or on Linux, the
[Docker Engine](https://hub.docker.com/search?offering=community&operating_system=linux&q=&type=edition)
can be installed as a valid substitute.

<sup>[3]</sup>: A file editor is required in order to edit hidden dot files. Any other file editor capable of this should also suffice.
