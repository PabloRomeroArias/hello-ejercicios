# Bucles

**NOTA**: no se permite hacer uso de ningún método a menos que tu lenguaje no permita realizar alguno de los algoritmos sin uso de ellos

## Ejercicio 1

Calcula la multiplicación de dos números mediante sumas sucesivas

<details>
<summary>Posible solución (TypeScrypt)</summary>

```typescript
let factor1 = 5
let factor2 = 3
let multiplicacion = 0

// Recuerda, 5 * 3 = 5 + 5 + 5 = 15
for (let i = 0; i < factor2; i++) {
	multiplicacion += factor1 // Vamos acumulando el resultado
}

let mensaje = `${factor1} * ${factor2} = ${multiplicacion}`
console.log(mensaje)
```

</details>

## Ejercicio 2

Calcula el exponente de dos números mediante multiplicaciones sucesivas

<details>
<summary>Posible solución (TypeScrypt)</summary>

```typescript
let base = 2
let exponente = 3
let potencia = 1

// Recuerda, 2 ^ 3 = 2 * 2 * 2 = 8
for (let i = 0; i < exponente; i++) {
	potencia *= base // Vamos acumulando el resultado
}

let mensaje = `${base} ^ ${exponente} = ${potencia}`
console.log(mensaje)
```

</details>

## Ejercicio 3

Calcula el cociente y el resto de dos números mediante restas sucesivas

<details>
<summary>Posible solución (TypeScrypt)</summary>

```typescript
let dividendo = 7
let divisor = 2
let cociente = 0
let sobrante = dividendo

// Recuerda, 7 / 2 => cociente: 3 resto: 1
// Bucle que se encarga de la división
while (sobrante > divisor) { // Mientras el sobrante sea más grande que el divisor, se puede seguir dividiendo
	cociente++ // Aumentamos cociente
	sobrante -= divisor // Actualizamos el número que nos sobra (y también la condición del bucle)
}
// Una vez el cociente está calculado, el resto es el sobrante (un número entre 0 y divisor - 1)
let resto = sobrante

let mensaje = `${dividendo} / ${divisor} => cociente: ${cociente} resto: ${resto}`
console.log(mensaje)
```

</details>

## Ejercicio 4

Crea un algoritmo que pida por teclado un entero y no pare hasta que introduzca un entero o un mensaje predefinido por ti. Muestra el número introducido o un mensaje de despedida en caso de no haber introducido nada. No te olvides de decir al usuario el texto que tiene que escribir para dejar de introducir números. Puedes usar un método que pase un *string* a *int*

<details>
<summary>Posible solución (TypeScrypt)</summary>

```typescript
import * as readline from 'readline';

(async () => {
    let input = ""
	// Primer intento fuera del bucle, sin avisar del mensaje para salir
	let numero = Number(await leerPorTeclado("Introduce un número: "))

	// Bucle que se encarga de leer un número o un texto para salir (s) en este algoritmo
    while (Number.isNaN(numero)) {
		// Recogemos lo introducido por teclado
        input = await leerPorTeclado()

		// Si es s, salimos
        if (input == "s")
            break
        
		// Intentamos pasar a número
        numero = Number(input)
    }

	// Si el input es "s", quiere decir que no ha introducido número
    if (input == "s")
        console.log("Hasta pronto!")
    else // Sino, quiere decir que el usuario ha introducido un número
        console.log(`El número introducido es: ${numero}`)
})()

// Función que lee un número por teclado con un mensaje para mostrar al usuario de manera predefinida para indicarle qué tiene que introducir
function leerPorTeclado(mensaje: string = "Introduce un número (s para salir): "): Promise<string> {
    return new Promise((resolve) => {
        const rl = readline.createInterface({
            input: process.stdin,
            output: process.stdout
        });

        rl.question(mensaje, (input) => {
            rl.close();
            resolve(input);
        });
    });
}
```

</details>

## Ejercicio 5

Implementa un algoritmo que simule la puntuación de un gimnasta olímpico. Hay 10 jueces y puntuarán con un número entero del 1 al 10, luego se eliminan la mayor y menor puntuación. Por último, la puntuación del gimnasta será la media de los jueces restantes

<details>
<summary>Posible solución (TypeScrypt)</summary>

