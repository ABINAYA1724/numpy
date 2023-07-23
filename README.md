
#7.a).NumPy Program to convert a list of numeric value into a one dimensional NumPy array.


import numpy as np
l = list(map(float, input("Type number with space: ").split()))
print("Original List:",l)
a = np.array(l)
print("One-dimensional NumPy array: ",a)


#7.b).NumPy Program to convert a list and tuple into arrays.

import numpy as np
lst = list(map(float, input("Type number with space (list): ").split()))
print("Original List: ",lst)
print("List to array conversion: ")
print(np.asarray(lst))
tup= tuple(map(float, input("Type number with space (Tuple): ").split()))
print("Original Tuple: ",tup)
print("Tuple to array: ")
print(np.asarray(tup))


#8.a).Program to convert a NumPy array and series to data frames.

import numpy as np
arr = np.random.rand(3) 
print("Numpy array:")
print(arr)
#conversion of array to dataframe
import pandas as pd 
print("\nArray to DataFrame: ")
#conversion of array to series
series = pd.Series(arr)
print("Series:")
print(series)
# conversion of series to dataframe
df = pd.DataFrame({'A':series})
print("\nSeries to DataFrame:")
print(df)


#8.b).Programs to add,subtract,multiple and divide two pandas series.


import pandas as pd
ds1 = pd.Series([12, 45, 6, 81, 10])
ds2 = pd.Series([1, 3, 5, 7, 9])
ds = ds1 + ds2
print("Addition of two Series:")
print(ds)
print("Subtraction of two Series:")
ds = ds1 - ds2
print(ds)
print("Multiplication of two Series:")
ds = ds1 * ds2
print(ds)
print("Division of Series1 by Series2:")
ds = ds1 / ds2
print(ds)



#8.c).Programs to retrive and manipulate data using data frames.


import pandas as pd

# Create a DataFrame
data = {
    'Name': ['John', 'Alice', 'Bob', 'Charlie', 'Eva'],
    'Age': [25, 32, 28, 41, 36],
    'Country': ['USA', 'Canada', 'UK', 'USA', 'Australia'],
    'Salary': [5000, 7000, 6000, 8000, 6500]
}

df = pd.DataFrame(data)

# Retrieve data from the DataFrame

# Access a single column
name_column = df['Name']
print("Name column:")
print(name_column)

# Access multiple columns
age_salary_columns = df[['Age', 'Salary']]
print("\nAge and Salary columns:")
print(age_salary_columns)

# Access a single row by index
row_2 = df.loc[2]
print("\nRow at index 2:")
print(row_2)

# Access a subset of rows using conditions
usa_rows = df[df['Country'] == 'USA']
print("\nRows with Country as USA:")
print(usa_rows)

# Manipulate data in the DataFrame

# Add a new column
df['Bonus'] = df['Salary'] * 0.1
print("\nDataFrame with Bonus column:")
print(df)

# Update values in a column
df.loc[3, 'Age'] = 42
print("\nDataFrame with updated Age value:")
print(df)

# Delete a column
df.drop('Salary', axis=1, inplace=True)
print("\nDataFrame with Salary column deleted:")
print(df)

















