1. 
  SELECT id, first_name FROM johnbryceusers.users WHERE date_of_birth IN 
	  (SELECT MAX(date_of_birth) FROM johnbryceusers.users WHERE date_of_birth < 
 		  (SELECT MAX(date_of_birth) FROM johnbryceusers.users));
<br>		  
2. <br>
  SELECT COUNT(*) FROM johnbryceusers.users WHERE email LIKE '%edu';
3.
  SELECT first_name,last_name from johnbryceusers.users WHERE date_of_birth='2000';
4. 
  SELECT ROUND(AVG(date_of_birth)) FROM johnbryceusers.users WHERE phone LIKE '050%';
5.
  SELECT date_of_birth FROM johnbryceusers.users 
    GROUP BY date_of_birth 
    ORDER BY Count(id) 
    DESC LIMIT 3;
