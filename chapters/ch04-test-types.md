## Chapter 4: Test Types {#ch04-test-types}

### What's with the Boxes?

![Gray-Box Testing](/images/red-green-refactor.jpg "Gray-Box Testing")

**White-box**, **clear-box**, and **black-box** testing are different approaches to testing software, each with its own focus and objectives. These testing methodologies help ensure the quality and reliability of software by identifying defects, vulnerabilities, and issues before the software is released.

**White-box testing**, also known as **clear-box** testing or **structural** testing, focuses on examining the internal structure and logic of the software's code. Testers with knowledge of the software's implementation details actively design test cases based on the code's logic, branches, paths, and conditions. This approach aims to ensure that all paths through the code are tested, leading to comprehensive coverage. Here are the key characteristics of white-box testing:
- Requires access to the source code.
- Tests the software's internal logic, code branches, and paths.
- Aims to achieve high code coverage.
- Helps uncover issues related to code correctness, missing functionalities, and security vulnerabilities.

**Black-box** testing is an approach where testers focus on the external behavior of the software without knowledge of its internal workings. Testers create test cases based on specifications, requirements, and input-output relationships to ensure that the software meets its functional and non-functional requirements. Here are the key characteristics of black-box testing:
- Does not require knowledge of the internal code structure.
- Tests the software's functionality, user interface, and interactions.
- Emphasizes testing from the user's perspective.
- Helps identify issues related to incorrect outputs, functional defects, and usability problems.

**Gray-box testing** is a combination of both white-box and black-box testing. Testers have partial knowledge of the internal workings of the software, allowing them to create test cases that target specific areas of the code without needing to know all implementation details. Here are the key characteristics of gray-box testing:
- Testers have limited knowledge of the internal code.
- Combines aspects of both white-box and black-box testing.
- Helps bridge the gap between structural testing and functional testing.
- Can be effective in uncovering defects that result from interactions between different parts of the software.
Each of these testing approaches offers unique advantages and is suitable for different testing scenarios. White-box testing is best for examining code logic, black-box testing is useful for ensuring software meets its specifications, and gray-box testing can be a practical compromise when some knowledge of the code is available but not exhaustive. Successful testing often involves a combination of these methodologies to achieve thorough coverage and ensure the software's reliability.

### The Testing Pyramid Keeps Our Mummies Beautiful

Mummies in the museum are intriguing yet incredibly gross. We need to keep the metaphorical mummy of our software quality safe and well kept inside a testing pyramid. This concept was popularized in the book ["Succeeding with Agile” by Mike Cohn](https://www.amazon.com/Succeeding-Agile-Software-Development-Using/dp/9332547963). The pyramid represents the distribution of different types of tests based on their scope, granularity, and quantity of tests at each level. It illustrates the ideal proportion of different types of tests for a well-balanced testing strategy.

![The Test Pyramid](/images/test-pyramid.jpg "Testing Pyramid")

The idea behind the testing pyramid is to emphasize a strong foundation of unit tests, followed by a moderate number of integration tests, and a smaller number of end-to-end tests. By adhering to the testing pyramid principles, development teams can build a comprehensive testing strategy that strikes a balance between coverage, speed, and reliability. This distribution helps achieve several benefits:
- **Faster Feedback:** Unit tests execute quickly and provide immediate feedback to developers. This allows them to catch and fix issues early in the development cycle.
- **Isolate Issues:** Unit tests isolate defects to specific components, making it easier to identify and fix problems.
- **Reduce Maintenance Costs:** Lower-level tests are generally more stable and easier to maintain than high-level end-to-end tests.
- **Faster Test Execution:** Relying primarily on unit tests makes the overall test suite run faster. This enables quicker continuous integration and deployment cycles.

The testing pyramid typically consists of three layers, each representing a different type of testing. At the _base_ of the pyramid are **unit tests**. These are small, focused tests that verify the correctness of individual components or units of code. Unit tests are designed to be fast, isolated, and have minimal dependencies. They help catch bugs early in the development process and provide a safety net for code changes. Unit tests form the largest portion of the testing pyramid. The development team should be active in building unit tests for their products.

The _middle_ layer of the pyramid consists of **integration tests**. These tests validate the interactions between different components, modules, or services within the system. Integration tests help ensure that the integrated parts of the software work correctly together. They focus on testing the interfaces and interactions between components.

**Service tests** are typically a subset of integration tests that focus on testing the interactions between different services or microservices in a distributed system. They ensure that the individual services communicate correctly, exchange data accurately, and function as expected when integrated together.

At the _top_ of the pyramid are **end-to-end (E2E) tests**, also known as **UI tests**. These tests simulate real user scenarios and cover the entire application stack, including the user interface, multiple components, databases, and external integrations. E2E tests provide confidence that the application functions as expected in a real-world environment. However, they tend to be slower, more complex to maintain, and may have higher execution times compared to lower-level tests. These tests are most pertinent to BDD and the UI/UX team.

### Useful Testing Tools

There are a massive variety of testing tools you can use to accomplish this. It’s easy to get lost in the deluge of information out there so here is a brief summary of some tools I see as quite useful.

For **C** and **C++** testing, **Google Test** and **Catch2** are quite popular. The Google Test framework requires the most up-to-date version of C++ whereas Catch2 is more backwards compatible but does not have as many features.

For **Java**, **JUnit** is a widely-used testing framework primarily for unit testing. **TestNG** supports both unit and integration testing. **Mockito** is a promising mocking framework that facilitates creating mock objects in unit tests. **Mocking** allows one to make a simple imitation of an object your code is dependent on to execute your tests.

**Jasmine** and **Cypress** are great BDD testing frameworks for **JavaScript**. JavaScript is very powerful for both web and mobile applications so these are very useful tools to have in your belt.

For **C#**, also known as Microsoft’s version of Java, **NUnit** is a widely-used testing framework for C# that supports various test attributes and runners similar to JUnit. xUnit.net is a more modern and extensible C# testing framework. **Moq** is a mocking framework for creating mock objects in unit tests for C# similar to Mockito.

For **Python**, **unittest** is the built-in testing framework for writing unit tests. **Pytest** is a popular testing framework for Python that offers advanced features and plugins. This was used in our organization to great effect!

&copy; Kaldun Technologies 2023
