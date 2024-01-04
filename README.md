
# Project 1 :- Data Visualization Using AWS Services 

## Hello, there...

In this AWS project, we will be visualizing data using __Amazon Quicksight__ and __Amazon S3__. 


## Design and Workflow

![Slide1](https://github.com/neelspatel02/repo-1/blob/dc4c39e7ac243c63484753a556a6b5ee68db8afd/images/Slide1.jpg)

This AWS project focuses on storing a dataset in an Amazon S3 bucket and using Amazon QuickSight to analyze and visualize the data. The project aims to demonstrate a simple yet powerful setup for managing and visualizing data using AWS services

## Setup
### 1 - Crating a Bucket.

- Go to Amazon S3 page in AWS management console and click on "Create bucket".
- Enter a unique name for your bucket (Bucket names must be globally unique across all of Amazon S3).
  
![S-1](https://github.com/neelspatel02/repo-1/blob/c76f0251251525f8d3d1b1996450f15f8c678ed9/images/S3-1.png)

- Choose a region for your bucket. Select a region that is geographically close to you for better performance.
- keep rest of the settings as default and select "create".

### 2 - Uploading necessary files. 
___

- Before doing anything first download the .csv and manifest.json files from the repo.
  +  The .csv file is a Demo dataset with 1000 entries of The most sold products on amazon. You can use your own dataset instead.
  + The purpose of the json file is to provide instructions to QuickSight to import the necessary .csv file 
- Now open the json file and change this line of code
  ` s3://BUCKET-NAME/Amazon-Bestseller-Dataset.csv `
  by putting the name of the S3 bucket you created inplace of "BUCKET-NAME" and save it.
 <br> For example ` s3://neel-project-bucket/Amazon-Bestseller-Dataset.csv `.
- Click on the bucket you just created in S3 console and click on "Upload". Then click on "Add files" and select the both .csv and json files. 
- Press "Upload". 

### 3 - Creating QuickSight Account.
___

- Search QuickSight in AWS console. And you will see this sigh-up page.

![S-2](https://github.com/neelspatel02/repo-1/blob/c76f0251251525f8d3d1b1996450f15f8c678ed9/images/QuickSight-1.png)
  
- Click on Sigh-up.

![S-3](https://github.com/neelspatel02/repo-1/blob/c76f0251251525f8d3d1b1996450f15f8c678ed9/images/QuickSight-2.png)
  
- You will be able to use free trial of the enterprise addition for 30 days. Press "Continue" 

**__NOTE:__** __Delete youe QuickSight account before 30 days if you don't want to incure any charges.__

- Fill in your details in "accoun info" section.

![S-4](https://github.com/neelspatel02/repo-1/blob/c76f0251251525f8d3d1b1996450f15f8c678ed9/images/QuickSight-3.png)

- Select the S3 bucket you created to link to QuickSight.

![S-5](https://github.com/neelspatel02/repo-1/blob/c76f0251251525f8d3d1b1996450f15f8c678ed9/images/QuickSight-4.png)

- Keep rest as Default then click "Finish".

![S-6](https://github.com/neelspatel02/repo-1/blob/c76f0251251525f8d3d1b1996450f15f8c678ed9/images/QuickSight-5.png)

- Click on "Go to Amazon QuickSight". 

### 4 - Visualizing The Dataset.
___

- In QuickSight click on "New Analysis" and then select "S3".

![S-7](https://github.com/neelspatel02/repo-1/blob/c76f0251251525f8d3d1b1996450f15f8c678ed9/images/V-2.png)
  
- Now go back to S3 console, choose the "manifest.jason" Object and click on "Copy S3 URL".

![S-8](https://github.com/neelspatel02/repo-1/blob/64718e385b082cbea05baae69b9a31a38ab89c96/images/v-4.png)

- Paste the URL in the QuickSight, Type-in the Data source name of your choice and click "Connect".

![S-9](https://github.com/neelspatel02/repo-1/blob/c76f0251251525f8d3d1b1996450f15f8c678ed9/images/v-5.png)

- Click "Visualize".
- Select the interactive sheet option and click "Create". The Dataset will start importing.
- QuickSight already imported the column names.

![S-10](https://github.com/neelspatel02/repo-1/blob/c76f0251251525f8d3d1b1996450f15f8c678ed9/images/v-7.png)

- You can now visualize the data by selecting the column of your choice.
- You compare different Feilds and Sort them in different ways accourding to your liking.

![S-11](https://github.com/neelspatel02/repo-1/blob/c76f0251251525f8d3d1b1996450f15f8c678ed9/images/v-8.png)

Here's the sorted graph of Brands by most popular to least popular. Standard motor products seem to be the most popular. (NOTE: This is based on the Demo Dataset and Not a Real one)  

![S-12](https://github.com/neelspatel02/repo-1/blob/04d2f5fc06a1cabd69882695920132f70f9cb471/images/Screenshot%202024-01-04%20180401.png)

You can try different types of graphs and charts.

![S-13](https://github.com/neelspatel02/repo-1/blob/04d2f5fc06a1cabd69882695920132f70f9cb471/images/v-9.png)
