https://spring.io/guides/gs/centralized-configuration/

	we set management.endpoints.web.exposure.include=* in the client app to make this easy to test (by default since Spring Boot 2.0 the Actuator endpoints are not exposed by default). By default you can still access them over JMX if you don’t set the flag.
