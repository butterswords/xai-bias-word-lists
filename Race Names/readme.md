# Generating Names from Census Data and Inferring Race for counterfactuals

While fixing some bugs I discovered that the app can detect and pull out names but we don't have a way to create counterfactuals if someone wanted to test against it. Doing a little research I started down a path of creating fake names from real data. 

1. We start by pulling data from the US Census, to start, for the most frequent names: `Female First Names`, `Male First Names`, `Surnames`
2. We build a set of fake names by sampling each list and building a data frame combining first and last.
3. We currently use sex as a categorizer, recognizing that we're inferring it from the government list it was on and not human experience.
4. We can use `ethnicolr` to infer the likelihood of a name belong to a particular race based on historical data.
5. We turn this into a `.csv` file that we can generate counterfactuals from

### Data Origin
* [US Census 1990](https://www.census.gov/topics/population/genealogy/data/1990_census/1990_census_namefiles.html) to get names from Census.
* Future Opportunity - [DIME Race 1980-2014](https://dataverse.harvard.edu/dataset.xhtml;jsessionid=be9768bb2b804582647d35d80e62?persistentId=doi%3A10.7910%2FDVN%2FM5K7VR&version=&q=&fileTypeGroupFacet=&fileAccess=&fileSortField=date)

### Tools
* https://pypi.org/project/ethnicolr/ Use this to predict the race of the artificial names generated.
* https://github.com/appeler/dime_race Provides several useful Jupyter Notebooks to see how we could build our own counterfactuals with racial inference