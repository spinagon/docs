---
editable: false
---

# GEOINFO

_Geographical functions_

#### Syntax {#syntax}


```
GEOINFO( address, scale )
```

#### Description {#description}
Converts `address` to geographical name corresponding to the specified `scale`.

Possible values for `scale` parameter:
- `"country"`,
- `"country_code"`,
- `"region"`,
- `"locality"`.

**Argument types:**
- `address` — `String`
- `scale` — `String`


**Return type**: `String`

{% note info %}

Only constant values are accepted for arguments (scale).

{% endnote %}

{% note warning %}

Function is available only with the Standard billing plan.

{% endnote %}


#### Examples {#examples}

```
GEOINFO("посёлок Свободный Серп", "country") = "Россия"
```


#### Data source support {#data-source-support}

`Materialized Dataset`.
