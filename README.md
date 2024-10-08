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

1. LEARNING CURVE: PostgreSQL due to its large feature set and indepth/complex syntax can prove quite the steep learning curve for developers that are unfamilliar with relational databases, which can have a significant impact of development time.

2. SETUP AND MAINENANCE: The setup and configuration process for postgreSQL requires knowledge and time, especially if the developer wants the best performance possible from the application. The maintenance with postgres can also add a fair bit of time to a project due to requiring data backups, tuning of the performance of the program and then of course updating the secruity management of the application all of which can contribute to time to deliver/deploy/maintain. 

3. INITIAL SETUP OF SCHEMA'S DATABASE: Properly setting up all of the requirements for the database to meet the spicific needs of the API project can also take a large amount of time due to needing to follow to structure of creations for schemas/tables and indexes/permissions. 

4. RESOURCE CONSUMPTION: Postgres can be highly resource consumptive due to  it's abillity to handle large numbers of API requests (if required). So properly using and allocating resources becomes paramount in preventing performance losses or better known "bottle necks" in performance.
So depending on the workload the requirements of not only hardware but software management is highly important for postgres to work efficiently. 

## Q3

Daily stand-ups are one of the many agile management methodolgies implemented when undertaking a API project.

The general structure of a daily stand-up is as follows.

- questions are asked

1. What did you do yesterday?
2. what will you do today?
3. Is there anything blocking your progress?

- The standup is usually only for 10 people max as having to many people in the meeting cna make it go alot longer than it should aswell as making the meeting less transparent as team member will begin to lose the motivation to be more questioning and open with a large amoutn of spectators.
- The standup is often reserved to be a maximum of 10-15 minutes long.

The standup meeting is largely structured around the 3 questions what did you do yesterday, what will you do today and is anything blocking your progress. Which not everyone is required to, but notes can be taken as it is considered quite beneficial to do so.

The main priniciples in daily standup meetings is simple
1. Keep them short (10mins)
2. Use the same questions every single meeting.
3. Conduct the meetings everyday and at the same time.

- The meeting can often kickoff with a round robin where each tem member answers the three questions.

- If there are blockers indetified in question 3 they are addressed and written down so that they can be pursued further AFTER the standup meeting by the proper team members(team managers/stake holders/project manager).

- The meeting is to remain positive and constructive, essentially the enviroment should be encouraging so that the fear of judgement doesnt sway team memmbers from expressing their ideas about any challenges.

- The standup meeting should regularly be reviewed to ensure its effecitive and doing the job it is supposed to, and if it is not it goes under review and is adjusted to make sure it meets proper standards.

The typical patricipants for daily standup meetings are fairly straight forward but not limited too.
1. Team members (which are all required)
2. Scrum master(optional)
3. Product Manager(optional)

obviously the team members are there to take their notes if they wish and help plan sprints and project goals.

The Scrum master although optional if there is tasked with ensuring the daily standup meetings follow the *Agile Cermonies Rules* and they will also manage any distractions. However having a scrum manager at every single daily standup is not a requirement.

If a product manager is invited it is important that they remain a spectator, as they can often turn meetings less transparent, which completely defeats the purpose of the meeting taking place in the first place. So if the product manager is invited they are present as a spectator, otherwise its better they don't attend the meeting atall.

Common problems with Standup meetings are as follows:
### Misalignment 
sometimes topics that are unrelated to the the meetings purpose can end up being discussed which in turn can mean there's less time to discuss the actual point of the meeting in the first place, or of course make the meeting go overtime while being filled with pointless information due to its unrelated nature to the project.

### Too Lengthy

Much like misalignment discussing things that are unrelated to the ask and project at hand can mean the meeting becomes to lengthy and begins to waste precious time resources on pointless discussions.
examples could be 
- tangential conversations or better known as watercooler talk
- someone begins rambling and it takes a long time for them to get to the point of their discussion, if they make it to the end of it atall.

### Problem - Solving During the Meeting

