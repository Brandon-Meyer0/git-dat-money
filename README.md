# Capstone Repository for "Git Dat Money" (GROUP 1A)

This is the project repository for the capstone of Cohort A Group 1 consisting of:

- [**Jahnavi Brahmbhatt**](https://github.com/Brandon-Meyer0/git-dat-money/tree/Jahnavi)
- [**Brandon Cancino**](https://github.com/Brandon-Meyer0/git-dat-money/tree/Brandon)
- [**Paniz Herrera**](https://github.com/Brandon-Meyer0/git-dat-money/tree/Paniz)
- [**Aidan Surowiec**](https://github.com/Brandon-Meyer0/git-dat-money/tree/Aidan)
- [**Ignacio Velazquez**](https://github.com/Brandon-Meyer0/git-dat-money/tree/Nacho)

### Repository Material

1) [IPython Notebook](https://github.com/Brandon-Meyer0/git-dat-money/blob/main/Capstone%20Group%201A.ipynb)
2) Presentation Slides

*Links to each of the team member's repositories as well as main notebook.

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

An important visual aid we can derive is whether or not a higher investment in the budget means a return of investment in profit.

![Budget-Profit](https://github.com/Brandon-Meyer0/git-dat-money/blob/Brandon/Budget-v-profit.png)

We can see that there definitely is a positive correlation between the budget and the profit a movie makes up to a certain extent, and that fund allocation in budget doesn't have to be incredibly high to make a strong profit, since many movies can be seen to work with a relatively small budget but earn more than five times their budget in profit.

After that, we dig into how the rating of the movie influences profitability, since it could determine many important factors such as determining whether to invest more in writing and directors to improve score, or produce a certain genre that is better rated than others (further visuals of this can be found in the Power Point or iPython Notebook).

![Profit-Rating](https://github.com/Brandon-Meyer0/git-dat-money/blob/Brandon/Profit-v-rating.png)

From the graph above we can see that there is also a correlation between the movie's rating and the profit it generates at the box office, and, that most movies that rate above average tend to make a profit as well. Accompanying visuals in this project will bridge the gap in logic between the popularity of the genre we recommend (how many films are produced and how well they rate) and the recommendation for producing a movie of the Adventure genre, since it tends to be the most profitable while also being averagely reviewed and not saturated in the market.
The rating 

And finally, we have our central visualization for one of the main insights we wished to give Computing Vision: the relationship between director experience and the rating the movie they direct has.

![Director-Exp](https://github.com/Brandon-Meyer0/git-dat-money/blob/Brandon/Avg-rating-v-Density-Director.png)

## Statistical Communication

The last visualization shown above leads us into the results of our statistical inference process. Our hypothesis is:

> **"The distributions of movie average fresh percentage for experienced directors are higher than for first time directors"**

This leaves us with the Null Hypothesis:

> **"The distributions of movie average fresh percentage for first time directors are statistically similar to experienced directors"**

We used a Mann-Whitney U test to analyze the aforementioned director data to arrive to the conclusion that **the movie average fresh percentage is significantly greater for movies that were directed by a director with experience of 2 or more movies**

Some greater insights we could gain from the linear regression are that:

> **As a director gains one movie in experience, the fresh percentage is expected to increae by 5%**
> 
> **For every fresh percentage point gained, we can expect to see box office revenue increased by $16.7K USD**

This would further indicate that director experience is a desirable characteristic to have when producing a movie, since every percentual increase in the movie's rating will be reflected in the box office's revenue, and see generated earnings for the company.

## Conclusions

This study was conducted within a week and, while most of our conclusions derive from our own analytical interpretations of the graphic representations produced, there was a statistic inference procedure conducted on the data related to directors in order to formally reject or accept our hypothesis as well as allow us to draw various conclusions that would derive into our recommendations. The three main points we would recommend Computing Vision are the following:

1) Hire experienced directors; having more than one movie under their belt tends to improve movie ratings, which in turn, improves profits.
2) Produce an adventure movie; not only is it the most profitable genre, but it also doesn't have a saturated presence in the market and tends to get average reviews.
3) Focus on Thai and Japanese Localizations; movies in this language tend to make money internationally, which would tell us to focus on the Asian market.

Furthermore, we produced some minor recommendations such as avoiding Documentaries, which tend to be highly rated and very produced but also tend to not make much of a profit in the box office.
