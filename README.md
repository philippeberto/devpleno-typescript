"# devpleno-typescript" 

  npm install --save-dev typescript

  npm instal express

  npm install --save-dev @types/express

* Para rodar a aplicação: 

  npx tsc src/index.ts --outDir dist/ --watch

* Para gerar o tsConfig inicia-se a configuração e define-se o diretório root e o destinatário. 

  npx tsc --init --rootDir src --outDir dist

* Também é possível outras configurações como:

  --noImplicitAny true: Impede tipagens com any
  --allowJs true: Permite JavaScript

* Para resolver os scripts de execução do projeto:

  npm install --save-dev ts-node nodemon

  Criar arquivo nodemon.json:
  {
    "watch": [
      "src"
    ],
    "ext": ".ts,.js",
    "ignore": [],
    "exec": "ts-node ./src/index.ts"
  }

* Configuração do "build" e "start"

No arquivo package.json adicionamos os scripts
  "start": "node dist/index.js",
  "build": "tsc"
O build cria os arquivos no diretório dist para produção e o start roda a aplicação que está em produção, no diretório dist.



