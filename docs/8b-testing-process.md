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

#### Other question list:
1. What are unit tests and why we use them?
2. What is TDD?
3. Why we use red to green method?
   1. The basic idea is no code is written before there is failing test (RED). When you have a failing test, then you write the code to pass the test (GREEN).
4. How to test if code is throwing proper type of exception?
   1. JUnit <= 4.12 : `@Test(expected = IndexOutOfBoundsException.class)`
   2. JUnit > 4.13 : `assertThrown(callMethod)`
      ```
         @Test
         public void testFooThrowsIndexOutOfBoundsException() {
            Throwable exception = assertThrows(IndexOutOfBoundsException.class, () -> foo.doStuff());
            assertEquals("expected messages", exception.getMessage());
         }
      ```
   3. More examples : https://stackoverflow.com/questions/156503/how-do-you-assert-that-a-certain-exception-is-thrown-in-junit-4-tests/2935935#2935935
5. What are Stubs? When we use them? (Stubbing third party services)
6. How to use Stubs? (Write a stub, inject it to service, use in tests)
7. What is the Mock?
8. What is the most common library for using stubs/mocks?
   1.  EasyMock, JMock, EasyMock 2, Mockito
9. How to use mocks using mockito?
10. How to check if the method from mock service was called?
    1. To check if a method was called on a mocked object you can use the `Mockito.verify` method:
       ```
          Mockito.verify(someMock).bla();
          Mockito.verify(someMock, Mockito.times(0)).bla();
          Mockito.verify(someMock, Mockito.times(23)).bla();
          Mockito.verify(someMock, Mockito.never()).bla(); // same as Mockito.times(0)
          Mockito.verify(someMock, Mockito.atLeast(3)).bla(); // min 3 calls
          Mockito.verify(someMock, Mockito.atLeastOnce()).bla(); // same as Mockito.atLeast(1)
          Mockito.verify(someMock, Mockito.atMost(3)).bla(); // max 3 calls
       ```
11. How to use a wildcard in verify method (anyString())
12. What is Fake object?
13. When we use fakes?
14. How to set up mocks for all tests methods?
    1. ?
15. What is tautology in test?
    1. TTDD – Tautological Test Driven Development as an anti-pattern of TDD
    2. Tautology Tests - They assert that the code is correct by ensuring the code executes as written which, of course, assumes the way it is written is correct.
    3. What are the common characteristics of a Tautological Test?
       1. Asserts more interactions with collaborators than the outputs;
       2. It doesn’t really test the behaviour of the class, but only its implementation
       3. The test is too white box
       4. Too much mock setup deviates the intent of the test
       5. Adding a new feature or changing an existing one requires changing mock expectations
16. What is spy and why we use it?
17. How to use Spy object?
18. What are the FIRST principles of good unit tests
19. What other good practices do you know? (http://www.kyleblaney.com/junit-best-practices/) 
