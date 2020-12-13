# Mission-to-Mars
## The Mission
Use BeautifulSoup and Splinter to scrape full-resolution images of Mars’s hemispheres and the titles of those images, store the scraped data on a Mongo database, and create a web application using flask to display the data and alter the design of the web app to accommodate these images.

## Mobile responsiveness
Mobile responsiveness was added to images and HTML tables to protocols and schematics to complete the pre-flight checklist from their mobile devices.

## Pre-Flight Adjustments

* The Button in the Jumbotron was made bigger and the color was changed to red. 
* Heading was changed from H2 to H4 to match the rest of the page design 
    * indexl.hml: `<h2>Mars Facts</h2>`
* Prevented the table index from being included by adding `index=False`
* created hover rows with the `table-hover` class
    * scraping.py: `return df.to_html(index=False,classes=('table', 'table-hover'))`
    