# Configurando o ReactJS no projeto

### 1-) Alterar o arquivo "index.html"
```html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta http-equiv="X-UA-Compatible" content="IE=edge">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Gihub Explorer</title>
</head>
<body>
  <div id="root"></div>

  <script src="../dist/bundle.js"></script>
</body>
</html>
```

### 2-) Alterar o arquivo "index.jsx" e o arquivo "App.jsx"
```js
import { render } from 'react-dom';

import { App } from './App';

render(<App />, document.getElementById('root'));
```

```js
export function App() {
  return (
    <h1>ReactJS :)</h1>
  )
}
```

### 3) Alterar o arquivo "babel.config.json"
```json
{
  "presets": [
    ["@babel/preset-env"],
    ["@babel/preset-react", {
      "runtime": "automatic"
    }
    ]
  ]
}
```

### 4) Rode o webpack
```bach
yarn webpack
```

### 5) Abrir o arquivo "index.html"

### 6) rode o git
```bach
git add .
git commit -m "Github Explorer: configuring ReactJS in our project"
```