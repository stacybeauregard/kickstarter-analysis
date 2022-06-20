# Kickstarting with Excel

## Overview of Project

A playright, Louise, is interested in creating a Kickstarter campaign to raise funds to produce her play, **Fever**. She has asked that we analyize data to help her set an appropriate goal and timeframe for her campaign.
### Purpose

We’ve been aiding Louise with her Kickstarter campaign for her play **Fever**. This assignment dives into similar campaigns for theater and more specifically, plays and how successful or not they are based upon the date of when the campaign was started, the goal amount set. We will be able to compare Louise’s start date and goal amount to these other campaigns to see if there is a likelihood of success or, based upon start date and goal set if she is likely to fail to reach her goal.
## Analysis and Challenges

### Analysis of Outcomes Based on Launch Date

Campaigns for theater were more successful if the Kickstarter began in late spring or early summer. The success rate then trickled down as campaigns began in the fall and winter months. An assumption could be made that people have less money to donate during the fall and wintertime due to holiday spending. 
We can also see that for a December launch there is a near 50/50 chance of having your goal met.
![Launch Date](https://github.com/stacybeauregard/kickstarter-analysis/blob/main/resources/Theater_Outcomes_vs_Launch.png)

### Analysis of Outcomes Based on Goals

After reviewing the data for “Outcomes based on Goals” campaign goals of $5000 or less have a higher chance of being successful, with a success rate of 70% or more. Campaigns with goals of $5000 to $25,000 are a near 50/50 split of success and failure.
![Outcomes Based on Goals](https://github.com/stacybeauregard/kickstarter-analysis/blob/main/resources/Outcomes_vs_Goals.png)
### Challenges and Difficulties Encountered

#### Challenge One
A challenge that needed to be overecome was converting the unix timestamp to readable format. We cannot create the Outcomes Based on Launch Date without this conversion. Initially, the data is a series of numbers that have no real meaning. I needed to decipher if this string of numbers was a date and created a new column Date Created Conversion. The formula used to convert to a readable date was '=(((J2662/60)/60)/24)+DATE(1970,1,1)' This formula divides the unreadable text by seconds, minutes, and then finally hours. It takes this number and references 1/1/1970 as the start date and counts up accordingly to input the correct date.
#### Challenge Two
The second challenge for me was calculating the percentages on the Outcomes Based on Goals line chart. I was having difficulty getting the chart to show percentages. I then remembered if I right click on just the Y axis titles I could then format these numbers to percentages with 0 decimal places.
 ![Percentage Challenge](https://github.com/stacybeauregard/kickstarter-analysis/blob/main/resources/Percentages_Formating.png)

## Results

- What are two conclusions you can draw about the Outcomes based on Launch Date?
1. Louise would be more likely to have a successful campaign if she set her launch date for the months of May or June.
2. Not only are campaigns more successful when startedn in May or June but more campaigns are started then as well.

- What can you conclude about the Outcomes based on Goals?
1. If Louise sets a goal of less than $5000 she is more likely to meet her campaign goal.

- What are some limitations of this dataset?
1. One limitation of the data is that we haven’t further defined which country the campaigns originate from. The campaign deadline has also not been taken into consideration. Perhaps the more successful campaigns set much longer deadlines enabling longer opportunity for donations.

- What are some other possible tables and/or graphs that we could create?
1. We could create another table to filter the goal amounts by originating country.
2. Another graph could show how many backers successful campaigns had, and then if these successful campaigns had backers that donated small or large amounts such as more than $100 versus the failed campaigns. 
