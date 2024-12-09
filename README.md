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
        }
        #to-do-list-output, #task-status {
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
    <pre>
# Python Password Checker by Mohammed Younus
# Full code omitted for brevity.
    </pre>
</section>

<section id="expense-tracker">
    <h3>Expense Tracker</h3>
    <pre>
# Expense Tracker by Mohammed Younus
# Full code omitted for brevity.
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
    <div id="task-status"></div>
    <pre>
# Python Code for To-Do List App
# Full code displayed here.
    </pre>
</section>

<footer>
    <p>&copy; 2024 Mohammed Younus</p>
</footer>

<script>
    const toDoList = [];
    
    function addTask() {
        const taskInput = document.getElementById("task-input");
        const task = taskInput.value;
        if (task) {
            toDoList.push({ task: task, completed: false });
            taskInput.value = "";
            displayTasks();
        }
    }

    function displayTasks() {
        const output = document.getElementById("to-do-list-output");
        if (toDoList.length === 0) {
            output.innerHTML = "Your to-do list is empty!";
        } else {
            output.innerHTML = toDoList.map((item, index) => {
                return `${index + 1}. ${item.completed ? "[✔]" : "[ ]"} ${item.task}`;
            }).join("<br>");
        }
    }
</script>

</body>
</html>
