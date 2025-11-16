`GAU`
`Municipios`, con la key de su GAU
`Distrito`, con la key de municipios y su GAU

```sql
-- viajes distristos
-- se castea en vez de VARCHAR de 'si/no' a un booleano de true o false
-- bronze_mitma_od_districts / bronze_mitma_viajes_distritos
CREATE TABLE bronze_mitma_od_districts (
    fecha DATE, -- de TEXT a DATE
    periodo TEXT,
    origen TEXT,
    destino TEXT,
    distancia TEXT,
    actividad_origen TEXT,
    actividad_destino TEXT,
    residencia TEXT,
    renta TEXT,
    edad TEXT,
    sexo TEXT,
    viajes DOUBLE,
    viajes_km DOUBLE,
    estudio_destino_posible BOOLEAN,  -- de VARCHAR a BOOLEAN
    estudio_origen_posible BOOLEAN,   -- de VARCHAR a BOOLEAN
    -- Columnas extras añadidas para auditoria. 
    loaded_at TIMESTAMP DEFAULT CURRENT_TIMESTAMP,
    -- loaded_by TEXT DEFAULT CURRENT_USER,
    source_file TEXT
);

-- Viajes municipios
-- bronze_mitma_od_municipalities / bronze_mitma_viajes_municipios
CREATE TABLE bronze_mitma_od_municipalities (
    fecha DATE,  -- de TEXT a DATE
    periodo TEXT,
    origen TEXT,
    destino TEXT,
    distancia TEXT,
    actividad_origen TEXT,
    actividad_destino TEXT,
    residencia TEXT,
    renta TEXT,
    edad TEXT,
    sexo TEXT,
    viajes DOUBLE,
    viajes_km DOUBLE,
    estudio_destino_posible BOOLEAN, -- de VARCHAR a BOOLEAN
    estudio_origen_posible BOOLEAN,  -- de VARCHAR a BOOLEAN
    -- auditoria
    loaded_at TIMESTAMP DEFAULT CURRENT_TIMESTAMP,
    -- loaded_by TEXT DEFAULT CURRENT_USER,
    source_file TEXT
);

-- Viajes GAU
-- bronze_mitma_od_gau / bronze_mitma_viajes_gau
CREATE TABLE bronze_mitma_od_gau (
    fecha DATE,  -- de TEXT a DATE
    periodo TEXT,
    origen TEXT,
    destino TEXT,
    distancia TEXT,
    actividad_origen TEXT,
    actividad_destino TEXT,
    residencia TEXT,
    renta TEXT,
    edad TEXT,
    sexo TEXT,
    viajes DOUBLE,
    viajes_km DOUBLE,
    estudio_destino_posible BOOLEAN, -- de VARCHAR a BOOLEAN
    estudio_origen_posible BOOLEAN,  -- de VARCHAR a BOOLEAN
    -- auditoria
    loaded_at TIMESTAMP DEFAULT CURRENT_TIMESTAMP,
    -- loaded_by TEXT DEFAULT CURRENT_USER,
    source_file TEXT
);
```