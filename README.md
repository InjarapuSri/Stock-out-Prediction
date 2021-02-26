#  Stock-out Predictor

A backorder is an order for a good or service that cannot be filled at the current time due to a lack of available supply. The item may not be held in the company's available inventory but could still be in production, or the company may need to still manufacture more of the product This can impede potential profit that a company can earn. 

> The backorder is an indication that demand for a company's product outweighs its supply.   
 
Stock-out Predictor can help mitigate this loos by forecasting the possibility of backorders whenever there maybe a surge in the demand.

# Environment Setup


This code works well with python 3.6 in conda environment.

install all the libraries mentioned in requirements.txt. Use following code.

''' pip install -r requirements.txt ''' 



# Project Structure 

![image-20210226182332386](https://github.com/InjarapuSri/Stock-out-Prediction/blob/main/Screenshot%20(84).png)



* **requirements.txt** file consists of all the packages that you need to deploy the app in the cloud.
* **main.py** is the entry point of our application, where the flask server starts. 
* **manifest.yml**:- This file contains the instance configuration, app name, and buildpack language.
* ![image-20210226182522801](https://github.com/InjarapuSri/Stock-out-Prediction/blob/main/Screenshot%20(85).png)
* **Procfile** :- It contains the entry point of the app.
* ![image-20210226182559893](https://github.com/InjarapuSri/Stock-out-Prediction/blob/main/Screenshot%20(86).png)




​     This is the architecture of the project-

![image-20210226182756761](https://github.com/InjarapuSri/Stock-out-Prediction/blob/main/Screenshot%20(83).png)

# Training Dataset

[(Back to top](#table-of-contents)

 

Let's talk a little bit about our training dataset.

''' **sku** –                Random ID for the product

**national**_**inv** –   Current inventory level for the part

**lead_time**–      Transit time for product (if available)

**in_transit_qty** –  Amount of product in transit from source

**forecast_3_mont**h –    Forecast sales for the next 3 months

**forecast_6_month** –    Forecast sales for the next 6 months

**forecast_9_month** –    Forecast sales for the next 9 months

**sales_1_month** –  Sales quantity for the prior 1 month time period

**sales_3_month** –  Sales quantity for the prior 3 month time period

**sales_6_month** –  Sales quantity for the prior 6 month time period

**sales_9_month** –  Sales quantity for the prior 9 month time period

**min_bank** –          Minimum recommend amount to stock

**potential_issue** –  Source issue for part identified

**pieces_past_due** –     Parts overdue from source

**perf_6_month_avg** –   Source performance for prior 6 month period

**perf_12_month_avg** –  Source performance for prior 12 month period

**local_bo_qty** –        Amount of stock orders overdue

**deck_risk** –           Part risk flag

**oe_constraint** –   Part risk flag

**ppap_risk** –          Part risk flag

**stop_auto_buy** –      Part risk flag

**rev_stop** –       Part risk flag

**went_on_backorder** –  Product actually went on backorder. This is the target value.'''

Apart from training files, we also require a "schema" file from the client, which contains all the relevant information about the training files such as:

Name of the files, Length of Date value in FileName, Length of Time value in FileName, Number of Columns, Name of the Columns, and their datatype.


