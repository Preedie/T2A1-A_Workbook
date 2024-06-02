# TERM 2 WORKBOOK

## Q1

### API ARCHITECTURE

The basic API structure of a typical API project follows this design process.


### THE CORE
#### Routes

These are known as endpoints that are often used to control and define how the user or client/s interact and use the application. These are usually written like, 
'@app.route('/')'.

#### Controllers/Views

This part is responsible for handling the logic behind the requests from the route aswell as processing the requests made and then generating the appropriate response.

#### Models and Services

#### Models

A blueprint or in most cases multiple blueprints will define their respective models followed by the business logic and data structures for said blueprint/model.
The models within the blueprint hold certain information and behaviours resposible for the behaviour related to the functionality of the blueprint. Having models specific to each blueprint helps the project stay organsied aswell as avoiding clutter and making it far easier to maintain.

#### Services

Much like models containing their own business logic and ways of accessing data related to the model, blueprints may do the same.
The services essentially contain many methods and functions that can create, read, update and delete (CRUD) any data related to the blueprint.
By applying services you are making the code you write far more reusable and maintainable aswell as making sure your code can be easily tested.
Services are best seperated by blueprints as this will allow for less conflicts as the code/project grows via isolation/seperation and it will also allow the code to evolve overtime.

#### Database Layer

Seperating database schemas is a good idea if your project is using multiple data domains as it is essentially seperating the database schema into seprate/different models that align with a different part of application.


