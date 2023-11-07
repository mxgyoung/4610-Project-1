
# MIST4610 Project 1






## Team Name

15058, 15061 Group 1
## Team Members

1. Jake Bogartz [@jab92323](https://github.com/jab92323)
2. Aiden Abramowitz [@aja1232](https://github.com/aja1232)
3. Max Young [@mxgyoung](https://github.com/mxgyoung)
4. Kiefer Sturisky [@ksturisky](https://github.com/ksturisky)
## Problem Description

The given problem is to create a database for an owner of a football team that models the entities and relationships that exist. We decided to improve the model by portraying the entities and relationships of an entire football league. The central entity of the model is Team, which represents each of the competing teams in our league. The team entity is then related to the players on the roster, the staff that works for them, the fans that cheer for them, their financial situation, and the results of each game they play in. Furthermore, we are looking to expand on the game entity by connecting it to entities that record player statistics within a game, injuries that occur, and the amount of games within a given season. Finally, we are including an awards entity to capture the best players from a given season. Our goal is to accurately model the relationships between these entities, insert sample data into each entity, and execute functioning queries in order to provide us with valuable information about our created football league.
## Data Model

Explanation of Data Model:
Our model is based on the structure of a created football league. The central entity, Team, includes information about the name of the team and where it is located. Within each team, there are many players, staff members, and fans, which explains the many to many relationships that exist between Team and the Player, Staff and Fan entities. Within the player entity, we capture the name, date of birth, and position of each individual. Within the staff entity, we include information on their name, job position, and salary. Furthermore, we implemented a recursive relationship within the staff entity in order to define who is the respective boss of each of the staff members. The fan entity includes information on their name, contact info, and season ticket status. 

Additionally, each team has different types of financial transactions they’re related to, which is why we created a one to many relationship between Team and Financials. The Financials entity includes other information such as the type of transaction, the amount, and the date that it takes place. The final relationship that takes place with the team entity is between Team and Game. Each team plays in many games which lead to using a many to many relationship to connect the entities. This relationship allows us to record which teams are playing in each game, what season it is taking place in, and the outcome of the game.

The Game entity has three other branches coming off of it, connecting to entities representing Statistics, Injuries, and Season. Within each game, there are many different statistics that can be recorded, however, a player can only record one of each type of statistic in a given game, leading to a one to one relationship. The statistics entity also records the type of statistic being logged, the value of the statistic, and which player the statistic correlates too. Similarly, there are many different injuries that can take place within a single game. Unlike statistics, it is possible for a player to have the same injury twice in a given game, leading to another one to many relationship. The Injuries entity records information on what type of injury occurred, to which player, and which game. The final branch that comes out of the game entity is in relation to the season entity. Although a season has many games, each game is identified by a unique number, making it impossible to have a repeating game ID. This means that the relationship between the two entities is one to one. Furthermore, we included information in the Season entity to capture the start and end dates of the given season.

The final relationships that take place within our model involve the Awards entity. The awards entity has a one to many relationship with season, since there are a number of different awards that are given out on any given season. The awards entity contains information on the name of the award, which player won the award, and in which season it was awarded. The other branch that Awards is related to is Player. Since it is impossible for a player to win the same award twice in the same season, a one to one relationship is used.

<img width="808" alt="Screenshot 2023-11-06 at 10 39 04 PM" src="https://github.com/aja1232/4610-Project-1/assets/148247965/422f7a17-93ed-43df-ae1f-45cf6bdf0b36">

## Data Dictionary

<img width="505" alt="Screenshot 2023-11-06 at 10 44 08 PM" src="https://github.com/aja1232/4610-Project-1/assets/148247965/4a91f584-e6d1-4136-b617-9838b99e9174">
<img width="502" alt="Screenshot 2023-11-06 at 10 43 55 PM" src="https://github.com/aja1232/4610-Project-1/assets/148247965/78ed1195-e5d6-45a8-9b8a-12473652c8aa">
<img width="500" alt="Screenshot 2023-11-06 at 10 43 41 PM" src="https://github.com/aja1232/4610-Project-1/assets/148247965/e4862ae0-c9fa-4166-8709-8800647b5a58">
<img width="502" alt="Screenshot 2023-11-06 at 10 43 32 PM" src="https://github.com/aja1232/4610-Project-1/assets/148247965/861a6e04-71c8-4a3e-a7ee-5894e09f8449">
<img width="511" alt="Screenshot 2023-11-06 at 10 43 18 PM" src="https://github.com/aja1232/4610-Project-1/assets/148247965/2e605cc8-e9df-4010-9eb4-53f507101af0">
<img width="506" alt="Screenshot 2023-11-06 at 10 42 47 PM" src="https://github.com/aja1232/4610-Project-1/assets/148247965/ec1f3e34-88db-430b-a62d-6ed9b1f6b750">
<img width="513" alt="Screenshot 2023-11-06 at 10 42 35 PM" src="https://github.com/aja1232/4610-Project-1/assets/148247965/fc1637fe-9c62-4068-9be6-03248eb5122f">
<img width="502" alt="Screenshot 2023-11-06 at 10 42 15 PM" src="https://github.com/aja1232/4610-Project-1/assets/148247965/acf023b7-d49f-4ee4-8ce2-265ff1a2336e">
<img width="501" alt="Screenshot 2023-11-06 at 10 41 55 PM" src="https://github.com/aja1232/4610-Project-1/assets/148247965/2112b52f-60ba-45dd-b5bc-14df919fd0d4">
<img width="506" alt="Screenshot 2023-11-06 at 10 41 45 PM" src="https://github.com/aja1232/4610-Project-1/assets/148247965/1acee50b-414f-4e3d-9b3f-f9d880d2bd3e">
<img width="496" alt="Screenshot 2023-11-06 at 10 41 31 PM" src="https://github.com/aja1232/4610-Project-1/assets/148247965/46fbc235-0c24-4b02-848f-bdd2d8cf3f58">
<img width="497" alt="Screenshot 2023-11-06 at 10 41 15 PM" src="https://github.com/aja1232/4610-Project-1/assets/148247965/ecd6ee0b-0b5b-4297-88bf-3310dfefb6b3">
<img width="491" alt="Screenshot 2023-11-06 at 10 40 43 PM" src="https://github.com/aja1232/4610-Project-1/assets/148247965/5902a2cb-f110-46af-af13-45823fd37fba">

## Queries

<img width="539" alt="Screenshot 2023-11-06 at 10 49 15 PM" src="https://github.com/aja1232/4610-Project-1/assets/148247965/42a09d0e-a47b-468d-b143-13b8ed456a68">



