import numpy as np
import matplotlib.pyplot as plt
import seaborn as sns
sns.set(color_codes=True)
import pandas as pd
%matplotlib inline

dataset=pd.read_csv('Titanic Testing Data.csv')
dataset.head()

dataset=dataset.drop('Id',axis=1)
dataset.head()

print(dataset.shape)

print(dataset.head(5))

print(dataset.info())

print(dataset.describe())

print(dataset.groupby('Name').size())

print(dataset.plot(kind='box', sharex=False, sharey=False))

print(dataset.hist(edgecolor='black', linewidth=1.2))

dataset.boxplot(by="Name",figsize=(10,10))

violinplots onpetal-length for each species
sns.violinplot(data=dataset,x="Name", y="PetalLength")

sns.violinplot(data=dataset,x="Name",y="PassengerId")

from pandas.plotting import scatter_matrix
scatter_plot matrix
scatter_matrix(dataset,figsize=(10,10))
plt.show()

sns.pairplot(dataset, hue="Name")

