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

