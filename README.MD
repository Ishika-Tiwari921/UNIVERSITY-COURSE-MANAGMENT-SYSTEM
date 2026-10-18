# 🎓 University Course Management System (SQL)

## 📌 Project Overview
The **University Course Management System** is a SQL-based database project designed to manage university departments, students, courses, instructors, and student enrollments.

This project demonstrates practical SQL skills through database creation, data manipulation, filtering, aggregation, joins, subqueries, and window functions.

## 🎯 Project Objectives
- Create and manage a relational database for a university.
- Store student, department, course, instructor, and enrollment information.
- Retrieve meaningful insights using SQL queries.
- Practice CRUD operations and relational database concepts.
- Analyze enrollment trends and instructor salary information.

## 🗂️ Database Structure

The project consists of five main tables:

| Table | Description |
|---|---|
| `Department` | Stores department IDs and names |
| `Students` | Stores student details and enrollment dates |
| `Courses` | Stores course names, credits, and department IDs |
| `Instructors` | Stores instructor details, departments, and salaries |
| `Enrollments` | Maintains student-course enrollment records |

### 🔗 Table Relationships
- A department can offer multiple courses.
- A department can have multiple instructors.
- A student can enroll in multiple courses.
- A course can have multiple students.
- The `Enrollments` table connects students and courses.

## 🛠️ Technologies Used
- **SQL**
- Relational Database Management System (RDBMS)
- Primary Keys and Foreign Keys
- Aggregate Functions Joins and Sub Queries

## 💡 SQL Concepts Covered

- Database and table creation using `CREATE`
- Data insertion using `INSERT`
- Data retrieval using `SELECT`
- Data modification using `UPDATE`
- Data deletion using `DELETE`
- Filtering with `WHERE`
- Sorting and limiting records using `ORDER BY` and `LIMIT`
- Aggregate functions: `COUNT()`, `AVG()`, and `MAX()`
- Grouping and filtering groups using `GROUP BY` and `HAVING`
- `INNER JOIN` and `LEFT JOIN`
- Subqueries and `DISTINCT`
- Date functions and `EXTRACT()`
- String manipulation using `CONCAT()`
- Conditional logic using `CASE`
- Window functions using `OVER()` and running totals

## 📊 Example SQL Queries

### 1. Retrieve Students Enrolled After 2022
```sql
SELECT *
FROM Students
WHERE EnrollmentDate >= '2023-01-01';
```

### 2. Count Students Enrolled in Each Course
```sql
SELECT CourseID, COUNT(StudentID) AS TotalStudents
FROM Enrollments
GROUP BY CourseID;
```

### 3. Display Students Along with Their Courses
```sql
SELECT s.FirstName, s.LastName, c.CourseName
FROM Students s
INNER JOIN Enrollments e
    ON s.StudentID = e.StudentID
INNER JOIN Courses c
    ON e.CourseID = c.CourseID;
```

### 4. Find the Maximum Instructor Salary in Computer Science
```sql
SELECT MAX(i.Salary) AS MaximumSalary
FROM Instructors i
JOIN Department d
    ON i.DepartmentID = d.DepartmentID
WHERE d.DepartmentName = 'Computer Science';
```

## 🚀 How to Run the Project

1. Install or open a SQL database tool, such as PostgreSQL with pgAdmin.
2. Create a new SQL query file.
3. Run the database and table creation statements.
4. Insert the sample data into all five tables.
5. Execute the CRUD operations and analytical queries.
6. Review the results to understand how the database works.

**Note:** Run the script in the correct order because foreign keys depend on the related tables. Use consistent table names throughout the script.

## 📚 Learning Outcomes

Through this project, I practiced:
- Designing relational database schemas.
- Establishing relationships using primary and foreign keys.
- Writing SQL queries for real-world data retrieval.
- Performing data analysis using aggregate functions.
- Combining data from multiple tables using joins.
- Applying advanced SQL concepts to solve database problems.

## 👩‍💻 About This Project

This project is part of my **Data Analytics learning journey**, where I am strengthening my SQL skills and building practical database projects.

I look forward to applying these skills to real-world data analysis problems and continuously improving my technical knowledge.

⭐ If you find this project useful, feel free to star the repository!

**#SQL #DataAnalytics #DatabaseManagement #PostgreSQL #LearningByDoing**
