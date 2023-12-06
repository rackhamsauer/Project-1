# Project One: Successful Movie Analysis

This is a group project for UC Berkeley's Data Analysis and Visualization bootcamp. By looking at a dataset, we studied various factors in determining possible correlations for critically successful movies.

The research of our analysis came from thinking about movies and questions arising if certain aspects could significantly impact if a movie is more statistically likely to be successful. Specifically, we looked to for trends within genre, audience approval, intended audience, revenue, and directors.

## Demystifying the Genre-Rating Myth: A Data-Driven Dive by Michéal McCloskey

Intrigued by thoughts of a connection between movie genres and ratings, I embarked on a statistical deep dive through a vast IMDB-like dataset of movies from the 2010’s. Armed with freshly learned skills of T-tests and P-values, I probed for correlations, tested hypotheses, and even employed the mighty linear regression. Yet, after much analysis and chart-gazing, I discovered a surprising truth: that there doesn’t appear to be any  grand, overarching correlation between genre and rating.

Instead, a curious pattern emerged. Movies with the highest ratings often held a secret weapon: scarcity. The most lauded films were those with the fewest logged ratings, most surprisingly War and Biography movies, suggesting a passionate but niche audience. This counterintuitive finding challenges the notion of genre-driven ratings and invites a deeper exploration of factors beyond genre that shape our movie experiences.

## Audience Approval and Critical Acclaim by Stacie Sauer-Rackham

To determine if Audience approval impacted the critical acclaim of movies, I decided to examine if correlation existed between these factors. To do this, I narrowed the data to only include movie ratings that were higher than 7.0 our value for critical acclaim. Then I sorted the data in multiple ways using group bys and binning to get familiar with the data. Then I used a .corr() function and calculated a p-value with the independent t test to determine if correlation existed. The corr() function returned a value of .68 and the p-value was an extremely small number 3.70810065329775565e-6 to the 6th power which was less than 0.5. These indicated that the correlation was moderately strong. I found this very interesting because I have seen many examples of critics rating films high when audiences do like the film and the opposite has also been true. Audiences can love a film without the critic agreeing. I was surprised there was a moderately strong correlation where there were not many throughout the rest of the group. I created a scatter plot that easily conveys to stakeholders that there is moderately strong correlation.

I also created a binning box plot that would show where movies fit within both the critic ratings and the audience ratings. This helps tell the story of distribution and gives stakeholders a visual representation of the variability of most loved films.

## Intended Audience Ratings and Movie Ratings by Seren Frazin

With the dataset used, I looked into potential correlation between a movie's rating and its intended audience rating (PG, PG-13, R, etc). My hypothesis was that certain audience ratings would be statistically rated better than other audience ratings. To look at this on an analytical level, I first listed a count of audience ratings/certifications, noting that the particular dataset used had a marginally higher number of PG-13 and R ratings compared to the others.

Keeping this in mind, I then filtered out movies that had achieved critical acclaim (7.0 or higher) and made a pie chart out of that data for visualization. The results indidcated about 43% and 34% of the movies that had critical acclaim were rated R and PG-13 respectively. However, taking into consideration the fact that the majority of films in the list were those ratings, I needed to take a deeper look for any correlation.

I calculated and created a visualization of the average movie ratings for each certification. The results indicated relatively similar scores, meaning that regardless of certification, there was no clear indicator that one certification did any better than the rest in terms of movie rating.

A boxplot interestingly showed that G rated movies had the highest min. Among other results, this could potentially show that G rated movies will be less likely bomb critically in ratings. However, overall the visualizations and analysis shows very minimal to no direct correlation of intended audience and movie ratings.

## Revenue and Critical Acclaim by Juliet Messier

To determine if net revenue impacted the critical acclaim of movies, we decided to examine if correlation existed between these factors. To do this, we narrowed the data to only include movie name, movie rating, and net revenue. Then we used a .corr() function to determine if correlation existed. The function returned a value of 0.23456. This indicated that the correlation was weak because the value was below 0.5. After finding this data, we created a scatter plot that easily conveys to stakeholders that there is weak correlation.

To determine if gross revenue impacted the critical acclaim of movies, we examined if correlation existed between these factors. To do this, we narrowed the data to only include movie name, movie rating, and gross revenue. Then we used a .corr() function to determine if correlation existed. The function returned a value of 0.23964. This indicated that the correlation was weak because the value was below 0.5. After finding this data, we created a scatter plot that easily conveys to stakeholders that there is weak correlation.

Since there was weak correlation for both net revenue and gross revenue, we decided to do additional analysis on net revenue and gross revenue to see if there was anything else interesting about these factors. We decided to search for outliers for both net revenue and gross revenue. After conducting our analysis, we found 134 potential outliers for net revenue and 105 potential outliers for gross revenue. The largest outlier for both net and gross revenue was the movie Avengers: Endgame.

As a fun bonus, we searched to see if there were any outliers for critical acclaim. Interestingly, there were no outliers for critical acclaim.

## Director and Film Rating Study by Judith Cuellar

I looked for a correlation between Film Director and Film Rating. I wanted to know if a director's name had any influence on the film's rating. I believed I would find a strong correlation between a director's name and their film's rating.

I split the filtered data that we all worked on to account for films who had multiple directors. Instead of using a directors name, which is a qualitative variable, I used a quantifiable variable related to the directors name. The quantifiable variable was the number of films directed, in other words I looked at a Director's experience in the form of films directed. The more films produced the greater the experience a director had and the higher rating a film received.

I counted the number of films each director produced and measured the average rating of the directors films. I then looked for a correlation between years of experience and their average film rating.

I created a scatter plot and found the following measures:
- The correlation is 0.12
- The pvalue is 0.0002
- The r-squared is 0.015055628633488258
- The Regression equation is y = 0.09x + 6.43

The correlation of 0.12 indicates a weak positive correlation. The p-value shows that the correlation is significant. The R-squared indicates that only 1.5% of the film's rating can be explained by the amount of films directed.

I created a boxplot to understand the variability within each group. Variability decreased as the amount of movies directed increased. Most directors only directed one film, followed by directors who only filmed two or three films; only one director produced 7 films which is why there exists no variability in that category. The central tendency of each group stayed constant throughout each category and there are a few observable outliers.

For further analysis one can consider looking at a larger time frame to further credit a directors experience and background. One can also consider a directors popularity by looking at social media presence through hashtags related to a directors name.


## Installation

The project was written in Python and utilizes Jupyter Notebook with the following dependencies:

```python
  import pandas as pd
  from pathlib import Path
  import matplotlib.pyplot as plt
  import numpy as np
  import scipy.stats as st
  import seaborn as sns

```

## Resources

The dataset used originated from a combination of the following public datasets:

 - [Kaggle Dataset: Top 10,000 Popular Movies TMDB](https://www.kaggle.com/datasets/ursmaheshj/top-10000-popular-movies-tmdb-05-2023)
 - [Kaggle Dataset: 10,000 Data About Movies](https://www.kaggle.com/datasets/willianoliveiragibin/10000-data-about-movies-1915-2023)

 ## Authors

- [Judith Cuellar](https://github.com/judelou)
- [Seren Frazin](https://github.com/serenology)
- [Michéal McCloskey](https://github.com/meehal0203)
- [Juliet Messier](https://github.com/JuliWritesStories)
- [Stacie Sauer-Rackham](https://github.com/rackhamsauer)