Teammates could begin to engauge in problem solving during the meeting, and as much as thats great, its the wrong time and place for it to occur as it can make it difficult to keep the meeting at the scheduled length.
Which, when you have multiple people scheduling there days to cater for a 10 minute standup meeting can become quite problematic for workflow outside of the meeting.

### Meeting Time/Scheduling

It can become very difficult to schedule a meeting time for when everyone is availble to attend, as there can be many timetable and calendar clashes between teammates which could make the standup meeting quite the chore to schedule in for everyone.

### Not Listening

Standups as much as they mean well can often lean towards teammates tuning out and not listening due to the inability to focus on the questions being asked and talked about.
It's also common for teammates to be to busy rehersing their questions while another teammate is speaking due to whatever reason (anxiety and the likes) causing them to not be paying attention.

### Skipping Meetings

If the meetings are not the same place/time and follow the same general cadence they can be forgotton about which can cause memebrs to be late meaning they missout on important information, or it could mean they complete miss the meeting, both of which can have significant impacts on the team memmbers work.

## Q4

A standard source control process in a API project starts with

1. Repo Setup: 
Setting up a repository on a cloud storage application system is typically the first process in the creatin of a API project. This will allow team members to work effectively alongside each other.

2. Branching: 
Working forward from Repo setup is branching, this effectively allows team memmbers to work with the main/master source but not "on" the main source, so a Dev will work alongside the main/master on a branched source to fix bugs, add features etc without effecting the main source code itself, then the "updates" so to speak can be added on or merged into the main/master source code later.

3. API Design Process: 
In this part of the API projects design process the blueprints along with modules, endpoints, how data and information is requested/responded to aswell as authentication processes and error handling strategies are created. Documentation of how the API is to be designed will also be done here through the use of applications that aid in the creation of blueprints.

4. Feature Development: Within this process the first thing done is a branch is created from the main/master, this allows for code to be edited/changed while keeping the working integrity of the main source true, through isolation using branches. This/these branches will allow developers to work collabratively on features, bug fixes and performance enhancements. Once all is completed the features are implemeneted and enter the review process in which code adherence, quality and code standards are reviewed to ensure there are no potential issues, and if there is they are caught early due to this process.

5. Feedback and Iteration: This is where the API project is adjusted and or improved based off of the feedback that's received until the application meets the requirements set in the scope of the project design and its features.

6. Testing: 
Throughout the testing phase of the project individual parts of code will be tested in isolation to ensure they function correctly aswell as testing how different code interacts with other code.
Functional testing will be done to ensure the code does what its supposed to do, or more so was designed too.
Code will also be tested repetitvely on previously parts of code to ensure any new implementations haven't broken code (known as regression testing). Testing to ensure performance isn't waning is also done testing the software against various conditions to ensure responsiveness.
Secruity testing is done to identify any possible vulnerabilities, ensuring data protection.

7. Continuous Intergration: 
Through continuous intergration and implementing it into the management process of the API project  developer teams can ensure the API remains stable, reliable and consistent throughout the projects life. As this process helps foster collaboration aswell as accelerating development and improving overall software quality through automated testing, automatic API building after each code change, deployment automation and creation on a CI that can provide immediate feedback to the developers about the status of their code changes.

8. Documentation: 
Keeping a well detailed documentation for the API project that includes, endpoint descriptions, request and response schemas examples of different usages and authentication details is another invaluable process as it allows the developers to not only themselves stay up to date with any code changes, but also helps to on board new developers quickly and concisely.

9. Deployment:
In this stage the API is pushed to the phase of staging and testing and once it's validated and all testing is done it is deployed. Deployment is done through containerization through tools like (docker), or it can be deployed by serverless platforms.

10. Release Management: 
Throughout this process of the management method developers ensure that the release of the API project is stable and remains so throughout the duration of its deployment and here after.
Developers will release plan, use a versioning scheme to track changes to the API and will also do rigerous testing throughout the APIs developement process to ensure it meets the standards set.

11. Monitoring/Maintenance:
Once deployed the API will be consistently tracked in regards to its performance along with responding to feedback with updates and testing to ensure the application stays cutting edge, highly performant and bug free for the best user experience.

