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

The initial list of movies is acquired from this [page](https://www.boxofficemojo.com/year/2010/?sort=openingWeekendGross&grossesOption=totalGrosses) of Box Office Mojo. It lists the movies in a tabular fashion, by year. As part of scope control, movies released only between 2010-2019 (inclusive) in U.S. is considered. Moreover, if a movie releases earlier internationally, this is not taken into account - only their Opening Weekend in U.S. matters. Lastly, all theatrical re-releases are discarded; as they potentially have a separate set of factors influencing their performance.  

Using the list of movies obtained, each movie's individual release page is scraped for additional information. An example of a release page can be seen [here](https://www.boxofficemojo.com/release/rl1265337857/).

Finally, the respective movie's [IMDB page](https://www.imdb.com/title/tt1201607/) is scrapped to obtain Budget information, as this was found to be missing on a majority of the Box Office Mojo release pages.

## Features & Target

The following features are organized from the scraped & parsed pages:  
  - Opening Weekend Theatres  
  - Release Date  
  - Studio Name  
  - Budget  
  - MPAA  
  - Genre  
  - Franchise  
  - Brand   
These features are imputed & engineered to arrive at a more accurate prediction.

The target variable is **'Opening Weekeng Gross'**.  

Additional information that was scraped and used for ancillary purposes included Release Link, Title, Domestic Gross, Max Theatres, Domestic to Opening Gross, Studio Link, Title ID, and Running Length.  

## Tools Used

  - Requests
  - Beautiful Soup
  - Pandas
  - Numpy
  - Matplotlib
  - Seaborn
  - Sci-kit Learn (subclasses: Metrics, Linear Model, Model Selection, Preprocessing, Pipeline)
  - Statsmodel
  
## Possible Impacts

The final model achieved a R<sup>2</sup> score of 0.73 and a mean absolute error of $6,558,159 on the hold out test set. To provide context, the mean of all values in the hold out set is  $13,201,940, with the maximum value going as high as $191,271,100.

Thus, the error is almost 50% of the mean value. Additionally, by looking at the residual graphs, the model over predicts for low value Opening Weekend Grosses & underpredicts quite a bit for huge blockbusters.   

Based on the results, a lot of additional work in terms of gathering more informative features is required to create a better model.  
Although **Budget** is quite an important feature, it is a proxy for other factors, such as the director, lead actor(s) & marketing spend - which play possibly plays an important role in drawing huge crowds for Opening Weekends.  

Lastly, it would be worth experimenting with separate models, based on binning the # of theatres the movie is getting released in on the opening weekend and/or if it is part of a franchise. 
