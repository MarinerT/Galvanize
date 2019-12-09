# Notes for Pandas

## Loading the Files
* There are several ways to load files:
  * df = pd.read_csv('filename', *options*) 
    https://pandas.pydata.org/pandas-docs/stable/user_guide/io.html 
  * df = pd.DataFrame({*label*: *Series*, etc. })
  * S = pd.Series([*array of values*], index = [*array of possibly categorical values*])
  
 ## Accessing Data within the DF
 ### .loc & .iloc
 * Use .loc to retrieve values based on value like a name
  Examples: 
  To retrieve columns:
    produce.loc[:,produce.max() > 5] says 1. locate all rows "[:, " 2. and columns where the max value is greater than 5.
  To retrieve a row: 
    produce.loc[produce['price'] == 1,:] says 1. locate all columns "[,:]" where just produce df's 'price' column value is 1. 
  
 * Use .iloc to retrieve values based on indexes
 
 ### Adding/Removing Columns
 * To add a column just set as you would set a variable. df['new column'] = df['col1'] * df['col2'] you can broadcast.
 * To remove a column, produce.drop('col1', axis=1). To do it permanently use 'inplace', produce.drop('col1',axis=1, inplace=True)
 
 ## Merging DataFrames
 ## pd.concat(array)
 * put all df in a list like frames = []
 * mergeddf = pd.concat(frames) (by columns)
 * mergeddf = pd.concat(frames, axis=1)
 ## pd.merge(df1,df2, how='',on='') 
 *'how' can specify whether inner or outer, left/right.  see documentation
 * Documentation: https://pandas.pydata.org/pandas-docs/stable/user_guide/merging.html
 
 ## Sorting the Data
 Useful Site: https://jakevdp.github.io/PythonDataScienceHandbook/03.08-aggregation-and-grouping.html
 
 ### Split 
 * groupby('col') - same as in SQL but more powerful
 
 ### Apply
 * .aggregate() returns a single number for such an event like the mean for each row (or category in a groupby)
 example: groupedcategories.aggregate(np.max)
 * .transform() changes the data based upon your needs but keeps the indices the same. 
 example: groupedcategories.transform(lambda x: x - x.mean())
 * .filter()
 example: groupedcategories.filter(lambda x: len(x) > 5)
 * .apply() can be substituted for the above methods.
 
 
 
 ### Combine
 
