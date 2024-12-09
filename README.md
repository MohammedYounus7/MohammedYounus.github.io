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
        textarea {
            width: 100%;
            padding: 10px;
            border: 1px solid #ccc;
            border-radius: 5px;
            margin-bottom: 20px;
        }
        input[type="text"] {
            width: 100%;
            padding: 10px;
            border: 1px solid #ccc;
            border-radius: 5px;
            margin-bottom: 20px;
        }
        input[type="submit"] {
            padding: 10px 20px;
            background-color: #333;
            color: white;
            border: none;
            border-radius: 5px;
            cursor: pointer;
        }
        input[type="submit"]:hover {
            background-color: #555;
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
    <p>Hi, I'm Mohammed Younus, an 18-year-old Level 2 IT student at Harrow College. I'm passionate about programming and currently learning languages like Python and Java. As an aspiring developer, I truly enjoy coding and building projects to improve my skills. This portfolio showcases my work and projects so far, and I am always looking for opportunities to learn and grow in the tech industry.</p>
</section>

<section id="projects">
    <h2>Projects</h2>
    <ul class="projects-list">
        <li><a href="#password-checker">Python Password Checker</a> - A Python script that checks the strength of a password.</li>
        <li><a href="https://github.com/yourusername/AnotherProject" target="_blank">Project Name</a> - A brief description of another project you have worked on.</li>
        <li><a href="https://github.com/yourusername/ProjectTitle" target="_blank">Project Name</a> - Short description of a third project you want to highlight.</li>
    </ul>
</section>

<section id="password-checker">
    <h2>Python Password Checker</h2>
    <p>Submit your Python code below. Use this form to test out your password checker script and see how it works:</p>

    <form action="#" method="POST">
        <label for="code">Paste your Python code:</label><br>
        <textarea id="code" name="code" rows="10" placeholder="Paste your Python code here..."></textarea><br><br>
        
        <label for="password">Enter a password to test:</label><br>
        <input type="text" id="password" name="password" placeholder="Enter password"><br><br>
        
        <input type="submit" value="Submit Code">
    </form>
    
    <p><strong>Note:</strong> This is just a form submission placeholder. For full functionality, a backend server or JavaScript would be needed to process the code.</p>
</section>

<section id="contact">
    <h2>Contact</h2>
    <p>Email: <a href="mailto:Yusufyounus786@icloud.com">Yusufyounus786@icloud.com</a></p>
</section>

<footer>
    <p>&copy; 2024 Mohammed Younus</p>
</footer>

</body>
</html>
