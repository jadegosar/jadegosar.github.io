## Project for Women's Basketball Team Performance Analysis

**Project description:** This project was completed for a collegiate men's basketball team with the ultimate goal of creating an application or UI that can be used by the Sport Performance team, particularly the Strength and Conditioning coaches. This interface would be used to inform decisions made around athlete injury risk based on fatigue on an individualized basis and if any interventions are needed to the training programs of a particular athlete. The objectives of this project were to make athlete monitoring easier for coaches and other performance staff as well as mitigate injury risk because it will provide a more objective indicator of when an athlete may be fatigued. Additionally this project will allow the performance staff and coaches to better understand the physical toll that practices and games have on the athletes, which in turn can be used to offer advice on how to adjust plans to mitigate athlete injury risk or flag those who might perform under their standard due to fatigue.

### 1. Data Description

The data sources used for this project were:

*Force Plate Data:* Data was collected from countermovement jumps that were performed on Force Plates twice a week. The initial step in this project was research focused on finding evidence that backed up associations between fatigue and variables we had access to from the countermovement jumps. The intention of this step was to determine the variables of interest in the analysis based on basketball specific research so that we could make a more manageable dataset from the ~200 variables that were available in the initial export. In our Principal Component Analysis of the Force Plate data, we were able to determine that 12 variables covered 92% of the variance in all of the data so we felt confident in our decision to reduce the number of variables to something very close to that number.

*Strive Data:* Data collected from Strive technology used EMG sensors in the athlete's shorts to provide various metrics of interest, many that are representive of accelerometer or muscle load measures. 

*Schedule Information:* Schedule information was used to map which Force Plate sessions and Strive files were collected during game weeks. Due to the fact that we wanted to look at the physical toll that practices leading up to the game had on athletes, we decided to...

*Minutes Played:* We used a file provided by the Applied Health and Performance Science department to determine the number of minutes every player was on the court in each game. This enabled us to...

*In-game metrics and player statistics:* These metrics were provided to us by a statistician that works with the basketball team in PDF format. From these inputs we were able to pull individual player plus/minuses per game as well as the overall team plus/minus. The plus/minus values we worked with were not the standard calculation for plus/minus as they were created using a formula that weighted certain metrics higher than others to calculate a number of "positive points" added and "negative points" which would be subtracted from the positive points to generate the plus/minus metric. We did not have a lot of visibility into the exact formula that calculated positive and negative points as they were generated using a propietary program created by the team's statistician but recieved feedback that this plus/minus was the preferred advanced statistic that the staff used to evaluate in-game performance. Ultimately, this allowed us to benchmark what games each athlete performed above their average plus/minus across the season along with when the team played particularly well or poorly irregardless of the outcome of the game.

### 2. Project Process

* Research sports performance related to men's basketball at a collegiate and professional level
* Clean and aggregate Sport Science data sources
* Exploratory data analysis of various data sources and data manipulation
* Trial Analysis
* Load Comparison and Analysis
* Regression modeling
* Statistical significance testing
* Determining Key Performance Indicators
* Creation of PowerBI dashboard
* Final conclusions and presentation to Sport Science and Performance Staff

### 3. Analysis in R Studio

*Cleaning and Aggregating Data Sources*

### 3. Final Output