# 13 - Express (continued) #

## Overview - Project 1 ##

1. Serve up the Pet Store Website through node and express 
    1. Use the express generator to create the initial scaffolding
    2. Add common elements to the jade layout template (like bootstrap, navigation, etc)
    3. Convert home page to index.jade
2. Products page 
    1. Must contain 6 products that have a product name, product image, and a “More Info” button
3. About Us page
    1. telephone, email, website, store address
4. Create routes for all the pages


### References: ###
1. Jade 
    1. http://jadelang.net/
    2. http://naltatis.github.io/jade-syntax-docs/
2. Express Generator
    1. http://expressjs.com/en/starter/generator.html


## Project 1 detail ##

1. From within the projects folder run: $ express mypets (this will create a mypets folder, node_modules folder, and package.json file)
2. Move into the /mypets folder: $ cd mypets 
3. Install dependencies: $ npm install
4. Test the app by entering  $ DEBUG=mypets:* npm start in the terminal and then navigating to localhost:3000 in the browser
5. Launch atom, open /mypets folder
6. Edit the layout.jade file (in the /views folder) so that it includes all the default stuff you should have for every page (like bootstrap, navigation, etc)
7. Edit the index.jade file (in the /views folder) so that it accurately displays the home page of the pet store site (refer to the pet store site you previously built for reference). Remember to add the main.css file to the /stylesheets folder (inside the /public folder) 
8. Create two additional .jade files (contactus and products - jade file names cannot have spaces so we use contactus)
9. Edit the contact page to include contact info (telephone, email, website, store address)
10. Edit the products page to display 6 products with: title, image, short description, price, and a “more info” <button>
11. The products should all be inside one big div with id = products
12. Open the index.js in the /routes folder and add routes for the 2 additional pet store pages: products and contactus 
13. relaunch the application and refresh in your browser…all 3 pages need to work
