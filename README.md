# Desafio Técnico - Desenvolvedora Back-end (Estágio)

Bem-vinda ao nosso desafio técnico! Esse teste foi criado para avaliar suas habilidades em Python para uma posição Back-end. Aqui, você encontrará uma série de exercícios que envolvem lógica de programação, manipulação de dados, interações com APIs, manipulação de bancos de dados e automação de tarefas.

Abaixo estão as instruções e os requisitos para cada parte do desafio. Boa sorte!

## 📋 Sumário

1. [Objetivo](#-objetivo)
2. [Instruções](#-instruções)
3. [Desafios](#-desafios)
   - [1. Lógica de Programação e Manipulação de Dados](#1-lógica-de-programação-e-manipulação-de-dados)
   - [2. Operações com APIs RESTful](#2-operações-com-apis-restful)
   - [3. CRUD Simples com Banco de Dados](#3-crud-simples-com-banco-de-dados)
   - [4. Automação de Tarefas](#4-automação-de-tarefas)
   - [5. Validação de Dados](#5-validação-de-dados)
4. [Observações](#-observações)
5. [Entrega](#-entrega)

## 🎯 Objetivo

Este desafio é dividido em cinco partes e foi desenvolvido para testar suas habilidades com:

- Lógica de programação e manipulação de dados
- Interação com APIs RESTful
- Operações de CRUD com bancos de dados
- Automação de tarefas
- Validação de dados

## 🚀 Instruções

1- **Clone este repositório** para o seu ambiente de desenvolvimento. (Recomendamos usar o [VSCode](https://code.visualstudio.com/))

```bash
git clone https://github.com/v1cferr/teste-tecnico-python.git
```

2- Crie um ambiente virtual para isolar suas dependências, e instale as bibliotecas necessárias (ex.: `requests` para chamadas de API e `sqlite3` para operações de banco de dados).
3- Siga as instruções de cada exercício para implementar as funcionalidades pedidas.
4- Organize seu código em funções e mantenha as instruções no arquivo `README.md` claras e fáceis de seguir.

## 🧩 Desafios

### 1. Lógica de Programação e Manipulação de Dados

**Objetivo**: Criar uma função para encontrar o produto mais caro e o mais barato em um dicionário.

**Tarefa**:

- Crie uma função chamada `encontra_precos` que receba um dicionário de produtos com preços.
- Exemplo de entrada: `{'produto1': 30.50, 'produto2': 20.00, 'produto3': 15.75}`
- A função deve retornar uma tupla com o produto mais caro e o mais barato. Exemplo de saída: `('produto1', 'produto3')`.

**Exemplo de uso**:

```python
produtos = {'produto1': 30.50, 'produto2': 20.00, 'produto3': 15.75}
mais_caro, mais_barato = encontra_precos(produtos)
print("Mais caro:", mais_caro)
print("Mais barato:", mais_barato)
```

### 2. Operações com APIs RESTful

**Objetivo**: Realizar requisições a uma API pública.

**Tarefa**:

- Crie um script `consulta_personagem.py` que consuma a [API de Star Wars (SWAPI)](https://swapi.dev).
- O script deve aceitar um ID como entrada, buscar os dados do personagem, e retornar o `nome` e o `planeta de origem`.
- Exemplo de chamada: `python consulta_personagem.py 1`
  - Exemplo de saída: `Personagem: Luke Skywalker, Planeta: Tatooine`

**Dicas**:

- Utilize a biblioteca `requests` para fazer requisições HTTP.
- Trate exceções para garantir que o script funcione mesmo se a API não responder.

### 3. CRUD Simples com Banco de Dados

**Objetivo**: Implementar operações básicas de CRUD em um banco de dados SQLite.

**Tarefa**:

- Crie um arquivo `banco_de_usuarios.py` que implemente um CRUD simples para uma tabela `usuarios`.
- Estrutura da tabela `usuarios`:
  - `id`: Inteiro, chave primária, autoincremento
  - `nome`: Texto
  - `email`: Texto
- Implemente as funções:
  - `adicionar_usuario(nome, email)`
  - `atualizar_usuario(id, nome, email)`
  - `obter_usuario(id)`
  - `deletar_usuario(id)`

**Exemplo de uso**:

```python
# Exemplo de criação e inserção
adicionar_usuario("Maria", "maria@email.com")
```

**Dicas**:

- Use `sqlite3` para conectar ao banco.
- Não se esqueça de incluir verificações de erro e garantir que o banco seja fechado ao final da execução.

### 4. Automação de Tarefas

**Objetivo**: Ler dados de um arquivo `.csv` e gerar um relatório.

**Tarefa**:

- Crie um script `relatorio_estoque.py` que leia um arquivo `produtos.csv` contendo dados no seguinte formato:

  ```csv
  nome,preco,estoque
  produto1,30.50,10
  produto2,20.00,3
  produto3,15.75,0
  ```

- Gere um relatório `relatorio.txt` listando apenas os produtos com estoque menor que 5.

**Exemplo de saída**:

```txt
Produtos com estoque baixo:
- produto2 (Estoque: 3)
- produto3 (Estoque: 0)
```

**Dicas**:

- Utilize a biblioteca `csv` para ler o arquivo e `open()` para gerar o relatório em `.txt`.
- Use condicionais para filtrar os produtos com estoque baixo.

### 5. Validação de Dados

**Objetivo**: Verificar a validade de um endereço de e-mail.

**Tarefa**:

- Crie uma função chamada `validar_email` que recebe um endereço de e-mail e verifica se ele é válido.
- Um e-mail válido deve:
  - Conter o caractere `@`
  - Conter um domínio (ex.: `.com`, `.org`, `.net`)
- Retorne `True` se o e-mail for válido ou `False` caso contrário.

**Exemplo de uso**:

```python
print(validar_email("exemplo@dominio.com"))  # Saída: True
print(validar_email("exemplo.com"))          # Saída: False
```

**Dicas**:

- Utilize a biblioteca `re` para trabalhar com expressões regulares (opcional).

## 📌 Observações

- **Documentação**: Mantenha seu código bem documentado, explicando funções e parâmetros.
- **Boas Práticas**: Use boas práticas de programação (nomes claros, organização de código e modularização).
- **Tratamento de Erros**: Inclua tratamento de erros onde for possível para evitar que o script quebre.

## 📬 Entrega

1. Organize todos os arquivos dentro do repositório.
2. Atualize este `README.md` com instruções sobre como rodar cada um dos scripts.
3. Envie o link do repositório para nosso [e-mail](mailto:victor.ferreira@xmartsolutions.com.br) com o assunto "Desafio Técnico - Estágio Back-end".

Boa sorte e esperamos que você aproveite este desafio! 🚀
