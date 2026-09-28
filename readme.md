# 👨‍💼 Employee Management System

A simple, menu-driven Employee Management System built with Python OOP, demonstrating classes, inheritance, constructors, objects, methods, and lists.

🎯 Project Overview

This project is a beginner-friendly Python application that demonstrates how Object-Oriented Programming (OOP) can be used to create an Employee Management System.

The system allows users to create and manage three types of objects:

👤 Person

👨‍💼 Employee

🧑‍💼 Manager

The project uses inheritance to establish a relationship between these classes:

Person
  │
  └── Employee
        │
        └── Manager

🎥 Video Explanation
▶️ Watch the Complete Project Explanation

📌 Video: [YOUR_VIDEO_LINK_HERE](https://drive.google.com/file/d/1tjpvy7VM38SruJe3m_eNYGUFhVglb55G/view?usp=drivesdk)

The video explains:

🐍 Python OOP concepts used in the project

🏗️ Class and object creation

🧬 Inheritance

🔧 Constructors

📦 Lists for storing objects

🖥️ Menu-driven program

🔍 Searching and displaying details

▶️ How the complete program works

✨ Features
Feature Description
👤 Create Person Add a new person with GR number, name, and age
👨‍💼 Create Employee Add employee information including ID and salary
🧑‍💼 Create Manager Add manager information including department
📋 Show Details Display information for Person, Employee, or Manager
🧬 Inheritance Uses multi-level inheritance
💾 Object Storage Stores created objects in Python lists
🖥️ Menu Driven Easy-to-use command-line interface
🚪 Exit Safely exit the application
🧠 OOP Concepts Used

1. 📦 Class

The project contains three classes:

class Person:
    ...
class Employee(Person):
    ...
class Manager(Employee):
    ...

🧬 Inheritance

The project demonstrates multi-level inheritance.

Person
   ↓
Employee
   ↓
Manager

Employee inherits from Person, while Manager inherits from Employee.

This allows the child classes to reuse properties and functionality from their parent classes.

🔧 Constructor

Each class uses the __init__() constructor to initialize object attributes.

Example:

def __init__(self, grno, name, age):
    self.geno = grno
    self.name = name
    self.age = age

   🔗 super()

The super() function is used to call the constructor of the parent class.

Example:

super().__init__(grno, name, age)

This avoids rewriting the same initialization code in the child classes.

   🧱 Objects
Objects are created from the classes:

Per = Person(grno, name, age)
Emp = Employee(grno, name, age, employee_id, salary)
Man = Manager(grno, name, age, employee_id, salary, department)

1. 📋 Lists
The program uses lists to store the created objects:

per = []
emp = []
man = []

Objects are then added using:

per.append(Per)
emp.append(Emp)
man.append(Man)

🏗️ Class Structure
👤 Person

The Person class contains:

GR Number

Name

Age

show_details() method

class Person:
    def __init__(self, grno, name, age):
        self.geno = grno
        self.name = name
        self.age = age

    def show_details(self):
        print(f"person created with name : {self.name}")
        print(f"and age: {self.age}")

👨‍💼 Employee

Employee inherits from Person and adds:

Employee ID

Salary

class Employee(Person):

It also contains:

def details(self):

for displaying employee information.

🧑‍💼 Manager

Manager inherits from Employee and adds:

Department

class Manager(Employee):

This creates a multi-level inheritance hierarchy.

📊 Program Flow
                ┌───────────────┐
                │     START     │
                └───────┬───────┘
                        ↓
             ┌────────────────────┐
             │ Display Main Menu  │
             └─────────┬──────────┘
                       ↓
          ┌────────────┴─────────────┐
          │                          │
          ↓                          ↓
   Create Person              Create Employee
          │                          │
          ↓                          ↓
    Store Object              Store Object
          │                          │
          └────────────┬─────────────┘
                       ↓
                Create Manager
                       │
                       ↓
                 Store Object
                       │
                       ↓
                 Show Details
                       │
                       ↓
                  Exit Program

🖥️ Main Menu

When the program starts, the user sees:

--- python oop Project: employee management system ---

choose an operation

1. create a person
2. create a employee
3. create a manager
4. show detail
5. exit

The user can select an operation by entering a number.

💻 Example
Creating a Manager
enter your choice: 3

enter your gr no: 101
enter your name: Rahul
enter your age: 28
enter employee id: 5001
enter employee salary: 50000
enter your department: IT

Output:

employee created with name: Rahul
age: 28, ID: 5001
and salary: 50000
and department: IT

🛠️ Technologies Used

🐍 Python 3

🧱 Object-Oriented Programming

📦 Python Lists

🔀 match-case

⌨️ Command Line Interface

📁 Project Structure
employee-management-system/
│
├── employee_management.py
│
└── README.md

🚀 How to Run
1️⃣ Install Python

Make sure Python 3 is installed on your computer.

Check your Python version:

python --version

or:

python3 --version

2️⃣ Clone the Repository
git clone YOUR_GITHUB_REPOSITORY_URL

3️⃣ Open the Project
cd employee-management-system

4️⃣ Run the Program
python employee_management.py

🎓 Learning Objectives

By completing this project, you can understand:

✅ What classes and objects are

✅ How constructors work

✅ How inheritance works

✅ How super() is used

✅ How methods work inside classes

✅ How objects can be stored in lists

✅ How to build a menu-driven Python program

✅ How multi-level inheritance works

🔮 Future Improvements

This project can be extended with:

🔍 Search by GR number

✏️ Update employee information

🗑️ Delete employees

💾 Save data to a file

🗄️ Connect to a database

📊 Display all employees

🔐 Add login/authentication

🖥️ Build a GUI using Tkinter

🌐 Convert it into a web application

📈 Add employee reports

⚠️ Current Limitations

This version stores objects only while the program is running.

When the program exits:

Program Exit
     ↓
Objects Removed
     ↓
Data Lost

A future version could use JSON, CSV, SQLite, or MySQL to permanently store employee data.

🐛 Possible Code Improvements

For a production-ready version, the detail-search functionality should search through the lists rather than relying on the most recently entered grno, Per, Emp, or Man variables.

For example:

for person in per:
    if person.geno == gr_no:
        person.show_details()
        break
else:
    print("GR number not found.")

This allows the program to find any previously created person, not just the latest object.

📚 Key OOP Relationship
                 ┌───────────────┐
                 │    Person     │
                 │───────────────│
                 │ grno          │
                 │ name          │
                 │ age           │
                 └───────┬───────┘
                         │
                    inherits
                         ↓
                 ┌───────────────┐
                 │   Employee    │
                 │───────────────│
                 │ employee_id   │
                 │ salary        │
                 └───────┬───────┘
                         │
                    inherits
                         ↓
                 ┌───────────────┐
                 │    Manager    │
                 │───────────────│
                 │ department    │
                 └───────────────┘

👨‍💻 Author

Your Name

💻 Python Developer | 🎓 OOP Learner | 🚀 Building Projects with Python

⭐ Support

If you found this project useful:

⭐ Star the repository
🍴 Fork the project
📢 Share it with others
💡 Suggest improvements

📜 License

This project is created for educational and learning purposes.

Feel free to modify and improve it for your own learning journey.
