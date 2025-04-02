# Api de Doação de Livros VnW

Esta é uma API simples desenvolvida com Flask e SQLite, criada para fins educacionais na escola Vai na Web. Ela permite o cadastro e a listagem de livros doados.

## Como rodar o projeto

1. Faça o clone do repositório
```bash
git clone link do repositório
cd nome-do-projeto
```

2. Crie um ambiente virtual (obrigatório):
```bash
python -m venv venv
source venv/Scripts/activate
```

3. Instale as dependências:
```bash
pip install -r requirements.txt
```

4. Inicie o servidor:
```bash
A API estará disponível em http://127.0.0.1:5000/
```

---

## Endpoints

### POST /doar

O endpoint /doar é utilizado para cadastrar um novo livro em nossa API.

**Envio de informações (JSON)**
```json
{
    "titulo":"Dom Casmurro",
    "categoria":"Romance Realista",
    "autor":"Machado de Assis",
    "image_url":"https://..."
}
```

**Resposta (201)**
```json
    "mensagem":"Livro cadastrado com sucesso!"
```

### GET /livros

O endpoint /livros retorna todos os livros cadastrados na API.

**Resposta (200):**
```json
{
    "id":"1",
    "titulo":"Ainda estou devendo aqui",
    "categoria":"Finanças",
    "autor":"Fernando Polia",
    "image_url":"https://..."
}
```