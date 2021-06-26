# An Analysis of Kickstarter Campaigns

## Overview of Project

	In this project we are analayzing kickstarter fundraising data (Kickstarter_Challenge.xlsx) to provide clarity on two main issues, 
Outcomes Based on Luanch Date, and Outcomes based on Goals. The Kickstarter datas consists of 21 Columns, and 4115 Rows of data. The quantitative variables are:
ID, Goal, Pledged, deadline, launched_at, Backers_count, Percentage Funded, Average Donation, Date Created Conversion,  Date Eneded Conversion, Year. 
The Nominal Categorical variables are: Name, Blurb, Outcomes, Country, Currency, Category and Subcategory, Parent Category, Subcategory. The Binary Categorical 
variables consists of just spotlight.

ID - Numerical value identifier for the row of data. 
Name - Name of the fundraiser
Blurb - A quick description of the fundraisier 
Goal - Amount of money the fundraiser wishes to raise,
Pledged - Amount of money raised by fund raiser
Outcome - Consists of 4 states: 
	Cancelled - The fundraiser is cancelled 
	Failed - The fundraiser did not get enough money pledged to reach its goal
	Live - The fundraiser is currently still on-going
	Successful - The fundraiser has concluded and has more or equal amount of money pledged to their goal
Country - An two letter abbreviation of the country the fundraiser is currently located.
Currency - The type of currency the fundraiser is using for their goal and pledged amounts. 
deadline - Unix timestamp as to when the fundraiser is due to conclude
launched_at - Unix timestamp as to when the fundraiser is created
staff_pick - Signifies if the fundraiser were favourited by the staff
backers_count - The amount of people who pledged to the fundraiser
spotlight - True if the fundraiser requires a spotlight, false if it does not
Category and Subcategory - Consists of two lists of main category and sub category to help sort the fundraisers into different groups
Percentage Funded - The amount of which the goal has been reached, rounded and converted into a percentage 
Average Donation - The amount of which the average amount a backer will commit to a fundraiser, calcualted by pledged divided by backers_count
Parent Category - Seperated the two list of categories into a main parent category, consisting of:
	Film & Video, Food, Games, Music, Photography, Publishing, Technology, Theater  
Subcategory - Seperated the two list of categories into a subcategory, consisting of:
	Classical Music, Documentary, Electronic Music, Hardware, Indie Rock, Makerspaces,
Metal, Musical, Nonfiction, Photobooks, Plays, Pop, Radio & Podcasts, Rock, Shorts,
Space Exploration, Spaces, Tabletop Games, Television, Wearables. 
Date Created Conversion - Converts launched_at, from Unix Timestamp to Human-readable date
Date Ended Conversion - Converts deadline,  from Unix Timestamp to Human-readable date
Year - Extracts the year from date created conversion. 
	
	



### Purpose

## Analysis and Challenges

### Analysis of Outcomes Based on Launch Date

### Analysis of Outcomes Based on Goals

### Challenges and Difficulties Encountered

## Results

- What are two conclusions you can draw about the Outcomes based on Launch Date?

- What can you conclude about the Outcomes based on Goals?

- What are some limitations of this dataset?

- What are some other possible tables and/or graphs that we could create?