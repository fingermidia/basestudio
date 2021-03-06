# Base Studio

O Base Studio é uma API genérica para utilização de base de dados simples. Nela o usuário (desenvolvedor) poderá criar coleções de dados de forma que automaticamente serão gerados os endpoints para acesso externo. A base de tudo é o Restful, conforme padrão (https://pt.wikipedia.org/wiki/REST). Além disso, o gerenciamento das coleções possuem um mínimo de segurança, de forma que o acesso pode ser restrito a um grupo de usuários ou aberto a todos. 

A versão inicial do Base Studio, de forma Beta, está aberta a todos que quiserem utilizar, porém ainda não existe uma interface de administração. Para a criação de usuários, projetos e coleções o desenvolvedor precisa utilizar uma API. Abaixo vamos detalhar o seu funcionamento.

#### URL Base: https://api.basestudio.com.br/v1/

## Criando um Usuário Administrador
```sh
POST account/admin
```
```json
{
  "email": "dirceu@fingermidia.com",
  "password": "senhadousuario",
  "name": "Dirceu Belem"
}
```
Retorno da API
```json
{"id":"4re85qd63lk3i1f6ht5hlf"}
```

### Esqueci minha senha Administrador
```sh
POST account/admin/forgot
```
```json
{
  "email": "dirceu@fingermidia.com"
}
```
Retorno da API
```json
{"code":0,"success":true}
```
