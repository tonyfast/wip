
# Works in progress

Keep track of the [posts](tonyfast.github.io/forever-whatever/) for progress.

## Lines On Deck

## `clsindex`

Pandas indices for different objects, but primarily `pathlib.Path` and `requests.Request`.


```python
from wip.clsindex import *
RequestIndex, ResponseIndex, PathIndex
```




    (wip.clsindex._requests.RequestIndex,
     wip.clsindex._requests.ResponseIndex,
     wip.clsindex._pathlib.PathIndex)



### `PathIndex` example.


```python
df = PathIndex('.').rglob('*.ipynb').to_series().pipe(
    lambda df: df[df.apply(lambda x: '-checkpoint' not in x.name)]).pipe(PathIndex)

"The are {1} notebooks in {0}.".format(PathIndex('.')[0].absolute().name, len(df))
```




    'The are 8 notebooks in wip.'




```python
"That is a total of {} cells.".format(
    df.read_text().apply(
        __import__('nbformat').reads, args=[4]
    ).apply(dict.__getitem__, args=['cells']).apply(len).sum())
```




    'That is a total of 26 cells'




```python
!jupyter nbconvert --to markdown readme.ipynb
```

    [NbConvertApp] Converting notebook readme.ipynb to markdown
    [NbConvertApp] Writing 179 bytes to readme.md

