##### Introduction Dataframes
- df.head()
- df.info()
- df.shape
- df.describe()
- `df.values` : A two dimensional NumPy array of values
- `df.columns` : An index of columns: the column names
- `df.index` : An index for the rows, either row number or row name

##### Sorting and subsetting

![[Pasted image 20240323104552.png]]


![[Pasted image 20240323104638.png]]

![[Pasted image 20240323105743.png]]

##### Adding new columns

![[Pasted image 20240323150636.png]]

##### Summary Statistics

![[Pasted image 20240323171934.png]]

- `dogs['weight_kg].cumsum()` : Cumulative sum
- `dogs['weight_kg].cummax()` Cumulative Maximum
- `dogs['weight_kg].cummin()` Cumulative Minimum
- `dogs['weight_kg].cumprod()` Cumulative Produce

##### Counting

![[Pasted image 20240323180215.png]]

- `unique_dogs['breed'].value_counts(sort=True)`
- `unique_dogs['breed'].value_counts(normalize=True)` 

##### Grouped summary statistics

![[Pasted image 20240323192639.png]]

![[Pasted image 20240323192656.png]]

##### Pivot tables

![[Pasted image 20240323195730.png]]

![[Pasted image 20240323195924.png]]

![[Pasted image 20240323200045.png]]

##### Explicit indexes

- dogs.columns
- dogs.index
- dogs.set_index("name")
- dogs.reset_index()
- dogs.reset_index(drop=True)
![[Pasted image 20240324162956.png]]
- dogs.sort_index()
![[Pasted image 20240324163122.png]]

##### Slicing and subsetting 

![[Pasted image 20240324174851.png]]

![[Pasted image 20240324174904.png]]

![[Pasted image 20240324174946.png]]

![[Pasted image 20240324175000.png]]

![[Pasted image 20240324175016.png]]

![[Pasted image 20240324175052.png]]

- Can slice dates by partial values, of just year.

##### Working with pivot tables

- df.mean(axis="index")
- You can access the components of a date (year, month and day) using code of the form `dataframe["column"].dt.component`. For example, the month component is `dataframe["column"].dt.month`, and the year component is `dataframe["column"].dt.year`.
```
# Get the worldwide mean temp by year

mean_temp_by_year = temp_by_country_city_vs_year.mean(axis='index')

  

# Filter for the year that had the highest mean temp

print(mean_temp_by_year[mean_temp_by_year == mean_temp_by_year.max()])

  

# Get the mean temp by city

mean_temp_by_city = temp_by_country_city_vs_year.mean(axis="columns")

  

# Filter for the city that had the lowest mean temp

print(mean_temp_by_city[mean_temp_by_city == mean_temp_by_city.min()])
```

##### Visualizing your data

![[Pasted image 20240324190941.png]]

![[Pasted image 20240324191013.png]]

![[Pasted image 20240324191040.png]]

![[Pasted image 20240324191136.png]]

##### Missing Values

- dataframe.isna()
- dataframe.isna().any()
- dataframe.isna().sum()
![[Pasted image 20240324211042.png]]
- dataframe.dropna()
- dataframe.fillna(0)

##### Creating Dataframe

![[Pasted image 20240325191756.png]]

![[Pasted image 20240325191820.png]]

![[Pasted image 20240325191909.png]]

##### Reading and writing CSVs

![[Pasted image 20240325193359.png]]

![[Pasted image 20240325193438.png]]

##### Inner Join

![[Pasted image 20240325202422.png]]

![[Pasted image 20240325202405.png]]

![[Pasted image 20240325202501.png]]

##### One- to-many relationship
![[Pasted image 20240327182343.png]]

![[Pasted image 20240327182357.png]]

![[Pasted image 20240327221144.png]]

![[Pasted image 20240327221247.png]]

##### Left Join

![[Pasted image 20240328193129.png]]

- A left join will return all of the rows from the left table. If those rows in the left table match multiple rows in the right table, then all of those rows will be returned. Therefore, the returned rows must be equal to if not greater than the left table. Knowing what to expect is useful in troubleshooting any suspicious merges.

##### Right Join

![[Pasted image 20240328194712.png]]

##### Outer Join

![[Pasted image 20240328195010.png]]

##### Merging a table to itself

![[Pasted image 20240328205401.png]]

![[Pasted image 20240328205436.png]]

![[Pasted image 20240328205509.png]]

##### Merging on indexes

![[Pasted image 20240329153120.png]]


![[Pasted image 20240329153016.png]]

![[Pasted image 20240329153214.png]]

![[Pasted image 20240329153410.png]]

##### Filtering joins

![[Pasted image 20240329185234.png]]

![[Pasted image 20240329185246.png]]

![[Pasted image 20240329185420.png]]

![[Pasted image 20240329201719.png]]

![[Pasted image 20240329201757.png]]

![[Pasted image 20240329201849.png]]

![[Pasted image 20240329201918.png]]

![[Pasted image 20240329201927.png]]

##### Concatenate DF together vertically

![[Pasted image 20240330184149.png]]

![[Pasted image 20240330184205.png]]

![[Pasted image 20240330184224.png]]

![[Pasted image 20240330184334.png]]

##### Verifying integrity

![[Pasted image 20240331151334.png]]


![[Pasted image 20240331145207.png]]

![[Pasted image 20240331145232.png]]

![[Pasted image 20240331150731.png]]

![[Pasted image 20240331150754.png]]

##### Using merge_ordered()

![[Pasted image 20240331153640.png]]

- The results are sorted
- Ordered data / time series
- Filling in missing values

![[Pasted image 20240331154133.png]]

![[Pasted image 20240331154413.png]]

![[Pasted image 20240331154456.png]]

##### merge_asof()

![[Pasted image 20240331171427.png]]

![[Pasted image 20240331173251.png]]

![[Pasted image 20240331173320.png]]

- Data sampled from a process
- Developing a training set (no data leakage)
- direction='forward' or 'nearest'

##### Selecting data with .query()

![[Pasted image 20240401160731.png]]

 ![[Pasted image 20240403173230.png]]

##### Reshaping data with .melt()

- When information on the other columns is related to the value of the other column, it's called wide.
- If one subject is related to many rows, it's called long
![[Pasted image 20240403174606.png]]

- Melt will help to transfer from wide to long
![[Pasted image 20240403174906.png]]

![[Pasted image 20240403174917.png]]

![[Pasted image 20240403175005.png]]

![[Pasted image 20240403175045.png]]

