<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Mohammed Younus | Coding Portfolio</title>
    <meta name="description" content="Mohammed Younus's portfolio showcasing projects like Python apps, expense trackers, and to-do lists.">
    <link href="https://fonts.googleapis.com/css2?family=Poppins:wght@300;400;600&display=swap" rel="stylesheet">
    <style>
        /* Global Styles */
        body {
            font-family: 'Poppins', sans-serif;
            background-color: #E0F2F1; /* Light teal background */
            color: #333333; /* Dark gray text color */
            margin: 0;
            padding: 0;
            scroll-behavior: smooth;
        }

        /* Header Styles */
        header {
            background-color: #2F4F4F; /* Dark Slate Blue background */
            color: white;
            padding: 20px 0;
            text-align: center;
            box-shadow: 0 2px 10px rgba(0, 0, 0, 0.1);
        }

        header h1 {
            margin: 0;
            font-weight: 600;
            font-size: 2rem;
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
            transition: color 0.3s ease;
        }

        header nav ul li a:hover {
            color: #00BFAE; /* Light teal color on hover */
        }

        /* Section Styles */
    section {
    margin: 20px auto;
    padding: 20px;
    max-width: 800px;
    background: #FFFFFF; /* White background */
    border-radius: 10px;
    box-shadow: 0 4px 20px rgba(0, 0, 0, 0.1);
    margin-bottom: 40px;
}


        section h2, section h3 {
            color: #2F4F4F; /* Dark Slate Blue for headers */
            margin-bottom: 20px;
        }

        section p {
            line-height: 1.6;
        }

        /* Projects Section */
        .projects-list {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 20px;
            list-style: none;
            padding: 0;
        }

        .projects-list li {
            background: #f4f4f9;
            padding: 20px;
            border-radius: 10px;
            text-align: center;
            box-shadow: 0 4px 15px rgba(0, 0, 0, 0.1);
            transition: transform 0.3s ease, box-shadow 0.3s ease;
        }

        .projects-list li:hover {
            transform: translateY(-5px);
            box-shadow: 0 6px 20px rgba(0, 0, 0, 0.15);
        }

        .projects-list li a {
            color: #00BFAE; /* Light teal color for links */
            text-decoration: none;
            font-weight: 600;
        }

        .projects-list li a:hover {
            text-decoration: underline;
        }

        /* Button Styles */
        button {
            background-color: #00BFAE; /* Light teal button */
            color: white;
            border: none;
            padding: 10px 20px;
            border-radius: 5px;
            cursor: pointer;
            font-weight: 500;
            transition: background-color 0.3s ease;
        }

        button:hover {
            background-color: #00796B; /* Darker teal button on hover */
        }

        /* Footer */
        footer {
            text-align: center;
            padding: 20px;
            background: #2F4F4F; /* Dark Slate Blue footer */
            color: white;
        }

        /* Form Input Styles */
        input[type="password"],
        input[type="text"],
        input[type="number"] {
            width: 100%;
            padding: 10px;
            margin: 10px 0;
            border: 1px solid #ddd; /* Light gray border */
            border-radius: 5px;
        }

        input:focus {
            border-color: #00BFAE; /* Green border on focus */
        }

        /* To-Do List Styles */
        .task {
            display: flex;
            align-items: center;
            justify-content: space-between;
            margin-bottom: 10px;
        }

        .task input {
            margin-right: 10px;
        }

        /* Responsive Design */
        @media (max-width: 768px) {
            header h1 {
                font-size: 1.5rem;
            }

            .projects-list li {
                padding: 15px;
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

<section id="projects">
    <h2>Projects</h2>
    <ul class="projects-list">
        <li><a href="#password-checker">Python Password Checker</a></li>
        <li><a href="#expense-tracker">Expense Tracker</a></li>
        <li><a href="#to-do-list">To-Do List App</a></li>
        <li><a href="#weather-app">Weather App</a></li>
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
        <input type="number" id="expense-amount" required>
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

<section id="weather-app">
    <h3>Weather App</h3>
    <form id="weather-form">
        <label for="city-input">Enter City:</label>
        <input type="text" id="city-input" required>
        <button type="button" onclick="fetchWeather()">Get Weather</button>
    </form>
    <div id="weather-output"></div>
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
        if (password.length < 8) {
            output.textContent = "Password is too short. It must be at least 8 characters long.";
        } else {
            output.textContent = "Password is strong!";
        }
    }

    // Expense Tracker Script
    let totalExpense = 0;

    function addExpense() {
        const name = document.getElementById("expense-name").value;
        const amount = parseFloat(document.getElementById("expense-amount").value);
        const output = document.getElementById("expense-tracker-output");
        const total = document.getElementById("expense-tracker-total");

        if (!isNaN(amount)) {
            totalExpense += amount;
            output.innerHTML += `<p>${name}: $${amount.toFixed(2)}</p>`;
            total.textContent = `Total Expense: $${totalExpense.toFixed(2)}`;
        }
    }

    // To-Do List Script
    function addTask() {
        const task = document.getElementById("task-input").value;
        const output = document.getElementById("to-do-list-output");

        if (task) {
            const taskDiv = document.createElement("div");
            taskDiv.classList.add("task");

            const taskContent = document.createElement("span");
            taskContent.textContent = task;

            const deleteButton = document.createElement("button");
            deleteButton.textContent = "Delete";
            deleteButton.onclick = () => taskDiv.remove();

            taskDiv.appendChild(taskContent);
            taskDiv.appendChild(deleteButton);
            output.appendChild(taskDiv);
        }
    }

       // Weather App Script
    async function fetchWeather() {
        const city = document.getElementById("city-input").value;
        if (!city) {
            alert("Please enter a city name.");
            return;
        }

        const apiKey = "681a5c4faa617eaa9e1f0b9a98ed999b"; // Your API Key
        const weatherDiv = document.getElementById("weather-output");

        try {
            const response = await fetch(`https://api.openweathermap.org/data/2.5/weather?q=${city}&appid=${apiKey}&units=metric`);
            if (!response.ok) {
                throw new Error("City not found");
            }
            const data = await response.json();

            const weatherData = {
                temperature: data.main.temp,
                humidity: data.main.humidity,
                description: data.weather[0].description,
                icon: `https://openweathermap.org/img/w/${data.weather[0].icon}.png`
            };

            // Display weather data
            weatherDiv.innerHTML = `
                <p>Temperature: ${weatherData.temperature}°C</p>
                <p>Humidity: ${weatherData.humidity}%</p>
                <p>Description: ${weatherData.description}</p>
                <img src="${weatherData.icon}" alt="Weather Icon">
            `;
        } catch (error) {
            console.error('Error:', error);
            weatherDiv.innerHTML = `<p>Error: ${error.message}</p>`;
        }
    }
</script>
</body>
</html>
