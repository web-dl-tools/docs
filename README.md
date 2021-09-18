# Introduction

![Web DL banner](./assets/overview.png)

[Web DL](https://web-dl-tools.github.io) tools are self-hosted tools to download audio & video resources, scrape various content types, direct download online resources and retrieve torrent file contents quickly and easily.

The main stack is comprised of an API and website, both which can be served from the same device/server.

_Build for the Raspberry Pi 4 (2GB+)_

## Features

* Fully authenticated with user creation and management.
* Secure, separate access to resources and files.
* Dynamic file download endpoint for secure file access management.
* Only stores files locally on device.
* Runs on less than 2 GB of memory across multiple containers.
* Authenticated websocket connection support for live status updates.
* Responsive for all screen sizes, from mobile to ultra-wide.
* Compiled for all modern web browsers.
* Authenticated user access to resources and files.
* Websocket live connection for automatic status and progress updates.
* Charts for data storage insights.
* Even more...

## Quick start

Please review the requirements, installation and config steps if errors occur when running these steps.

```bash
$ git clone git@github.com:web-dl-tools/api.git
$ cd ./api
$ make start
```

```bash
$ git clone git@github.com:web-dl-tools/website.git
$ cd ./website
$ make start
```