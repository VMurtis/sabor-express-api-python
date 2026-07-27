# 🍽️ Restaurant API com POO e FastAPI

API de restaurantes desenvolvida em Python, aplicando conceitos de **Programação Orientada a Objetos (POO)** e construção de APIs modernas com **FastAPI**.

O projeto consome dados de uma API externa, organiza as informações e disponibiliza endpoints para consulta de cardápios.

---

## 🚀 Tecnologias utilizadas

- Python 3.x
- FastAPI
- Requests
- Uvicorn
- Pydantic
- Pytest

---

## Programação Orientada a Objetos (POO)

Nesta etapa foi criada a estrutura de classes para representar itens de um cardápio.

### 📌 Conceitos aplicados:

- Abstração (`ABC`, `@abstractmethod`)
- Herança
- Polimorfismo
- Encapsulamento

### 🧩 Estrutura:

- `ItemCardapio` (classe abstrata)
- `Bebida` (herda e aplica 8% de desconto)
- `Prato` (herda e aplica 5% de desconto)

---

## API com FastAPI

A API consome dados externos e fornece endpoints para consulta de restaurantes e cardápios.

---

## ⚙️ Como executar o projeto

Siga os passos abaixo para rodar o projeto localmente:

### ▶️ 1. Clonar o repositório
```bash
git clone https://github.com/VMurtis/sabor-express-api-python.git
```
## ▶️ 2. Ativar ambiente virtual

Após criar a venv, é necessário ativá-la antes de instalar as dependências do projeto.

### Windows

```bash
venv\Scripts\activate
```

## ▶️ 3. Instalar dependências

Com o ambiente virtual ativado, instale todas as bibliotecas necessárias através do arquivo `requirements.txt`.

```bash
pip install -r requirements.txt
```

---

## ▶️ 4. Executar a API

Para iniciar o servidor FastAPI, execute:

```bash
uvicorn app.main:app --reload
```

Após iniciar o servidor, a API ficará disponível localmente para testes.

---

# 📄 Documentação automática

O FastAPI disponibiliza uma documentação interativa utilizando **Swagger UI**, permitindo testar os endpoints diretamente pelo navegador.

Após iniciar a aplicação, acesse:

```
http://127.0.0.1:8000/docs
```

Na documentação será possível:

- Visualizar os endpoints disponíveis
- Testar as requisições diretamente pelo navegador
- Ver os formatos de resposta da API

---

# 🔗 Endpoints

## 📌 Listar restaurantes

Retorna a lista completa de restaurantes disponíveis.

```http
GET /api/restaurantes
```

---

## 🔍 Buscar restaurante

Permite buscar o cardápio de um restaurante específico através do nome informado.

```http
GET http://127.0.0.1:8000/api/restaurantes/?restaurante={nome_do_restaurante}
```

### Exemplo:

```http
GET http://127.0.0.1:8000/api/restaurantes/?restaurante=KFC
```

---

# 💡 Exemplo de resposta

```json
{
  "Restaurante": "KFC",
  "Cardapio": [
    {
      "item": "Limited Time Cinnabon Dessert  Biscuits",
      "price": 58.53,
      "description": "Uma explosão de sabores em cada mordida."
    },
    {
      "item": "Limited Time ORIGINAL RECIPE CHICKEN Chicken Breast",
      "price": 45.72,
      "description": "Sabores autênticos que aquecem o coração."
    },
    {
      "item": "Limited Time ORIGINAL RECIPE CHICKEN Chicken Limited Time Drumstick",
      "price": 30.51,
      "description": "Sabores autênticos que aquecem o coração."
    }
  ]
}
```
