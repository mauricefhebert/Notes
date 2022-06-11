---
id: h6bbbjw9gdt8d3f7j83wln9
title: Razor Pages
desc: ""
updated: 1654910765432
created: 1654907162498
---

## Creating a razor page application with the cli

1. Navigate to where you wanna save your project
2. Open the terminal and run the following command to create a new project solution `dotnet new sln`
3. Create a new Razor page application `dotnet new webapp -o WebApplication1 `
4. Add the new application to the solution file `dotnet sln add WebApplication1 `

**Explaining the above command**
<br>
`dotnet new sln`
<br>
Create a new solution file in the current folder
<br>
`dotnet new webapp -o WebApplication1`
<br>

- `dotnet new webapp` -> Create a new razor page application
- `-o` -> Specify a output directory
- `WebApplication1` -> The name of the output directory and the name of the application

To see all the available template run `dotnet new --list`

## Create a new pages

1. Navigate to the root of your project where the .csproj is located
2. Run the following command <br>`dotnet new page -n Welcome -o Pages -na WebApplication1.Pages`

**Explaining of the above command**

- `dotnet new pages` -> Create a new page
- `-n Welcome` -> The name of the new page
- `-o Pages` -> Specify the output directory in our case the Pages folder you can also create a new folder at the same time to store your page in by adding a folder at the end `-o Pages\FolderName`
- `-na WebApplication.Pages` -> The namespace that should be applied
