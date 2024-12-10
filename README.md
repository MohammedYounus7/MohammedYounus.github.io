<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta name="description" content="Mohammed Younus's coding portfolio showcasing projects in Python, JavaScript, and more.">
    <meta name="author" content="Mohammed Younus">
    <title>Mohammed Younus | Coding Portfolio</title>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0-beta3/css/all.min.css">
    <style>
        body {
            font-family: Arial, sans-serif;
            background-color: #f4f4f9;
            margin: 0;
            padding: 0;
            overflow-x: hidden;
        }
        header {
            background-color: #333;
            color: white;
            padding: 20px;
            text-align: center;
            position: sticky;
            top: 0;
            z-index: 1000;
            transition: background-color 0.3s ease;
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
            transition: color 0.3s ease;
        }
        header nav ul li a:hover {
            color: #f4f4f9;
        }
        section {
            margin: 20px;
            padding: 20px;
            background-color: white;
            border-radius: 8px;
            box-shadow: 0 2px 8px rgba(0, 0, 0, 0.1);
            opacity: 0;
            transform: translateY(20px);
            animation: fadeIn 1s forwards;
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
        .skills-list {
            display: flex;
            gap: 20px;
            flex-wrap: wrap;
            justify-content: center;
        }
        .skills-list .skill {
            text-align: center;
            width: 80px;
        }
        .skills-list img {
            width: 50px;
            height: 50px;
            transition: transform 0.3s ease;
        }
        .skills-list img:hover {
            transform: scale(1.1);
        }
        .back-to-top {
            position: fixed;
            bottom: 30px;
            right: 30px;
            background-color: #333;
            color: white;
            border: none;
            padding: 10px;
            border-radius: 50%;
            cursor: pointer;
            display: none;
        }
        .back-to-top:hover {
            background-color: #444;
        }
        @keyframes fadeIn {
            to {
                opacity: 1;
                transform: translateY(0);
            }
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

<section id="skills">
    <h2>Skills & Technologies</h2>
    <div class="skills-list">
        <div class="skill">
            <img src="https://img.icons8.com/ios/50/000000/python.png" alt="Python">
            <p>Python</p>
        </div>
        <div class="skill">
            <img src="https://img.icons8.com/ios/50/000000/javascript.png" alt="JavaScript">
            <p>JavaScript</p>
        </div>
        <div class="skill">
            <img src="https://img.icons8.com/ios/50/000000/html-5.png" alt="HTML">
            <p>HTML</p>
        </div>
        <div class="skill">
            <img src="https://img.icons8.com/ios/50/000000/css3.png" alt="CSS">
            <p>CSS</p>
        </div>
    </div>
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
    <p>Project Description: A Python application that checks if a password meets the minimum security requirements.</p>
    <p>Challenges: Implementing a user-friendly password validation system with retry logic.</p>
    <p>Solutions: I added clear instructions and provided feedback on each incorrect attempt.</p>
    <p>Technologies: Python</p>
    <form id="password-form">
        <label for="password-input">Enter Password:</label>
        <input type="password" id="password-input" required>
        <button type="button" onclick="checkPassword()">Check Password</button>
    </form>
    <div id="password-checker-output"></div>
</section>

<section id="expense-tracker">
    <h3>Expense Tracker</h3>
    <p>Project Description: A simple application for tracking personal expenses.</p>
    <p>Challenges: Implementing a user-friendly way to add and calculate expenses.</p>
    <p>Solutions: I used JavaScript to dynamically update the total expenses in real-time.</p>
    <p>Technologies: HTML, CSS, JavaScript</p>
    <form id="expense-form">
        <label for="expense-name">Expense Name:</label>
        <input type="text" id="expense-name" required>
        <label for="expense-amount">Amount:</label>
        <input type="number" id="expense-amount" required>
        <button type="button" onclick="addExpense()">Add Expense</button>
    </form>
    <div id="expense-tracker-output"></div>
    <div id="expense-tracker-total"></div>
</section>

<section id="to-do-list">
    <h3>To-Do List App</h3>
    <p>Project Description: A simple To-Do List app to manage tasks.</p>
    <p>Challenges: Ensuring that tasks were added and displayed correctly.</p>
    <p>Solutions: I used JavaScript to handle the tasks dynamically.</p>
    <p>Technologies: HTML, CSS, JavaScript</p>
    <form id="to-do-list-form">
        <label for="task-input">Enter Task:</label>
        <input type="text" id="task-input" required>
        <button type="button" onclick="addTask()">Add Task</button>
    </form>
    <div id="to-do-list-output"></div>
</section>

<section id="contact">
    <h2>Contact</h2>
    <p>Email: <a href="mailto:Yusufyounus786@icloud.com">Yusufyounus786@icloud.com</a></p>
    <p>Phone: <a href="tel:+447895515945">07895515945</a></p>
    <p>LinkedIn: <a href="https://www.linkedin.com/in/mohammedyusufyounus/" target="_blank">Mohammed Younus LinkedIn Profile</a></p>
</section>

<footer>
    <p>&copy; 2024 Mohammed Younus</p>
    <p><a href="#about">About</a> | <a href="#projects">Projects</a> | <a href="#contact">Contact</a></p>
</footer>

<button class="back-to-top" onclick="scrollToTop()">&#8593;</button>

<script>
    // Page Load Animation
    window.addEventListener('load', () => {
        document.querySelectorAll('section').forEach((section, index) => {
            setTimeout(() => {
                section.style.opacity = 1;
                section.style.transform = 'translateY(0)';
            }, index * 300);
        });
    });

    // Scroll to Top
    window.onscroll = function() {
        if (document.body.scrollTop > 100 || document.documentElement.scrollTop > 100) {
            document.querySelector('.back-to-top').style.display = "block";
        } else {
            document.querySelector('.back-to-top').style.display = "none";
        }
    };
    
    function scrollToTop() {
        window.scrollTo({top: 0, behavior: 'smooth'});
    }

    // Password Checker
    function checkPassword() {
        const password = document.getElementById("password-input").value;
        const output = document.getElementById("password-checker-output");
        if (password.length >= 8) {
            output.textContent = "Password accepted!";
        } else {
            output.textContent = "Password too short!";
        }
    }

    // Expense Tracker
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

    // To-Do List
    let tasks = [];
    function addTask() {
        const task = document.getElementById("task-input").value;
        if (task) {
            tasks.push(task);
            displayTasks();
        }
    }

    function displayTasks() {
        const output = document.getElementById("to-do-list-output");
        output.innerHTML = tasks.map(task => `<li>${task}</li>`).join("");
    }
</script>

</body>
</html>

