# Instalação e configuração do Webpack

### 1-) Instalando o webpack
```bach
yarn add -D webpack webpack-cli babel-loader
```

### 2-) Criar o arquivo de configuração do webpack "webpack.config.js"

webpack.config.js
```js
const path = require('path');

module.exports = {
  mode: 'development',
  entry: path.resolve(__dirname, 'src', 'index.jsx'),
  output: {
    path: path.resolve(__dirname, 'dist'),
    filename: 'bundle.js'
  },
  resolve: {
    extensions: ['.js', '.jsx']
  },
  module: {
    rules: [
      {
        test: /\.jsx$/,
        exclude: /node_modules/,
        use: 'babel-loader'
      }
    ]
  }
}
```

### 3-) Alterar o nome do arquivo "index.js" para "index.jsx"
```
mv index.js index.jsx
```

### 4-) Altera o conteudo do arquivo "index.jsx"
```js
import { App } from './App';
```

### 5-) execute o webpack

```bach
yarn webpack
```

### 6-) Roda o git

```bach
git add .
git commit -m "Github Explorer: install webpack"
```