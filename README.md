# Implementation of Geometric Distance Based Feature Selection
This package is intended for use with 'geometric distance based feature selection'.
For more information on this feature selection, please refer to 'https://github.com/seo-young-kim/GeometricDistanceBasedFeatureSelection'

~~~
pip install gdbfs 
~~~

## How to Use
Currently, only functions implemented in the sequential forward selection method exist.
Therefore, import sfs of the package and use it with fit() function.

~~~
from gdbfs import sfs
~~~

### fit()
__arguments__  
1. the entire dataframe for the data.
2. the target columns name.

__return__  
Print the process of selecting with added feature name and evaluated value.  
return a subset of the selected features using the gdbfs.

__for a instance, we can select best features int iris problem as follows:__

1. make dataframe that contains all information (data,target)
~~~
from sklearn.datasets import load_iris
import pandas as pd

data = load_iris()
df = pd.DataFrame(data.data)
df['result']=data.target
~~~

2. call fit with two arguments

~~~
sfs.fit(df,'result')
~~~

3. result

print  

~~~
   feature to add     gdbfs
0               2  2.215350
1               0  2.969618
2               3  2.521875
3               1  2.533693
~~~

return  

~~~
array([[2],
       [0]], dtype=int64)
~~~

seoykim996@gmail.com
