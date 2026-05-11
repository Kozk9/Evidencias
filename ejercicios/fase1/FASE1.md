# Fase 1: JavaScript desde Cero (con base de programación)  

## Fundamentos de JavaScript

"JavaScript (o "JS") es un lenguaje de programación que se usa con mayor frecuencia para scripts dinámicos de lado del cliente en páginas web, pero también se usa a menudo en el lado del servidor usando un entorno de ejecución como Node.js" (1) 

___  

"JavaScript es el lenguaje de programación que debes usar para añadir características interactivas a tu sitio web, (por ejemplo, juegos, eventos que ocurren cuando los botones son presionados o los datos son introducidos en los formularios, efectos de estilo dinámicos, animación, y mucho más)  

¿Qué es JavaScript realmente?

JavaScript es un robusto lenguaje de programación que se puede aplicar a un documento HTML y usarse para crear interactividad dinámica en los sitios web. Fue inventado por Brendan Eich, cofundador del proyecto Mozilla, Mozilla Foundation y la Corporación Mozilla.  

JavaScript por sí solo es bastante compacto aunque muy flexible, y los desarrolladores han escrito gran cantidad de herramientas encima del núcleo del lenguaje JavaScript, desbloqueando una gran cantidad de funcionalidad adicional con un mínimo esfuerzo. Esto incluye:  

+ Interfaces de Programación de Aplicaciones del Navegador (APIs) — APIs construidas dentro de los navegadores que ofrecen funcionalidades como crear dinámicamente contenido HTML y establecer estilos CSS, hasta capturar y manipular un vídeo desde la cámara web del usuario, o generar gráficos 3D y muestras de sonido.
+ APIs de terceros, que permiten a los desarrolladores incorporar funcionalidades en sus sitios de otros proveedores de contenidos como Twitter o Facebook.
+ Marcos de trabajo y librerías de terceros que puedes aplicar a tu HTML para que puedas construir y publicar rápidamente sitios y aplicaciones." (2)  

___

- [X] Sintaxis básica: Tipos, operadores, estructuras de control (**if, for, while**).

### Conceptos básicos

#### Sintaxis básica

JavaScript está influenciado sobre todo por la _sintaxis_ de Java, C y C++, pero también ha sido influenciado por Awk, Perl y Python.   

JavaScript distingue entre mayúsculas y minúsculas (es case-sensitive) y utiliza el conjunto de caracteres Unicode. Por ejemplo, la palabra «Früh» (que significa "temprano" en Alemán) se podría usar como el nombre de una variable.   

`let Früh = "foobar";`  

En JavaScript, las instrucciones se denominan declaraciones y están separadas por punto y coma (;).

No es necesario un punto y coma después de una declaración si está escrita en su propia línea. Pero si se deseas más de una declaración en una línea, entonces debes separarlas con punto y coma. 

##### Comentarios   

La sintaxis de los comentarios es la misma que en C++ y en muchos otros lenguajes:   

// un comentario de una línea

/* este es un comentario
 * más largo, de varias líneas
 */

/* Sin embargo, no puedes /* anidar comentarios */ SyntaxError */  

##### Declaraciones  

JavaScript tiene tres tipos de declaraciones de variables.  

var  

Declara una variable, opcionalmente la inicia a un valor.  

let  

Declara una variable local con ámbito de bloque, opcionalmente la inicia a un valor.   

const  

Declara un nombre de constante de solo lectura y ámbito de bloque.  

##### Variables   

Utiliza variables como nombres simbólicos para valores en tu aplicación. Los nombres de las variables, llamados identificadores, se ajustan a ciertas reglas.  

Un identificador de JavaScript debe comenzar con una letra, un guión bajo (_) o un signo de dólar ($). Los siguientes caracteres también pueden ser dígitos (0-9).  

Dado que JavaScript distingue entre mayúsculas y minúsculas, las letras incluyen los caracteres "A" a "Z" (mayúsculas), así como "a" a "z" (minúsculas).  

Puedes utilizar la mayoría de las letras ISO 8859-1 o Unicode como å y ü en los identificadores. (Para obtener más detalles, consulta esta publicación del blog). También puedes usar Secuencias de escape Unicode como caracteres en identificadores.  

Algunos ejemplos de nombres legales son Number_hits, temp99, $credit y _name.  

