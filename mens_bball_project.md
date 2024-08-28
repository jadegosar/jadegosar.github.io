## Project for Men's Basketball Team KPI Analysis

**Project description:** This project was completed for a collegiate men's basketball team with the ultimate goal of creating an application or UI that can be used by the Sport Performance team, particularly the Strength and Conditioning coaches. This interface would be used to inform decisions made around athlete injury risk based on fatigue on an individualized basis and if any interventions are needed to the training programs of a particular athlete. The objectives of this project were to make athlete monitoring easier for coaches and other performance staff as well as mitigate injury risk because it will provide a more objective indicator of when an athlete may be fatigued. Additionally, our hope was this analysis would allow the performance staff and coaches to better understand the physical toll that practices and games have on the athletes, which in turn can be used to offer advice on how to adjust plans to mitigate athlete injury risk or flag those who might perform under their standard due to fatigue.

### 1. Data Description

The data sources used for this project were:

*Force Plate Data:* Data was collected from countermovement jumps that were performed on Vald Forcedecks twice a week. The initial step in this project was research focused on finding evidence that backed up associations between fatigue and variables we had access to from the countermovement jumps. The intention of this step was to determine the variables of interest in the analysis based on basketball specific research so that we could make a more manageable dataset from the ~200 variables that were available in the initial export.

*Strive Data:* Data collected from Strive technology used EMG sensors in the athlete's shorts to provide various metrics of interest, many that represent accelerometer or muscle load measures. Due to the fact that we wanted to look at the physical toll that practices had on the athletes and inform decision-making leading up the game, we did not use data collected from the day of the competition.

*Schedule Information:* Schedule information was used to map which Force Plate sessions and Strive files were collected during game weeks and create a variable that determined how many days before or after a game each session was. This was used to map sessions that fell within 3 days before or after a game to explore if there was statistically significant differences in metrics between sessions leading up to and following a game.

*Minutes Played:* We used a file provided by the Applied Health and Performance Science department to determine the number of minutes every player was on the court in each game. This enabled us to set a minimum threshold for minutes played in a game to filter for athletes who played over a certain number of minutes across each game in the season.

*In-game metrics and player statistics:* These metrics were provided to us by a statistician that works with the basketball team in PDF format. From these inputs we were able to pull individual player plus/minuses per game as well as the overall team plus/minus. The plus/minus values we worked with were not the standard calculation for plus/minus as they were created using a formula that weighted certain metrics higher than others to calculate a number of "positive points" added and "negative points" which would be subtracted from the positive points to generate the plus/minus metric. We did not have a lot of visibility into the exact formula that calculated positive and negative points as they were generated using a propietary program created by the team's statistician but recieved feedback that this plus/minus was the preferred advanced statistic that the staff used to evaluate in-game performance. Ultimately, this allowed us to benchmark what games each athlete performed above their average plus/minus across the season along with when the team played particularly well or poorly irregardless of the outcome of the game.

### 2. Project Process

* Research sports performance related to men's basketball at a collegiate and professional level
* Clean and aggregate Sports Science data sources
* Exploratory data analysis of various data sources and data manipulation
* Trial Analysis
* Load Comparison and Analysis
* Regression modeling
* Statistical significance testing
* Determining Key Performance Indicators
* Creation of PowerBI dashboard
* Final conclusions and presentation to Sports Science and Performance Staff

### 3. Analysis in R Studio

**Exploratory Data Analysis**

<center><img src="images/MBB_Peak_Power_BP.png"/></center>
<center><img src="images/MBB_PlusMinus_Score.png"/></center>

**Force Plate Trial Analysis**

The purpose of the trial analysis was to establish the best way to represent an athlete's best effort and ability on a given test date. We knew that averaging across a given day or just taking the trial where one metric was at its maximum may not accomplish this so we decided to look at if the variables we were primarily interested in typically fell in the same trial or not.

**Strive Load Comparison and Analysis**

A supplemental analysis to compare Strive metrics, specifically external load, load per minute, and session duration, for the team across multiple seasons. The intention of this step was to explore how load metrics may have changed from the '22 to '23 when looking at returners versus the entire team in each respective part of the season. The html file with comparisons from each part of season was shared with the Men's Basketball Sports Scientist and was summarized at a high level for the Strength and Conditioning coach who was interested in whether the returners had similar load metrics in sessions across both seasons and to what extent the intensity and density of the sessions varied for the team.

**Regression Modeling**

We used linear regression modeling to determine which metrics from the Force Plate data had the strongest relationship with each position group (Bigs, Guards, Wings). We wanted to see if we could differentiate what metrics may be the most important indicators of underperformance or fatigue and personalize the results to each position group. To get the data ready for modeling, we created dummay variables for the position groups so they could be included in the linear regressions.

**Statistical Significance Testing**

We performed various t-tests to determine if there was a statistically signficant difference in means for the metrics of interest when comparing force plate testing sessions from before games to the ones that took place after games. The ultimate intention in this was to ascertain which metrics may best represent fatigue from the weekend as these variables would show a decrease when comparing the test before the game to the test after. We also looked into whether there were significant differences for the differing number of days after the game that testing sessions were held (i.e. 1-3 days after each game).

**Determining Key Performance Indicators**

The metrics that had statistically signficant differences between tests before a game and tests after a game were included in the final dashboard that my partner created to share with the Strength and Conditioning coach for the basketball team. Additionally, the variables that we found had significance in our linear regression modeling were included in the final PowerBI dashboard to create a comprehensive application that could provide feedback in real-time on the most important metrics from the countermovement jumps. From our trial analysis findings, we were also able to identify how to select the trial that represented the athlete's best ability on each test date and only show that jump in the dashboard. We were then able to calculate z-scores of each metric to compare over time and flag players whose scores fall outside of a specified number of standard deviations.

### 4. Final Deliverables

**Creation of PowerBI dashboard**

The below visualization shows the dashboard page that I created in PowerBI as a potential supplement to the dashboard my group created. The main goal I had was to see if there was a way we could effectively integrate our Strive data source to represent both the most important metrics we found from our force plate analysis and accelerometer and load measures collected via Strive.

<center><img src="images/MBB_Dashboard.png"/></center>



For more details on the code related to this project see my [Men's Basketball GitHub Repository](https://github.com/jadegosar/Collegiate_MBB_KPI_Reporting).
