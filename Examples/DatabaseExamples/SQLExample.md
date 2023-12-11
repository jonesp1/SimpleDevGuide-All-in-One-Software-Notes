# SQL Example: Employee Database

In this SQL example, we'll create a simple Employee Database with tables for employees and departments. This example assumes a relational database system like MySQL, PostgreSQL, or SQLite.

## Database Schema

### Employees Table

```sql
-- Create tables
CREATE TABLE Employees (
  EmployeeID INT PRIMARY KEY,
  FirstName VARCHAR(50),
  LastName VARCHAR(50),
  Birthdate DATE,
  DepartmentID INT,
  FOREIGN KEY (DepartmentID) REFERENCES Departments(DepartmentID)
);

CREATE TABLE Departments (
  DepartmentID INT PRIMARY KEY,
  DepartmentName VARCHAR(50)
);

-- Insert data
INSERT INTO Employees (EmployeeID, FirstName, LastName, Birthdate, DepartmentID)
VALUES
  (1, 'John', 'Doe', '1990-01-15', 1),
  (2, 'Jane', 'Smith', '1988-05-20', 2),
  (3, 'Bob', 'Johnson', '1995-08-10', 1);

INSERT INTO Departments (DepartmentID, DepartmentName)
VALUES
  (1, 'Engineering'),
  (2, 'Marketing'),
  (3, 'Human Resources');

-- Query employees
SELECT * FROM Employees;

-- Update employee
UPDATE Employees
SET Birthdate = '1993-03-25'
WHERE EmployeeID = 2;

-- Delete employee
DELETE FROM Employees
WHERE EmployeeID = 3;

/*
Query Employees with Departments by using join 
The JOIN operation is allows to combine data from both the Employees and Departments tables. 
It's a way to associate employees with their respective departments.
*/
SELECT Employees.EmployeeID, FirstName, LastName, Birthdate, DepartmentName
FROM Employees
JOIN Departments ON Employees.DepartmentID = Departments.DepartmentID;
Join 


