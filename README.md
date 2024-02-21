# dotNet
My Dotnet course

  "ConnectionStrings": { "Connection": "Server=(localdb)\\MSSQLLocalDB;Database=School;Trusted_Connection=True;" },
  


>>>>>>Now, we want to add the migrations and update the DB (terminal):as we are using vs code, we need to install a few things in order first:<<<<<<

dotnet new tool-manifest

dotnet tool install --local dotnet-ef

dotnet ef migrations add InitialCreate

    >>>>>>>>To undo<<<<<<<<<<<

      dotnet ef migrations remove

dotnet ef database update

>>>>>>>Genrate the controllers:<<<<<<<<<

dotnet tool install --local dotnet-aspnet-codegenerator

dotnet add package Microsoft.VisualStudio.Web.CodeGeneration.Design

dotnet add package Microsoft.EntityFrameworkCore.SqlServer

dotnet aspnet-codegenerator controller -name <StudentsController> -async -api -m <Student> -dc <SchoolContext> -outDir <Controllers>

dotnet aspnet-codegenerator controller -name <CoursesController> -async -api -m <Course> -dc <SchoolContext> -outDir <Controllers>

dotnet aspnet-codegenerator controller -name <EnrollmentsController> -async -api -m <Enrollment> -dc <SchoolContext> -outDir <Controllers>

dotnet run

dotnet aspnet-codegenerator controller -name ProductsController -async -api -m Product -dc ProductContext -outDir Controller


dotnet add package MailKit --version 4.3.0

