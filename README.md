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

### Database Layer

Seperating database schemas is a good idea if your project is using multiple data domains as it is essentially seperating the database schema into seprate/different models that align with a different part of application.

### Testing

In this particular phase of the API project you'll find the developer testing individual parts of an applications that can range from routes to controllers and modules aswell as making sure all the different parts of the application integrate correctly with the others, such as endpoint requests and other parts of the app in that nature, executing through their duties.

### Middleware

Middleware is another vital part of a API project/applications, this essentially acts as a "middleman" and requests data from the client to authenticate, do a request parse or even login a client.
for example much like a waiter in a restaurant if you order wine, the waiter will then ask for proof of age, if you order a steak they will bring you a steak knife to cut it rather than go to the kitchen staff, acting as a middleman or in API project structure context middleware.

### Error Handling

Error handling is a important part of API application/project structure, as ensuring the user is provided information about what problem has been encountered allows the client to understand the issue and troubleshoot (if possible) on their own, or of course inform technical support with error codes to troubleshoot for them.

### Security 

Structuring proper security methods for authentication and authorization from a client to their perosnal information database aswell as creating validation input to prevent injection attacks (injecting melicious code) so that the database and the information/data within is protected, is highly important and never NOT included in information collecting applications.

### Deployment

Finally we have deployment applications that allow us (the developer) to contain and package our application and its depedencies, often using another application to then deploy.
Following deployment is having a CI/CD (continuous intergraction/Continues Deployment) to allow the project to continue to be modified and changed throughout the course of either it's life or usage.
(github actions is a CI/CD service example that allows for devs to customise workflows and execute them based on certain events pulls/commits scheduled triggers).