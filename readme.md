# Documentação
https://www.typescriptlang.org/pt/
https://www.typescriptlang.org/pt/docs
https://www.typescriptlang.org/pt/docs/handbook/typescript-from-scratch.html

# Configurando Typescript globalmente
npm i -g typescript

# Iniciando o Node.js
npm init --y  
Ao iniciar o Node.js será instalado um arquivo chamado package.json, que é responsável por gerenciar as dependências do projeto.

# Instalando duas dependências de desenvolvimento
npm i -D typescript
Será criado dentro do package.json  um bloco chamado "scripts" onde poderemos executar os scripts que quisermos.

npm i -D ts-node-dev

# Inixiando o tyscript do projeto
npx tsc --init
O arquivo "tsconfig.json" é criado na raiz do projeto

# Executar um script TypeScript com ts-node-dev
npx tsc app.ts
o arquivo app.ts é transplilado  para js e executado pelo node, mas sem recarga automática

# Para não ficar transpilando  todo o tempo, usamos a ferramenta ts-node-dev que faz isso por nós:
# Temos que instalar uma depedência para poder rodar
npm i -D ts-node

# Dentro do package.json você acrescenta
"scripts": {
    "dev" : "ts-node-dev app.ts",    
},

# Agora você pode executar
npm run dev
Ele roda o arquivo .ts sem precisar transpilar para javascript toda vez, somente quando quiser colocar em produção