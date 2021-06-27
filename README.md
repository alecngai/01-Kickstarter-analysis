# An Analysis of Kickstarter Campaigns

## Overview of Project

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; In this project, we are analyzing kickstarter fundraising data (Kickstarter_Challenge.xlsx) to provide clarity on two main issues, 
outcomes based on launch date, and Outcomes based on Goals. The Kickstarter data consists of 21 Columns, and 4115 Rows of data. The quantitative variables are:
ID, Goal, Pledged, deadline, launched_at, Backers_count, Percentage Funded, Average Donation, Date Created Conversion,  Date Ended Conversion, Year. 
The Nominal Categorical variables are: Name, Blurb, Outcomes, Country, Currency, Category and Subcategory, Parent Category, Subcategory. 
The Binary Categorical variables consist of just spotlight. Using this data, we can extract a solution, and create charts to help our client visualize her solution to her problem. 

_**ID**_ - Numerical value identifier for the row of data.  
_**Name**_ - Name of the fundraiser  
_**Blurb**_ - A quick description of the fundraisier  
_**Goal**_ - Amount of money the fundraiser wishes to raise, \
_**Pledged**_ - Amount of money raised by fund raiser \
_**Outcome**_ - Consists of 4 states:  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; Cancelled - The fundraiser is cancelled  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; Failed - The fundraiser did not get enough money pledged to reach its goal  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; Live - The fundraiser is currently still on-going  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; Successful - The fundraiser has concluded and has more or equal amount of money pledged to their goal \
_**Country**_ - An two letter abbreviation of the country the fundraiser is currently located. 
_**Currency**_ - The type of currency the fundraiser is using for their goal and pledged amounts.  
_**deadline**_ - Unix timestamp as to when the fundraiser is due to conclude  
_**launched_at**_ - Unix timestamp as to when the fundraiser is created 
_**staff_pick**_ - Signifies if the fundraiser were favourited by the staff \
_**backers_count**_ - The amount of people who pledged to the fundraiser \
_**spotlight**_ - True if the fundraiser requires a spotlight, false if it does not \
_**Category and Subcategory**_ - Consists of two lists of main category and sub category to help sort the fundraisers into different groups \
_**Percentage Funded**_ - The amount of which the goal has been reached, rounded and converted into a percentage \
_**Average Donation**_ - The amount of which the average amount a backer will commit to a fundraiser, calcualted by pledged divided by backers_count \
_**Parent Category**_ - Seperated the two list of categories into a main parent category, consisting of: \
	Film & Video, Food, Games, Music, Photography, Publishing, Technology, Theater   \
_**Subcategory**_ - Seperated the two list of categories into a subcategory, consisting of: \
	Classical Music, Documentary, Electronic Music, Hardware, Indie Rock, Makerspaces,
Metal, Musical, Nonfiction, Photobooks, Plays, Pop, Radio & Podcasts, Rock, Shorts,
Space Exploration, Spaces, Tabletop Games, Television, Wearables.  
_**Date Created Conversion**_ - Converts launched_at, from Unix Timestamp to Human-readable date  
_**Date Ended Conversion**_ - Converts deadline,  from Unix Timestamp to Human-readable date  
_**Year**_ - Extracts the year from date created conversion.  
	
### Purpose

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; Our Client "Louise" recently had a fundraiser for her play "Fever", a story of love, 
friendship and sonnets. She had a goal of $2,885.00,  unfortunately by the time her fundraiser has ended (March 16, 2015) she could not reach her goal 
and was short $400.00. Due to this failure of only reaching 86% of her goal, she was interested in how other fundraiser campaigns fared in to relation 
to their launch dates and their funding goals. We will help visualize the campaign outcomes in relation to launch dates and funding goals, to assist Louise
in her decisions regarding her future fundraisers. By utilizing outcomes based on launch date, we can see the trend on when the most successful fundraisers were created.
In addition, by using outcomes based on goals amount, we can see how setting different amount of money for your fundraiser goal can equate to more successful fundraisers.  


## Analysis and Challenges

### Analysis of Outcomes Based on Launch Date

