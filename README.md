# 💻 Desafio de projeto - Trilha .NET | Integrando APIs NET Csharp com Entity Framework

### Desafio de projeto
Para este desafio, precisei usar meus conhecimentos adquiridos no módulo de APIs, da trilha .NET da [DIO](https://www.dio.me).

## 💼 Contexto
Preciso construir um sistema gerenciador de tarefas, onde o usuário poderá cadastrar uma lista de tarefas que permitirá organizar melhor a sua rotina.

Essa lista de tarefas precisa ter um CRUD, ou seja, deverá permitir ao usuário obter os registros, criar, salvar e deletar esses registros.

A aplicação deverá ser do tipo Web API ou MVC. Nesse caso, desenvolvi uma Web API.

A classe principal, a classe de tarefa, deve ser a seguinte:

![Diagrama da classe Tarefa](diagrama.png)

## Métodos esperados
É esperado tenha os métodos conforme a seguir:


**Swagger**


![Métodos Swagger](swagger.png)


**Endpoints**


| Verbo  | Endpoint                | Parâmetro | Body          |
|--------|-------------------------|-----------|---------------|
| GET    | /Tarefa/{id}            | id        | N/A           |
| PUT    | /Tarefa/{id}            | id        | Schema Tarefa |
| DELETE | /Tarefa/{id}            | id        | N/A           |
| GET    | /Tarefa/ObterTodos      | N/A       | N/A           |
| GET    | /Tarefa/ObterPorTitulo  | titulo    | N/A           |
| GET    | /Tarefa/ObterPorData    | data      | N/A           |
| GET    | /Tarefa/ObterPorStatus  | status    | N/A           |
| POST   | /Tarefa                 | N/A       | Schema Tarefa |

Esse é o schema (model) de Tarefa, utilizado para passar para os métodos que exigirem

```json
{
  "id": 0,
  "titulo": "string",
  "descricao": "string",
  "data": "2022-06-08T01:31:07.056Z",
  "status": "Pendente"
}
```


## ✅ Solução
Implementei todas tarefas listadas no TODO dentro do código que estava pela metade. Agora o sistems gerenciador de tarefas se encontra funcional e é possível cadastrar tarefas, editar, deletar e procurar. 