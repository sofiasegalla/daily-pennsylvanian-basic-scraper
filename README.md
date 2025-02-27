# Daily Pennsylvanian Opinion Section Headline Scraper

This is a Python-based scraper that will take the top headline from the opinion piece of the Daily Pennsylvanian, and save it every day to a data file. Completed for CIS 3500 Homework 2, Part IV. 

## Overview

This repository takes the basic scraper template here: ![GitHub stars](https://img.shields.io/github/stars/username/repository?style=social)](https://github.com/jlumbroso/basic-git-scraper-template), which tracks the front page headline of the Daily Pennsylvanian, and changes the code to track the top headline of the daily opinion section. 

In order to avoid data downloading errors, the User-Agent header was also updated. 

## Modifications

The base url requested was changed from [https://www.thedp.com](https://www.thedp.com) to [https://www.thedp.com/section/opinion](https://www.thedp.com/section/opinion). It also changes the HTML element targeting, because the website links to the homepage headlines differently than opinion headlines. Instead of using an an 'a' tag with 'homepage' link, it uses the 'h3' tag with 'standard' link. 

## Usage

You can run the scraper with the following: 
```sh
python scraper.py
```
## Cron Syntax

The cron syntax "0 20 * * *" basically means the scraper will run once a day at 8:00 PM UTC. Breaking it down:

1. First number 0 = at the top of the hour (0 minutes)
2. Second number 20 = at 8 PM (using 24-hour time)
3. Asterisks * * * = every day, every month, all year round

The scraper is set to automatically kick off every evening at the same time.
