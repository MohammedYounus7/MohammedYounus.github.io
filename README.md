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

        /* Weather Section */
        #weather {
            background-color: #ffffff;
            padding: 20px;
            border-radius: 10px;
            box-shadow: 0 4px 10px rgba(0, 0, 0, 0.1);
            margin-top: 20px;
        }

        .weather-result {
            margin-top: 20px;
        }

        .weather-result p {
            font-weight: bold;
        }

        .weather-result span {
            font-size: 1.5rem;
        }

        /* Responsive Design */
        @media (max-width: 768px) {
            header h1 {
                font-size: 1.5rem;
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
        <li><a href="#weather">Weather Application</a></li> <!-- Link to Weather Project -->
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

<section id="weather">
    <h3>Weather Application</h3>
    <form id="weather-form">
        <label for="location">Enter City Name:</label>
        <input type="text" id="location" required>
        <button type="button" onclick="getWeather()">Get Weather</button>
    </form>
    <div id="weather-result" class="weather-result"></div>
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
        output.innerHTML = toDoList.map((task, index) => {
            return `
                <div class="task">
                    <It looks like you need a complete working version of the code with the various interactive features (weather app, expense tracker, password checker, to-do list) for your website. Below is a consolidated, fully functional version of the portfolio webpage, which should work correctly with all the interactive applications, including the weather app. Just make sure to replace `'YOUR_API_KEY'` in the weather app section with your own valid OpenWeatherMap API key.

### Complete HTML, CSS, and JavaScript Code:

```html
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

        /* Weather Section */
        #weather {
            background-color: #ffffff;
            padding: 20px;
            border-radius: 10px;
            box-shadow: 0 4px 10px rgba(0, 0, 0, 0.1);
            margin-top: 20px;
        }

        .weather-result {
            margin-top: 20px;
        }

        .weather-result p {
            font-weight: bold;
        }

        .weather-result span {
            font-size: 1.5rem;
        }

        /* Responsive Design */
        @media (max-width: 768px) {
            header h1 {
                font-size: 1.5rem;
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
        <li><a href="#weather">Weather Application</a></li> <!-- Link to Weather Project -->
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

<section id="weather">
    <h3>Weather Application</h3>
    <form id="weather-form">
        <label for="location">Enter City Name:</label>
        <input type="text" id="location" required>
        <button type="button" onclick="getWeather()">Get Weather</button>
    </form>
    <div id="weather-result" class="weather-result"></div>
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
        output.innerHTML = toDoList.map((task, index) => {
            return `
                <div class="task">
                    <input type="checkbox" id="task-${index}" onclick="removeTask(${index})">
                    <label for="task-${index}">${task}</label>
                </It looks like you're trying to ensure the full functionality of various web applications in your portfolio, including a weather app, password checker, expense tracker, and to-do list. Here's the complete and working HTML, CSS, and JavaScript for your portfolio webpage:

```html
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
            background-color: #E0F2F1;
            color: #333333;
            margin: 0;
            padding: 0;
            scroll-behavior: smooth;
        }
        header {
            background-color: #2F4F4F;
            color: white;
            padding: 20px 0;
            text-align: center;
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
        }
        section {
            margin: 20px auto;
            padding: 20px;
            max-width: 800px;
            background: #FFFFFF;
            border-radius: 10px;
            box-shadow: 0 4px 20px rgba(0, 0, 0, 0.1);
            margin-bottom: 40px;
        }
        section h2, section h3 {
            color: #2F4F4F;
        }
        section p {
            line-height: 1.6;
        }
        #weather {
            background-color: #ffffff;
            padding: 20px;
            border-radius: 10px;
            box-shadow: 0 4px 10px rgba(0, 0, 0, 0.1);
        }
        .weather-result {
            margin-top: 20px;
        }
        .weather-result p {
            font-weight: bold;
        }
        .weather-result span {
            font-size: 1.5rem;
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
        <li><a href="#weather">Weather Application</a></li>
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

<section id="weather">
    <h3>Weather Application</h3>
    <form id="weather-form">
        <label for="location">Enter City Name:</label>
        <input type="text" id="location" required>
        <button type="button" onclick="getWeather()">Get Weather</button>
    </form>
    <div id="weather-result" class="weather-result"></div>
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
        output.innerHTML = toDoList.map((task, index) => {
            return `
                <div class="task">
                    <input type="checkbox" id="task-${index}" onclick="removeTask(${index})">
                    <label for="task-${index}">${task}</label>
                </div>
            `;
        }).join("");
    }

    function removeTask(index) {
        toDoList.splice(index, 1);
        displayTasks();
    }

    // Weather App Script
    function getWeather() {
        const city = document.getElementById("location").value;
        const apiKey = 'YOUR_API_KEY';  // Replace with your OpenWeatherMap API Key
        const url = `https://api.openweathermap.org/data/2.5/weather?q=${city}&appid=${apiKey}&units=metric`;

        fetch(url)
            .then(response => response.json())
            .then(data => {
                const weatherResult = document.getElementById("weather-result");
                if (data.cod === 200) {
                    weatherResult.innerHTML = `
                        <p>Weather in ${data.name}, ${data.sys.country}:</p>
                        <p><span>${data.weather[0].main}</span> - ${data.weather[0].description}</p>
                        <p>Temperature: ${data.main.temp}°C</p>
                        <p>Humidity: ${data.main.humidity}%</p>
                        <p>Wind Speed: ${data.wind.speed} m/s</p>
                    `;
                } else {
                    weatherResult.innerHTML = `<p>City not found. Please try again.</p>`;
                }
            })
            .catch(error => {
                console.error('Error fetching weather data:', error);
            });
    }
</script>

</body>
</html>