## Q5

### API TESTING

API testing is essentially confirming that a particular API is working how it was intended to.
It is tested various ways by developers in which the developer can manually do the tests or automate tests to happen via the use of an API testing tool.
there are multiple ways of testing a API and its functionality/performance and they all play a important role in ensuring the API is functional.

### Contract Testing

This type of testing requires the developer to test that the API adheres to the contract or the particular specifications that the API is required to.
Along with testing that contract testing also ensures that the API adheres and does not break the exisiting functionality.
Lastly a Developer will check the format of the information/functionality of the API and ensure the API meets/agrees with the requirements of the contract.

### Unit Testing

Through this method of testing the Developer will ensure that certain endpoints within the code return correct responses that have been given to said request. Basically endpoint testing will ensure that any given endpoint will return and handle the request properly and also return the correct message that was created for it by the Developer whether that message be user information to and error message code.

### End-to-end testing

Where unit testing ensure certain endpoints are working independently from each other, end-to-end testing ensures and helps indentify possible integration issues from different components of the system. So it will also ensure that all individual endpoints works however will always ensure that there is is seamless/performative intergration between various parts of the application stack.

### Load Testing

Load testings purpose is to work out how the system/s will perform under a regular load (requests/post etc) and answer a few different questions that may be of importance like.

1. Wil a system be able to handle a certain number of users or requests without crashing or slowing down?
2. How does the system respond under different load levels (low, med, high).
3. How doe sthe system grow and handle said growth, are there any types of performance issues or bottle necks?

Doing load testing ensures that the developers can isolate and contain any performance pitfalls or to spot any potential code improvements to allow the application to run smoothly providing a seamless, enjoyable user experience that performs well as it scales to a larger more mature program with more requests and users.


## Q6

The three principles of information security and what they are/do are as follows.

### Confidentiality 

The purpose of this principle is to ensure private data is kept private and only accessible by the user it pertains to (who is logged in) it will protect the data through authorization and authentication using encryption and access controls to prevent disclosure or theft of user/s sensitive information.

### Integrity 

integrity ensure that data as its stored is un changed or tampered with through un authorized modification, insertio of data by a un authorized individual aswell as deletion. It does this through the use of chechsums, digitial signatures using encryption methods and access controls all help in ensuring the data maintains its intergity.

### Availability 

Availability ensures that the data/information protected is accessible at all times by the user that is authorized to access it. Essentially this principle is to prevent any type of interruption to the access of the database from outages, server downtime or even access denial. Making sure redundant systems are in place aswell as backup and recovery systems and procedures along with ensuring the network to the database server remains strong and uninterrupted.

By following and implementing these security measures organisations or even solo developers can create a excellent foundation or framework to ensure system/application security for their users, ensuring that data and information stored can be done so safely.

## Q7

So if I were to provide an overview of implementing confidentiality into a API project i would:

1. ENCRYPT:
Making sure all the sensitive data that is stored within the project was properly encrypted using a secure algorithm that secures data transmission and storage through disk/file encryption.
AES (Advanced Encryptions Standard) uses a symmetric encryption algorithm that is used for doing just that.
Or alternatively i would use RSA (Rivest-Shamir-Adleman) which is a asymmetric encryption algorithm that is used to do key exchanges and digitla signatures to store sensitive information. This will mean each user will have a public-private ket pair. The public key will be used for encryption and the signature verification whereas the private key will be used to decrypt the signature. 

2. ACCESSS CONTROLS:
Implementing controls to limit access to the endpoints within an API project through the use of API keys, one example of a API key is JWT tokens for authentication and authorization. These will validate the user and the users permission within the application before granting access to sensitive information.

3. DATA MASKING:
This is the simple implementation of concealing information returned in a message to the user, for example if there is an email that needs to be shown parts of it can be masked with asterisks or by hashing the data entirely!

4. SECURE STORAGE:
Ensuring secure storage via encrypting the Data inside and using strong encryption algorithms and key management to maintain data protection for the database/storage system.

## Q8

