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



