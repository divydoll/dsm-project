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

