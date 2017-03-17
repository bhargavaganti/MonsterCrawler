# monsterCrawl
**Description:** Crawls job description from monster.de
**Current Version:** 0.1
**Author:** Dynobo

## Install
Install dependencies:

* scrapy

## Configure
In `/spiders/jobs_spider.py`, in the class `linkSpider`, adjust the variable `url` in order to get the result for desired region and keywords.

## Run
First extract links to job offers from search results:

```
scrapy crawl links -a search=datascience -o datascience.json
scrapy crawl links -a search=itinstuttgart -o itinstuttgart.json
```

Second extract job descriptions:

```
scrapy crawl jobs  -a search=datascience -o datascience.xml
scrapy crawl jobs  -a search=itinstuttgart -o itinstuttgart.xml
```

## Changelog
**v0.1**
Inital Spider