# json-server-base

Esse é o repositório com a base de JSON-Server + JSON-Server-Auth já configurada, feita para ser usada no desenvolvimento das API's nos Capstones do Q2.

## Endpoints

Assim como a documentação do JSON-Server-Auth traz (https://www.npmjs.com/package/json-server-auth), existem 3 endpoints que podem ser utilizados para cadastro e 2 endpoints que podem ser usados para login.

### Cadastro

POST /register <br/>
POST /signup <br/>
POST /users

Qualquer um desses 3 endpoints irá cadastrar o usuário na lista de "Users", sendo que os campos obrigatórios são : 

- Email como "email"
- Senha como "password"
- Nome como "name"
- Idade como "age"

### Login

POST /login <br/>
POST /signin

Qualquer um desses 2 endpoints pode ser usado para realizar login com um dos usuários cadastrados na lista de "Users" sendo que os campos obrigatórios são :

- Email como "email"
- Senha como "password"


### Notes

POST /notes

Para adicionar uma nova nota pessoal use este endpoint, lembre-se de estar logado e de passar o seu userId e dos campos obrigatórios :

- Título como "title"
- Data como "date"
- Descrição como "description"

### Event

POST /events

Eventos podem ter vários usuários mas só o dono pode alterar o evento, lembre-se de estar logado e passar seu userId
LEMBRE-SE DE PASSAR SEU AUTHTOKEN PARA FAZER GET EM NOTES E EVENTS
