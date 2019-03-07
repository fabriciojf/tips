# Facilities for my development environment 

Based on a debian environment

### Installing Node.js

Option 1 - Node 6

```console
$ curl -sL https://deb.nodesource.com/setup_6.x | sudo -E bash -
$ sudo apt-get install -y nodejs
```

Option 2 - Node 7

```console
$ curl -sL https://deb.nodesource.com/setup_7.x | sudo -E bash -
$ sudo apt-get install -y nodejs
```

Option 3 - Node 8

```console
$ curl -sL https://deb.nodesource.com/setup_8.x | sudo -E bash -
$ sudo apt-get install -y nodejs
```

For Node 10

```console
sudo apt-get install curl software-properties-common
curl -sL https://deb.nodesource.com/setup_10.x | sudo bash -
```

For Node 11

```console
sudo apt-get install curl software-properties-common
curl -sL https://deb.nodesource.com/setup_11.x | sudo bash -
```

Option 4 - Making

```console
$ sudo apt-get install g++
$ wget -N http://nodejs.org/dist/node-latest.tar.gz
$ tar xzvf node-latest.tar.gz && cd `ls -rd node-v*`
$ ./configure
$ make install
```
Extras

```console
$ sudo apt-get install build-essential nodejs-legacy
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
  - pm2
  
```console
$ sudo npm install -g angular-cli webpack bower 
$ sudo npm install -g express nodemon http-server pm2
```

### Installing Mongodb - Debian

```console
$ sudo apt-get update  
$ sudo apt-get install mongodb-server -y 
```
### Install BmAPI / Speedcob

```console
$ sudo apt-get install mongodb-server -y
$ sudo apt-get install node-express
$ sudo npm install -g express nodemon http-server pm2
```

### PM2 Upgrade

Updating pm2 monit view

```console
$ npm update -g pm2  
$ pm2 update  
```
