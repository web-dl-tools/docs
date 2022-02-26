# Upgrade

Web DL tools have been developed to update with a simply command. For that reason Git is recommended to simplify the update process. It will automatically update to the latest version.

## Check for running tasks
> :warning: **Make sure there aren't any requests currently running**. _They might become stuck once the update process shuts down the repository._

A command is provided to check for actively running tasks. This command fails with returncode 1 when there are tasks active. Make sure you combine this command when creating a custom cronjob to automatically upgrade the API.

```bash
$ docker exec -it web-dl_django python3 manage.py tasks
```

## Check for updates

The website can check for updates for both the website and API. Simply go to the build page (by clicking on the versions in the footer). An automatic check and version comparison will start. If there are any updates available you will be notified, with the version difference (patch, minor or major) as well as quick links to the update guide and a change log.

## Updating

In order to quickly update both repositories a make command is available to perform the update. Simply enter one of the repositories via the command line and run the following command in order to stop, update and then restart the application.

```bash
$ make update && make start
```

### Automatic updating

Automatic updating is currently not supported. Please periodically check the website build page for updates and manually run the make commands. A custom cronjob can be created to automatically upgrade the containers. Make sure to use the command mentioned above to safely shutdown the API.
