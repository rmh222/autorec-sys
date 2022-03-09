# Week 4 README file

## Code Description: 
The code used for web crawling TheNewYorkTimes website can be found in the Week4-CrawlingWithSelenium jupyter notebook file. In this file I designed a number of python functions to use the selenium library to access the html contents of a given url containing the results of a search for a specific tag(in this case technology tag). The driver simulates a person scrolling through the webpage and thus can activate the automatic load more function in the webpage. The code then uses the BeautifulSoup library to parse the html data and extract all the articles in the page as well as the rest of the search result pages. 

There are functions for all of the following tasks: 

* A function that finds the last loaded article in the page and moves the pointer to that element on the page using the driver by scrolling down. 
* A function that moves up a fixed distance in small intervals to simulate the movement of a human scrolling and give time for more articles to be loaded onto the screen 
* Lastly a function that uses the two previous functions to simulate the movements of a person scrolling all while checking if the last element previously loaded is the same as the current last element loaded (indicating the last article has been reached).  

The program then extracts all articles in a page by parsing the html content and retrieving section tags or div tags with specific keywords in the class attribute that I found while inspecting the website to be present in all articles. 

The program then prints the results of the webcrawling to csv files. Then it reads in the csv file created and stores it as a dataframe object. Finally it iterates over all the links in the dataframe and downloads them onto the device in the folder named images. 


The other jupyter notbook file called Week4-ImageClassificationWithCLIP uses the downloaded images and the library CLIP to classify all images into one of 5 categories that I determined from inspecting the images. 
