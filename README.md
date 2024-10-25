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

$VF$=50,000
$r$=6%=0.06 (convertido a decimal) anual
$t$=60

Se realizan los calculos:

```{r}
# Creamos objetos con los valores de entrada:
VF=50000
r=0.06
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

$VF$=20,000.00
$A$=244.89
$t$=60 meses

Se realizan los calculos:

```{r}
# Creamos objetos con los valores de entrada:
VF=20000
A=244.89
t=60
# Calculamos la tasa del periodo
tasa=r(VF,A,t)
# Imprimimmos el resultado: 
tasa
```

###Calculo del valor actual, conociendo la anualidad, tasa de interés del periodo y el número (plazo) de anualidades


se tienen los siguientes datos:

$A$=244.89
$r$=1% mensual
$t$=60 meses

Se realizan los calculos:

```{r}
# Creamos objetos con los valores de entrada:
A=244.89
r=0.01
t=60
# Calculamos la tasa del periodo
ValorActual=VA(A,r,t)
# Imprimimmos el resultado: 
ValorActual
```

###Calculo de la anualidad, conociendo valor actual, tasa del periodo y número de pagos

se tienen los siguientes datos:

$VA$=10,000.00
$r$=1% mensual
$t$=60 meses

Se realizan los calculos:

```{r}
# Creamos objetos con los valores de entrada:
VA=10000
r=0.01
t=60
# Calculamos la anualidad
anualidad=A(VA,r,t)
# Imprimimmos el resultado: 
anualidad
```

###Calculo de el número de pagos o plazo, conociendo valor actual, anualidad y tasa del periodo

se tienen los siguientes datos:

$VA$=5,000.00
$A$=100.00
$r$=1.00% mensual

Se realizan los calculos:

```{r}
# Creamos objetos con los valores de entrada:
VA=5000
A=100
r=0.01
# Calculamos el número de pagos
numeroDePagos=t(VA,A,r)
# Imprimimmos el resultado: 
numeroDePagos
```

###Calculo la tasa del periodo, conociendo valor actual, número de pagos y monto de la anualidad.

se tienen los siguientes datos:

$VA$=4,000.00
$A$=100.00
$t$=36 meses

Se realizan los calculos:

```{r}
# Creamos objetos con los valores de entrada:
VA=4000
A=100
t=36
# Calculamos el número de pagos
tasa=r(VA,A,t)
# Imprimimmos el resultado: 
tasa
```

