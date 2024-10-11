# Ativi3-ExoApi-Get

Este repositório contém a implementação de uma API para a empresa **ExoApi**, desenvolvida como parte de uma atividade de **Desenvolvimento de APIs**. A API permite a conexão com o banco de dados e a listagem de projetos cadastrados, além de funcionalidades CRUD completas para **Projetos** e **Usuários**, bem como a implementação de **Login** e suporte a **CORS**.

## Estrutura do Projeto

O projeto está organizado da seguinte forma:

- `.vscode/`: Configurações do VSCode.
- `Contexts/`: Classe responsável pela configuração da conexão com o banco de dados.
- `Controllers/`: Controladores que expõem as operações da API.
- `Models/`: Modelos das entidades **Projeto** e **Usuário**, com seus atributos.
- `Properties/`: Configurações do projeto.
- `Repositories/`: Repositórios responsáveis pela manipulação e acesso aos dados do banco.
- `bin/`, `obj/`: Diretórios gerados automaticamente com a build do projeto.
- `Exo.WebApi.csproj`: Arquivo de configuração do projeto.
- `Exo.WebApi.sln`: Solução do projeto.
- `Program.cs`: Arquivo de entrada do projeto.
- `appsettings.json` e `appsettings.Development.json`: Configurações de ambiente do projeto.

## Funcionalidades

A API desenvolvida oferece as seguintes funcionalidades principais:

### **Branch `Atividade 03 - GET`**
- **Listagem de Projetos**: Disponibiliza uma lista dos projetos cadastrados no banco de dados via o endpoint `GET /api/projetos`.

### **Branch `Atividade 04D - CRUD de Projetos`**
- **Criação de Projetos**: Permite adicionar novos projetos via o endpoint `POST /api/projetos`.
- **Leitura de Projetos**: Exibe uma lista de projetos via `GET /api/projetos`.
- **Atualização de Projetos**: Permite a edição de projetos já cadastrados via `PUT /api/projetos/{id}`.
- **Exclusão de Projetos**: Remove um projeto existente no banco de dados via `DELETE /api/projetos/{id}`.

### **Branch `Atividade 04E - CRUD de Usuários`**
- **Criação de Usuários**: Permite adicionar novos usuários via o endpoint `POST /api/usuarios`.
- **Leitura de Usuários**: Exibe uma lista de usuários via `GET /api/usuarios`.
- **Atualização de Usuários**: Permite a edição de usuários já cadastrados via `PUT /api/usuarios/{id}`.
- **Exclusão de Usuários**: Remove um usuário existente no banco de dados via `DELETE /api/usuarios/{id}`.

### **Branch `Atividade 04F - Login e CORS`**
- **Login de Usuários**: Permite que os usuários façam login no sistema via o endpoint `POST /api/login`.
- **Configuração de CORS**: Implementa suporte a CORS, permitindo o acesso à API a partir de diferentes origens.

## Como Executar

### Pré-requisitos

- [SQL Server Management Studio (SSMS)](https://aka.ms/ssmsfullsetup)
- [.NET 6 ou superior](https://dotnet.microsoft.com/download/dotnet/6.0)

### Passos para execução:

1. **Banco de Dados**:
   - Abra o **SQL Server Management Studio (SSMS)**.
   - Carregue o script `cria-db.sql` e execute para criar o banco de dados e os usuários.

2. **Configurando o Projeto**:
   - Abra o terminal e verifique se o .NET está instalado e na versão correta:
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

3. **Configuração da String de Conexão**:
   - Configure a string de conexão para o seu ambiente no arquivo `ExoContext.cs`.

4. **Compilação e Execução**:
   - Compile o projeto:
     ```bash
     dotnet build
     ```
   - Execute o projeto:
     ```bash
     dotnet run
     ```

5. **Testando no Navegador**:
   - Após a execução do comando `dotnet run`, acesse o navegador e digite a URL gerada pelo servidor seguido do sufixo `/api/projetos` para visualizar a lista de projetos cadastrados.
   
   Para testar as outras funcionalidades (CRUD e login), utilize ferramentas como **Insomnia** ou **Postman**.

## Branches do Projeto

### **Atividade 03 - GET**
- Implementa a funcionalidade de listagem de projetos cadastrados no banco de dados via `GET /api/projetos`.

### **Atividade 04D - CRUD de Projetos**
- Implementa as operações de **Criação**, **Leitura**, **Atualização** e **Exclusão** de projetos.

### **Atividade 04E - CRUD de Usuários**
- Implementa as operações de **Criação**, **Leitura**, **Atualização** e **Exclusão** de usuários.

### **Atividade 04F - Login e CORS**
- Implementa o **Login** de usuários via `POST /api/login` e adiciona suporte a **CORS** para permitir o acesso à API a partir de diferentes origens.
