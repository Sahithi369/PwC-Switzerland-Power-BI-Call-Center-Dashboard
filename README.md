# PwC-Switzerland-Power-BI-Call-Center-Dashboard
The present scenario case focuses on the call center trends. We analyze the amount of incoming calls, call agent performance, response time, call duartion, daily and hourly trends, including customer satisfication ratings. The dashboard defines key KPI's which impact the customer satisfaction as well as the productivity of the call agents. The purpose is to uncover potential ways of tracking efficency and enhancement.
# Background information of task
The digital revolution and our fast-changing world requires a skills revolution. And it’s not just about the digital skills. 
The skills revolution is about helping people build their digital awareness, emotional intelligence and creativity to fully participate in the digital future workplace — and it needs to start now.

At PwC, we are working with other organisations across the world, building on our work with clients and on upskilling our 276,000 people. Still, more must be done if we are to ensure everyone has the opportunity to learn, work and participate in the digital world. This is at the heart of our purpose.

We are enabling employees who are motivated to further accelerate their skills to do so by offering them a “career pivot” to become what we call “Digital Accelerators”. 
Accelerators rapidly deepen their skills in digital specialties, such as data, automation, AI, and digital storytelling by learning a variety of self-service tools and coding languages and applying these skills across our business.

We're happy you joined us, welcome to the team! Giulia is your manager and helps you through your upskilling journey in PowerBI - your step to become a true data jedi and Digital Accelerator. 
But wait no more, word spreads fast and an important client reached out to you to help him visualising their data. 
# Task:
It’s omnipresent: telecom marketing. Better price here. Better service there. Best for small businesses here. Best for young urbanites there. 
But what do customers really want? Our client, a big telecom company needs to know. This email just arrived for you:

Create a dashboard in Power BI for Claire that reflects all relevant Key Performance Indicators (KPIs) and metrics in the dataset. Get creative! 

Possible KPIs include (to get you started, but not limited to):-

1] Overall customer satisfaction
2] Overall calls answered/abandoned
3] Calls by time
4] Average speed of answer
5] Agent’s performance quadrant -> average handle time (talk duration) vs calls answered.
<img width="716" alt="image" src="https://github.com/user-attachments/assets/4e7ebbd7-42cf-4133-8796-7437cf82add1" />

DAX commands used:
Agent Performance Score = AVERAGE('Sheet1'[Satisfaction rating])

Avg_Satisfaction = AVERAGE('Sheet1'[Satisfaction rating])

Avg_Speed_of_Answer = AVERAGE('Sheet1'[Speed of answer in seconds])

Call Answer Rate = DIVIDE(COUNTROWS(FILTER('Sheet1', 'Sheet1'[Answered (Y/N)] = "Answered")), COUNTROWS('Sheet1'))

Calls_Abandoned = COUNTROWS(FILTER('Sheet1', 'Sheet1'[Answered (Y/N)] = "N"))

Total_calls_Answered = COUNTROWS(FILTER('Sheet1', 'Sheet1'[Answered (Y/N)] = "Y"))
