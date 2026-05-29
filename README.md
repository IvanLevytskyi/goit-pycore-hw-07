# goit-pycore-hw-07
```markdown
# Assistant Bot (Address Book CLI App)

A functional command-line assistant bot designed to manage an address book, keep track of contacts, phone numbers, and birthdays, and dynamically calculate upcoming birthdays for the week ahead.

## Features

- **Contact Management:** Add new contacts or update existing phone numbers.
- **Phone Validation:** Ensures all stored numbers consist of exactly 10 digits.
- **Birthday Tracking:** Add and view birthdays formatted as `DD.MM.YYYY`.
- **Upcoming Birthday Notifications:** Automatically calculates which contacts have birthdays within the next 7 days, adjusting for weekend dates by moving the congratulation date to the upcoming Monday.
- **Robust Error Handling:** Uses Python decorators to capture missing arguments, invalid inputs, or non-existent records gracefully.

## Project Structure

- `classes.py`: Contains the core data models (`Field`, `Name`, `Phone`, `Birthday`, `Record`, `AddressBook`).
- `main.py`: Implements the command-line interface, input parsing, error handling, and logical command handlers.

## Command List

| Command | Arguments | Description |
| :--- | :--- | :--- |
| `hello` | None | Greets the user. |
| `add` | `[name] [phone]` | Adds a new contact or appends a phone number to an existing one. |
| `change` | `[name] [old_phone] [new_phone]` | Replaces an existing phone number with a new valid one. |
| `phone` | `[name]` | Shows all registered phone numbers for the specified contact. |
| `all` | None | Displays all saved contacts along with their details. |
| `add-birthday` | `[name] [date]` | Saves a birthday (`DD.MM.YYYY`) for the specified contact. |
| `show-birthday`| `[name]` | Displays the contact's birthday. |
| `birthdays` | None | Lists contacts whose birthdays occur within the next 7 days. |
| `close` / `exit`| None | Gracefully saves state (if applicable) and terminates the bot. |

## How to Run

1. Ensure you have Python 3.8+ installed.
2. Clone this repository or download the source files.
3. Open a terminal in the project directory and run:
   ```bash
   python main.py
