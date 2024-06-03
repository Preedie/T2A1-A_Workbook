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

## Q2

The database that ive chosen which is commonly used in API database project is Postgres it is a highly popular language and I'm going to describe its pros and cons.

### Pros:

1. ACID ADHERENCE: Postgres complies with the ACID rules/properties which allows for the data have.
- Atomicity: essentially "it" happens, or nothing at all does. So there's no halfway changes!
- Consistency: Very straight forward but everything stays the same before, during and after "Consistency is key" as they say.
- Isolation: Regardless of how many things are happening at once they happen seperately within their scope.
- Durability: Once the change or transaction is confirmed there is no "going back" so to speak, but essentially this means the data is saved no matter what happens to the system.

2. SCALABILITY AND VERSATILITY: PostgresSQL is incredibly scalable for larger projects as it allows for replication and clustering, this lets APIs handle the project efficiently as it grows through allowing the database to scale horizontally through allowing the dev to distribute a workload across many different servers or "nodes". postgreSQL also ensures that there's no data redundancy and high availability while the clustering aspect helps balance the fault tolerances through load balancing. Horizontal scalability is incredibly important for larger projects as it allows for effecient data trasfer and performance as the traffic increases and the data size increases.

PostgreSQL's versatility makes it highly suitable for many different sized projects (small, medium and large). Its more advanced support features also make it excellent for different types of use cases, e.g. geospatial data types(Mapping, enviromental monitoring, urban planning, emergency response and disaster management etc), JSONB data type (User profiles, catalogs for trade goods, Event information ) and full text searching!(E commerse, knowledge bases and wikis, search engines/web portals, social media platforms). 

3. CONCURRENCY CONTROL: postgreSQL allows for concurrency control, MVCC - Multi Version Concurrency Control. This makes sure that the API can make multiple requests like reading or writing to the data without interfering with itself making another request of the same nature.

4. DATA INTEGRITY: PostgresSQL through multiple operations helps maintain integrity. By applying contraints through NOT NULL, UNIQUE, PRIMARY KEY etc the dev is able to enforce rules and restrictions on the data that is stored within the database. Triggers and foreign keys within postgreSQL are also able to reduce the chance of data corruption or inconsistancy in API operations by not only adding triggers like INSERT, UPDATE or DELETE but by assigning relationships to multiple tables through the use of the foreign key which was afformentioned.

### CONS:

