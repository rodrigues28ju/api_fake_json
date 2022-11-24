
# Api Rest Simples Fake com json-server

## Procedimento de instalação

* Criar uma pasta e colocar o nome desejado
* npm init -y
* npm i json-server

* Criar o arquivo db.json que será usado como o 'banco de dados'

* No package.json na parte scripts "dev": "json-server --watch db.json --port 3000" e apague o anterior que ja existe lá.

* Para executar, basta digitar npm run dev 

* Criar um arquivo: server.js

 Inserir o js da documentação no server.js:

// server.js

const jsonServer = require('json-server')

const server = jsonServer.create()


const router = jsonServer.router('db.json'
)

const middlewares = jsonServer.defaults()


server.use(middlewares)


server.use(router)

server.listen(3000, () => {
  console.log('JSON Server is running')
})

* No Terminal, inserir o comando da documentação para executar o JS acima:

  npm install json-server --save-dev        //Instalação do servidor local


 * Executar o comando no terminal  para execução do node:

 node server.js


### VERBOS HTTP

- GET: Receber dados de um Resource.
- POST: Enviar dados ou informações para serem processados por um Resource.
- PUT: Atualizar dados de um Resource.
- DELETE: Deletar um Resource

### STATUS DAS RESPOSTAS


1xx Informativo

   - 100 Continue
   - 101 Switching Protocols
   - 102 Processing

2xx Sucesso

   - 200 OK
   - 201 Created
   - 202 Accepted
   - 203 Non-authoritative Information
   - 204 No Content
   - 205 Reset Content
   - 206 Partial Content
   - 207 Multi-Status
   - 208 Already Reported
   - 226 IM Used

3xx Redirecionamento

   - 300 Multiple Choices
   - 301 Moved Permanently
   - 302 Found
   - 303 See Other
   - 304 Not Modified
   - 305 Use Proxy
   - 307 Temporary Redirect
   - 308 Permanent Redirect

4xx Erro no Cliente

   - 400 Bad Request
   - 401 Unauthorized
   - 402 Payment Required
   - 403 Forbidden
   - 404 Not Found
   - 405 Method Not Allowed
   - 406 Not Acceptable
   - 407 Proxy Authentication Required
   - 408 Request Timeout
   - 409 Conflict
   - 410 Gone
   - 411 Length Required
   - 412 Precondition Failed
   - 413 Payload Too Large
   - 414 Request-URI Too Long
   - 415 Unsupported Media Type
   - 416 Requested Range Not Satisfiable
   - 417 Expectation Failed
   - 418 I'm a teapot
   - 421 Misdirected Request
   - 422 Unprocessable Entity
   - 423 Locked
   - 424 Failed Dependency
   - 426 Upgrade Required
   - 428 Precondition Required
   - 429 Too Many Requests
   - 431 Request Header Fields Too Large
   - 444 Connection Closed Without Response
  -  451 Unavailable For Legal Reasons
  - 499 Client Closed Request

5xx Erro no Servidor

   - 500 Internal Server Error
   - 501 Not Implemented
   - 502 Bad Gateway
   - 503 Service Unavailable
   - 504 Gateway Timeout
   - 505 HTTP Version Not Supported
   - 506 Variant Also Negociates
   - 507 Insufficient Storage
   - 508 Loop Detected
   - 510 Not Extended
   - 511 Network Authentication Required
   - 599 Network Connection Timeout Error
   
   * no projeto foi ultizidado o Postman para o teste da Api
   
   
   [![Run in Postman](https://run.pstmn.io/button.svg)](https://app.getpostman.com/run-collection/24581722-39fd6a49-72f5-4b3b-87e5-3a1e06424c7f?action=collection%2Ffork&collection-url=entityId%3D24581722-39fd6a49-72f5-4b3b-87e5-3a1e06424c7f%26entityType%3Dcollection%26workspaceId%3Dd3a8a28d-f7dd-4f5d-8393-7f0b8a995168)
