---
layout: default
title: "ePortfolio"
---

# Welcome to My CS499 ePortfolio {#top}

Thank you for visiting my ePortfolio! This site showcases my final project for the Computer Science Capstone at SNHU, including:

- My professional self-assessment
- The original project artifacts comprising the MEAN stack Travlr Trip Listings application from CS465
- A code review video, submitted as Milestone One in this course
- Three enhancements to the Travlr Trip Listings project (Milestones Two, Three, and Four)
- Narratives explaining each enhancement and its alignment with program outcomes

> 🔒 For security and academic integrity reasons, the project repository is private. If you're a reviewer or instructor, please [request access](https://github.com/joselgarza/cs465-fullstack) via GitHub or contact me directly [here](mailto:jose.garza4@snhu.edu).

---

### 🔗 Quick Navigation

- [Professional Self-Assessment](#self-assessment)
- [Travlr Trip Listings: Original Project](#original)
- [Code Review Video](#code-review)
- [Enhancement One](#enhancement-one)
- [Enhancement Two](#enhancement-two)
- [Enhancement Three](#enhancement-three)

---

## 🧠 Building Secure, Scalable Solutions: My Self-Assessment {#self-assessment}

Over the course of the Computer Science program at SNHU, I’ve evolved from a novice developer into a strategic, security-focused engineer who builds narratable, modular, and professionally aligned applications. This ePortfolio reflects that transformation, showcasing the broader skills, values, and experiences I’ve cultivated throughout the program. Through my years at SNHU, various assignments and projects challenged me to think critically about software architecture, security, and user experience.

Courses in software engineering, algorithms, databases, and cybersecurity laid the foundation for my technical depth, while the capstone project helped me synthesize those lessons into a cohesive, real-world application. For example, the CS-405 Secure Coding course bolstered me as a developer to think beyond functionality and to protect users, applications, and data through integrating secure practices at all possible points in the Software Development Lifecycle. An instance of this was protecting an application against buffer overflow due to a lack of user input validation, allowing for more characters to exceed the user input array’s limit. To prevent this, we checked input length, rejected oversized entries, cleared the input stream, and prompted the user to retry with fewer than 20 characters as follows:

```cpp
char user_input[20];

// Previously, the code allowed for unsafe input like this:
// std::cout << "Enter a value: ";
// std::cin >> user_input;

// Use getline to read input and prevent buffer overflow
while (true) {
    std::cout << "Enter a value (max 19 characters): ";
    std::cin.getline(user_input, sizeof(user_input));

    // Check if input was too long
    if (std::cin.fail()) {
        std::cin.clear(); // Clear error state
        std::cin.ignore(std::numeric_limits<std::streamsize>::max(), '\n'); // Flush overflow

        std::cerr << "Input too long! Please enter fewer than 20 characters.\n";
    } else {
        break; // Valid input
    }
}

std::cout << "You entered: " << user_input << std::endl;
```
This experience taught me to anticipate edge cases and design defensively, which is a mindset I now apply across all projects.

Another great skill I developed during my academic career at SNHU is debugging code effectively to identify issues. One memorable time was while developing a pedometer mobile application in the Android Studio using SensorManager. To watch the application in more detail, I enabled breakpoints in the code and ran the application in debug mode.  Stepping through each breakpoint showed each update to variables based on the movement detected by the sensor:

![Debugging Java code in Android Studio](images/debug.png)

Debugging in Android Studio sharpened my ability to trace sensor-driven logic and isolate variable state changes, a skill I’ve carried into more complex systems.

## 🤝 Development, Collaboration, and Communication

While much of my development work was independent, I collaborated with peers through code reviews, discussion forums, and shared repositories such as GitHub. I practiced asynchronous teamwork by resolving merge conflicts, aligning shared goals, and giving constructive feedback. These experiences sharpened my ability to work in a team environment and adapt to different communication styles.
The following areas showcase application of my skills:

## 🧩 Core Competencies

- **Team Collaboration**  
  Throughout my tenure at SNHU as well as my professional experience, I have led and been member of small and large teams, fostering cross-functional team collaboration, fielding various communication styles, and supporting both direct and indirect efforts to achieve overall team impact. To support my efforts in this regard, I have experience using Visual Studio, Azure DevOps for story boards and code lifecycle management, GitHub, Microsoft Teams, SharePoint, and more. I value honesty, transparency, and direct language in collaborative situations.

- **Stakeholder Communication**  
  I enjoy championing projects and their requirements, objectives, milestones, and completion to both technical and non-technical audiences. Be it live presentations to leaders, training to users, or technical documentation, my aim is to always ensure that technical designs and solutions are easily understood to all audiences.

- **Data Structures & Algorithms**  
  I apply core structures such as arrays, lists, stacks, and hash maps as needed to solve problems effectively. I’ve implemented recursive and iterative algorithms for sorting, searching, and traversal. Additionally, I evaluate how fast an algorithm runs (time complexity: e.g. linear O(n) vs. quadratic O(n²)) and how much memory it uses (space complexity: e.g. storing extra arrays, recursion stack depth) before choosing or implementing a solution. This helps me pick the most efficient and scalable approach, especially when handling large datasets, nested loops, or recursive functions. I balance algorithmic challenges between performance with maintainability.

- **Software Engineering & Database**  
  I design modern solutions using cloud and serverless architectures. I prioritize principles such as separation of concerns, clear comments and documentation, and debug/test tools and practices. I normalize database schemas, enforce validation rules, and optimize queries through indexing and thoughtful data modeling. I am comfortable with traditional relational on-premises database engines such as Microsoft SQL and Oracle, cloud NoSQL databases such as MongoDB, or serverless varieties such as Cosmos DB and DynamoDB.

- **Security**  
  I embed secure coding practices across all layers of development. This includes input sanitization, role-based access control, authentication and authorization, and schema enforcement. I’m familiar with threat modeling, OWASP guidelines, and cloud-based IAM policies. Protecting applications, data, and users are pinnacle concerns during the development process.

While I’ve gained a wide range of skills, the best demonstration of my technical and strategic growth is captured in my capstone project: Enhancements to the MEAN stack Travlr Trip Listings app.

## 🧵 Capstone Artifact Summary and Portfolio Summary

The following code review and artifacts in this portfolio form a cohesive narrative of my growth. Each enhancement builds on the last:

- RBAC roles using route guards and service-level authorization checks  
- Reactive form validation  
- API modularity  
- Search with fuzzy matching, compound indexing, and partial matching  
- Input sanitizing  
- Schema validation

Together, they demonstrate my ability to develop and improve complex systems, prioritizing security and user experience. My desire is to deliver similar best practice solutions and create real-world impact. Each artifact on display is linked to a GitHub repository, organized by enhancement branches, with structured content for reviewer clarity.

[⬆️ Back to Top](#top)

---

## Original Artifact: Travlr Project (CS465) {#original}

This is the original version of the Travlr MEAN stack application, created during CS 465: Full-Stack Development I (July - August 2025) before any enhancements were applied.

The artifact began as an Express server-rendered HTML/Handlebars implementation and was later refactored into a modular Angular Single Page Application (SPA) later in the class. This refactoring allowed me to apply Separation of Concerns (SoC), improve maintainability, and align with modern front-end architecture standards.  

🔗 <a href="https://github.com/joselgarza/cs465-fullstack/tree/main" target="_blank">View Original Project (Main Branch)</a>

[⬆️ Back to Top](#top)

---

## Code Review Video {#code-review}

<iframe width="560" height="315" src="https://www.youtube.com/embed/OFDothTvoj4" title="Travlr Project Code Review" frameborder="0" allowfullscreen></iframe>

[⬆️ Back to Top](#top)

---

## Enhancement One: Software Design & Engineering {#enhancement-one}

This enhancement focused on modularizing the Angular frontend, implementing route guards, and adopting standalone architecture.

🔗 <a href="https://github.com/joselgarza/cs465-fullstack/tree/enhancement-one" target="_blank">View Enhancement One Branch</a>

[⬆️ Back to Top](#top)

---

## Enhancement Two: Algorithms & Data Structures {#enhancement-two}

This enhancement restored backend search functionality, refined regex validation, and handled edge cases.

🔗 <a href="https://github.com/joselgarza/cs465-fullstack/tree/enhancement-two" target="_blank">View Enhancement Two Branch</a>

[⬆️ Back to Top](#top)

---

## Enhancement Three: Databases {#enhancement-three}

This enhancement added compound indexing, normalized schema inputs, and improved validation logic.

🔗 <a href="https://github.com/joselgarza/cs465-fullstack/tree/enhancement-three" target="_blank">View Enhancement Three Branch</a>

[⬆️ Back to Top](#top)
