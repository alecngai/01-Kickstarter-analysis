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
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; In May we have 111 successful fundraisers out of 166 and in June 100 out of 153. These two months have the highest success rate of 66.87% to 65.36% of success if launched in between these two months. This chart was generated by
taking successful fundraisers in that month divided by grand total of fundraisers in that month. This allows us to have a more objective view of the success launched in the months. Just because there are more number of successes in a specific month does not equate to that month being more successful,  we have to look deeper to see the amount of fundraisers and the percentage out of the total for that month to see the true success rate. By doing this we can see majority of the months have an above %60 success rate, while the lowest is in December. 

![Grand_total_vs_Launch_Date](https://github.com/alecngai/Kickstarter-analysis/blob/main/Resources/Grand_total_vs_Launch_Date.png)
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; Here we can see majority of the fundraisers are launched April to August, with May and Jun being the most, we can see that because there is more fundraisers the amount of successes will also increase. You can confirm this by comparing this chart with the first chart "Theater Outcomes Based on Launch Date", this graph has an extremely familar trend as the successful trend in that chart. That is why it is important to look at the "Percentage of Success vs Launch Date" rather than just the amount of success to avoid biases from the total amount of fundraisers. 

### Analysis of Outcomes Based on Goals

![Outcomes_vs_Goals](https://github.com/alecngai/Kickstarter-analysis/blob/main/Resources/Outcomes_vs_Goals.png)
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; This chart is created by filtering the data by subcategory *"Plays"* from the sheet *"Kickstarter"*, to create a new table, this table consists of the following columns: *Goal Range, Number Successful, Number Failed, Number Cancelled, Total Projects, Percentage Successful, Percentage Failed, Percentage cancelled*.  

_**Goal Range**_ - From less than 1000 to greater than 50,000 by increments of 5,000 \
_**Number Successful**_ - Number of successful fundraisers in that goal range, using COUNTIFS to check if successful, is in Plays subcategory and in goal range. \
_**Number Failed**_ - Number of failed fundraisers in that goal range, using COUNTIFS to check if failed, is in Plays subcategory and in goal range. \
_**Number Cancelled**_ - Number of cancelled fundraisers in that goal range, using COUNTIFS to check if cancelled, is in Plays subcategory and in goal range. \
_**Total Projects**_ - Sum of Number of Successful, Failed, and Cancelled fundraisers, excluding Live fundraisers \
_**Percentage Successful**_ - Percentage Succesful, calcualted by Number of Succesful divided by Total projects \
_**Percentage Failed**_ - Percentage Failed, calcualted by Number of Failed divided by Total projects \
_**Percentage Cancelled**_ - Percentage Succesful, calcualted by Number of Failed divided by Total projects  

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; The main objective of this chart is to determine wether setting a specific goal price will affect the success of the fundraiser. We can see the most successful fundraisers (75.81% to 72.66%) are set with lower goals of less than 1,000 to 5,000, except for the range of 35,000 to 45,000, which also has a high success rate (66.67%). This chart takes into account the number of successful fundraisers divided by total projects to determine a percentage of successful fundraisers.  It is clear that the percentage successful,is also affected by the amount of fundraisers,  we can see that there are a total of 720 Plays in the goal range of 0 to 5000, while only 9 in the range 35,000 to 45,000. Roughly 2 in 3 fundraisers are successful when they set their goals to 35,000 to 45,000, however, the sample data of only 9 plays is quite low so the number could be biased. 
 
![Goals_Based_on_Outcome_for_Theater](https://github.com/alecngai/Kickstarter-analysis/blob/main/Resources/Goals_Based_on_Outcome_for_Theater.png)

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; If we look at this next chart which is the same as previous except it is filtering by Theater we can still see the same hypothesis stands,  however we must take note the the amount of fundraisers changed from 9 to 15 for the range 35,000 to 45,000. We can concluded that there is some sort of trend as the Percentage Successful actually increased if not stayed the same for these ranges from 66.67% to 75%.00,  however,  due to the small amount of fundraisers, the affects of a single fundraiser can affect this percentage of successful which could artifically inflate this value giving us a false conclusion to our hypothesis. 


![Goals_Based_on_Outcome_for_All](https://github.com/alecngai/Kickstarter-analysis/blob/main/Resources/Goals_Based_on_Outcome_for_All.png)

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; Now we look at all the fundraisers as a whole, disregarding what category they belong too, we can see the trend of the lower the amount the higher the success rate, it averages out around 45.30% from 5,000 to 45,000. Then drops to low 28.57% to 16.37% from 45,000 to greater than 50,000. We can conclude that the lower the goal the higher percentage of success, anything greater than $5,000 will have a lower rate of success and is not worth the risk. If Lousie does have a high risk tolerance, then we can recommend her to set the goal of between 35,000 to 45,000 as it is still the highest average of 47.27% to 48.84%. We can also see a linear trend of when the goal becomes larger, it is porportional to fundraisers being cancelled. 
 

### Challenges and Difficulties Encountered

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; For the first analysis, I had issues splitting the count of outcomes on the pivot table into different fields of "successful", "failed" ,"canceled",  and "live". I finally figured it out through trial and error by putting the outcomes in both columns and values. Another issure I encounter was trying to generate the "Percentage of Success" column. I first tried to do it by adding another outcome to the value and setting it to percentage of rows, it does work, however it makes the pivot table unsightly and unorginized. I then tried to add a calculated field, however, altough outcomes was a field, its subfields of successful,  failed, canceled and grand total did not show up, thus it did not allow to me make the proper calculations with the fields I was given in the options. I decided on a fool proof method of creating a table below it which linked the values, and using this new table generate a new column which calculates the percentage of success by taking successful fundraisers of that month divided by the grand total of that month. This way the filter will still work and affect both tables and charts, altough it is a bit redundant since I could had made a new column and reference the pivot table, I wanted more clean forumla, since I was not familar with the formula (GETPIVOTDATA), and did not want to further waste time when I already had a solution, altough a bit more elementary. However, if I had more time I would like to further explore different options to organically add a new column to my pivot table to do these types of calculations. Another solution was to create another field in the main kickstarter sheet, I did not want to do this as the sheet already has 21 columns of data and it would be redundant data, just wasting more space and efficency. In the future I would like to be able to have a more clean sheet with less redundant columns of data, and rather I would use more complex forumlas to extract data and allow me to be more efficent with a more organized workflow. 


&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; For the second analysis the challenge was the tedius nature of this data collection, I tried my best to smoothline the experience by adding static fields to allow me to drag and expand the forumlas over different columns so I could save time as I wanted to do this for categorys "Play", "Theater" and every category combined. I used find and replace, to replace successful into failed and cancelled to save my time of manually editting each formula for each field. The next challenge was dealing with this data, since there was not enough fundraisers for "Plays" and "Theater" for the goal range of 35,000 to 45,000,  I took the result of the percentage of success with a grain of salt, as one or two successful fundraisers could heavily skew the percentage of success making it seem like a more enticing option for Louise. This is why I chose the route of looking at multiple different categories and over acrching data so I could try to understand the trends better.



## Results

- What are two conclusions you can draw about the Outcomes based on Launch Date?
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; First conclusion is that the best months to launch your fundraiser is May and June, as grants the highest percentage of success out of all the months. The second conclusion is to avoid Decemeber, this was the lowest out of all the months. We can also see that the number of successes is porportional to the number of fundraisers, so we can see that most fundraisers are laucnhed between April to August, however with the trend we can conclude that the best option for Louise is to launch in May, as it has the highest success rate, and to avoid december. 

- What can you conclude about the Outcomes based on Goals?

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; We can conclude that the lower the goal, the higher rate of success, there are some outliers for "Play" and "Theater" where it is also successful to set your goal range to be 35,000 to 45,000. However, the limited amount of fundraisers makes this data biased and not a long run average. We would recommend Lousie if her main goal is a succesful fundraiser then a lower goal is the best, if she has a high risk tolerance and needs more money then the next option would be to avoid anything between 10,000 to 34,999 but to set the goal from 35,000 to 45,000 as it is still a decent chances of successe compared to the rest of the goal range amounts. 

- What are some limitations of this dataset? What are some other possible tables and/or graphs that we could create?

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;  If I had more time I would look into how the duration of the fundraiser affected it's outcome, in addition to using the country column to see in which country is it best to lauch your fundraiser. There are some missing data that would be very beneficial,  for example, how many people attended the fundraiser, vs people who pledged money. This way we can see how enticing the fundraiser itself was. The two analysis we were chosen to do was based on launch date and goal. It would also be important to look at all the other fields, the staff_pick field, what are the criteria for a fundraiser to be a staff pick? and what does this true or false value mean in regards to the success of a fundraiser? Also what does spotlight mean, what does this column have to do with the success of the fundraiser? There are many data points missing, like the cost of setting up the fundraiser, maybe a more expensive fundraiser could mean more successful? Or prehaps more people who attended as well combined with amount spent on the fundraiser. It is common sense a lower goal is easier to reach thus has a higher success rate, there are outliers in the 35,000 to 45,000 range, however not much data on these fundraiser are collected and the population size is too small and has the chance to be biased. For launch date, it is insightful, but the key to a succesful fundraiser does not just rely on when it was launched, there are many more factors to take into consideration. What complexes people to first come to your fundraiser, second is how do you get the people to pledge to your fundraiser. Working backwards from these two questions gave me insight in the direction I would had like to take this analysis. First is the class of people and their income, it makes sense to have a successful fundraiser it is important to invite weathy people as they have the most potential for generous donations, or you could take the volumn approach and aim for lots of people to attend your fundraiser, but then you run into the issue of cost, the more people means bigger venue, food, entertainment, and money. Next is how to get people to pledge, it would be useful to find out why each pledge was made, was it common interest, pity, common friend, kindness, tax write off or any other option, it would help you understand the main majority for why people pledge to fundraiser and cater to those individuals.

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;  Another limitation is the fictional client Louise, we do not know her intent. We do know she wishes to compare her play's outcome to others, and have more insight from launch data and goal range. However, we do not know what she wishes to achieve with this information, if for example we knew her the amount she needed to raise, or the time constraints of her future fundraiser, does she want to just have an succesful fundraiser or to have a succesful fundraiser and have lots of money raised, it was not clearly described to us when taking into consideration the analysis. In the end it was an interesting data set and we can recommend based on what we know for Louise to start her next fundraiser in May and to set her goal range low if she is aiming for sucess.