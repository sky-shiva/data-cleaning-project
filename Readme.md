# This is my first data-cleaning-project

There are some steps in data cleaning project the steps are :

# Cleaning Headers and Column names
first of we will do df.columns.to_list() --> this will help us to view the column names in the form of list 

problems we will get their are :

1) spaces before the header names and spaces after the header names and the solution for this is using str.strip() because the data is in the form of string so we are using str.strip() this will help us to trim the unwanted spaces in the dataset

2) And better to keep the names of the columns in lower case in this case we will use str.lower() and , if the spaces are in between we will use the str.replace(' ','_') 

Now lets print the fix
