## Users of Database System
- Database designer: *logical Designer* and *Physical Designer* 
- System Analyst & Application Programmers: Determine the requirements of end users analysts determine specification programmer implements it
- End users: These are general users
- Database Administrator: 

## DBMS Architecture
- The DBMS design depends upon its architecture. The basic client/server architecture is used to deal with a large number of PCs, web servers, database servers and other components that are connected with networks.

- DBMS architecture depends upon how users are connected to the database to get their request done.

### Types of DBMS Architecture.
#### 1-tier Architecture
- Also called Monolithic Architecture
- All layers of an application are combine into one deployment unit and run on the same machine or server. the database is directly available to the user. It means the user can directly sit on the DBMS and uses it.

#### 2-tier Architecture
- In a 2-tier architecture, the application is divided into two layers: *the client layer* and *the server layer*. 
- The client layer, also known as the front-end, handles the user interface and interacts with the user. 
- The server layer, also known as the back-end, contains the database and handles the data storage and retrieval. 
- The client layer communicates directly with the server layer to access and manipulate the data. 
This architecture is commonly used in client-server applications like

- In order to learn the Structure Query Language (SQL), we set up our SQL server and the database on our local system. This SQL server enables us to directly interact with the relational database and execute certain operations without requiring any network connection. This whole setup to learn SQL queries is an example of Single-Tier DBMS architecture.




- **The main disadvantages of Two-Tier DBMS Architecture are:**

- Scalability - As the number of clients increases, the load on the server increases. Thereby declining the performance of the DBMS and, in turn, the client-side application.
- Security - The Direct connection between the client and server systems makes this architecture vulnerable to attacks.

- Consider a situation where you went to a bank to withdraw some cash. After entering the withdrawal amount and the account details on the withdrawal slip, the banker will go through the server-side database via his credential (API call) and will check whether there is enough balance present or not. This client-server model is an example of Two-Tier DBMS architecture.



### 3-tier Architecture
- The 3-tier architecture further separates the application into three layers: the presentation layer, the application layer, and the data layer.
- The presentation layer handles the user interface and user interaction, similar to the client layer in the 2-tier architecture. 
- The application layer, also known as the business logic layer, contains the application's logic and processes user requests. 
- The data layer, similar to the server layer in the 2-tier architecture, handles data storage and retrieval. 
- This architecture provides better scalability and flexibility by decoupling the different layers.



### N-tier Architecture
- The N-tier architecture is an extension of the 3-tier architecture, where the application is divided into multiple layers or tiers. Each tier is responsible for specific functionality, such as presentation, business logic, data access, and data storage. This architecture allows for better modularization and scalability, as each tier can be developed and scaled independently.

- NB **When the layers are increased in the architecture, the level of abstraction also increases, resulting in an increase in the security and the complexity of the DBMS structure.**


# Database modelling
- Divided into 2 phases:
      1. Conceptual Modelling
      2. Logical Modelling

- Conceptual modeling is the initial phase of database design, where the focus is on understanding and representing the real-world entities, relationships, and constraints that the database needs to capture (overall view of the real world). 

- The main goal of conceptual modeling is to create a conceptual schema, which serves as a blueprint for the database design.

- Involves the use of entity-relationship diagrams (ERDs) to represent entities (things of interest),

- Logical modeling is the next phase in the database design process. It takes the conceptual schema from the conceptual modeling phase and translates it into a more detailed representation that is closer to the actual implementation. 
- The focus shifts from the high-level concepts to the specifics of how the data will be organized and stored in the database system.

- N/B all this is represented in an ERD diagram

## Relationship
- Cardinality ratio of relationship: Maximum number of relationship instances an entity can participate.

#### One-to-one Relationship
- A relationship where each entity in one table is related to at most one entity in another table

#### One-to-many Relationship
- It is a relationship between two entities where one entity can be associated with multiple instances of the other entity, but each instance of the other entity is associated with only one instance of the first entity. 
- FK in many I.E employee and office fk will be in employee

## Weak and Strong entities

### Weak(surbodinate) entity
- A weak entity is an entity that cannot be uniquely identified by its own attributes alone. 
- It depends on a related entity, known as the dominant entity, to establish its identity.
- A weak entity has a primary key that consists of its own attributes as well as the foreign key(s) referencing the owner entity