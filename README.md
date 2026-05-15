
#  Diwali Sales Data Analysis

##  Project Overview

This project explores customer purchasing behavior during the Diwali festival season using Python-based data analysis techniques. The analysis focuses on identifying customer demographics, purchasing patterns, high-performing product categories, and business insights that can help improve sales strategies.

The project aims to uncover meaningful insights from the Diwali sales dataset and demonstrate practical data analysis and visualization skills.

---

##  Objectives

The primary objectives of this project were:

* Analyze customer demographics during Diwali sales
* Identify top-performing product categories
* Understand purchasing behavior across different states and occupations
* Discover which customer segments contribute the most revenue
* Generate business insights using exploratory data analysis (EDA)

---

#  Tools & Technologies Used

* **Python** – Core programming language used for analysis
* **Pandas** – Data cleaning and manipulation
* **NumPy** – Numerical computations
* **Matplotlib** – Data visualization
* **Seaborn** – Statistical data visualization
* **Jupyter Notebook** – Interactive analysis environment
* **Git & GitHub** – Version control and project sharing

---

#  Project Structure

```bash
Diwali-Sales-Analysis/
│
├── Diwali_Data_Analysis.ipynb
├── Diwali Sales Data.csv
├── README.md
└── images/
```

---

#  Exploratory Data Analysis (EDA)

## 1️Data Cleaning

Before starting the analysis, the dataset was cleaned by:

* Removing null values
* Dropping unnecessary columns
* Correcting data types
* Handling missing values
* Preparing the dataset for visualization and analysis

### Key Learning

Data cleaning is one of the most important steps in data analysis because accurate insights depend on clean and reliable data.

---

## 2️Gender Analysis

The analysis explored purchasing behavior based on gender.
```python
# plotting a bar chart for Gender and it's count

ax = sns.countplot(x = 'Gender',data = df)

for bars in ax.containers:
    ax.bar_label(bars)
```
<img width="395" height="262" alt="download" src="https://github.com/user-attachments/assets/d2b24a47-5970-4789-a607-d7fb2cd41cfa" />

###  Key Insights

* Female customers contributed more to total purchases compared to male customers
* Women showed higher purchasing power during the Diwali season
* Female shoppers represented a larger share of the customer base

### Business Insight

Businesses can target female customers more effectively through personalized marketing campaigns and festive offers.

---

## 3️ Age Group Analysis

Customer purchases were analyzed across different age groups.
```python
ax = sns.countplot(data = df, x = 'Age Group', hue = 'Gender')

for bars in ax.containers:
    ax.bar_label(bars)
```

<img width="395" height="262" alt="download" src="https://github.com/user-attachments/assets/2725af18-2ef6-4b27-8336-520301992723" />

### 📈 Key Insights

* Customers aged between **26–35 years** contributed the highest number of purchases
* Young adults were the most active shoppers during the festival season
* Both male and female customers in this age group showed strong purchasing behavior

###  Business Insight

Brands can focus their festive campaigns on young working professionals and young families.

---

## 4️State-wise Analysis

The analysis identified states with the highest sales and order volumes
```python
sales_state = df.groupby(['State'], as_index=False)['Orders'].sum().sort_values(by='Orders', ascending=False).head(10)

sns.set(rc={'figure.figsize':(15,5)})
sns.barplot(data = sales_state, x = 'State',y= 'Orders')


```
<img width="899" height="321" alt="download" src="https://github.com/user-attachments/assets/08c8cf02-238c-4948-b3e9-f482026f0af0" />


### Top Contributing States

* Uttar Pradesh
* Maharashtra
* Karnataka
* Delhi

### Business Insight

These states represent major revenue-generating regions and can be prioritized for future marketing and inventory planning.

---

## 5️ Marital Status Analysis

The project explored the relationship between marital status and purchasing behavior.
```python
sales_state = df.groupby(['Marital_Status', 'Gender'], as_index=False)['Amount'].sum().sort_values(by='Amount', ascending=False)

sns.set(rc={'figure.figsize':(6,5)})
sns.barplot(data = sales_state, x = 'Marital_Status',y= 'Amount', hue='Gender')

```
<img width="378" height="330" alt="download" src="https://github.com/user-attachments/assets/3708dcf8-9922-4015-a94c-b61906810c9a" />

### 📈 Key Insights

* Married women contributed significantly to total sales
* Married customers had higher purchasing activity during Diwali

### Business Insight

Family-oriented products and festive bundles may perform better among married customers.

---

## 6️ Occupation Analysis

Purchasing trends were analyzed based on customer occupation.
```python
sales_state = df.groupby(['Occupation'], as_index=False)['Amount'].sum().sort_values(by='Amount', ascending=False)

sns.set(rc={'figure.figsize':(20,5)})
sns.barplot(data = sales_state, x = 'Occupation',y= 'Amount')
```

<img width="1169" height="330" alt="download" src="https://github.com/user-attachments/assets/d4f3df15-76a4-434a-8b17-b1f60c642097" />


### Key Insights

Customers working in the following sectors contributed the highest sales:

* IT Sector
* Healthcare
* Aviation
* Banking

###  Business Insight

Professionals with stable income groups tend to spend more during festive seasons.

---

## 7️Product Category Analysis

The project identified the most popular product categories during Diwali sales.
```python
sales_state = df.groupby(['Product_Category'], as_index=False)['Amount'].sum().sort_values(by='Amount', ascending=False).head(10)

sns.set(rc={'figure.figsize':(20,5)})
sns.barplot(data = sales_state, x = 'Product_Category',y= 'Amount')

```
<img width="1169" height="330" alt="download" src="https://github.com/user-attachments/assets/271ce5da-7c64-4f03-94af-5363ae30cfa9" />


Top Product Categories

* Food
* Clothing & Apparel
* Electronics
* Footwear

### Business Insight

Retailers can optimize inventory and promotional campaigns around these high-demand categories during festive seasons.

---

#  Skills Demonstrated

Through this project, I strengthened my skills in:

* Data Cleaning & Preprocessing
* Exploratory Data Analysis (EDA)
* Data Visualization
* Statistical Insights
* Business Problem Solving
* Python Programming
* Pandas & Seaborn Libraries

---

#  Key Takeaways

* Customer demographics strongly influence purchasing behavior
* Female customers and young adults were major contributors to sales
* Festive shopping trends vary significantly across states and occupations
* Data analysis helps businesses make informed marketing and inventory decisions

---

# Conclusion

This project provided valuable hands-on experience in real-world data analysis using Python. By analyzing Diwali sales data, I gained practical exposure to:

* Cleaning and transforming raw datasets
* Performing exploratory data analysis
* Creating meaningful visualizations
* Extracting actionable business insights

The project highlights how data-driven decisions can help businesses better understand customer behavior and improve sales performance during festive seasons.

---


