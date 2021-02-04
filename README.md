# PuMAC

## Paquete julia para la extracción de archivos csv

### Pre-requisitos 

CSV, DataFrames, JLD, FileIO

### Instalación 

```julia
using Pkg
Pkg.add("PuMac")
```

```julia
using PuMac
```

```julia
unir(archivos::Array, columnas::Array, nombre_archivo::String = "new_PuMAC.csv", faltantes::Bool = true)
#= Se obtiene y se exporta un data frame=#
```
### Licencia 

Este proyecto está bajo la Licencia MIT - mira el archivo [LICENSE.md](LICENSE.md) para detalle
