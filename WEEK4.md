#week 3
###ASSIGNMENT 1 (EXERCISE4)

Q1 
select country.name as "country name" , airport.name as "airport name" 
from country join airport on country.iso_country=airport.iso_country 
where country.name="Finland";
![Week4Assign1Q1.png](Week4Assign1Q1.png)

Q2
select game.screen_name as "screen_name" , airport.name as "name" 
from game join airport on game.location = airport.ident;
![Week4Assign1Q2.png](Week4Assign1Q2.png)

Q3
SELECT game.screen_name AS "screen_name", country.name AS "name" 
FROM game JOIN airport ON game.location = airport.ident 
JOIN country ON airport.iso_country = country.iso_country; 
![Week4Assign1Q3.png](Week4Assign1Q3.png)

Q4
SELECT airport.name AS "Airport Name", game.screen_name AS "Player Name"
FROM airport LEFT JOIN game ON game.location = airport.ident 
WHERE airport.name LIKE '%Hels%';
![Week4Assign1Q4.png](Week4Assign1Q4.png)

Q5
SELECT goal.name, game.screen_name FROM goal 
LEFT JOIN goal_reached ON goal.id = goal_reached.goal_id  
LEFT JOIN game ON goal_reached.game_id=game.id;
![Week4Assign1Q5.png](Week4Assign1Q5.png)



###ASSIGNMENT 2 (EXERCISE5)

Q1
select name from country where iso_country in
(select iso_country from airport where name like 'Satsuma%');
![Week4Assign2Q1.png](Week4Assign2Q1.png)

Q2
select name from airport where iso_country in 
(select iso_country from country where name ="Monaco");
![Week4Assign2Q2.png](Week4Assign2Q2.png)

Q3
select screen_name from game where id in  
(select game_id from goal_reached where goal_id in 
(select id from goal where name='clouds'));
![Week4Assign2Q3.png](Week4Assign2Q3.png)

Q4
select name from country where iso_country not in 
(select iso_country from airport );
![Week4Assign2Q4.png](Week4Assign2Q4.png)

Q5
select name from goal where id not in (select goal_id from goal_reached 
where game_id in (select id from game where screen_name="Heini"));
![Week4Assign2Q5.png](Week4Assign2Q5.png)