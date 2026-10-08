

### Architectural Overview of the project


### Backend Architectural Overview.

## Folder structure

- src -> This is the root directory , which will contain all the server level code.
Inside source we will have following folders.
1. config
2. db
3. routes.
4. services.
5. repository.
6. utils.
7. middlewares.

- config -> The config folder will have all the configrations.
Different configrations related to different services should present in different files.

- db -> db will have the folders related  to tables/schema/database.
For example out db folder can have the folders like models, seeders, migrations etc.

- models -> models folders will have the models representing the schema.
- seeders -> Will have the seed data if any.
- migrations -> Should have the migrations.

- routes -> The router folder will have all the routes.
Routes related to one type of entity should be kept in a seperate file togetherly, means differnt routes relatated to different entities should be kept in a seperately. For example the user.route file should contain the routes relates to the user. Similarly for all the expenses routes we will need a seperate file containing all the routes related to the expences.

- controllers -> The controllers folder will have all the controller functions.
Controllers related to one type of entity should be kept in a seperate file togetherly, means differnt controllers relatated to different entities should be kept in a seperately. For example the user.controller file should contain the controllers relates to the user.Similarly for expenses controllers we will need a seperate controller file containing all the controllers related to the expences.

- services -> The services folder will have all the services functions. These services function will mainly contain the business logic that needs to be performed at the application server level. Services related to one entity should be kept in a seperate file togetherly.

For example the user.services file should contain the services related to the user only. Similarly for expenses we will need a seperate file containing all the controllers related to the expences.

- repository -> repository contains the code/functions which directly intracts with models.
Functions dealing with one type of model should be kept togetherly in one seperate file.

Ex- user.repository will have all the functions primarily dealing with the user model. Similarly user.expenditure will have all the functions primarily dealing with the expense model. 




# User Management.

Any request coming related to the user should follow the following mentioned mechanism.

If the client is the web or mobile browser
Client  -> Frontend Server -> Backend Server -> Database -> User Table

If the client is tool like postman or thunderclient
Client -> Backend Server -> Database -> User Table


# Expense Management.
Any request coming related to the expense should follow the following mentioned mechanism.

If the client is the web or mobile browser
Client  -> Frontend Server -> Backend Server -> Database -> Expense Table

If the client is tool like postman or thunderclient
Client -> Backend Server -> Database -> User Table


### At the backend we will have identical routes for all the service. No matter the client is a web browser or a mobile browser or it is a tool like postman or thunderclient. The route t the controllers/services will be identical.