## Run
First run `pip install scrapy`
### Run the spider:

- Set `DEBUG = False` in `recipescrape/spiders/recipes.py`
- Run `scrapy crawl recipes`

### Run the spider w/ minimal logs with count of items scraped and pause/resume-ability:

- Set `DEBUG = True` in `recipescrape/spiders/recipes.py`
- Run `scrapy crawl recipes -L WARN --logfile=scrapelog.txt -s JOBDIR=recipes/spider-1`

## Extras

### Spider to extract all the nutrient names:

- Run `pip install pandas`
- Make sure `DEBUG = True` in `nutrient_list.py`
- Run `scrapy crawl nutrients -o nutrients.csv -L WARN -s JOBDIR=nutrients/spider-1`
- Outputs 'items_count', 'nutri_count', 'nutri_list', 'url' in `nutrients.csv` in which the last row contains the unified list of nutritients found so far.

### Combine CSV files generated

- There are many ways to combine CSV files, a sample python file `/extras/combine_csv.py` is included for quick reference
