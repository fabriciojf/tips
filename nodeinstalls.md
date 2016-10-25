# Facilities for my development environment 

### Installing Node.js
```console
$ sudo apt-get install g++
$ wget -N http://nodejs.org/dist/node-latest.tar.gz
$ tar xzvf node-latest.tar.gz && cd `ls -rd node-v*`
$ ./configure
$ make install
$ apt-get install nodejs-legacy
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
