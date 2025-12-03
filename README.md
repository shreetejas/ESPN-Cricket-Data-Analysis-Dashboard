
# Project Title

A brief description of what this project does and who it's for

# ESPN Cricket Data Analysis-Dashboard

### Dashboard Link : https://app.powerbi.com/groups/me/reports/3af1be4b-8386-42c8-91e3-e9fadc91f714/157ccfd330bb86eea259?experience=power-bi

## Problem Statement

This dashboard gives teams and coaches a clear view of player performance across batting, bowling, and fielding. It highlights strengths, exposes weak areas, and helps compare players effectively. By analyzing key metrics like strike rate, economy, wickets, and fielding contributions, it reveals performance patterns and consistency levels. This enables teams to identify underperforming areas and take corrective actions through targeted training and better strategy planning.

Since the number of inconsistent or low-performing players is higher than the consistently performing ones, the team needs to work on improving overall player performance.

Also, since key metrics like batting strike rate, bowling economy, and fielding contributions show noticeable gaps, the team must focus on reducing these performance issues to achieve better match outcomes.

## ERD

<img width="1006" height="691" alt="Image" src="https://github.com/user-attachments/assets/ffacee4d-a627-4c6a-b16d-db24bdc0b1e2" />

### Steps followed 

- Step 1: Loaded the batting, bowling, and fielding datasets from ESPN Cricket website into Power BI Desktop.
- Step 2: In Power Query Editor, enabled Column distribution, Column quality, and Column profile options.
- Step 3: Enabled column profiling based on entire dataset to assess all rows.
- Step 4: Checked for missing, incorrect datatype in player metrics.
- Step 5: For calculations like average strike rate, economy, and dismissals, null values were ignored as they were not relevant for all players.
	In our dataset, Some parameters were assigned value 0, representing those parameters are not applicable.
	All these values have been ignored while calculating average rating
- Step 7: Added slicers for Player Name, Format, Span, and Role to analyze performance from multiple perspectives.
- Step 8: Added card visuals for overall performance metrics like total runs, wickets, catches, and combined strike rates.
- Step 9: Used custom visuals where required (e.g., KPI indicators) to represent strike rate, economy, and averages.
- Step 11: Calculated new measures such as, 

	a)Batting Consistency
        
	b)Bowling Strike Rate Efficiency

	c)Fielding Contribution Index

	These were used to show player overall impact.
- Step 12: Added logo, dashboard title, and section headers for a clean layout.
- Step 13: Published the final report to Power BI Service.


for creating new column following DAX expression was written;

- Step 14: New measure was created to find total count of customers.
Following DAX expression was written for the same,
## Snap of Rank column,     
Rank = RANKX(ALL(Batting),Batting[SR],,DESC,Dense)

<img width="73" height="731" alt="Image" src="https://github.com/user-attachments/assets/e1c93a6b-e085-4022-95f1-aedb93c9c2be" />

## Snap of Squared Deviation column,
Squared Deviation = POWER(Batting[Deviation],2) 

<img width="162" height="727" alt="Image" src="https://github.com/user-attachments/assets/6f001c66-3eca-45a4-9ae5-daf612241dee" />

## Snap of Absolute Deviation column,
Absolute Deviation = ABS(Batting[Deviation])

<img width="174" height="732" alt="Image" src="https://github.com/user-attachments/assets/01665cba-cfbb-453c-8d05-8e2a28ebe800" />

## Snap of Deviation column,
Deviation = Batting[Runs]-AVERAGE(Batting[Runs]) 

<img width="141" height="726" alt="Image" src="https://github.com/user-attachments/assets/8f719ee5-895f-4e7a-9959-aaf0bfdad040" />


## Snap of Category,
Category = LOOKUPVALUE('Strike Rate Table'[Category],'Strike Rate Table'[Strike_Rate],Batting[SR])

<img width="100" height="737" alt="Image" src="https://github.com/user-attachments/assets/13d227ce-8d1c-4867-bd8e-56188c3e0a16" />

Insights

interactive cricket performance dashboard was created in Power BI Desktop and then published to Power BI Service.

Below are some sample insights:

[1] Batting Performance Overview

Total runs scored by player is combined.

Player with highest strike rates and averages.

Comparison of 4s, 6s, and innings played.

[2] Bowling Performance Overview

Total wickets taken.

Bowling average and economy rate comparisons.

Best bowling figures and strike rate analysis.

[3] Fielding Performance Overview

Total catches, stumpings, and dismissals.

Dismissals per innings metric.   

##snapshot 
###Batting 

<img width="1312" height="735" alt="Image" src="https://github.com/user-attachments/assets/5485d7db-0333-4c98-9aff-db3141b885a2" />


###Bowling

<img width="1313" height="746" alt="Image" src="https://github.com/user-attachments/assets/6d0cc3d1-c9b4-4fd5-812a-3c9b356c5136" />

###Fielding

<img width="1335" height="751" alt="Image" src="https://github.com/user-attachments/assets/fb73256e-c3b9-41e3-90cf-3f320691b7ef" />

##Actionable Recommendations

-- Improve Low Strike Rate Batters: Conduct specialized batting sessions focused on power-hitting and strike rotation.

-- Control Bowling Economy: Provide targeted training for bowlers with high economy rates, especially in death overs.

-- Boost Fielding Performance: Introduce regular fielding drills focusing on catching, throwing accuracy, and anticipation.

-- Player Comparison for Selection: Use dashboard insights to select the most consistent players for crucial matches.

-- Role Optimization: Assign roles based on strengths—e.g., power hitters in the top order, economical bowlers in pressure overs.

-- Performance Tracking: Monitor player metrics across matches to maintain consistency and identify early signs of underperformance.

##Conclusion

This project showcases my ability to analyze multi-dimensional cricket data using Power BI, uncover meaningful insights, and translate them into actionable strategies for selectors, coaches, and analysts. It demonstrates strong skills in DAX, data modeling, performance measurement, and dashboard storytelling—while solving real-world sports analysis challenges.
