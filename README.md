# Item-Description-Generator
This repo is meant to display an algorithm that generates item descriptions for medical items. However, it can be applied to any industries item. 

# Overview of process
The code is laid out in the way it was developed. First you will see a brief test of the model. It is loaded using ollama running a local server which is why I elected to use smaller models (llama3 or phi3.5 perform well).
Then you will see a definition of the 3 core processes of the scraping. The first searches the URLs using a DDG_search library from duck duck go. The second loads the page using chromedriver. I elected to use this because of its ability to process javascript and dynamic pages. Lastly, I use beautifulsoup parser to read and identify the parts of the site that I want.
After this you will see a test of these processes using an example search query.
After this you will see a redefinition of these to be applied to a dataframe of items with manufacturer and catalog number as input. The processes will iterate through the dataframe and populate the descriptions in a new column.