##### Declaración de variables  

Puedes declarar una variable de dos formas:  

Con la palabra clave var. Por ejemplo, var x = 42. Esta sintaxis se puede utilizar para declarar variables locales y globales, dependiendo del contexto de ejecución.  
Con la palabra clave const o let. Por ejemplo, let y = 13. Esta sintaxis se puede utilizar para declarar una variable local con ámbito de bloque. (Ve el Ámbito de variables abajo.)  
También puedes simplemente asignar un valor a una variable. Por ejemplo, x = 42. Este formulario crea una variable global no declarada. También genera una advertencia estricta de JavaScript. Las variables globales no declaradas a menudo pueden provocar un comportamiento inesperado. Por lo tanto, se desaconseja utilizar variables globales no declaradas.   

##### Evaluar variables  

Una variable declarada usando la instrucción var o let sin un valor asignado especificado tiene el valor de undefined.  

Un intento de acceder a una variable no declarada da como resultado el disparo de una excepción ReferenceError.  

##### Ámbito de variables  

Cuando declaras una variable fuera de cualquier función, se denomina variable global, porque está disponible para cualquier otro código en el documento actual. Cuando declaras una variable dentro de una función, se llama variable local, porque solo está disponible dentro de esa función.  

JavaScript anterior a ECMAScript 2015 no tiene el ámbito de la declaración de bloque. Más bien, una variable declarada dentro de un bloque es local a la función (o ámbito global) en el que reside el bloque.  

##### Conversión de tipos de datos  
JavaScript es un lenguaje tipado dinámicamente. Esto significa que no tienes que especificar el tipo de dato de una variable cuando la declaras. También significa que los tipos de datos se convierten automáticamente según sea necesario durante la ejecución del script. (3)   

___  

#### Tipos y Operadores

Se cuentan nueve tipos de datos en JavaScript, de ellos son 7 los tipos primitivos:   

+ **number**
+ **string**
+ **boolean**
+ null
+ undefined
+ symbol  
+ bigint  

#### Números

En JavaScript, no hay una diferencia entre números enteros y números decimales, todos los números son de tipo **number**

##### Operadores

+ Suma (+)  
+ Resta (-)  
+ Multiplicación (*)
+ División (/)
+ Módulo (%)
+ Exponente (**)

Los operadores mantienen los convenios matemáticos que describen el orden en que se ejecutan las operaciones según su sintáxis o el uso de signos de agrupación como los paréntesis, corchetes o llaves.  

#### Cadenas de Texto  

'Entre comillas simples'  

"Entre comillas dobles \n y con un salto de línea"  

`O entre acentos graves`  

Las comillas simples y dobles funcionan igual, pero al usar acentos graves podemos escribir cadenas de texto que ocupen varias líneas:

`Esto es una cadena de texto
que ocupa varias líneas. Puedes escribir
tantas líneas como quieras`

- Operadores

##### Concatenador (+)

"Se usa cuando se pretende unir" + "dos cadenas de texto en una sola"  

#### Booleanos

Se usan para operaciones de lógica binaria, verdadero o falso.  

#### Estructuras de Control

##### Declaración de bloque  

La declaración más básica es una declaración de bloque, que se utiliza para agrupar instrucciones. El bloque está delimitado por un par de llaves:  

>{  
>  statement_1;  
>  statement_2;  
>  ⋮  
>  statement_n;  
>}  

Las declaraciones de bloque se utilizan comúnmente con declaraciones de control de flujo (if, for, while).  


- [ ] Funciones: declaración, expresiones, ámbitos y closures.
- [ ] Objetos y arrays literales: creación, acceso, mutación.
- [ ] Programación orientada a prototipos vs clases (**ES6**)
- [ ] El entorno Node.js: REPL, ejecuución de scripts, módilos nativos (**fs, path, http**).
- [ ] _Documentar en el repo: snippets que contrasten con otros lenguajes (Python, Java, C#). Notas sobre el modelo de objetos de JS._

(1) https://developer.mozilla.org/es/docs/Glossary/JavaScript  
(2) https://developer.mozilla.org/es/docs/Learn_web_development/Getting_started/Your_first_website/Adding_interactivity  
(3) https://developer.mozilla.org/es/docs/Web/JavaScript/Guide/Grammar_and_types


