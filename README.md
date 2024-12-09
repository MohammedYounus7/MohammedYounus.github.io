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
        #password-checker-output {
            margin-top: 10px;
            font-weight: bold;
            color: green;
        }
        #password-checker-fail {
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
        <p>This project allows users to input and track their expenses. The total spending is calculated, and the user can view all of their expenses with categories and descriptions.</p>
        <pre>
import json

class ExpenseTracker:
    def __init__(self):
        self.expenses = []
        self.load_expenses()

    def load_expenses(self):
        try:
            with open('expenses.json', 'r') as f:
                self.expenses = json.load(f)
        except FileNotFoundError:
            self.expenses = []

    def save_expenses(self):
        with open('expenses.json', 'w') as f:
            json.dump(self.expenses, f)

    def add_expense(self, amount, category, description):
        expense = {'amount': amount, 'category': category, 'description': description}
        self.expenses.append(expense)
        self.save_expenses()
        print(f"Added expense: {amount} in {category} - {description}")

    def show_expenses(self):
        print("\nExpense Summary:")
        for idx, expense in enumerate(self.expenses, 1):
            print(f"{idx}. {expense['amount']} in {expense['category']} - {expense['description']}")

    def total_expenses(self):
        total = sum(expense['amount'] for expense in self.expenses)
        print(f"\nTotal Expenses: {total}")

def print_watermark():
    watermark = "Mohammed Younus"
    print(f"\n{'*' * 40}\n{watermark}\n{'*' * 40}\n")

tracker = ExpenseTracker()

def start_expense_tracker():
    print_watermark()
    print("Welcome to the Expense Tracker!")
    while True:
        print("\nOptions:")
        print("1. Add Expense")
        print("2. Show Expenses")
        print("3. Total Expenses")
        print("4. Exit")
        choice = input("Choose an option (1-4): ")

        if choice == "1":
            amount = float(input("Enter the expense amount: "))
            category = input("Enter the expense category (e.g., Food, Travel): ")
            description = input("Enter a brief description of the expense: ")
            tracker.add_expense(amount, category, description)
        elif choice == "2":
            tracker.show_expenses()
        elif choice == "3":
            tracker.total_expenses()
        elif choice == "4":
            print("Exiting Expense Tracker.")
            break
        else:
            print("Invalid choice. Please try again.")
    print_watermark()

start_expense_tracker()
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
// Function to handle password checking
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
</script>

</body>
</html>
