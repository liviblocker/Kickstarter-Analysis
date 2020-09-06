# Kickstarting with Excel

## Overview of Project

### Purpose
Louise’s play <i>Fever</i> came close to its fundraising goal in a short amount of time. The purpose of this project is to compare how different Kickstarter campaigns fared in relation to their launch dates and their funding goals. By looking at the campaign launch dates of 1369 theatre projects and the campaign funding goals of 1047 plays, we were able to determine the optimum months to launch a campaign and the ideal funding goal.

Click the following to see the full analysis: [Kickstarter Challenge](path/to/Kickstarter Challenge.xlxs)

## Analysis and Challenges

### Analysis of Outcomes Based on Launch Date
In the analysis of outcomes based on launch date, we looked at 1369 campaigns for theatre projects, including plays, musicals, and spaces. We can see the number of campaigns that were successful, failed, or canceled from month to month based on data from 2009 - 2017.

Of the 1369 theatre campaigns, 839 (61%) were successful, 493 (36%) failed, and only 37 (3%) were canceled. In general, most of the campaigns were launched in May and June. 111 successful campaigns were launched in May, more than any other month. While May was also the month of the most failed campaigns, there is less variation in the number of failed campaigns from month to month. That pattern can be seen in the graph below.

![Launch_Date_Chart](https://github.com/liviblocker/Kickstarter-Analysis/blob/master/Launch_Date_Chart.png)

Whether a campaign was canceled or not does not appear to be correlated with the date of the launch.

### Analysis of Outcomes Based on Goals
In this analysis, we looked at 1047 successful, failed, and canceled campaigns for theatrical plays, based on the campaign funding goals. We looked at the number and percentage of successful, failed, and canceled projects.

The chart below shows the percentage of successful, failed, and canceled projects at each funding goal range.

![Outcomes_vs_Goals](https://github.com/liviblocker/Kickstarter-Analysis/blob/master/Outcomes_vs_Goals.png)

As the funding goals get higher the percentage of successful campaigns decrease until around the $30000 mark. Between $30000 - $44999 the percentage of successful campaigns begin to increase again, with 67% of campaigns with funding goals between $35000 and $44999 being successful.

Because there were no canceled projects in this data set, the percentage of failed campaigns inversely reflects the successful campaigns.

### Challenges and Difficulties Encountered
The biggest challenge in analyzing the data was thinking through the COUNTIFS function in Excel. The number of successful, failed, and canceled campaigns wasn't graphing properly, and it took me a while to realize that the way I had written the goal range part of the function didn't include an "equal to" part of the "greater/less than" signs. e.g. I had to change 

=COUNTIFS(Kickstarter!$D$2:$D$4115, ">1000", Kickstarter!$D$2:$D$4115, "<4999")

to

=COUNTIFS(Kickstarter!$D$2:$D$4115, ">=1000", Kickstarter!$D$2:$D$4115, "<=4999")

Once that had been figured out, the data came together.

## Results

<b>- What are two conclusions you can draw about the Outcomes based on Launch Date?</b>

In general, campaigns for theatre projects are successful, so Louise has the kind of project that does well on Kickstarter. The general success of her type of campaign could - in part - account for the quick success of her campaign. Additionally, most successful campagins are launched in May, so I'd recommend that she launch any future campaigns in May.

<b>- What can you conclude about the Outcomes based on Goals?</b>

Most of the successful campaigns have funding goals less than $5000 and even more successful campaigns have funding goals less than $1000. Most of the successful campaigns for larger budget productions have funding goals between $35000 and $45000. Depending on the production, a funding goal of either less than $5000 or between $35000 - $45000 have a good chance of being funded.

<b>- What are some limitations of this dataset?</b>

Looking at the outcomes based on launch date was difficult to come to firm conclusions, because we only had raw numbers. Without percentages it's difficult to determine whether the higher rates of successful campaigns in May is due to the overal higher rate of campaigns launched that month or if there is a correlation between the the launch date and the success of a campaign.

This is further exemplified by the outcomes based on goals analysis. Most of the successful campaigns fell between the funding goals of $1000-$4999 with 388 of the total 694 successful campaigns in that range. While most of the successful campaigns fell between the funding goals of $1000-$4999, that is also the range of funding goals for most of the projects, overall. As such, there is actually a higher percentage of successful campaigns with the funding goal less than $1000. That could not have been determined just looking at the numbers.

<b>- What are some other possible tables and/or graphs that we could create?</b>

Based on the limitation stated above, I would like to extend the Outcomes Based on Launch Date table to include percentages, but there is a lot of potential in other tables and graphs that we could create.

In order to best support Louise, ideally we'd have data for her play Fever to better compare the success of her campaign to others like hers. I'd like to analyze the outcomes based on the length of time to reach the funding goal and I'd look at the outcomes based on the difference between different types of theatre projects: musicals, plays, and spaces.
