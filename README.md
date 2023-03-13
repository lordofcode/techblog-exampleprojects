# techblog-exampleprojects
My Techblog is a blogging site (text), when showing code/examples use this repository.

2023-03-13  When connecting from a .NET Framework 4.7.2 application with a MariaDB database in a Docker container you might get DBNull exceptions.

I used Entity Framework and the MySql.Data-, MySql.Data.Entity-, MySql.Data.EntityFrameworkCore-nuget packes from Oracle, but it did not work.
Possible solutions is to use an older version of MariaDB. 
I choosed to create a new library-project and used the MySqlConnector nuget-package of Bradley Grainger
https://www.nuget.org/packages/MySqlConnector/

It is an ADO.NET provider, so it uses the Connection-, Command-, DataAdapter-objects. I did not want to convert all my code from entity-framework LINQ objects to plain old SQL, so
I created some kind of wrapper. This project shows an example.

More details can be read on my blog (Dutch):
https://techblog.dirkhornstra.nl/node/478