# Análisis ventas videojuegos
Este análisis se realiza para poder ver las diferentes tendencias en las ventas de videojuegos lanzados hasta el 2020, el set de datos fue extraído desde la siguiente página [Set de datos](https://data.world/sumitrock/video-games-sales)

La web como tal tiene una sugerencia para descargar el set sin tener el archivo localmente, las instrucciones son

```python
import pandas as pd
df = pd.read_csv('https://query.data.world/s/pijetu6nmtism34urgku24yfzd2tce?dws=00000')
```

---

## Análisis exploratorio
Podemos ver que este set de datos se compone de 16.719 filas de datos y las siguientes 16 columnas:
```text
['Name',
 'Platform',
 'Year_of_Release',
 'Genre',
 'Publisher',
 'NA_Sales',
 'EU_Sales',
 'JP_Sales',
 'Other_Sales',
 'Global_Sales',
 'Critic_Score',
 'Critic_Count',
 'User_Score',
 'User_Count',
 'Developer',
 'Rating']
```
De estas columnas, se distribuyen en los siguientes tipos
```text
float64    9
object     7
```

Además de lo anterior tenemos los siguientes porcentajes de nulos en cada columna
```text
Name                0.01
Platform            0.00
Year_of_Release     1.61
Genre               0.01
Publisher           0.32
NA_Sales            0.00
EU_Sales            0.00
JP_Sales            0.00
Other_Sales         0.00
Global_Sales        0.00
Critic_Score       51.33
Critic_Count       51.33
User_Score         40.10
User_Count         54.60
Developer          39.61
Rating             40.49
dtype: float64
```

Según el método `df.describe().T` podemos también resumir lo siguiente
|              | count   | mean      | std       | min     | 25%     | 50%     | 75%     | max      |
|--------------|---------|-----------|-----------|---------|---------|---------|---------|----------|
| Year_of_Release | 16450.0 | 2006.487356 | 5.878995 | 1980.00 | 2003.00 | 2007.00 | 2010.00 | 2020.00 |
| NA_Sales        | 16719.0 | 0.263330    | 0.813514  | 0.00    | 0.00    | 0.08    | 0.24    | 41.36    |
| EU_Sales        | 16719.0 | 0.145025    | 0.503283  | 0.00    | 0.00    | 0.02    | 0.11    | 28.96    |
| JP_Sales        | 16719.0 | 0.077602    | 0.308818  | 0.00    | 0.00    | 0.00    | 0.04    | 10.22    |
| Other_Sales     | 16719.0 | 0.047332    | 0.186710  | 0.00    | 0.00    | 0.01    | 0.03    | 10.57    |
| Global_Sales    | 16719.0 | 0.533543    | 1.547935  | 0.01    | 0.06    | 0.17    | 0.47    | 82.53    |
| Critic_Score    | 8137.0  | 68.967679  | 13.938165 | 13.00   | 60.00   | 71.00   | 79.00   | 98.00    |
| Critic_Count    | 8137.0  | 26.360821  | 18.980495 | 3.00    | 12.00   | 21.00   | 36.00   | 113.00   |
| User_Count      | 7590.0  | 162.229908 | 561.282326| 4.00    | 10.00   | 24.00   | 81.00   | 10665.00 |


