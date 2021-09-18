# Installation & usage

Web DL tools have been developed to run fully inside docker containers. For that reason Docker is the sole requirement to run the application. All installations will be performed during runtime.

In other to assist in retrieving and updating the tools Git is required.

## Cloning the repositories

It is recommended to clone the repositories to your home directory due to how Docker manages file/folder permissions on Linux. Please open (a folder inside) your home directory via the terminal and run the following commands:

```bash
$ git clone git@github.com:web-dl-tools/api.git
$ git clone git@github.com:web-dl-tools/website.git
```

This will create two folders for the [api](https://github.com/web-dl-tools/api) and [website](https://github.com/web-dl-tools/website) repositories. Both folders will contain a valid origin remote enabling automatic updates via the command line.

## Managing containers

In order to perform actions on the containers both repositories contain make commands that simplify the usage of the stack. Simply enter one of the repositories via the command line and run the following commands:

### Building

Build the containers, install all dependacies and store the (intermediate) images.

```bash
$ make build
```

### Starting

Start the containers and serve the application.

```bash
$ make start
```

### Stopping

Stop the application. Note that this will not remove the (intermediate) images.

```bash
$ make stop
```

### Update

Stop, update and then restart the application.

```bash
$ make update && make start
```

### Cleanup

Docker will store various intermediate images during the build process. In order to remove outdated images run this command periodically.

```bash
$ make clean
```