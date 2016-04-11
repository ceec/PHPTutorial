
#End Goal: Build a resume website

##Concepts covered
- MVC framework setup
- creating routes
- creating models
- creating views
- creating controllers

##Week 1 - Getting Started with Silex

###Goal - Getting Example Page to Display

Download the Silex code here http://silex.sensiolabs.org/download

Don't worry about composer for now, you can download all the files you need and put it in your local setup.

Next we'll set up the first example page, following the instructions here: http://silex.sensiolabs.org/doc/intro.html

Create a example.php and put the example code from the above link into it.

Make sure the:
```PHP
require_once __DIR__.'/../vendor/autoload.php';
```
is pointing to where your silex code is.

To test if this code is working go to /hello/word, you should see Hello World printed to the screen. Try different routes /hello/test , hello/one , etc, to see how it takes the variable and displays it.

###Extra
If you get that setup and feel comfortable with everything, try making a different route that prints a different sentence.
