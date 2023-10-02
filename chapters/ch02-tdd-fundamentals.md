## Chapter 2: TDD Fundamentals <a id="ch02-tdd-fundamentals"></a>
<link rel="stylesheet" type-"text/css" href="styles.css">
### TDD and BDD - What's the Difference

**Test-Driven Development (TDD)** and **Behavior-Driven Development (BDD)** are two software development methodologies that focus on writing tests before or alongside writing code. The aim is to improve code quality, maintainability, and to ensure that the software meets its requirements. There are a couple key differences.

In TDD, the developer writes tests before writing the actual code (implementation) for a feature or functionality. This describes the commonly used **Red-Green-Refactor Cycle** process.

![The Red-Green-Refactor Cycle by [Nat Pryce](http://www.natpryce.com/articles.html)](/images/red-green-refactor.jpg "Red-Green-Refactor Cycle")

1. The developer writes a **failing test** that defines the desired behavior of a new feature or function according to the project requirements. This test will initially fail, indicated by the <span class="red-text">red phase</span>.
2. The developer writes the **minimal code required** to make the test pass which makes the test state <span class="green-text">green</span>. The code is likely not fully functional or optimized at this point.
3. Once the test passes, the developer **refactors** the code to improve its design and maintainability while ensuring that all tests still pass. This is discussed further in the next section.

TDD is often combined with unit testing, where individual components or functions are tested in isolation. This helps ensure that each piece of code behaves as intended and remains functional as the project evolves.

BDD is an extension of TDD that shifts the focus from just writing tests to describing the expected behavior of the software in a more human-readable format. BDD is often used to align development with business requirements and facilitate collaboration between developers, testers, and other non-technical stakeholders. BDD is a recent innovation that forms a superset of TDD.

In BDD, one works with **scenarios** written in a plain language format that describes the behavior of the software from the user's perspective. Scenarios are often written in a format known as **Given-When-Then**:

1. **Given:** Describes the initial context or setup.
2. **When:** Describes the action or event being tested.
3. **Then:** Describes the expected outcome or behavior.

BDD tools can then automatically generate tests from these scenarios, which makes it easier to communicate and educate teams on the desired behavior.

In summary, TDD focuses on writing tests for specific code units (usually functions or methods) to ensure their correctness.

BDD focuses on describing the expected behavior of the software from a user's perspective using plain language scenarios, fostering collaboration and understanding between stakeholders.

TDD and BDD have different focuses but are complementary practices. BDD scenarios provide a higher-level perspective on system behavior, whereas TDD is used to implement and validate the lower-level components that make up that behavior. Both methodologies contribute to producing well-tested and well-understood software.

## Refactoring: Enhance Code Confidently

**Refactoring** code is the practice of changing the structure of the software without changing the functionality. This idea of changing the software is scary, especially to management of risk averse companies. How can a developer do this correctly without breaking the critical functionality?

This critical functionality must be clearly defined and tests must be implemented. These tests should be run regularly and automated as much as possible. Once the team has these automated tests in place and running consistently, developers can make changes and check that the functionality remains correct with confidence.

#### How can refactoring improve code?
- **Extract** a commonly used hard-coded value like a number or string to a **constant**. This helps clean up code by storing the value in a common place that is referenced as needed.
- Extract a commonly used modifiable value to a **variable**.
- Extract an area of functionality that is or will be commonly used into a **function, method, or class**. This helps encapsulate the functionality in a module that can be reused in the future and that the developers have better access control of than copypasta.

How does one refactor code? The most basic way is to bust out the cut and paste feature in your favorite text editor, but most **interactive development environments (IDEs)** like Visual Studio and Eclipse have built in functionality specifically for this. AI tools like GitHub Copilot and AWS CodeWhisperer can also assist with this.

&copy; Kaldun Technologies 2023
