# Project Management System in Java
Application includes:
    • Inheritance
    • Polymorphism
    • Abstract Data Type
    • Collections
    • Mediator Pattern

### Exercise Details & Requirements:
The object and class diagram of the system is given in URL.png. 
Implement the system as given in the class diagram 
and to extend Resource class with Person superclass, which has Employee
and Consultant subclasses.

##### Also, implement a Project Management System class which should be your Mediator and is responsible of:
• Adding a project
• Finding and removing a project
• Finding and updating a project by
- Adding, removing and updating an activity
- Adding, removing and updating a task
- Adding, removing and updating a resource
- Assigning a resource to a task
- Unassigning a resource from a task
• Calculating project, activity, and task duration by hours
• Finding number of distinct employees and consultants assigned to a project, activity, and task

The user should be able to select commands from menu and enter data from command line to
manage projects and resources and display project and resource details. Projects should be stored in
a file named Projects-YYYY-MM-DD.txt. When program starts, the program should find latest file and
read project details to corresponding objects. When user exits, all project data should be saved to a
file. Make sure you have three-layer architecture implemented.