```typescript
import * as readline from 'readline';

(async () => {
    let calificaciones: number[] = [] // Array donde almacenaremos las calificaciones de los 10 jueces
    let index = 0 // Índice en el que irá cada calificación
    
	let calificacion: number
	let input = ""

    // Mientras que no tengamos 10 elementos en el array, seguimos leyendo calificación (10 elementos == 9 índice, ya que empezamos en el 0)
    while (index < 10) {
		// NaN == Not a Number
		calificacion = NaN // cada vez que vayamos a leer calificacion, reseteamos el valor a NaN para que entre en el siguiente bucle

		// COMIENZO mismo algoritmo lectura números por teclado
        while (Number.isNaN(calificacion)) {
            input = await leerPorTeclado()

            if (input == "s")
                break
            
            calificacion = Number(input)
        }
		// FIN mismo algoritmo lectura números por teclado

		// Permitimos al usuario salir si no quiere introducir más números (no hacemos la media)
        if (input == "s")
            break

		// Si el número NO es un NaN (Not a Number), quiere decir que es un número
		if (!Number.isNaN(calificacion)) {
            calificaciones[index] = calificacion // Añadimos la calificación en el índice libre
            index++ // Nuevo índice para la nueva calificación
        }
    }

    // Si índice es menor que 9, no se han introducido 10 calificaciones, salimos porque el usuario así lo ha querido
    if (index < 9) {
        console.log("Hasta pronto!") // Mensaje de despedida
        return // Ya no ejecutamos más código
    }

    let calificacionesFinales = eliminarMayorYMenor(calificaciones) // Algoritmo que elimina el mayor y el menor de los elementos
    let media = calcularMedia(calificacionesFinales) // Algoritmo que calcula la media aritmética de las 8 calificaciones

    console.log(`La puntuación del gimnasta olímpico según los 8 jueces es: ${media}`)
})()

function eliminarMayorYMenor(calificaciones: number[]): number[] {
    let mayor = calificaciones[0] // Suponemos que el mayor de los números es el primero
    let indexMayor = 0 // Suponemos que el índice del mayor es el primero

    let menor = calificaciones[0] // Suponemos que el menor de los números es el primero
    let indexMenor = 0 // Suponemos que el índice del menor es el primero

	// Recorremos el array con un forEach, necesitaremos tanto el valor como el índice
    calificaciones.forEach((calificacion, i) => {
        if (calificacion > mayor) { // Si la calificación es estrictamente mayor, cambia el valor del mayor y su índice
            mayor = calificacion // Actualizamos valor del mayor
            indexMayor = i // Actualizamos índice del mayor
        }

		// ÍDEM con el menor
        if (calificacion < menor) { // Si la calificación es estrictamente menor, cambia el valor del menor y su índice
            menor = calificacion  // Actualizamos valor del menor
            indexMenor = i // Actualizamos valor del menor
        }
    })

    let calificacionesFiltradas: number[] = [] // Array que almacenará las 8 calificaciones (quitando la mayor y la menor)
	let indiceFiltrada = 0

	// Recorremos de nuevo el array ahora que ya sabemos cuál es el mayor y menor de los índices
    calificaciones.forEach((calificacion, i) => {
		// Si index es distinto que el mayor y el menor (calculados anteriormente), la calificación debe de añadirse
        if (i != indexMayor && i != indexMenor) {
            calificacionesFiltradas[indiceFiltrada] = calificacion // Añadimos calificación
			indiceFiltrada++ // // Actualizamos nueva posición filtrada
        }
    })

    return calificacionesFiltradas // Devolvemos el array con las 8 calificaciones
}

// Media aritmética => suma_elementos / numero_elementos
function calcularMedia(calificaciones: number[]): number {
    let sumaCalificaciones = 0 // calcularemos la suma de los elementos
	// calcularemos el número de elementos (aunque sea 8, hay que intentar hacer la función lo más reusable posible)
	// si ponemos 8 HARDCODEADO, solo podremos hacerlo con un array de 8 elementos
    let numeroCalificaciones = 0 

	// Recorremos para ir calculando la suma y el numero de elementos
    calificaciones.forEach(calificacion => {
        suma += calificacion
        contador++
    })

    let media = suma / contador // Calculamos la media aritmética
    return media // Devolvemos la media aritmética
}

function leerPorTeclado(mensaje: string = "Introduce un número (s para salir): "): Promise<string> {
    return new Promise((resolve) => {
        const rl = readline.createInterface({
            input: process.stdin,
            output: process.stdout
        });

        rl.question(mensaje, (input) => {
            rl.close();
            resolve(input);
        });
    });
}
```

</details>

## Ejercicio 6

