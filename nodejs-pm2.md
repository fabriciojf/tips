# Running pm2 in production
### Install

```console
$ sudo npm install pm2 -g
```

### Basic

```console
$ pm2 start file_start.js
```
### Clustering in 2 instances

```console
$ pm2 start file_start.js -i 2
```
### View active apps

```console
$ pm2 list
```

### Removing an app

```console
$ pm2 delete <id>
$ pm2 delete 0
```

### Others commands

```console
$ pm2 monit
$ pm2 show <app_name>
$ pm2 logs
$ pm2 logs <app_name>
$ pm2 reload all
$ pm2 restart all
$ pm2 startup
```
