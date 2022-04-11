#  Configurando o Babel

### 1) Instala o Babel
```bach
yarn add -D @babel/core @babel/cli @babel/preset-env @babel/preset-react
```

### 2) Criar  o arquivo de configuração do Babel "babel.config.json" ou "babel.config.js"

1 - Conteudo do arquivo "babel.config.json"
```json
{
  "presets": [
    ["@babel/preset-env"],
    ["@babel/preset-react"]
  ]
}
```

ou

2 - Conteudo do arquivo "babel.config.js"
```js
madul.exports = {
  "presets": [
    ["@babel/preset-env"],
     ["@babel/preset-react"]
  ]
}
```
ou 
```js
const presets = [
  ["@babel/preset-env"],
  ["@babel/preset-react"]
]

module.exports = { presets };
```

### 3) Criando arquivo App.jsx

```js
function App() {
  return (
    <h1>Olá pessoal da live :)</h1>
  )
}
```

### 4) Rodando o comando para converter .jsx para .js
```bach
yarn babel src/App.jsx --out-file dist/bundle.js
```

### 5) Rodar git
```
git add .

git commit -m "Github Explorer: installing and configuring babel"
```
