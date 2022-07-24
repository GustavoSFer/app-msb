# Seja Muito Bem Vindo!!! - app-msb
<p>Uso exclusivo para a empresa MSB</p>

  * Hospedado no heroku: https://msb-front.herokuapp.com/

## TECNOLOGIAS UTILIZADOS
<ul>
  <li>React</li>
  <li>React-router-dom</li>
  <li>Dotenv</li>
  <li>React test library</li>
  <li>Axios</li>
  <li>Node.js</li>
  <li>Express</li>
  <li>MySql</li>
  <li>Mocha | Chai | Sinon.js </li>
</ul>

## Habilidades
<ul>
  <li>Criação de uma pagina de envio de formulário</li>
  <li>Validações de campos</li>
  <li>Informações salvas, como Ip e data e hora do envio</li>
  <li>Validação do formato do arquivo</li>
</ul>


# Instruções para iniciar o projeto

1. Clone o repositório
  * Chave SSH
    * `git clone git@github.com:GustavoSFer/app-msb.git`
  * Entre na pasta do repositório que você acabou de clonar:
    * `cd app-msb`

2. Instale as dependências e inicialize o projeto
  * Instale as dependências:
    * `npm install`
  * Inicialize o projeto:
    * `npm start`

## Rodando os testes
1. Teste Front-end
    * npm run test:front
2. Teste Back-end
    * npm run test:back

## Utilizando o projeto com o Docker
  * Obs: Cada repositório tem o seu Dockerfile. Entrar no Readme de cada um para seguir os passos.

#### Observação: O Banco de dados Utilizado no projeto é o MySQL. Certifique-se que ja tenha em seu computador ou rodando em um container Docker.
 -- Link: https://hub.docker.com/_/mysql

## Configurando variavel de ambiente API
  * Crie um arquivo .env e informe nele a URL do banco
  ``` REACT_APP_API_URL=https://.... ```
<p>
  Se não foi informado por padão será utilizado 'http://localhost:3001'
</p>

**⚠️ IMPORTANTE! ⚠️**
# Configurações necessarias para o Back-End

### Conexão com o Banco:

**⚠️ IMPORTANTE! ⚠️**

```javascript
const connection = mysql.createPool({
  username: process.env.MYSQL_USER,
  password: process.env.MYSQL_PASSWORD,
  database: process.env.MYSQL_DATABASE,
  host: process.env.MYSQL_HOST,
});
```
Para rodar corretamente, na raiz do projeto **renomeie o arquivo `.env.example` para `.env`** com as variáveis de ambiente. Por exemplo, caso o seu usuário SQL seja `nome` e a senha `1234` seu arquivo ficará desta forma:

```sh
MYSQL_HOST=localhost
MYSQL_USER=nome
MYSQL_PASSWORD=1234
PORT=3001
```

#### Projeto no back-end não tem um banco online, neste caso o banco MySQL é utilizado do computador do usuario.
