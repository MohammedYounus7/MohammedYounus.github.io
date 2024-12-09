<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Mohammed Younus | Coding Portfolio</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            background-color: #f4f4f9;
            margin: 0;
            padding: 0;
        }
        header {
            background-color: #333;
            color: white;
            padding: 20px;
            text-align: center;
        }
        header h1 {
            margin: 0;
        }
        header nav ul {
            list-style-type: none;
            padding: 0;
        }
        header nav ul li {
            display: inline;
            margin-right: 20px;
        }
        header nav ul li a {
            color: white;
            text-decoration: none;
        }
        section {
            margin: 20px;
            padding: 20px;
            background-color: white;
            border-radius: 8px;
            box-shadow: 0 2px 8px rgba(0, 0, 0, 0.1);
        }
        footer {
            text-align: center;
            padding: 10px;
            background-color: #333;
            color: white;
            position: fixed;
            bottom: 0;
            width: 100%;
        }
        .projects-list {
            list-style-type: none;
            padding: 0;
        }
        .projects-list li {
            margin: 10px 0;
        }
        .projects-list li a {
            color: #333;
            text-decoration: none;
            font-weight: bold;
        }
        pre {
            background-color: #f4f4f4;
            padding: 15px;
            border-radius: 5px;
            border: 1px solid #ddd;
            font-size: 14px;
            overflow-x: auto;
            white-space: pre-wrap; /* Ensures long lines wrap */
        }
        #password-checker-output, #expense-tracker-output, #expense-tracker-total, #to-do-list-output {
            margin-top: 10px;
            font-weight: bold;
        }
    </style>
</head>
<body>

<header>
    <h1>Mohammed Younus | Coding Portfolio</h1>
    <nav>
        <ul>
            <li><a href="#about">About Me</a></li>
            <li><a href="#projects">Projects</a></li>
            <li><a href="#contact">Contact</a></li>
        </ul>
    </nav>
</header>

<section id="about">
    <h2>About Me</h2>
    <p>Hi, I'm Mohammed Younus, a passionate IT student currently learning programming languages like Python and Java. I'm 18 years old and studying Level 2 IT at Harrow College. I enjoy coding and love building projects to improve my skills. This portfolio showcases my work and projects so far. I'm always looking for opportunities to learn and grow in the tech industry.</p>
</section>

<section id="projects">
    <h2>Projects</h2>
    <ul class="projects-list">
        <li><a href="#password-checker">Python Password Checker</a></li>
        <li><a href="#expense-tracker">Expense Tracker</a></li>
        <li><a href="#to-do-list">To-Do List App</a></li>
    </ul>
</section>

<section id="password-checker">
    <h3>Python Password Checker</h3>
    <form id="password-form">
        <label for="password-input">Enter Password:</label>
        <input type="password" id="password-input" required>
        <button type="button" onclick="checkPassword()">Check Password</button>
    </form>
    <div id="password-checker-output"></div>
    <pre>
# Python Password Checker by Mohammed Younus
def check_password_length(password):
    return len(password) >= 8

def password_checker():
    attempts = 3
    while attempts > 0:
        password = input("Enter your password (at least 8 characters): ")
        if check_password_length(password):
            print("Password accepted!")
            break
        else:
            attempts -= 1
            print(f"Password too short! {attempts} attempts left.")
    </pre>
</section>

<section id="expense-tracker">
    <h3>Expense Tracker</h3>
    <form id="expense-form">
        <label for="expense-name">Expense Name:</label>
        <input type="text" id="expense-name" required>
        <label for="expense-amount">Amount:</label>
        <input type="number" id="expense-amount" required>
        <button type="button" onclick="addExpense()">Add Expense</button>
    </form>
    <div id="expense-tracker-output"></div>
    <div id="expense-tracker-total"></div>
    <pre>
# Expense Tracker by Mohammed Younus
expenses = []

def add_expense(name, amount):
    expenses.append({"name": name, "amount": amount})

def calculate_total():
    return sum(exp["amount"] for exp in expenses)
    </pre>
</section>

<section id="to-do-list">
    <h3>To-Do List App</h3>
    <form id="to-do-list-form">
        <label for="task-input">Enter Task:</label>
        <input type="text" id="task-input" required>
        <button type="button" onclick="addTask()">Add Task</button>
    </form>
    <div id="to-do-list-output"></div>
    <pre>
# To-Do List App by Mohammed Younus
tasks = []

def add_task(task):
    tasks.append(task)

def display_tasks():
    for i, task in enumerate(tasks, start=1):
        print(f"{i}. {task}")
    </pre>
</section>

<section id="contact">
    <h2>Contact</h2>
    <p>Email: <a href="mailto:Yusufyounus786@icloud.com">Yusufyounus786@icloud.com</a></p>
    <p>Phone: <a href="tel:+447895515945">07895515945</a></p>
    <p>LinkedIn: <a href="https://www.linkedin.com/in/mohammedyusufyounus/" target="_blank">Mohammed Younus LinkedIn Profile</a></p>
</section>


<footer>
    <p>&copy; 2024 Mohammed Younus</p>
</footer>

<script>
    // Password Checker Script
    function checkPassword() {
        const password = document.getElementById("password-input").value;
        const output = document.getElementById("password-checker-output");
        if (password.length >= 8) {
            output.textContent = "Password accepted!";
        } else {
            output.textContent = "Password too short!";
        }
    }

    // Expense Tracker Script
    let expenses = [];
    function addExpense() {
        const name = document.getElementById("expense-name").value;
        const amount = parseFloat(document.getElementById("expense-amount").value);
        if (name && amount > 0) {
            expenses.push({ name, amount });
            displayExpenses();
        }
    }
    function displayExpenses() {
        const output = document.getElementById("expense-tracker-output");
        const totalDisplay = document.getElementById("expense-tracker-total");
        output.innerHTML = expenses.map(exp => `${exp.name}: £${exp.amount.toFixed(2)}`).join("<br>");
        const total = expenses.reduce((sum, exp) => sum + exp.amount, 0);
        totalDisplay.textContent = `Total: £${total.toFixed(2)}`;
    }

    // To-Do List Script
    const toDoList = [];
    function addTask() {
        const taskInput = document.getElementById("task-input").value;
        if (taskInput) {
            toDoList.push(taskInput);
            displayTasks();
        }
    }
    function displayTasks() {
        const output = document.getElementById("to-do-list-output");
        if (toDoList.length === 0) {
            output.innerHTML = "No tasks available.";
        } else {
            output.innerHTML = toDoList.map((task, index) => `${index + 1}. ${task}`).join("<br>");
        }
    }
</script>

</body>
</html>

