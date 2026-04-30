## REVISION.md para revisión de programa de mentoria


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
