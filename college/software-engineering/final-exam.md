# CPSC:480 Software Engineering Final Exam Notes
### Peyton Gardner
### 12/5/2024

* Types of testing
    1. **Black Box**
        * **Viewpoint:** Tester (or user).
        * **Focus:** Functionality of the software
        * **What it tests:** The tester is concerned with whether the software
        behaves as expected, focusing on input-output behavior without
        considering the internal code or logic. It checks the software's overall
        functionality, usability, ,and adherence to specifications. 

    2. **White Box** 
        * **Viewpoint:** Developer (internal perspective)
        * **Focus:** Internal logic and structure of the appliation
        * **What it tests:** The tester has access to the source code and tests
          the software at the code level. This involves examining the program's
          flow, logic, and internal workings to identify bugs in specific
          components (e.g., code coverage, branch testing, path testing).

    3. **Grey Box** 
        * **Viewpoint:** Combination of tester and developer
        * **Focus:** Both the functionality and the internal workings of the
          application
        * **What it tests: The test has partial knowledge of the internal
          structures (such as the system architecture or database design) but is
          primarily focused on how th esytem functions from the users
          perspective. Grey box testing often uses system architecture and
          documentation to focus on areas like security vulnerabilities, API
          calls, or authentication mechanisms

* Test-Driven Development (TDD)
A software development methodology where tests are written before the actual
code to ensure the system behaves as expected. It helps improve the design of
the code, enhances maintainability, and reduces bugs.

Process:  
    1. Write a test (Red):
       Write a test the describes a small unit of behavior you want to
       implement. The test should initially fail. This confirms the test is
       valid and the feature has not yet been implemented.
    
    2. Write the code to pass the test (Green):
       Write just enough code to make the test pass. It doesn't have to be
       pretty.

    3. Refactor (clean up):  
        Refactor the code to imporve its structure, readability, or efficiency,
        while keeping the test passing. Clean up the code.

    4. Continue these steps to add features to the software.  

Principles:  
    You refactor and "clean up" your code during each test. There is not a big
    "clean up" stage at the end. You do it as you develop. TDD gives you
    confidence with code changes. It ensures the functionality doesn't change.

* SE Code of Ethics (in order)
    1. Public
    2. Client and Employer
    3. Product
    4. Judgement
    5. Management
    6. Profession
    7. Colleagues
    8. Self

