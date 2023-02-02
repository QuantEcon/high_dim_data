---
jupytext:
  text_representation:
    extension: .md
    format_name: myst
    format_version: 0.13
    jupytext_version: 1.14.1
kernelspec:
  display_name: Python 3 (ipykernel)
  language: python
  name: python3
---



Regarding converting between ``.ipynb`` and ``.md`` please refer to https://manual.quantecon.org/writing/converting.html

```{code-cell} ipython3
import pandas as pd
```

```{code-cell} ipython3
var_list = ['yearmerge',    # 3-year window
            'ffanw',        # net wealth (ffafin + ffanfin - tdebt)
            'tinc',         # total household income, excluding capital gains
            'incws',        # income from wages, salaries and self-employment
            'wgtI95W95',    # survey weight 
            'ffanwgroups',  # wealth groups
            'tincgroups']   # income groups
```

Rename the variables needed.

```{code-cell} ipython3
var_names_new = 'year', 'n_wealth', 't_income', 'l_income', 'weights', 'nw_groups', 'ti_groups'
```

```{code-cell} ipython3
df = pd.read_stata('https://github.com/QuantEcon/high_dim_data/blob/main/SCF_plus/SCF_plus.dta?raw=true')
```

```{code-cell} ipython3
df = df[[*var_list]]
df1=df.astype({'yearmerge': int}).dropna()
df1.columns = var_names_new
```

```{code-cell} ipython3
df1
```

```{code-cell} ipython3
df1.to_csv('SCF_plus_mini.csv', index=None)
```

```{code-cell} ipython3

```
