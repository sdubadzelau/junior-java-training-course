[![index.md](assets/back_main_page_icon_124174_32.png)](index.md) [Go to Contents](index.md)

## Spring
Initially started as dependency injection framework.
### Spring Core
Injects dependencies at runtime.
#### Dependency Injection
##### Spring IoC Container
* Create Objects
* Manage Lifecycle of Objects
* Inject dependencies to our class/es
* **BeanFactory** interface
* **ApplicationContext** interface - extends BeanFactory interface, provide more features. Recommended by Spring instead of BeanFactory.
* **ClassPathXmlApplicationContext** - implements ApplicationContext interface
* **AnnotationConfigApplicationContext** - implements ApplicationContext interface

IoC Container reads the XML Configuration file and create the required objects and inject them at runtime in our classes.
Spring Bean - Java POJO managed by Spring.

XML Configuration: <bean id=" ...>
Annotation Configuration: @Bean

* Types of Dependency Injection 
  * Setter Injection
  * Constructor Injection
  * Field Injection
* Component Scanning: @ComponentScan(basePackages = "com.com"), @Component
* Autowiring: @Autowire Bean can be injected by name(name convention used)
  * By Type
  * By Name
  * @Primary used for prioritizing  candidate for Injection
  * @Qualifier 

##### Bean Scopes 
It controls how many times bean can be initialized in the container
* Singleton - 95% - cretate bean only one time when container is starting. The same bean(object) can be reused
* Prototype - bean is created each time when it is requested.
* Request - creates unique bean for each incoming HTTP request
* Session - bean created for each HTTP session
* Application - bean is created only once for the serverless environment 
* Websocket - bean is created once for the websocket enrolment in application in websocket application context 

##### Bean Lifecycle
* Initializing Phase
* Bean Usage
* Destruction Phase
* InitializingBean, DisposableBean interfaces that bean should implement: methods: afterPropertiesSet, destroy 
* JSR-250 annotations (@PostConstruct, @PreDestroy)
* initMethod, destroyMethod from @Bean

##### Read External Properties
* Property files are used to externalize th configuration(eg: Database URL)
* Prevents Hard Coding
* Can be injected at runtime

@PropertySource(value="classpath:/path to property file"), then use @Value("${db.uri}")


Usage: @Scope("singleton")







