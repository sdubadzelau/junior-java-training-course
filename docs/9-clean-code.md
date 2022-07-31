[![index.md](assets/back_main_page_icon_124174_32.png)](index.md) [Go to Contents](index.md)

### Clean Code

- **"What Is Clean Code?**
  - Clean code can be summarized as a code that any developer can read and change easily.
- **Why Should We Care About Clean Code?**
  - Maintainable Codebase
  - Easier Troubleshooting
  - Faster Onboarding
- **Characteristics of Clean Code**
  - Focused
  - Simple
  - Testable
- **Clean Coding in Java**
  - **Project Structure**
    - It's always useful to follow a consistent pattern to organize our source files, tests, configurations, data, and other code artifacts.
  - **Naming Convention**
  - **Source File Structure**
  - **Whitespaces**
  - **Indentation**
  - **Method Parameters**
    - a long list of parameters can make it difficult for someone to read and understand the code
  - **Hardcoding**
  - **Code Comments**
  - **Logging**
    - Importance of logs can not be over-emphasized in development in general and maintenance in particular
- **SOLID**
- **DRY & KISS**
- **TDD**
- **Tools for Help**
  - Code reviews
  - Code Formatters: IDE, etc
  - Static Analysis Tools:
    - SonarQube, Checkstyle, PMD and SpotBugs"


### Questions:

- How can we understand that function does one thing?
  - A: We cannot extract the another function from it.
- Why using if statement in method is bad practice?
  - A: Because we can extract method.
- Why do we need avoid switch statements?
  - A:
    - Many methods, 
    - because if we need to modify we fail open-close principle
    - Switch statement is a dependency magnet, if change, all should be recompiled
- Why do we need to prefer exceptions to returning error codes?
  - A:
- Why we don't have to use nested try catch blocks?
  - A:
- Why we should follow DRY?
  - A: If code duplicates we can extract it to method.
  - A: We can extract loop into Lambda for example
- Structured Programming?
  - A: 
- Why do we need to test each line of code?
  - A: 
- What can you say about comments regarding the Clean Code?
  - A: Use comments only if code cannot explain itself.
  - Not all comments are bad, some great.
  - Delete comment and fix the code if the comment is not understandable.
  - Use comment with regular expressions
- What do you think about JavaDoc?
  - A: USe when you are providing external API only
  - Don't write stupid JavaDoc and comments, like some kind of repeating fields or parameters name, examples:
    - This is Default Constructor
    - The name - `private String name`
    - the license name
    - The version (`private String version`)
    - `/* Added by Rick */`
- How long source file should be?
  - A: File size this is a style of project, you can select
- How long should be line?
  - A: 
- What intent should we use?
  - A: 
- Avoid convenient misspellings
  - A: 
- Noise words?
  - A:
- How much time should you spend on Code Review?
  - A:



