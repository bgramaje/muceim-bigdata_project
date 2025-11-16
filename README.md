### Big Data MITMA

#### DATASET
> A continuación se detalla el dataset MITMA


```js
28079_AM (Área Metropolitana de Madrid) // GAU
    └─ 28079 (Municipio de Madrid) // MUNICIPIO
        ├─ 2807910 (Distrito Centro) // DISTRITO
        ├─ 2807912 (Distrito Salamanca)
        └─ 2807921 (Distrito Chamartín)
    └─ 28013 (Municipio de Getafe)
    └─ 28023 (Municipio de Alcorcón)
```

##### ERROR solucionado

> Error que aparecía por intentar parsear con duckdb el .csv sin cambio alguno, pero no funcionaba por que por defecto el duckDb interpreta `NO` como `FALSE` y `YES` como `TRUE`, pero desconoce lo que es `si`

ConversionException: Conversion Error: CSV Error on Line: 5384386
Original Line: 20230701|19|01010|01002|2-10|casa|frecuente|no|si|01|10-15|NA|NA|3.458|16.573
Error when converting column "estudio_destino_posible". Could not convert string "si" to 'BOOLEAN'
