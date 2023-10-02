## Chapter 3: Requirements <a id="ch03-requirements"></a>

### Understand Your Requirements
**Software requirements** describe the features, functionalities, constraints, and qualities that a software system should possess. These different types of requirements help define the scope of the project and guide development. Security and privacy are critical aspects of software development, and various types of requirements can directly affect them. Notice that requirements often use the word _shall_, indicating that the software must consistently support the enumerated feature. These are some of the most important types of requirements:

**Functional requirements** define the specific features, capabilities, and interactions that the software should have. These requirements can directly impact security and privacy by specifying how data is processed, stored, and transmitted. For example, if the software handles user authentication, a functional requirement might read that passwords shall be stored securely using encryption and hashing techniques to protect user data.

**Security requirements** explicitly focus on safeguarding the software and its data from unauthorized access, attacks, and vulnerabilities. These requirements can include specifying encryption protocols, access control mechanisms, user authentication methods, audit trails, and more. Security requirements directly affect the overall security posture of the software and help prevent data breaches and unauthorized access.

**Privacy requirements** aim to protect users' personal information and ensure that the software complies with relevant privacy regulations. These requirements dictate how user data is collected, processed, stored, and shared. For example, privacy requirements might mandate that _user consent_ must be obtained for data collection, allow users to delete their data, and ensure that _sensitive information_ is anonymized or pseudonymized.

**Non-functional requirements** encompass qualities like _performance, scalability, reliability, and usability_. Security and privacy considerations can be part of these requirements. For instance, a non-functional requirement might specify that the software should handle a certain number of concurrent users securely without compromising performance. This should describe appropriate performance metrics given standard user configuration.

**Regulatory requirements**, such as industry standards or legal mandates, can have a significant impact on security and privacy. Software must comply with these regulations, which often include specific security and privacy measures to be implemented. Three critical regulations in the software industry include:
- General Data Protection Regulation (GDPR) in the EU
- Health Insurance Portability and Accountability (HIPAA) in the US
- Federal Energy Regulatory Commission (FERC) in the US energy industry

**Usability requirements** focus on making the software user-friendly and efficient. These requirements indirectly impact security and privacy by influencing user behavior. If security measures are overly complex, users might resort to insecure workarounds, potentially compromising security and privacy. User interface and experience (UI/UX) professionals are very insightful in the process of drafting and implementing such requirements.

**Performance requirements** dictate how the software should perform under various conditions. Security mechanisms like encryption and authentication can introduce processing overhead. Performance requirements should ensure that security measures do not significantly degrade system performance, as slow responses might discourage users from using secure methods. Understanding _software profiling_ is an important skill in assessing performance requirements.

**Availability and reliability** requirements ensure that the software is accessible and functions as expected. Security incidents can lead to system downtime or data breaches, impacting both availability and reliability. Your organization’s _operations_ and _support_ professionals are key stakeholders to discuss these requirements with.

&copy; Kaldun Technologies 2023
