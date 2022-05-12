# kipa-backup-script

Bash script for backing up https://github.com/partio-scout/kipa events to Github.

For example, schedule this to be run every 15 min. 

Might also want to use some simple monitoring tool e.g. cronitor. 

## Set up envs

Replace values with your own.

```
touch .env
echo HOST="localhost" >> .env
echo PORT="3000" >> .env
echo EVENT_NAME="testikisa" >> .env
echo BACKUP_REPO_DIR="/Users/pekkine/testikisa-kipa-backup" >> .env
```

## Set up git repo

Create `BACKUP_REPO_DIR` and a (private) git repo

## Take backup

Grant execution permissions if needed

`chmod +x take_backup`

Run script

`./take_backup`

## Restoring event from backup

For now, this has to be done via Kipa UI. Some kind of automated xml import at kipa startup might be nice feature but probably not worth the effort.