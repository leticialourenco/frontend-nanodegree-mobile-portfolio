## Performance Optimization

Launch website by clicking [here](http://leticialourenco.github.io/frontend-nanodegree-mobile-portfolio/index.html).

### General changes

* Compressed the images profilepic.jpg and pizzeria.jpg
* Embedded above-the-fold CSS to eliminate render-blocking
* Minified the CSS
* Added ```media="print"``` for print.css to eliminate render-blocking
* Added ```async``` attribute to javascript files
* Added .htaccess file to leverage browser caching

### Cam's Pizzeria changes

* Embedded CSS files
* Minified CSS files
* Compressed the images pizzeria.jpg and pizza.png
* Added the property ```backfact-visibility:hidden``` to ```.mover``` to reduce repainting time - so it repaints only the moving pixels
* Toke out of the loop the calculation and declaration of constants so they won't do unnecessary re-calculations on each loop iteration 
* Toke calculation of ```phase``` out of the main loop - so they don't need to calculate over every single iteration (only the useful 5 times)
* Exchange all uses of the ```querySelectorAll``` to ```getElementsByClassName``` - since the second is faster
* Made changes to the function ```changePizzaSizes(size)``` so the DOM is accessed only once per loop iteration (by creating a var wrapping the access and using its value)
* Removed unnecessary pizzas from ```addEventListener``` (200 pizzas were unreasonable since most of them weren't visible)
* Adapted the function ```logAverageFrame``` to measure the last 60 frames instead of the last 10




