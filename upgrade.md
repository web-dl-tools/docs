# Upgrade

> :warning: **Make sure there aren't any requests currently running**. _They might become stuck once the update process shuts down the repository._


Web DL tools have been developed to update with a simply command. For that reason Git is recommended to simplify the update process. It will automatically update to the latest version.

## Check for updates

The website can check for updates for both the website and API. simply go to the build page (by clicking on the versions in the footer). An automatic check and version comparison will start. If there are any updates available you will be notified, with the version difference (patch, minor or major) as well as quick links to the update guide and a changelog.

## Updating

In order to quickly update both repositories a make command is available to perform the update. Simply enter one of the repositories via the command line and run the following command in order to stop, update and then restart the application.

```bash
$ make update && make start
```

### Automatic updating

Automatic updating is currently not supported. Please periodically check the website build page for updates.
