## Do I want to live in this city?

As a person who still doesn’t have a driver license, a major thing I need to research when moving to a new city is how good is its transit system. And after almost a year of living in the car country that is Texas, I can further attest to how big of an impact a city’s walkability, transit system and general urban planning have on my social life and mental health — especially when my favorite thing to do in the world is walking around with a little cold drink. As a result of that, I wanted to see how cities in the US and Canada stack up in terms of their walk and transit scores.

## Methodology

I scraped [walkscore.com](https://www.walkscore.com/cities-and-neighborhoods/) to get their data on walk and transit scores for 130 cities with at least 200,000 people. I still included the website's population data in my scraping, but I didn't end up using them since I later realized that they are outdated. 

I used pandas to slice the raw data into US-only and Canada-only datasets for futher analysis and visualization. I then mostly tried to count, rank and sort the individual datapoints for outliers or interesting trends. As a result of this, I also pulled Texas-only data from the US-only dataset to take a deeper look at the state because of an transit score outlier (Arlington). 

Here are the relevant files
 - [Analysis Notebook](https://github.com/ann2128/lede-project-2/blob/main/project-2-scraping.ipynb)
 - [Raw data from scraping](https://github.com/ann2128/lede-project-2/blob/main/walkable_cities.csv)
 - [US-only data](https://github.com/ann2128/lede-project-2/blob/main/us_only.csv)
 - [Canada-only data](https://github.com/ann2128/lede-project-2/blob/main/canadian_cities.csv)
 - [Texas-only data](https://github.com/ann2128/lede-project-2/blob/main/texas.csv)
 - [Below-average cities for walk score data](https://github.com/ann2128/lede-project-2/blob/main/bottom_walkscore.csv)

I then used datawrapper to make the two main charts. For the Texas chart, I also used datawrapper to create the visualization of the state so I could combine its svg file with the bar chart as a quick locator map. 

## Main Findings

### US
 - The average walk score is 48.7 for the 108 American cities included in walkscore.com's ranking. Sixty-seven of the cities have scores lower than this average. 
 - Chesapeake, Virginia's second-most populous city, has the lowest walk score of 21.3. On the flipside, San Franscisco, CA has the highest walk score of 88.7. New York City is in second place at 88. 
 - Also unsurprisingly, the top 10 cities for walk score are mostly in the Northeast, except for San Fransciso, Oakland and Miami. Meanwhile, the bottom 10 cities are in the South and Southwest, with four of them being in North Carolina alone!
 - For transit score, walkscore.com didn't have data for 7 cities. Among those with available data, New York City is unsurprisingly on top at 88.6, while San Franscisco is in second place at 77.1. Other cities in the top 10 list are also similar to those in the top walk score list, though Miami is out of the list.
 - Arlington, TX is at the bottom for transit score with 0.3, so there's no public transit in this city of close to 400,000. There are also two other Texas cities — Plano and Lubbock — in the bottom 10 cities for transit score. 
 - More on Texas: all 13 of the state's featured cities are have below-average walk and transit scores.
 
## Canada
 - The average walk score is 47.6 for the 22 Canadian cities included in walkscore.com's ranking. Fourteen of the cities have scores lower than this average.
 - The average transit score is 51.8 for the 22 cities, and 15 of them have lower scores. 
  - Vancouver — where I grew up — has the best walk score and second-best transit score. The other close competitor is Toronto, which is the biggest city in the country.

### New Skills

I was able to use the newly-acquired scraping skill for this project. I was also able to combine some Datawrapper charts together to create a more informative visualization by using other softwares.

### What Else To Try

I quickly realized that the population data that I could acquire through scraping was outdated and I didn't have time to pull the most recent one, so I wasn't able to do more analysis on that front. Walkscore.com also has transit and walk scores for the neighborhoods within each city, which could have allowed for an additional layer of analysis. 

In general, I think there are never-ending amount of things I could do more with scraping and data viz if I have more skill and time!
