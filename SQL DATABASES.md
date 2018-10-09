I used Chinook.sqlite database from SmartNInja git 

SELECT Name FROM Artist;
SELECT * FROM Invoice WHERE Invoice.BillingCountry='Germany';
SELECT COUNT(AlbumId) FROM Album;
SELECT COUNT(Country) FROM Customer WHERE Customer.Country='France';

Other commands for SQL with Chinook_Sqlite database:

SHOW DATABASES;
USE name_table;
SHOW TABLES;

SELECT SUM(total) FROM Invoice;

SELECT total FROM Invoice WHERE 
	total > 4.00 AND total < 8.00;

SELECT Total,CustomerId FROM Invoice WHERE 
	Total > 4.00 OR CustomerId < 8.00;

SELECT Total,CustomerId AS Total_results FROM Invoice WHERE 
	Total > 4.00 OR CustomerId < 8.00
	GROUP BY Total;

SELECT Total FROM Invoice GROUP BY Total HAVING COUNT(*);

SELECT Count(*) FROM Invoice WHERE Total > 15.00;


Change table data:

ALTER TABLE Album RENAME Album_New;
ALTER TABLE Album ADD country;
ALTER  TABLE Album MODIFY COLUMN country;
ALTER TABLE Album DROP COLUMN country;
