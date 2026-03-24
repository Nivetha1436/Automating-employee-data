# Automating-employee-data

This project automates the processing and analysis of employee data using Python in Google Colab.
The system reads employee information from an Excel file, performs automatic calculations such as salary analysis and bonus calculation, and generates an updated report.

The automation helps reduce manual work and improves data accuracy when handling employee records.

Features

Upload employee data from Excel file

Automatic salary analysis

Department-based employee filtering

Automatic bonus calculation

Generate updated Excel report

Download processed employee data

Technologies Used

Python

Google Colab

Pandas Library

Openpyxl Library

Microsoft Excel

Project Workflow
Employee Excel File
        ↓
Upload File to Google Colab
        ↓
Read Data using Pandas
        ↓
Process Employee Data
        ↓
Salary Analysis & Bonus Calculation
        ↓
Generate Updated Excel Report
Installation / Setup
Step 1 – Open Google Colab

Go to:

https://colab.research.google.com

Create a New Notebook.

Step 2 – Install Required Libraries
!pip install pandas openpyxl

Libraries used:

pandas – data processing and analysis

openpyxl – reading and writing Excel files

Usage
Upload Employee Data File
from google.colab import files
uploaded = files.upload()

Example file:

employee_data.xlsx
Read Employee Data
import pandas as pd

df = pd.read_excel("employee_data.xlsx")
df.head()
Salary Analysis
print("Average Salary:", df["Salary"].mean())
print("Maximum Salary:", df["Salary"].max())
print("Minimum Salary:", df["Salary"].min())
Filter Employees by Department
it_employees = df[df["Department"] == "IT"]
print(it_employees)
Bonus Calculation
df["Bonus"] = df["Salary"] * 0.10
Save Updated File
df.to_excel("updated_employee_data.xlsx", index=False)

Download the file:

files.download("updated_employee_data.xlsx")
Example Employee Dataset
ID	Name	Department	Salary	Experience
1	Ravi	IT	50000	3
2	Priya	HR	45000	4
3	Arun	IT	60000	5
Output Example
ID	Name	Department	Salary	Bonus
1	Ravi	IT	50000	5000
2	Priya	HR	45000	4500
3	Arun	IT	60000	6000
Advantages

Reduces manual data processing

Improves accuracy

Saves time

Easy to implement

Suitable for small HR data analysis

Future Enhancements

Add graphical salary analysis

Connect with database systems

Create employee dashboard

Integrate with web applications
