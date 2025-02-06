# Operadores Relacionales

## Ejercicio 1
Juan y Pedro son amigos de la infancia y quieren saber si tienen la misma edad (vaya amigos...). Compara sus edades y muestra el resultado

<details>
<summary>Posible solución (TypeScrypt)</summary>

```typescript
// Datos de entrada
let edadJuan = 23
let edadPedro = 22

// Algoritmo que resuelve el problema
let tienenMismaEdad = edadJuan == edadPedro

// Datos de salida
let mensaje = `¿Tienen la misma edad? -> ${tienenMismaEdad}`
console.log(mensaje)
```

</details>

## Ejercicio 2
Tu cuñado está comparando los precios de dos teléfonos móviles. Como no tiene ni idea, te pregunta a tí que eres informático (y hacker). Sus opciones son un iPhone 15 y un Samsung Galaxy S24. Verifica si los precios son distintos y aconseja a tu cuñado

<details>
<summary>Posible solución (TypeScrypt)</summary>

```typescript
// Datos de entrada
let precioIphone = 1600
let precioSamsung = 1350

// Algoritmo que resuelve el problema
let tienenPreciosDistintos = precioIphone != precioSamsung

// Datos de salida
let mensaje = `¿Tienen precios distintos? -> ${tienenPreciosDistintos}`
console.log(mensaje)
```

</details>

## Ejercicio 3
Mi prima pequeña siempre ha soñado con montarse en la atracción Jaguar del parque de atracciones de la ciudad. La altura mínima para entrar es 140 cm. ¿Podrá por fin este año cumplir su sueño?

<details>
<summary>Posible solución (TypeScrypt)</summary>

```typescript
// Datos de entrada
let alturaPrima = 140

// Algoritmo que resuelve el problema
let puedeEntrar = alturaPrima >= 140

// Datos de salida
let mensaje = `¿Puede entrar en la atracción? -> ${puedeEntrar}`
console.log(mensaje)
```

</details>

## Ejercicio 4
Mario y Luigi han completado y obtenido diferentes puntuaciones en la carrera del circuito Arcoiris. Yo soy más de Luigi, ¿ha ganado a Mario?

<details>
<summary>Posible solución (TypeScrypt)</summary>

```typescript
// Datos de entrada
let puntuacionMario = 12
let puntuacionLuigi = 10

// Algoritmo que resuelve el problema
let ganaLuigi = puntuacionMario < puntuacionLuigi

// Datos de salida
let mensaje = `¿Ha ganado Luigi? -> ${ganaLuigi}`
console.log(mensaje)
```

</details>

## Ejercicio 5
NYC y LA tienen diferentes temperaturas. Las temperaturas vienen en ºF y ºK. Debido a mi desconocimiento, necesito que compares las temperaturas en ºC y determina si hace más frío en Nueva York que en Los Ángeles

<details>
<summary>Posible solución (TypeScrypt)</summary>

```typescript
// Datos de entrada
let nycFahrenheit = 32
let laKelvin = 273.15

// Algoritmo que resuelve el problema
let nycGrados = (nycFahrenheit - 32) * 5 / 9
let laGrados = laKelvin - 273.15

let haceMasFrioEnNyc = nycGrados < laGrados

// Datos de salida
let mensaje = `¿Hace más frío en NYC? -> ${haceMasFrioEnNyc}`
console.log(mensaje)
```

</details>