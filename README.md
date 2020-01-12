# ASP.NET Core 3 Application

During this workshop you will learn how to scaffold an ASP.NET core application.

[Source MS](https://docs.microsoft.com/en-us/aspnet/core/getting-started/?view=aspnetcore-3.1&tabs=macos)

## Create a web app project from the command lines

Using the command line you can create a new web app:

```
$ dotnet new webapp -o aspnetcoreapp
```

## Start the app

* Expected behavior is that it will open an example ASP.NET application when you run the following commands: 

```
$ cd aspnetcoreapp
$ dotnet run --urls http://0.0.0.0:5001 
```

Browse to `localhost:5001` and you should see the webpage.

## Setup GitPod to run your app by default

In the `.gitpod.yaml` file you can uncomment out the lines 11-12:

```
tasks:
  - command: cd aspnetcoreapp/ && dotnet run --urls http://0.0.0.0:5001
```

Your application will now start automatically when Gitpod launches.

## Edit a Razor page

Open `Pages/Index.cshtml` and modify and save the page with the following highlighted markup:
```
@page
@model IndexModel
@{
    ViewData["Title"] = "Home page";
}

<div class="text-center">
    <h1 class="display-4">Welcome</h1>
    <p>Hello, world! The time on the server is @DateTime.Now</p>
</div>
```
