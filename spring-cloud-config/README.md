What you’ll build

You’ll setup a Config Server and then build a client that consumes the configuration on startup and then refreshes the configuration without restarting the client.

https://spring.io/guides/gs/centralized-configuration/

	we set management.endpoints.web.exposure.include=* in the client app to make this easy to test (by default since Spring Boot 2.0 the Actuator endpoints are not exposed by default). By default you can still access them over JMX if you don’t set the flag.
