# Data-Manipulation-with-Pandas

### Transforming DataFrames
Inspecting a data frame: 
- .head() returns the first few rows
- .info() shows info on each of the columns, such as the data type and number of missing values
- .shape returns the number of rows and columns of the DataFrame
- .describe() calculates a few summary statistics for each column

#### Parts of the DataFrame
Dataframe objects are made of three components stored as attributes:
- .values: A two-dimensional NumPy array of values
- .columns: An index of columns, the colmns names
- .index: And index for the rows, either row numbers or row names

### Sorting and Subsetting
- .sort_values(" ") - change the order of the rows by sorting them
- .sort_values(" ", ascending = False) 
- .sort_values([" ", " "]) - sorting by multiple variables
- .sort_values([" ", " "], ascending = [True, False]) 
