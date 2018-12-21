# SuPy

[![Build Status](https://dev.azure.com/sunt05/SUEWS/_apis/build/status/sunt05.SuPy?branchName=master)](https://dev.azure.com/sunt05/SUEWS/_build/latest?definitionId=11?branchName=master)

[![Documentation Status](https://readthedocs.org/projects/supy/badge/?version=latest)](https://supy.readthedocs.io/en/latest/?badge=latest)

[**SU**EWS](https://suews-docs.readthedocs.io) that speaks **Py**thon

## Installation

```shell
python3 -m pip install supy --upgrade
```

## Quickstart

```python
import supy as sp

# load sample data
df_state_init, df_forcing = sp.load_SampleData()

# run supy/SUEWS simulation
df_output, df_state_end = sp.run_supy(df_forcing, df_state_init)

# plot results
res_plot = df_output.SUEWS.loc[1, ['QN', 'QF', 'QS', 'QE', 'QH']]
res_plot.loc['2012 6 4':'2012 6 6'].resample('30T').mean().plot()
```
![sample plot](./sample_plot.png)

## Tutorial
Please check out [more SuPy tutorials here!](https://supy.readthedocs.io/en/latest/tutorial/tutorial.html)
