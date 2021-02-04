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

### Implementación 
```julia
unir(archivos::Array, columnas::Array, nombre_archivo::String = "new_PuMAC.csv", faltantes = true)

4×2 DataFrame
 Row │ A        B      
     │ Any      Any    
─────┼─────────────────
   1 │ 1        M      
   2 │ 2        F      
   3 │ 3        F      
   4 │ 4        M      
   5 │ missing  missing
   6 │ missing  missing
   
   6×1 DataFrame
 Row │ C   
     │ Any    
─────┼─────
   1 │ 1
   2 │ 2
   3 │ 3
   4 │ 5
   5 │ 8
   6 │ 13   

6×3 DataFrame
 Row │ A        B        C   
     │ Any      Any      Any    
─────┼───────────────────────
   1 │ 1        M        1
   2 │ 2        F        2
   3 │ 3        F        3
   4 │ 4        M        5
   5 │ missing  missing  8
   6 │ missing  missing  13    
```
```julia
unir(archivos::Array, columnas::Array, nombre_archivo::String = "new_PuMAC.csv", faltantes = false)
```

```julia
unir(carpeta::String, columnas::Array, nombre_archivo::String = "new_PuMAC.csv", faltantes::Bool = true)
```
### Licencia 

Este proyecto está bajo la Licencia MIT - mira el archivo [LICENSE.md](LICENSE.md) para detalle
