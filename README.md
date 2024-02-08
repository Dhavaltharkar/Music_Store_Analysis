use music_store_analysis;
show tables;

-- Q1 What is the senior most employee based on job title?

SELECT * FROM employee order by levels DESC limit 1;

-- Q2 Which countries have the most invoices?

SELECT COUNT(*) AS bill_count, billing_country
FROM invoice
GROUP BY billing_country
ORDER BY bill_count DESC;

-- Q3 What are the top 3 values of total invoices?

SELECT total
FROM invoice
ORDER BY total DESC
LIMIT 3;

/* Q4. Which city has the best customers? We would ;ike to throw a promotional Music festival in the city
 we made the most money. 
 Write a query that returns one city that has the highest sum of invoice totals. Return both the city n
 ame and sum of all invoices totals*/
 
SELECT SUM(total) AS invoice_total, billing_city
FROM invoice
GROUP BY billing_city
ORDER BY invoice_total DESC;

 
 /* Q5. Who is the best customer? The customer who has spent the most money will be the declared the best 
 customer. 
 Write a query that returns the person who has spwnt the most money.*/
 
SELECT c.customer_id, c.first_name, c.last_name, SUM(voice.total) AS total
FROM customer AS c
JOIN invoice AS voice ON c.customer_id = voice.customer_id
GROUP BY c.customer_id, c.first_name, c.last_name
ORDER BY total DESC
LIMIT 1;

/* Q6. Write a query to return the email, first name, last name  and genre of all Rock Music listeers. 
Return your list ordered alphabetically by email starting with A */

SELECT DISTINCT c.email, c.first_name, c.last_name
FROM customer AS c
JOIN invoice AS voice ON c.customer_id = voice.customer_id
JOIN invoice_line AS inv ON voice.invoice_id = inv.invoice_id
JOIN track AS tr ON inv.track_id = tr.track_id
JOIN genre AS g ON tr.genre_id = g.genre_id
WHERE g.name LIKE 'Rock'
ORDER BY c.first_name, c.last_name
LIMIT 0, 1000;


use music_store_analysis;
show tables;

-- Q1 What is the senior most employee based on job title?

SELECT * FROM employee order by levels DESC limit 1;

-- Q2 Which countries have the most invoices?

SELECT COUNT(*) AS bill_count, billing_country
FROM invoice
GROUP BY billing_country
ORDER BY bill_count DESC;

-- Q3 What are the top 3 values of total invoices?

SELECT total
FROM invoice
ORDER BY total DESC
LIMIT 3;

/* Q4. Which city has the best customers? We would ;ike to throw a promotional Music festival in the city
 we made the most money. 
 Write a query that returns one city that has the highest sum of invoice totals. Return both the city n
 ame and sum of all invoices totals*/
 
SELECT SUM(total) AS invoice_total, billing_city
FROM invoice
GROUP BY billing_city
ORDER BY invoice_total DESC;

 
 /* Q5. Who is the best customer? The customer who has spent the most money will be the declared the best 
 customer. 
 Write a query that returns the person who has spwnt the most money.*/
 
SELECT c.customer_id, c.first_name, c.last_name, SUM(voice.total) AS total
FROM customer AS c
JOIN invoice AS voice ON c.customer_id = voice.customer_id
GROUP BY c.customer_id, c.first_name, c.last_name
ORDER BY total DESC
LIMIT 1;

/* Q6. Write a query to return the email, first name, last name  and genre of all Rock Music listeers. 
Return your list ordered alphabetically by email starting with A */

SELECT DISTINCT c.email, c.first_name, c.last_name
FROM customer AS c
JOIN invoice AS voice ON c.customer_id = voice.customer_id
JOIN invoice_line AS inv ON voice.invoice_id = inv.invoice_id
JOIN track AS tr ON inv.track_id = tr.track_id
JOIN genre AS g ON tr.genre_id = g.genre_id
WHERE g.name LIKE 'Rock'
ORDER BY c.first_name, c.last_name
LIMIT 0, 1000;


