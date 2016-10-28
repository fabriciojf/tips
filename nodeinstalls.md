# Facilities for my development environment 

Based on a debian environment

### Installing Node.js

```console
$ sudo apt-get install g++
$ wget -N http://nodejs.org/dist/node-latest.tar.gz
$ tar xzvf node-latest.tar.gz && cd `ls -rd node-v*`
$ ./configure
$ make install
$ apt-get install nodejs-legacy
```

### Installing Node-express

Used to create projects by express command line

```console
$ sudo apt-get install node-express
```

### Suggested global Packages

  - angular-cli
  - webpack
  - bower
  - express
  - nodemon
  - http-server
  
```console
$ sudo npm install -g angular-cli webpack bower express nodemon http-server
```

### Installing Mongodb - Debian

```console
$ sudo apt-get update  
$ sudo apt-get install mongodb-server -y 
```
### Running pm2 in production

Basic

```console
$ pm2 start file_start.js
```
Clustering in 2 instances

```console
$ pm2 start file_start.js -i 2
```
View active apps

```console
$ pm2 list
```

Others commands

```console
$ pm2 monit
$ pm2 show <app_name>
$ pm2 logs
$ pm2 logs <app_name>
$ pm2 reload all
$ pm2 restart all
$ pm2 startup
```
