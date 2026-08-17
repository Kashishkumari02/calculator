# 🧮 Java MVC Calculator

A simple desktop calculator application developed using **Java Swing** and the **MVC (Model-View-Controller) architecture**.

This project demonstrates how a Java GUI application can be organized into separate components for the **user interface, business logic, and event handling**.

---

## 📌 Project Overview

The Java MVC Calculator performs basic arithmetic operations through an easy-to-use graphical user interface.

### Supported Operations

* Addition `+`
* Subtraction `-`
* Multiplication `*`
* Division `/`
* Percentage `%`

The application follows the **MVC design pattern**, which separates the calculator's responsibilities into three components:

* **Model** → Performs calculations
* **View** → Displays the graphical user interface
* **Controller** → Handles user interactions and connects the Model with the View

---

## ✨ Features

* Simple and user-friendly GUI
* Built using Java Swing
* Supports basic arithmetic operations
* Uses MVC architecture
* Event-driven programming using `ActionListener`
* Separate files for Model, View, Controller, and application startup
* Result field is non-editable

---

## 🛠️ Technologies Used

* **Java**
* **Java Swing**
* **AWT Event Handling**
* **MVC Architecture**
* **Object-Oriented Programming**

### Java Components Used

* `JFrame`
* `JLabel`
* `JTextField`
* `JButton`
* `ActionListener`

---

## 📂 Project Structure

```text
Java-MVC-Calculator/
│
├── Main.java
├── Cmodels.java
├── Cviews.java
├── Ccontroller.java
└── README.md
```

---

## 🏗️ MVC Architecture

The project follows the **Model-View-Controller** design pattern.

```text
                Main.java
                    |
                    ↓
        ┌─────────────────────┐
        │     Controller      │
        │   Ccontroller.java  │
        └──────────┬──────────┘
                   |
          ┌────────┴────────┐
          ↓                 ↓
    ┌───────────┐     ┌───────────┐
    │   Model   │     │   View    │
    │ Cmodels   │     │ Cviews    │
    └───────────┘     └───────────┘
          |                 ↑
          |                 |
          └───── Result ────┘
```

### 1. Model — `Cmodels.java`

The Model contains the calculation logic.

It provides methods for:

```text
add()
sub()
mul()
div()
percentage()
```

The Model does not handle the graphical interface.

---

### 2. View — `Cviews.java`

The View creates the calculator's graphical interface using Java Swing.

It contains:

* Input fields for A and B
* Operation buttons
* Result field
* Calculator window

The View is responsible for displaying information to the user.

---

### 3. Controller — `Ccontroller.java`

The Controller handles button-click events using `ActionListener`.

It:

1. Reads the values entered by the user.
2. Detects which operation button was clicked.
3. Sends the values to the Model.
4. Receives the calculated result.
5. Displays the result in the View.

---

### 4. Main — `Main.java`

The Main class starts the application and connects the Model, View, and Controller.

```java
Cviews cv = new Cviews();
Cmodels cm = new Cmodels();
new Ccontroller(cm, cv);
```

---

## ➕ Operations

| Operation      |    Example | Result |
| -------------- | ---------: | -----: |
| Addition       |     10 + 5 |     15 |
| Subtraction    |     10 - 5 |      5 |
| Multiplication |     10 × 5 |     50 |
| Division       |     10 ÷ 5 |      2 |
| Percentage     | 20% of 500 |    100 |

---

## ⚙️ How to Run

### Prerequisites

Make sure the **Java Development Kit (JDK)** is installed.

Check Java:

```bash
java -version
```

Check the Java compiler:

```bash
javac -version
```

---

### Step 1: Clone the Repository

```bash
git clone YOUR_GITHUB_REPOSITORY_URL
```

Navigate into the project folder:

```bash
cd Java-MVC-Calculator
```

---

### Step 2: Compile the Project

Compile all Java files:

```bash
javac *.java
```

---

### Step 3: Run the Application

Run the Main class:

```bash
java Main
```

The Calculator GUI will open.

---

## 🖥️ Application Workflow

```text
User enters A and B
        ↓
User clicks an operation
        ↓
Controller detects the button
        ↓
Controller sends values to Model
        ↓
Model performs calculation
        ↓
Result returned to Controller
        ↓
Controller displays result in View
```

---

## 🧠 Concepts Learned

This project demonstrates practical understanding of:

* Java Classes and Objects
* Encapsulation
* Inheritance
* Interfaces
* Java Swing
* GUI Development
* Event Handling
* `ActionListener`
* MVC Architecture
* Exception Prevention
* Object-Oriented Programming

---

## 🚀 Future Improvements

The project can be enhanced with:

* Input validation for empty fields
* Better handling of division by zero
* Improved percentage functionality
* Clear/Reset button
* Decimal and advanced mathematical operations
* Keyboard support
* Improved GUI design
* Responsive layout
* Calculation history
* Scientific calculator functions
* Dark mode
* Better error messages

---

## 🎯 Learning Objective

The main objective of this project is to understand how to build a basic desktop application in Java while applying the **MVC architecture** and **event-driven programming**.

It is suitable as a beginner-level Java project for practicing **OOP, Swing, GUI development, and software architecture**.

---

## 📄 License

This project is created for **educational and learning purposes**.

You are free to modify and improve the project for your own learning.
