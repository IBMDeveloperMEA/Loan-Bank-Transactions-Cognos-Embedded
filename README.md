# Analyze Loan Transactions with Cognos Embedded on Watson Studio

## Workshop Resources

- Login/Sign Up for IBM Cloud: <Link>
  
- Slides: <Link>

- Workshop Replay: <Link>
  
There are 3 steps to create your account on [IBM Cloud](<PUT TRACK LINK HERE>): <br>
1- Put your email and password. <br>
2- You get a verification link with the registered email to verify your account. <br>
3- Fill the personal information fields. <br>
  
<img width="1188" alt="Screen Shot 2021-05-31 at 11 25 01 AM" src="https://user-images.githubusercontent.com/15332386/120156441-0769d980-c203-11eb-8cb3-29f4a8d5616a.png">
  
## Architecture Flow

<img width="589" alt="Screen Shot 2021-07-13 at 11 03 19 AM" src="https://user-images.githubusercontent.com/15332386/125406584-0911ea00-e3ca-11eb-9707-22097f1e43b0.png">
  
## Use Case
  
Banks prefer to not give loans to everyone, they want to know the customer that will most likely pay loans and those who won't. In this tutorial we will be working with a loan transaction dataset where we will be visualizing the data to make a better understanding of these customers and their credit risk.
  
## Learning Objectives
  
In this tutorial, you will learn how to use Cognos Embedded on Watson Studio to gain insights into loan transaction data from a bank.
We will focus on the role of the business analyst and see how Cognos Embedded can be used to gain insights into many visualization using different predictors/fields and information that can affect the risk like loan amount, loan length, credits saving and owning a property.
  
## Prerequisites
To complete the tutorial, you need an IBM Cloud account. You can get a free trial account, which gives you access to IBM Cloud and Watson Studio.
  
## Estimated time
Completing this tutorial should take about 30 minutes.
  
## Steps:
  
Download the asset **german_credit_score.csv**
  
### Create an Object Storage service. 
In IBM Cloud main page, you can either type **object storage** in the search field, or click on **Create resource** and then search for **object storage**. Select the **Lite plan** and click **Create**.
  
<img width="1280" alt="Screen Shot 2021-07-13 at 11 31 50 AM" src="https://user-images.githubusercontent.com/15332386/125410517-00231780-e3ce-11eb-8035-a5e2ff4f27c4.png">
  
### Create Watson Studio
Repeat the same step as the previous one, but this time search for Watso Studio. Select the **Lite plan** and choose any **location** you want.
 
<img width="1280" alt="Screen Shot 2021-07-13 at 11 35 23 AM" src="https://user-images.githubusercontent.com/15332386/125410927-73c52480-e3ce-11eb-88b2-e815a27aa3cc.png">
  
Go back to the main page in IBM Cloud. You will see your **Watson Studio** service created in **Resources** under **Services and software**. Click on it and launch **Watson Studio**.
  
<img width="1275" alt="Screen Shot 2021-07-13 at 11 37 35 AM" src="https://user-images.githubusercontent.com/15332386/125411428-f817a780-e3ce-11eb-8a85-6b2387eed99b.png">
  
### Create Watson Studio Project
  
Once you open Watson Studio click on create a project and choose **Create an empty project**. 
  
<img width="1275" alt="Screen Shot 2021-07-13 at 11 42 21 AM" src="https://user-images.githubusercontent.com/15332386/125411897-6b211e00-e3cf-11eb-8a46-84d3ea1f9b6b.png">
  
### Upload Dataset
Inside your project, choose the **Assets** tab and click **browse** to upload the data file `german_credit_data.csv` (make sure that you have downloaded this repo to use the dataset file).

<img width="1280" alt="Screen Shot 2021-07-13 at 11 43 53 AM" src="https://user-images.githubusercontent.com/15332386/125412632-25b12080-e3d0-11eb-9a1a-5ae84eba2151.png">
  
### Add Cognos Embedded Dashbaord
Click on the blue **Add to project button** and choose **Dashboard**. Give it a name and choose the cognos dashboard embedded service that you create it earlier at the beginning.
  
<img width="1280" alt="Screen Shot 2021-07-13 at 11 48 41 AM" src="https://user-images.githubusercontent.com/15332386/125413156-8ea3c563-016e-43fd-aa4b-7fb065ec2bf7.png">
  
Choose a template layout. We will use the default one. 
<img width="1280" alt="Screen Shot 2021-07-13 at 11 53 58 AM" src="https://user-images.githubusercontent.com/15332386/125413609-966e1d47-d073-4e61-876b-39ae8705b1cd.png">  
  
### Add Data Source
  
Click on the add button next to **Selected sources** to choose our dataset that we have uploaded before.
  
<img width="1278" alt="Screen Shot 2021-07-13 at 11 55 10 AM" src="https://user-images.githubusercontent.com/15332386/125413944-c9cff6f8-b4ec-432a-b008-c920e886a8b8.png"> 
  
Click **Data asset** and and choose see the `german_credit_data.csv` file.
  
<img width="1280" alt="Screen Shot 2021-07-13 at 11 57 33 AM" src="https://user-images.githubusercontent.com/15332386/125414303-185b673a-7e09-4d16-b11c-aaa094bd8dc4.png">  
  
Now you should see the file under selected sources. Click on it to see all its fields.
  
### Creating first visualization

There are multiple way to create visualizations in **Cognos Embedded Dashbaord**. First one is by draggind and dropping the field that we want to work with into the canvas. Drag and drop **Loan Purpose** and then **Loan Amont** (Make sure to drag Loan Amount into Loan Purpose since we want to use these fields together).In this case the service will autimatically choose a suitable visualization. 

  <img width="1280" alt="Screen Shot 2021-07-13 at 12 04 59 PM" src="https://user-images.githubusercontent.com/15332386/125415684-0eb418b9-52fe-43dd-9f75-40fd3582fc1c.png">

 Now notice that the *Loan Amount** values are summed (This is done by default). We can change it to average instead of sum. On the top you will see 3 different tabs: **Filters**, **Fields** and **Properties**. These tabs help us to customize our visualizations. Click on **Fields**, and then on the *...* icon next to **Loam Amount** under the **y-axis**. Choose **Summarize** and then **Average**.

  <img width="843" alt="Screen Shot 2021-07-13 at 12 10 01 PM" src="https://user-images.githubusercontent.com/15332386/125416601-21df22b1-a2a8-4ccf-aa69-df0b1c4dcc84.png">
  
  
  
  
  
  


  




  
  
