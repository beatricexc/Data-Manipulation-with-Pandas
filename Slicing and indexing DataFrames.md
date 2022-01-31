# Chapter 3. Slicing and Indexing DataFrames
Indexing is used to make subsetting code cleaner with .loc[[""]] and .iloc[]
.loc filters on index values
pass the value name you want into the list, and .loc will filter that for you


#### Setting the column as the index with .set_index("name") 

![image](https://user-images.githubusercontent.com/72341578/151882510-3331e067-c507-4d1f-897c-88507260a3d2.png)

- the index values are now left aligned
- the index values don't have to be unique
- resetting or removing the index is done with .reset_index()
- .reset_index() has a drop argument which allows us to discard an index :

                                                  df_ind.reset_index(drop = True) # entirely removes the dog names (below)
                                                  
![image](https://user-images.githubusercontent.com/72341578/151882933-7ddb3e0e-8a9e-4faf-8215-3819d244e075.png)

#### Multi-level indexes a.k.a hierarchical indexes
- new_variable = df.set_index(["", ""])
- 
![image](https://user-images.githubusercontent.com/72341578/151886824-28bd36e9-ab7d-4a05-bd92-b844c1d9d71c.png)


- "color" is the inner level and the implication is that the inner level is nested inside the outer level "breed". 
