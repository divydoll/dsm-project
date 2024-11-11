**Group 9- Manchester City**

**Team Members**
JT Warren
Charlie Mixson
Cassandra Albright
Divya Matthew

**Scenario Description**
We are building our model for Manchester City to scout future potential opponents in the Champions League. We included real teams, players, and coaches from the Premier League, Bundesliga, La Liga, and the MLS. Our tables give Man City insight on the performance of other teams. Our model can track goals scored, wins, matches against common opponent, etc. Advanced statistics and data modeling has taken over the professional sports industry, and this a tiny example of what they do on a weekly basis

**Data Model**
![image](https://github.com/user-attachments/assets/4d9230da-f7ba-49b8-9cbe-f812adc36824)
	Entities:
	players
 		player_id PK
   		f_name
     		l_name
       		position
	 	nationality
   		team_id FK from teams
 	playerStats
 		player_id PK, FK from Players
   		goals
     		assists
       		passes
	 	tackles
   		minutes_played
     	teams
      		team_id PK
		team_name
  		city
    		league
      		wins
		draws
  		losses
    	coaches
     		coach_id PK
       		cf_name
	 	cl_name
   		start_date
     		team_id FK from teams
       		assistant_coach_id FK from coaches
	 matches
  		match_id PK
    		match_date
      		match_time
		match_loc
  	match_team_pairings
   		team_id PK, FK from teams
     		match_id PK, FK from matches
       	matchStats
   		team_id PK, FK from teams
     		match_id PK, FK from matches
       		shots_per_game
	 	pass_percentage
   		fouls_per_game
     		goals_scored
       		result
Our data model shows the relationships between Coachs, Players, Teams, and their statistics. We also included a relationships between coaches and their proteges. This can help Manchester City determine who to hire next based on which coach produces the best assistants. We can also track our opponents and their star players

**Data Dictionary**

![image](https://github.com/user-attachments/assets/d7cfd964-25db-4f81-af93-56153443dedc)
![image](https://github.com/user-attachments/assets/7e5866c1-1a9b-4427-8000-7fb4f09b52fc)
![image](https://github.com/user-attachments/assets/65355de2-ba15-4485-93ea-697ea9220c77)
![image](https://github.com/user-attachments/assets/ad1cccf3-8d23-4b0c-8ed6-95377caf68ee)
![image](https://github.com/user-attachments/assets/8b2910b2-0cdb-4dfb-b2d6-a5fa30e037a9)
![image](https://github.com/user-attachments/assets/0246e32a-c056-4059-ad47-f21e412eeb94)
![image](https://github.com/user-attachments/assets/26ce1580-d8be-481a-8881-3da37f308015)

**Ten Queries**

## 1. Identify the top 5 players with the most assists along with the teams they play for 
![image](https://github.com/user-attachments/assets/ca3c1bea-b973-4024-b36e-288a545386c6)

Identifying the top 5 players with the most assists and their respective teams is valuable for managers as it highlights key playmakers in the league, aiding in recruitment decisions, team strategy, and player valuations. Additionally, this data can be used for marketing purposes and to identify areas for player development, ultimately enhancing overall team performance and profitability.


## 2. Identify the top scorers from each club 
![image](https://github.com/user-attachments/assets/f9569d78-9017-44e8-8616-3c03aec2c216)

Identifying the top scorers from each club helps managers understand which players are most effective at converting opportunities into goals, guiding decisions on player retention, recruitment, and tactical planning. It also provides insights for marketing and promotional efforts by highlighting standout performers to fans and potential sponsors.


## 3. Identify matches where a team scored more goals than their average and what were their results, shots pg and passes pg were 
![image](https://github.com/user-attachments/assets/fb245c49-4bfc-4ff1-8ac2-63410a95374c)

Identifying matches where a team scored more goals than their average provides managers with insights into factors contributing to above-average performance, such as tactics, player form, or opponent weaknesses. Analyzing the results, shots per game, and passes per game in these matches can reveal patterns that help optimize strategies, improve training, and make data-driven decisions to replicate such high-scoring outcomes consistently.

## 4. Provide a detailed breakdown of each player’s performance in different leagues, specifically focusing on their average goals scored per match and average pass percentage. 
![image](https://github.com/user-attachments/assets/2b03f6f9-bc8c-4b1d-88ea-198fe8ba56e3)

By grouping the data by league and player, and then sorting by league and average goals scored, this query helps identify top performers in each league, making it valuable for comparing player efficiency and impact across different competitions. This information can assist managers, scouts, and analysts in evaluating player consistency and making data-driven decisions regarding player development, transfers, or strategic planning.


## 5. Retrieve the players with the highest number of tackles from each team, along with their first name, last name, and team name. 
![image](https://github.com/user-attachments/assets/9314f3e7-1d5d-4ed8-abb4-8f5e086454ef)

It allows managers and analysts to identify the best defensive players within each team, which is valuable for understanding defensive strengths, player contributions, and for making decisions about player training, positioning, and strategy. By sorting the results by team name, the query provides an organized view of top tacklers across all teams.


## 6. Retrieve detailed information about the player Lionel Messi, including his first name, last name, team name, and position. 
![image](https://github.com/user-attachments/assets/a0801467-0608-431f-ada1-3a3adbb581db)

It helps quickly identify specific details about a well-known player and can be used for player profile generation, reporting, or verifying his current team and position, which can be useful for managers, fans, or analysts looking for up-to-date player information.


## 7. Calculate the total number of goals scored by Lionel Messi. 
![image](https://github.com/user-attachments/assets/c45efcc2-9719-48da-bd6f-414c3252b271)

It aggregates his goal count across all matches in the playerStats table, providing an overview of his scoring performance. This information can be used for player performance analysis, historical records, or comparisons against other players. It's valuable for managers, analysts, and fans who want to quantify Messi’s goal-scoring achievements.

## 8. Provide an overview of player performance based on nationality, showing the number of players and the total number of goals scored by players from each nationality.
![image](https://github.com/user-attachments/assets/be57b98f-cb4e-4cb6-86d6-5039b43cc2ca)

It offers insights into how different nationalities contribute to overall performance. This information can help managers, analysts, and scouts identify strong talent pools by nationality, understand scoring patterns, and inform recruitment or scouting strategies.


## 9. Compare the performance of mentor-mentee coaching pairs based on the number of team wins
![image](https://github.com/user-attachments/assets/b07428f6-01eb-4cc3-8784-55a3886e660a)

This analysis can provide insights into the effectiveness of mentorship programs, track mentee development, and highlight successful coaches who have outperformed their mentors.


## 10. Retrieve the teams and the corresponding match ID for teams that competed against each other at Old Trafford on January 15, 2024, at 3:30 PM. 
![image](https://github.com/user-attachments/assets/b605da78-6f50-4da3-b9ce-e38eb964750a)

Retrieving this information is useful for managers, analysts, and fans to review specific matches played at a particular venue and time, such as Old Trafford. It helps identify key games, analyze performance metrics, and understand the context of team matchups. This data can also be used for scheduling, historical analysis, and preparing for future encounters between these teams at similar venues or conditions.


**Database Information**

![image](https://github.com/user-attachments/assets/65aaf018-3740-4e88-a8af-ba3cb869dd66)




