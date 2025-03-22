# Operadores de Asignación

Recuerda que estamos practicando operadores de asignación, por lo que intenta hacer uso de ellos en esta relación de ejercicios

## Ejercicio 1
Carlos ha ahorrado una cantidad de dinero y lo ingresa en su cuenta corriente. ¿Cuánto dinero tiene Carlos ahora?

<details>
<summary>Posible solución (TypeScrypt)</summary>

```typescript
// Datos de entrada
let ahorros = 281
let cuentaCorriente = 720

// Algoritmo que resuelve el problema
cuentaCorriente += ahorros

// Datos de salida
let mensaje = `Al ahorrar ${ahorros}€, ahora dispone de ${cuentaCorriente}`
console.log(mensaje)
```

</details>

## Ejercicio 2
Pedro ha pagado la factura de la luz, actualiza el saldo de su cuenta

<details>
<summary>Posible solución (TypeScrypt)</summary>

```typescript
// Datos de entrada
let factura = 281
let saldo = 720

// Algoritmo que resuelve el problema
saldo -= factura

// Datos de salida
let mensaje = `Al pagar ${factura}€ de luz, ahora dispone de ${saldo}`
console.log(mensaje)
```

</details>

## Ejercicio 3
Ana ha invertido en acciones y su inversión ha subido un 50%. ¿Cuánto valen ahora sus acciones?

<details>
<summary>Posible solución (TypeScrypt)</summary>

```typescript
// Datos de entrada
let valorAcciones = 1000
let indiceSubida = 1.5

// Algoritmo que resuelve el problema
valorAcciones *= indiceSubida

// Datos de salida
let mensaje = `Al subir un 50% el valor de las acciones, El valor de las mismas son ${valorAcciones}`
console.log(mensaje)
```

</details>

## Ejercicio 4
Luis quiere repartir las horas que tiene de su tiempo de estudio entre sus materias. ¿Cuánto tiempo le dedica a cada materia?

<details>
<summary>Posible solución (TypeScrypt)</summary>

```typescript
// Datos de entrada
let tiempoEstudio = 10
let materias = 5

// Algoritmo que resuelve el problema
tiempoEstudio /= materias

// Datos de salida
let mensaje = `Al tener ${materias} materias, Va a dedicarle ${tiempoEstudio}h a cada una`
console.log(mensaje)
```

</details>

## Ejercicio 5
Marta está organizando una fiesta y quiere saber cuántos invitados se quedarán sin mesa

<details>
<summary>Posible solución (TypeScrypt)</summary>

```typescript
// Datos de entrada
let personasRestantes = 50
let personasPorMesa = 6

// Algoritmo que resuelve el problema
personasRestantes %= personasPorMesa

// Datos de salida
let mensaje = `Hay ${personasRestantes} personas que se quedan sin mesa`
console.log(mensaje)
```

</details>

## Ejercicio 6
Juan ha completado una tarea y quiere incrementar su contador de tareas completadas

<details>
<summary>Posible solución (TypeScrypt)</summary>

```typescript
// Datos de entrada
let tareasCompletadas = 7

// Algoritmo que resuelve el problema
++tareasCompletadas

// Datos de salida
let mensaje = `Juan ha completado ${tareasCompletadas} tareas en total`
console.log(mensaje)
```

</details>

## Ejercicio 7
Elena ha perdido un punto en su juego favorito. Actualiza su puntuación

<details>
<summary>Posible solución (TypeScrypt)</summary>

```typescript
// Datos de entrada
let puntosElena = 23

// Algoritmo que resuelve el problema
--puntosElena

// Datos de salida
let mensaje = `Tras perder un punto, Elena tiene ${puntosElena} puntos`
console.log(mensaje)
```

</details>