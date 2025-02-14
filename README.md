## What insights can be derived from the 2024 Customer Service Week (CSW) free bet campaign on sports activities to optimize future campaigns?
## Table of Contents
- [Project Background](#project-background)
  - [Objective](#objective)
  - [Overview](#overview)
  - [Goals](#goals)
  - [Deliverables](#deliverables)
  - [Thought Process](#thought-process)
- [Data Structure](#data-structure)
- [Executive Summary](#executive-summary)
- [Insights Deep Dive](#insights-deep-dive)
  - [First Time Deposit Trend Structure](#first-time-deposit-trend)
  - [Total Deoosit](#total-deposit)
  - [Gross Gaming Revenue](#gross-gaming-revenue-ggr)
  - [Bonus Wins](#bonus-wins)
  - [Player Retention](#player-retention)
  - [Free Bet Usage](#free-bet-usage)
- [Conclusions and Recommendations](#conclusions-and-recommendations)
  - [Conclusions](#conclusions)
  - [Recommendations](#recommendations)
- [Technical Details](#technical-details)
- [Clarifying Questions, Assumptions and Caveats](#clarifying-questions-assumptions-and-caveats)
  
## Project Background:
### Objective:
To analyze the impact of the CSW free bet campaign on sports betting activities, providing actionable insights to optimize future campaigns.
### Overview: 
I analyzed sports betting activities including YTD aggregated betting activities before the CSW free bet offer was given, betting activities during and one week after the campaign week, and compared players' betting patterns with real money and free bets, GGR trends, and first-time deposit trends related to new users and activation of inactive players. 
### Goals:
- Provided insights and recommendations tied to data findings to help marketing teams better align the next few months' marketing campaigns to the company’s goal.  
  - Mitigate risks such as negative gross gaming revenue 
  - Better tailor campaigns to reactivate inactive players, improve user acquisition, and retention, and ROI on commercial spending.
  - Built a high-level interactive dashboard to help Executives, and stakeholders monitor campaign KPIs.
### Deliverables: 
- I delivered tailored insights for top executives and marketing and commercial team stakeholders.
- Built an interactive Power BI dashboard with hierarchical row-level security providing various report access for stakeholders to monitor trends and KPIs.

## Data Structure: 

- *Players Segment*: This dataset provides the player IDs of all players offered a free bet and the amount of freebies given.

- *Jan_Oct8_ Activities*: Each record represents aggregated betting activities of players from January to October, a day before the free bet campaign, outlined bet counts, bonus stakes, bonus winnings, profit margin, stakes, and GGR, this gives us a YTD total of different KPIs

- *Oct_Activities*: This dataset provides insights into aggregating individual players' betting activities in October, including first-time deposit, and date, last deposit amount and date, GGR, withdrawal, stakes, and total deposit per player in October

- *Oct9-20_Activities*: Information about players' betting activities in campaign week and immediate post-campaign week, give insights into bet counts, bonus stakes, bonus winnings, profit margin, stakes, and GGR, help us to understand the betting patterns in the campaign week and track inactive players conversion

  <img width="485" alt="Data modelling" src="https://github.com/user-attachments/assets/25e04460-4cb4-41db-a671-9d89c7334b3b" />

Data cleaning, transformation, merging, and modeling were conducted in Power Query(Power BI) for granularity reporting and data visualization.

### Thought Process:
My deep domain knowledge in gaming, particularly in sports betting, shaped my approach to analyzing data insights most valuable to different stakeholders. The goal was to optimize future campaigns by catering to the needs of top executives, commercial managers, and marketing teams.  

This understanding influenced my data modeling and transformation process. I began by merging stand-alone datasets for Oct 9-13 (campaign week) and Oct 14-20 (post-campaign week) using the Append function in Power Query Editor. This allowed me to create a comprehensive view of player activities during and after the campaign.  

Next, I utilized advanced DAX queries to build visualizations, presenting high-level KPIs to offer top executives actionable insights. I then drilled down into granular trends such as registration patterns, first-time deposits, player attrition, and comparisons of behaviors between those using real money and free bets. These detailed insights catered to the specific needs of Commercial and Marketing managers, enabling a more nuanced understanding of player engagement and campaign impact.  

This structured and stakeholder-focused approach ensured that both high-level overviews and deep dives into critical KPIs were available, helping to inform strategic decisions for future campaigns.  

## Executive summary: 
The campaign spanned October 9th to 13th, during which free bets were distributed to both YTD active and inactive players, the company did **₦2.75M** GGR in the campaign week, and less than **2.5%** of the **431** FTDs recorded in the campaign week came from players offered free bets, which means the free bet drove new user acquisition and converted first-time deposits of **₦1.31M** during the campaign week.  

Most of the bonus bets that linger into the post-campaign week cost the company **62%** of the **-₦28.6M** GGR big loss recorded. October recorded the highest FTDs count and deposit value at **₦4,899,509**, a **46.5%** increase from August 2024. While the campaign successfully drove new user acquisition and FTDs, it resulted in a significant revenue loss due to lingering bonuses, To mitigate risk in the future, wagering requirements should be implemented and disallow bonus usage to extend beyond promotional week.

![KPIs Card](https://github.com/user-attachments/assets/99328f69-5923-4ba7-8508-2c9c11db77d5)

## Insights Deep-Dive: 

### First-time deposit trend
- FTDs exhibit a steady increase in the monthly trend, October recorded the highest FTDs of **₦4.89M**, a **114.8% MoM** increase.
- During the campaign week, **431** FTDs totaled **₦1.31M**, followed by a **64.89%** rise in FTD counts the next week, although there was no notable increase in the actual deposit value.
- Most FTDs, **99.64%** during the campaign and **99.24%** post-campaign were from new users, indicating limited impact from free bets given to existing players.

![Deposit trend](https://github.com/user-attachments/assets/c68564ed-8bd0-4c9e-8300-f54cfc4ef561)

![Alltime KPIs trend](https://github.com/user-attachments/assets/7f2dae1f-73c1-49d2-b8c5-19c8d2194d0b)

### Total Deposit:
- Campaign week deposits totaled **₦86.02M**, with a slight **-1.93%** decline the following week.
- FTDs accounted for only **1.52%** and **1.6%** of total deposits during and after the campaign week.


### Gross Gaming Revenue (GGR): 
- The company did **₦341,799,041** year-to-date GGR as of October 20, 2024.

- The campaign week generated **₦2.75M** GGR, while the post-campaign week recorded a huge **₦28.46M** loss.
- **62%** of the loss was linked to bonus bets that lingered into the post-campaign period.
- There’s a huge margin between the pre-campaign profit margin, campaign week, and post-campaign week profit margin.

![CampWeekVsPostCampWeek](https://github.com/user-attachments/assets/83f41018-4cdc-4c52-bd1c-cdf450299262)


### Bonus Wins: 
- The business incurred a free bet cost (Bonus Wins) of **₦1.19M** during the campaign week, which escalated significantly by **265.3%** in the following week, reaching **₦ 4.35 M**.

### Player Retention:
- Only **7.07%** of **136,257** free bet recipients players were active during the campaign week, with a **2.45%** retention rate in the post-campaign week.
- Overall company recorded a **3.44%** retention rate of free bet recipients in the post-campaign week.

![Player Retention](https://github.com/user-attachments/assets/5016afc2-57f5-453a-b6aa-eb34c794aff1)

### Free Bet Usage: 
- A total of **₦29M** in free bets was distributed to **136,257** recipients, but **92%** of recipients remained inactive or didn’t log in to access their free bet in the campaign week.
- Only **₦5.33M** free bets were used during the campaign and Immediate post-campaign week, with **77%** of the total bonus bet stake in the post-campaign week.

 ![Screenshot 2025-02-14 145354](https://github.com/user-attachments/assets/f9d25624-c1f8-4422-bc3c-aa45a00e6539)

## Conclusions and Recommendations:

### Conclusions: 
- *Success in New User Acquisition*: The campaign drove significant FTDs and new user registrations.
- *Revenue Loss*: Bonus bets contributed heavily to a **₦28.6M** loss post-campaign.

- *Low Conversion Among Free Bet Recipients*: Most free bet recipients did not deposit or engage meaningfully during the campaign.
- *Sustained Engagement Needed*: Retention rates among free bet recipients were very low, highlighting the need for better follow-up strategies.

### Recommendations:
- *Refine Target Audience*: Focus free bet offers on players segments with a higher likelihood of conversion, such as players with prior deposits or moderate activity levels and new users.
- *Optimize Bonus Structures*: Implement wagering requirements for bonus usage to mitigate potential revenue losses.
- *Diversify Incentives*: Introduce tiered rewards like loyalty points or cashback incentives to attract and retain players without excessive bonus costs.
- *Post-Campaign Follow-Up*: To encourage sustained activity, create personalized offers for new users who registered and deposited during and after the campaign.
- *Track ROI Metrics*: Use insights from the dashboard to refine audience segmentation and predict future trends. Monitor the profitability of free bets and other promotional activities more closely using tailored KPIs.

Click this link to interact with the [dashboard:](https://app.powerbi.com/view?r=eyJrIjoiZDZiNTQ0YWUtODY1YS00ZGEwLTllMWYtMDFkZWExMTZjZTFjIiwidCI6ImIxNjIzYzU5LWJjYmQtNGU1YS1iNTY3LTBkZjI0NGI5ODU0MyJ9)

![_CampaignAnalysisdashboard](https://github.com/user-attachments/assets/c8e0e386-dad6-47b1-abd7-977b736dde69)

## Technical Details: 
- *DAX Query*: Calculations for GGR, FTDs, free bet used, and given target and retention metrics were calculated for visualization writing advanced DAX.
- *Data Modelling*: Tables were linked through Power BI’s relationship manager, ensuring seamless data integration for reporting through Snowflake schema.
- *Data Visualization*: An interactive dashboard was created, choosing appropriate charts for different data points to provide actionable insights and real-time tracking of future campaign success.
- *Row Level Security*: Hierarchical access was implemented, granting tailored data access to the Executive, marketing, and commercial manager.

## Clarifying Questions, Assumptions, and Caveats
- One of the major caveats was the inability to distinguish between active and inactive players in the player segment table, with a record of each player offered a free bet and how much.
- Not having access to the previous month's existing players' activities, like GGR and stakes, deprived us of the opportunity to compare staking trends between regular week and campaign weeks and to know what effect the campaign has on existing users.

😄 😄 😄 💻 💻 💻
