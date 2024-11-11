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






