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

#### Spring Bean Annotations
1. @Component
Marks a class as a generic Spring-managed component. Spring automatically detects and registers it during component scanning.
2. @Service </br>
-- Used in the service layer to define business logic and improve code readability. </br>
   @Autowired
   private UserService userService; // ❌ will fail if UserService has no @Service
-- Harder to maintain and understand
3. @Repository
Used in the DAO layer to interact with the database. Automatically translates database-related exceptions into Spring exceptions.
4. @Configuration
Indicates that a class contains Spring configuration and bean definitions. Acts as a replacement for XML-based configuration.
5. @Bean
Used to define a Spring bean explicitly inside a configuration class. Gives full control over bean creation and lifecycle.

#### Dependency Injection Annotations
1. @Autowired
Automatically injects required dependencies into a class. Eliminates the need for manual object creation.
2. @Qualifier
Specifies which bean to inject when multiple beans of the same type exist.
3. @Primary
Marks a bean as the default choice among multiple candidates. Used when no @Qualifier is explicitly specified.

Note: Qualifier overrides Primary when both are mentioned together

#### Web and REST API Annotations
1. @RestController
Used to create RESTful web services and automatically returns data in JSON or XML format
2. @RequestMapping
Maps HTTP requests to controller classes or methods. Defines the base URL path for request handling.
3. HTTP Method Annotations
@@GetMapping, @PostMapping, @PutMapping, @DeleteMapping
4. @PathVariable
Extracts values from the URI path and binds them to method parameters.
5. @RequestParam
Reads query parameters from the request URL. Used for optional or filtering inputs.
6. @RequestBody
Binds the HTTP request body to a Java object. Commonly used with POST and PUT requests.

#### Exception Handling annotations
1. @ExceptionHandler
Handles specific exceptions within a controller. Allows custom error responses for exceptions.
2. @ControllerAdvice
Provides global exception handling across all controllers. Centralizes error-handling logic.

#### JPA
Entity, column, table, id etc

### [Bean Scopes]()  </br> 
Singleton : The Spring container creates only one instance of the bean per Spring IoC container. </br> 
This single instance is shared across the entire application context and all subsequent requests for that bean return the same object
Prototype : A new instance of the bean is created every time it is requested from the container.
request : A new instance of the bean is created for each individual HTTP request. It is destroyed when the request processing completes
Session, Application, Web Socket 



