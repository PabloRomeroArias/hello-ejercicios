# Ejercicios variables
## Ejercicio 1

Declara una variable de tipo _string_ en la que se almacenará tu nombre. Asígnale el valor correspondiente a dicha variable

<details>
<summary>Posible solución (TypeScrypt)</summary>

```typescript
let nombre : string = "Pablo"
console.log(nombre)
```

</details>

## Ejercicio 2
Declara una variable de tipo entero en la que se almacenará tu edad. Asígnale el valor correspondiente a dicha variable (no vale quitarse años). Muestra por pantalla el valor de la variable. Luego, simula tu cumpleaños y asígnale el valor correspondiente a la variable. Vuelve a mostrar por pantalla el valor de la variable

<details>
<summary>Posible solución (TypeScrypt)</summary>

```typescript
let edad : number = 27
console.log(edad)
edad = 28
console.log(edad)
```

</details>

## Ejercicio 3
Guarda en dos variables el dinero que tienen Mortadelo y Filemón en sus respectivas carteras. Antes de irse cada uno a su casa, se dan cuenta que tienen la cartera el uno del otro, por lo que tienes que intercambiar los valores anteriormente almacenados

<details>
<summary>Posible solución (TypeScrypt)</summary>

```typescript
// Datos de entrada
let dineroMortadelo : number = 150
let dineroFilemon : number = 200

// Algoritmo que resuelve el problema
let aux = dineroMortadelo
dineroMortadelo = dineroFilemon
dineroFilemon = aux

// Datos de salida
let mensaje : string = `Ahora Mortadelo tiene sus ${dineroMortadelo}€ y filemón sus ${dineroFilemon}`
console.log(mensaje)
```

</details>

## Ejercicio 4
Declara una constante e intenta cambiar su valor

<details>
<summary>Posible solución (TypeScrypt)</summary>

```typescript
// Datos de entrada
const NUMERO_PI : number = 3.1415
NUMERO_PI = 3.14 // Da error
```

</details>

## Nota
Es importante que el nombre de las variables y constantes describan el valor del dato que contienen