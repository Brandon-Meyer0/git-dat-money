# Capstone Repository for "Git Dat Money" (GROUP 1A)

This is the project repository for the capstone of Cohort A Group 1 consisting of:

- **Jahnavi Brahmbhatt**
- **Brandon Cancino**
- **Paniz Herrera**
- **Aidan Surowiec**
- **Ignacio Velazquez**

## Overview

This project aims to provide recommendations to the Computing Vision company, we aim to advise them - based on the readily available data, on their decisions to be able to grow the company with a succesful movie release. Contained in this repository you will find an iPython Notebook, graphs, and analysis of the data that was provided to us by our Flatiron teachers (**Nick McCarty** and **Julian Ward**) regarding the movie industry, as well as resulting business insights we have obtained from working with said information and arrived to as a conclusion of us tinkering with the data.

The iPython Notebook that we've been working on as a team, as well as the presentation and this README file are all related to our insights for the Computing Vision company. They are all based on the data obtained from the websites: Rotten Tomatoes, The Numbers, The Movie DB, and Box Office Mojo.


## Business Understanding

Our key business variable for this study is *profit*; we want to help Computing Vision in making the correct decision when looking to produce, and launch a succesful film that will make its budget back, and earn them revenue. 
The main questions we will be answering will be:

- **Does a big budget influence revenue?** 
  - This is to know the funds they should allocate to the project

- **Do good, average, or bad reviews affect the earnings?** 
  - This is to determine if a bad or average rated film can make a profit.

- **Will hiring experienced writers/directors for the project influence box office results?**
  - This is to find out whether the company should invest in hiring talent to make their investment back.

The stakeholders for our project are our clients at Computing Vision to whom we will address with the non-technical presentation.

## Data Understanding and Analysis

Our data comes from the data frames generated from the *.csv* and *.tsv* files provided to us by our instructors, sourced from the aformentioned movie rating websites (Rotten Tomatoes, The Numbers, The Movie DB, and Box Office Mojo). We also had access to a SQL database from IMDB that we were planning on using, but didn't end up using due to time constraints.

The data was formatted in a way were we could easily import it with the Pandas library and begin the clean-up process. In one case we had to specify the indices row. We opted to drop various columns where, we had an idea on how to use them, but decided the clean-up would be too time consuming for the tight schedule we had -such as the score field for the Rotten Tomatoes data frame, which we eneded dropping once we saw the variability it introduced by having an open rating system that went from having values out of 10, or out of 5 to having letter grades or even random letters. 

Other columns that were dropped during EDA include *synopsis*, *currency* (after all data was corroborated to be in USD), *dvd_date*, *top_critic*, *publisher* and *date* (of the review) due to relevancy of the data contained while *box_office* was dropped in one data frame due to it containing information for only about 1/5th of the total records in the data frame (340/1560). Other fields we wanted to use but didn't because of time include *runtime* (to analyze if it had anything to do with nature of the review or earnings) as well as maturity *rating*. Those fields could potentially yield interesting results if explored with more time.


-- DRAFT: This study was conducted within a week and, while most of our conclusions derive from our own analytical interpretations of the graphic representations produced, there was a statistic inference procedure conducted on the data related to directors in order to formally reject or accept our hypothesis 
