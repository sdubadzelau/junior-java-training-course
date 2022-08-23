[![index.md](assets/back_main_page_icon_124174_32.png)](index.md) [Go to Contents](index.md)

## Agile Software Development

The agile approach—which emphasizes continuous delivery and improvement, collaboration, and openness
to change—can help professionals enhance both their productivity and the quality of their final products.

Course Goal

    Agile principles
    Scrum roles, artifacts, and rules
    Common myths and misconceptions about agile approaches
    Agile software engineering techniques
    Extreme programming (XP) and test-driven development (TDD)
    Kanban for developers
    Limiting work in progress (WIP)
    Scaling the output of agile teams

### Waterfall
90-s
1. Stages
   1. Requirements
   2. Analysis and Design
   3. Development
   4. Testing
   5. Deployment and Maintenance
2. It prioritizes processes over people

## Agile
Many unpredictable things.
IT is Iterative and Incremental.

Agile Manifesto:
1. Customer satisfaction by early and continuous delivery of valuable software.
2. Welcome changing requirements, even in late development.
3. Deliver working software frequently (weeks rather than months).
4. Close, daily cooperation between business people and developers.
5. Projects are built around motivated individuals, who should be trusted.
6. Face-to-face conversation is the best form of communication (co-location).
7. Working software is the primary measure of progress.
8. Sustainable development, able to maintain a constant pace.
9. Continuous attention to technical excellence and good design.
10. Simplicity—the art of maximizing the amount of work not done—is essential.
11. Best architectures, requirements, and designs emerge from self-organizing teams.
12. Regularly, the team reflects on how to become more effective, and adjusts accordingly.

### Scrum
This is a framework that can help teams build complex products
It is framework, not a methodology.
It is abstract and not prescriptive.
1995

Has only 3 team roles, 5 events, and 3 artifacts

Team roles:
   * Product Owner - Defines what will be build(done) and in what order
   * Team Member - Recommended Development Team size is 3-5 people. Team member with Multiple skills is generally
                   preferable to the specialized.
                   There are no managers or team leads - it is a flat hierarchy.
   * Scrum Master - Coach all team members to effectively apply Scrum. Is a management role, but is considered 
                   a servant leader and not a top-down manager.

Scrum Sprints
   * Sprint goal is the high-level goal of each time-boxed sprint written as concisely as possible
   * The development team then plans how to convert the goal items into a product increment
   * The sprint backlog is a subset of the product backlog and contains items selected for the sprint, plus additional 
     items for the development team

Scrum is based on TIA:
* Transparency
* Inspection
* Adaptation

Scrum Values:
* Focus - time-boxed events facilitate focused work
* Respect - 
* Openness
* Courage - continuous inspection and adaptation of work requires a degree of courage
* Commitment - Scrum requires a commitment to agile principles to be successful

Scrum Events:
* Sprint
* Sprint planning
* Daily scrum
* Sprint review
* Sprint retrospective

Scrum artifacts:
* Product Backlog
* Sprint Backlog
* Product Increment

Common Myths:
* FALSE: Daily Scrum is a status meeting
* FALSE: Using agile software tools makes your team agile
* FALSE: Agile teams do not document
* FALSE: Agile teams doesn't do design
* FALSE: Sprint reviews are product demos

### Agile Software Engineering Techniques

###### Extreme programming(XP)
Extreme programming (XP) is a software development methodology intended to improve software quality and responsiveness to changing customer requirements. As a type of agile software development,[1][2][3] it advocates frequent releases in short development cycles, intended to improve productivity and introduce checkpoints at which new customer requirements can be adopted.

Other elements of extreme programming include: programming in pairs or doing extensive code review, unit testing of all code, not programming features until they are actually needed, a flat management structure, code simplicity and clarity, expecting changes in the customer's requirements as time passes and the problem is better understood, and frequent communication with the customer and among programmers.[2][3][4] The methodology takes its name from the idea that the beneficial elements of traditional software engineering practices are taken to "extreme" levels. As an example, code reviews are considered a beneficial practice; taken to the extreme, code can be reviewed continuously (i.e. the practice of pair programming).

It uses weekly iterations
Also there is Quarterly Cycle
XP execution:
* XP teams do test-first development
* XP teams do incremental design
* XP practice include a quick build process of 10 minutes or less
* XP teams use pair programming
  * Switch roles periodically
  * It provides constant PR review
  * Facilitates knowledge sharing
  * I-Shaped (people)
    * Deep knowledge
    * Narrow area of skills
  * T-Shaped
    * Deep narrow knowledge
    * Also has knowledge of wider skills
* XP teams use continues integration

User Stories
* Template `As a <role> I can <capability>, so that <receive benefit>`
* The 3 Cs
  * Card - User Story text
  * Conversation
  * Confirmation - the steps of verifying that the Story meets conditions of satisfaction

