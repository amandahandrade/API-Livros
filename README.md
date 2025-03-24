# Api de Doação de Livros VnW

Esta é uma API simples desenvolvida com Flask e QELite, criada para fins educacionais na escola Vai na Web. Ela permite o cadastro e a listagem de livros doados.

## Como rodar o projeto

1. Faça o clone do repositório
```bash
git clone <https://github.com/amandahandrade/API-Livros>
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
    "image_url":"https://www.google.com/imgres?q=capa%20livro%20dom%20casmurro&imgurl=https%3A%2F%2Fimages.tcdn.com.br%2Fimg%2Fimg_prod%2F1271663%2Fdom_casmurro_edicao_de_luxo_almofadada_89_1_038fb70c564eb50f71ea49f6027e827a.jpg&imgrefurl=https%3A%2F%2Fwww.editoraonline.com.br%2Flivros%2Fdom-casmurro-edicao-de-luxo-almofadada&docid=zL4ph0w3ZNvM1M&tbnid=_Hw9Vf8_pq-ZuM&vet=12ahUKEwjWlZXmwZyMAxUgq5UCHYEcCNEQM3oECBkQAA..i&w=520&h=800&hcb=2&ved=2ahUKEwjWlZXmwZyMAxUgq5UCHYEcCNEQM3oECBkQAA"
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
    "image_url":"https://exemplo.com"
}
```