1. PRIVACY ACT:
The Privacy act 1988 ensures that the handling of personal information of asutralian government agencies and businesses with a turnover of over 3 million AUD. it sets APPs (Australian Privacy Principles) which controls the use, disclosure, collection and secruity of personal information. Social media developers are required to comply with the Privacy Act and APPs when handling all user data.

2. NOTIFY OF BREACHES TO SECURITY: 
Under the prvacy act organizations that are covered by the privacy act are required to report any users that may be affected by a possible and eligable security/data breach. This particular act/schema controls and mandates the the timely notification to all required sources when there is a unauthorized breach or access to a user/s personal information, that is likely to harm individuals.

3. SPAM ACT:
The spam act is in charge of making sure a organization or business is regulated in the sending of commercial electronic messages, this could be emails, SMS, and instant messages through social media. This partocular act will also ensure that the developers have aquired consent prior to to sending the electronic messages aswell as providing a functional unsubscribe feature.

4. TELECOMMUNICATIONS ACT: The telecommunications act regulates the access and collection of telecommunications in Australia as many social media platforms offer messaging services which are required to comply with the acts concerning the interception access and disclosure of the data/information communicated.

5. SURVEILLANCE DEVICES ACT: This particular act regulates the programs access and use of listening devices and tracking devices, in Australia. Social media platforms must ensure that they comply with acts requirements in relations to a individuals communcation and location data.

6. CONSUMER LAW:
This act regulates and prohibits the use of deceptive and misleading trade practices. Developers must ensure that ther social media application does not mislead users and that the data handling procedures are true to their nature.

7. CHILDRENS ONLINE PROVACY PROTECTION: 
Australia itself does not have a law specific to COPPA, however social media developers should still protect the personal information of any children user. Although COPPA doesnt directly target child protection and privacy it does still regulate the handling of personal information including children.

## Q9

A structual aspect of a database will include the following.

1. Tables:

- One of the fundamental structures used in all database models.
- Each table represents its own entity or concept which could be "users", "products.
- Each table is designed in a row and column form.
-Columns are referenced to as attributes which define the entity thats being shown.
- Each of these columns are also data type specific so, Integer/string/date or boolean.

2. Keys:

- Keys allow the developers to create relationsships between different tables.
- A primarky key is a unique key that identifies said record in a table. This key will ensure there are no duplicate rows.
- Foreign keys allow the developer to establish relationships between primary keys in a different table.
- Foreign keys allow for creating relational integrity through linking between related tables.

3. Relationships:

- Relationships dictate how different tables can or are related to each other.
- Commong types of relationships are one-to-one, one-to-many and many-to-many.
- In a one to one relationship in a record is related to exactly one record in another table.
- a one-to-many relationship is a single record in a table that relates to multiple records in another table, however the many records only relate to one record in the first table.
- in a many-to-many relationship many records in a table can be related to many records in another table, often requiring a joiner table (junction) to represent the relationship.

4. Normalisation:

- Normalization allows datat in a database to be organised to reduce redundancy and dependancy.
- Normalization is implicity allows the developer to break down large tables into smaller tables to minimise duplication and maintain data integrity.
- Normalization helps stop any type of data issues and ensures that the data storage is efficient aswell as the retrieval.

5. Contraints:

 - Constraint are rules and conditions that ensure the databases data adheres to the enforced integrity.
 - Typical contraints invlude, keys, unique contraints and check contraints.
- Primary keys ensure the records stored in the table are uniquely identified.
- foreign keys ensure integrity through making sure vaules match primary key vaules in related tables.
- check contraints ensure data meets a specific condition or expression that has been set before allowing it to be stored into a database.

## Q10

Relational Database Models create data integrity through making sure the data and information stored within are accurate and consistent. There are multiple types of data integrity within a relational database model and all of them play a special role in ensuring the data remains valid and reliable. These types of data integrity are referential, entity and domain integrity. Each of these relational database model integrity methods can be enforced through constraints and rules in the relational database management system.

1. ## Entity Integrity 

Entity Integrity makes sure that each table within the database carries a unique identifier for the each of its rows. This is done through the use of primary keys.

