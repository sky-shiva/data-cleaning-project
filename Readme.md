# This is my first data-cleaning-project

There are some steps in data cleaning project the steps are :

# Cleaning Headers and Column names
first of we will do df.columns.to_list() --> this will help us to view the column names in the form of list 

problems we will get their are :

1) spaces before the header names and spaces after the header names and the solution for this is using str.strip() because the data is in the form of string so we are using str.strip() this will help us to trim the unwanted spaces in the dataset

2) And better to keep the names of the columns in lower case in this case we will use str.lower() and , if the spaces are in between we will use the str.replace(' ','_') 

Now lets print the fix

# Type conversion and currency cleaning in the data set 

Those dollar symbols ($) make them strings, not numbers.
So your analysis/calculations would break.

$1,234.56
$987.00
$42.50

🔹 Step 1 — Convert everything to a string
df['spend'] = df['spend'].astype(str)

🔹 Step 2 — Remove currency characters manually
df['spend'] = df['spend'].str.replace('$', '').str.replace(',', '')


Here we manually strip out the characters that don't belong in a number:

'$' → dollar sign

',' → comma separators

After this step:

"$1,234.56"  ➜  "1234.56"

🔹 Step 3 — Convert cleaned strings into numeric values
df['spend'] = pd.to_numeric(df['spend'])


This transforms the cleaned string into an actual float, so you can:

perform calculations

aggregate spending

sort numerically

visualize data

Example:

"1234.56"  ➜  1234.56 (float)

After processing, the spend column becomes clean, numeric, and analysis-ready — no currency symbols, no commas, just pure numbers.

# why i have taken demo.ipynb and demo.csv

see i have taken demos because to explain clearly about the replacing of correct values you can understand by seeing the code in demo.ipynb
