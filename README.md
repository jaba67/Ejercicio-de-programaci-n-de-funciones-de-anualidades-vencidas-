# Ejercicio-de-programacion-de-funciones-de-anualidades-vencidas

## Se dara a continuacion un ejemplo del uso de las formulas
## Funciones de anualidades vencidas 
Las siguientes formulas puedes utilizarlas para realizar los calculos de las funciones de las anualidades vencidas 

```{r}
source("https://raw.githubusercontent.com/jaba67/Ejercicio-de-programaci-n-de-funciones-de-anualidades-vencidas-/refs/heads/main/funciones%20de%20anualidades%20vencidas.R")
```

se daran ejemplos a contunuacion del uso de las formulas en problemas practicos para su mejor entendimiento

### Calculo de valor futuro 

Se tienen los siguientes datos:

$A$=700.00
$r$=1.00% mensual
$t$=36 meses

Se realizan los calculos:

```{r}
# Creamos objetos con los valores de entrada:
A=700
r=0.10
t=36
# Calculamos el valor futuro
ValorFuturo=VF(A,r,t)
# Imprimimmos el resultado: 
ValorFuturo
```

### Calculo de la anualidad , conociendo valor futuro, tasa del periodo y número de pagos

se tienen los siguientes datos:

$VF$=46,000.00
$r$=2.00% mensual
$t$=30 meses

Se realizan los calculos:

```{r}
# Creamos objetos con los valores de entrada:
VF=46000
r=0.02
t=60
# Calculamos la anualidad
Anualidad=A(VF,r,t)
# Imprimimmos el resultado: 
Anualidad
```

###Calculo de el Número de pagos o plazo, conociendo valor futuro, anualidad y tasa del periodo

se tienen los siguientes datos:

$VF$=10,000.00
$A$=201.40
$r$=1.00% mensual

Se realizan los calculos:

```{r}
# Creamos objetos con los valores de entrada:
VF=10000
A=201.40
r=0.01
# Calculamos el numero de pagos
NumeroDePagos=t(VF,A,r)
# Imprimimmos el resultado: 
NumeroDePagos
```

###Calculo de  la tasa del periodo, conociendo valor futuro, número de pagos y monto de la anualidad

se tienen los siguientes datos:

