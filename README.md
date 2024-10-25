# Ejercicio-de-programacion-de-funciones-de-anualidades-vencidas

## Se dara a continuacion un ejemplo del uso de las formulas
## Funciones de anualidades vencidas 
Las siguientes formulas puedes utilizarlas para realizar los calculos de las funciones de las anualidades vencidas 

```{r}
source("https://raw.githubusercontent.com/jaba67/Ejercicio-de-programaci-n-de-funciones-de-anualidades-vencidas-/refs/heads/main/unciones%20de%20anualidades%20vencidas.R")
```

se daran ejemplos a contunuacion del uso de las formulas en problemas practicos para su mejor entendimiento

### Calculo de valor futuro: 

Se tienen el siguiente problema: 
Supón que realizas depósitos anuales de $2,000 en una cuenta que paga una tasa de interés del 5% anual. ¿Cuál será el valor futuro de la cuenta después de 10 años?

$A$=2000
$r$=0.05
$t$=10 meses

Se realizan los calculos:

```{r}
# Creamos objetos con los valores de entrada:
A <- 2000
r <- 0.05
Tper <- 10

# Calculamos el valor futuro
VF <- function(A, r, Tper) {
  return(A * (((1 + r)^Tper - 1) / r))
}

# Imprimimos el resultado:
VF(A, r, Tper)

```

### Cálculo de la Anualidad:

se tiene el siguiente problema: 
Deseas acumular $100,000 en una cuenta de ahorro en 8 años. La cuenta paga una tasa de interés del 4% anual. ¿Cuánto debes depositar al final de cada año para alcanzar esta cantidad?

$VF$=100000
$r$=0.04
$t$=8 meses

```{r}
# Creamos objetos con los valores de entrada:
VF <- 100000
r <- 0.04
Tper <- 8

# Calculamos anualidad
A <- function(VF, r, Tper) {
  result <- (VF * r) / ((1 + r)^Tper - 1)
  return(result)
}

# Imprimimos el resultado:
A(VF, r, Tper)
```

### Fórmula para calcular el Número de pagos o plazo:

se tiene el siguiente problema:
Tienes una anualidad de $5,000 que pagas cada año en una cuenta que ofrece un 3% anual. Si deseas alcanzar un valor futuro de $30,000, ¿cuántos años necesitarás?

$VF$=30000
$A$=5000
$r$=0.03

```{r}
# Creamos objetos con los valores de entrada:
VF <- 30000
A <- 5000
r <- 0.03

# Calculamos numero de pagos:
Tper <- function(VF, A, r) {
  result <- log((VF * r) / A + 1) / log(1 + r)
  return(result)
}

# Imprimimos el resultado:
Tper(VF, A, r)
```

### Fórmula para calcular la Tasa del periodo:

se tiene el siguiente problema: 
Tienes una cuenta de ahorro donde depositas $4,000 al final de cada año durante 7 años, y al final obtienes $35,000. ¿Cuál es la tasa de interés anual que ofrece esta cuenta?

$VF$=35000
$A$=4000
$Tper$=7

```{r}
# Creamos objetos con los valores de entrada:
VF <- 35000
A <- 4000
Tper <- 7

# Calculamos calcular la Tasa del periodo :
r <- function(VF, A, Tper) {
  result <- uniroot(function(r) A * (((1 + r)^Tper - 1) / r) - VF, lower = 0, upper = 1)$root
  return(result)
}


# Imprimimos el resultado:
r(VF, A, Tper)
```

### Fórmula para calcular el Valor Actual:

se tiene el siguiente problema:
Deseas recibir pagos anuales de $3,000 durante 12 años. La tasa de interés del periodo es del 4% anual. ¿Cuál es el valor actual de esta serie de pagos?

$r$=0.04
$A$=3000
$Tper$=12

```{r}
# Creamos objetos con los valores de entrada:
r <- 0.04
A <- 3000
Tper <- 12

# Calculamos valor actual:
VA <- function(A, r, Tper) {
  result <- A * (1 - (1 + r)^(-Tper)) / r
  return(result)
}

# Imprimimos el resultado:
VA(A, r, Tper)
```

### Fórmula para calcular la Anualidad: 

se tiene el siguiente problema:
Deseas un préstamo de $50,000 que planeas pagar en 10 años con una tasa de interés del 6% anual. ¿Cuál será el pago anual?

$VA$=50000
$r$=0.06
$Tper$=10

```{r}
# Creamos objetos con los valores de entrada:
VA <- 50000
r <- 0.06
Tper <- 10

# Calculamos anualidad:
A <- function(VA, r, Tper) {
  result <- VA * (r / (1 - (1 + r)^(-Tper)))
  return(result)
}

# Imprimimos el resultado:
A(VA, r, Tper)
```

### Fórmula para calcular el Número de pagos o plazo:

se tiene el siguiente problema: 
Tomaste un préstamo de $20,000 y estás pagando $2,500 al final de cada año con una tasa del 5% anual. ¿Cuántos años tardarás en pagar el préstamo?

$VA$=20000
$A$=2500
$r$=0.05

```{r}
# Creamos objetos con los valores de entrada:
VA <- 20000
A <- 2500
r <- 0,05

# Calculamos el numero de pagos o plazos:
A <- function(VA, r, Tper) {
  result <- VA * (r / (1 - (1 + r)^(-Tper)))
  return(result)
}

# Imprimimos el resultado:
A(VA, r, Tper)
```

### Fórmula para calcular la Tasa del periodo:

se tiene el siguiente problema: 
Pides un préstamo de $30,000 que pagarás en 15 años con pagos anuales de $3,000. ¿Cuál es la tasa de interés anual?

$VA$=30000
$A$=3000
$Tper$=15

```{r}
# Creamos objetos con los valores de entrada:
VA <- 30000
A <- 3000
Tper <- 15

# Calculamos tasa del periodo:
r <- function(VA, A, Tper) {
  result <- uniroot(function(r) A * (1 - (1 + r)^(-Tper)) / r - VA, lower = 0, upper = 1)$root
  return(result)
}

# Imprimimos el resultado:
r(VA, A, Tper)
```
