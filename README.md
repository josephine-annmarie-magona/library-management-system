# JIAM Library Management System

## Project Overview
JIAM Library Management System is a Python-based application designed to help manage books, users, and borrow transactions. This system allows students and employees to view available books, borrow and return books, and track their borrowed books. The project provides an easy-to-use interface using PyQt5 for the front-end and integrates with an SQLite database to store book and user information.

Features
- User Management: 
  - Different user roles (Student, Employee).
  - Login and registration functionality.
  - Role-based access control.

- Book Management:
  - View available books.
  - Search for books based on title, author, or year.
  - Borrow and return books.
  - View detailed information about each book.

- Borrowed Books:
  - List borrowed books.
  - Option to read books (opens book details within the app).
  - Return books when finished.

- Interactive UI:
  - User-friendly interface built using PyQt5.
  - Grid layout for displaying books.
  - Scroll area integration for better user experience.

## Installation

### Requirements:
- Python 3.6 or higher
- PyQt5
- MySQL (or another SQL database of choice)

### Steps to Install:

1. Clone the repository:
   ```bash
   git clone https://github.com/josephine-annmarie-magona/library-management-system.git
   ```

2. Install dependencies:
   You will need to install PyQt5 :
   ```bash
   pip install PyQt5 
   ```

3. Run the Application:
   ```bash
   python main.py
   ```

## Usage

1. **Login**: 
   - Users can log in using their credentials (student ID or employee ID).
   
2. **Book Management**:
   - Users can browse all available books.
   - They can borrow a book and the system will track the return date.
   - After borrowing, users can read the book content (if applicable).

3. **Borrowed Books**:
   - The "Borrowed Books" section lists all books currently borrowed by the user.
   - Users can return books from this page.



## Technologies Used

- Python SQLite: Backend logic and application functionality.
- PyQt5: User interface (UI) for the application.
- Qt designer: for designing the interface.


## Database Schema

### Users Table
- `user_id`: Primary Key, User's unique identifier.
- `name`: User's full name.
- `role`: The user's role (student/employee).
- `email`: User's email address.
- `password`: User's hashed password.
And other role personalized fields

### Books Table
- `book_id`: Primary Key, Unique identifier for books.
- `title`: Title of the book.
- `author`: Author of the book.
- `year`: Year of publication.
- `description`: Short description or synopsis of the book.
- `image`: Path to the book's cover image.
- etc.....

### Borrowed Books Table
- `borrow_id`: Primary Key, Unique identifier for each borrow transaction.
- `book_id`: Foreign Key, Links to the Books table.
- `user_id`: Foreign Key, Links to the Users table.
- `borrow_date`: Date the book was borrowed.
- `return_date`: Date the book is due to be returned.
  

## License

This project is licensed under the BSD 2-Clause - see the [LICENSE](LICENSE) file for details.

