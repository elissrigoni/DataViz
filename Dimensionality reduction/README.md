# countries.csv

`df = pd.read_csv('https://raw.githubusercontent.com/elissrigoni/DataViz/main/Text_12Jun20/countries.csv', decimal = ',')`
`df = df.dropna()`


**IF THE TARGET VARIABLE IS FLOAT YOU HAVE TO CONVERT IT IN INT:**

`df = df.astype({'Climate':'int'})`

**drop more than one column**
`x = df[df.columns.difference((['Climate', 'Country', 'Region']))]`

# define target variable
y = df.Climate.values

`unique, counts = np.unique(y, return_counts=True)`

`classes = len(counts)`

`from sklearn.preprocessing import StandardScaler`

`sc = StandardScaler()`

`x = sc.fit_transform(x)`
