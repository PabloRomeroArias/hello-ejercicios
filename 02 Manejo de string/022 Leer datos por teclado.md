# Leer datos por teclado

## NOTAS
Para este apartado, elige de 5 a 10 ejercicios que hayas realizado en los apartados anteriores y pide los datos por teclado

No hay que controlar los errores

<details>
<summary>Lectura datos en C#</summary>

```csharp
// En TypeSscript, leer datos por teclado es algo complejo, así que vamos a poner el ejemplo en C#
Console.Write("Escribe algo por teclado: ")
string texto = Console.ReadLine()
Console.WriteLine($"El texto es: {texto}")
```

<details>
<summary>Solo apto para valientes (Lectura por teclado en TypeScript)</summary>

```typescript
// Primero tenemos que tener el paquete instalado con npm, luego ejecutamos el siguiente comando en consola
// npm install readline-sync
// Y luego
// npm install @types/node --save-dev
// Por último importamos el paquete en el archivo de TypeScript
import * as readline from 'readline';

(async () => {
    let texto = await leerPorTeclado();
    console.log(`El texto introducido es: ${texto}`);
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

</details>