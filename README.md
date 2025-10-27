# Cloud-Database-Practical
Cloud database instance creation and connection task (AWS RDS + MySQL Workbench)

Task 5: Create and Connect to a Cloud Database Instance
Objective:

To understand how cloud databases work by creating a managed SQL database instance on AWS RDS, connecting it using MySQL Workbench, and performing basic SQL operations.

Steps:

Logged in to AWS Management Console and opened RDS service.

Clicked on Create database, selected MySQL, and used the Free Tier template.

Set the database name as intern-db, created username and password.

Enabled Public access so that the instance can be accessed from MySQL Workbench.

Created a new security group and added an inbound rule with type MySQL/Aurora, port 3306, and source as My IP.

Waited for the database to be available, then copied the endpoint from AWS RDS.

Opened MySQL Workbench, created a new connection using the endpoint, port 3306, username, and password.

Connected successfully to the RDS instance.

Ran the following SQL commands:

CREATE DATABASE intern_db;
USE intern_db;

CREATE TABLE students (
  id INT AUTO_INCREMENT PRIMARY KEY,
  name VARCHAR(50),
  domain VARCHAR(30),
  score INT
);

INSERT INTO students (name, domain, score)
VALUES ('Aarav', 'Cloud', 95), ('Diya', 'DevOps', 89);

SELECT * FROM students;


Verified that data was inserted successfully and the database was working fine.

Learnings:

Learned how to create and configure an AWS RDS MySQL database.

Understood how to manage access using security groups.

Learned to connect and run SQL commands using MySQL Workbench.

Screenshots:

AWS-RDS.png

MySQL-Workbench.png

SQL-Commands-and-Output.png
