# Upgrade

Web DL tools have been developed to update with a simple command. You do need to have a proper git origin remote setup for the command to work. If you cloned the repositories as described in the [configuration](https://web-dl-tools.github.io/docs/#/configuration) this will be setup already. The command will automatically update the repository to the latest master commit.

## Check for running tasks
> :warning: **Make sure there aren't any requests currently running before updating the API**. _They might become stuck once the update process shuts down the repository._

A command is provided to check for actively running tasks in the API. Make sure you run this command before manually running the update command. Additionally this command fails with returncode 1 and can (and should) therefore be combined if you're using a custom cronjob to automatically upgrade the API.

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

Automatic updating is currently not supported. Please periodically check the website build page for updates and manually run the make commands. A custom cronjob can be created to automatically upgrade the containers. Make sure to use the command mentioned above to check for running tasks.
