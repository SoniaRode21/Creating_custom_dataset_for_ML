# Creating an animal classifier( 'horse','camel','zebra','elephant') form custom dataset by scraping images from google.


## Steps for creating a deep learning dataset from google images 

Inspired by Adrian Rosebrock, fast.ai course lesson 2

STEPS:
1. For every class label, google search the images. Scroll down until you have enough images for that class.

2. Save the urls of all the images into a file.

    1. Use cmd opt J on a mac (ctrl shift J for windows) to get the javascript console
    2. Copy the following code in the js console. It downloads a file containing the urls of all the images in the google search

    
    urls=Array.from(document.querySelectorAll('.rg_i')).map(el=> el.hasAttribute('data-src')?el.getAttribute('data-src'):el.getAttribute('data-iurl')); window.open('data:text/csv;charset=utf-8,' + escape(urls.join('\n')));  

3. Repeat these steps for all the classes you want in the dataset