Crea un programa que pida una cadena por teclado y la imprima sin vocales, sin consonantes y con las vocales en mayúsculas. Los caracteres especiales no se tendrán en cuenta. Puedes hacer uso de un método que convierta en mayúsculas

<details>
<summary>Posible solución (TypeScrypt)</summary>

```typescript
import * as readline from 'readline';

(async () => {
    let texto = await leerPorTeclado();

    let sinVocales = textoSinVocales(texto)
    let conVocales = textoConVocales(texto)
    let vocalesMayusculas = textoConVocalesMayusculas(texto)

    console.log(`Texto sin vocales: ${sinVocales}`)
    console.log(`Texto con vocales: ${conVocales}`)
    console.log(`Texto con vocales en mayúsculas: ${vocalesMayusculas}`)
})()

function textoSinVocales(texto: string): string {
    let sinVocales = ""

	// Recorremos el string gracias a este bucle
    for (let letra of texto) {
        if (esVocal(letra)) // Si es bocal, pasamos a la siguiente letra
            continue

        sinVocales += letra // Añadimos
    }

    return sinVocales
}

function textoConVocales(texto: string): string {
    let conVocales = ""

    for (let letra of texto) {
        if (!esVocal(letra)) // Si NO es bocal, pasamos a la siguiente letra
            continue

        conVocales += letra
    }

    return conVocales
}

function textoConVocalesMayusculas(texto: string): string {
    let conVocales = ""

    for (let letra of texto) {
        if (esVocal(letra)) // Si es bocal, añadimos en mayúsculas
            conVocales += letra.toUpperCase()
        else
            conVocales += letra // Si es consonante, añadimos tal cual
    }

    return conVocales
}

// Algoritmo que calcula si "una letra" es vocal: si es a, e, i, o ó u devuelve true
function esVocal(letra: string): boolean {
    return letra == "a" || letra == "e" || letra == "i" || letra == "o" || letra == "u"
}

function leerPorTeclado(mensaje: string = "Introduce un texto: "): Promise<string> {
    return new Promise((resolve) => {
        const rl = readline.createInterface({
            input: process.stdin,
            output: process.stdout
        });

        rl.question(mensaje, (input) => {
            rl.close();
            resolve(input);
        });
    });
}
```

</details>

## Ejercicio 7

Pide una frase por teclado y escribe por pantalla, con un mensaje elaborado, las veces que se repite cada caracter. El espacio no se cuenta como caracter y tienes que mostrar también el número de palabras que hay

<details>
<summary>Posible solución (TypeScrypt)</summary>

```typescript
import * as readline from 'readline';

(async () => {
    let texto = await leerPorTeclado()
	// Hashmap para almacenar la letra (clave) y las veces que aparece (valor)
    let conteoLetras : Map<string, number> = new Map<string, number>()

	// Bucle para para añadir al hashmap cada letra o aumentar sus apariciones
    for (let caracter of texto) {
		// Si es espacio, pasamos al siguiente caracter
        if (caracter == ' ') {
            continue;
        }

		// Si el hashmap tiene el caracter (tiene la clave), vamos a añadir uno a sus apariciones
        if (conteoLetras.has(caracter)) {
            let nuevaAparicion : number = 0 //

			// Recorremos hashmap con el foreach, recuerda, primer valor, luego clave
            conteoLetras.forEach((apariciones, letra) => {
                if (letra == caracter) { // Cuando encontremos en el hashmap la letra (clave):
                    nuevaAparicion = apariciones + 1; // Habrá aparecido 1 vez más a las que ya había aparecido previamente
                }
            });
			// Una vez calculada la nueva aparición, guardamos en el el elemento con clave caracter y su valor con la nueva aparición añadida
            conteoLetras.set(caracter, nuevaAparicion);
        } else {
			// Si no tiene la clave, será su primera aparición
            conteoLetras.set(caracter, 1);
        }
    }

	// Mensaje con las apariciones de cada letra de manera amigable
    let mensaje = ""

    conteoLetras.forEach((apariciones, letra) => {
        mensaje += `La letra '${letra}' aparece ${apariciones} veces\n`;
    });
    console.log(mensaje);
})()

function leerPorTeclado(mensaje: string = "Introduce un texto: "): Promise<string> {
    return new Promise((resolve) => {
        const rl = readline.createInterface({
            input: process.stdin,
            output: process.stdout
        });

        rl.question(mensaje, (input) => {
            rl.close();
            resolve(input);
        });
    });
}
```

</details>

## Ejercicio 8

