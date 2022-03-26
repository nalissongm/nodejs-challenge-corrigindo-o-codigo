# Requisitos

### GET `/repositories`

- [x] Deve retornar uma lista contendo todos os repositórios cadastrados.

### POST `/repositories`

- [x] Deve receber `title`, `url` e `techs` pelo corpo da requisição.
- [x] Deve retornar um objeto com as informações do repositório criado e um status `201`.

### PUT `/repositories/:id`

- [x] Deve receber `title`, `url` e `techs` pelo corpo da requisição.
- [x] Deve receber `id` do repositório que deve ser atualizado pelo parâmetro da rota.
- [x] Deve alterar apenas as informações recebidas pelo corpo da requisição e retornar esse repositório atualizado.

### DELETE `/repositories/:id`

- [x] Deve receber, pelo parâmetro da rota, o `id` do repositório que deve ser excluído.
- [x] Deve retornar um status `204` após a exclusão.

### POST `/repositories/:id/like`

- [x] Deve receber, pelo parâmetro da rota, o `id` do repositório que deve receber o like.
- [x] Deve retornar o repositório com a quantidade de likes atualizada.

# Testes

### Repositórios

- [x] Should be able to create a new repository => status code `201`.
- [x] Should be able to list the projects.
- [x] Should be able to update repository.
- [x] Should not be able to update a non existing repository => status code `404` and `{ error: "Mensagem do erro" }`.
- [x] Should not be able to update repository likes manually.
- [x] Should be able to delete the repository.
- [x] Should not be able to delete a non existing repository => status code `404` and `{ error: "Mensagem do erro" }`.

### Likes

- [x] Should be able to give a like to the repository.
- [x] Should not be able to give a like to a non existing repository => status code `404` and `{ error: "Mensagem do erro" }`.
