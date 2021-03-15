---
layout: post
title:      "Creating a webscrapper with Selenium"
date:       2021-03-15 18:36:40 +0000
permalink:  creating_a_webscrapper_with_selenium
---

While getting ready for my Capstone project, I couldn't find the dataset I needed for my project. Therefore, I was desperately needing a way to extract data. 
I went through the lessons in module 1 to refresh my memory. However, I found that using beautiful soup was not what I needed as I could not access the data I was hoping to get. 

## Selenium 
I research the top 3 web scrapers online and came across Selenium. 
Selenium was created to automate your web browser. This includes going through HTML and CSS. It also has an advantage against beautifulSoup and Scrapy, because it is accessing the website like a normal user, normally it doesn't get block. 

## How to build your Web Scrapper 
### Installing Selenium 

First, we need to install Selenium. We need to go to anaconda's CMD and type the following code: 
```
pip install selenium 
```

Secondly, we need to download a driver, in my case, Chromedriver. If you are using a different web browser, then you need to download accordingly.  Once downloaded you need to put the file in a easy accessible folder, in my case
```
C:/Users/chromedriver.exe
```
### Importing Selenium 
Once installed, we need to import some of the libraries inside selenium.
```
from selenium import webdriver
from selenium.webdriver.common.keys import Keys
from selenium.webdriver.support import expected_conditions as EC
from selenium.webdriver.common.by import By
from selenium.webdriver.support.wait import WebDriverWait
```

Next, we need to set a path for the webdriver for Selenium to use. 
```
#chrome driver path
driver = webdriver.Chrome('C:/Users/EC/chromedriver.exe')
```

Now, we can use the driver to manipulate the web page you want to scrape. 
```
#open the webpage 
driver.get("https://www.somewebsite.com/")
```

### Scraping
Everything is ready, We are going to scrap some information from a website. 
We direct the webdriver to the website you want to scrap. 
```
driver.get("https://www.quora.com/")
```

The next thing you want to do is to find the data you want to scrap. As I chose Quora, I will be getting the title of the post. To this we need to use  the inspect tool in google chrome. We select the part we want to get and check the HTML code. 
In my case I just want to get the subtitle in the main website. 

```
subtitle = driver.find_element(By.XPATH ,"//div/div/div/div/div/div/div[1]/div/div[2]")
subtitle.text
```

this returns the following: 
> 'A place to share knowledge and better understand the world'

# Bonus 

I wanted to explained in more detail what the code above does.  
using the method `find_element` allows you to find an element within the website. Now the most important part is to choose how you want to find it, you have different ways, such as: by_class, by_id, by_CSS. However, by XPATH takes you directly to the xpath you are trying to get, leaving no room for a mistake.