![Theater_Outcomes_vs_Launch](https://github.com/alecngai/Kickstarter-analysis/blob/main/Resources/Theater_Outcomes_vs_Launch.png)

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; This chart was created from a pivot table, the pivot table contains _Date Created Conversion_ in Rows, *outcomes* for columns, *count of outcomes* for values and *parent category, years* for the filter.
The data is then filtered in the parent category by "Theater". Here we are visualizing campaign outcomes ("successful", "failed", and "canceled") based on launch date, in parent category "theatre". 
The reasoning behind this is, Louise can see other fundraisers of similar genre and their outcomes based on when they launched their fundraiser. Here we can see in between May and June there are more than 100 successful 
fundraisers almost double the failed amount. We can see the trend of the most amount of fundraisers start in this period of time.  While the worst time would be in December, where there are similar amount of success and failed fundraisers that launch around this time. 

![Percentage_of_Success_vs_Launch_Date](https://github.com/alecngai/Kickstarter-analysis/blob/main/Resources/Percentage_of_Success_vs_Launch_Date.png)
In May we have 111 successful fundraisers out of 166 and in June 100 out of 153. These two months have the highest success rate of 66.87% to 65.36% of success if launched in between these two months. This chart was generated by
taking successful fundraisers in that month divided by grand total of fundraisers in that month. This allows us to have a more objective view of the success launched in the months. Just because there are more number of successes in a specific month does not equate to that month being more successful,  we have to look deeper to see the amount of fundraisers and the percentage out of the total for that month to see the true success rate. By doing this we can see majority of the months have an above %60 success rate, while the lowest is in December. 

![Grand_total_vs_Launch_Date](https://github.com/alecngai/Kickstarter-analysis/blob/main/Resources/Grand_total_vs_Launch_Date.png)
Here we can see majority of the fundraisers are launched April to August, with May and Jun being the most, we can see that because there is more fundraisers the amount of successes will also increase. You can confirm this by comparing this chart with the first chart "Theater Outcomes Based on Launch Date", this graph has an extremely familar trend as the successful trend in that chart. That is why it is important to look at the "Percentage of Success vs Launch Date" rather than just the amount of success to avoid biases from the total amount of fundraisers. 

### Analysis of Outcomes Based on Goals

![Outcomes_vs_Goals](https://github.com/alecngai/Kickstarter-analysis/blob/main/Resources/Outcomes_vs_Goals.png)
This chart is created by filtering the data by subcategory *"Plays"* from the sheet *"Kickstarter"*, to create a new table, this table consists of the following columns: *Goal Range, Number Successful, Number Failed, Number Cancelled, Total Projects, Percentage Successful, Percentage Failed, Percentage cancelled*.  

_**Goal Range**_ - From less than 1000 to greater than 50,000 by increments of 5,000 \
_**Number Successful**_ - Number of successful fundraisers in that goal range, using COUNTIFS to check if successful, is in Plays subcategory and in goal range. \
_**Number Failed**_ - Number of failed fundraisers in that goal range, using COUNTIFS to check if failed, is in Plays subcategory and in goal range. \
_**Number Cancelled**_ - Number of cancelled fundraisers in that goal range, using COUNTIFS to check if cancelled, is in Plays subcategory and in goal range. \
_**Total Projects**_ - Sum of Number of Successful, Failed, and Cancelled fundraisers, excluding Live fundraisers \
_**Percentage Successful**_ - Percentage Succesful, calcualted by Number of Succesful divided by Total projects \
_**Percentage Failed**_ - Percentage Failed, calcualted by Number of Failed divided by Total projects \
_**Percentage Cancelled**_ - Percentage Succesful, calcualted by Number of Failed divided by Total projects  

The main objective of this chart is to determine wether setting a specific goal price will affect the success of the fundraiser. We can see the most successful fundraisers (75.81% to 72.66%) are set with lower goals of less than 1,000 to 5,000, except for the range of 35,000 to 45,000, which also has a high success rate (66.67%). This chart takes into account the number of successful fundraisers divided by total projects to determine a percentage of successful fundraisers.  It is clear that the percentage successful,is also affected by the amount of fundraisers,  we can see that there are a total of 720 Plays in the goal range of 0 to 5000, while only 9 in the range 35,000 to 45,000. Roughly 2 in 3 fundraisers are successful when they set their goals to 35,000 to 45,000, however, the sample data of only 9 plays is quite low so the number could be biased. 
 
![Goals_Based_on_Outcome_for_Theater](https://github.com/alecngai/Kickstarter-analysis/blob/main/Resources/Goals_Based_on_Outcome_for_Theater.png)

If we look at this next chart which is the same as previous except it is filtering by Theater we can still see the same hypothesis stands,  however we must take note the the amount of fundraisers changed from 9 to 15 for the range 35,000 to 45,000. We can concluded that there is some sort of trend as the Percentage Successful actually increased if not stayed the same for these ranges from 66.67% to 75%.00,  however,  due to the small amount of fundraisers, the affects of a single fundraiser can affect this percentage of successful which could artifically inflate this value giving us a false conclusion to our hypothesis. 


![Goals_Based_on_Outcome_for_All](https://github.com/alecngai/Kickstarter-analysis/blob/main/Resources/Goals_Based_on_Outcome_for_All.png)

Now we look at all the fundraisers as a whole, disregarding what category they belong too, we can see the trend of the lower the amount the higher the success rate, it averages out around 51.44% from 5,000 to 45,000. Then drops to low 35.29% to 21.74% from 45,000 to greater than 50,000. We can conclude that the lower the goal the higher percentage of success, anything greater than $5,000 will have a lower rate of success and is not worth the risk. If Lousie does have a high risk tolerance, then we can recommend her to set the goal of between 35,000 to 45,000 as it is still the highest average of 54.17% to 56.76%.
 

### Challenges and Difficulties Encountered

## Results

- What are two conclusions you can draw about the Outcomes based on Launch Date?

- What can you conclude about the Outcomes based on Goals?

- What are some limitations of this dataset?

- What are some other possible tables and/or graphs that we could create?