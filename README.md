[# api-connect-lucas-smidt](https://github.com/lucassmidt/api-connect-lucas-smidt

# API Connect

## Objetivo da API
A **API Connect** é um Produto Mínimo Viável (MVP) desenvolvido em Python utilizando o microframework Flask. O seu principal objetivo é fornecer uma arquitetura RESTful robusta, limpa e modular para o gerenciamento e cadastro de usuários, implementando o ciclo CRUD completo com validações rígidas de entrada, tratamento de exceções (como 404 e 400) e respostas padronizadas em formato JSON.

## Tecnologias Utilizadas
* **Python** (Versão 3.x)
* **Flask** (Microframework para rotas e requisições HTTP)
* **Ambiente Virtual (venv)** para isolamento de dependências
* **Git e GitHub** para versionamento de código

## Passo a Passo para Execução Local

Siga os comandos abaixo no seu terminal para clonar, configurar e executar o projeto em sua máquina:

1. **Clone o repositório:**
   ```bash
   git clone [https://github.com/lucassmidt/api-connect-lucas-smidt.git](https://github.com/lucassmidt/api-connect-lucas-smidt.git)
   cd api-connect-lucas-smidt)

Crie e ative o ambiente virtual:

No Windows (PowerShell):Bashpython -m venv venv
venv\Scripts\activate

No Linux/macOS:Bashpython3 -m venv venv
source venv/bin/activate

Instale as dependências:Bashpip install -r requirements.txt
Execute o servidor da aplicação:Bashpython app.py

Documentação de Endpoints

Abaixo estão listadas as rotas configuradas na API, seus respectivos métodos HTTP, códigos de status e exemplos de uso:

Endpoint: /usuarios | Método: GET | Status Esperado: 200 OK

Descrição e Finalidade: Retorna a listagem geral de todos os usuários cadastrados na base de dados em memória.

Endpoint: /usuarios | Método: POST | Status Esperado: 201 Created (ou 400 Bad Request em caso de falha)

Descrição e Finalidade: Cadastra um novo usuário. Exige o envio de nome e email no corpo (JSON). Retorna o código 400 se faltarem campos obrigatórios.

Endpoint: /usuarios/<id> | Método: GET | Status Esperado: 200 OK (ou 404 Not Found se ausente)

Descrição e Finalidade: Busca um usuário específico através do seu ID numérico passado na URL. Retorna o código 404 caso o ID não exista na base.

Endpoint: /usuarios/<id> | Método: PUT | Status Esperado: 200 OK (ou 404 Not Found se ausente)

Descrição e Finalidade: Atualiza os dados cadastrais de um usuário existente com base no ID informado na URL. Retorna o código 404 se o ID for inválido.

Endpoint: /usuarios/<id> | Método: DELETE | Status Esperado: 200 OK (ou 404 Not Found se ausente)

Descrição e Finalidade: Remove o registro do usuário correspondente ao ID informado diretamente da memória do servidor. Retorna o código 404 se não for encontrado.
