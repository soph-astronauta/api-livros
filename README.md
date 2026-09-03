# api-livros
# 📚 API de Livros

API RESTful para gerenciamento de um acervo de livros, permitindo operações de cadastro, consulta, atualização e remoção.

## 📖 Sobre

Esta API permite gerenciar um catálogo de livros, armazenando informações essenciais como título, autor, ano de publicação e disponibilidade para empréstimo/venda.

## 🗂️ Modelo de Dados

Cada livro é representado pelo seguinte objeto:

| Campo            | Tipo    | Descrição                                   |
|-------------------|---------|----------------------------------------------|
| `id`              | number  | Identificador numérico único                 |
| `titulo`          | string  | Título do livro                              |
| `autor`           | string  | Nome do autor                                |
| `ano_publicacao`  | number  | Ano em que o livro foi publicado             |
| `disponivel`      | boolean | Indica se o livro está disponível            |

### Exemplo de objeto

```json
{
  "id": 1,
  "titulo": "Dom Casmurro",
  "autor": "Machado de Assis",
  "ano_publicacao": 1899,
  "disponivel": true
}
```

## 🚀 Endpoints

### Listar todos os livros

```
GET /livros
```

**Resposta**

```json
[
  {
    "id": 1,
    "titulo": "Dom Casmurro",
    "autor": "Machado de Assis",
    "ano_publicacao": 1899,
    "disponivel": true
  }
]
```

### Buscar livro por ID

```
GET /livros/:id
```

**Resposta**

```json
{
  "id": 1,
  "titulo": "Dom Casmurro",
  "autor": "Machado de Assis",
  "ano_publicacao": 1899,
  "disponivel": true
}
```

### Cadastrar novo livro

```
POST /livros
```

**Body**

```json
{
  "titulo": "O Cortiço",
  "autor": "Aluísio Azevedo",
  "ano_publicacao": 1890,
  "disponivel": true
}
```

**Resposta**

```json
{
  "id": 2,
  "titulo": "O Cortiço",
  "autor": "Aluísio Azevedo",
  "ano_publicacao": 1890,
  "disponivel": true
}
```

### Atualizar livro existente

```
PUT /livros/:id
```

**Body**

```json
{
  "titulo": "O Cortiço",
  "autor": "Aluísio Azevedo",
  "ano_publicacao": 1890,
  "disponivel": false
}
```

### Remover livro

```
DELETE /livros/:id
```

**Resposta**

```json
{
  "mensagem": "Livro removido com sucesso."
}
```

## ⚙️ Tecnologias utilizadas

- Node.js
- Express
- (adicione aqui o banco de dados e demais libs utilizadas)

## ▶️ Como executar o projeto

```bash
# Clonar o repositório
git clone https://github.com/seu-usuario/api-livros.git

# Acessar a pasta do projeto
cd api-livros

# Instalar dependências
npm install

# Executar a aplicação
npm start
```

A API estará disponível em `http://localhost:3000`.

## 📌 Códigos de status

| Código | Descrição                          |
|--------|-------------------------------------|
| 200    | Requisição bem-sucedida             |
| 201    | Recurso criado com sucesso          |
| 400    | Requisição inválida                 |
| 404    | Recurso não encontrado              |
| 500    | Erro interno do servidor            |

## 📄 Licença

Este projeto está sob a licença MIT.
