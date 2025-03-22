# API de Cadastro de Livros - Desafio Vai na Web

Este projeto é a implementação de uma API RESTful simples, desenvolvida com **Python** e **Flask**, para cadastrar e listar livros em um banco de dados **SQLite3**. O objetivo é aplicar os conceitos de desenvolvimento web, manipulação de dados com SQLite3 e boas práticas na construção de APIs.

---

## 🎯 Desafio

O objetivo deste projeto é criar uma API que permita:

1. **Cadastrar um livro** no banco de dados (POST na rota `/doar`).
2. **Listar todos os livros** cadastrados (GET na rota `/livros`).
3. **Exibir uma página inicial** personalizada (GET na rota `/`).

---

## ⚙️ Requisitos Técnicos

1. Utilizar **Flask** para criar as rotas.
2. Utilizar **SQLite** como banco de dados.
3. A tabela do banco de dados deve ser chamada **LIVROS** e conter os seguintes campos:
   - **id** (chave primária, autoincrementada)
   - **titulo** (texto, obrigatório)
   - **categoria** (texto, obrigatório)
   - **autor** (texto, obrigatório)
   - **image_url** (texto, obrigatório)
4. Ao cadastrar um novo livro, a API deve retornar uma resposta **JSON** com o código **201** confirmando o cadastro.
5. A rota `GET /livros` deve retornar todos os livros cadastrados no banco de dados, organizados em um **JSON** com:
   - **id**
   - **titulo**
   - **categoria**
   - **autor**
   - **image_url**
6. A rota inicial (`/`) deve exibir uma mensagem personalizada à sua escolha.

---

## 🛠 Tecnologias Utilizadas

- Python
- Flask
- SQLite3
- JSON

---

## 🔧 Detalhes Adicionais

No código da API, utilizei o método `json.dumps()` com as opções `sort_keys=False` e `ensure_ascii=False` para garantir que os livros retornados pela rota /livros sejam exibidos de forma correta, sem alterar a ordem original dos dados e permitindo a exibição de caracteres especiais.

---

## 🚀 Como Rodar o Projeto

1. Clone este repositório para a sua máquina local:

   ```bash
   git clone https://github.com/seu-usuario/nome-do-repositorio.git
