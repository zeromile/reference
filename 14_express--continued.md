# 14 - Express (continued) #

## Overview - Project 2 ##

1. Enhanced products page - clicking on the “More info” button will dynamically load the product name, a larger version of the image, and more info…into the current page!!


## Project 2 detail ##

1. Part 1 - index.js
    1. In the index.js file add 6 additional routes that are assigned to product1, product2, product3, etc
    2. However, from these routes we will only be sending a JSON object of data, not calling a template so you will need to look at this page here to see how to send JSON data from express: http://expressjs.com/en/4x/api.html#res.json
    3. Here is the structure of the data you will be sending: { productname: 'Product Name', image: 'someimage.jpg', info: 'This is some info' }
    4. You will need to make up information for each of the product name and info values of each JSON object
    5. You will need to download 6 images to your /public/images folder and name them in the image value of each JSON object
2. Part 2 - products.jade
    1. Open the products.jade file in the /views folder 
    2. At the end of the file add a script link that points to /javascripts/javascripts.js (make sure your indenting is correct)
    3. Give the 6 buttons id’s = product1, product2, product3, etc and each button the same classname class = product
    4. Above or below the “products” div add a div with an id = highlight, and then inside that div add…
        1. An h3 tag with an id = productname
        2. An img tag with an id = image
        3. A p tag with an id = info
3. Part 3 - javascripts.js
    1. Create a new file called javascripts.js inside the /javascripts folder inside the /public folder
    2. Open this empty file for editing
    3. Copy the script from the end of jrp10 index.html file (from two weeks ago) and paste it into the javascripts.js file (the script was inside the <script></script> tags)
    4. Modify the script so that the event listener is assigned to the div with an id of products (instead of “buttons”)
    5. Modify the conditional to check if the target clicked has a class of “product” (e.target.class == “product”)
    6. The date coming in from the Node server will be a JSON object so we will need to use Javascript to parse that object in order to access it’s values once the node server has responded…so inside the if (this.readystate….. conditional block add:
        1. The reference code: var obj = JSON.parse(text);  we will need to use this to parse this.responseText and set it to a variable
        2. Once that variable is set we can then access its values like obj.productname or obj.info
        3. We will then need to assign the innerHTML of the productname (id=“productname”) and info (id=“info”) divs 
        4. And finally we will need to set the img (id=“image”) tag src to obj.image

