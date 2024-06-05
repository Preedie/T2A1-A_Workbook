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