Entity Integrity is enforced through the use a Primary Key Contraints, A primary key is a unique identifier for a particular record in a table.
The Primary Key will ensure that no one record in a table can have the same value.

2. ## Referential Integrity

Referential Integrity is done through ensuring that relationships between tables are consistent specifically it ensures that foreign keys always point to an already existing and valid record within another table.

Foreign keys point to primary keys in other tables which in turn creates a relationship between the tables. The foriegn key contraint ensures that the foreign key column matches a primary key value in a referenced table even if the table is valued null.

3. ## Domain Integrity 

Domain Integrity ensures that all values within a column in a table are defined by valid values which follow a data type, format and range.

The enforcement of domain integrity is done through ensureing each column in a table is assigned a specific data type (Intger, vchar, date etc) RDMS will ensure that all the values in the colmun adhere to the data type specified.

The value constraints used in domain integrity are:

- NOT NULL Contraint:
This ensures that the column does not contain null values, making sure there is a valid value in the column

- UNIQUE Constraint:
Unique constraints ensure that all the values in a column or in multiple columns are unqiue across the table, this will prevent duplicate entries.

- CHECK Contraint:
Makes sure all values in a column meet a specific condition which in turn eforces domain rules at the data level.

- DEFAULT Contraint:
This constraint employes a default value in a column when there is no value specified, ensuring the column has always has a valid value.

## Q11

The relational database model provides several operations to manipulate data, ensuring efficient and flexible data management. These operations include adding, removing, changing, and retrieving data. Below are the main ways to manipulate data within a relational database:

### Adding Data
INSERT: The insert command is used to add new rows to a data table.
- Syntax:

```
INSERT INTO table_name (column1, column2, column3)
VALUES (value1, value2, value3);
```
### Removing Data 
DELETE Statement:

- The delete statement allows the user to remove data from rows within the table based on a condition e.g (WHERE)

- Syntax:

```
DELETE FROM table_name
WHERE condition;
```

TRUNCATE Statement: 
- The TRUNCATE statement will remove all rows from the table, however it will not delete the table itself.

- Syntax:

```
TRUNCATE TABLE table_name;
```
### Changing Data

UPDATE statement:

- The update statement allows the user to "Update" or modify the data that is already stored within the table.

- Syntax

```
UPDATE table_name
SET column1 = value1, column2 = value2, 
WHERE condition;
```

### Retrieving Data

SELECT Statement: 

- The SELECT statement is used to search for and retrieve data from a single or multiple tables.

- Syntax:

```
SELECT column1, column2,
FROM table_name
WHERE condition;
```
### COMPLEX QUERIES:

Along with the afformentioned data manipulation operations there is the ability to use complex queries to combine rows from two or more tables based on the related column, know as a JOIN, aswell as the ability to Aggregate Functions which lets us perform different calculations on a set of values to return a single value. (COUNT, SUM, AVG, MAX, MIN).
another complex query known as Subqueries, also known as nested queries allows us to embed one query in another query. This enables us to do more complex requests to refine the data retrieval requests these Sub queries can be used in 'SELECT, FROM and WHERE' clauses. Examples of each below.

- JOIN Syntax:
```
SELECT table1.column1, table2.column2
FROM table1
JOIN table2 ON table1.common_column = table2.common_column;
```

- AGGREGATE Syntax:
```
SELECT COUNT(*)
FROM table_name
WHERE condition;
```

- SUBQUERIES Syntax:
```
SELECT column1
FROM table_name
WHERE column2 IN (SELECT column2 FROM another_table WHERE condition);
```

### CONCLUSION

These operations enable comprehensive data manipulation within a relational database model, allowing users to perform CRUD (Create, Read, Update, Delete) operations to manage the data as required. By utilizing these SQL commands, users can efficiently handle and maintain the data integrity and consistency within the database.

## Q12 

1Password provides users with award winning design and industry leading security to store passwords in a private, secure and user friendly fashion the tech stack used within this application is as follows.

### Part 1. TECH STACK:


1. Programming Languages:



- C++: Is used for core parts of the applications which includes encryption and data storage. C++ is a powerful language that uses data management and memory managment incredibily well, this make C+++ very performant and efficient at data structures aswell as directly accessing hardware.

- Objective-C: Objective-C is used for macOS and ios versions as its a general purpose, object oriented programming language that is a superset of the C programming language and includes all of its capabillities.

- Java/Kotlin: This programming language is used for the android versions of the application. Java runs by a similar syntax as C/C++ which explains the choice to use it for android versions which means ease of learning for developers already familliar with those languages.
Kotlin is a statically type language that runs on the Java Virutal Machine, it is designed to be concise and reduce boilerplate code significantly. This makes it far more readable and maintainable compared to Java.

2. Frameworks and Libraries:

- SQLite: SQLite is a software library that rpovides a relational database management system for 1Password. It provides local embedded database capabilities aswell as a structured query language for query and managing the database.

- Qt: A cross-platform application framework used for building the user interface.
QT will let developers write code once and then deploy it across multiple desktops, embbedded and mobile platforms without the requirement of rewriting the original code (source code) QT is very modular and provides many modules for library networking, SQL databases, XML parsing, JSON parsing aswell as many others.

- WebKit: Provides web browsing capabilities within the application.
Webkit has support for rendering HTML and CSS which allows the 1Password to display web content within their UI.
JavaScript execution is also achievable as webkit includes the JavaScript Engine.
All in all webkit will integrates into 1Password well to provide a smooth browsing experience.

- Crypto++: A C++ library used for encryption and 
cryptographic functions. Crypto++ is a cryptographic library that provides the developer with a large suite of crytographic algorithms and functions.
Crypto++ allows for 1Password to use Encryption Algorithms, Hash functions, Digital signatures and random number generation. 

- SQLCipher: An open-source extension to SQLite used for 
database encryption.
SQLCipher uses Database encryption to encrypt and decrypt database files, its uses the AES standards for encryption securing the contents and providing excellent protection for the data/information.

- libsodium: A library for encryption, decryption, signatures, password hashing, etc.
Libsodium provides encryption, digital signatures, password hashing, secure key generation and is cross platform with Windows, Linux, MacOS and mobile platforms.

3. Operating Systems:

- Windows: A popular OS system developed by microsoft which provides the user with a GUI and the ability to do tasks on their device.

- macOS: A popular OS system developed by Apple Inc for their line of Macintosh computers, providing a simple GUI and the ability to multitask and perform said tasks within said GUI/OS.

- iOS: iOS is Apples mobile device operating system that provides a sleek GUI for users to interact and complete/do tasks within.

- Android: Android developed by Google provides a Operating system for Android devices which also provides a sleek GUI for the user to interact and complete/do tasks within.

- Web: Web is a Linux operating system developed by Palm, its GUI is entended to be simple and sleek while also implements the use of gesture-based navigation.

4. Other Tech:

- Git: A control system for managing source code so that teams can collabrate remotely through the use of git pulls/push/clones etc.

- JIRA: Issue and project tracking software for teams.
JIRA will allow the management of tasks bugs through agile project management. it will allow the tracking of the progress/collaboration among teams and helps in planning/tracking the projects sprints.

- Jenkins: Used for continuous integration and continuous deployment (CI/CD).
jenkins allows for the automation of deployment phases aswell as testing and building. It also ingrates with many different version control and testing tools.

- AWS (Amazon Web Services): Used for hosting and managing infrastructure for cloud-based services.
AWS is a large secure cloud storage infrastructure that allows the stoarge of databases, analytics, applications and deployment services.

- Fastlane: Automates beta deployments and releases for mobile apps.
Fastlane streamlines the building and deployment proccesses for iOS and android apps. It will automate the signing, building, testing and deployment aspects of apps to app stores.

5. Development Tools:

- Xcode: This is used as a intergrated development enviroment for macOS and iOS versions of the application.

- Android Studio: This is a intergrated development enviroment used for developing the application on Android.

- Visual Studio: Visual studio is a intergrated development enviroment used for developing the application on a Windows Version.