Epic and Themes
* Epic - Business workflow or process that is too lage to be estimated
* Themes - Themes are attributes of user stories.

Agile Estimation
* Provided by team members, not by managers.
* Types
  * Absolute Units (by time)
  * Relative Estimation (estimate regarding by other task estimation)
* Scale
  * Fibonacci Scale - 0,1,2,3,5,8,13
  * Exponential Scale - 0,1,2,4,8,16
  * 0 - Already done or easily completed
  * XS> S > M > L > XL

Planning poker - estimation done by teammembers by showing cards with numbers(3,5,8 etc.)
Discuss and then vote again

DevOps - Culture of close cooperation between developers and QA teams (Dev) and IT operations teams (Ops)

###### Agile Reporting
Burndown charts
Burnup charts
Cumulative flow diagrams

### Kanban for Developers
Kanban is from Lean
Lean was invented for convair  
Little's Law for Software Development
`Work in Progress(L) = Completion Rate (Lambda) * Cycle Time (W)`
Cycle Time - Analysis, Design, Implementation, Deployment

###### Kanban Board
Kanban = Kan(Visual) + Ban(Card)

###### Limiting WIP
* Humans are not productive at task switching like computers
* Too many work items causes distractions and lowers productivity

###### How to Set WIP limits
* Kanban teams can set WIP limits to the number of team members plus a buffer
* WIP = Team members(6) + 50% Buffer(3) = Team members + Buffer (9)
* Doing and Done 
  * Completion criteria defined for each step
  * Work item must meet completion criteria before moving from Doing column to Done column
  * Process enforces stricter quality criteria
* Kanban Daily Standap
  * Focused on indentifyiing and addressing bottlenecks
  * Efficiency is the priority
  * All status updates visible on Kanban board

###### Kanban vs. Scrum
* Scrum is a framework, Kanban is a process management tool
* Kanban is more lightweight than Scrum
* Kanban can be combined with Scrum (Scrumban) but each can also be used independantly 
* Kanban
  * Developer-friendly and simple process
  * No mandatory time-boxed events
  * One product backlog
  * Daily standup focused only on bottlenecks
  * Manage work-in-progress(WIP) and continuously improve 

### Scaling Agile
* Why Scale Agile?
  * One product with too many features to be developed in a specific timeframe
  * One team cannot feasibly produce large amounts of features
  * Business case to ship those features to market in a specific timeframe compels organization to scale
* Rules of Scaling
  * Don't scale
  * Scale lowly: Continuously identify and address challenges and minimize dependencies (between teams)
  * Develop architectural standards and guidelines before scaling

#### Scaling frameworks
* Nexus 
  * Essentially Scrum with one additional artifact, a few additional events, and one additional team role
  * Principles of Scrum also apply to Nexus
  * Execution is like running multiple Scrum teams in parallel that produce one integrated product increment at the end of sprint
* Scrum@Scale
  * Scrum of Scrums
* LeSS
  * More prescriptive
  * Framework designed to work with two to eight teams and one product owner, with one Scrum master per one to three teams
  * Introduces the overall retrospective, an event that occurs after the sprint retrospective
  * LeSS Huge for more than 8 teams (new role: area product owner)
* Scaled Agile Framework (SAFe)
  * Works at multiple levels; the base levels required for SAFe implementation are called program amd team
  * Combination of levels form the configurations Essential SAFe, Full SAFe, Large Solution SAFe, and Portfolio SAFe
  * Smallest team unit is similar to a typical agile team
  * Multiple teams work in parallel at the team level
  * Work from all agile teams combined to produce product increment at the program level






### Questions
1. Why is software development risky in Agile?
   1. Because change is welcomed in Agile, development is risky because more issues can arise.
2. How do Agile stakeholders regard change?
   1. Agile developers welcome change and work with the customer.
3. Why are self-organizing teams better in an Agile approach?
   1. Self-organizing teams have a better understanding of what needs to get done because they are directly involved in the process. 
4. What is a self-organized team? 
   1. A team that knows how to do their work without help from outside.
5. Consider this quote: "Simplicity--the art of maximizing the amount
   of work not done--is essential." What does this quote mean?
   1. Agile Teams work on features that are really needed. Nothing more. Nothing less. The other options are incorrect explanations of this agile principle.
6. After an iteration is made, what is the first stage of the next iteration?
   1. After an iteration, a new set of requirements is defined. 
7. Why is frequent customer feedback necessary in Agile development? 
   1. It is a best practice to provide the feedback early, and make changes prior to implementing the system into production.
#### Scrum
8. How is the scrum master role different than the top management role? 
   1. They are servants to the project, and should be advocates of the scrum and Agile approach.
