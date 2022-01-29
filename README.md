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

#### Subsetting columns
- dfname[" "]
- dfname[[" ", " "]] - subsetting multiple columns

#### Subsetting rows 
- the easiset way is to create a logical condition to filter it: dfname[ "column name"] > 50
- subsetting based on text data eg: dogs[dogs["breed"] == "Labrador"]
- subsetting based on dates: dogs[dogs["data_of_birth"] == "2014-02-01"] yyyy/mm/dd (international format)
- subsetting based on multiple conditions : 

                                            eg. is_lab = dogs["breed] == "Labrador" 
                                                is_brown = dogs["color"] == "Brown"
                                                
                                                dogs[is_lab & is_brown]  
  or in one line of code
                                                
                                                dogs[(dogs["breed"] == "Labraddor") & (dogs["color"] == "Brown)]

                                        
- filtering on multiple values of categorical variable with the .isin() method ![image](https://user-images.githubusercontent.com/72341578/151679689-183ce6fd-076d-4ad5-885b-a5432e3990f2.png)
