# Configuration

Configuration in both repositories is managed by an environment file. They will require some manual configuration to set Web DL up for your network situation. In order to perform these changes you'll need a text editor with the ability to modify dot files. _These files are hidden/invisible by default in most operating systems._ It is recommended to use Microsoft Visual Code for this.

## Environment file

 A base example is provided in the
repository as _.env.dist_. Please copy and rename this file to _.env_ and fill in the values.

Both repositories require a _.env_ file on the root level of each folder. A base example file is provided in the
repository as _dist.env_.

1. Copy and rename the example _dist.env_ file to _.env_.
2. Fill in the empty values in the _.env_ file.

### Properties

#### Website

| Property               | Description                           | Required | Example                                               |
|------------------------|---------------------------------------|----------|-------------------------------------------------------|
| **VUE_APP_API_URL**    | The URL of the Web DL API             | Yes      | http://localhost:8000/api/                            |
| **VUE_APP_SENTRY_DSN** | The DSN URL for Sentry error tracking | No       | https://1234567890abcdef@12345.ingest.sentry.io/67890 |

#### API

| Property              | Description                                         | Required | Example                                               |
|-----------------------|-----------------------------------------------------|----------|-------------------------------------------------------|
| **USER_ID**           | The user ID of owner the files folder               | Yes      | 1                                                     |
| **FILES_PATH**        | The path of the files folder                        | Yes      | ./files                                               |
| **DJANGO_DEBUG**      | Enable/disable Django debug mode                    | Yes      | False                                                 |
| **DJANGO_SECRET_KEY** | Key used by Django to provide cryptographic signing | Yes      | someSecureDjangoSecretkeyFromhttps://djecrety.ir      |
| **SENTRY_DSN**        | The DSN URL for Sentry error tracking               | No       | https://1234567890abcdef@12345.ingest.sentry.io/67890 |
| **POSTGRES_USER**     | The PostgreSQL username                             | Yes      | postgres                                              |
| **POSTGRES_PASSWORD** | The PostgreSQL user password                        | Yes      | someSecurePW                                          |
| **POSTGRES_DB**       | The PostgreSQL default database                     | Yes      | postgres                                              |
