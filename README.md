# Insight_Fellow_Background_Analysis

Insight Data Science Fellow Background Investigation, including Data-clean, wrangle and analysis

## Getting Started

Python and iPython Notebook are used 

### Prerequisites

The following Python Libraries are used in this investigation

```

1. regular expression (re)
2. requests
3. pandas
4. Beautifulsoup
5. folium and plugins
6. seaborn

```

## End to End Flow

```

1. Web Scraping for data collection
2. Data Wrangle and Retrieve the Geo-Location of fellows
3. API and Mapping (Using Free API)
4. Background Investigation

```

### Web Scrapping

I navigate the website of Insight, [Insight Data Science Fellows](https://www.insightdatascience.com/fellows) to retrieve the background information of Insight's Fellow. Insight's website is created on a structured way which leads to the convinient way to scrap the structured data

The basic workflow in this section is like the following:
1. Request the html data page by page => Utilize [Requests](http://docs.python-requests.org/en/master/)
2. Scrap the html data from pages in a structued way => Recommend [BeautifulSoup](https://www.crummy.com/software/BeautifulSoup/bs4/doc/) for html data
3. Manipulate String with [Regular Expression](https://docs.python.org/3/library/re.html)
4. Store the scrapped data into Dataframe format for the further wranggling => Use [Pandas](https://pandas.pydata.org/)

### Data Wrangle

Even with the web data successfully loaded into Pandas Dataframe, the scrapped data are sometimes very row. The row data in this web-scrapping action comes from two actions:
1. Missing Data or Null Data or Non-PhD Background
2. Miss Placement in the html

The row data will further requires cleanning and can be `reasonable` manipulated sometimes.
The basic cleanning workflow is like the following:

1. Identify the null data in the dataframe
2. To see if the mis-placed data could be fixed or manipulated
3. Save the data into new csv 

The workflow can be implemented with `Pandas` 

### API and Mapping (Free API)

In this section, we utilize [Folium Map](https://python-visualization.github.io/folium/docs-v0.6.0/) to have the interactive marker. In addition, we can also have the plugin function of `MarkerCluster` to have the interactive aggregated number of regional cluster shown in Map

#### Results

![Mapping](https://github.com/MacYeh/Insight_Fellow_Background_Analysis/blob/master/Results/Insight_Fellows_Mapping_USA.png)

### Major Background Investigation

In this section, we would use the following functions to have the background check of fellows:
1. `Pandas Apply` => This is similar as `SQL` `casewhen` to have the catogorized data
2. Visualize the distribution of the major => Use [Seaborn](https://seaborn.pydata.org/index.html)

#### Results

