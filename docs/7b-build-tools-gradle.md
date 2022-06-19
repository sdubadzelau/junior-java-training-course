[![index.md](assets/back_main_page_icon_124174_32.png)](index.md) [Go to Contents](index.md)

## Build Tools

### Gradle
Gradle one of the de facto standard build tools for programming languages and ecosystems
Features:
  - Runs on Java virtual machine
  - Build logic defined as instructions in a script
  - Plugins can provide predefined functionality
  - Tool can be executed from the terminal and IDE

Terminology:
  - Project: models a software component
  - Build script: contains automation instructions for a project
  - Task: defines executable automation instructions

Gradle defines a domain specific language (DSL):
  - Groovy DSL
  - Kotlin DSL

#### The Gradle Wrapper
- Gradle wrapper is a set of files checked into SCM alongside source code
- Standardizes compatible Gradle version for a project
- Automatically downloads the Gradle distribution with defined version

#### settings.gradle
We can define multi-project build in the file named **settings.gradle**
- Resides in root directory
- Declares participating projects
- Can change defaults(e.g. project name)

#### gradle.properties
- Resides on root directory of project hierarchy or Gradle user home directory
- Preconfigures runtime behavior

#### Tasks
- Types: 
  - Ad Hoc Task
    - Implements one-off, simplistic action code by defining doFirst or doLast
    - Automatically extends DefaultTask without having to declare it
  - Typed Task
    - Explicitly declares Type (e.g. Copy, Zip)
    ```
      task copyDocs(type: Copy) {
      from 'src/main/doc'
      into 'build/target/doc'
      }
    ```
    - Does not necessarily need to define actions as they are already provided by type
- Execution Order
  - Directed Acyclic Graph (DAG)
  - Issue: Circular Dependencies

#### Build lifecycle phases
- Initialization phase
  - Evaluates settings file sets up build
- Configuration Phase
  - Evaluates build scripts and runs configuration logic
  - But task are not executed, it is just configured
  - Configuration code is always outside of `doFirst` and `doLast` actions
  - Configuration code es executed during configuration phase
- Execution Phase
  - Execute task in a correct order
  - Always inside of `doFirst` and `doLast`

#### Plugins
- Goals:
  - Avoid repetitive code
  - Make build logic more maintainable
  - Provide reusable functionality across projects
- Types:
  - Script Plugin: 
    - Same syntax, just a different file
    - `apply from: example.gradle`
  - Binary Plugins: 
    - Implemented as a class; bundled as JAR files
    - more complex
    - `apply plugin: "base"`

#### Domain Objects in Memory
- Gradle represents the DAG in memory
- Task are just one domain object of a build
- Domain objects can be inspected and modified from the build script
- The DAG cannot be modified once it has been created in memory.

Important Domain Objects:
- Gradle domain object - represents invocation of the build 
  <details>
    <summary>Expand...</summary>
    <p>This domain object has knowledge about the project hierarchy in a single project,
    or multi-project build provides pointers to the higher level properties of a build. 
    For example, the Gradle user home directory or the Use Gradle version and can register callback 
    logic to react to certain events in the build. </p>
  </details>
- Project domain object - represents a software component and provides API access to object hierarchy
  <details>
    <summary>Expand...</summary>
    <p>The project domain object serves as the main entry 
    point of a build. It provides methods for walking the whole hierarchy of domain objects. 
    For example, you could ask for the reference to the Gradle instance, register new tasks, 
    or get an modified typical environmental properties like the build output directory.</p>
  </details>
- Task domain object - Represents unit of work with potential dependencies
  - Task define at least one action
- Action Domain Object - Actual work performed during execution phase
- Plugin Domain Object (`org.gradle.api.Plugin`)
  - Provides reusable logic for project


### Part 2: From Presentation
- Declarative(Maven) and Imperative(Ant) style of build scripts
  - Gradle: Declarative? -Yes, Rigid? -No
  - Gradle can be imperative
  - In Gradle we always try to separate declarative and imperative parts.
  - Build script should be spec like

- Extensible Build Language(sourceSets) vs Build Framework ?
  - With Gradle you can do what you want, you can create plugin with your own requirements.
- 
- Multi-Modules build
- Gradle has very good Ant integration
- Gradle has good integration with Maven on repository level

### Questions
1. What is Gradle Framework?
   - It is a type of automated build system which is open source and creates builds on the concepts of Apache Ant and Maven. It uses a domain-specific language (DSL) which is based on Groovy to declare the configuration of the project. It doesn’t use the XML form that Apache Maven uses for this declaration.

2. Q: What is Gradle Wrapper?
   - A:The Gradle Wrapper is the preferred way of starting a Gradle build. The wrapper is a batch script on Windows, and a shell script for other operating systems. When we start a Gradle build via the wrapper, Gradle will be automatically downloaded and used to run the build.

3. Q: How do you add gradle dependencies ?
   - A:To add a dependency to your project, specify a dependency configuration such as compile in the dependencies block of your build.gradle file.

4. Explain Groovy?
   - A: Gradle uses a programming language that is written in script form, and the name of that script is Groovy. The features of this language are:
     - It interoperates with Java easily as Groovy operates on JVM (Java Virtual Machine).
     - To write a build script, you don’t have to learn Groovy.
     - It is simple to write and read a Groovy due to its smaller codes than Java.
     - It is a dynamic and flexible language that works somewhat similarly to Java. It is also compatible with the byte code of JVM.

5. What is the file name built by Gradle?
   - A: Build.gradle is the name of the file name that Gradle builds.

6. Why developers prefer Gradle over other Frameworks?
   - A: Developers prefer Gradle over other Frameworks because it uses Groovy for scriptwriting which has a similar syntax to Java. It is easy to understand and also offers support for multi-build projects.

7. What is Dependency Configuration? Explain
   - A: A configuration dependency is a set of dependencies that includes external dependency that you require to install and ensure that the downloading is happening via the web. Some key features of dependency configuration are:
     - **Compilation**: The initial project that you will start and work on should be well-compiled. Also, ensure that you maintain it in good condition.
     - **Runtime**: Runtime is the preferred time that you need to complete the work dependency in a collection form.
     - **Test Compile**: It requires a complete collection for making the project run.
     - **Test Runtime**: It’s the final process that requires the checking to complete for running a test which is the default runtime mode.

8. What are the two types of plugins in Gradle?
   - A: Two types of plugins in Gradle are:
     - Script Plugins: This provides the additional build script which gives a declarative approach for manipulating the build, and is typically used within a particular build.
     - Binary Plugins: These consist of the classes which are responsible for implementing the plugin interface. It adopts a programmatic approach in order to perform manipulation of the build.

9. Name the configuration files of the Gradle build concept?
   - Build.gradle define the script for build configuration
   - The other script in demand is settings.gradle
   - Another option is gradle.properties



