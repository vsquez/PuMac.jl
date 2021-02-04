# PuMAC

## Paquete julia para la extracción de archivos csv

### Pre-requisitos 

Tener los paquetes 
`CSV`
`DataFrames`
`JLD`
`FileIO`

### Instalación 

```julia
using Pkg
Pkg.add(url = "https://github.com/JacoboL/PuMac.jl")
```

```julia
using PuMac
```

```julia
unir(archivos::Array, columnas::Array, nombre_archivo::String = "new_PuMAC.csv", faltantes = true)
```
6×3 DataFrame
 Row │ A        B        C   
     │ Any      Any      Any    

─────┼───────────────────────

   1 │ 1        M        1 
   2 │ 1        F        2  
   3 │ 1        F        3
   4 │ 1        M        4   
   5 │ missing  missing  5    
   6 │ missing  missing  6    
   
```julia
unir(archivos::Array, columnas::Array, nombre_archivo::String = "new_PuMAC.csv", faltantes = false)
```

```julia
unir(carpeta::String, columnas::Array, nombre_archivo::String = "new_PuMAC.csv", faltantes::Bool = true)
```
### Licencia 

Este proyecto está bajo la Licencia MIT - mira el archivo [LICENSE.md](LICENSE.md) para detalle
