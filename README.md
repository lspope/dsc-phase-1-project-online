# Microsoft Movie Studio Case Study
<p>A Flatiron Data Science Bootcamp Production

Prepared and presented by: Leah Pope (full time Data Science student)

Presentation URL: [here](PhaseOneProject_LeahPope.pdf)

Presentation Video URL:[here](external link)

<img src="./images/abstraction-movie-cinema-art-wallpaper-thumb.jpg"/></p>

# Business Problem
<p>Microsoft has decided to create a new movie studio (code name: "Clippy: Resurrection") and has enlisted the promising data science prowess of the Flatiron DS-FT-081720 Cohort to gather insights into the movie industry. 

You will be exploring what type of films are currently doing the best at the box office and will translate your findings into actionable insights that the head of Microsoft's new movie studio can use to help decide what type of films to create.</p>

# Data
<p>Datasets from three major movie information services (Box Office Mojo, IMDb, and Rotten Tomatoes) were used to conduct this analysis.</p> 

* bom.movie_gross.csv.gz
    * Contains the title, studio, release year, domestic, and foreign gross for select movies from the online box office reporting and analysis service, Box Office Mojo (by IMDbPro).

* imdb.title.ratings.csv.gz
    * Contains the average rating and number of votes for select movies in the IMDb online database of films. Ratings are provided by IMDb registered users.

* imdb.title.basics.csv.gz
    * Contains the title, start/release year, runtime minutes, and genres for select movies in the IMDb online database of films.

* rt.movie_info.tsv.gz
    * Contains the synopses, film rating, genre(s), director, writer, theater release date, dvd release date, box office, runtime, and studio for select movies featured on the Rotten Tomatoes review-aggregation website.

* rt.reviews.tsv.gz
    * Contains movie review details for select movies featured on the Rotten Tomatoes review-aggregation website. Movie review details include, review text, critic rating, Rotten Tomatoes-assigned "fresh" score, critic name and "top critic" status, review publisher, and review date. Ratings are provided by various movie critics.


# Questions Explored

## Question: What insights we can gain from gross amount?
a. How gross box-office trends over time.
b. What is the current gross box-office revenue to meet and beat?
### Data used:
* bom.movie_gross.csv.gz
### [Notebook](./notebooks/gross_amount_insights.ipynb)


## Question: Which studios are [Worthy Rivals](https://ideas.ted.com/how-having-the-right-kind-of-rival-can-help-you-thrive-in-a-changing-world/)?
ex: Which studios are currently releasing top-grossing movies?
### Data used:
* bom.movie_gross.csv.gz
### [Notebook](./notebooks/worthy_rivals.ipynb)


## Question: Do critics really count? 
What insights can be we gain by examining ratings from professional (and non-professional) movie reviewers and box-office revenue?
### Data used:
* rt.movie_info.tsv.gz
* rt.reviews.tsv.gz
* imdb.title.basics.csv.gz
* imdb.title.ratings.csv.gz
### [Notebook](./notebooks/do_critics_count.ipynb)


# Results
See individual Question Notebook for Exploratory Data Analysis (EDA) and Results.

# Conclusions
The analysis leads to the following recommendations as Microsoft Studios plans to enter the movie industry.

 *__Movie gross amounts are on an upwards trend.__ For the past nine years, domestic, foreign, (and worldwide) movie gross amounts are rising. Movies are still in demand which is good news for our client's new endevour.

* __Recent movie gross amounts dipped but recovered.__ More good news but also a slight warning to expect that yearly increases are a sure thing.

* __Set target gross goals wisely.__ If the client want to swing for the fences and release the next blockbuster, they should target the recent average gross amounts. If they want to start sensible and strong, they should target the recent median gross amounts.

*  __11 studios are the ones to watch in the current movie industry.__  Buenua Vista (BV), Warner Brothers (WB), Fox, Universal (Uni). Sony, Paramount (Par.) Warner Brothers/New Line (NL), Lions Gate Films (LGF), LG/S, HC, and Well Go USA Entertainment (WGUSA) are the studios to consider Worthy Rivals. Recommend that Microsoft Movie Studio prioritize competitor-focused research on these studios.

*  __No conclusive relationships identifed between critics' ratings (nor runtime) and box office amount.__  Recommend that the client not spend excessive effort/attention to critics. Sound advice for everyone.


# Next Steps/Future Work

Futher analysis into the following areas could yield additional insights.

* __Explore International market by Regions.__ Box Office Mojo appears to have datasets on International gross box-office revenue by Region. It would be worth-while to research if such data is available so that the client can produce content with specific Regions mind and identity Worthy International Rivals by Region.

* __Procure more data from BOM with both domestic and foreign gross.__  I would like to follow the same steps but on a larger dataset from Box Office Mojo that contains more domestic and foreign gross data.

 __Consider running "do critics really count" analysis again with more data.__ This data set is small. Only 340 movies had box office numbers. I did not check the time span on this dataset. Determine if there is more of this data on Rotten Tomatoes.

* __Clean up the messy critics' ratings.__ Maybe the Tomatometer is not all it is hyped up to be?  I could come up with a way to standardize the messy reviews from the critics. (Note: I do not suggest the critics are messy...just their rating systems.)

* __Check for faster changing trends.__ Create additional time breakdowns for top-grossing movie genres (last 5 years, last 3 years, last year) to uncover potental quicker moving trends.

* __Genre analysis.__ Use the dummy variable technique on movies that were assigned mult-genres (ex: Action, Adventure, Thriller) to get more detailed on which single genres are currently peforming well in the box ofice.

* __Explore "star-power".__ Explore the imdb.title.crew and imdb.title.principles datasets to see if there is a relationships between crew members (i.e., actors, writer, directors, producers) and high grossing movies. 


# For More Information
* See the full technical data analysis in the [Question 1](./notebooks/gross_amount_insights.ipynb) [Question 2](./notebooks/worthy_rivals.ipynb) and [Question 3](./notebooks/do_critics_count.ipynb) Jupyter Notebooks.
* Review the non-technical presentation [here](PhaseOneProject_LeahPope.pdf)
* View the non-technical presentation video [here](link)
* Contact the author [Leah Pope](https://www.linkedin.com/in/leahspope/)


# Repository Structure
```
--notebooks
----gross_amount_insights.ipynb
----worthy_rivals.ipynb
----do_critics_count.ipynb
--zippedData
----rt.movie_info.tsv.gz
----rt.reviews.tsv.gz
----imdb.title.basics.csv.gz
----imdb.title.ratings.csv.gz
----bom.movie_gross.csv.gz
--cleanedData
----bom.worldwide_gross.csv
```