9. Why is the Sprint review important as a scrum event? 
   1. The team can discuss the status of the scrum, and then make changes as necessary.
10. What are 3 pillars of Scrum?
    1. transparency, inspection, and adaptation
11. What are three components within the product backlog?
    1. requirements, user stories, and enhancements. (Product backlogs are the to-dos for the project, and contain many components that outline what needs to get done.)
12. Why is the product implement important? 
    1. It represents the completed deliverables, and should have some business value. 
13. What are some of the product owner's key responsibilities? 
    1. They determine what is defined and in what order.
14. When does the product owner work the most with the development team?
    1. during sprint planning - Goals should be defined during a sprint, and the product owner will primarily handle this task. 
15. How is the development team organized in scrum? 
    1. Self-organized
16. Which skills should members of the development team possess?
    1. multiple IT skills - The development team should have multiple IT skills in order to view different tasks in different ways.
17. How is focus one of the important values of scrum? 
    1. There are specific deliverables for certain durations of time. - Small deliverables are usually made within a two-week timeframe, and should be met in the designated durations of time.
18. What is a Daily Scrum?
    1. An opportunity for the Development Team to synchronize their work.
19.  When is the sole use of Agile tools inefficient within the scrum? 
    1. when the stakeholders lack the adoption of Agile. - All stakeholders need to adopt the Agile methodology in order for it to succeed.
#### Agile Software Engineering Techniques
20. How should a widening gap between the completed work and total scope be interpreted in a Burn Up Chart?
    1. There is too much work, and it will probably be unachievable before the sprint completes. 
21. What is the first part of a user story? 
    1. The first part of a user story should include who will benefit from this story.
22. Under what condition might an epic exist? 
    1. when there are too many conditions or user stories
23. How is the Fibonacci Scale used in Agile estimation? 
    1. It is used to rank the difficulty and scope of backlogged product deliverables. 
24. When is planning poker appropriate? 
    1. when estimating user stories - Planning poker is a method that involves all stakeholders coming to a consensus, where each suggests a result and presents it to the team.
25. How does test-driven development expose poorly designed monolithic code?
    1. If the code is too large, it is difficult to develop specific tests. - If the development team is struggling to define the test, then the code might need to be broken down to work with it.
26. There are three categories within the user stories. What is the purpose of the final category? 
    1. It shows the end results or reason why the user story exists. - The final category defines what needs to get done for the user story.
27. Why is pair programming an important part of Extreme Programming (XP)? 
    1. It enables new perspectives by having the coder and monitor switch roles. - By having the roles of coder and monitor switched, there can be fresh, new viewpoints.
28. How are customers integrated within Extreme Programming (XP)?
    1. Customers are included within the project. - One notable aspect of Extreme Programming is that customers are always included.
29. What is the first phase of XP execution?
    1. Tests are written. - Tests are done prior to the XP execution in order to determine what are valid and invalid results.
#### Kanban
30. Which manufacturing company originally applied lean history? 
    1. Toyota, with the manufacturing of automobiles.
31. What does a well-designed Kanban Board communicate?
    1. the status of work-in-progress items
    2. the number of work-in-progress items.
    3. the workflow steps that are closed to being overloaded
32. How do you set the WIP limits?
    1. find the slowest step - The first limit will be the slowest step or least duration needed to complete that task.
33. What is one similarity between Kanban and scrum? 
    1. Both scrum and Kanban are used within the Agile process.
34. What is a difference between scrum and Kanban?
    1. Scrum is a framework, while Kanban is a process management tool. - `Scrum is a methodology, while Kanban contains a tool to list project backlogs and how they are to be completed.` 
35. What is the first step in the Kanban board? 
    1. planning coordination - `The Kanban board is a visual tool that allows users to drag items from the product backlog to the planning coordination stage.`
#### Scaling Agile
36. Are There ways to scale the output of an agile effort without adding more teams?
    1. The output of an agile team can be scaled by improving skills, optimizing the delivery pipeline, adding automation etc. There are limits to how much a team can scale but that should be the first resort before attempting to add additional teams.
37. TRUE/FALSE: Adding more teams to an agile development effort will most likely slow down the existing teams for some time.
    1. TRUE: New Teams will need help from existing teams to become productive. This will reduce the time available for the existing teams to do their work. The same effect is observed when adding new members to a team.
38. How does Scrum@Scale differ from standard scrum?
    1. Scrum@Scale can be scaled infinitely. - `Using Scrum@Scale, there could be multiple scrums and subsets that all feed into each other.`
39. How does the Scaled Agile Framework (SAFe) differ from scrum?
    1. SAFe works at multiple levels. - `SAFe operates at all the levels, including the program and team.`




