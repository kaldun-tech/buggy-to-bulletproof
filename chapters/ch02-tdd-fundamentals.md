## Chapter 2: TDD Fundamentals {#ch02-tdd-fundamentals}

### TDD and BDD - What's the Difference

**Test-Driven Development (TDD)** and **Behavior-Driven Development (BDD)** are two software development methodologies that focus on writing tests before or alongside writing code. The aim is to improve code quality, maintainability, and to ensure that the software meets its requirements. There are a couple key differences.

In TDD, the developer writes tests before writing the actual code (implementation) for a feature or functionality. This describes the commonly used **Red-Green-Refactor Cycle** process.

![The Red-Green-Refactor Cycle by <a href="http://www.natpryce.com/articles.html">Nat Pryce</a>](/images/red-green-refactor.jpg "Red-Green-Refactor Cycle")

1. The developer writes a **failing test** that defines the desired behavior of a new feature or function according to the project requirements. This test will initially fail, indicated by the <color='red'>red phase</color>.
2. The developer writes the **minimal code required** to make the test pass which makes the test state <color='green'>green</color>. The code is likely not fully functional or optimized at this point.
3. Once the test passes, the developer **refactors** the code to improve its design and maintainability while ensuring that all tests still pass. This is discussed further in the next section.

TDD is often combined with unit testing, where individual components or functions are tested in isolation. This helps ensure that each piece of code behaves as intended and remains functional as the project evolves.

BDD is an extension of TDD that shifts the focus from just writing tests to describing the expected behavior of the software in a more human-readable format. BDD is often used to align development with business requirements and facilitate collaboration between developers, testers, and other non-technical stakeholders. BDD is a recent innovation that forms a superset of TDD.

In BDD, one works with **scenarios** written in a plain language format that describes the behavior of the software from the user's perspective. Scenarios are often written in a format known as **Given-When-Then**:

1. **Given:** Describes the initial context or setup.
2. **When:** Describes the action or event being tested.
3. **Then:** Describes the expected outcome or behavior.