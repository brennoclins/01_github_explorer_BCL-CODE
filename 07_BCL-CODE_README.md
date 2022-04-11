# Utilizando source maps

### 1-) Alterar o arquivo "App.jsx"
```bash
export function App() {
  throw new Error('Ops! bugou kkkk');
  return (
    <h1>Ola pessoal da live opa :)</h1>
  )
}
```

### 2-) Rode o webpack dev server
```bach
yarn webpack serve
```

### 3-) Acesso o aplicativo no seu navegador web no endereço: http://localhost:8080

### 4-) Acesso o devtools do navegador web e vou na opção "console"

### 5-) Identifique o erro que com o comando "throw new Error" clique nele

### 6-) Configurar no "webpack.config.js" a funcionalidade source-map
```js
devtool: 'eval-source-map',
```

o arquivo final deve ficar assim:
```js
const path = require('path');
const HtmlWebpackPlugin = require('html-webpack-plugin');

module.exports = {
  mode: 'development',
  devtool: 'eval-source-map',
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

### 7-) Rodar o webpack novamente
```bach
yarn webpack serve
```

### 8-) Abra novamente o aplicativo e clique no erro

### 9-) Roda o git
```bach
git add .
git commit -m "BCL-CODE: Configuring Source Maps"
```