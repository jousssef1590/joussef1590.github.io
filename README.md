# Data Portfolio: Excel, SQL, Python, & Power BI - Top 10 youtupers in UK 

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

# Objective
- What is the key pain point?

Create a dashboard to identify top UK YouTubers in 2024 for marketing campaigns.

- Key Features:
	- Metrics: Subscriber count, total views, total videos, engagement rate.
	- Filters: Search by niche, engagement, and subscriber growth.
	- Tools: Use YouTube API for data collection and tools like Tableau or Power BI for visualization.
	- Automation: Regular updates for real-time insights.
	- This dashboard will help the marketing team make data-driven decisions and efficiently choose YouTubers for campaigns.

This dashboard will help the marketing team make data-driven decisions and efficiently choose YouTubers for their campaigns.

## User story

As the Head of Marketing,
I want to use a dashboard that analyzes YouTube channel data in the UK,
so that I can identify the top-performing channels based on metrics like subscriber base and average views.

This will allow me to make more informed decisions about which YouTubers to collaborate with,
ensuring that each marketing campaign is as effective as possible.


# Data source
- What data is needed to achieve the objective?

  We need data on the top UK YouTubers in 2024 that includes their

- channel names

- total subscribers

- total views

- total videos uploaded

- Where is the data coming from? Kaggle[see here to find it](https://www.kaggle.com/datasets/bhavyadhingra00020/top-100-social-media-influencers-2024-countrywise?resource=download) as Excel file, and Youtube API to extract (subscribers, viewers) by python


# Stages
  
- Design
- Developement
- Testing
- Analysis

# Design
## Dashboard components required
- What should the dashboard contain based on the requirements provided?

To understand what it should contain, we need to figure out what questions we need the dashboard to answer:

1. Who are the top 10 YouTubers with the most subscribers?
2. Which 3 channels have uploaded the most videos?
3. Which 3 channels have the most views?
4. Which 3 channels have the highest average views per video?
5. Which 3 channels have the highest views per subscriber ratio?
6. Which 3 channels have the highest subscriber engagement rate per video uploaded?

For now, these are some of the questions we need to answer, this may change as we progress down our analysis.

# Dashboard mockup

Some of the data visuals that may be appropriate in answering our questions include:

1. Table
2. Treemap
3. Scorecards
4. Horizontal bar chart


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


