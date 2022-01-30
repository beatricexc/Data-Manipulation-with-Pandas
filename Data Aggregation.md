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
     
- using .agg() on multiple columns 
                  
                                                      df[["column_name1", "column_name2", "column_name3"]].agg(function)
                                                      
                                                      
                                                      
 ![image](https://user-images.githubusercontent.com/72341578/151698038-7d20d834-60c4-4834-966d-cb7a0916c2a1.png)
 
 
 - complex usage of .agg()
 
                                                    df[["column_name1", "column_name2", "column_name3"]]. agg([function, np.median]))
                                                    
                                                    
                                                    
  ![image](https://user-images.githubusercontent.com/72341578/151698174-d7e19767-0c9f-4a50-b5b7-bb9bcf438d93.png)


                                             
#### Cumulative Statistics 
Helpful in tracking summary statistics over time
- .cumsum()
- .cummax()

![image](https://user-images.githubusercontent.com/72341578/151698406-ead143d5-da9f-4dff-addd-3a1bc62b8535.png)


**Output** 

![image](https://user-images.githubusercontent.com/72341578/151698421-973d9ef3-7cfb-4ba3-ae3b-ed01bf922efa.png)


#### Counting 
Used with **categorical** values 
- dropping duplicate names .drop_duplicates(subset="name")
- dropping duplicate paris .drop_duplicates(subset=["name", "breed"])
- counting  

                                        
                                       variable_name["column_name"].value_counts() 
                                       variable_name["column_name"].value_counts(sort = True)    #descending order 
                                       variable_name["column_name].value_counts(normalize = True)  #getting the proportion of the column with the normalize argument 





#### Grouped summary statistics 

- Calculations with .groupby()
- Multiple group summaries
- Pivot tables
- Pivoting in one variable
- Fill in missing values and sum values with pivot tables
