# EcoPowerSolutions

## About the Project:
This is a web application programming interface project that integrates with the ConnectedOffice database. An Azure-hosted SQL Server database houses this data. Three tables—Categories, Devices, and Zone—make up the database. 

This API functions essentially as an IoT Device Management System, keeping track of all IoT devices that the company has deployed. Different types of gadgets are employed depending on the type of organization. Each IoT device is initially registered and assigned a category. Then, IoT devices are installed in designated zones throughout the organization's structures. Administrators have access to every IoT device and can view it, modify its settings, add new devices, and move it to different zones.  
## Creation of the API
### Azure database
Started off with creating an account on Azure and created a resource group, under which I added an SQL database and hosted my database there. I then added tables to the database via Sql Server Management Studio (SSMS). 
![Screenshot (72)](https://github.com/bafanamahase/CMPG-323-project-2.0-29910439/assets/88552699/1e7ae751-0e73-4911-93ac-125de55b99a3)

### API creation
I used visual studio to create the web API. Added controllers that will support the manipulation of tables in the database that is hosted on azure server. Thereafter I implemented security on the API so that no unauthorized user can get access to the API functionality.

### Hosting the API
I created an API Management Service on azure so that I could be able to work with it there. I then published the API via Visual Studio, and pulled it from the Azure side.
![Screenshot (73)](https://github.com/bafanamahase/CMPG-323-project-2.0-29910439/assets/88552699/5b77cb7f-4595-435f-b057-5e1fe6d75abe)

## Security:
Not everyone can access the API. You must register an account in order to use the API to access and manipulate database data. The server on which the database is hosted on is also secured, and those details are not accessible to everyone.

## Usage:
Upon accessing the API, the user must register an account. Then the user may proceed to login. The user should request a token when accessing tables and manipulating data contained in those tables. The account that should be registered is the admin one because it is the only one that is authorized to access the tables.
### Registering an account:
The user must register an admin user because it is the only role that is authorized to access he tables and table manipulation.

### Logging in:
The user must click on the login button and insert the newly registered credentials.After logging in the user will receive the token. That token must be saved as will be used to access the tables since this system uses a tokeen based security.

### Link to API on Azure
ecopowersolutions20230829142227.azurewebsites.net


### Reference List
Muller, J. 2023. Project 2 – ASP.NET Core guidance documentation. Unpublished lecture notes on efundi. Vanderbijl: NWU

Muller, J. 2023. Project 2 – ASP.NET Core security guidance documentation. Unpublished lecture notes on efundi. Vanderbijl: NWU

https://docs.github.com/en/get-started/getting-started-with-git/ignoring-files

https://stackoverflow.com/questions/13426984/500-internal-server-error-for-sql-server-error


https://social.msdn.microsoft.com/Forums/sqlserver/en-US/16a79e1f-e48c-4b7b-8388-08a5b1130f60/internal-error-500-and-the-report-server-not-responding?forum=sqlreportingservices


https://www.entityframeworktutorial.net/efcore/entity-framework-core-migration.aspx


https://docs.microsoft.com/en-us/ef/core/cli/dotnet


https://www.learnentityframeworkcore.com/walkthroughs/existing-database


https://docs.microsoft.com/en-us/ef/core/managing-schemas/migrations/providers?tabs=dotnet-core-cli


https://www.apimatic.io/blog/2018/10/redesigning-apis-at-apimatic-a-case-study/


https://docs.microsoft.com/en-us/dotnet/csharp/language-reference/operators/await


https://docs.microsoft.com/en-us/dotnet/csharp/language-reference/compiler-messages/cs4014?f1url=%3FappId%3Droslyn%26k%3Dk(CS4014)


https://stackoverflow.com/questions/48408559/asp-net-web-api-perform-search-on-table-using-http-get-method-and-linq-to-sql-d


https://docs.microsoft.com/en-us/power-apps/developer/data-platform/webapi/query-data-web-api


https://www.c-sharpcorner.com/UploadFile/219d4d/working-with-multiple-tables-in-mvc-using-entity-framework/


https://stackoverflow.com/questions/50388344/how-to-get-data-from-two-tables-using-web-api


https://stackoverflow.com/questions/35675747/asp-net-5-mvc-unable-to-connect-to-web-server-iis-express


https://makolyte.com/system-invalidoperationexception-unable-to-resolve-service-for-type-while-attempting-to-activate/


https://stackoverflow.com/questions/40900414/unable-to-resolve-service-for-type-while-attempting-to-activate-while-class-is


https://www.youtube.com/watch?v=GU1uvShcPeo


https://stackoverflow.com/questions/52311053/more-than-one-dbcontext-was-found


https://docs.microsoft.com/en-us/sql/relational-databases/errors-events/mssqlserver-18456-database-engine-error?view=sql-server-ver16


https://www.nuget.org/packages/Microsoft.Data.SqlClient



https://stackoverflow.com/questions/53405760/problem-with-dotnet-ef-dbcontext-scaffold-on-linux-bash


https://entityframeworkcore.com/knowledge-base/45350317/entityframework-scaffold-dbcontext-not-recognised


https://stackoverflow.com/questions/70921985/scaffold-dbcontext-runs-successfully-but-does-not-create-any-models


https://docs.microsoft.com/en-us/azure/azure-resource-manager/management/delete-resource-group?tabs=azure-powershell


https://docs.microsoft.com/en-us/sql/relational-databases/errors-events/mssqlserver-10060-database-engine-error?view=sql-server-ver16



