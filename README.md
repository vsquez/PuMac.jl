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
```

```julia
unir(carpeta::String, columnas::Array, nombre_archivo::String = "new_PuMAC.csv", faltantes::Bool = true)
```
### Ejemplo 
Supongamos que tenemos dos archivos csv, si el primero contiene el siguiente DataFrame
```julia
4×2 DataFrame
 Row │ A        B      
     │ Any      String    
─────┼─────────────────
   1 │ 1        M      
   2 │ 2        F      
   3 │ 3        F      
   4 │ 4        M      
```
Y el segundo archivo contiene este otro DataFrame
```julia   
6×2 DataFrame
 Row │ C        D      
     │ Any      String    
─────┼─────────────────
   1 │ 1        Z      
   2 │ 2        Y      
   3 │ 3        X      
   4 │ 5        W      
   5 │ 8        V
   6 │ 13       U
```
```julia
unir(["Archivo_1.csv", "Archivo_2.csv"], ["A", "C"], nombre_archivo = "NuevoCSV.csv", faltantes = true)
```
```julia
6×3 DataFrame
 Row │ A        C   
     │ Any      Any    
─────┼──────────────
   1 │ 1        1
   2 │ 2        2
   3 │ 3        3
   4 │ 4        5
   5 │ missing  8
   6 │ missing  13    
```
### Licencia 

Este proyecto está bajo la Licencia MIT - mira el archivo [LICENSE.md](LICENSE.md) para detalle