- QT Creator: This is a intergrated development enviroment that is used for/with the QT framework.

6. Encryption and Security:

- 1Password is heavily reliant on strong encryption, it uses strong encryption standards such as the AES-256 for encrypting user data while its in transit aswell as when its resting.

- Key gathering functions like PBKDF2, bcrypt and scrypt are used to hash a users password, adding another layer of security.

- Secure Number Generation is done though ising the OS provided APIs once again adding another layer of security through generation of highly secure passwords.

### Part 2. HARDWARE USED:

As the hardware is not listed by 1Password my educated guesses are:

1. Servers: 
These would have highly powerful CPUs, often 2 CPUs are utilized in servers to combat storage performance issues aswell as increase the core and hyper/multi threaded cores for better performance in computing tasks.
These servers would likely have large amounts of RAM aswell, upwards of 128gbs and un suprisingly 1TB to once again increase performance and effciency due to the large amounts of tasks and stress the servers would be under.

2. Storage: 
The main method of storage for 1Password is cloud storage through AWS, however there is likely a database storage infrastructure in place that comprimises of SSDs and HDDs although HDDs are less likely due to their slow nature, but may still be used in a static data storage format (think record keeping rather than data reading and writing) but with if the company isnt cutting costs for large static storage it is mroe likely that SSDs are used in place of HDDs, if at all.

3. Networking:
A number of routers and switches would be used to ensure minimal downtime if any.
Load balancers would be used to correctly distribute "load" or incoming traffic to multiple servers rather than overloading one server causing crashes, or performance issues.

4. Security: 
Physical Firewall devices that meet an enterprise grade are likely used for security and filtering of the networks traffic.
IDS/IPS applicances (Intrusion detection/Prevention) hardware would be used to monitor the network traffic allow the detection and prevention of potential security breaches.

5. Encryption Hardware:

Hardware Security Modules (HSMs) are dedicated pieces of hardware that are used to manage the encryption keys aswell as perform cryptographic operations in a secure fashion.

6. Backup Recovery:

Backup servers are most probable with 1Password, they would store the backup information of users.
With that is could be possible that there is a secondary data center that stores the information for recovery in case of catastrophic disaster and data loss.

7. Monitoring and Management:

Monitoring hardware to ensure the health and performance of servers and all hardware related to the application/infrastructure.

Although there is alot of hardware used within 1Password it seems that it is far more likely that anything that can reduce hardware usage via software and cloud storage systems is being implemented, however if this is my educated guess (in areas unknown) to what 1Password uses hardware wise.

## Part 3. Technologies:

Due to 1Password beign a password generation and storage application it would use a various amount of technologies to display, create, read, update and delete the data/information given to it by users. 

1. Encryption:
1Password is known to use AES-256 encryption to protect the data of the users. This particular type of technology is widely recognised encryptioon standard that is strong and ensures your information remains secure.

2. Syncing and Cloud Storage:
1Password uses many different types of cloud storages to sync the encrypted data vaults across multiple devices. This allows the use to access their passwords from any device they're using with ease.
1Password also uses end-to-end encryption which essentially means you have access to your sensitive information and only your information.

3. Multi-Factor Authentication (MFA):
1Password encorporates MDA to add another layer of protection for their users. The MFA process can be done via many different applications but not limited to Google Authenticator or Authy.

4. Cross-Platform Compatibility:
1Password supports its use over multiple types of Operating platforms (Windows, macOS, iOS, Android aswell as web browsers) This is done through the use of development frameworks/processes and APIs specific to the platform.
 
5. Password Generation:
1Password can generate passwords for the users that are complex, strong and completely RNG removing the need for personal passwords. This will ensure any attackers are unable to "guess" the users password.

6. User Interface and Experience:
1Password has a sleek and seamless user experience across many different interfaces (desktop, browsers, mobile apps) which is done though userface frameworks which follow a design and pattern similar to each other for the user over said appication accesses.

7. APIs and Intergrations:
1Password uses APIs that allow the developer to properly integrate the applications functionality into other applications. Features such as accessing passwords, managing vaults and performing other actions are all features of the intergration.

