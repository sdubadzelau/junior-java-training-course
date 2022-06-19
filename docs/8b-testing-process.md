[![index.md](assets/back_main_page_icon_124174_32.png)](index.md) [Go to Contents](index.md)

### Testing

- Non-functional testing
  - Performance
  - Stability
  - Usability
  - Security
  - I18n and localization
  - Destructive

#### Unit Testing - Principles
- F **Fast** - Unit tests should be fast otherwise they will slow down your development/deployment time and will take longer time to pass or fail.
- I **Independent** (Isolated) - Never ever write tests which depend on other test cases.
- R **Repeatable** A repeatable test is one that produces the same results each time you run it.
- S **Self-validating** - Tests must be self-validating means – each test must be able to determine that the output is expected or not. It must determine it is failed or pass. There must be no manual interpretation of results.
- T **Timely** - Practically, You can write unit tests at any time. You can wait up to code is production-ready or you’re better off focusing on writing unit tests in a timely fashion.

See more - https://howtodoinjava.com/best-practices/first-principles-for-good-tests/

Naming conventions: https://dzone.com/articles/7-popular-unit-test-naming


### Questions
- What can be considered a unit in unit testing?
  - A: A unit is the smallest testable part of an application.
- Describe what AAA and Given-when-then.
  - A: 
    - The AAA (Arrange-Act-Assert) pattern has become almost a standard across the industry. It suggests that you should divide your test method into three sections: arrange, act and assert. Each one of them only responsible for the part in which they are named after.
    - Given-When-Then (GWT) is a semi-structured way to write down test cases. They can either be tested manually or automated as browser tests with Selenium.
    <br>It derives its name from the three clauses used, which start with the words given, when and then. Given describes the preconditions and initial state before the start of a test and allows for any pre-test setup that may occur. When describes actions taken by a user during a test. Then describes the outcome resulting from actions taken in the when clause.
- What is an assertion and how work, what are the main functions there?
  - A: Assertions are utility methods to support asserting conditions in tests; these methods are accessible through the Assert class, in JUnit 4, and the Assertions one, in JUnit 5.
    - JUnit4: `assertEquals, assertArrayEquals, assertNotNull and assertNull, assertNotSame and assertSame, assertTrue and assertFalse, fail(), assertThat`
    - JUnit 5 Assertions: `assertArrayEquals, assertEquals, assertTrue and assertFalse, assertNull and assertNotNull, assertSame and assertNotSame, fail, assertAll, assertIterableEquals, assertLinesMatch, assertNotEquals,
      assertThrows, assertTimeout and assertTimeoutPreemptively`
- Introduce mocking, what it does, what tools you can use, and how
  - A: Mocking means creating a fake version of an external or internal service that can stand in for the real one, helping your tests run more quickly and more reliably. When your implementation interacts with an object's properties, rather than its function or behavior, a mock can be used.
- What is stubbing, and how can you use it
  - A: Stubbing, like mocking, means creating a stand-in, but a stub only mocks the behavior, but not the entire object. This is used when your implementation only interacts with a certain behavior of the object.
- What are mock, stub, dummy, and fake and when should we use them?
  - A: 
    - Fake: Fakes are objects that have working implementations, but not the same as production one. Such as: in-memory implementation of Data Access Object or Repository.
    - Stub: Stub is an object that holds predefined data and uses it to answer calls during tests. Such as: an object that needs to grab some data from the database to respond to a method call.
    - Mocks: Mocks are objects that register calls they receive. In test assertion, we can verify on Mocks that all expected actions were performed. Such as: a functionality that calls e-mail sending service.
- Introduce the FIRST principle
  - A: See above at this page
- When can we say that a unit test is a good unit test
  - A: If test fits FIRST principle it can be considered as good 
- What other approaches should you follow to have good unit tests
  - A: See 13 Tips Here: [13 Tips for Writing Useful Unit Tests](assets/13%20Tips%20for%20Writing%20Useful%20Unit%20Tests%20_%20by%20Nick%20Hodges%20_%20Better%20Programming.pdf)
- Introduce test coverage, what it is, and how it should be used
  - A: The test coverage report provides information about parts of the software where test coverage is being implemented. Essentially, it provides information about the tests executed on an application or website.
  - See more here: https://www.browserstack.com/guide/code-coverage-vs-test-coverage
