<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Mohammed Younus | Coding Portfolio</title>
    <meta name="description" content="Mohammed Younus's portfolio showcasing projects like Python apps, expense trackers, and to-do lists.">
    <style>
        body {
            font-family: Arial, sans-serif;
            background-color: #f4f4f9;
            margin: 0;
            padding: 10px;
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
            display: flex;
            justify-content: center;
            list-style-type: none;
            padding: 0;
            gap: 20px;
        }
        header nav ul li a {
            color: white;
            text-decoration: none;
        }
        section {
            margin: 10px auto;
            padding: 20px;
            background-color: white;
            border-radius: 8px;
            box-shadow: 0 2px 8px rgba(0, 0, 0, 0.1);
            max-width: 90%;
        }
        footer {
            text-align: center;
            padding: 20px;
            background-color: #333;
            color: white;
            margin-top: 20px;
        }
        .projects-list {
            list-style-type: none;
            padding: 0;
        }
        .projects-list li {
            margin: 15px 0;
            padding: 10px;
            background-color: #f9f9f9;
            border-left: 4px solid #333;
            border-radius: 5px;
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
            white-space: pre-wrap;
        }
        button {
            transition: background-color 0.3s ease;
        }
        button:hover {
            background-color: #555;
            color: white;
        }
        button:focus {
            outline: 2px solid #007BFF;
        }
        #password-checker-output, #expense-tracker-output, #expense-tracker-total, #to-do-list-output {
            margin-top: 10px;
            font-weight: bold;
        }
        .dark-mode {
            background-color: #121212;
            color: #f4f4f4;
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
        <input type="number" id="expense-amount" required min="0.01">
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
    <button onclick="toggleDarkMode()">Toggle Dark Mode</button>
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
        output.innerHTML = expenses.map((exp, index) => `
            ${index + 1}. ${exp.name}: £${exp.amount.toFixed(2)}
            <button onclick="deleteExpense(${index})">Delete</button>
        `).join("<br>");
        const total = expenses.reduce((sum, exp) => sum + exp.amount, 0);
        totalDisplay.textContent = `Total: £${total.toFixed(2)}`;
    }
    function deleteExpense(index) {
        expenses.splice(index, 1);
        displayExpenses();
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
        output.innerHTML = toDoList.map((task, index) => `
            ${index + 1}. ${task}
            <button onclick="deleteTask(${index})">Delete</button>
        `).join("<br>");
    }
    function deleteTask(index) {
        toDoList.splice(index, 1);
        displayTasks();
    }

    // Dark Mode Toggle
    function toggleDarkMode() {
        document.body.classList.toggle("dark-mode");
    }
</script>

</body>
</html>

