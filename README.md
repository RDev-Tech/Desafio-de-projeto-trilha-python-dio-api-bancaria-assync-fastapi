# 🏦 Desafio: API Bancária Assíncrona com FastAPI

[![Python](https://img.shields.io/badge/python-3.11+-blue.svg)](https://www.python.org/)
[![FastAPI](https://img.shields.io/badge/FastAPI-0.100.0+-05998b.svg)](https://fastapi.tiangolo.com/)
[![SQLAlchemy](https://img.shields.io/badge/SQLAlchemy-2.0+-red.svg)](https://www.sqlalchemy.org/)
[![PostgreSQL](https://img.shields.io/badge/PostgreSQL-15+-336791.svg)](https://www.postgresql.org/)

Este projeto foi desenvolvido como parte do desafio de projeto da trilha **Python AI Backend Developer** da **Digital Innovation One (DIO)**. O objetivo foi construir uma API robusta, performática e totalmente assíncrona para gerenciamento bancário/financeiro, utilizando as melhores práticas de desenvolvimento com FastAPI.

## 🎯 Objetivo do Desafio
O foco principal foi implementar o padrão **CRUD** (Create, Read, Update, Delete) para entidades do sistema, garantindo a integridade dos dados e a alta disponibilidade através de operações assíncronas (`async/await`).

## 🛠️ Tecnologias e Ferramentas
* **Python 3.11+**: Linguagem base.
* **FastAPI**: Framework web moderno de alta performance.
* **Pydantic v2**: Validação de dados e criação de schemas.
* **SQLAlchemy 2.0**: ORM para interação com o banco de dados (modo assíncrono).
* **Alembic**: Gerenciamento de migrações do banco de dados.
* **PostgreSQL**: Banco de dados relacional.
* **Docker & Docker Compose**: Containerização do ambiente de desenvolvimento.

## 🚀 Como Executar o Projeto

### Pré-requisitos
* [Docker](https://www.docker.com/) e [Docker Compose](https://docs.docker.com/compose/) instalados.

### Passo a Passo
1.  **Clonar o repositório:**
    ```bash
    git clone [https://github.com/SEU_USUARIO/NOME_DO_REPO.git](https://github.com/SEU_USUARIO/NOME_DO_REPO.git)
    cd NOME_DO_REPO
    ```

2.  **Subir os serviços (Banco de Dados):**
    ```bash
    docker-compose up -d
    ```

3.  **Configurar o ambiente Python (opcional se rodar local):**
    ```bash
    python -m venv venv
    source venv/bin/activate  # Linux/Mac
    # ou
    venv\Scripts\activate     # Windows
    pip install -r requirements.txt
    ```

4.  **Executar Migrações:**
    ```bash
    alembic upgrade head
    ```

5.  **Iniciar a API:**
    ```bash
    uvicorn workout_api.main:app --reload
    ```
    A API estará disponível em `http://127.0.0.1:8000`.

## 📖 Documentação da API
Uma das grandes vantagens do FastAPI é a documentação automática. Com o servidor rodando, acesse:
* **Swagger UI:** `http://127.0.0.1:8000/docs`
* **Redoc:** `http://127.0.0.1:8000/redoc`



## 🧠 O que eu aprendi?
Durante o desenvolvimento deste desafio, pude consolidar conhecimentos em:
* **Programação Assíncrona:** Diferença entre chamadas síncronas e assíncronas e como o `asyncio` otimiza o I/O no Python.
* **Modelagem de Dados:** Criação de modelos relacionais eficientes com SQLAlchemy.
* **Tratamento de Exceções:** Implementação de handlers para capturar erros de banco de dados (como duplicidade de campos) e retornar respostas HTTP adequadas.
* **Paginação e Filtros:** Implementação de parâmetros de consulta para facilitar a busca de grandes volumes de dados.
