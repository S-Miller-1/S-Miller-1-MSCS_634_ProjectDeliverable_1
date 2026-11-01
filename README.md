# MSCS 634 — Project Deliverable 1

### Data Collection, Cleaning, and Exploration

**Student:** Shawn
**Course:** MSCS 634 — Data Mining
**Project:** Advanced Data Mining for Data-Driven Insights and Predictive Modeling

## About This Project

For this project, I worked with an online retail dataset to learn more about sales and customer shopping habits. I used Python and Jupyter Notebook to look through the information, clean up problems, and create graphs to see what patterns I could find.

The main goal of this first assignment was to get the data ready for the next parts of the project. Later on, I'll be using the same information to make predictions and look for patterns using machine learning.

## The Dataset

I used the Online Retail dataset from the UCI Machine Learning Repository.

The dataset has **541,909 records and 8 columns**. It contains sales information from an online store in the United Kingdom between December 2010 and December 2011.

The information includes:

* Invoice numbers and product codes
* Product names and descriptions
* How many items were purchased
* The date of each purchase
* Product prices
* Customer IDs
* The country where the purchase was made

I chose this dataset because it has plenty of information to work with. I can use it to compare sales, see which countries purchase the most, and find patterns in customer orders.

It also gives me different options for the machine learning parts of the project.

## Cleaning the Data

Before making any graphs, I checked the dataset for problems.

I found missing information, duplicate records, canceled orders, and some unusual values.

**Missing Information**

There were 1,454 records missing product descriptions and 135,080 records missing customer IDs.

I removed records that were missing information needed to analyze product sales. However, I kept records with missing customer IDs because they could still be useful when looking at overall sales.

When I work with individual customers later, I'll only use records with valid customer IDs.

**Duplicate Records**

I found and removed 5,268 duplicate rows.

I wanted to make sure the same information wasn't being counted more than once. However, I also understand that some repeated purchases could be real transactions.

**Canceled Orders and Incorrect Values**

Some orders were canceled or had quantities and prices that were zero or negative.

Since I wanted to focus on completed sales, I separated the canceled orders and removed records that didn't make sense for this part of the analysis.

**Unusually Large Orders**

I also noticed that some purchases were much larger than others.

I decided to keep these because they could be legitimate bulk purchases. I didn't want to remove useful information just because the numbers were unusually high.

After cleaning everything, I had **524,878 records remaining**.

I also kept the original dataset unchanged in case I need to look back at anything.

## Exploring the Data

After cleaning the dataset, I created five graphs to see what I could learn.

### 1. Sales by Month

The first graph shows how sales changed from month to month.

I noticed that sales weren't consistent throughout the year. Some months had much higher sales than others, with November 2011 having the highest total.

December 2011 showed a large drop, but the dataset only included the first part of that month. Because of this, I wouldn't assume that sales actually dropped that much.

### 2. Sales by Country

The second graph compares sales between countries.

One thing that stood out was how much of the sales came from the United Kingdom.

The UK accounted for about **84.6% of the total sales**.

Outside the UK, the Netherlands and Ireland had some of the highest sales, followed by countries such as Germany and France.

This showed me that sales were not evenly spread between countries.

### 3. Sales Amounts

The third graph shows how much was spent on individual product lines.

The median amount was **£9.92**, while the average was **£20.28**.

I noticed that most product lines had smaller amounts, but some were much more expensive.

Those larger amounts made the average higher than the median.

This is something I'll need to keep in mind when working with prediction models later.

### 4. Unusually Large Orders

The fourth graph compares the total amounts of different invoices.

Most orders were relatively small, but a few were much larger.

The largest invoice was over **£168,000**, which was significantly higher than most of the others.

I kept these orders in the dataset because they could be real purchases.

I also learned that unusual values can affect the results, especially when calculating averages or building prediction models.

### 5. Quantity Compared with Price

The last graph compares how many items were purchased with the price of each item.

I noticed that buying more items didn't necessarily mean those items had higher prices.

Some orders had large quantities of cheaper products, while others had smaller quantities of more expensive products.

There wasn't much of a relationship between quantity and unit price.

This helped me understand that I need to look at more than one piece of information when trying to explain sales patterns.

## Challenges I Had

One of the challenges with this project was figuring out which records should be removed and which ones were still useful.

For example, a missing customer ID doesn't mean the sale never happened. I didn't want to remove thousands of purchases just because I couldn't identify the customers.

I also had to decide what to do with unusually large orders. Some of those numbers looked extreme, but that doesn't automatically mean they're wrong.

Another thing I noticed was that cleaning the data changes what the dataset represents. Once I removed cancellations and invalid sales, I was working with completed purchases rather than every transaction in the original file.

Overall, I learned that cleaning data isn't just about deleting rows. It's about understanding the information and making decisions that make sense for what I'm trying to study.

## Preparing for the Next Deliverables

This first part of the project helped me get familiar with the dataset and prepare it for future assignments.

For the next parts, I plan to use the information in a few different ways.

**Deliverable 2 — Regression**

I plan to build models that predict sales or order amounts. I'll compare different models to see which one gives better results.

**Deliverable 3 — Classification and Clustering**

I want to group customers based on their purchasing habits and classify orders into different categories.

I'll also look for products that customers frequently purchase together.

**Deliverable 4 — Final Project**

For the final deliverable, I'll bring everything together and explain the results, what I learned, and how the information could be useful to a business.

I'll also discuss the limitations of the data and any privacy concerns.

## Project Files

The project includes the following files:

| File                                        | Description                                               |
| ------------------------------------------- | --------------------------------------------------------- |
| `MSCS_634_ProjectDeliverable_1_Shawn.ipynb` | Jupyter Notebook with my Python code, graphs, and results |
| `Online Retail.xlsx`                        | Original retail dataset                                   |
| `Online_Retail_Cleaned.csv.gz`              | Cleaned dataset                                           |
| `cleaning_audit.csv`                        | Shows how many records remained after cleaning            |
| `figures/`                                  | Contains the five graphs                                  |
| `requirements.txt`                          | Python libraries needed to run the project                |

## How to Run the Project

To open and run the project:

1. Download the project files.
2. Make sure Python and Jupyter Notebook are installed.
3. Open Command Prompt inside the project folder.
4. Install the required libraries using `py -m pip install -r requirements.txt`.
5. Start Jupyter using `py -m notebook`.
6. Open `MSCS_634_ProjectDeliverable_1_Shawn.ipynb`.
7. Run the notebook cells from top to bottom.

The original Excel dataset needs to be in the same folder as the notebook.

Running the notebook will create the cleaned dataset and save the graphs.

## Conclusion

This project helped me get more comfortable working with larger datasets in Python.

I learned how to find missing information, remove duplicate records, separate canceled orders, and create graphs to better understand sales information.

The graphs showed me that sales can vary quite a bit depending on the month, country, and size of the purchase.

I also learned that the decisions made while cleaning data can change the results, so it's important to understand what each step does.

I think this dataset will work well for the next parts of the project, especially when I start using machine learning to make predictions and find more patterns.

## Dataset Source

Chen, D. (2015). *Online Retail*. UCI Machine Learning Repository.

https://doi.org/10.24432/C5BW33

The dataset is provided under a CC BY 4.0 license.
