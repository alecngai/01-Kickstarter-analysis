# An Analysis of Kickstarter Campaigns

## Overview of Project

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; In this project we are analayzing kickstarter fundraising data (Kickstarter_Challenge.xlsx) to provide clarity on two main issues, 
Outcomes Based on Luanch Date, and Outcomes based on Goals. The Kickstarter data consists of 21 Columns, and 4115 Rows of data. The quantitative variables are:
ID, Goal, Pledged, deadline, launched_at, Backers_count, Percentage Funded, Average Donation, Date Created Conversion,  Date Eneded Conversion, Year. 
The Nominal Categorical variables are: Name, Blurb, Outcomes, Country, Currency, Category and Subcategory, Parent Category, Subcategory. The Binary Categorical 
variables consists of just spotlight. Using this data, we can extract an solution, and create charts to help our client visualize her solution to her problem. 

ID - Numerical value identifier for the row of data.  
Name - Name of the fundraiser  
Blurb - A quick description of the fundraisier  
Goal - Amount of money the fundraiser wishes to raise, 
Pledged - Amount of money raised by fund raiser 
Outcome - Consists of 4 states:  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; Cancelled - The fundraiser is cancelled  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; Failed - The fundraiser did not get enough money pledged to reach its goal  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; Live - The fundraiser is currently still on-going  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; Successful - The fundraiser has concluded and has more or equal amount of money pledged to their goal \
Country - An two letter abbreviation of the country the fundraiser is currently located. 
Currency - The type of currency the fundraiser is using for their goal and pledged amounts.  
deadline - Unix timestamp as to when the fundraiser is due to conclude  
launched_at - Unix timestamp as to when the fundraiser is created 
staff_pick - Signifies if the fundraiser were favourited by the staff \
backers_count - The amount of people who pledged to the fundraiser \
spotlight - True if the fundraiser requires a spotlight, false if it does not \
Category and Subcategory - Consists of two lists of main category and sub category to help sort the fundraisers into different groups \
Percentage Funded - The amount of which the goal has been reached, rounded and converted into a percentage \
Average Donation - The amount of which the average amount a backer will commit to a fundraiser, calcualted by pledged divided by backers_count \
Parent Category - Seperated the two list of categories into a main parent category, consisting of: \
	Film & Video, Food, Games, Music, Photography, Publishing, Technology, Theater   \
Subcategory - Seperated the two list of categories into a subcategory, consisting of: \
	Classical Music, Documentary, Electronic Music, Hardware, Indie Rock, Makerspaces,
Metal, Musical, Nonfiction, Photobooks, Plays, Pop, Radio & Podcasts, Rock, Shorts,
Space Exploration, Spaces, Tabletop Games, Television, Wearables.  
Date Created Conversion - Converts launched_at, from Unix Timestamp to Human-readable date  
Date Ended Conversion - Converts deadline,  from Unix Timestamp to Human-readable date  
Year - Extracts the year from date created conversion.  
	
### Purpose

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; Our Client "Louise" recently had a fundraiser for her play "Fever", a story of love, 
friendship and sonnets. She had a goal of $2,885.00,  unfortunately by the time her fundraiser has ended (March 16, 2015) she could not reach her goal 
and was short $400.00. Due to this failure of only reaching 86% of her goal, she was interested in how other fundraiser campaigns fared in to relation 
to their launch dates and their funding goals. We will help visualize the campaign outcomes in relation to launch dates and funding goals, to assist Louise
in her decisions regarding her future fundraisers. By utilizing outcomes based on launch date, we can see the trend on when the most successful fundraisers were created.
In addition, by using outcomes based on goals amount, we can see how setting different amount of money for your fundraiser goal can equate to more successful fundraisers.  


## Analysis and Challenges

### Analysis of Outcomes Based on Launch Date

### Analysis of Outcomes Based on Goals

### Challenges and Difficulties Encountered

## Results

- What are two conclusions you can draw about the Outcomes based on Launch Date?

- What can you conclude about the Outcomes based on Goals?

- What are some limitations of this dataset?

- What are some other possible tables and/or graphs that we could create?