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
- - `unique_dogs['breed'].value_counts(normalize=True)`
- 