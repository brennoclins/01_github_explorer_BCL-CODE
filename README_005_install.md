# Servindo HTML estático, injetando código javascript no html

### 1-) Remover do arquivo "index.html" a tag "script" que contem o caminho para o nosso "bundle.js"
```html
<script src="../dist/bundle.js"></script>
```

### 2-) Instalar o "html-webpack-plugin"
```bach
yarn add -D html-webpack-plugin
```

### 3-) Configurar no "webpack.config.js" o novo plugin
```js
const HtmlWebpackPlugin = require('html-webpack-plugin');

...
plugins: [
  new HtmlWebpackPlugin({
    template: path.resolve(__dirname, 'public', 'index.html')
  })
],
...

```

### 4-) Rodar o webpack
```bach
yarn webpack
```

### 5-) Roda o git
```bach
git add .
git commit -m "BCL-CODE: Injecting Javascript code into HTML with html-webpack-plugin"
```