8. Secruity Practices: 
1Password follows the best practices when it comes to security. This includes audits, bug fixing programs and complying with standards such as GDPR (General Data Protection Regulation) and SOC 2 (System and Organization Controls 2).

## Part 4. Data Structure in 1Password:

1. Vaults:
Vaults are used as the primary storage container within 1Paswword. Each vault can hold multiple items which consist of passwords, notes, credit card information and other sensitive information. Some items will have a defined structure dependant on their type, for example different vaults for personal or work related information.

2. Items:
Within each of the "vaults" are items and each item can represent a certain type of data be it login information, secure notes or a bank account. These items all have a predefined structure which is based off of their type, for example

- Login items will typically include a username and password, URL and additional notes.
- Secure Notes on the other hand contain a large field for text for storing any type of sensitive data that the user may want to.

3. Fields:

Each item will contain various "fields" to which each field stores a piece of data that can include data such as:

- Text allowing for usernames, passwords or notes.
- Fields for data that may have an expiration date.
- A field for attaching different documents or images.

4. Metadata:

Each of the items within the fields in the vaults have metdata. Metadata includes:
- Timestamps of creation and modification.
- UUIDs which are unique identifiers for each item and field
- Versioning which supports information about any changes and revisions to features like item history for example.

5. Encryption:

1Password as previously observed implements end to end encryption for data security.

This is achieved through encryption keys, these keys are derived from the users master password and other cryptographic elements.
It also ensures that data is not only encrypted while its being transferred but also while it sits in static form waiting for transferal.

6. Syncing and Backup:

Information stored by the user in 1Password is not only syned to the AWS cloud but it is also sycned to the local device, which will allow for a backup copy to be stored in case of catastrophic failure or for the use of the applications features offline.

7. Sharing and Permissions:

1Password has the ability to share vaults with others. This can be done through the changing and allowing of certain permissions changing control access levels for others.

- Read-Only or Full Access: 1Password allows for read only or a Full Access permissions for multiple users. This will give the people a vault is shared with either Read access only or the same permissions as the admin/owner of the vault.

8. Database Structure:

The main underlying structure for 1Password is a mixture of relational and non relational database management, this allows the application to handle differet types of information effciently.

- SQL is used to structure data in relationships and querying 
- NoSQL is used for a more flexible ane salable storage of non structured or semi structured data.

9. Data Integrity:

1Password incorporates checksums and hashes to properly detect if any data has been corrupted.
Aswell as using Audit lofs to track how the data has been accessed and any changes to said data.

## Part 5. 1Password Entities and Tables:

1. Vaults: 

- Each user in 1Password can have multiple vaults, which collect items and store them.
- These vaults can be shared among others, be they users or team members.

2. Items/Entries:

-Items are seperate and individual entries stored within a vault.
- The different types of items can be login details, credit card information, notes, identities, passwords and bank account information to list a few.


3. Fields:

- fields are individual pieces of information that is stored within a item/
- Examples of fields are usernames, passwords, credit card numbers etc.

4. Users:

- Here information about the user who has access to specific vaults.
- This will include usernames, passwords and roles set by the main user.

5. Teams/Members:

- This will allow for the organisation for managing multiple users, popular for team or business enviroments where multiple people are required to access the same information easily.
- This is done through user permissions and the access control granted.

6. History:

- This will track any changes to the items, which will allow the user to view or even go back to a previous version of an entry.

## Part 6. Relationships Between Entities/Tables:

- Users to Vaults - One to many (A single user can have multiple vaults)
- Vaults to Items - One to many(A single vault can have multiple items)
- Items to ItemHistory - One to many (A single item can have multiple histories)
- Teams to TeamMemberships - One to many (A single team can have multiple memberships)
- Users to TeamMemberships One to many (A single User can belong to multiple teams)
- TeamMemberships to Teams - Many to one (A single membership links to only one team)
- TeamMemberships to user - Many to one (A single membership belongs to only one User) 

## Part 7. 1Password ERD Diagram.

![ERD Diagram](./1Password%20ERD.drawio.png)