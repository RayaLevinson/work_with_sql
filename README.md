1. 
  SELECT id, first_name FROM johnbryceusers.users WHERE date_of_birth IN 
	  (SELECT MAX(date_of_birth) FROM johnbryceusers.users WHERE date_of_birth < 
 		  (SELECT MAX(date_of_birth) FROM johnbryceusers.users));
<br>		  
2. <br>
  SELECT COUNT(*) FROM johnbryceusers.users WHERE email LIKE '%edu';
<br>
3. <br>
  SELECT first_name,last_name from johnbryceusers.users WHERE date_of_birth='2000';
<br>  
4. <br>
  SELECT ROUND(AVG(date_of_birth)) FROM johnbryceusers.users WHERE phone LIKE '050%';
<br>  
5. <br>
  SELECT date_of_birth FROM johnbryceusers.users 
    GROUP BY date_of_birth 
    ORDER BY Count(id) 
    DESC LIMIT 3;
