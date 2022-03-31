# kipa-backup-script

Bash script for backing up https://github.com/partio-scout/kipa events.

For example, schedule this to be run every 15 min, create (private) github repo for backups and add some magic for auto commits. Might also want to implement some simple monitoring for failing backups and/or latest backup age, e.g. a simple html page that is updated depending on script exit code.

## Set up envs

Replace values with your own.

```
touch .env
echo HOST="localhost" >> .env
echo PORT="3000" >> .env
echo EVENT_NAME="testikisa" >> .env
echo BACKUP_DIR="/Users/pekkine/testikisa_backups" >> .env
```

## Take backup

Grant execution permissions if needed

`chmod +x take_backup`

Run script

`./take_backup`

## Restoring event from backup

For now, this has to be done via Kipa UI. Some kind of automated xml import at kipa startup might be nice feature but probably not worth the effort.