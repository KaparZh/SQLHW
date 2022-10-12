1)

SELECT FirstName,
       LastName,
       City,
       State
FROM Person p
         JOIN Address a ON p.PersonId = a.PersonId

2)

SELECT salary AS SecondHighestSalary
FROM employee
ORDER BY salary DESC
OFFSET 1
LIMIT 1;

3)

SELECT e.Name
FROM employee e
         JOIN Manager m ON e.managerid = m.id
    AND e.salary > m.salary

4)

SELECT email,
       count(*)
FROM person
GROUP BY email
HAVING count(*) > 1

5)

SELECT name
FROM customers
EXCEPT
SELECT name
FROM customers c
         JOIN orders o ON c.id = o.customerid

6)

SELECT class
FROM courses
GROUP BY class
HAVING count(*) >= 5
