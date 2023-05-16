Here is the schema diagram to show us the available tables and their relationships within the database:
![](https://github.com/PreetalM/SQL-Murder-Mystery/blob/main/schema.png)

In order to first learn about the crime that has taken place, I wanted to see the "crime_scene_report" table. I filtered the data based on the information I had: the crime type, city, and date.
![](https://github.com/PreetalM/SQL-Murder-Mystery/blob/main/query1.png)
![](https://github.com/PreetalM/SQL-Murder-Mystery/blob/main/result1.png)

Then I wanted to investigate each of the witnesses, starting with Annabel, searching the "person" table using her first name and address street name, using the SQL query below:
![](https://github.com/PreetalM/SQL-Murder-Mystery/blob/main/query2.png)
![](https://github.com/PreetalM/SQL-Murder-Mystery/blob/main/result2.png)

The second witness’ information is found by searching the same table for the street name and the last number on that street using the following query:
![](https://github.com/PreetalM/SQL-Murder-Mystery/blob/main/query3.png)
![](https://github.com/PreetalM/SQL-Murder-Mystery/blob/main/result3.png)

Now that we’ve narrowed down information about the 2 witnesses, it is time to explore more about what they know. Looking next at the "interview" table to see information the witnesses shared about the crime, I used this query:
![](https://github.com/PreetalM/SQL-Murder-Mystery/blob/main/query4.png)
![](https://github.com/PreetalM/SQL-Murder-Mystery/blob/main/result4.png)
![](https://github.com/PreetalM/SQL-Murder-Mystery/blob/main/query5.png)
![](https://github.com/PreetalM/SQL-Murder-Mystery/blob/main/result5.png)

Based on these interviews from the witnesses above, I know the suspect was seen on January 9th at the gym and has a membership number that starts with “48Z.”
![](https://github.com/PreetalM/SQL-Murder-Mystery/blob/main/query6.png)
![](https://github.com/PreetalM/SQL-Murder-Mystery/blob/main/result6.png)

I have now narrowed the suspects down to the 2 individuals above. In order to learn the identify of these suspects and considering they are gold members I ran the following:
![](https://github.com/PreetalM/SQL-Murder-Mystery/blob/main/query7.png)
![](https://github.com/PreetalM/SQL-Murder-Mystery/blob/main/result7.png)

I now know the 2 names of possible suspects. From the witness interviews, I also know the license number the witness saw. The license number is in the "drivers_license" table while the names are in the "person" table, so I need to JOIN these tables in order to have both pieces of information together to solve who committed the crime. I will do an INNER JOIN so that I only see the rows these tables have in common.
![](https://github.com/PreetalM/SQL-Murder-Mystery/blob/main/query8.png)
![](https://github.com/PreetalM/SQL-Murder-Mystery/blob/main/result8.png)

Hence, the person who committed the murder was Jeremy Bowers!
