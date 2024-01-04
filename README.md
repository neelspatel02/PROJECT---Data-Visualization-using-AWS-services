
# Project 1:- Data Visualization Using AWS Services 

Hello, there...

In this AWS project, we will be visualizing data using __Amazon Quicksight__ and __Amazon S3__. 


## Design

![Slide1](https://github.com/neelspatel02/repo-1/blob/dc4c39e7ac243c63484753a556a6b5ee68db8afd/images/Slide1.jpg)

This AWS project focuses on storing a dataset in an Amazon S3 bucket and using Amazon QuickSight to visualize the data. The project aims to demonstrate a simple yet powerful setup for managing and visualizing data using AWS services

## Setup
### 1 - Crating a Bucket.

- Go to Amazon S3 page in AWS management console and click on "Create bucket".
- Enter a unique name for your bucket (Bucket names must be globally unique across all of Amazon S3).
- Choose a region for your bucket. Select a region that is geographically close to you for better performance.
- keep rest of the settings as default and select "create".

### 2 - Uploading necessary files.

- Before doing anything first download the .csv and manifest.json files from the repo.
  +  The .csv file is a Demo dataset with 1000 entries of The most sold products on amazon. You can use your own dataset instead.
  + The purpose of the json file is to provide instructions to QuickSight to import the necessary .csv file 
- Now open the json file and change this line of code 's3://BUCKET-NAME/Amazon-Bestseller-Dataset.csv' by putting the name of the S3 bucket you created inplace of "BUCKET-NAME" and save it.
- Click on the bucket you just created in S3 console and click on "Upload". Then click on "Add files" and select the both .csv and json files. 
- Press "Upload". 

### 3 - Creating QuickSight Account.

- Search QuickSight in AWS console. And you will see this sigh-up page.
- Click on Sigh-up.
- You will be able to use free trial of the enterprise addition for 30 days. Press "Continue" 

**__NOTE:__** __Delete youe QuickSight account before 30 days if you don't want to incure any charges.__

- Fill in your details in "accoun info" section.
- Select the S3 bucket you created to link to QuickSight. 
- Keep rest as Default then click "Finish".
- Click on "Go to Amazon QuickSight". 

### 4 - Visualizing The Dataset.

- In QuickSight click on "New Analysis" and then select "S3".
- Now go back to S3 console, choose the "manifest.jason" Object and click on "Copy S3 URL".
- Paste the URL in the QuickSight, Type-in the Data source name of your choice and click "Connect".
- Click "Visualize".
- Select the interactive sheet option and click "Create". The Dataset will start importing.
- QuickSight already imported the column names. 
- You can now visualize the data by selecting the column of your choice.
- You compare different Feilds and Sort them in different ways accourding to your liking.
- Here's the sorted graph of Brands by most popular to least popular.
