# Inventory_Purchasing-Operational-Dashboard
Operational Dashboard provides a comprehensive overview of key purchasing metrics, supplier performance, and inventory management, enabling leadership to make informed decisions and optimize operational efficiency. Created with BigQuery and PowerBI. Please check Dashboard.pdf for overview

## I. Introduction
### 1. Business question
The Purchasing Department requested the Data Analyst Team to develop an Operational Dashboard that provides leadership with a clear and intuitive overview to aid in decision-making and enhance operational efficiency. This booklet has been created to introduce the process of building this Dashboard, provide instructions for using the Dashboard, and present the team's recommendations.
### 2. Dataset
Dataset: **adventureworks2019** (public Google BigQuery dataset)

Dataset dictionary: Please reach file "Data Dictionary" attached above

Dataset Schema: https://i0.wp.com/improveandrepeat.com/wp-content/uploads/2018/12/AdvWorksOLTPSchemaVisio.png?ssl=1

Dataset access: 
- Log in to your Google Cloud Platform account and create a new project.
- Navigate to the BigQuery console and select your newly created project.
- In the navigation panel, select "Add Data" and then "Star a project by name".
- Enter the project name "adventurework2019"

## II. Apply design thinking mindset
**1. Empathize**

***a. 5W1H***
![image](https://github.com/user-attachments/assets/af120642-2139-4192-a49c-ef5b07297de7)

***b. Empathy Map***
![image (1)](https://github.com/user-attachments/assets/cfd94068-4fc7-47cb-81b3-4552a864850f)


***c. Stakeholder Journey***
![image (8)](https://github.com/user-attachments/assets/c4161c14-63fa-469e-897b-ef987db2476a)


**2. Northstar Metric and POV**
![POV](https://github.com/user-attachments/assets/2af80dff-cc9a-4395-acc6-3400db6263ed)


**3. Ideate**
![image (10)](https://github.com/user-attachments/assets/107c02ad-1c1b-4ab9-8292-c9d51e15f908)



## III. Main Process
### 1. Extract data with Google BigQuery


#### Output product ID, product name, sub-category, category 
![image (11)](https://github.com/user-attachments/assets/364f961f-ebbb-47cb-b6b6-e0ced6d096a2)


#### Output total inventory quantity by product ID 
![image (12)](https://github.com/user-attachments/assets/232220c0-e78b-4570-aa70-7dac7af6c083)


### 2. Connect data to PBI and modelling

- Connect queries above and available tables of dataset to PBI
- Modelling
![image (13)](https://github.com/user-attachments/assets/d40a1a98-af3c-4667-b0c6-2acc13244d6d)


### 3. Build dashboard

- Using DAX to create measures and calculated columns
- Build 3 report pages

**Overview of Purchasing Operations**

![image (14)](https://github.com/user-attachments/assets/c0e3e075-22fb-445d-95ed-8fb2234c08f5)
Goal: Overview with most important KPIs of Purchasing Operations 


**Inventory Management**

![image (15)](https://github.com/user-attachments/assets/87631c61-6cd1-41cb-b78f-1a6bbf0baa45)
Goal: Provide an overview of current inventory, indicate products that need replenishment, and highlight inventory turnover.

**Vendor Profile and Performance**
![image (16)](https://github.com/user-attachments/assets/b5f4d8ef-700b-44ec-841d-d1619def785a)
Goal: Provide the profile and performance metrics of each vendor. Suitable for purchasing department for further analysis in the future.

## IV. Insights

#### Page 1. Overview of Purchasing Operations

- Net Purchase saw a significant increase from Q2 2013 at around 1.7 million USD, peaking in Q2 2014 at approximately 17 million USD (Note: Q3 2014 data is unavailable, so no conclusion can be made about a potential decline).
- AdventureWorks is sourcing a large proportion from non-preferred vendors, accounting for over 90%.
- Key KPIs like rejected rate and on-time delivery rate are at very good and stable levels.
- Spending from vendors with low credit ratings is at an acceptable level and provides stability for the company.


#### Page 2. Inventory Management
- Locations that are occupying the highest amount of inventory are Subassembly (95K units) and Miscellaneous Storage (83K units), but have low total inventory values (3.3M and 1.5M, respectively) => Store many items that are low-value
- Location Final Assembly and Finished Goods Storage, although not having a high inventory volume (20K and 17K, respectively), have the highest total inventory value (13.6M and 12.2M respectively) => Store items that are high-value.

  

## V. Recommendations
- Optimize Vendor Selection: Shift focus towards preferred vendors to improve supply stability and credit rating. Monitor vendors with low credit ratings but stable performance to reduce risk.

- Improve Inventory Replenishment: Address the 69 SKUs below safety stock immediately to prevent shortages. Enhance forecasting and reduce lead times to improve the Inventory Turnover Ratio.

- Implement Inventory Tracking Over Time: The current dataset contains no inventory data  over time. Set up a system to regularly capture and store inventory data at key intervals (daily, weekly, or monthly) to enable trend analysis, forecasting, and better inventory management decisions.

- Strategic Inventory Management: Rebalance inventory across locations to avoid congestion and manage high-value items like HL Mountain Frames carefully to maintain optimal stock levels.









