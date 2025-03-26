# Api de Doação de Livros VnW

Esta é uma API simples feita com Flask e SQLite
para fins de estudo na escola Vai na Web, que
permite cadastrar e listar os livros doados.

## Como rodar o projeto

1. Clone o repositório
```bash
git clone <https://github.com/DWN0/API-Livros-Vai-Na-Web>
cd API-Livros-Vai-Na-Web
```

2. Crie um ambiente virtual (Obrigatório):
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
python app.py
```

> A API estará disponível em http://127.0.0.1:5000/

---

## Endpoints

### POST /doar

O endpoint /doar é utilizado para cadastrar um
novo livro em nossa API.

**Envio informações (JSON):**
```json
{
    "titulo":"Exemplo",
    "categoria":"Exemplo",
    "autor":"Exemplo",
    "image_url":"https://exemplo.com"
}
```

**Resposta (201):**
```json
{
    "mensagem":"Livro cadastrado com sucesso!"
}
```

---

### GET /livros

O endepoint /livros retorna todos os livros
cadastrados na API.

**Resposta (200):**
```json
{
    "id":"1",
    "titulo":"Exemplo",
    "categoria":"Exemplo",
    "autor":"Exemplo",
    "image_url":"https://exemplo.com"
}
```

---