# Para estudiar el backend 'totoni'

Se comienza por 'analizar' los llamados 'archivos principales' (_app.js, package.json, package-lock.json_, mencionados en el README.md del repositorio `totoni`). El análisis consistirá en seguir el código, en secuencia, de acuerdo a cómo está construido y se pretende explicar en forma breve las líneas o conceptos que ocurren (para profundizar los temas, se agregan las fuentes al respecto de las citas introducidas en este documento).

El primero de los archivos es _app.js_. 

* Este código da inicio (a la fecha) con una serie de `import`s, lo primero que solicita importar es otro archivo ubicado en la carpeta *config*, el archivo se llama _env.js_. 

`import "./config/env.js";` 

* Entonces sigue estudiar el contenido de _env.js_, el cual da comienzo de igual manera con la importación de cuatro diferentes librerías, da inicio por la librería llamada `dotenv` 

`import dotenv from "dotenv";`

> `dotenv`: "Se usa en Node.js para mejorar la seguridad y la flexibilidad de la aplicación.
Para entender mejor el desempeño de la librería `dotenv`, es preciso conocer qué son las *Variables de Entorno* y su manejo por medio del archivo _.env_."

"*Las variables de entorno son valores dinámicos que se pueden configurar fuera de nuestro código y que afectan al comportamiento de nuestra aplicación*. Estos valores pueden incluir información sensible, como contraseñas de bases de datos o claves de API, que no queremos exponer directamente en nuestro código fuente."

"El archivo _.env_ es una forma de almacenar y gestionar estas variables de entorno. Es un archivo de configuración que se utiliza para definir y almacenar diferentes valores clave-valor que nuestra aplicación utilizará durante su ejecución. Cada línea del archivo _.env_ sigue la sintaxis `NOMBRE_VARIABLE=valor`." 

[Fuente](https://keepcoding.io/blog/sabes-que-es-el-dotenv-en-node-js/)

* Seguido de `dotenv`, el código del archivo _env.js_ importa otra librería de nombre `path`.
 
`import path from "path";`

> `path`: "*El módulo `path` es uno de los módulos incorporados de casa en NodeJS y lo podemos usar para trabajar con rutas dentro del sistema de archivos*."

"Para separar los segmentos de las rutas en Windows se usa la contrabarra o barra invertida, mientras que en Linux y Mac usamos barras inclinadas normales."

"El módulo `path` se encargará automáticamente de trabajar adecuadamente con el sistema de rutas que tengas en el sistema operativo donde se ejecutan los programas, por lo que te aisla de las complejidades de lidiar con las barras o contrabarras de manera condicional. Pero además, este módulo tiene métodos específicos para usar notaciones específicas de un sistema u otro."

[Fuente](https://desarrolloweb.com/articulos/modulo-path-nodejs)

* El siguiente `import` en el archivo _env.js_ es el módulo `url`. 

`import { fileURLToPath } from "url";`

La ayuda de Codium muestra lo siguiente:

"This function ensures the correct decodings of percent-encoded characters as well as ensuring a cross-platform valid absolute path string."

> `url`: "The node:url module provides utilities for URL resolution and parsing."

[Fuente](https://nodejs-org.translate.goog/api/url.html?_x_tr_sl=en&_x_tr_tl=es&_x_tr_hl=es&_x_tr_pto=tc#url)

* Sigue importar el módulo `fs` que deriva de `f`ile `s`ystem.

`import fs from "fs";`

> `fs`: "The node:fs module enables interacting with the file system in a way modeled on standard POSIX functions."

[Fuente](https://nodejs.org/api/fs.html#file-system)

"Existen muchos otros métodos que pueden resultar interesantes, relacionados con el sistema de ficheros y carpetas. Por ejemplo, aquí algunos:"

[Fuente](https://lenguajejs.com/nodejs/fundamentos/fs/#otros-m%C3%A9todos-interesantes)
