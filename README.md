- 👋 Hi, I’m SakshiPandey
- 👀 I’m interested in ...
- 🌱 I’m currently learning ...
- 💞️ I’m looking to collaborate on ...
- 📫 How to reach me ...

<!---
SakshiPandey07/SakshiPandey07 is a ✨ special ✨ repository because its `README.md` (this file) appears on your GitHub profile.
You can click the Preview link to take a look at your changes.
--->
import java.util.ArrayList;

import java.util.List;

import java.util.Scanner;

class Expense {

private String category;

private double amount;

public Expense(String category, double amount) {

this.category = category;

this.amount = amount;

}

public String getCategory() {

return category;

}

public double getAmount() {

return amount;

}

}

public class ExpenseTrackerApp {

private List<Expense> expenses;

private Scanner scanner;

public ExpenseTrackerApp() {

expenses = new ArrayList<>();

scanner = new Scanner(System.in);

}

public void start() {

boolean running = true;

while (running) {

System.out.println(“Expense Tracker App”);

System.out.println(“1. Add Expense”);

System.out.println(“2. Show Expenses”);

System.out.println(“3. Exit”);

System.out.print(“Choose an option: “);

int choice = scanner.nextInt();

switch (choice) {

case 1:

addExpense();

break;

case 2:

showExpenses();

break;

case 3:

running = false;

break;

default:

System.out.println(“Invalid choice.”);

}

}

System.out.println(“Thank you for using Expense Tracker App!”);

}

private void addExpense() {

System.out.print(“Enter expense category: “);

scanner.nextLine();

String category = scanner.nextLine();

System.out.print(“Enter expense amount: “);

double amount = scanner.nextDouble();

expenses.add(new Expense(category, amount));

System.out.println(“Expense added successfully.”);

}

private void showExpenses() {

if (expenses.isEmpty()) {

System.out.println(“No expenses recorded yet.”);

return;

}

System.out.println(“Expense List:”);

for (Expense expense : expenses) {

System.out.println(“Category: “ + expense.getCategory() + “, Amount: “ + expense.getAmount());

}

}

public static void main(String[] args) {

ExpenseTrackerApp app = new ExpenseTrackerApp();

app.start();

}

}
