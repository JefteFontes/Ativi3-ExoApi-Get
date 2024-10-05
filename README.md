# Atividade 04E - CRUD de Usuários

## Descrição
Este branch implementa o CRUD de usuários. A funcionalidade permite criar, ler, atualizar e excluir usuários na API.

## Requisitos
- Editor de código: Visual Studio Code
- SDK .NET: versão 6 ou 7
- Banco de dados: SQL Server (use o script `cria-db.sql` para criar o banco de dados)

## Funcionalidades Implementadas
1. **Criação de Usuários**: Permite adicionar novos usuários.
2. **Leitura de Usuários**: Consulta e exibe usuários armazenados no banco de dados.
3. **Atualização de Usuários**: Edita as informações de um usuário existente.
4. **Exclusão de Usuários**: Remove um usuário do banco de dados.

## Como Testar
Use o aplicativo Insomnia ou Postman para testar as funcionalidades do CRUD:

- **POST** `/api/usuarios`: Adiciona um novo usuário.
- **GET** `/api/usuarios`: Retorna a lista de usuários.
- **PUT** `/api/usuarios/{id}`: Atualiza um usuário existente.
- **DELETE** `/api/usuarios/{id}`: Remove um usuário.

## Passos para Executar
1. Clone este repositório.
2. Crie o banco de dados no SQL Server usando o arquivo `cria-db.sql`.
3. Execute o projeto no Visual Studio Code.
4. Teste as funcionalidades do CRUD no Insomnia/Postman.

