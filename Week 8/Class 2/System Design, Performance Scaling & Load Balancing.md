# System Design, Performance Scaling & Load Balancing

Class: Server
Class Date: July 2, 2021

Pdf Link: https://drive.google.com/file/d/1Pq6IKgeomKDsL3_IKGOIgk-t6phmjKIh/view


Video Link: https://drive.google.com/file/d/1QN9pC8bGolSP9SI6AQ0calvwZvZhR3Bu/view

------



**Monolithic Architecture :** 3 tiers are in 1 Server. (Not Always)

Can we call a Microservice Architecture if we divide 3 Layers in 3 servers?

> No we cannot call it microservice as long as Business Logic Tier is together. As long as all Business Logic Stay Together, we call it Monolithic Architecture. Even if we use A Load Balancer to Duplicate 1 Server into 5 Servers, it still isn't Microservice because we haven't split the Business Logic, we have just cloned it. Only When we DeCouple Business Tier, we call it Microservice Architecture.

[Introduction to Monolithic Architecture and MicroServices Architecture](https://medium.com/koderlabs/introduction-to-monolithic-architecture-and-microservices-architecture-b211a5955c63)

[Monolithic vs. Microservices Architecture](https://articles.microservices.com/monolithic-vs-microservices-architecture-5c4848858f59)

[What is database sharding?](https://www.educative.io/edpresso/what-is-database-sharding)

[Understanding Database Sharding | DigitalOcean](https://www.digitalocean.com/community/tutorials/understanding-database-sharding)

