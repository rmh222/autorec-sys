# Week 2 README file

## Code Description: 
The code used for web crawling Euronews website can be found in the Frontrunner-Week3 jupyter notebook file. In this file I designed a python class called webCrawler that uses the requests library to access the html contents of a given url containing the results of a search for a specific tag. The code then uses the BeautifulSoup library to parse the html data and extract all the articles in the page as well as the rest of the search result pages. 

The class contains functions for all of the following tasks: 

* A function that extracts all articles from all pages in the search result for a specific tag. This is done by extracting the urls of all the next pages and then running a concurrent threadpoolexecuter mapping each url of a page to a helper function that extracts all articles in that page. 
* The function that extracts all articles in a page by parsing the html content and retrieving section tags or div tags with specific keywords in the class attribute that I found while inspecting the website to be present in all articles. 
* Then another function again uses concurrent threadpoolexecuter to extract and retrieve the html contents of each article in the list of articles previously extracted. This function uses a helper function that extract img information, links, titles and text. 

The program then prints the results of the webcrawling to csv files.

After that since I faced some problems installing pytorch and tensorflow libraries, i could not imploy typical image classification tools, instead I used opencv to get the histograms of the images as well as other statistical information about the images such as the mean value of the pixels and the standard deviations. 
Then i ran the results through a kmeans clustering algorithm and attempted to cluster them into 2 groups. However the result was that lighter images were grouped together and darker images were grouped together. There is not much significance in this result. 

I also tried classifying the images using their texual descriptions by creating TFIDF vectors of all the words extracted from all the descriptions and then again usiong kmeans clustering to group them. In the end the data was divided into 2 categroies; russia related news and other cyber attack news. 

