Para el silver.

Las tablas de GAU, municipios y distritos, tienen la misma info replicada practicamente. Entonces, todo lo que lleva _AM es GAU, y lo que son distritos tienen dos digitos mas de codigos que los municipios. Quiero diferenciar esto para tener una tabla de solo lo que son municipos, solo lo que son GAU, y solo lo que son distritos. Los distritos tendran la key del municipio. Y el municio la key de los GAU, ya que


```js
28079_AM (Área Metropolitana de Madrid) // GAU
    └─ 28079 (Municipio de Madrid) // MUNICIPIO
        ├─ 2807910 (Distrito Centro) // DISTRITO
        ├─ 2807912 (Distrito Salamanca)
        └─ 2807921 (Distrito Chamartín)
    └─ 28013 (Municipio de Getafe)
    └─ 28023 (Municipio de Alcorcón)
```