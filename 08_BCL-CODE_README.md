# Configurando os ambientes para: desenvolvimento ou produção

### 1-) Alterar o "webpack.config.js" e definir o ambiente que a aplicação esta rodando.
```js
...

const isDevelopment = process.env.NODE_ENV !== 'production';

module.exports = {
  mode: isDevelopment ? 'development' : 'production',
  devtool: isDevelopment ? 'eval-source-map' : 'source-map',

...
```

O arquivo final deve ficar assim:
```js
const path = require('path');
const HtmlWebpackPlugin = require('html-webpack-plugin');
const isDevelopment = process.env.NODE_ENV !== 'production';

module.exports = {
  mode: isDevelopment ? 'development' : 'production',
  devtool: isDevelopment ? 'eval-source-map' : 'source-map',
  entry: path.resolve(__dirname, 'src', 'index.jsx'),
  output: {
    path: path.resolve(__dirname, 'dist'),
    filename: 'bundle.js'
  },
  resolve: {
    extensions: ['.js', '.jsx']
  },
  plugins: [
    new HtmlWebpackPlugin({
      template: path.resolve(__dirname, 'public', 'index.html')
    })
  ],
  devServer: {
    static: path.resolve(__dirname, 'public')
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

### 2-) Instalar "cross-env"
```bach
yarn add cross-env
```

### 3-) Configurar os "scripts" no arquivo "package.json"
```json
"scripts": {
  "dev": "webpack serve",
  "build": "cross-env NODE_ENV=production webpack"
},
```
### 5-) Rodar em ambiente de desenvolvimento ou em produção
```bach
yarn dev
```
ou 

```bach
yarn build
```

### 6-) Roda o git
```bach
git add .
git commit -m "BCL-CODE: Configuring development and production environments"
```