# Testes

> 1 passo : Adicionar o Jest no projeto como depedência de desenvolvimento

`$ yarn add jest @types/jest -D`

<br>

> 2 passo : Reponder as perguntas solicitadas após o comando de instalação

`$ yarn jest --init`

```
The following questions will help Jest to create a suitable configuration for your project 

- Would you like to use Jest when running "test" script in "package.json"? > (Y/n) : Yes

- Would you like to use Typescript for the configuration file? > (Y/n) : Yes

- Choose the test environment that will be used for testing
  (x) node 
  () jsdom (browser-like) 
  
- Do you want Jest to add coverage reports? (Y/n) : Not

- Which provider should be used to instrument code for coverage?
  (x) v8
  () babel
  
- Automatically clear mock call and instances between every test? > (Y/n) : Yes
```

- Após o passo 2 é criado um arquivo (jest.config.ts) no projeto que por sua vés é um arquivo de configurações do jest.

> Configurações no arquivo jest.config.ts

```
bail: true,
testMatch: ["**/*.spec.ts"]
```
- bail : uma opção para , parar ou não após o primeiro erro encontrado.

<br><br>

## Adicionando o Typescript

> Instalando e configurando o typescript nos testes

`$ yarn add ts-jest -D`

- No arquivo de configurações do jest, deve descomentar a propiedade preset <br> e trocar de undefined para "ts-jest"

<br><br>

## Inserindo o supertest para teste de integração

> Instalando e configurando o supertest no projeto

`$ yarn add supertest @types/supertest -D`

<br><br>

## Configurando o Coverage Report

> O coverage é uma ferramenta para realizar um mapeamentos dos testes que foram feitos e os que não foram realizados.

- No arquivo jest.config.ts deve ser alterados os atributos abaixo.

```
collectCoverage : true,
collectCoverageFrom: [ "<rootDir>/src/modules/**/useCases/**/*.ts" ],
coverageDirectory: 'coverage',
coverageReports: ["text-sumary", "lcov"]
```




