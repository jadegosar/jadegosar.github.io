## RShiny App to visualize a Soccer Team's Performance over the course of a Season

**Project description:** This project was completed for the performance coach of an elite youth soccer club. The dataset that was provided was summarized event and GPS data for the six month season ranging from January to June at the indiviudal player level. The objective of the project was to build a Shiny app that allowed for the client to visualize data on a player and team level and the requirements were to have the ability to select players along with a regression line of trends over the season.

### 1. Data Description

The dataset contains columns containing the following information:
* player_id
* team_name
* activity_name
* match_id
* session_date - match date
* cat_min_played - minutes played from GPS
* distance - distance covered in meters
* decels - amount of decelerations
* accels - amount of accelerations
* hsr - high speed running yards (distance above 18 km/h)
* running_distance_2ms - distance covered over 2 m/s
* def_act - sum of tackles, pressure, foul
* touches - amount of ball receptions
* obv - sum on ball value
* actions_sum - def_act + touches
* team_score - goals scored by home team
* opp_score - goals scored by opponent

### 2. Application Functionality

```r
if (isAwesome){
  return true
}
```

### 3. Application User Interface

<center><img src="images/Soccer_App_1.png"/></center>
<center><img src="images/Soccer_App_2.png"/></center>
<center><img src="images/Soccer_App_3.png"/></center>
<center><img src="images/Soccer_App_4.png"/></center>
<center><img src="images/Soccer_App_5.png"/></center>
<center><img src="images/Soccer_App_6.png"/></center>
<center><img src="images/Soccer_App_7.png"/></center>
<center><img src="images/Soccer_App_8.png"/></center>

### 4. Provide a basis for further data collection through surveys or experiments

Sed ut perspiciatis unde omnis iste natus error sit voluptatem accusantium doloremque laudantium, totam rem aperiam, eaque ipsa quae ab illo inventore veritatis et quasi architecto beatae vitae dicta sunt explicabo. 

For more details on the code used to create the application see my [GitHub Repository](https://github.com/jadegosar/Game_Data_App).
