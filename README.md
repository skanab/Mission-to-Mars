# Mission-to-Mars
## The Mission
Use BeautifulSoup and Splinter to scrape full-resolution images of Mars’s hemispheres and the titles of those images, store the scraped data on a Mongo database, and create a web application using flask to display the data and alter the design of the web app to accommodate these images.

## Mobile responsiveness
Mission control reviewed mobile responsiveness to ensure the site was bootstrap 3 compliant and added BS3 attributes to images and tables to ensure that ground crews' mobile platforms were responsive and rendered all content correctly.

```
<link
    rel="stylesheet"
    href="https://maxcdn.bootstrapcdn.com/bootstrap/3.3.7/css/bootstrap.min.css"
/>

 <img src="{{mars.featured_image | default('static/images/error.png', true) }}"
      class="img-responsive"
      alt="Responsive image"
 />

<div class="table-responsive">
    {{ mars.facts | safe }}
</div>

```

## Pre-Flight Adjustments

* The Button in the Jumbotron was made bigger and the color was changed to red. 
* Heading was changed from H2 to H4 to match the rest of the page design 
    * indexl.hml: `<h2>Mars Facts</h2>`
* Prevented the table index from being included by adding `index=False`
* created hover rows with the `table-hover` class
    * scraping.py: `return df.to_html(index=False,classes=('table', 'table-hover'))`
    