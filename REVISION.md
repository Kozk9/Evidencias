## REVISION.md para revisión de programa de mentoria

### 02/07/2026

#### Puntos positivos

- Se sigue el orden cronológico inverso (más reciente primero), que es el estándar.
- Uso correcto de los encabezados Agregado, Correcciones y Eliminado.

#### Puntos negativos

- Error de formato grave: Varias entradas usan {1.1.1] (llave de apertura en vez de corchete). Debe ser siempre [1.1.1]. Es un detalle mínimo pero rompe el estándar.
  
- Mal uso del Versionado Semántico: Tiene 16 entradas repartidas en 3 meses y todas usan la misma versión 1.1.1. Esto no es SemVer. Si se añaden cosas nuevas, debería ser 1.2.0; si solo son correcciones, 1.1.2. Si aún no hay un lanzamiento oficial, todo debería ir bajo [Unreleased] hasta que decida liberar una versión concreta.

- Frases como "He tenido algunas dificultades...", "Me dedico a estudiar las causas..." o "BTW Se sigue el Plan..." sobran. Un changelog debe ser objetivo, frío y técnico: solo debe decir qué cambió (ej. "Se agrega archivo X", "Se corrige enlace Y"). No se pone el contexto personal ni los tropiezos del proceso.

- Ortografía y redacción: Tienes varias faltas ("froma", "referenia", "encuentrar"). Corregir antes de agregar nuevos cambios.


### 04/05/2026

- Se aprecia en [README](README.md) inclusión de instrucciones completas para replicar repositorio correctamente, así como la separación del contenido sobre el progreso de las fases en [FASES.md](/fases/FASES.md). 
- En [CHANGELOG.md](CHANGELOG.md) se aprecian que los enlaces se encuentran como
`[REVISION.md](https://github.com/Kozk9/Evidencias/blob/main/REVISION.`. 
Si bien esto funciona, cabe mencionar que en los proyectos no se utilizan URL `publicas`, sino `relativas`.
Para este caso, te comparto el como veo la estructura al clonar el repositorio en mi equipo con el comando `tree`:

```bash
$ tree .
.
├── CHANGELOG.md
├── ejercicios
│   └── fase1
│       ├── Fase1.md
│       └── fase1.txt
├── fases
│   └── FASES.md
├── LICENSE
├── notas
│   └── notas.txt
├── README.md
└── REVISION.md

5 directories, 8 files

```
De modo que en mi entorno `local`, la referencia relativa a [REVISION](REVISION.md) es directa, ya que ambas se encuentran en el mismo _nivel_ o el mismo _directorio_.

> Nota: Si fue deliverado (por las limitaciones de tu equipo), esta bien, solo hago el comentario por si se me paso.

> Nota 2: May The Force Be With You!

### 30/04/2026

- Sobre contenido de `/ejercicios` y `/notas`, se aprecia que se acataron las indicaciones.
- Como sugerencia a los mentorados, se hace la invitación a mover el contenido sobre los temas de la mentoria a un archivo separado y referenciarlo en el `README.md`, por ejemplo crear un archivo llamado `FASES.md` donde colocar eso y agregar enlaces de navegación al `README.md` y con un indice.

>Nota: es una sugerencia, si es demasiado o todavia hay dudas, puede no hacerse y no hay problema.

- Sobre [CHANGELOG](CHANGELOG.md), se aprecia una estructura muy bien elaborada. Se recomienda cambiar la jerarquía de los índices de 

```markdown
	
	### Add

	#### [1.1.1] - 2026-04-25

```
A esto:

```markdown
	
	#### Add

	### [1.1.1] - 2026-04-25

```
Debido a que entre menos caracteres `#` tenga un índice, mayor es su jerarquía. Las fechas, al ser bloques que separan la continuidad del trabajo, pueden contener N secciones como `Agregado`, `Bugs`, `Correcciones`, `Eliminado`, etc.

> Para ilustrarte con un ejemplo real, te recomiendo darle un vistazo a [sisdai-proyecto-base/CHANGELOG.md](https://github.com/CentroGeo/sisdai-proyecto-base/blob/main/CHANGELOG.md).

- Sobre [README](README.md), es necesario expandir las instrucciones de instalacion, ya que si bien se encuentran al final del repositorio, _deberían_ encontrarse al principio.

> Como ejemplo te puedo comparitr [sisdai-mapas/README.md](https://github.com/CentroGeo/sisdai-mapas/blob/main/README.md). Como es una biblioteca de frontend, trae instrucciones más detalladas con comandos como `npm install` para la instalación de las dependencias.

- En mi caso, para clonar tu repositorio ejecuté el siguiente comando en mi terminal:

```bash
	git clone https://github.com/Kozk9/Evidencias.git # Para HTTPS
	git clone git@github.com:Kozk9/Evidencias.git # Para SSH 
```

Y ya. Si en el futuro utilizas una libreria instalada con `npm` o `yarn`, entonces será necesario indicar también que después de clonar el repositorio deberás ejecutar:

```bash
	npm install 
```

- Sobre el contenido, no te presiones. Solo que, si no hay contenido o algo falta o esta en proceso, indicalo explicitamente con una nota o un comentario. Puede ser algo como `En proceso`, `Pendiente`, o para cosas pequeñas o etiquetas algo como `TBA` o `🚧`.

### 28/04/2026

- Se visualiza contenido con fases en [README](README.md) y casillas estilo `checkbox`. Se sugiere eliminar firma y lema de quién elaboró al final del contenido, así como agregar instrucciones para replicar repositorio, pues es la finalidad del archivo README.md. 
- Para [CHANGELOG](CHANGELOG.md), se sugiere revisar contenido agregado ya que aparecen notas con comentarios como `🚧# Changelog` que estan fuera del proposito del archivo. Además, el nombrel de archivo README está con el emoji 🚧. Favor de corregirlo, pues rompé compatibilidad con REVISION.md.
- Se visualizan folders de `ejercicios` y `notas`. Para `ejercicios` se aprecian notas que no parecen tener relación con el contenido, o bien, no está explicito cuál es su función. Favor de confirmar o corregir el contenido. 

### 23/04/2026

- Se acepta invitación a repositorio `Evidencias`.
- Se crea rama de `revision` a partir de `main`, donde se agrega archivo REVISION.md.
- Se confirma existencia de archivos [README](README.md), [CHANGELOG](CHANGELOG.md) y [LICENSE](LICENSE.md).
- Repositorio cuenta con rama principal.

> Notas: Quizá este vídeo pueda ayudar. Ya sé que es con windows, pero el proceso es similar [Enlace](https://www.youtube.com/watch?v=pRC8t6cFzJQ). 
