### Data Aggregation 

#### Mean and Median

- df["column_name"].mean()
- df["column_name"].median()

#### Summarizing dates
The minimum and the maximum can help you see what time range the dataset covers. 
- df["date"].max()
- df["date"].min()


#### Efficient summaries
The .agg() method allows you to apply your own custom functions to a df


                                                    - df["column_name"].agg(function)
                                                 
                                                 
                                                 
 ![image](https://user-images.githubusercontent.com/72341578/151697432-961de1ae-2e9b-4925-9691-1c41ff8a469f.png)
    
                                             
- Cumulative Statistics 
- Counting
- Dropping Duplicates
- Counting categorical variables
- Grouped summary statistics
- Calculations with .groupby()
- Multiple group summaries
- Pivot tables
- Pivoting in one variable
- Fill in missing values and sum values with pivot tables