use music_store_analysis;
show tables;

-- Q1 What is the senior most employee based on job title?

SELECT * FROM employee order by levels DESC limit 1;

-- Q2 Which countries have the most invoices?

SELECT COUNT(*) AS bill_count, billing_country
FROM invoice
GROUP BY billing_country
ORDER BY bill_count DESC;

-- Q3 What are the top 3 values of total invoices?

SELECT total
FROM invoice
ORDER BY total DESC
LIMIT 3;

/* Q4. Which city has the best customers? We would ;ike to throw a promotional Music festival in the city
 we made the most money. 
 Write a query that returns one city that has the highest sum of invoice totals. Return both the city n
 ame and sum of all invoices totals*/
 
SELECT SUM(total) AS invoice_total, billing_city
FROM invoice
GROUP BY billing_city
ORDER BY invoice_total DESC;

 
 /* Q5. Who is the best customer? The customer who has spent the most money will be the declared the best 
 customer. 
 Write a query that returns the person who has spwnt the most money.*/
 
SELECT c.customer_id, c.first_name, c.last_name, SUM(voice.total) AS total
FROM customer AS c
JOIN invoice AS voice ON c.customer_id = voice.customer_id
GROUP BY c.customer_id, c.first_name, c.last_name
ORDER BY total DESC
LIMIT 1;

/* Q6. Write a query to return the email, first name, last name  and genre of all Rock Music listeers. 
Return your list ordered alphabetically by email starting with A */

SELECT DISTINCT c.email, c.first_name, c.last_name
FROM customer AS c
JOIN invoice AS voice ON c.customer_id = voice.customer_id
JOIN invoice_line AS inv ON voice.invoice_id = inv.invoice_id
JOIN track AS tr ON inv.track_id = tr.track_id
JOIN genre AS g ON tr.genre_id = g.genre_id
WHERE g.name LIKE 'Rock'
ORDER BY c.first_name, c.last_name
LIMIT 0, 1000;


use music_store_analysis;
show tables;

-- Q1 What is the senior most employee based on job title?

SELECT * FROM employee order by levels DESC limit 1;

-- Q2 Which countries have the most invoices?

SELECT COUNT(*) AS bill_count, billing_country
FROM invoice
GROUP BY billing_country
ORDER BY bill_count DESC;

-- Q3 What are the top 3 values of total invoices?

SELECT total
FROM invoice
ORDER BY total DESC
LIMIT 3;

/* Q4. Which city has the best customers? We would ;ike to throw a promotional Music festival in the city
 we made the most money. 
 Write a query that returns one city that has the highest sum of invoice totals. Return both the city n
 ame and sum of all invoices totals*/
 
SELECT SUM(total) AS invoice_total, billing_city
FROM invoice
GROUP BY billing_city
ORDER BY invoice_total DESC;

 
 /* Q5. Who is the best customer? The customer who has spent the most money will be the declared the best 
 customer. 
 Write a query that returns the person who has spwnt the most money.*/
 
SELECT c.customer_id, c.first_name, c.last_name, SUM(voice.total) AS total
FROM customer AS c
JOIN invoice AS voice ON c.customer_id = voice.customer_id
GROUP BY c.customer_id, c.first_name, c.last_name
ORDER BY total DESC
LIMIT 1;

/* Q6. Write a query to return the email, first name, last name  and genre of all Rock Music listeers. 
Return your list ordered alphabetically by email starting with A */

SELECT DISTINCT c.email, c.first_name, c.last_name
FROM customer AS c
JOIN invoice AS voice ON c.customer_id = voice.customer_id
JOIN invoice_line AS inv ON voice.invoice_id = inv.invoice_id
JOIN track AS tr ON inv.track_id = tr.track_id
JOIN genre AS g ON tr.genre_id = g.genre_id
WHERE g.name LIKE 'Rock'
ORDER BY c.first_name, c.last_name
LIMIT 0, 1000;


