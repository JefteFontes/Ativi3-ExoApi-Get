# Atividade 03 - ExoApi - Listagem de Projetos

Este repositório contém a implementação de uma API para a empresa **ExoApi**, desenvolvida como parte de uma atividade de **Desenvolvimento de APIs**. A API permite a conexão com o banco de dados e a listagem de projetos cadastrados.

## Estrutura do Projeto

O projeto está organizado da seguinte forma:

- `.vscode/`: Configurações do VSCode.
- `Contexts/`: Contém a classe responsável pela configuração da conexão com o banco de dados.
- `Controllers/`: Controlador que expõe as operações de listagem de projetos via API.
- `Models/`: Modelo da entidade **Projeto**, com seus atributos.
- `Properties/`: Configurações do projeto.
- `Repositories/`: Repositório responsável pela manipulação e acesso aos dados do banco.
- `bin/`, `obj/`: Diretórios gerados automaticamente com a build do projeto.
- `Exo.WebApi.csproj`: Arquivo de configuração do projeto.
- `Exo.WebApi.sln`: Solução do projeto.
- `Program.cs`: Arquivo de entrada do projeto.
- `appsettings.json` e `appsettings.Development.json`: Configurações de ambiente do projeto.

## Funcionalidade

A API desenvolvida oferece uma funcionalidade principal:

- **Listagem de Projetos**: Disponibiliza uma lista dos projetos cadastrados no banco de dados via o endpoint `GET /api/projetos`.

## Branches

O projeto é organizado em diferentes branches para cada etapa de desenvolvimento e funcionalidade. As principais branches são:

- **main**: Branch principal, contém a versão estável do projeto.
- **feature/listagem-projetos**: Contém a implementação da funcionalidade de listagem de projetos via API.
- **feature/conexao-banco**: Responsável pela implementação da conexão com o banco de dados.
- **feature/model-projeto**: Inclui o modelo da entidade **Projeto** com seus atributos.

Ao desenvolver novas funcionalidades, recomenda-se criar uma nova branch seguindo o padrão `feature/nome-da-funcionalidade`.

## Como Executar

### Pré-requisitos

- [SQL Server Management Studio (SSMS)](https://aka.ms/ssmsfullsetup)
- [.NET 6 ou superior](https://dotnet.microsoft.com/download/dotnet/6.0)

### Passos para execução:

1. **Banco de Dados**:
   - Abra o **SQL Server Management Studio (SSMS)**.
   - Carregue o script `cria-db.sql` disponível na pasta `Material-Aluno` e execute para criar o banco de dados e os usuários.

2. **Clonando o Repositório**:
   - Clone o repositório e escolha a branch desejada:
     ```bash
     git clone https://github.com/usuario/exoapi.git
     cd exoapi
     git checkout feature/listagem-projetos
     ```

3. **Configurando o Projeto**:
   - Abra o terminal dentro da pasta do projeto (`Exo.WebApi`).
   - Verifique se o .NET está instalado e na versão correta:
     ```bash
     dotnet --version
     ```
   - Abra o projeto no VSCode:
     ```bash
     code .
     ```
   - Restaure os pacotes do projeto:
     ```bash
     dotnet restore
     ```

4. **Configuração da String de Conexão**:
   - Configure a string de conexão para o seu ambiente no arquivo `ExoContext.cs`.

5. **Compilação e Execução**:
   - Compile o projeto:
     ```bash
     dotnet build
     ```
   - Execute o projeto:
     ```bash
     dotnet run
     ```

6. **Testando no Navegador**:
   - Após a execução do comando `dotnet run`, acesse o navegador e digite a URL gerada pelo servidor seguido do sufixo `/api/projetos` para visualizar a lista de projetos cadastrados.

## Arquitetura

- **Context**: A classe `ExoContext` é responsável por gerenciar a conexão com o banco de dados e o acesso às entidades.
- **Model**: A classe `Projeto` representa o modelo da entidade **Projeto**, contendo atributos como `Id`, `NomeDoProjeto`, `Area` e `Status`.
- **Repository**: A classe `ProjetoRepository` implementa a lógica de acesso e manipulação dos dados de projetos.
- **Controller**: A classe `ProjetosController` expõe os endpoints da API, sendo responsável pelo método **GET** que lista os projetos.

## Teste da API

Use ferramentas como **Insomnia** ou **Postman** para fazer requisições à API e visualizar a listagem de projetos cadastrados no banco de dados. A URL para testar o **GET** da listagem de projetos é:

