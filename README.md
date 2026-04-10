# InterviewQuestionsByMegh
## Spring core (IOC, DI, Bean scopes, qualifiers)  
### Spring IOC - Inversion of Control : 
[Source of answer](https://medium.com/@ksaquib/a-quick-introduction-to-inversion-of-control-ioc-in-spring-a67a644aeb0c) </br>
- The responsibility of managing object instantiation and dependencies is shifted from the application itself to an external entity. </br>
Rather than tightly coupling components and controlling their lifecycle internally, IoC promotes loose coupling and delegates control to frameworks or containers.
- an object factory that dynamically creates instances of messaging service based on a configuration. We’ll then use this factory to instantiate different messaging services.
- the Spring container manages object creation and dependency injection, allowing us to configure and switch between different messaging service implementations effortlessly.
- Through Spring’s dependency injection mechanism, we can inject the desired messaging service implementation into our application components without hardcoding dependencies. This promotes modularity, testability, and maintainability, as components remain loosely coupled and easily replaceable.

### [Spring boot Annotations](https://www.geeksforgeeks.org/springboot/spring-boot-annotations/) : </br>
#### Spring boot annotations >> 
1. @SpringBootApplication Annotation </br>
This annotation is used to mark the main class of a Spring Boot application.</br>
It encapsulates @SpringBootConfiguration, @EnableAutoConfiguration and @ComponentScan annotations with their default attributes.
2. @SpringBootConfiguration Annotation
Indicates that a class provides configuration for a Spring Boot application. It is a specialized version of @Configuration and is automatically included in @SpringBootApplication.
3. @EnableAutoConfiguration Annotation
Enables Spring Boot’s auto-configuration mechanism, automatically configuring beans based on classpath dependencies and application properties.
4. @ComponentScan Annotation
Tells Spring where to search for components like @Controller, @Service, @Repository, etc.
