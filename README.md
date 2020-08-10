# Google_Email_Scraper
Scrape emails from a google search query. Using Scrapy open source scraping software with regex for finding emails, within PANDAS for easy CSV output.

This solution is adopted from previous work done at: https://towardsdatascience.com/web-scraping-to-extract-contact-information-part-1-mailing-lists-854e8a8844d2

Technical Descripion:
We use a google search API (https://github.com/MarioVilas/googlesearch) to allow a Google search query to be passed in to the scraper.
A regex(https://docs.python.org/3/library/re.html) function is created to find emails within web pages, with a common solution of images being scraped being taken out through dropping rows containing images ("@2x.png"). 
https://scrapy.org Is an open source website scraping resource, and the API used to scrape websites in this solution.
The final result is turned into a CSV file to any desired pathway as shown in the internal instructions. 

External Notes: 
This program may run slow the more you increase the number of desired site URLs to be scraped for two reasons. 
1) Google has a limit to the number of queries per second (https://developers.google.com/analytics/devguides/config/mgmt/v3/limits-quotas), so the number of queries is limited to avoid an error.
2) Many sites have scrape detection software that recognize the script as so. The program will still run, but . A possible solution not implemented here is to swap in random USER AGENTS/IP addresses(the legality of doing so is unknown as depends on individual website policies!), nonetheless the program still works just may be slowed down as result.
