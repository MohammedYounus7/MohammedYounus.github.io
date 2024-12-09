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
        #password-checker-output, #expense-tracker-output, #expense-tracker-total {
            margin-top: 10px;
            font-weight: bold;
        }
        #password-checker-fail, #expense-tracker-fail {
            margin-top: 10px;
            font-weight: bold;
            color: red;
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
        <li><a href="#password-checker">Python Password Checker</a> - A Python script that checks the strength of a password and limits the number of attempts.</li>
        <li><a href="#expense-tracker">Expense Tracker</a> - A Python application that allows users to input and manage their expenses, providing a summary and total spending.</li>
    </ul>

    <!-- Password Checker Section -->
    <section id="password-checker">
        <h3>Python Password Checker</h3>
        <p>Enter a password below to check if it's at least 8 characters long (you have 3 attempts). The password checker will give you feedback based on your input:</p>
        
        <input type="text" id="password-input" placeholder="Enter your password">
        <button onclick="checkPassword()">Check Password</button>
        
        <div id="password-checker-output"></div>
        <div id="password-checker-fail"></div>

        <h4>Python Code for Password Checker</h4>
        <pre>
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
        </pre>
    </section>

    <!-- Expense Tracker Section -->
    <section id="expense-tracker">
        <h3>Expense Tracker</h3>
        <p>Track your expenses by entering the amount, category, and description. The total expenses will be calculated and displayed below.</p>
        
        <input type="number" id="expense-amount" placeholder="Amount" step="0.01">
        <input type="text" id="expense-category" placeholder="Category">
        <input type="text" id="expense-description" placeholder="Description">
        <button onclick="addExpense()">Add Expense</button>

        <div id="expense-tracker-output"></div>
        <div id="expense-tracker-total"></div>
        <div id="expense-tracker-fail"></div>

        <h4>Python Code for Expense Tracker</h4>
        <pre>
import json

class ExpenseTracker:
    def __init__(self):
        self.expenses = []

    def add_expense(self, amount, category, description):
        expense = {'amount': amount, 'category': category, 'description': description}
        self.expenses.push(expense)

    def get_total(self):
        total = sum(expense['amount'] for expense in self.expenses)
        return total

def add_expense(amount, category, description):
    tracker.add_expense(amount, category, description)
    display_expenses()

def display_expenses():
    total = tracker.get_total()
    document.getElementById('expense-tracker-output').innerText = "Expenses Added Successfully"
    document.getElementById('expense-tracker-total').innerText = "Total Expenses: " + total
        </pre>
    </section>

</section>

<section id="contact">
    <h2>Contact</h2>
    <p>Email: <a href="mailto:Yusufyounus786@icloud.com">Yusufyounus786@icloud.com</a></p>
</section>

<footer>
    <p>&copy; 2024 Mohammed Younus</p>
</footer>

<script>
// Password Checker Functionality
let attempts = 3;

function checkPassword() {
    const password = document.getElementById('password-input').value;
    const output = document.getElementById('password-checker-output');
    const fail = document.getElementById('password-checker-fail');

    if (password.length >= 8) {
        output.innerText = "Password accepted!";
        fail.innerText = "";
        attempts = 3; // Reset attempts on successful entry
    } else {
        attempts--;
        fail.innerText = `Password too short! You have ${attempts} attempts left.`;
        output.innerText = "";
    }

    if (attempts === 0) {
        fail.innerText = "You have run out of attempts. Please try again later.";
        document.getElementById('password-input').disabled = true; // Disable input after 3 attempts
    }
}

// Expense Tracker Functionality
let expenses = [];

function addExpense() {
    const amount = parseFloat(document.getElementById('expense-amount').value);
    const category = document.getElementById('expense-category').value;
    const description = document.getElementById('expense-description').value;
    
    const fail = document.getElementById('expense-tracker-fail');
    const output = document.getElementById('expense-tracker-output');
    const totalOutput = document.getElementById('expense-tracker-total');

    if (amount && category && description) {
        expenses.push({amount, category, description});
        output.innerText = `Expense of ${amount} in category '${category}' added successfully.`;
        
        // Calculate total expenses
        let total = expenses.reduce((sum, expense) => sum + expense.amount, 0);
        totalOutput.innerText = `Total Expenses: ${total.toFixed(2)}`;
        fail.innerText = "";
    } else {
        fail.innerText = "Please fill in all fields correctly.";
        output.innerText = "";
        totalOutput.innerText = "";
    }
}
</script>

</body>
</html>

