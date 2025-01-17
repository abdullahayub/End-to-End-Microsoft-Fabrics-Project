# Microsoft Fabrics Working

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
#

## Data Pipeline Activities

**Child Pipeline 1: Dynamic Pipeline (Get Data from GitHub)**

Our Data source was on GitHub account, get the data from their and pushed into Fabrics Lake house by creating Dynamic Pipeline. 

Created Dynamic Data Pipeline, add three parameters for copying data activity, Relative URL (base URL), Destination (Sink_Folder_name And Sink_File_name).

Created git.Json file where the links of these (parameters) were stored in the form of dictionary.

Lookup Activity (FileNames), this will fetch all the URL’s, all folder names and file names. Applied Foreach Loop (ForAllFiles) performed Copy Activity.

![DPipeline1](https://github.com/user-attachments/assets/ee683d47-2ff0-4d4a-bcf3-f111a3b5f6a9)

![Dynamicpipeline](https://github.com/user-attachments/assets/e4a677ff-9705-4638-8ec2-b5252bdc8e07)

**Data Flow**

Created Data flows, execute ETL Process extract two tables from existing Lake house, perform some transformation and then merge the tables applied Left join primary key of one table with the foreign key of other table. Add destination to the AWLakeHouse.

![DataFlow1](https://github.com/user-attachments/assets/f99c7790-d02b-48fb-8e01-749a6f77eb0d)

**Child Pipeline 2: Azure Data Lake Storage Gen2 Pipeline**

Pull the Data file from Azure Data Lake storage and upload to Fabrics Lake House by creating Copy Activity Pipeline. Make connection between Fabrics Data Lake and Azure Data Lake storage account.

![ADLSPipeline2](https://github.com/user-attachments/assets/11fcaf5f-2622-4be0-a221-e96233e0ce98)

![ADLSFile](https://github.com/user-attachments/assets/eb2d0fa0-2592-4ea2-a321-90fd96be4707)

**Child Pipeline 3:** Created pipeline to run the Data flow called DataFlowJoin.

![DataFlowPipeline](https://github.com/user-attachments/assets/5a489fe7-0914-4540-9414-393e8b526134)

**Parent Pipeline:**

In which we Orchestrated all three Child Pipeline

![ParentPieline](https://github.com/user-attachments/assets/645d7b69-e963-4269-a7b4-f994f717979a)

## Fabric Data Engineering

We read data from AWLakeHouse and Ingest data into silver Lake House using Notebook (PySpark) with some transformations on to the data tables. Create Notebook and read the data tables, transformed it pushed into silver lake house in the Delta format and Save External Table as well.

![SilverNotebook](https://github.com/user-attachments/assets/da48d21c-537b-46d4-bd41-3cad4aee0120)

**Silver LakeHouse**

![external Tables](https://github.com/user-attachments/assets/a3727ffe-f91a-4e3e-9fa4-ce356fff332a)

## Fabric Data WareHoouse

![DataWareHouse](https://github.com/user-attachments/assets/e8211f46-dbcd-473e-8389-efd8fb1e9f4c)

**Created View SQL Query**

![Created View](https://github.com/user-attachments/assets/fae95c7e-2aa6-4924-8fc6-fc53970e62e7)

**Data Modelling - Star Schema**

![Image](https://github.com/user-attachments/assets/b57a50ed-cfde-47b2-bc67-f976fb1985c2)

## Fabrics Data Science

#

https://github.com/user-attachments/assets/161b81bf-19df-4993-ab1a-5be6c411cd15

### Transformation using Data Wrangling

![Image](https://github.com/user-attachments/assets/596a8983-888b-48b1-bf61-e0d5017ea619)

![Image](https://github.com/user-attachments/assets/73912235-1131-4d03-ac94-725b12481d70)



