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

Option 3 - Making
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
$ sudo npm install -g angular-cli webpack bower express nodemon http-server pm2
```

### Installing Mongodb - Debian

```console
$ sudo apt-get update  
$ sudo apt-get install mongodb-server -y 
```
