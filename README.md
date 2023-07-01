# Movie-industry
What happened in the movie industry in the last 40 years?

## Situation + Task
Our situation. I'm a big fan of movies. I watch them every week. And every week, I participate in the movie club. 
So I am interested in two questions: what has happened in the film industry in the last 30-40 years? And the second question is what movie to watch tonight.

## Action
What did I do to solve these problems? I downloaded a dataset of 7,000 movies from 1980 to 2020 (roughly the top 200 movies from each year). The data is from IMDb.com. 
I opened this dataset in Power BI and made a dozen graphs. Then I opened it in PyCharm. 
Cleaned up the dataset, transformed the data a bit, filled in the gaps where there were many, and found correlations between numerical parameters. And at the end, built a trivial k-Nearest Neighbors model.

## Result + Reflection
What results did I get in the end? As for the genres, everything is mostly the same. There are local spikes (e.g., biographies were popular 3-4 years ago, but not anymore). 
But globally, over the past 35 years, the animation genre has become more popular due to the decreasing cost of computer power. 

The age limit is also almost unchanged. The only thing is that the PG-13 rating has become more popular because the ratings have become softer. 
And what used to be R is now PG-13 (e.g., The Hunger Games or The Avengers). Most likely, someone just lobbied for the change to gain access to a larger audience. 
Also, there is an interesting correlation; adult films are slightly more expensive.

Now let's move on to even more stable parameters. Movies, on average, are made precisely the same length as they used to be. The average length of a movie is one hour and 47 minutes.
By the way, an interesting correlation has been discovered. The longer the movie, the higher its rating.

Users give the film an average rating of 6.5 out of 10. And this value has stayed the same in the last 40 years. 
The film industry is over 100 years old, and people rate films relative to their contemporaries. That's why this value doesn't change. 
The rating correlates with the number of ratings. Maybe a good movie encourages people to give a score. But that's not certain. The correlation does not say what is the cause and what is the effect.

I answered the first question about what happened. Nothing.
Now I have to answer the second question: what movie to watch tonight?
For this, I used the k-NN model. This model works only in numerical values. So to find the closest (similar) movie, I used the length of the film, its rating, number of votes, age limit, and year of release. 
Are the answers I got valid? Unfortunately, not really. Because this model does not consider the director, the screenwriter, the main actor in the film, and the country in which it was filmed. 
These characteristics are hard enough to digitize. I need likely use a more complex model to account for these characteristics (Decision Tree or Neural Network).
