# JPA_SpringNotes
Spring Framework: Spring Data JP 5 with Hibernate 

What is spring: Spring used for less complexities of java. Spring is POJO based and interface driven. 


Best practice: singleton, factory, abstract factory, and template methods. Annotation based    configuration based. 


JPA (Java Persistence API): started as hibernate, ORM, POJO based, focuses on good OO design. Multiple providers. It’s a bridge between spring app models and the database. 



Problems JPA and hibernate solves: developers != DBAs , data model doesn’t always line up with object model, configuration( better with JPA but even more so when spring steps in). The business focus-Business cares that you get a certain query done and its shoved in an object.

JPA is the solution: It removes boiler plate code, stays in object, spring handles all configuration and transactions behind the scene, testable, transactions are transparent to the developer, annotation/java based.  



Components: We represent the tiers with Spring with the three components: Controller, Service and Repository. Controllers: route where we’re going and interpret the user’s request. Service: where our business logic goes. Also be where our transactions will likely start if accessing more than one database table. Repository: sometimes referred to as a data access object. Usually has as one to one mapping with database table.


Annotation: getting the framework up to speed, allow you to get the framework to get things done without having to build equivalent functionality yourself.



Controllers: handle request/response, no business logic should be handles here, coordinate with service and repository, annotated with @Controller, handles exceptions and view routing


Service: Annotated with @Service, describes verbs/actions of system, business logic belongs here, ensures business object state, transactional, often has same methods as repository but a different focus.


Repository: Annotated with @Repository, Nouns(data) of the system, focuses on interacting with database or basic CRUD functions, often one to one database table mapping.


Transaction-needs to be annotate with @Transactional 
