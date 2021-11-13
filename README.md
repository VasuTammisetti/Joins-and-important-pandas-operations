# Joins-and-important-pandas-operations

pandas provides various facilities for easily combining together Series or DataFrame with various kinds of set logic for the indexes and relational algebra functionality in the case of join / merge-type operations.

In addition, pandas also provides utilities to compare two Series or DataFrame and summarize their differences.




**Concatenating objects**
The concat() function (in the main pandas namespace) does all of the heavy lifting of performing concatenation operations along an axis while performing optional set logic (union or intersection) of the indexes (if any) on the other axes



**Set logic on the other axes**
When gluing together multiple DataFrames, you have a choice of how to handle the other axes (other than the one being concatenated). This can be done in the following two ways:

Take the union of them all, join='outer'. This is the default option as it results in zero information loss.

Take the intersection, join='inner'.


**
Concatenating using append**
A useful shortcut to concat() are the append() instance methods on Series and DataFrame. These methods actually predated concat. They concatenate along axis=0, namely the index:

https://pandas.pydata.org/pandas-docs/stable/user_guide/merging.html
