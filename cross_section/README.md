### Datasets information

Here is an information table for the dataset:

| name                     | description                                                 | size  | source                                                    | Features                                                     |
| ------------------------ | ----------------------------------------------------------- | ----- | --------------------------------------------------------- | ------------------------------------------------------------ |
| cities_brazil.csv        | Population of cities in 2023 Brazil                         | 18kb  | https://worldpopulationreview.com/countries/cities/brazil |                                                              |
| cities_us.csv            | Population of cities in United States                       | 37kb  | https://worldpopulationreview.com/us-cities               | Including population data in 2023, 2022, 2020 census, 2010 census |
| forbes-billionaires.csv* | The world's richest 2000 people in 2020 according to Forbes | 790kb | https://www.forbes.com/billionaires/                      |                                                              |
| forbes-global2000.csv*   | The world's largest 2000 firms in 2020 according to Forbes  | 118kb | https://www.forbes.com/lists/global2000/                  | Variables measuring the firm size: sales, profits, assets, market value |
|                          |                                                             |       |                                                           |                                                              |

*These two datasets are generated using the file ``webscrape_forbes.ipynb`` with the Forbes API.

### Instructions on fetching the data for use in a lecture

There are many different method of fetching and using the data.

In ``Python`` environment you can follow:

Step 1: find the url code by clicking the file -->> view raw -->> copy the url path

Step 2: paste the url path in the following code

```
import pandas as pd

url = "<Paste the url path here>"
pd.read_csv(url)                              # for csv files
```



