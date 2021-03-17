# Implementation of Geometric Distance Based Feature Selection
This package is intended for use with 'geometric distance based feature selection'.
For more information on this feature selection, please refer to 'https://github.com/seo-young-kim/GeometricDistanceBasedFeatureSelection'

## How to Use
Currently, only functions implemented in the sequential forward selection method exist.
Therefore, import sfs of the package and use it with fit() function.

### fit()
This function takes two arguments.
The first is the entire dataframe for the data.
The second is the target columns name.
You can the return a subset of the selected features using the gdbfs.

seoykim996@gmail.com
