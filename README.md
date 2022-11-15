# 🏨 Online Hotel Web Search 
## Final Test of "BI Course" of MINDX TECHNOLOGY SCHOOL.

![image](https://user-images.githubusercontent.com/101379141/201806216-c1121751-d0b9-4c77-be8d-f6d8568d7d7a.png)

 <img src="https://user-images.githubusercontent.com/101379141/201035143-6f1af4fe-4169-4074-8287-6790d88803db.png" alt="Image" width="350" height="160">


# :books: Table of Contents <!-- omit in toc -->

- [:briefcase: Business Case](#briefcase-business-case)
- [:bookmark_tabs:Example Datasets](#bookmark_tabsexample-datasets)
- [:triangular_flag_on_post: The Requirement](#triangular_flag_on_post-the-final-test-requirements)
- [A. Data Exploration and Cleansing](#a-data-exploration-and-cleansing)
- [B. Analysis](#b-analysis)

- [📃 What can you practice with this case study?](#what-can-you-practice-with-this-case-study)

---

# :briefcase: Business Case


You are a candidate who wants to apply for the position of data analyst in the Marketplace team of company X. Company X's main product is the ABC website, which is a search and comparison website for large hotels in the world's top. . Team Marketplace is a large team of data analysts, data scientists, data engineers and software developers from many different countries. The team's mission is to provide data analytics to support the decision making of Company X.

Team Marketplace gives you the following headline, and reminds you that no solution is perfect, but the way you think and find new solutions is what matters most to them. The leader of the team advises you to come up with creative, but also practical solutions.

---

# :bookmark_tabs:Example Datasets

You are provided with daily performance data of 3 advertisers (advertisers) on ABC website in 2019 in 1 country (out of a total of many countries where ABC website operates)

Advertisers offer different prices to 3 different customer segments based on “time-to-travel” (TTT) time (measured by the number of days from the date a customer makes a hotel reservation until the date the customer booked a hotel room until the date of arrival). 
- Date of customer check-in at the booked hotel 3 customer segments based on TTT include:
  - Short : 0 – 14 days
  - Medium : 15- 60 days
  - Long : More than 60 days
  
- For each of the above advertisers, you are provided with the following parameters:
  - Clicks: the number of clicks that users of ABC website make
  - Cost: the amount the advertiser has to pay for the ABC website (according to the cost-per-click model)
  - Bookings: the number of hotel bookings made by users of the ABC website
  - Booking_rev: the amount that users spend on hotel bookings (ie gross revenue of each advertiser

<div align="center">

**Table marketplace_data_2019** 

<div align="center">
First 10 rows

---
|date|ttt_group|click_A|click_B|click_C|cost_A|cost_B|cost_C|bookings_A|bookings_B|bookings_C|booking_rev_A|booking_rev_B|booking_rev_C|
|:----|:-----|:----|:----|:----|:----|:----|:----|:----|:----|:----|:----|:----|:----|
1/6/2019|short|117272|68608|27152|113299|61987|21848|5664|2651|1311|864767|423745|197976|
1/6/2019|medium|96050|12415|137291|74761|7483|111740|3738|386|5343|565066|60799|812847|
1/6/2019|long|7060|9568|408676|3407|4796|327505|170|184|9813|27480|27867|1506297|
1/13/2019|short|109700|64097|25477|105743|57771|20462|5277|2467|1225|794086|387316|193915|
1/13/2019|medium|128847|16787|172639|101018|10201|140393|5049|526|6766|795529|80124|1020371|
1/13/2019|long|6473|9551|415381|3116|4827|336438|155|183|9944|24288|29623|1495347|
1/20/2019|short|132562|83019|31839|127954|75580|25714|6364|3189|1529|985840|500023|232915|
1/20/2019|medium|179077|22359|196475|141829|13653|157422|7071|706|7758|1136687|108024|1174109|
1/20/2019|long|5544|9485|422090|2628|4809|343933|131|180|9999|21043|27102|1579326|
1/27/2019|short|189934|118627|44164|182416|107422|35346|9117|4556|2120|1408158|719603|333481|

</div>
</div>



---

# :triangular_flag_on_post: The Final Test Requirements
## 1.	Market Trending
One of the indicators that the Marketplace team cares about is the conversion rate of users. In other words, they care about the percentage of users who can find the right hotel booking for their needs on the ABC website. One way to determine this is to calculate the booking conversion rate, which is calculated by dividing the number of bookings by the number of clicks.

- These are some suggestions:
  - Draw a daily booking conversion chart for the whole year of 2019 for ABC website
  - Do you notice any trends? What factors are driving this trend? (What are the main drivers of this trend?)
  - Can you guess which country these data are from? On what basis do you speculate?

## 2.	Advertiser performance
- One of your main tasks as a Market Data Analyst is to understand advertisers' performance, using datasets similar to the one you were provided with. From an advertiser's perspective:
  - Assuming every advertiser has a profit margin of 15% for all customer segments (short, medium, long), calculate the total profit of each advertiser for the year.
  - Based on the trends you've discovered, what recommendations do you have for each advertiser to improve their advertising campaigns in 202


# A. [Data Exploration and Cleansing](https://github.com/beto1810/Online_Hotel_Web_Search/blob/main/A.%20Data%20Exploration%20and%20Cleansing.md)


# B. [Analysis](https://github.com/beto1810/Online_Hotel_Web_Search/blob/main/B.Analysis.md)


# What can you practice with this case study?
- Python
  - pandas, numpy
  - cleaning, transforming.
  - unpivot, wide_to_long
  - import, save csv file. 
- POWER BI
  - Visualize
  - Analyze
  - Import CSV File and Transform data

