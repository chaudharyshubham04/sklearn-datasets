# wine-sklearn-dataset

 Wine recognition dataset
Data Set Characteristics:

Number of Instances
178 (50 in each of three classes)

Number of Attributes
13 numeric, predictive attributes and the class

Attribute Information
Alcohol

Malic acid

Ash

Alcalinity of ash

Magnesium

Total phenols

Flavanoids

Nonflavanoid phenols

Proanthocyanins

Color intensity

Hue

OD280/OD315 of diluted wines

Proline

class:
class_0

class_1

class_2

Summary Statistics
Alcohol:

11.0

14.8

13.0

0.8

Malic Acid:

0.74

5.80

2.34

1.12

Ash:

1.36

3.23

2.36

0.27

Alcalinity of Ash:

10.6

30.0

19.5

3.3

Magnesium:

70.0

162.0

99.7

14.3

Total Phenols:

0.98

3.88

2.29

0.63

Flavanoids:

0.34

5.08

2.03

1.00

Nonflavanoid Phenols:

0.13

0.66

0.36

0.12

Proanthocyanins:

0.41

3.58

1.59

0.57

Colour Intensity:

1.3

13.0

5.1

2.3

Hue:

0.48

1.71

0.96

0.23

OD280/OD315 of diluted wines:

1.27

4.00

2.61

0.71

Proline:

278

1680

746

315

Missing Attribute Values
None

Class Distribution
class_0 (59), class_1 (71), class_2 (48)

Creator
R.A. Fisher

Donor
Michael Marshall (MARSHALL%PLU@io.arc.nasa.gov)

Date
July, 1988

This is a copy of UCI ML Wine recognition datasets. https://archive.ics.uci.edu/ml/machine-learning-databases/wine/wine.data
               LOAD DIGITS DATASET

sklearn.datasets.load_digits(*, n_class=10, return_X_y=False, as_frame=False)[source]
Load and return the digits dataset (classification).

Each datapoint is a 8x8 image of a digit.

Classes

10

Samples per class

~180

Samples total

1797

Dimensionality

64

Features

integers 0-16

Read more in the User Guide.

Parameters
n_classinteger, between 0 and 10, optional (default=10)
The number of classes to return.

return_X_ybool, default=False.
If True, returns (data, target) instead of a Bunch object. See below for more information about the data and target object.

New in version 0.18.

as_framebool, default=False
If True, the data is a pandas DataFrame including columns with appropriate dtypes (numeric). The target is a pandas DataFrame or Series depending on the number of target columns. If return_X_y is True, then (data, target) will be pandas DataFrames or Series as described below.

New in version 0.23.

Returns
dataBunch
Dictionary-like object, with the following attributes.

data{ndarray, dataframe} of shape (1797, 64)
The flattened data matrix. If as_frame=True, data will be a pandas DataFrame.

target: {ndarray, Series} of shape (1797,)
The classification target. If as_frame=True, target will be a pandas Series.

feature_names: list
The names of the dataset columns.

target_names: list
The names of target classes.

New in version 0.20.

frame: DataFrame of shape (1797, 65)
Only present when as_frame=True. DataFrame with data and target.

New in version 0.23.

images: {ndarray} of shape (1797, 8, 8)
The raw image data.

DESCR: str
The full description of the dataset.

(data, target)tuple if return_X_y is True
New in version 0.18.

This is a copy of the test set of the UCI ML hand-written digits datasets
https://archive.ics.uci.edu/ml/datasets/Optical+Recognition+of+Handwritten+Digits
Examples

To load the data and visualize the images:

>>>
>>> from sklearn.datasets import load_digits
>>> digits = load_digits()
>>> print(digits.data.shape)
(1797, 64)
>>> import matplotlib.pyplot as plt 
>>> plt.gray() 
>>> plt.matshow(digits.images[0]) 
>>> plt.show() 
