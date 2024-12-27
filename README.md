### Crowdfunding Data Analysis Using Excel


**Background**

Crowdfunding platforms like Kickstarter and Indiegogo have been growing in success and popularity since the late 2000s. From independent content creators to famous celebrities, more and more people are using crowdfunding to launch new products and generate buzz, but not every project has found success.
To receive funding, the project must meet or exceed an initial goal, so many organisations dedicate considerable resources looking through old projects in an attempt to discover “the trick” to finding success. 
For this assignment, I organised and analysed a database of 1,000 sample projects to uncover any hidden trends.

**Steps Followed,** 

- Using the Excel workbook, modify and analyse the sample-project data and try to uncover market trends.
- Use conditional formatting to fill each cell in the outcome column with a different colour, depending on whether the associated campaign was successful, failed, cancelled, or is currently live.
- Create a new column called Percent Funded that uses a formula to find how much money a campaign made relative to its initial funding goal.
- Use conditional formatting to fill each cell in the Percent Funded column according to a three-colour scale. The scale should start at 0 with a dark shade of red, and it should transition to green at 100 and blue at 200.
- Create a new column called Average Donation that uses a formula to find how much each project backer paid on average.
- Create two new columns, one called Parent Category and another called Sub-Category, that use formulas to split the Category and Sub-Category column into the two new, separate columns.

**Pivot Table**

![image](https://github.com/user-attachments/assets/e42cfb98-6a8e-4022-99f5-72ef54e2399b)

- Create a new sheet with a pivot table that analyses your initial worksheet to count how many campaigns were successful, failed, cancelled, or are currently live per category.
  ![image](https://github.com/user-attachments/assets/7aff616c-ab6d-48dd-be2e-01db8b26a281)
  
- Create a stacked-column pivot chart that can be filtered by country based on the table that you created.
- The dates in the deadline and launched_at columns use Unix timestamps. Create a new column named Date Created Conversion Formula used to to convert the data contained in launched_at into Excel's date format = (((A1/60)/60)/24)+DATE(1970,1,1)
  - Create a new column named Date Ended Conversion that will use =(((O2/60)/60)/24)+DATE(1970,1,1) to convert the data contained in deadline into Excel's date format.
  - Create a new sheet with a pivot table that has a column of outcome, rows of Date Created Conversion, values based on the count of outcome, and filters based on parent category and Years.
  ![image](https://github.com/user-attachments/assets/9c65007e-49d0-406d-b022-e3e78dd16a7c)

- Now, create a pivot-chart line graph that visualises this new table.
- Create a new sheet with 8 columns:
  - Goal
  - Number Successful
  - Number Failed
  - Number Cancelled
  - Total Projects
  - Percentage Successful
  - Percentage Failed
  - Percentage Cancelled
  - In the Goal column, create 12 rows with the following headers:
    - Less than 1000
    - 1000 to 4999
    - 5000 to 9999
    - 10000 to 14999
    - 15000 to 19999
    - 20000 to 24999
    - 25000 to 29999
    - 30000 to 34999
    - 35000 to 39999
    - 40000 to 44999
    - 45000 to 49999
    - Greater than or equal to 50000
- Using the COUNTIFS() formula, count how many successful, failed, and cancelled projects were created with goals within the ranges listed above. Populate the Number Successful, Number Failed, and Number Cancelled columns with these data points.
- Add up each of the values in the Number Successful, Number Failed, and Number Cancelled columns to populate the Total Projects column. Then, using a mathematical formula, find the percentage of projects that were successful, failed, or cancelled per goal range.
- Create a line chart that graphs the relationship between a goal amount and its chances of success, failure, or cancellation.
![image](https://github.com/user-attachments/assets/7b76cb27-1dda-4ee0-b6c7-fb9e08d69ba3)

**Statistical Analysis**

Most people would use the number of campaign backers to assess the success of a crowdfunding campaign. Creating a summary statistics table is one of the most efficient ways that data scientists can characterise quantitative metrics, such as the number of campaign backers.
For an additional challenge, evaluate the number of backers of successful and unsuccessful campaigns by creating your own summary statistics table.

- Create a new worksheet in your workbook, and create one column for the number of backers of successful campaigns and one column for unsuccessful campaigns
- Use Excel to evaluate the following values for successful campaigns, and then do the same for unsuccessful campaigns:
  - The mean number of backers
  - The median number of backers
  - The minimum number of backers
  - The maximum number of backers
- The variance of the number of backers
- The standard deviation of the number of backers
- Use your data to determine whether the mean or the median better summarises the data.
- Use your data to determine if there is more variability with successful or unsuccessful campaigns. Does this make sense? Why or why not?

- Create a report in Microsoft Word, and answer the following questions:
1.	Given the provided data, what are three conclusions that we can draw about crowdfunding campaigns?
2.	What are some limitations of this dataset?
3.	What are some other possible tables and/or graphs that we could create, and what additional value would they provide?

#### Reference

- [How to convert between date and Unix timestamp in Excel](https://www.extendoffice.com/documents/excel/2473-excel-timestamp-to-date.html)

- Data for this dataset was generated by edX Boot Camps LLC, and is intended for educational purposes only.


