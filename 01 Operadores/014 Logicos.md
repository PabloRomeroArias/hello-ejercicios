# Operadores Lógicos

## Ejercicio 1
Pedro quiere saber si puede ver una película en el cine. Para ello, necesita que la película esté en cartelera y que tenga suficiente dinero para la entrada

<details>
<summary>Enunciado simplificado</summary>
<p>Guarda en una variable el dinero que tiene Pedro</p>
<p>Guarda en una variable el dinero que cuesta la entrada de cine</p>
<p>Guarda en otra variable si la película está en cartelera o no (boolean)</p>
<p>Guarda en otra variable si tiene dinero suficiente</p>
<p>Guarda en otra variable el resultado de la comparación lógica con el operador <b>AND</b></p>
<details>
<summary>Posible solución (TypeScrypt)</summary>

```typescript
// Datos de entrada
// Hay que variar los datos de entrada para que el programa haga lo que tiene que hacer...
// Pero también para que NO HAGA LO QUE NO TIENE QUE HACER
let dineroPedro = 4.5
let costeEntrada = 5
let estaEnCartelera = true

// Algoritmo que resuelve el problema
let tieneDineroSuficiente = dineroPedro >= costeEntrada
let vaAlCine = tieneDineroSuficiente && estaEnCartelera

// Datos de salida
let mensaje = `Tiene dinero suficiente: ${tieneDineroSuficiente}.\nLa película está en cartelera: ${estaEnCartelera}.\nPor lo tanto, Pedro va al cine: ${vaAlCine}`
console.log(mensaje)
```

</details>
</details>

## Ejercicio 2
Harry Potter quiere saber si puede ir al Bosque Prohibido. Para ello, necesita que la capa de invisibilidad no la tenga Ron y que Hagrid esté despierto para que le explique los nuevos peligros que acechan Hogwarts

<details>
<summary>Enunciado simplificado</summary>
<p>Guarda en una variable si Ron tiene la capa</p>
<p>Guarda en otra variable si Hagrid está despierto</p>
<p>Guarda en otra variable el resultado de la comparación lógica con el operador <b>AND</b></p>
<details>
<summary>Posible solución (TypeScrypt)</summary>

```typescript
// Datos de entrada (hay que variar los datos de entrada para que el programa haga lo que tiene que hacer,
// pero también para que NO HAGA LO QUE NO TIENE QUE HACER)
let tieneLaCapaRon = true
let estaDespiertoHagrid = false

// Algoritmo que resuelve el problema
let puedeIrAlBosqueHarry = !tieneLaCapaRon && estaDespiertoHagrid // CUIDADO hay que negar que Ron tenga la capa, ya que para que el algoritmo se correcto, necesitamos que NO la tenga

// Datos de salida
let mensaje = `Ron tiene la capa: ${tieneLaCapaRon}.\nHagrid está depierto: ${estaDespiertoHagrid}.\nPor lo tanto, Harry puede ir al Bosque Prohibido: ${puedeIrAlBosqueHarry}`
console.log(mensaje)
```

</details>
</details>

## Ejercicio 3
María está decidiendo si comprar un nuevo teléfono. Ella comprará el teléfono si no es más antiguo que del año 2022 o si tiene un descuento mínimo del 20%

<details>
<summary>Enunciado simplificado</summary>
<p>Guarda en una variable el año del móvil</p>
<p>Guarda en otra variable el descuento del móvil</p>
<p>Guarda en otra variable si el móvil es antiguo</p>
<p>Guarda en otra variable si el móvil tiene descuento suficiente</p>
<p>Guarda en otra variable el resultado de la comparación lógica con el operador <b>OR</b></p>
<details>
<summary>Posible solución (TypeScrypt)</summary>

```typescript
// Datos de entrada (hay que variar los datos de entrada para que el programa haga lo que tiene que hacer,
// pero también para que NO HAGA LO QUE NO TIENE QUE HACER)
let anioMovil = 2020
let descuentoMovil = 30

// Algoritmo que resuelve el problema
let esAntiguo = anioMovil < 2022
let tieneSuficienteDescuento = descuentoMovil >= 20
let compraElMovil = !esAntiguo || tieneSuficienteDescuento // Recuerda que el móvil se comprará si NO es antiguo

// Datos de salida
let mensaje = `Es antiguo el móvil: ${esAntiguo}.\nTiene descuento suficiente: ${tieneSuficienteDescuento}.\nPor lo tanto, María compra el móvil: ${compraElMovil}`
console.log(mensaje)
```

</details>
</details>

## Ejercicio 4
Elsa está organizando una fiesta en Arendelle y quiere saber si puede usar el jardín del castillo. Para ello, necesita que haga buen tiempo (xD) con una temperatura entre -5 y 10 ºC (xDD) y que Olaf haya colocado los adornos. ¿Se puede celebrar la fiesta?

