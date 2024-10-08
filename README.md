# Microsoft_Fabric_Workings

**DirectLake and Power BI**
- Semantic model direct lake connection between PowerBI report and LakeHouse
![SematicModelDirectlake](https://github.com/user-attachments/assets/e56093f3-5ae3-43f5-97ab-a12553e42670)
  
**Data Factory in Microsoft Fabrics**
- Data Pipeline: Copy of dimmension tables from lakehouse to wraehouse.
![DataPipeline](https://github.com/user-attachments/assets/22ce23b6-5732-4569-8df8-d071eb4c67d6)
- Data Flows: Execute ETL Process.
**Data Flow 1**
  ![Dataflow1](https://github.com/user-attachments/assets/356f4d1f-b2ba-4a64-a075-b1604ea6cf16)

**Data Flow 2**
![DataFlow2](https://github.com/user-attachments/assets/ae62d351-6193-45d7-9b79-32900d91335b)

**Data Warehouse in Microsoft Fabrics**
![Warehouse](https://github.com/user-attachments/assets/1ffc9516-0ca1-4f06-9e57-5f014b02a8ea)

**Complete Microsoft Fabrics Video Tour**

https://github.com/user-attachments/assets/5d06da06-1a0b-4088-8dd1-78be7c63f80e


# Data Science Project on Microsoft Fabrics

The dataset contains churn status of 10,000 customers. It also includes attributes that could impact churn such as:

* Credit score
* Geographical location (Germany, France, Spain)
* Gender (male, female)
* Age
* Tenure (years of being bank's customer)
* Account balance
* Estimated salary
* Number of products that a customer has purchased through the bank
* Credit card status (whether a customer has a credit card or not)
* Active member status (whether an active bank's customer or not)

The dataset also includes columns such as row number, customer ID, and customer surname that should have no impact on customer's decision to leave the bank. 

The event that defines the customer's churn is the closing of the customer's bank account. The column `exited` in the dataset refers to customer's abandonment. There isn't much context available about these attributes so you have to proceed without having background information about the dataset. The aim is to understand how these attributes contribute to the `exited` status.
