# Library Management System Database

## Project Description
This project implements a relational database for a Library Management System using MySQL. The database manages books, authors, publishers, categories, members, and loans, supporting key library operations such as tracking book availability, member loans, and fines.

### Features
- **Tables**: Authors, Publishers, Categories, Books, Members, Loans, Book_Authors, Book_Categories.
- **Relationships**:
  - One-to-Many: Publishers to Books, Members to Loans, Books to Loans.
  - Many-to-Many: Books to Authors, Books to Categories (via junction tables).
- **Constraints**: Primary keys, foreign keys, UNIQUE, NOT NULL, and CHECK constraints for data integrity.
- **Additional Constraints**:
  - Books: `available_copies <= total_copies` (ensures available copies don’t exceed total copies).
  - Loans: `due_date >= loan_date` (ensures due date is on or after loan date).

## How to Run/Setup the Project
1. **Prerequisites**:
   - Install MySQL (e.g., MySQL Community Server).
   - Use a MySQL client (e.g., MySQL Workbench, VS Code with SQLTools, or command-line).
2. **Steps**:
   - Clone this repository:
     ```bash
     git clone https://github.com/your-username/Library-Management-System.git