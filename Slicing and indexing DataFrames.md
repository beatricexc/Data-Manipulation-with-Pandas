# Chapter 3. Slicing and Indexing DataFrames
Indexing is used to make subsetting code cleaner with .loc[[""]] and .iloc[]
- .loc filters on index values
- pass the value name you want into the list, and .loc will filter that for you


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

![image](https://user-images.githubusercontent.com/72341578/151886824-28bd36e9-ab7d-4a05-bd92-b844c1d9d71c.png)


- "color" is the inner level and the implication is that the inner level is nested inside the outer level "breed"
- to subset on the outer level we use a list 
- 
![image](https://user-images.githubusercontent.com/72341578/151887408-10924cc0-bc45-4db0-a1f2-c99ab5f5288b.png)

- to subset on the inner level, we need to pass a list of tuples ( the resulting rows need to match all conditions in order to be returned)

![image](https://user-images.githubusercontent.com/72341578/151887344-133cf139-ef60-4754-bd55-782757dfa93d.png)

#### Sorting by index values 
- using the .sort_index() by default from outer to inner in ascending order
- controlling the sorting by passing lists to te *level* and the *ascending* argument

![image](https://user-images.githubusercontent.com/72341578/151887741-07708418-afc6-4cd0-8da4-7a15880ffae3.png)

 Subsetting 
 - using square brackets 
 
![image](https://user-images.githubusercontent.com/72341578/151889849-be162f11-73fe-4495-9657-97d83ea3d13a.png)

- using .iloc[]

![image](https://user-images.githubusercontent.com/72341578/151889914-c3a13833-ccc8-4e9c-9b75-bcd32c264e2d.png)

**Output** 

![image](https://user-images.githubusercontent.com/72341578/151890017-1ca303e6-6ca1-4e09-993c-09f845da0bbe.png)


![image](https://user-images.githubusercontent.com/72341578/151890062-983cf058-5bcd-431d-9f00-3f9d2a783a9e.png)

### Slicing 
- you can slice a list by stating the index position [2:4] etc.
- if you want to slice a dataframe, you first need to sort the index before slicing 

![image](https://user-images.githubusercontent.com/72341578/151891761-c7a0a4dd-6605-49b7-bb9e-ba5ad4d28a5a.png)

- slicing at the outer level with .loc by passing the first and last column separated by ":" 

![image](https://user-images.githubusercontent.com/72341578/151891854-d4fce1ac-f770-4815-abac-95a344a23098.png)

- slicing at the inner level by passing the first and last positions as tuples 

![image](https://user-images.githubusercontent.com/72341578/151892009-cb0fb7f1-33ab-4dd6-8928-1e29f6ed9d09.png)

- since df are two-dimensional objects, we can also slice columns by passing 2 arguments to .loc
                  - subsetting columns but keeping all rows df_st.loc[:, " " : " " ] 

 ![image](https://user-images.githubusercontent.com/72341578/151895313-d36e5af8-4633-4f67-b515-2fdb438efa04.png)

- slice twice 

 ![image](https://user-images.githubusercontent.com/72341578/151895406-709a7e76-fbbe-4b15-8bfe-f320030e9727.png)



