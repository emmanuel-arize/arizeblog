---
layout: Power-Query-post
title: Data Transformation using Power Query
author: Emmanuel Arize
category: Power-Query
---

The number one issue facing data analyst when building robust and stable solutions has been accessing,
cleansing and transforming the data but with the integration of Power Query into all the data analysis and business intelligence tools from Microsoft such as Excel, Power BI and Analysis Services, data accessing, cleansing and transformation has been made easy because Power Query is designed to be an easy to use data accessing, transformation and manipulation tool. In this post I will be illustrating how to clean and transform data using power query. Before the cleansing and transformation I'll assume you have been given a project to complete and as analyst you've define a clear measurable and quantifiable goal for the project, your audience have been identified and any other requirements are also met. You now have the required data for the project but you've seen that the data is in state not suitable for analysis so you've decided to condition or transform the data to suit your analysis. Transforming the data to suit your analysis is a critical step in the data analysis process as it helps to ensure that the data is in a format that is suitable for analysis and modeling, and that it is free of errors and inconsistencies. A failure to transform the data to suit your analysis will result in producing faulty output as there is the popular saying among the data analyst community which state "garbage in, garbage out" which simply means "incorrect or poor input will produce faulty output".

### What is Data Transformation?

Data transformation is the process of converting, cleansing, and structuring data into a usable format that can be used for analysis and modeling. The goal of data transformation is to prepare the data so that it can be used to extract useful insights and knowledge. Data transformation include data cleaning, data integration, normalization, scaling, reduction, discretization, aggregation and many more.

### Sample Data

To work through the examples in this post, you need to download the data used in  this post from <a href="https://github.com/emmanuel-arize/Power-Query/blob/main/data/Life-Expectancy-At-Birth.xls" target="_blank">Life-Expectancy-At-Birth.xls</a> and load it into power query as shown below

<br>
<img class="w3-card" src="{{'/assets/images/power_query/trans_1.jpg' |relative_url}}">
<br>

## Data Transformation

From the data above we can see that power query was not able to determine correctly the column headers of the data loaded. Looking at the data we can see that the actual column headers for the data is Row 1 but because power query could not determine it correctly, it labels the column headers as column1, column2 and in that order.

### Promote Headers Operation

Sometimes the actual column headers of the table is the first row as seen above but because power query could not determine it correctly it labels the column headers incorrectly and this need to be corrected. With the promote headers operation, it promotes the first row of values as the new column headers. There are a number of places where we can select the promote headers operation (**Use First Row as Headers** )

Click on the Home tab then in the Transform group

<br>
<img class="w3-card" src="{{'/assets/images/power_query/append_5.jpg' |relative_url}}">
<br>

Or On the Transform tab, in the Table group.

<br>
<img class="w3-card" src="{{'/assets/images/power_query/append_6.jpg' |relative_url}}">
<br>

After clicking on Use First Row as Headers, the first row in the query is used as the column headers of the query and we get the table below

<br>
<img class="w3-card" src="{{'/assets/images/power_query/trans_2.jpg' |relative_url}}">
<br>

### Remove columns

Remove columns is an operations that help you define what columns your table needs to remove. From the data the columns named **Indicator Name** and **Indicator Code** contain data not relevant to our analysis so we need to remove them.
To remove these columns select the columns to remove, in our case the column **Indicator Name** and **Indicator Code**
as below

<br>
<img class="w3-card" src="{{'/assets/images/power_query/trans_3.jpg' |relative_url}}">
<br>

then **right click** and select **Remove Columns** to remove the selected columns. **Remove Columns can also be found on the Home tab**. With the unwanted columns removed we now have the table given below

<br>
<img class="w3-card" src="{{'/assets/images/power_query/trans_4.jpg' |relative_url}}">
<br>

### Filtering the Data

From the data some countries such as **Andorra, American Samoa** etc, contain null values throughout, so we need to filter out such rows from the data. Since this can be completed using the M language, I will use the **Advanced Editor** which can be located on the Home tab of the query editor. To open the Advanced Editor

- Click on the **home tab** then **Advanced Editor**

When the Advanced Editor is clicked it will opened an editor similar to one below

<br>
<img class="w3-card" src="{{'/assets/images/power_query/trans_5.jpg' |relative_url}}">
<br>

With the Advanced Editor opened I will write M code named **#"RemoveNullRows"** to remove any row containing null value under the column named 1960. The code is given below

<br>
<img class="w3-card" src="{{'/assets/images/power_query/trans_6.jpg' |relative_url}}">
<br>

with the null values removed we now have a table as the one below

<br>
<img class="w3-card" src="{{'/assets/images/power_query/trans_7.jpg' |relative_url}}">
<br>

**NOTE:** The filtering of the 1960 column to remove of null values can also be achieved by selecting the 1960 column then from the Home tab under the **Remove Rows drop-down options** in the Reduce Rows group select **Remove blank rows**.
Remove blank rows remove any null and blank values.


### Unpivot columns

given a table like the one above, where country rows and date columns create a matrix of values, it's difficult to analyze the data in a scalable way. In such cases we might want to unpivot or flatten the data, to put it in a matrix format so that all similar values are in one column. To unpivot the table to have country, country code ,year and life Expectancy at birth as columns select the country and country code columns as below

<br>
<img class="w3-card" src="{{'/assets/images/power_query/trans_8.jpg' |relative_url}}">
<br>

right on the selected columns and select **Unpivot Other Columns**. This give the table below

<br>
<img class="w3-card" src="{{'/assets/images/power_query/trans_9.jpg' |relative_url}}">
<br>

Now rename the **Attribute** column to **Year** and **Value** to **Life_Expentancy_At_Birth**. Sort the data in ascending order based on the Year column. This give the table as below

<br>
<img class="w3-card" src="{{'/assets/images/power_query/trans_10.jpg' |relative_url}}">
<br>

The M code for all the transformation perform is this post is given as

<br>
<img class="w3-card" src="{{'/assets/images/power_query/trans_11.jpg' |relative_url}}">
<br>
