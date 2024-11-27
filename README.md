# Data Portfolio: Excel, SQL, Python, & Power BI

# Table of contents

- [Objective](#Objective)
- [Data Source](#Data-Source)
- [Stages](#Stages)
- [Design](#Design)
	- [Mockup](#Mockup)
	- [Tools](#Tools)
- [Development](#Development)
	- [Pseudocode](#Pseudocode)
	- [Data Exploration](#Data-Exploration)
	- [Data Cleaning](#Data-Cleaning)
	- [Transform the Data](#Transform-the-Data)
 	- [Create the SQL View](#Create-the-SQL-View)
- [Testing](#Testing)
  	- [Data Quality Tests](#Data-Quality-Tests)
- [Visualization](#Visualization)
  	- [Results](#Results)
   	- [DAX Measures](#DAX-Measures)
- [Analysis](#Analysis)
	- [Findings](#Findings)
	- [Validation](#Validation)
	- [Discovery](#Discovery)
- [Recommendations](#Recommendations)
	- [Potential ROI](#Potential-ROI)
	- [Potential Courses of Actions](#Potential-Courses-of-Actions)
 [Conclusion](#Conclusion)

#Objective
- [What is the key pain point?]
Create a dashboard to identify top UK YouTubers in 2024 for marketing campaigns.

- [Key Features:]
	- [Metrics: Subscriber count, total views, total videos, engagement rate.]
	- [Filters: Search by niche, engagement, and subscriber growth.]
	- [Tools: Use YouTube API for data collection and tools like Tableau or Power BI for visualization.]
	- [Automation: Regular updates for real-time insights.]
	- [This dashboard will help the marketing team make data-driven decisions and efficiently choose YouTubers for campaigns.]



## Subheader (Smaller header)

###### Smallest header you can write in Markdown 


2. How to make table of conent
# Table of content
- [Objective](#objective)

3. How to make pic 
![random-name-example](File path.png)

4. Code blockes, '''Language of the code I want to enter for example
'''sql 
/*

1.Define the variables
2.Create a CTE that rounds the average view per video 
3.Select the columns that are required for the analysis 
4.Filter the results by Youtube channels with the highest subscribers bases 
5.Order by net_profit (form highest th lowest)

*/


--1.
DECLARE @ConversationRate FLOAT = 0.02;		--The Converstion rate
DECLARE @ProductCost MONEY = 5.0;			--The product cost
DECLARE @CampaignCost MONEY = 50000.0;		--The campaign cost


--2.
WITH ChannelData AS (
	SELECT
		channel_name,
		total_views,
		total_videos,
		ROUND((CAST(total_views as FLOAT) / total_videos), -4) as rounded_avg_views_per_video
	
	FROM
		youtube_db.dbo.view_uk_youtube_2024
)

'''

5.Markdown table
| column1 | column2 | column3 |
|---|---|---|
|Product1|Product2|Product3|


