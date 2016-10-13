### Configurando webpack e angular 1.5

Instale o webpack, no meu caso eu prefiro uma instalação global
```console
$ sudo npm install webpack -g
```

Crie o arquivo de input para o webpack
``` console
$ touch input.js
```
Ou liste o conteúdo de uma pasta jogando a saída para o input e depois reorganize-o
```
$ find -name *.js | grep js/ > input.js
```
Insira os arquivos javascript que deseja minificar e ofuscar dentro do input.js através da tag require. Exemplo:
```javascript
// input.js content
require('./js/app_front.js');
require('./js/controller/home/home_controller.js');
require('./js/controller/header/header_controller.js');
require('./js/model/user.js');
```

Crie o arquivo de configuração webpack para projetos angular 1.5
``` console
$ touch webpack.config.js
```

Insira o conteúdo abaixo setando os arquivos de input e onde deseja alocar o arquivo de saída
```javascript
// webpack.config.js content
var webpack = require('webpack');
module.exports = {
  entry: './input.js',
  output: {
    path: __dirname + '/js/dist',
    filename: 'bundle.js',
  },
  plugins: [
    new webpack.optimize.UglifyJsPlugin({minimize:true,sourceMap: false,mangle: false})
  ],
};
```
Execute o webpack na pasta do seu projeto
```console
$ webpack
```

Você pode ainda dexá-lo ouvindo as alterações dos seus javacripts mapeados e criando a saída automaticamente, para isso execute:
```console
$ webpack --watch
```
