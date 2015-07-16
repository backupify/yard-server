# yard-server

scripts for managing our yard doc server

## Installation

```
# clone project
git clone git@github.com:backupify/yard-server.git

# copy restart script to repo
cp yard-server/restart_server my_project/
# tweak the script for your use case

# copy nginx conf
cp yard-server/yard-nginx.conf /etc/nginx/sites-enabled/default.conf

# create a cronjob to run the restart script
crontab -e
# save in cron editor
0,30 * * * * ~/my_project/restart_server > ~/my_project/restart_server.log 2>&1
```

## Usage

```
./~/my_project/restart_server && sudo service nginx restart
```
