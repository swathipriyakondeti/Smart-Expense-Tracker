# 💰 Smart Expense Tracker

A multi-user expense management system in Python (Tkinter) with budget monitoring, multiple graph types and Excel-ready CSV export.

## Overview
Smart Expense Tracker helps users record their daily spending, set a monthly budget and understand where their money goes. Each user has a separate account, and all data is stored locally in JSON files, so the app runs without any database or internet connection.

## Features
- **User accounts** – sign up and log in; passwords are stored as salted PBKDF2-SHA256 hashes, never as plain text
- **Add and delete expenses** with date, amount and category (Food, Rent, Transport, Shopping, Bills, Other, or your own)
- **Expense table** showing every recorded transaction
- **Monthly budget** with a dashboard showing total spent, budget, remaining amount and an animated progress bar
- **Budget alerts** – a warning at 80% usage and a clear message when the budget is exceeded
- **Graphs** – Pie (by category), Bar, Monthly Trend and a Combined view
- **Export to CSV** – opens directly in Excel
- **Input validation** – rejects invalid amounts, negative budgets and unsafe usernames

## Tech Stack
| Area | Technology |
|------|------------|
| Language | Python 3.11+ |
| Interface | Tkinter |
| Charts | Matplotlib |
| Storage | JSON files (one per user) |
| Security | `hashlib` PBKDF2-SHA256 with random salt |

## Getting Started

**Requirements:** Python 3.11 or newer.

```bash
git clone https://github.com/swathipriyakondeti/Smart-Expense-Tracker.git
cd Smart-Expense-Tracker
pip install -r requirements.txt
python app.py
```


## How to Use
1. **Log in** or create an account.
2. **Set Budget** – enter your monthly budget.
3. **Add Expense** – enter the amount and choose a category, then save. Select a row and click *Delete Selected* to remove it.
4. **Dashboard** – see how much of your budget is used and get alerts.
5. **Graphs** – pick a chart type and click *Generate Graph*.
6. **Export** – save your expenses as a CSV file to open in Excel.

## Project Structure
```
Smart-expense-tracker/
├── app.py             # Application: login, dashboard, expenses, budget, graphs
├── requirements.txt   # Python dependencies
├── .gitignore
├── README.md
├── users.json     # Accounts (username + salted password hash)
└── swathi.json    # Demo user's expenses and budget
```

## Future Improvements
- Expense prediction with machine learning (forecast next month per category)
- Edit existing expenses and add custom budgets per category
- Recurring expenses and reminders
- Move storage from JSON to SQLite
- Cross-platform window handling

## Author
Swathi Priya Kondeti
Computer Science Student


🏁 Conclusion

Smart Expense Tracker turns everyday expense records into clear, useful information. Users can log their spending, set a monthly budget, get alerts before they overspend and see where their money goes through graphs. The project combines a Tkinter interface, secure password storage, input validation and Matplotlib data visualization in a simple application that works offline, with no database setup. It can be extended later with features like expense prediction and SQLite storage.
