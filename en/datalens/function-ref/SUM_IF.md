---
editable: false
---

# SUM_IF

_Aggregate functions_

#### Syntax {#syntax}


```
SUM_IF( expression, condition )
```

#### Description {#description}
Returns the sum of all the expression values that meet the `condition` condition. Applicable to numeric data types only.

**Argument types:**
- `expression` — `Number`
- `condition` — `Boolean`


**Return type**: Same type as (`expression`)

#### Examples {#examples}

```
SUM_IF([Profit], [Profit] > 15)
```


#### Data source support {#data-source-support}

`Materialized Dataset`, `ClickHouse 1.1`, `Microsoft SQL Server 2017 (14.0)`, `MySQL 5.6`, `PostgreSQL 9.3`.

### As Window Function {#as-window-function}

Function `SUM_IF` is also available as a window function.
#### Syntax {#window-syntax}


```
SUM_IF( expression, condition [ TOTAL | WITHIN [ dim1, ... ] | AMONG [ dim1, ... ] ] )
```

#### Examples {#window-examples}

```
SUM_IF([Profit], [Category] = 'Office Supplies' TOTAL)
```

```
SUM_IF([Profit], [Category] = 'Office Supplies' WITHIN [Date])
```

```
SUM_IF([Profit], [Category] = 'Office Supplies' AMONG [Date])
```
