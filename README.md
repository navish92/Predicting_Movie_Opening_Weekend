# Predicting Opening Weekend Gross for Movies

The following undertaking aims to predict the Opening Weekend Gross Revenue earned by movies released in the U.S. Market, using Linear Regression Modeling techniques.

## Description

In the movie entertainment industry, the Opening Weekend is comprised of Friday, Saturday & Sunday; regardless of whether the movie is released on a Friday or not of that week. This revenue number holds a very high significance due to a multitude of factors: 

  * Gross revenue earned on a movie's ticket sales is split between the movie theatres and the studios, based on complex agreements. But overall, studios get the maximum split % (typically 50%+) in the first week; and a majority of the first week sales happens on the opening weekend. 
  * Ratings for the movie are not available or highly publicized yet. A lot of opening revenue is incumbent on successful marketing & anticipation creation. Therefore, a blockbuster opening can help recoup a good portion of the movie costs.
  * A successful opening can help garner additional media attention that can further help buoy the movie for ticket sales.
 
This makes getting a better understanding of Opening Weekend Gross along with the various factors acting in tandem with it a highly important one.

## Data Used

**Sources:** [Box Office Mojo](www.boxofficemojo.com), [IMDB](www.imdb.com)  

The initial list of movies is acquired from this [page](https://www.boxofficemojo.com/year/2010/?sort=openingWeekendGross&grossesOption=totalGrosses) that lists the movies in a tabular fashion, by year. As part of scope control, movies released only between 2010-2019 (inclusive) in U.S. is considered. Moreover, if a movie releases earlier internationally, this is not taken into account - only their Opening Weekend in U.S. matters. Lastly, all theatrical re-releases are discarded; as they have a separate set of factors influencing their performance.  

Using the list of movies obtained, each movie's individual release page is scraped for additional information. An example of a release page can be seen [here](https://www.boxofficemojo.com/release/rl1265337857/).

Finally, the respective movie's [IMDB page](https://www.imdb.com/title/tt1201607/) is scrapped to obtain Budget information, as this was found to be missing on a majority of the Box Office Mojo release pages.

## Features & Target

The following features are organized from the scraped & parsed pages:
    * Opening Weekend Theatres
    * Release Date
    * Studio Name
    * Budget
    * MPAA
    * Genre
    * Franchise
    * Brand
These features are imputed & engineered to arrive at a more accurate prediction.

The target variable is **'Opening Weekeng Gross'**.  

Additional information that was scraped and used for ancillary purposes included Release Link, Title, Domestic Gross, Max Theatres, Domestic to Opening Gross, Studio Link, Title ID, Running Length.  


## Tools Used

## Possible Impacts
