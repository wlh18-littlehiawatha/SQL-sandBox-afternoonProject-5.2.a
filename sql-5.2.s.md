<!-- -- 1.
-- CREATE TABLE person (
--   person_id SERIAL PRIMARY KEY,
--   name TEXT,
--   age INTEGER,
--   height INTEGER,
--   city TEXT,
--   favorite_color TEXT
  
--   );

-- 2.

-- INSERT INTO person 
-- (name, age, height, city, favorite_color)

-- Values
-- ('j', 21, 160, 'Lehi', 'red'),

-- ('k', 2, 160, 'Lehi', 'red'),
-- ('l', 64, 160, 'Bountiful', 'Pink'),
-- ('m', 28, 165, 'Provo', 'Azul'),
-- ('n', 25, 167, 'Brigham', 'red')

-- 3.
-- SELECT * FROM person ORDER BY height DESC;

-- 4.
-- SELECT * FROM person ORDER BY height ASC;

-- 5.
-- SELECT * FROM person ORDER BY age DESC;

-- 6.
-- SELECT * FROM person WHERE age > 20;

-- 7.
-- SELECT * FROM person WHERE age = 18;

-- 8.
--  SELECT * FROM person WHERE age < 20 OR age > 30;

-- 9.
-- SELECT * FROM person WHERE age != 27;

-- 10.
-- SELECT * FROM person WHERE favorite_color != 'red';

-- 11.
-- SELECT * FROM person WHERE favorite_color NOT IN ('Azul', 'red');
-- solution code Answer
-- SELECT * FROM person WHERE favorite_color != 'red' AND favorite_color != 'blue';

-- 12.
-- SELECT * FROM person WHERE favorite_color IN ('orange', 'green');
-- solution code Answer
-- SELECT * FROM person WHERE favorite_color = 'orange' OR favorite_color = 'green';

--13. 
-- SELECT * FROM person WHERE favorite_color IN ('Azul', 'orange', 'green');

--14.
-- SELECT * FROM person WHERE favorite_color IN ('yellow', 'purple');








-- Table - orders -----------------------------------------------------------
-- 1.
-- CREATE TABLE orders (
--   order_id SERIAL PRIMARY KEY,
--   person_id INTEGER,
--   product_name VARCHAR(40),
--   product_price NUMERIC,
--   quantity INTEGER
--   )

-- 2.
-- INSERT INTO orders (person_id, product_name, product_price, quantity)
-- VALUES (0, 'Product', 12.50, 2),
-- (32, 'Product', 12.50, 2),
-- (2345, 'Product', 1.98, 2),
-- (32452, 'Product', 10.98, 2),
-- (245, 'Product', 0.99, 2),
-- (245, 'Product', 5.99, 2);
  
--3. 
-- SELECT * FROM orders

-- 4.
-- SELECT SUM(quantity) FROM orders;

-- 5.
-- SELECT SUM(product_price * quantity) FROM orders;

-- 6.
-- SELECT SUM(product_price * quantity) 
-- FROM orders
-- WHERE person_id = 0;






-- Table - artist-------------------------------------------------

-- 1.
-- INSERT INTO artist (name)
-- VALUES ('Joe Frost'),
-- ('Alex HinckelBurg'),
-- ('Whats my Name Again')

-- 2.
-- SELECT * FROM artist
-- ORDER BY name DESC
-- LIMIT 10;

-- 3.
-- SELECT * FROM artist 
-- ORDER BY name ASC
-- LIMIT 5

-- 4.
-- SELECT * FROM artist 
-- WHERE name 
-- LIKE 'Black%'

-- 5.
-- SELECT * FROM artist 
-- WHERE name 
-- LIKE '%Black%'




-- Table - employee-------------------------------------------------------

-- 1.
-- SELECT first_name, last_name 
-- FROM employee 
-- WHERE city = 'Calgary';

-- 2.
-- SELECT * FROM employee 
-- ORDER BY birth_date DESC;

-- SELECT MAX(birth_date) from employee;

-- 3.
-- SELECT MIN(birth_date) from employee;

-- 4. Is there a way to return the employee id out of this with the statement below?
-- SELECT * FROM employee
-- WHERE first_name = 'Nancy' 
-- AND last_name =  'Edwards';

-- SELECT * FROM employee
-- WHERE reports_to = 2

-- -- Alternative to the above, below is a nested function

--SELECT * FROM employee
--WHERE reports_to = (SELECT employee_id FROM employee
--WHERE first_name = 'Nancy'
--AND last_name = 'Edwards')


-- 5.
-- SELECT * FROM employee
-- WHERE city ='Lethbridge';

-- SELECT COUNT(*) FROM employee
-- WHERE city = 'Lethbridge';








-- Table - invoice --------------------------------------------------
-- 1.
-- SELECT COUNT(*) FROM invoice 
-- WHERE billing_country = 'USA';
  
--   2.
-- SELECT MAX(total) FROM invoice;

-- 3.
-- SELECT MIN(total) FROM invoice;

-- 4.
-- SELECT * FROM invoice 
-- WHERE total > 5;

-- 5.
-- SELECT COUNT(*) FROM invoice 
-- WHERE total < 5;

-- 6.
-- SELECT COUNT(*) FROM invoice 
-- WHERE billing_state 
-- IN ('CA', 'TX', 'AZ');

-- 7.
-- SELECT AVG(total) FROM invoice;

-- 8.
-- SELECT SUM(total) FROM invoice;



 -->
