# README

## TodoApi

Este é um projeto simples, feito no vscode e utilizando o terminal, para exemplificar a criação de uma Web API utilizando o .NET. Este README contém os passos necessários para gerar e configurar a aplicação.

Este projeto foi criado seguindo as orientações do tutorial "[Criar uma Web API com ASP.NET Core](https://learn.microsoft.com/pt-br/aspnet/core/tutorials/first-web-api?view=aspnetcore-7.0&tabs=visual-studio-code)" da Microsoft.

## Passo 1: Geração do projeto

Para gerar o projeto, basta executar o seguinte comando no terminal:

    ``dotnet new webapi -o TodoApi``

Após a criação do projeto, navegue até o diretório TodoApi:

    ``cd TodoApi``

E então adicione o pacote Microsoft.EntityFrameworkCore.InMemory:

    ``dotnet add package Microsoft.EntityFrameworkCore.InMemory``

E por fim, abra o projeto no Visual Studio Code:

    ``code -r ../TodoApi``



## Passo 2: Confie no certificado de desenvolvimento HTTPS

Para confiar no certificado de desenvolvimento HTTPS, execute o seguinte comando no terminal:

    ``dotnet dev-certs https --trust``

E clique em **Sim** na caixa de diálogo.


## Passo 3: Scaffold do Controller

Para gerar o Controller, você precisará adicionar alguns pacotes ao projeto. Execute os seguintes comandos no terminal:

    ``dotnet add package Microsoft.VisualStudio.Web.CodeGeneration.Design -v 7.0.0``

    ``dotnet add package Microsoft.EntityFrameworkCore.Design -v 7.0.0``

    ``dotnet add package Microsoft.EntityFrameworkCore.SqlServer -v 7.0.0``

    ``dotnet tool uninstall -g dotnet-aspnet-codegenerator``

    ``dotnet tool install -g dotnet-aspnet-codegenerator``

Em seguida, compile o código e execute o comando abaixo para gerar o Controller:

    ``dotnet-aspnet-codegenerator controller -name TodoItemsController -async -api -m TodoItem -dc TodoContext -outDir Controllers``

Após a execução deste comando, você terá um novo arquivo ``TodoItemsController.cs`` no diretório ``Controllers``.


## Conclusão

Seguindo esses passos, você terá uma Web API simples e funcional em poucos minutos. Sinta-se à vontade para explorar mais sobre o .NET e aprimorar a sua aplicação!

