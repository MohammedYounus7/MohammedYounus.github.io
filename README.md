<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Mohammed Younus | Coding Portfolio</title>
    <meta name="description" content="Mohammed Younus's portfolio showcasing projects like Python apps, expense trackers, and to-do lists.">
    <link href="https://fonts.googleapis.com/css2?family=Poppins:wght@300;400;600&display=swap" rel="stylesheet">
    <style>
        body {
            font-family: 'Poppins', sans-serif;
            background-color: #f9f9fb;
            color: #333;
            margin: 0;
            padding: 0;
        }
        header {
            background: linear-gradient(135deg, #6a11cb, #2575fc);
            color: white;
            padding: 20px 0;
            text-align: center;
            box-shadow: 0 2px 10px rgba(0, 0, 0, 0.1);
        }
        header h1 {
            margin: 0;
            font-weight: 600;
        }
        header nav ul {
            display: flex;
            justify-content: center;
            list-style: none;
            margin: 10px 0 0;
            padding: 0;
        }
        header nav ul li {
            margin: 0 15px;
        }
        header nav ul li a {
            color: white;
            text-decoration: none;
            font-weight: 500;
        }
        header nav ul li a:hover {
            text-decoration: underline;
        }
        section {
            margin: 20px auto;
            padding: 20px;
            max-width: 800px;
            background: white;
            border-radius: 10px;
            box-shadow: 0 4px 20px rgba(0, 0, 0, 0.1);
        }
        section h2, section h3 {
            color: #6a11cb;
        }
        footer {
            text-align: center;
            padding: 20px;
            background: #333;
            color: white;
            margin-top: 30px;
        }
        .projects-list {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
            gap: 20px;
            list-style: none;
            padding: 0;
        }
        .projects-list li {
            background: #f4f4f9;
            padding: 15px;
            border-radius: 10px;
            text-align: center;
            box-shadow: 0 4px 10px rgba(0, 0, 0, 0.1);
            transition: transform 0.3s ease, box-shadow 0.3s ease;
        }
        .projects-list li:hover {
            transform: translateY(-5px);
            box-shadow: 0 6px 15px rgba(0, 0, 0, 0.15);
        }
        .projects-list li a {
            text-decoration: none;
            font-weight: 600;
            color: #333;
        }
        button {
            background: linear-gradient(135deg, #2575fc, #6a11cb);
            color: white;
            border: none;
            padding: 10px 20px;
            border-radius: 5px;
            cursor: pointer;
            transition: background 0.3s ease;
            font-weight: 500;
        }
        button:hover {
            background: linear-gradient(135deg, #6a11cb, #2575fc);
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
        <li>
            <a href="#password-checker">Python Password Checker</a>
        </li>
        <li>
            <a href="#expense-tracker">Expense Tracker</a>
        </li>
        <li>
            <a href="#to-do-list">To-Do List App</a>
        </li>
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
</section>

<section id="to-do-list">
    <h3>To-Do List App</h3>
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
</footer>

<script>
    // JavaScript remains the same
</script>

</body>
</html>

