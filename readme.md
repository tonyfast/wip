
# [<small>works in progress</small>](https://tonyfast.github.io/wip)

<code>pip install git+<a href="https://github.com/tonyfast/wip">https://github.com/tonyfast/wip </a></code>


```python
from wip import *
```

# Build


```python
!jupyter nbconvert --execute index.ipynb
```

    [NbConvertApp] Converting notebook index.ipynb to html
    [NbConvertApp] Executing notebook with kernel: python3
    [NbConvertApp] ERROR | Error while converting 'index.ipynb'
    Traceback (most recent call last):
      File "/Users/tonyfast/anaconda/lib/python3.5/site-packages/nbconvert/nbconvertapp.py", line 381, in export_single_notebook
        output, resources = self.exporter.from_filename(notebook_filename, resources=resources)
      File "/Users/tonyfast/anaconda/lib/python3.5/site-packages/nbconvert/exporters/exporter.py", line 172, in from_filename
        return self.from_file(f, resources=resources, **kw)
      File "/Users/tonyfast/anaconda/lib/python3.5/site-packages/nbconvert/exporters/exporter.py", line 190, in from_file
        return self.from_notebook_node(nbformat.read(file_stream, as_version=4), resources=resources, **kw)
      File "/Users/tonyfast/anaconda/lib/python3.5/site-packages/nbconvert/exporters/html.py", line 84, in from_notebook_node
        return super(HTMLExporter, self).from_notebook_node(nb, resources, **kw)
      File "/Users/tonyfast/anaconda/lib/python3.5/site-packages/nbconvert/exporters/templateexporter.py", line 268, in from_notebook_node
        nb_copy, resources = super(TemplateExporter, self).from_notebook_node(nb, resources, **kw)
      File "/Users/tonyfast/anaconda/lib/python3.5/site-packages/nbconvert/exporters/exporter.py", line 132, in from_notebook_node
        nb_copy, resources = self._preprocess(nb_copy, resources)
      File "/Users/tonyfast/anaconda/lib/python3.5/site-packages/nbconvert/exporters/exporter.py", line 309, in _preprocess
        nbc, resc = preprocessor(nbc, resc)
      File "/Users/tonyfast/anaconda/lib/python3.5/site-packages/nbconvert/preprocessors/base.py", line 47, in __call__
        return self.preprocess(nb,resources)
      File "/Users/tonyfast/anaconda/lib/python3.5/site-packages/nbconvert/preprocessors/execute.py", line 242, in preprocess
        nb, resources = super(ExecutePreprocessor, self).preprocess(nb, resources)
      File "/Users/tonyfast/anaconda/lib/python3.5/site-packages/nbconvert/preprocessors/base.py", line 70, in preprocess
        nb.cells[index], resources = self.preprocess_cell(cell, resources, index)
      File "/Users/tonyfast/anaconda/lib/python3.5/site-packages/nbconvert/preprocessors/execute.py", line 275, in preprocess_cell
        raise CellExecutionError(msg)
    nbconvert.preprocessors.execute.CellExecutionError: An error occurred while executing the following cell:
    ------------------
    from IPython.display import *; from pathlib import Path
    for pkg in __import__('setuptools').find_packages():
        for path in Path(pkg).rglob('*.ipynb'): 
            display(Markdown("[{}]({})".format(path, pat`h.with_suffix('.html'))))
    ------------------
    
    SyntaxError: invalid syntax (<ipython-input-1-0f9bed543840>, line 4)
    

