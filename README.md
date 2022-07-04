# Introduction

![Web DL banner](./assets/overview.png)

[Web DL](https://web-dl-tools.github.io) tools are self-hosted tools to download audio & video resources, scrape various content types, direct download online resources and retrieve torrent file contents quickly and easily.

The main stack comprises of an API and website, both which can be served from the same device/server.

_Build for the Raspberry Pi 4 (2 GB+)_

## Stack

**Website**:
A Vue.js SPA Website built to fully integrate the Web DL API and all of its features. 
It's the official browser client for the Web DL stack.

**API**:
A Django RESTful API build to form the core of the entire Web DL stack.
It's the **sole requirement to run Web DL**.


## Features

* Fully authenticated with user creation and management.
* Secure, separate access to resources and files.
* Dynamic file download endpoint for secure file access management.
* Only stores files locally on device.
* Runs on less than 2 GB of memory across multiple containers.
* Authenticated web socket connection support for live status updates.
* Responsive for all screen sizes, from mobile to ultra-wide.
* Compiled for all modern web browsers.
* Authenticated user access to resources and files.
* Web socket live connection for automatic status and progress updates.
* Charts for data storage insights.
* Even more...

## Quick start

```bash
$ git clone https://github.com/web-dl-tools/api.git
$ cd ./api
// Fill in .env file
$ make start
```

```bash
$ git clone https://github.com/web-dl-tools/website.git
$ cd ./website
// Fill in .env file
$ make start
```

Please review the [requirements](https://web-dl-tools.github.io/docs/#/requirements), [installation](https://web-dl-tools.github.io/docs/#/installation) and [configuration](https://web-dl-tools.github.io/docs/#/configuration) steps for additional information and troubleshooting.