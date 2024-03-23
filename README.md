Report: Addressing SOLID Principles in Software Development
Introduction
The SOLID principles are fundamental principles of object-oriented design aimed at creating robust, maintainable, and scalable software systems. In this report, we explore the application of three out of the five SOLID principles in a software development project. The principles covered include:

Single Responsibility Principle (SRP)
Open/Closed Principle (OCP)
Liskov Substitution Principle (LSP)
For each principle, we demonstrate both the violation and adherence to the principle through code examples and explanations. Additionally, a use case scenario is provided to illustrate the practical application of these principles.

Use Case Scenario
For our project, we consider a library management system where users can borrow and return books. The system consists of various modules for managing users, books, borrowing transactions, and notifications.

Single Responsibility Principle (SRP)
Violation:
In the Violated folder, we have a User class that violates the SRP. This class is responsible for both managing user data (name, email) and sending email notifications. This violates the SRP by combining two distinct responsibilities into a single class.

Solution:
To adhere to the SRP, we introduce an EmailSender class in the Solved folder. The User class now focuses solely on managing user data, while the EmailSender class is responsible for sending email notifications. This separation of concerns ensures better maintainability and flexibility in our system.

Open/Closed Principle (OCP)
Violation:
In the Violated folder, the Shape class demonstrates a violation of the OCP. This class contains a method calculateArea() that calculates the area of different shapes (e.g., rectangles and circles) using conditional statements. Any modification or extension to support new shapes would require modifying the existing class, violating the principle of being open for extension but closed for modification.

Solution:
To adhere to the OCP, we introduce an Shape interface and separate concrete implementations for each shape (e.g., Rectangle and Circle) in the Solved folder. This allows for adding new shapes without modifying existing code, thereby preserving the class's closed nature while being open for extension through new implementations.

Liskov Substitution Principle (LSP)
Violation:
In the Violated folder, the Square class violates the LSP. Despite inheriting from the Rectangle class, it overrides the setWidth() and setHeight() methods to set both dimensions to the same value, breaking the expected behavior of the superclass.

Solution:
To adhere to the LSP, we ensure that the Square class does not inherit from Rectangle. Instead, both Rectangle and Square classes implement the Shape interface. This allows each class to maintain its specific behavior without violating the LSP, ensuring substitutability of objects of derived classes for objects of their base classes.

Conclusion
In conclusion, adhering to the SOLID principles leads to more modular, flexible, and maintainable software systems. By identifying violations and applying appropriate solutions, we can improve the design quality of our codebase. Through this assignment, we gained practical experience in applying the SRP, OCP, and LSP principles to a real-world software development project.