<details>
<summary>Enunciado simplificado</summary>
<p>Guarda en una variable la temperatura que hace</p>
<p>Guarda en otra variable si hace una buena Temperatura para Elsa (Temperatura >= -5 && Temperatura <= 10)</p>
<p>Guarda en otra variable si Olaf ha colocado los adornos</p>
<p>Guarda en otra variable el resultado de la comparación lógica con el operador <b>AND</b></p>
<details>
<summary>Posible solución (TypeScrypt)</summary>

```typescript
// Datos de entrada
// Hay que variar los datos de entrada para que el programa haga lo que tiene que hacer...
// Pero también para que NO HAGA LO QUE NO TIENE QUE HACER
let temperatura = 11.5
let haColocadoAdornosOlaf = false

// Algoritmo que resuelve el problema
let haceTemperaturaAgradable = temperatura >= -5 && temperatura <= 10
let puedeUsarJardin = haceTemperaturaAgradable && haColocadoAdornosOlaf

// Datos de salida
let mensaje = `Hace Temperatura agradable: ${haceTemperaturaAgradable}.\nOlaf ha colocado los adornos: ${haColocadoAdornosOlaf}.\nPor lo tanto, Se celebra la fiesta: ${puedeUsarJardin}`
console.log(mensaje)
```

</details>
</details>

## Ejercicio 5
Marta está decidiendo si ir de vacaciones. Se irá si tiene 1000€ ahorrados, o si encuentra una oferta con un descuento mayor al 30%

<details>
<summary>Enunciado simplificado</summary>
<p>Guarda en una variable el dinero que tiene Marta ahorrado</p>
<p>Guarda en otra variable la cantidad del descuento de la oferta</p>
<p>Guarda en otra variable si tiene dinero suficiente</p>
<p>Guarda en otra variable si es suficiente el descuento</p>
<p>Guarda en otra variable el resultado de la comparación lógica pertinente</p>
<details>
<summary>Posible solución (TypeScrypt)</summary>

```typescript
// Datos de entrada
// Hay que variar los datos de entrada para que el programa haga lo que tiene que hacer...
// Pero también para que NO HAGA LO QUE NO TIENE QUE HACER
let dineroAhorrado = 700
let hayDescuento = false
let cantidadDescuento = 30

// Algoritmo que resuelve el problema
let tieneDineroSuficiente = dineroAhorrado >= 1000
let esDescuentoSuficiente = cantidadDescuento > 30
let hayDescuentoYEsSuficiente = hayDescuento && esDescuentoSuficiente
let vaDeVacaciones = tieneDineroSuficiente || hayDescuentoYEsSuficiente

// Datos de salida
let mensaje = `Tiene dinero suficiente: ${tieneDineroSuficiente}.\nHay descuento: ${hayDescuento}.\nEs descuento suficiente: ${esDescuentoSuficiente}\nPor lo tanto, Marta se va de vacaciones: ${vaDeVacaciones}`
console.log(mensaje)
```

</details>
</details>

## Ejercicio 6
Mi sobrino nació el 29 de febrero de 2024. Quiero saber si en el año 2036 podrá celebrar su cumpleaños

<details>
<summary>Enunciado simplificado</summary>
<p>Calcular si un año es bisiesto. Un año es bisiesto si es divisible entre 4 y <b>NO</b> lo es entre 100 o si el año es divisible entre 400</p>
<p>Guarda en una variable el año</p>
<p>Guarda en otra variable si es divisible entre 4</p>
<p>Guarda en otra variable si <b>NO</b> es divisible entre 100</p>
<p>Guarda en otra variable si es divisible entre 400</p>
<p>Guarda en otra variable el resultado de la comparación lógica pertinente</p>
<details>
<summary>Posible solución (TypeScrypt)</summary>

```typescript
// Datos de entrada
// Hay que variar los datos de entrada para que el programa haga lo que tiene que hacer...
// Pero también para que NO HAGA LO QUE NO TIENE QUE HACER
let anio = 700
// Años bisiestos: 2000, 2024
// Años no bisiestos: 1800, 2019, 2200

// Algoritmo que resuelve el problema
let esDivisibleEntre4 = anio % 4 == 0
let noEsDivisibleEntre100 = anio % 100 != 0
let esDivisibleEntre400 = anio % 400 == 0
let anioBisiesto = (esDivisibleEntre4 && noEsDivisibleEntre100) || esDivisibleEntre400

// Datos de salida
let mensaje = `El año ${anio} es bisiesto: ${anioBisiesto}`
console.log(mensaje)
```

</details>
</details>