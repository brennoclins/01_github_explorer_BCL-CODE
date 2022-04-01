# Criando a estrutura de pastas para desenvolvimento de código com ReactJS

### 1) Crie uma pasta com o nome do projeto "github-explorer"
```bach
mkdir github-explorer
```

### 2) Entre na pasta e inicialize o projeto
```bach
yarn init -y

ou 

yarn init
```

### 3) Inicialize o Git para controle de versões
```bach
git init
```

### 4) Instanado o React e o React-Dom
```bach
yarn add react react-dom
```

### 5) Crie um arquivo "gitignore" e ignore a pasta "node_modules" 
```
node_modules/
```

### 6) Crie as pastas "public" e "src"
```bach
mkdir src public
```

### 7) Crie dentro da pasta "public" uma arquivo "index.html" com o seguinte conteudo dentro dele
```html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta http-equiv="X-UA-Compatible" content="IE=edge">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>GitHub Explorer by BCL-ST</title>
</head>
<body>
  
</body>
</html>
```

### 8) Criar documentação "README.md"
```bach
mkdir README_001.md
```

### 9) Crie seu primeiro ponto de versão com o git
```bach
git add .

git commit -m "GitHub Explorer - Starting Project"
```

## Fim :)