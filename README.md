# Hello Ejercicios

Bienvenido a **Hello Ejercicios**, una colección de ejercicios de programación clasificados por temarios y ordenados desde el nivel más básico hasta el nivel avanzado

Este repositorio está diseñado para ayudarte a mejorar tus habilidades de programación a través de la práctica continua. Intentando plantear ejercicios que se acerquen más a la realidad para proponer problemas a los que te puedas enfrentar en tu día a día. De esta manera aprenderás a transformar un problema real en una solución

La idea es que resuelvas los ejercicios usando el conocimiento adquirido de los ejercicios anteriores hasta que llegues a bucles. Una vez que resuelvas los ejercicios de bucles, podrás hacer uso de todas las herramientas que te provea el lenguaje que uses, aunque no hayas hecho ejercicios usando dichas herramientas

Si algún ejercicio no está bien definido, tendrás que tomar una decisión como programador. Comenta en el código qué decisión has tomado para tu yo del futuro y sigue resolviendo en base a las decisiones tomadas. Se ha intentado definir bien los ejercicios pero sin llegar a poner paso a paso lo que tienes que hacer, esa tarea te corresponde a ti

## Estructura del Repositorio

El repositorio está organizado en carpetas, cada una representando un temario distinto. Tanto las carpetas como los ejercicios dentro de cada carpeta están ordenados de manera progresiva, comenzando con conceptos básicos y avanzando hacia temas más complejos

## Pasos para resolver un ejercicio

A continuación, se recojen los pasos que tienes que seguir a la hora de resolver un problema. Algunos pasos, sobre todo al principio te los podrás saltar

Lo más importante es que no te pongas directamente a picar código, sino que pienses la mejor manera de resolver un algoritmo con papel y boli

1. Analizar el problema, saber qué me están pidiendo realmente. Pasar de un enunciado abstracto (cliente) a un problema lo más sintetizado y ordenado posible
2. Atomizar, dividir el programa en subprogramas. Resolver cada subprograma de manera independiente e ir juntando las piezas
3. Tener claros los datos de entrada de cada subprograma, es decir, lo que necesita el subprograma para resolver aquello para lo que ha sido diseñado. Al principio puede causar confusión porque nosotros mismos somos los que escribimos los datos de entrada. En un escenario real es cualquier agente externo, una base de datos, un formulario en una Web, etc. Una vez escrito el programa completo, cambia los datos de entrada y el programa debe de poder ejecutarse y resolver el algoritmo con los nuevos *inputs*
4. Haz un diagrama de flujo por cada subprograma para tener claro todos los posibles caminos de cada algoritmo y no dejar ningún cabo suelto
5. Datos de salida. Para cada subprograma, piensa la manera en que el subprograma debe devolver los datos: un número, un string, un mensaje elaborado para mostrar por pantalla, etc.
6. Plantea los posibles errores que tengas que controlar (cuando sepas hacerlo)
7. Picamos código. Aquí ya pasaremos del papel y boli al código fuente
8.  Controla los errores (cuando sepas hacerlo). Tanto en los datos de entrada como en el propio algoritmo. Si por ejemplo nuestro algoritmo pide dos números a un usuario para hacer la división, habría que controlar:
    1.  Introduce números y no letras
    2.  La división no es una división por 0 

## Temario