Pide un número natural *N* por teclado y muestra la sucesión de Fibonacci hasta el elemento *N*

Resultado si introducimos 10: `10 primeros elementos de Fibonacci: 1, 1, 2, 3, 5, 8, 13, 21, 34, 55.`

## Ejercicio 9

Crea un algorito que calcule todos los divisores de un número entero positivo introducido por teclado. Imprime de manera amigable al usuario los divisores

## Ejercicio 10

Implementa un programa que calcule los primeros *N* números primos

## Ejercicio 11

Crea un algoritmo que genere una lista de 20 números aleatorios del 1 al 100 que no contenga duplicados

## Ejercicio 12

Haz un algoritmo que genere un número aleatorio entre 1 y 20, el usuario tendrá 5 intentos para adivinarlo

## Ejercicio 13

Dada una matriz, crea una nueva que sea su traspuesta

## Ejercicio 14

Implementa el intento de inicio de sesión de un usuario mediante una interfaz de consola. El usuario deberá introducir el usuario y la contraseña en el mismo mensaje y tiene 3 intentos para que introduzca las credenciales. Si no inicia sesión, el algoritmo terminará, si no, tendrás que mostrar un mensaje que de la bienvenida al usuario

## Ejercicio 15

Crea un algoritmo que pida una lista de enteros por teclado y devuelva otra lista con ordenada de manera ascendente

## Ejercicio 16

Crea un programa que haga lo siguiente:

- Pida un, y solo un, caracter por teclado
- Pida una frase de al menos dos palabras
- Separa en dos listas distintas dependiendo de si cada palabra de la frase contiene o no el caracter pedido al inicio

## Ejercicio 17

Pide por teclado números del 0 al 10 hasta que el usuario introduzca fin. Almacena los números introducidos y luego muestra una interfaz al usuario que le permita:

- Cantidad de aprobados
- Cantidad de suspensos
- Suma de todos los elementos
- Número de elementos introducios
- Nota media de la clase

## Ejercicio 18

Implementa un programa que diga si una palabra es palíndorma. Una palabra palíndroma se lee de izquierda a derecha y viceversa. Ej: rallar, eje, reconocer, rajar, salas, etc.

## Ejercicio 19

Crea un algoritmo que imprima un árbol de navidad. El usuario introducirá en un mismo mensaje un solo caracter con el que se representará, y el número de filas que tendrá el árbol de Navidad:

- La base tendrá siempre 3 filas y 3 caracteres por fila
- Podrá tener tantas filas como se quieran

Para orientarte, el árbol ha de ser algo similar a [este ejemplo](https://programacion1z.wordpress.com/wp-content/uploads/2023/01/captura-de-pantalla_20230111_163809.png "Ejemplo"), teniendo en cuenta los cambios que se requieren en este ejercicio

## Ejercicio 20

Implementa el famoso juego del ahorcado (no hace falta imprimir la horca por pantalla). Recuerda avisar al jugador de cómo va el estado de la partida: las vidas restantes, las letras acertadas y las restantes, etc.

## Ejercicio 21

Crea un programa para gestionar una agenda de contactos. En este ejercicio puedes hacer uso de cualquier método. El programa hará lo siguiente:
1. Se podrá introducir por teclado:
	- Número de teléfono. Si existe, muestra el nombre de contacto. Si no, pide el nombre para dar de alta el número con su nombre de contacto
	- Nombre contacto: Si existe, muestra el número de teléfono. Si no, pide el número de teléfono para dar de alta el contacto con su número de teléfono
	- Se permitirá al usuario volver atrás introduciendo algún caracter o input "especial"

2. Debe reconocer números de teléfono con espacios entre dígitos o no y con el prefijo de tu país (+34 en España)
3. Los nombres deben comenzar por letras y pueden contener números y caracteres especiales imprimibles
4. Comandos especiales:
- *salir*: sale del programa
- *listado*: muestra el listado completo de los contactos ordenados por nombre
- *filtra texto*: muestra el listado de los contactos o números que contengan *texto* o *Ningún contacto contiene texto* si no hubiera ninguno

## Ejercicio 22

Crea una función que reciba una lista y devuelva si se encuentra ordenada de manera ascendente

## Enhorabuena

Acabas de desbloquear todo el potencial de tu lenguaje. A partir de ahora, ya puedes hacer uso de cualquier método o herramienta que te facilite tu lenguaje de programación. También se debe de empezar a tener más responsabilidad y ser más exigente con tu nivel de programación