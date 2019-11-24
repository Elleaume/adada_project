# Terrorism perceived though western news

# Abstract

Since September 11 2001, terrorism has been in the headlines around the globe. A general fear reappears every few years as events labeled as "terrorist attacks" occur. Certain parties have gained in popularity in the past few years, often using the anxiety of "dangerous terrorists" as a pretext to defend anti-immigrant policies. Have terrorist attacks increased in the past years as we are lead to believe? or has the rate been more or less constant? Are foreigners or immigrants really more likely to commit these terrorist attacks? News coverage plays a big role in how we perceive these events, some events are debated and discussed during weeks, while others are never mentioned. We want to explore the rate and distribution of these attacks over the world, and dive into their news coverage in the western hemisphere.  

# Research questions

- Have the terrorist attack rates, motives, locations, changed over the past 50 years?
- Where do terrorist attacks occur?
- Who commit terrorist attacks and by what motive?
- How are is global terrorism depicted in some selected popular western newpapers? 

# Datasets

## Global Terrorism Database

This database is a collection of facts about terrorist attacks from 1970-2017. The facts cover location, date, motive, and who claimed the attack and a very large variety of other very specific metrics. 
https://www.kaggle.com/START-UMD/gtd

Also all the data from 1993 was lost during the digitalisation process. 


## All the news 
This database is a collection of news coverage from CNN, New York Times, Breitbart, Fox news, the Guardian, 
https://www.kaggle.com/snapcrack/all-the-news#articles3.csv 

After investigating all-the-news datset, we found out that the distribution in time of the articles was highly imbalanced and most of the data was dated from 2017 and 2016 with very few entries for earlier yeares. After a first fitlering of the articles using a sentence matcher on the titles, only 9 articles corresponding to a custom-build dictionary of words of interest on terrorism. Given that the dataset had to be cleaned further and that there were evidence of a lot of data not concerning our topic we decide to drop it. 

### New York Times articles

To construct a new dataset, we had to narrow down the diversity of publishers and chose to start using only New York Times articles. The New York Times provides a very robust Application Programming Interfaces (APIs) to enable computer applications to request informations on a large diversity of subjects. Article Search API retrieves headlines, abstracts and links to associated multimedia from 1851 to today and can be used to look up articles by keyword. To contrsuct a preliminary database, we used the keyword `terrorism` and data was returned in a  `JSON` format. 

New York Times data contains an abstract, date, headline, location when available, section, list of subjects, the url	and a word count.

### Limitations

The New York Times sets two rate limits per API, 4000 requests per day and 10 requests per minute, which can be limiting to construct a full database in a limited amount of time. However, we planned to enrich the database as time goes by using also more query keywords. 

Furthermore, limiting news coverage only to New York Times is clearly not as representative to western media in general even if we chose one of the most popular newspaper written in english. 

Because of this, in the furture we would also like to scrape articles from The Guardian as its Content API provides access to all the content the Guardian published as far back as 1999 but this would mean that the timespan we would have to consider would be from 1999 to 2017. 



