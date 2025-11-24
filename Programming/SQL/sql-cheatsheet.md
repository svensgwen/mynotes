# 🗄️ SQL Cheat Sheet — Essentials

![SQL](../../Images/sql.webp)

## 📌 Create / Drop / Select DB
```sql
CREATE DATABASE mydb;
DROP DATABASE mydb;
USE mydb;
```

## 🧱 Create Table
```sql
CREATE TABLE users (
  id INT PRIMARY KEY AUTO_INCREMENT,
  name VARCHAR(50),
  email VARCHAR(100) UNIQUE,
  age INT,
  created_at TIMESTAMP DEFAULT CURRENT_TIMESTAMP
);
```

## 🧹 Drop / Alter Table
```sql
DROP TABLE users;

ALTER TABLE users ADD COLUMN phone VARCHAR(20);
ALTER TABLE users DROP COLUMN phone;
```

## ✍️ Insert
```sql
INSERT INTO users (name, email, age)
VALUES ('Bob', 'bob@mail.com', 25);
```

## 📥 Select (Basics)
```sql
SELECT * FROM users;
SELECT name, email FROM users;
SELECT * FROM users WHERE age > 20;
```

## 🎯 Filtering
```sql
WHERE age >= 18
AND name LIKE 'A%'
OR email IS NOT NULL;
```

## 🔢 Sorting & Limiting
```sql
ORDER BY age DESC;
LIMIT 5;
```

## 🔄 Update / Delete
```sql
UPDATE users SET age = 30 WHERE id = 1;

DELETE FROM users WHERE age < 18;
```

## ⚡ Aggregate Functions
```sql
SELECT COUNT(*), AVG(age), MAX(age), MIN(age)
FROM users;
```

## 🧩 GROUP BY / HAVING
```sql
SELECT age, COUNT(*) 
FROM users
GROUP BY age
HAVING COUNT(*) > 1;
```

## 🔗 Joins
```sql
SELECT u.name, o.amount
FROM users u
JOIN orders o ON u.id = o.user_id;

LEFT JOIN
RIGHT JOIN
FULL JOIN
```

## 🪄 Subqueries
```sql
SELECT * FROM users
WHERE age > (SELECT AVG(age) FROM users);
```

## 🗜️ Indexing
```sql
CREATE INDEX idx_email ON users(email);
DROP INDEX idx_email;
```

## 🔐 User + Privileges (MySQL)
```sql
CREATE USER 'dev'@'localhost' IDENTIFIED BY 'pass';
GRANT ALL PRIVILEGES ON mydb.* TO 'dev'@'localhost';
FLUSH PRIVILEGES;
```
