# Upgrade

> :warning: **Make sure there aren't any requests currently running**. _They might become stuck once the update process shuts down the repository._


Web DL tools have been developed to update with a simply command. For that reason Git is the recommended to simplify the update process. It will automatically update to the latest version.

## Updating

In order to quickly update both repositories a make command is available to perform the update. Simply enter one of the repositories via the command line and run the following command in order to stop, update and then restart the application.

```bash
$ make update && make start
```

### Automatic updating

Automatic updating is currently not supported. Once a task check has been build a periodic cron job can be created to automatically perform an update (if Web DL is inactive).