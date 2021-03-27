# Yarn tips

## Installing

```console
# install global
$ sudo npm install yarn -g

# setting the prefix
$ yarn global bin
$ yarn config get prefix
$ yarn config set prefix ~/.yarn

# exporting path
$ export PATH="$PATH:`yarn global bin`"

# running a react project for example
$ yarn
$ yarnpkg start
```
