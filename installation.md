# Installation & usage

Web DL tools have been developed to run fully inside docker containers. For that reason Docker is the sole requirement to run the application. All installations will be performed during runtime.

## Cloning the repositories

It is recommended to clone the repositories to your home directory due to how Docker manages file/folder permissions on Linux. Please open (a folder inside) your home directory via the terminal and run the following commands:

```bash
$ git clone git@github.com:web-dl-tools/api.git
$ git clone git@github.com:web-dl-tools/website.git
```

This will create two folders for the [api](https://github.com/web-dl-tools/api) and [website](https://github.com/web-dl-tools/website) repositories. Both folders will contain a valid origin remote enabling automatic updates via the command line.

## Installation

In order to perform actions on the containers both repositories contain make commands that simplify the usage of the stack. Simply enter one of the repositories via the command line and run the following commands:

**Building**:
Build the containers, install all dependencies and store the (intermediate) images.

```bash
$ make build
```

**Starting**:
Start the containers and serve the application.

```bash
$ make start
```

### Additional action

**Stopping**:
Stop the application. _This will not remove the (intermediate) images._

```bash
$ make stop
```

**Cleanup**:
Docker will store various intermediate images during the build process. In order to remove outdated images run this command periodically.

```bash
$ make clean
```

## Usage

### As a user
Once the API and Website are both running you can simply go to the server address or IP address in any modern browser and Web DL will load. **Do make sure your firewall settings allow external access on port 80.**

**Example**:
Web DL is running on a local device with IP address _192.168.1.3_. You can use the following URL to access Web DL.

```url
http://192.168.1.3/
```

From there you can register a new user and login. 

### As an admin

In order manage Web DL users as an admin a separate flow exists. First you need to create a superuser. You can do this by running the following command: _Make sure the API containers are running._

```bash
$ docker exec -it web-dl_django python3 manage.py createsuperuser
```

This will access a container inside the API stack and run a command to create a new user. You will be prompted for the account details. After the superadmin has been created you can access the admin panel on port 8000. In addition to this you can still use your admin user as a regular user on the website.

**Example**:
Using the same scenario as above you can now use the following URL to access the admin panel for Web DL.

```url
http://192.168.1.3:8000/adminlogin/
```
