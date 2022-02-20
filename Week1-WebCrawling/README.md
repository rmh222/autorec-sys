# Week 1 README file

## Code Description: 
The code used for web crawling a BBC news article can be found in the Frontrunner-Week1 jupyter notebook file. In this file I designed a python class called BBCWebCrawler that uses the requests library to access the html contents of a given BBC article's url. The code then uses the BeautifulSoup library to parse the html data and extract the desired parts. 

The class contains functions for all of the following tasks: 

* First the title of the article is extracted using the title tag nested in the head tag of the html contents. 

* After that, the article, containg all the images and text, is extracted. To do this I inspected the source code on the BBC webpage and found that all articles have an article tag nested in the body tag that contains everything in the webpage related to the article. So using BeautifulSoup the code extracts all "article" tags and their contents. 

* Next, to extract the subheadings, children "h2" tags are looked for withing the parent "article" tags. Then the text is extracted from them. 

* Similary, the hyperlinks are found in the article by extracting the "href" attribiute of children "a" tags within the parent "article" tags. 

* For images in the article, the code extracts both the description of the image and the link of the image. To do that it finds all "img" tags nested in the "article" tags and extracts the "alt" attribute for the name/description of the image, and the "src" attribute for the link. 

* Finally a function is used to extract the information fo the author of the article. Their name, image, link and social media. To do this i extract from the page all "p" tags whose class contains the word "Contributor". Then from there the code looks for "img" tags, hyperlinks and text. 

The program then prints the results of the webcrawling to txt and csv files.

## How To Compile:

* Ensure Jupyter Notebook is installed on your device then download the project. 
