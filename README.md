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
        .watermark {
            text-align: center;
            font-size: 24px;
            color: #888;
            font-weight: bold;
        }
        #password-checker {
            margin-top: 20px;
            padding: 20px;
            background-color: #f9f9f9;
            border-radius: 8px;
            border: 1px solid #ddd;
        }
        input[type="password"], input[type="submit"] {
            padding: 10px;
            margin: 10px 0;
            border-radius: 5px;
            border: 1px solid #ccc;
        }
        input[type="submit"]:hover {
            background-color: #333;
            color: white;
        }
        pre {
            background-color: #f0f0f0;
            padding: 15px;
            border-radius: 5px;
            border: 1px solid #ddd;
            overflow: auto;
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
            <li><a href="#password-checker">Password Checker</a></li>
        </ul>
    </nav>
</header>

<section id="about">
    <h2>About Me</h2>
    <p>Hi, I'm Mohammed Younus, a passionate IT student currently learning programming languages like Python and Java. I'm an aspiring developer and love building projects to improve my skills. This portfolio showcases my work and projects so far. I'm 18 years old and a Level 2 IT student at Harrow College. I enjoy coding and am always looking for opportunities to learn and grow in the tech industry.</p>
</section>

<section id="projects">
    <h2>Projects</h2>
    <ul class="projects-list">
        <li><a href="https://github.com/yourusername/Password-Checker" target="_blank">Python Password Checker</a> - A Python script that checks the strength of a password.</li>
        <li><a href="https://github.com/yourusername/AnotherProject" target="_blank">Project Name</a> - A brief description of another project you have worked on.</li>
        <li><a href="https://github.com/yourusername/ProjectTitle" target="_blank">Project Name</a> - Short description of a third project you want to highlight.</li>
    </ul>
</section>

<section id="password-checker">
    <div class="watermark">Mohammed Younus</div>
    <h2>Password Checker</h2>
    <p>Enter a password (at least 8 characters) to check its validity. You have 3 attempts:</p>
    <form id="passwordForm">
        <label for="password">Password: </label>
        <input type="password" id="password" placeholder="Enter your password" required><br><br>
        <input type="submit" value="Submit">
    </form>
    <p id="result"></p>
    <p id="attempts"></p>
    
    <h3>Python Code for Password Checker:</h3>
    <pre>
# Python Password Checker with Multiple Attempts and Watermark Text
def check_password_length(password):
    if len(password) < 8:
        return False
    return True

def password_checker():
    watermark = "Mohammed Younus"  # Watermark text
    attempts = 3  # Number of attempts allowed
    print(f"\n{'*' * 40}\n{watermark}\n{'*' * 40}\n")  # Display watermark at the top
    
    while attempts > 0:
        password = input("Enter your password (at least 8 characters): ")
        if check_password_length(password):
            print("Password accepted!")
            break
        else:
            attempts -= 1
            if attempts > 0:
                print(f"Password too short! You have {attempts} attempts left.")
            else:
                print("You have run out of attempts. Please try again later.")
                break

    print(f"\n{'*' * 40}\n{watermark}\n{'*' * 40}\n")  # Display watermark at the bottom

# Call the password checker
password_checker()
    </pre>
</section>

<section id="contact">
    <h2>Contact</h2>
    <p>Email: <a href="mailto:Yusufyounus786@icloud.com">Yusufyounus786@icloud.com</a></p>
</section>

<footer>
    <p>&copy; 2024 Mohammed Younus</p>
</footer>

<script>
    let attemptsLeft = 3;  // Number of attempts allowed

    // Handle form submission
    document.getElementById('passwordForm').addEventListener('submit', function(event) {
        event.preventDefault(); // Prevent form from reloading the page
        
        const password = document.getElementById('password').value;
        const resultElement = document.getElementById('result');
        const attemptsElement = document.getElementById('attempts');

        // Check password length
        if (password.length >= 8) {
            resultElement.textContent = "Password accepted!";
            resultElement.style.color = "green";
        } else {
            attemptsLeft--;
            if (attemptsLeft > 0) {
                resultElement.textContent = "Password too short! Try again.";
                resultElement.style.color = "red";
                attemptsElement.textContent = `You have ${attemptsLeft} attempts left.`;
            } else {
                resultElement.textContent = "You have run out of attempts. Please try again later.";
                resultElement.style.color = "red";
                attemptsElement.textContent = "";
            }
        }
    });
</script>

</body>
</html>

