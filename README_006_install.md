# Webpack Dev Server

### 1-) Instalar o webpack dev server
```bash
yarn add -D webpack-dev-server
```

### 3-) Configurar no "webpack.config.js" o novo modulo
```js
devServer: {
  static: path.resolve(__dirname, 'public')
},
```

### 4-) Rodar o webpack
```bach
yarn webpack serve
```

### 5-) Acessar o http://localhost:8080

### 6-) Roda o git
```bach
git add .
git commit -m "BCL-CODE: Configuring Webpack Dev Server"
```