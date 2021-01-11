```python
import re
import pandas as pd
```


```python
df = pd.DataFrame({'Animal': ['Falcon', 'Falcon',
                              'Parrot', 'Parrot'],
                   'Max Speed': [380., 370., 24., 26.],
                  'Min Speed': [10., 20., 25., 40.],
                  'hi':['ab1','bb2','cb3','db4'],
                  'hai':['p','r','o','f']})
```


```python
df
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>Animal</th>
      <th>Max Speed</th>
      <th>Min Speed</th>
      <th>hi</th>
      <th>hai</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>Falcon</td>
      <td>380.0</td>
      <td>10.0</td>
      <td>ab1</td>
      <td>p</td>
    </tr>
    <tr>
      <th>1</th>
      <td>Falcon</td>
      <td>370.0</td>
      <td>20.0</td>
      <td>bb2</td>
      <td>r</td>
    </tr>
    <tr>
      <th>2</th>
      <td>Parrot</td>
      <td>24.0</td>
      <td>25.0</td>
      <td>cb3</td>
      <td>o</td>
    </tr>
    <tr>
      <th>3</th>
      <td>Parrot</td>
      <td>26.0</td>
      <td>40.0</td>
      <td>db4</td>
      <td>f</td>
    </tr>
  </tbody>
</table>
</div>




```python
df.loc[:,['Animal']]
```


```python
deef.loc[:,'Animal'].tolist()
```


```python
deef = df.groupby(['Animal'])[['Max Speed']].sum()
deef = deef.reset_index()
```


```python
df.groupby(['Animal']).max()
```


```python
df.loc[0,'hi'].replace('a','p')
```


```python
def replaceYear(row):
    return 'ii'
```


```python
df['hi'] = df['hi'].apply(replaceYear)
```


```python
s = df.loc[0,:]
s
```




    Animal       Falcon
    Max Speed       380
    Min Speed        10
    hi              ab1
    hai               p
    Name: 0, dtype: object




```python
s.iloc[3]
```




    'ab1'




```python
pattern = '\d+$'
re.findall(pattern, s['hi'])[0] + s['hai']
```




    '1p'




```python
s.loc['hi']
```




    'ab1'




```python
df = pd.DataFrame({'Animal': ['Fon', 'Fcon',
                              'Pat', 'Parrot'],
                  'date': ['2020','2020','2010','2000']})
df
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>Animal</th>
      <th>date</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>Fon</td>
      <td>2020</td>
    </tr>
    <tr>
      <th>1</th>
      <td>Fcon</td>
      <td>2020</td>
    </tr>
    <tr>
      <th>2</th>
      <td>Pat</td>
      <td>2010</td>
    </tr>
    <tr>
      <th>3</th>
      <td>Parrot</td>
      <td>2000</td>
    </tr>
  </tbody>
</table>
</div>




```python
df.groupby('date').count()
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>Animal</th>
    </tr>
    <tr>
      <th>date</th>
      <th></th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>2000</th>
      <td>1</td>
    </tr>
    <tr>
      <th>2010</th>
      <td>1</td>
    </tr>
    <tr>
      <th>2020</th>
      <td>2</td>
    </tr>
  </tbody>
</table>
</div>




```python

```
