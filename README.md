# AtariBoot

**AtariBoot** é o backend de uma loja de games desenvolvido em Spring Boot. Este projeto tem como objetivo implementar funcionalidades CRUD para gerenciar Produtos e Categorias, além de configurar o relacionamento entre essas entidades.  

<br>

## Tecnologias Utilizadas  
- **Java 17**  
- **Spring Boot 3.x**  
- **Spring Data JPA**  
- **MySQL**  
- **Maven**  

<br>

# Estrutura do Projeto

## Camadas do Sistema
O projeto foi estruturado em camadas de acordo com as boas práticas do Spring:

- **Model**: Classes que representam os dados do sistema.
- **Repository**: Interface responsável pela interação com o banco de dados.
- **Controller**: Define os endpoints da API e gerencia as requisições.

<br>

## Estrutura de Pacotes

Abaixo está a estrutura de pacotes do projeto:
```
src/main/java/com/generation/atariboot
├── controller
│   ├── ProdutoController.java
│   └── CategoriaController.java
├── model
│   ├── Produto.java
│   └── Categoria.java
├── repository
│   ├── ProdutoRepository.java
│   └── CategoriaRepository.java
```
Essa estrutura segue o padrão de separação de responsabilidades, tornando o código mais organizado e fácil de manter.

<br>

## Endpoints da API

### Produto

<table>
  <tr>
    <th>Método</th>
    <th>Endpoint</th>
    <th>Descrição</th>
  </tr>
  <tr>
    <td>POST</td>
    <td>/produtos</td>
    <td>Cadastrar um novo produto.</td>
  </tr>
  <tr>
    <td>GET</td>
    <td>/produtos</td>
    <td>Listar todos os produtos.</td>
  </tr>
  <tr>
    <td>GET</td>
    <td>/produtos/{id}</td>
    <td>Buscar produto pelo ID.</td>
  </tr>
  <tr>
    <td>PUT</td>
    <td>/produtos</td>
    <td>Atualizar um produto existente.</td>
  </tr>
  <tr>
    <td>DELETE</td>
    <td>/produtos/{id}</td>
    <td>Deletar produto pelo ID.</td>
  </tr>
</table>

### Categoria

<table>
  <tr>
    <th>Método</th>
    <th>Endpoint</th>
    <th>Descrição</th>
  </tr>
  <tr>
    <td>POST</td>
    <td>/categorias</td>
    <td>Cadastrar uma nova categoria.</td>
  </tr>
  <tr>
    <td>GET</td>
    <td>/categorias</td>
    <td>Listar todas as categorias.</td>
  </tr>
  <tr>
    <td>GET</td>
    <td>/categorias/{id}</td>
    <td>Buscar categoria pelo ID.</td>
  </tr>
  <tr>
    <td>PUT</td>
    <td>/categorias</td>
    <td>Atualizar uma categoria existente.</td>
  </tr>
  <tr>
    <td>DELETE</td>
    <td>/categorias/{id}</td>
    <td>Deletar categoria pelo ID.</td>
  </tr>
</table>

<br>

## Exemplo de Requisição

### 1. Criar Produto (`POST /produtos`)

**Request Body:**
```json
{
    "nome": "Controle",
    "descricao": "Controle sem fio",
    "preco": 199.99,
    "categoria": {
        "id": 1
    }
}
```

<br>

