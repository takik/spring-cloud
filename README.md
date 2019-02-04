# spring-cloud-intro
Introduction to Spring Cloud Netflix – Eureka


https://www.baeldung.com/spring-cloud-netflix-eureka

In this tutorial, we’ll introduce client-side service discovery via “Spring Cloud Netflix Eureka“.

Client-side service discovery allows services to find and communicate with each other without hard coding hostname and port. The only ‘fixed point’ in such an architecture consists of a service registry with which each service has to register.

A drawback is that all clients must implement a certain logic to interact with this fixed point. This assumes an additional network round trip before the actual request.

With Netflix Eureka each client can simultaneously act as a server, to replicate its status to a connected peer. In other words, a client retrieves a list of all connected peers of a service registry and makes all further requests to any other services through a load-balancing algorithm.

To be informed about the presence of a client, they have to send a heartbeat signal to the registry.

To achieve the goal of this write-up, we will implement three microservices:

a service registry (Eureka Server),
a REST service which registers itself at the registry (Eureka Client) and
a web-application, which is consuming the REST service as a registry-aware client (Spring Cloud Netflix Feign Client).
