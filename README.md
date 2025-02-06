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

1. Analizar el problema, saber qué me están pidiendo realmente. Pasar de un enunciado abstracto (cliente) a un problema lo más sintetizado posible
2. Atomizar, dividir el problema en partes. Resolver cada parte del algoritmo de manera independiente y luego juntar todo
3. Tener claros los datos de entrada, es decir, lo que necesita el algoritmo (lo que necesitamos nosotros) para resolver el problema planteado. Al principio puede causar confusión porque nosotros mismos somos los que escribimos los datos de entrada. En un escenario real es cualquier agente externo, una base de datos, un formulario en una Web, etc. Se recomienda que una vez resuelto el ejercicio, habrá que cambiar los datos de entrada y el algoritmo debe de poder resolver el algoritmo con los nuevos *inputs*
4. Plantear los posibles errores que hay que controlar (cuando sepas hacerlo)
5. Resolución del problema. Esta es la parte más importante, aquí vendría la implementación del algoritmo. A esta parte se le llama lógica de negocio
6.  Picamos código. Aquí ya pasaremos del papel y boli al código fuente
7. Control de errores (cuando sepas hacerlo). Tanto en los datos de entrada como en el propio algoritmo. Si por ejemplo nuestro algoritmo recibe dos números y hay que hacer la división, tendríamos que controlar que el divisor no sea 0
8. Datos de salida. Esto se refiere a lo que nos ha pedido el algoritmo. Normalmente, habrá que mostrar un mensaje con el resultado. No hay que olvidar que se supone que nosotros no vamos a usar el algoritmo, nosotros lo diseñamos e implementamos, pero lo probarán los clientes que usen nuestras aplicaciones. No es lo mismo decir `750`, que solo nos acordaremos nosotros (a la semana nosotros tampoco), que `Pablo cobra este mes 750€`. Con este segundo mensaje queda mucho más claro qué se ha solucionado

### Temarios

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
[Gmail](mailto:pablo.romeroarias.main@gmail.com)

[Linkedin](https://www.linkedin.com/in/pablo-romero-arias-425b66197/)

## Contribuciones
Las contribuciones son bienvenidas. Si deseas agregar nuevos ejercicios, mejorar los existentes o corregir errores, por favor abre un _issue_ o envía un _pull request_
