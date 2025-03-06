# Operadores Aritméticos

## Ejercicio 1
Juan tiene manzanas y compra más en el mercado(na). Calcula cuántas manzanas tiene en total

<details>
<summary>Posible solución (TypeScrypt)</summary>

```typescript
// Datos de entrada
let manzanaActuales = 2
let manzanasCompradas = 3

// Algoritmo que resuelve el problema
let manzanasTotalesJuan = manzanasActuales + manzanasCompradas

// Datos de salida
let mensaje = `Tenía ${manzanasActuales} manzanas y compra: ${manzanasCompradas}.\nAhora tiene en total: ${manzanasTotalesJuan} manzanas`
console.log(mensaje)
```

</details>

## Ejercicio 2
María tenía unas onzas de chocolate y se comió  unas cuantas. Calcula cuántas le quedan

<details>
<summary>Posible solución (TypeScrypt)</summary>

```typescript
// Datos de entrada
let onzasTotales = 10
let onzasComidas = 3

// Algoritmo que resuelve el problema
let onzasSobrantes = onzasTotales - onzasComidas

// Datos de salida
let mensaje = `Tenía ${onzasTotales} onzas y se come ${onzasComidas}.\nAhora le sobran: ${onzasSobrantes} onzas`
console.log(mensaje)
```

</details>

## Ejercicio 3
Pedro va a comprar caramelos y quiere saber cuántos caramelos tendrá en total si compra los mismos durante unos días más

<details>
<summary>Enunciado simplificado</summary>

Multiplica los caramelos de Pedro por los días que va a comprar y obtendrás los caramelos totales

<details>
<summary>Posible solución (TypeScrypt)</summary>

```typescript
// Datos de entrada
let caramelosComprados = 4
let diasDeCompra = 3

// Algoritmo que resuelve el problema
let caramelosTotales = caramelosComprados * diasDeCompra

// Datos de salida
let mensaje = `Compra ${caramelosComprados} caramelos durante ${diasDeCompra} días.\nTiene en total: ${caramelosTotales} caramelos`
console.log(mensaje)
```

</details>

</details>

## Ejercicio 4
Ana tiene galletas y quiere repartirlas entre sus amigos. Calcula cuántas galletas le tocarán a cada amigo. Si tu lenguaje lo permite, intenta que no se puedan dividir en trozos las galletas

<details>
<summary>Posible solución (TypeScrypt)</summary>

```typescript
// Datos de entrada
let galletas = 20
let amigos = 3

// Algoritmo que resuelve el problema
let galletasPorAmigo = Math.floor(galletas / amigos) // Redondea por abajo la división

// Datos de salida
let mensaje = `${galletas} entre ${amigos} amigos.\nA cada amigo le corresponde: ${galletasPorAmigo} galletas`
console.log(mensaje)
```

</details>

## Ejercicio 5
¿Se pudo comer Ana alguna galleta?

<details>
<summary>Enuncuado simplificado</summary>

Calcula si sobró alguna galleta mediante el resto de la división

<details>
<summary>Posible solución (TypeScrypt)</summary>


```typescript
// Datos de entrada
let galletas = 20
let amigos = 3

// Algoritmo que resuelve el problema
let galletasRestantes = galletas % amigos // El resto de la división da las galletas que han sobrado

// Datos de salida
let mensaje = `Ana se puede comer ${galletasRestantes} ya que sobraron`
console.log(mensaje)
```

</details>
</details>

## Ejercicio 6
Quiero demostrarle a mi prima pequeña que no es lo mismo `(a + b) * c` que `a + (b * c)`. No me hace caso, así que como es una friki como yo, si se lo programome hará caso y podrá ver la magia. Abra... Cadabra... **¡ALAKAZAM!**

<details>
<summary>Posible solución (TypeScrypt)</summary>

```typescript
// Datos de entrada
let a = 4
let b = 3
let c = 7

// Algoritmo que resuelve el problema
let resultado1 = (a + b) * c
let resultado2 = a + (b * c)

// Datos de salida
let mensaje = `${resultado1} no es lo mismo que  ${resultado2}`
console.log(mensaje)
```

</details>

## Ejercicio 7
Popósito de año nuevo: hacer ejercicio. Y antes de empezar mi nutricionista me ha pedido que diseñe un algoritmo que me diga mi IMC (índice de masa corporal). Si es posible, redondea a 2 decimales

<details>
<summary>Posible solución (TypeScrypt)</summary>

Fórmula IMC = Peso / (Altura * Altura)

Peso en kilogramos. Altura en metros

```typescript
// Datos de entrada
let peso = 80
let altura = 1.80

// Algoritmo que resuelve el problema
let alturaCuadrado = altura * altura
let imc = (peso / alturaCuadrado).toFixed(2) // El método toFixed(2) te redondea a 2 decimales

// Datos de salida
let mensaje = `Mi IMC es ${imc}%`
console.log(mensaje)
```

</details>

## Ejercicio 8
El cronómetro del reloj que costó 0.99 € solo cuenta los segundos y ahora no puedo jugar con mi primo al juego de cronometrar cuánto tiempo puede estar callado (para que haya silencio en casa). Calcula las horas, minutos y segundos que mi primo está callado a partir de los segundos que marca el reloj

<details>
<summary>Posible solución (TypeScrypt)</summary>

Redondea (hacia abajo) el resultado de la división

```typescript
// Datos de entrada
let segundosTotales = 10921

// Algoritmo que resuelve el problema
let horas = Math.floor(segundosTotales / 3600)
let minRestantes = segundosTotales % 3600
let min = Math.floor(minRestantes / 60)
let segundos = minRestantes % 60

// Datos de salida
let mensaje = `${segundosTotales} segundos son: ${horas}h ${min}min y ${segundos}seg`
console.log(mensaje)
```

</details>
