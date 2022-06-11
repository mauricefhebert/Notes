---
id: h6bbbjw9gdt8d3f7j83wln9
title: Razor Pages
desc: ""
updated: 1654915075957
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

## \_Layout Page

The layout page is the layout that will be shared between all the page the default one is located in **Pages/Shared/\_Layout**.<br>
You can create additional layout if you need more then one but you would need to implicitly select which page would use the layout in the page view by convention the layout are stored in the shared folder and always start with an underscore (\_Layout)

### Defining a different layout for a page

```cshtml
@page
@model Chapter02.Pages.WelcomeModel
@{
    Layout = "_LayoutYouWannaUse";
}
```

## Exploring the file of the application

### .sln

The solution file store all the information of related project it act as a container in large web application you will often find multiple project all part of the same solution that form one application for example you could have a project that is responsible for the user interface and one that is responsible for the logic they would both be in the same solution.

### .csproj

The csproj file is responsible for storing the information about the build this file is used to enable the dotnet build to convert the source code file into something that the .net runtime can execute.
<br>
In this file you can edit two functionality of your program
<br>
`Nullable` is to control the amount of feedback you receive from the code analyzer that look for potential <em>NullReferenceException</em> by turning this feature off you simply remove a warning that their some chance that a value could be null
<br>
<br>
`ImplicitUsings` This is a C# 10 feature that reduce the amount of implicit using you have to in .cs file they are set globally in the dotnet sdk

### The bin and obj folder

They simply are the file that are created when you build you project they contain debug information and all the file needed to execute your application

### The properties folder

This folder container the `launchSetting.json` which contain the setting used for when you run your application

### The wwwroot folder

This folder contain all the static file of your website you should never place a file that you don't want the end user to be able to access because this will be accessible through the source folder in the browser debug tools. This folder should contain you css, javascript front end library, image, video, audio etc...

### The pages folder

The page folder contain all the page of your application it contain both the view and the view-model.
It also contain the **Shared** folder which is used to store all the content that will be shared across multiple page

### The appSettings files

The `appSettings.json` and `appSettings.Development.json` is used to store some config information about your application for example your database connection string

### Program.cs

This is the entry point of your application this is where you will manage all your service and dependencies injection. This is where you will manage the pipeline and middleware

<!-- Tag helper section -->

## Tag Helper Reference Sheet

| Tag Helper | Function                       |
| ---------- | ------------------------------ |
| asp-page   | Use to navigate to a page      |
| asp-for    | Create a name and id attribute |
