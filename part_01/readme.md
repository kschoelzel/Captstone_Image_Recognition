## Introduction 

For my capstone project I used the cDiscount product catalog from kaggle to build an image recognition model using Keras Convoluted Neural Networks libraries. 

The data for this project was massive (58GB) and consisted of over 7 million distinct pictures, which could be classified into 5720 distinct categories. This data was too large to be classified on a non-GPU computer in an efficient manner. 

As such, I created two smaller datasets, containing five categories each. I refer to these two sets as samples throughout my notebooks. I then built two CNN models to gain a better understanding of how these algorithms work. 


The first sample was comprised of objects that were all similar to each other; I refer to the files dealing with this first sample as Wine. 

The five categories for this sample were: 

- Whiskey  
- Red Wine
- White Wine
- Rose
- Champagne

The second set of items I selected were all different. I wanted to see if there was a noticeable difference in how the model performed when there were visually more distinct differences to train on. I refer to this second set as Mixed Bag or MB throughout my notebooks. 

The five categories for this sample were

- Photography Books 
- Auto Fuses
- Hinges
- Lotion 
- Bed Headboards

Both test sets were 7916 items (roughly 0.1% of the total database). I picked these items because they had almost the same number of items per category. In keeping these characteristics of my data "constant" I hoped to isolate the variables I was testing. 

## Notebooks, Data Cleaning, and Modeling 


To jump from the EDA to different sections of my capstone, you can use the links below: 

[II. Wine Data Pipeline an Generator  ](II. Wine - Data Pipeline and Generator - Final.ipynb).

[II. MB Data Pipeline an Generator  ](II. MB Data Pipeline and Generator - Final.ipynb).

During the Data Generation, the items were converted to categorical numbers before they were loaded into the final model pipeline. Because of the requirements of Neural Nets to have distinct shapes of the input data it was creating an error when I tried to convert them back to create the confusion matrix. Luckily, this could be remedied by using a separate pandas dataframe that had the category and product ids (but not the picture data). It was easier to get the information I needed, which is what the fixed Y-vales shows. 

I have commented out the to-categorical lines in the main pipelines, but these Fixed Y-Values files should still be run, as its the arrays saved out of them that are loaded into my final models. 

[III. Wine Fixed Y-Values ](Wine Fixed Y-Values - Final.ipynb).

[III. MB Fixed Y-Values ](III. MB Fixed Y-Values - Final.ipynb).


The model notebooks:


[IV. Wine Model and Analysis ](IV. Wine Model and Analysis - Final.ipynb).

[IV. MB Model and Analysis ](IV. MB Model and Analysis - Final.ipynb).


In addition, here is the link to my notebook from part two, which illustrates working with the BSON file type and extracting the images. The insights from this notebook were what I used in the data generators and pipelines. 

[Exploring Image Files and BSON](Exploring Image Files and BSON.ipynb).
