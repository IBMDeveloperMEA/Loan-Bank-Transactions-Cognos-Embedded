# Analyze Loan Transactions with Cognos Embedded on Watson Studio
Dasboard Result [HERE](https://eu-gb.dataplatform.cloud.ibm.com/dashboards/247fbdaf-c089-42eb-b502-856e67f05e00/view/6e27dd2412ec3ff561e7b1e407cd2b037c33735db7bb810a80d77b495a337497a86a4690c82d420bdb190c64f7ea475e9b)

## Workshop Resources

- Login/Sign Up for [IBM Cloud](https://cloud.ibm.com/registration?utm_medium=Inpersondirected&utm_content=000039JL&utm_term=10010797&utm_id=Jul2021-analyzeloantransactionswithcognosembeddedonwatsonstudio-eventid-60d30158fd948362e7c19b44-global-devadvgrp-dubai-hybrid-workshop-dubai) <br>
- [Slides]() <br>
- Workshop [Replay]() <br>
- [Survey](www.surveygizmo.com/s3/6083679/c11a45c047b4?uid=60d30158fd948362e7c19b44) (We really appreciate any feedback :D) <br><br>
- Follow Our [Meetup Page](https://www.meetup.com/IBM-Cloud-MEA/) to get updates on our events <br>
- Check [IBM Developer](https://developer.ibm.com/) to learn and explore a variety technologies and services that you're interested in <br>
  
There are 3 steps to create your account on [IBM Cloud](https://cloud.ibm.com/registration?utm_medium=Inpersondirected&utm_content=000039JL&utm_term=10010797&utm_id=Jul2021-analyzeloantransactionswithcognosembeddedonwatsonstudio-eventid-60d30158fd948362e7c19b44-global-devadvgrp-dubai-hybrid-workshop-dubai): <br>
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
  
### Creating First Visualization

There are multiple way to create visualizations in **Cognos Embedded Dashbaord**. First one is by draggind and dropping the field that we want to work with into the canvas. Drag and drop **Loan Purpose** and then **Loan Amont** (Make sure to drag Loan Amount into Loan Purpose since we want to use these fields together).In this case the service will autimatically choose a suitable visualization. 

  <img width="1280" alt="Screen Shot 2021-07-13 at 12 04 59 PM" src="https://user-images.githubusercontent.com/15332386/125415684-0eb418b9-52fe-43dd-9f75-40fd3582fc1c.png">

 Now notice that the *Loan Amount** values are summed (This is done by default). We can change it to average instead of sum. On the top you will see 3 different tabs: **Filters**, **Fields** and **Properties**. These tabs help us to customize our visualizations. Click on **Fields**, and then on the *...* icon next to **Loam Amount** under the **y-axis**. Choose **Summarize** and then **Average**.

  <img width="843" alt="Screen Shot 2021-07-13 at 12 10 01 PM" src="https://user-images.githubusercontent.com/15332386/125416601-21df22b1-a2a8-4ccf-aa69-df0b1c4dcc84.png">
 
Let's change this visualization to a pie chart. Above the visualization there is button and next to it you see the type of the current chart that you are using. Click on it, and click on **All Visalizations**. Select **Pie**. Now we have a pie chart instead of a line graph.
  
<img width="946" alt="Screen Shot 2021-07-13 at 12 29 57 PM" src="https://user-images.githubusercontent.com/15332386/125419481-a0ea79fb-18da-4728-8e48-262ff637b363.png">
  
We can see that loans amounts are the highest for **business**, **repairs** and **other** purposes, and are lowest **new cars** and used **cards**
  
Now let's add a title to this visulization. Next to the button that allows us to change the visualization type, there is a button that allows to to add a title. Click on it and give a title to your visualization.

<img width="840" alt="Screen Shot 2021-07-13 at 12 35 58 PM" src="https://user-images.githubusercontent.com/15332386/125419957-639eea7a-93b0-4f0e-800e-4f54de99a6f0.png">
  
### Creating the second visuzalization
This time we will use another way to create a visualization. From the left side, click on the **Visualization** button, drag and drop **Stacked bar**

<img width="879" alt="Screen Shot 2021-07-13 at 12 43 29 PM" src="https://user-images.githubusercontent.com/15332386/125421173-7e09fe9e-2a4d-4769-b6e4-613fbbc64899.png">
  
Obviously it will be empty since we didn't choose the fields yet. Drag and drop **OwnsProperty** to the **Bars** field, **LoanDuration** to the **Length** field  and **Risk** to the **Color** field. For **Loan Duration** just like we did before, choose it to **Average** instead of **Sum**.
  
<img width="834" alt="Screen Shot 2021-07-13 at 12 51 29 PM" src="https://user-images.githubusercontent.com/15332386/125422234-d4e88117-73ed-456f-91b2-8c0ab03ca73a.png">
  

<img width="817" alt="Screen Shot 2021-07-13 at 1 08 16 PM" src="https://user-images.githubusercontent.com/15332386/125428047-d9c7605e-c956-4d3d-9d7b-d13846bcfb06.png">
  
Here for example we can see that for people who have a real estate and applied for a loan with duration of more than 15 days show a risk. For people who have savings insurance, the risks starts for a duration that is longer than 20 days.
  
### Creating third visualization
  
Let's repeat the same process but this time let's choose a **Line** visuzalization. Drag and drop **LoanDuration** to the **y-axis**, **Risk** to **Color** and **LoanAmount** to **x-axis**.
  
<img width="827" alt="Screen Shot 2021-07-13 at 1 42 53 PM" src="https://user-images.githubusercontent.com/15332386/125430451-9c8f321a-c473-4af1-8828-a8e2066aaebd.png">
  
This initial graph layout is too compact, and a warning icon is displayed in the upper-right corner. The warning states that multiple items had to be clipped and that we should apply a filter to show less data.

Make the suggested adjustment by clicking the menu *...* icon for the **LoanAmount** field, then enabling the Auto-group option.
  
<img width="269" alt="Screen Shot 2021-07-13 at 1 46 09 PM" src="https://user-images.githubusercontent.com/15332386/125430810-3efac65d-2942-4147-8eb6-42f930337cf4.png">
  
This will result in a much more useful chart. We can see that the least risky loans are for small loan amount that have a large loan duration.
  
<img width="484" alt="Screen Shot 2021-07-13 at 1 48 00 PM" src="https://user-images.githubusercontent.com/15332386/125430965-198f27a4-bb9f-4b00-8d51-d7e76e5a6e5e.png">
  
We can change the colors by going to **Properties** -> **Visualization** -> **Change color palette**.
  
<img width="825" alt="Screen Shot 2021-07-13 at 1 49 05 PM" src="https://user-images.githubusercontent.com/15332386/125431382-37550251-abb6-4b48-aef5-69d852eab0bc.png">
  
### Creating the Last Visualization
For this one we are going to create a new tab. Just press the plus icon next to **Tab1**. Now we have a **Tab2** and we will do this visualization in this new tab.
Just like before, we repeat the steps. This time choose the **Packed bubble** visualization and drag it to the canvas. Drag and drop **ExistingSavings** to **Bubbles** and **Color**, and drag and drop **Risk** to **Size**.
  
<img width="1236" alt="Screen Shot 2021-07-13 at 1 57 02 PM" src="https://user-images.githubusercontent.com/15332386/125432344-b677a125-a82f-4147-be39-b22158052380.png">.
  
This is not very useful because all the bubble have the exact same size and that's because we are counting the unique values or **Risk** which are *Risk* and *No Risk*. So the first thing to do is to change the way we are counting the risk values. Open the menu of **Risk** that is on **Size**, choose summarize and then choose **Count** instead of **Count distinct**.
  
<img width="276" alt="Screen Shot 2021-07-13 at 2 00 24 PM" src="https://user-images.githubusercontent.com/15332386/125433148-c4b0013b-648e-4673-948e-175d8eb74b45.png">
  
Now we counting all the values of risks. But to make it more useful, I want to check which category of the existing savings (range) has the higest risk and which has the lowest. Let's add a filter and drag **Risk** to this filter. Now because we have 2 tabs, make sure ro drag **Risk** to the second Filter Tab.

  <img width="1280" alt="Screen Shot 2021-07-13 at 2 18 50 PM" src="https://user-images.githubusercontent.com/15332386/125436005-ab885035-76fc-457f-b7aa-7f8fe5a4ee1c.png">
  
Click on this new added filter and choose only the *Risk* value.


<img width="515" alt="Screen Shot 2021-07-13 at 2 10 13 PM" src="https://user-images.githubusercontent.com/15332386/125434313-d9dc7c6b-62fc-45bf-9487-d506e682dd56.png">
  
Now are only counting the *Risk* value. This visualizations tells us that the customers who have savings between 500 and 1000 are much rikser than other customers. The least riksy are the customers who have savings less than 100 (We are ignoring the **Unkown** category).
  
<img width="735" alt="Screen Shot 2021-07-13 at 2 13 21 PM" src="https://user-images.githubusercontent.com/15332386/125434945-2b5ee928-7698-41f9-98e3-f4d7b9342f2d.png">

  
### Saving and Sharing the Dashbaord
  
Once you're done click the save button at the very top and then click on the share icon. This generates a link that can be shared with other people to see and interact with your dashboard.

<img width="1280" alt="Screen Shot 2021-07-13 at 2 27 00 PM" src="https://user-images.githubusercontent.com/15332386/125437260-7b845935-93ba-4f58-9587-6c2b5e26f5ad.png">
  
Enable the share to anyone who has the link and share the generated link.
  
<img width="1079" alt="Screen Shot 2021-07-13 at 2 31 39 PM" src="https://user-images.githubusercontent.com/15332386/125437455-87d13b41-a58f-4ab9-9611-9eb3f8196bb2.png">

### Summary
In this tutorial, we detailed how to use some of the features in Cognos Embedded Dashboard to help visualize loan transactions. You learned how to create and customize charts and graphs to help explain credit risk, gains insights and have a better understanding of loan transactions.

## Workshop Resources

- Login/Sign Up for [IBM Cloud](https://cloud.ibm.com/registration?utm_medium=Inpersondirected&utm_content=000039JL&utm_term=10010797&utm_id=Jul2021-analyzeloantransactionswithcognosembeddedonwatsonstudio-eventid-60d30158fd948362e7c19b44-global-devadvgrp-dubai-hybrid-workshop-dubai) <br>
- [Slides]() <br>
- Workshop [Replay]() <br>
- [Survey](www.surveygizmo.com/s3/6083679/c11a45c047b4?uid=60d30158fd948362e7c19b44) (We really appreciate any feedback :D) <br><br>
- Follow Our [Meetup Page](https://www.meetup.com/IBM-Cloud-MEA/) to get updates on our events <br>
- Check [IBM Developer](https://developer.ibm.com/) to learn and explore a variety technologies and services that you're interested in <br>


## Reference Links
- https://developer.ibm.com/tutorials/go-serverless-in-watson-assistant-with-ibm-cloud-function/
  
  

  
  
  

  
  
  

  
  

  

  


  
  
  
  
  


  




  
  
