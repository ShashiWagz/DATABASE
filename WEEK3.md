#week 3
###ASSIGNMENT 1 (EXERCISE2)

Q1 - 
select*from goal;
![Week3Assign1Q1.png](Week3Assign1Q1.png)


Q2 - 
select name,type from airport where iso_country="FI";
![Week3Assign1Q2.png](Week3Assign1Q2.png)


Q3
select name from airport where iso_country="FI" order by name asc;
![Week3Assign1Q3.png](Week3Assign1Q3.png)


Q4
select name,type from airport where iso_country="FI" order by type asc,name asc;
![Week3Assign1Q4.png](Week3Assign1Q4.png)


Q5
select name from country where name like "F%";
![Week3Assign1Q5.png](Week3Assign1Q5.png)


Q6
select name from country where name like "%F%";
![Week3Assign1Q6.png](Week3Assign1Q6.png)


Q7
select location from game where screen_name="Vesa";
![Week3Assign1Q7.png](Week3Assign1Q7.png)


Q8
select co2_consumed from game where screen_name="Ilkka";
![Week3Assign1Q8.png](Week3Assign1Q8.png)


Q9
SELECT DISTINCT co2_budget FROM game;
![Week3Assign1Q9.png](Week3Assign1Q9.png)


Q10
select screen_name, co2_budget, co2_consumed, co2_budget - co2_consumed as co2_left from game where screen_name="Ilkka";
![Week3Assign1Q10.png](Week3Assign1Q10.png)



###ASSIGNMENT 2 (EXERCISE3)

Q1
SELECT country.name AS "country name", airport.name AS "airport name" 
FROM country JOIN airport ON country.iso_country = airport.iso_country 
WHERE country.name = 'Iceland';
![Week3Assign2Q1.png](Week3Assign2Q1.png)

Q2
SELECT airport.name AS "airport name" FROM airport INNER JOIN 
country ON airport.iso_country = country.iso_country 
WHERE country.name = 'France' AND airport.type="Large_airport";
![Week3Assign2Q2.png](Week3Assign2Q2.png)


Q3
SELECT country.name AS "country_name", airport.name AS "airport_name" 
FROM country JOIN airport ON country.iso_country = airport.iso_country 
WHERE country.continent = 'AN';
![Week3Assign2Q3.png](Week3Assign2Q3.png)


Q4
select airport.name from game, airport 
where airport.ident=game.location and game.screen_name="Ilkka";
![Week3Assign2Q4.png](Week3Assign2Q4.png)


Q5
select airport.elevation_ft * 0.3048 AS elevation_m from game, 
airport where airport.ident=game.location and 
game.screen_name="heini";
![Week3Assign2Q5.png](Week3Assign2Q5.png)


Q6
select airport.name from game, airport 
where airport.ident=game.location and game.screen_name="Ilkka";
![Week3Assign2Q6.png](Week3Assign2Q6.png)


Q7
SELECT country.name FROM game 
JOIN airport ON airport.ident = game.location 
INNER JOIN country ON country.iso_country = airport.iso_country 
WHERE game.screen_name = "Ilkka";
![Week3Assign2Q7.png](Week3Assign2Q7.png)


Q8
SELECT goal.name FROM goal 
INNER JOIN goal_reached ON goal.id = goal_reached.goal_id
INNER JOIN game ON goal_reached.game_id = game.id
WHERE game.screen_name = "heini";
![Week3Assign2Q8.png](Week3Assign2Q8.png)


Q9
SELECT airport.name FROM airport  
INNER JOIN game ON airport.ident = game.location 
INNER JOIN goal_reached ON game.id = goal_reached.game_id
INNER JOIN goal ON goal_reached.goal_id = goal.id
WHERE goal.name = 'clouds'
AND game.screen_name = 'Ilkka';
![Week3Assign2Q9.png](Week3Assign2Q9.png)


Q10
SELECT country.name FROM airport  
INNER JOIN game ON airport.ident = game.location  
INNER JOIN goal_reached ON game.id = goal_reached.game_id  
INNER JOIN goal ON goal_reached.goal_id = goal.id  
INNER JOIN country ON airport.iso_country = country.iso_country  
WHERE goal.name = 'clouds' AND game.screen_name = 'Ilkka';

![Week3Assign2Q10.png](Week3Assign2Q10.png)




