# Configuration

Configuration in both repositories is managed by an environment file. They will require some manual configuration to set Web DL up for your network situation. In order to perform these changes you'll need a text editor with the ability to modify dot files. _These files are hidden/invisible by default in most operating systems._ It is recommended to use Microsoft Visual Code for this.

## Environment file

 A base example is provided in the repositories as _.env.dist_. Please copy and rename this file to _.env_ and fill in the values.

## User ID

In order to properly set permissions and manage folder access for the downloaded files Web DL needs to be aware of the user ID of the user in which's home directory Web DL is installed. Below you can find out how to find the user ID for your operating system. Please enter the following command in a console:

### Apple macOS

```bash
$ id -i
```
For a single user Mac system the user id is often _501_.

### Ubuntu/Raspbian/UNIX based operating systems

```bash
$ id -u
```
For a single user Linux system the user id is often _1000_.


## Properties

Below you can find a description and required status for all current properties. 

#### Website

| Property               | Description                           | Required | Example                                               |
|------------------------|---------------------------------------|----------|-------------------------------------------------------|
| **VUE_APP_API_URL**    | The URL of the Web DL API             | Yes      | http://localhost:8000/api/                            |
| **VUE_APP_SENTRY_DSN** | The DSN URL for Sentry error tracking | No       | https://1234567890abcdef@12345.ingest.sentry.io/67890 |

#### API

| Property              | Description                                         | Required | Example                                               |
|-----------------------|-----------------------------------------------------|----------|-------------------------------------------------------|
| **USER_ID**           | The user ID of the owner of the files folder        | Yes      | 501                                                   |
| **FILES_PATH**        | The path of the files folder                        | Yes      | ./files                                               |
| **DJANGO_DEBUG**      | Enable/disable Django debug mode                    | Yes      | False                                                 |
| **DJANGO_SECRET_KEY** | Key used by Django to provide cryptographic signing | Yes      | someSecureDjangoSecretkeyFromhttps://djecrety.ir      |
| **SENTRY_DSN**        | The DSN URL for Sentry error tracking               | No       | https://1234567890abcdef@12345.ingest.sentry.io/67890 |
| **POSTGRES_USER**     | The PostgreSQL username                             | Yes      | postgres                                              |
| **POSTGRES_PASSWORD** | The PostgreSQL user password                        | Yes      | someSecurePW                                          |
| **POSTGRES_DB**       | The PostgreSQL default database                     | Yes      | postgres                                              |
