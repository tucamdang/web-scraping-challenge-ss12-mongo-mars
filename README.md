# Mission to Mars
We build a web application that scrapes various websites for data related to the Mission to Mars and displays the information in a single HTML page.
--------------------------
## There will be 3 Parts: Scraping | MongoDB and Flask Application | Submission
The websites will be used: 
``
nasa mars news: Nasa_url ='https://redplanetscience.com/'

JPL image: url = 'https://spaceimages-mars.com'

Mars fact: https://galaxyfacts-mars.com/

Hemisphere: https://marshemispheres.com/
``
![image](https://user-images.githubusercontent.com/99168697/168410253-6cf05ad6-c611-4f36-92c1-617ac7e66d4d.png)

- This project is about Mission to Mars, we run the code in jupyternotebook and then created the python script (scraping_mars.py) to scrape text and images from many websites/ link provided. we have to link this app.py to index.html, and use Bootstrap to display all search data in left location. 
We also connect to MongoDB, whenever the data scraped and displayed will be stored in non-relational Mongo Database. The scrape button is set to collect the newest data in relation to the link/ website provided.  
![image](https://user-images.githubusercontent.com/99168697/168410333-0255f6cb-20ae-47af-97d5-d57e08e286ca.png)
- Secondly, we created app.py as flask web application with  HTML template 
![image](https://user-images.githubusercontent.com/99168697/168410349-a156579d-97e5-43f6-831c-5e4880f181b5.png)

## Part  1: Scraping
Jupyter Notebook file called ``mission_to_mars.ipynb``. Use this file to complete all your scraping and analysis tasks. The following information outlines what you need to scrape.
Make sure you pip install some function it Git bash/ your Terminal 		
    Pip install Flask-PyMongo
		Pip install selenium
		Pip install bs4
		Pip install webdriver_manager
    		Pip install lxml 
		
### NASA Mars News: https://redplanetscience.com/
Scrape the Mars News Site and collect the latest News Title and Paragraph Text.

### JPL Mars Space Images—Featured Image: https://spaceimages-mars.com
Use Splinter to navigate the site and find the image URL for the current Featured Mars Image, then assign the URL string to a variable called ``featured_image_url``.
  NOTE: we need to store ``chromedriver.exe`` in folder to run `ipynb` smoothly.
![image](https://user-images.githubusercontent.com/99168697/168410994-f6b99339-9f43-4d14-b5d9-c80e275ccf4e.png)

  Store ``chromedriver.exe`` in folder
  
![image](https://user-images.githubusercontent.com/99168697/168410910-8a54190f-a6ad-4859-8dcb-eea2468aa461.png)

### Mars Facts: https://galaxyfacts-mars.com/
Visit the Mars Facts webpage and use Pandas to scrape the table containing facts about the planet including diameter, mass, etc.
Use Pandas to convert the data to a HTML table string.
![image](https://user-images.githubusercontent.com/99168697/168411056-888bc8b2-f335-4222-a003-d093017dd808.png)

### Mars Hemispheres: https://marshemispheres.com/
You will need to click each of the links to the hemispheres in order to find the image URL to the full-resolution image.
Save the image URL string for the full resolution hemisphere image and the hemisphere title containing the hemisphere name. Use a Python dictionary to store the data using the keys img_url and title.
Append the dictionary with the image URL string and the hemisphere title to a list. This list will contain one dictionary for each hemisphere.

## Part 2: MongoDB and Flask Application
After running smoothly the code in Jupyter Notebook. 
- Use MongoDB with Flask templating to create a new HTML page that displays all the information that was scraped from the URLs above.
We can copy the code and convert from Jupyter Notebook it into Python script called scrap_mars.py

- Create a template HTML file called index.html that will take the Mars data dictionary and display all the data in the appropriate HTML elements. Use the following as a guide for what the final product should look like, but feel free to create your own design.

## Part 3: Submission
Place index.html into templates folder. 

![1](https://user-images.githubusercontent.com/99168697/168413311-b4acfcb5-6982-4bd9-b1be-91bd14118da2.png)
