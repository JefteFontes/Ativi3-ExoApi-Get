# Atividade 04D - CRUD de Projetos

## Descrição
Este branch implementa o restante do CRUD de projetos. A funcionalidade permite criar, ler, atualizar e excluir projetos na API.

## Requisitos
- Editor de código: Visual Studio Code
- SDK .NET: versão 6 ou 7
- Banco de dados: SQL Server (use o script `cria-db.sql` para criar o banco de dados)

## Funcionalidades Implementadas
1. **Criação de Projetos**: Permite adicionar novos projetos.
2. **Leitura de Projetos**: Consulta e exibe projetos armazenados no banco de dados.
3. **Atualização de Projetos**: Edita as informações de um projeto existente.
4. **Exclusão de Projetos**: Remove um projeto do banco de dados.

## Como Testar
Use o aplicativo Insomnia ou Postman para testar as funcionalidades do CRUD:

- **POST** `/api/projetos`: Adiciona um novo projeto.
- **GET** `/api/projetos`: Retorna a lista de projetos.
- **PUT** `/api/projetos/{id}`: Atualiza um projeto existente.
- **DELETE** `/api/projetos/{id}`: Remove um projeto.

## Passos para Executar
1. Clone este repositório.
2. Crie o banco de dados no SQL Server usando o arquivo `cria-db.sql`.
3. Execute o projeto no Visual Studio Code.
4. Teste as funcionalidades do CRUD no Insomnia/Postman.

