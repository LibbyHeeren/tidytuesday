### Please add alt text to your posts

Please add alt text (alternative text) to all of your posted graphics for `#TidyTuesday`.

Twitter provides [guidelines](https://help.twitter.com/en/using-twitter/picture-descriptions) for how to add alt text to your images.

The DataViz Society/Nightingale by way of Amy Cesal has an [article](https://medium.com/nightingale/writing-alt-text-for-data-visualization-2a218ef43f81) on writing *good* alt text for plots/graphs.

> Here's a simple formula for writing alt text for data visualization:
>
> ### Chart type
>
> It's helpful for people with partial sight to know what chart type it is and gives context for understanding the rest of the visual. Example: Line graph
>
> ### Type of data
>
> What data is included in the chart? The x and y axis labels may help you figure this out. Example: number of bananas sold per day in the last year
>
> ### Reason for including the chart
>
> Think about why you're including this visual. What does it show that's meaningful. There should be a point to every visual and you should tell people what to look for. Example: the winter months have more banana sales
>
> ### Link to data or source
>
> Don't include this in your alt text, but it should be included somewhere in the surrounding text. People should be able to click on a link to view the source data or dig further into the visual. This provides transparency about your source and lets people explore the data. Example: Data from the USDA

Penn State has an [article](https://accessibility.psu.edu/images/charts/) on writing alt text descriptions for charts and tables.

> Charts, graphs and maps use visuals to convey complex images to users. But since they are images, these media provide serious accessibility issues to colorblind users and users of screen readers. See the [examples on this page](https://accessibility.psu.edu/images/charts/) for details on how to make charts more accessible.

The `{rtweet}` package includes the [ability to post tweets](https://docs.ropensci.org/rtweet/reference/post_tweet.html) with alt text programatically.

Need a **reminder**? There are [extensions](https://chrome.google.com/webstore/detail/twitter-required-alt-text/fpjlpckbikddocimpfcgaldjghimjiik/related) that force you to remember to add Alt Text to Tweets with media.

# Kaggle Hidden Gems

The data this week comes from [Kaggle](https://www.kaggle.com/datasets/headsortails/notebooks-of-the-week-hidden-gems?resource=download) by way of [Martin Henze (Heads or Tails)](https://twitter.com/heads0rtai1s). You can find some of their initial analysis in a [starter R notebook](https://www.kaggle.com/code/headsortails/hidden-gems-a-collection-of-underrated-notebooks).

This dataset is born out of the [Notebooks of the Week - Hidden Gems](https://www.kaggle.com/datasets/headsortails/notebooks-of-the-week-hidden-gems/discussion/317098) project.

> On Kaggle, many great Notebooks (aka "Kernels") can be found that have a large number of well-deserved upvotes. I'm publishing a weekly series of "Hidden Gems" in which I aspire to find and showcase underrated Notebooks on Kaggle in an effort to illuminate the diversity and creativity of our community.
>
> This series looks beyond those well-recognised works to find Notebooks which I personally like and which, somehow, didn't receive the attention that I think they deserve. My selections are always highly subjective; reflecting my own views and preferences. I have managed to publish an episode of "Hidden Gems" every week since the first post back in May 2020 and I hope to be able to keep this weekly schedule for the foreseeable future.

> ### **Welcome to this special Kaggle Community competition on the Hidden Gems dataset!**
>
> To celebrate 100 episodes of Hidden Gems we are hosting a Notebooks contest aimed at exploring all 300 Notebook entries and their (meta) characteristics. This is the place for you to showcase and practice your skills when it comes to exploratory data analysis, data visualisation, and crafting engaging narratives. Discover insights, publish your notebooks, and win cool prizes!
>
> As an introduction & AMA to this competition, we will be talking very shortly with [Sanyam Bhutani about the Hidden Gems series and the Notebooks challenge](https://youtu.be/o__J3bkp2PQ): Tune in at 6pm CET today on April 5th!
>
> See all the details below, and don't hesitate to ask for clarification. I hope you'll enjoy this competition.

To participate in the crossover challenge, please check out the [Kaggle page](https://www.kaggle.com/datasets/headsortails/notebooks-of-the-week-hidden-gems/discussion/317098).

### Get the data here

```r
# Get the Data

# Read in with tidytuesdayR package 
# Install from CRAN via: install.packages("tidytuesdayR")
# This loads the readme and all the datasets for the week of interest

# Either ISO-8601 date or year/week works!

tuesdata <- tidytuesdayR::tt_load('2022-04-26')
tuesdata <- tidytuesdayR::tt_load(2022, week = 17)

hidden_gems <- tuesdata$hidden_gems

# Or read in the data manually

hidden_gems <- readr::read_csv('https://raw.githubusercontent.com/rfordatascience/tidytuesday/main/data/2022/2022-04-26/hidden_gems.csv')

```

### Data Dictionary

# `hidden_gems.csv`

The file of interest is `kaggle_hidden_gems.csv`, containing the following columns:

-   `vol` and `date`: The consecutive number of the Hidden Gems episode and when it was first published.

-   `link_forum` and `link_twitter`: The hyperlinks to the Kaggle Forum post and Twitter post for the episode.

-   `notebook` and `author`: The hyperlinks to the Notebook itself, as well as to the Kaggle profile of the author.

-   `title`: The Notebook title as a string.

-   `review`: My brief review of the Notebook.

-   `author_name`: The name of the Notebook author as listed on their Kaggle profile at the time the episode was published.

-   `author_twitter` and `author_linkedin`: The social media links of the author, if listed on their Kaggle profile.

-   `notes`: Notes about special episodes.

### Cleaning Script
