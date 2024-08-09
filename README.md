# Telecom-Call-Center-Performance-Dashboard
This repository contains a Power BI dashboard that visualizes the KPIs for a telecom call center.
The dashboard provides insights into various aspects of call center operations, including agent performance, customer satisfaction, and call resolution efficiency.

Features
Total Calls: Displays the total number of calls handled by the call center.
Resolved Calls: Shows the total number of calls that were resolved.
Call Answer Rate: Percentage of calls that were answered.
Average Talk Duration: The average duration of conversations between agents and customers.
Average Satisfaction Score: Displays the average customer satisfaction rating.
Calls per Agent: Visualizes the distribution of calls handled by each agent.
Resolved Call Rate: Percentage of resolved calls out of the total calls.
Average Speed of Answer: The average time taken to answer calls.
Calls by Topic: Distribution of calls based on various topics.
Call Volume by Day of Week: Analyzes the call volume trends over the week.

The dataset used in this dashboard includes the following columns:
caller id
agent
date
time
topic
answered (True/False)
resolved (True/False)
Speed of answer in seconds
Average talk duration
satisfaction
ratings

Data Source
The dataset was provided as part of a virtual internship through the Forage platform.

KPIs Implemented
Total Calls: The total number of calls.

DAX: Total Calls = COUNTROWS('Sheet1')
Total Resolved Calls: The total number of calls that were resolved.

DAX: Total Resolved Calls = CALCULATE(COUNTROWS('Sheet1'), 'Sheet1'[resolved] = TRUE())
Call Answer Rate: The percentage of calls that were answered.

DAX: Call Answer Rate = DIVIDE(CALCULATE(COUNTROWS('Sheet1'), 'Sheet1'[answered] = TRUE()), COUNTROWS('Sheet1')) * 100
Average Talk Duration: The average duration of all calls.

DAX: Average Talk Duration = AVERAGE('Sheet1'[Average talk duration])
Average Satisfaction Score: The average satisfaction score from customers.

DAX: Average Satisfaction Score = AVERAGE('Sheet1'[satisfaction])
Calls per Agent: The number of calls handled by each agent.

DAX: Calls per Agent = COUNTROWS('Sheet1')
Resolved Call Rate: The percentage of resolved calls out of the total calls.

DAX: Resolved Call Rate = DIVIDE([Total Resolved Calls], [Total Calls]) * 100
Average Speed of Answer: The average speed at which calls were answered.

DAX: Average Speed of Answer = AVERAGE('Sheet1'[Speed of answer in seconds])
Calls by Topic: The distribution of calls based on their topics.

DAX: Calls by Topic = COUNTROWS('Sheet1')
Call Volume by Day of Week: Analysis of call volumes on different days.

DAX: Day of Week = FORMAT('Sheet1'[date], "dddd")
Visualization: A line chart or bar chart showing call volumes.

How to Use
Clone the Repository:
bash
Copy code
git clone https://github.com/YourUsername/telecom-call-center-dashboard.git

Open the Power BI file:

Open the Call_Center_Performance_Dashboard.pbix file in Power BI Desktop.
Explore the Dashboard:

Use the various filters and slicers to interact with the data.
Explore different KPIs and visualizations to gain insights into call center performance.
License
This project is licensed under the MIT License - see the LICENSE file for details.

Contact
For any queries or suggestions, feel free to contact me at adarshupreti63@gmail.com