<table>
  <tr>
    <th>Temario</th>
    <th>Contenido</th>
  </tr>
  <tr>
    <td rowspan="6"><a href="./00%20Elementos%20de%20un%20programa">00 Elementos de un programa</a></td>
    <td><a href="./00%20Elementos%20de%20un%20programa/001%20Hola%20mundo.md">001 Hola mundo</a></td>
  </tr>
  <tr>
    <td><a href="./00%20Elementos%20de%20un%20programa/002%20Variables%20y%20constantes.md">002 Variables y constantes</a></td>
  </tr>
  <tr>
    <td><a href="./00%20Elementos%20de%20un%20programa/003%20Tipos%20mas%20comunes.md">003 Tipos mas comunes</a></td>
  </tr>
  <tr>
    <td><a href="./00%20Elementos%20de%20un%20programa/004%20Sintaxis.md">004 Sintaxis</a></td>
  </tr>
  <tr>
    <td><a href="./00%20Elementos%20de%20un%20programa/005%20Formateo%20de%20strings.md">005 Formateo de <i>strings</i></a></td>
  </tr>
  <tr>
    <td><a href="./00%20Elementos%20de%20un%20programa/006%20Palabras%20reservadas.md">006 Palabras reservadas</a></td>
  </tr>

  <tr>
    <td rowspan="4"><a href="./01%20Operadores">01 Operadores</a></td>
    <td><a href="./01%20Operadores/011%20Aritmeticos.md">011 Aritmeticos</a></td>
  </tr>
  <tr>
    <td><a href="./01%20Operadores/012%20Asignacion.md">012 Asignacion</a></td>
  </tr>
  <tr>
    <td><a href="./01%20Operadores/013%20Relacionales.md">013 Relacionales</a></td>
  </tr>
  <tr>
    <td><a href="./01%20Operadores/014%20Logicos.md">014 Logicos</a></td>
  </tr>

  <tr>
    <td rowspan="2"><a href="./02%20Manejo%20de%20string">02 Manejo de string</a></td>
    <td><a href="./02%20Manejo%20de%20string/021%20Metodos%20de%20string.md">021 Metodos de <i>strings</i></a></td>
  </tr>
  <tr>
    <td><a href="./02%20Manejo%20de%20string/022%20Leer%20datos%20por%20teclado.md">022 Leer datos por teclado</a></td>
  </tr>

  <tr>
    <td rowspan="3"><a href="./03%20Funciones">03 Funciones</a></td>
    <td><a href="./03%20Funciones/031%20Funciones.md">031 Funciones</a></td>
  </tr>
  <tr>
    <td><a href="./03%20Funciones/032%20Recursividad.md">032 Recursividad</a></td>
  </tr>
  <tr>
    <td><a href="./03%20Funciones/033%20Punteros.md">033 Punteros</a></td>
  </tr>

  <tr>
    <td rowspan="3"><a href="./04%20Estructuras%20selectivas">04 Estructuras selectivas</a></td>
    <td><a href="./04%20Estructuras%20selectivas/041%20If.md">041 If</a></td>
  </tr>
  <tr>
    <td><a href="./04%20Estructuras%20selectivas/042%20If-else.md">042 If-else</a></td>
  </tr>
  <tr>
    <td><a href="./04%20Estructuras%20selectivas/043%20Switch.md">043 Switch</a></td>
  </tr>

  <tr>
    <td rowspan="5"><a href="./05%20Estructuras%20de%20datos">05 Estructuras de datos</a></td>
    <td><a href="./05%20Estructuras%20de%20datos/051%20Enum.md">051 Enum</a></td>
  </tr>
  <tr>
    <td><a href="./05%20Estructuras%20de%20datos/052%20Array.md">052 Array</a></td>
  </tr>
  <tr>
    <td><a href="./05%20Estructuras%20de%20datos/053%20Pilas%20y%20colas.md">053 Pilas y colas</a></td>
  </tr>
  <tr>
    <td><a href="./05%20Estructuras%20de%20datos/054%20Matrices.md">054 Matrices</a></td>
  </tr>
  <tr>
    <td><a href="./05%20Estructuras%20de%20datos/055%20Hash%20map.md">055 Hash map</a></td>
  </tr>

  <tr>
    <td rowspan="3"><a href="./06%20Bucles">06 Bucles</a></td>
    <td><a href="./06%20Bucles/061%20While%20y%20DoWhile.md">061 While y DoWhile</a></td>
  </tr>
  <tr>
    <td><a href="./06%20Bucles/062%20For.md">062 For</a></td>
  </tr>
  <tr>
    <td><a href="./06%20Bucles/063%20Foreach.md">063 Foreach</a></td>
  </tr>
</table>

## Contacto
[Discord](https://discord.com/invite/g8zmywTFm8)

[Linkedin](https://www.linkedin.com/in/pablo-romero-arias-425b66197/)

[Gmail](mailto:pablo.romeroarias.main@gmail.com)

[YouTube](https://www.youtube.com/@DevePoler)

[GitHub](https://www.github.com/PabloRomeroArias)

## Contribuciones
Las contribuciones son bienvenidas. Si deseas agregar nuevos ejercicios, mejorar los existentes o corregir errores, por favor abre un _issue_, envía un _pull request_ o ponte en contacto conmigo
