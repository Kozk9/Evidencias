# Evidencias
Repositorio para Evidencias sobre el Plan de Formación Técnica para SAPCI.
## Plan de Formación Técnica:
## Backend con Node.js, Express y PostgreSQL
### Coordinación Técnica de Gestión de Información, Evaluación, Tecnologías y Estadísticas
#### Abril, 2026

> Ruta de aprendizaje prograsiva y autogestionada orientada al desarrolle backend. El enfoque prioriza
> la comprensión de la asincronía, el manejo de peticiones HTTP y la integración con bases de datos
> relacionales. Se recomienda llevar un registro continuo en un repositorio personal de evidencias. Sin
> fechas límite: Avanza a tu ritmo y consolida cada concepto antes de continuar.

## Repositorio de Evidencias (GitHub)
- [ ] Crear un reposotorio público o privado bajo su cuenta de GitHub.
- [ ] Estructura inicial recomendada:

      **README.md** Propósito del repositorio, stack en estudio, enlaces a recursos útiles y notas generales de aprendizaje. 
      **CHANGELOG.md** Bitácora de progreso (conceptos explorados, dudas resueltas, patrones descubiertos, sin marcar fechas). 
      **REVISION.md** Archivo vacío inicialmente. Aquí se centralizará la retroalimentación del mentor.  
      /ejercicios/ o /notas/: Carpetas para snippets, pruebas aisladas y documentación interna.  
- [ ] Flujo de revisión: al consolidar un bloque temático, abrir un Pull Request (PR) / Merge Request (MR) hjjacia la rama principal. El mentor revisará y añadirá comentarios o sugerencias directamente en **REVISION.md** dentro del mismo PR.
- [ ] Mantener un historial de commits limpio y descriptivo (docs:, feat:, chore:, refactor:)

## Fase 1: JavaScript desde Cero (con base de programación)
- [ ] Sintaxis básica: Tipos, operadores, estructuras de control (if, for, while).
- [ ] Funciones: declaración, expresiones, ámbitos y closures.
- [ ] Objetos y arrays literales: creación, acceso, mutación.
- [ ] Programación orientada a prototipos vs clases (ES6)
- [ ] El entorno Node.js: REPL, ejecuución de scripts, módilos nativos (fs, path, http).
- [ ] _Documentar en el repo: snippets que contrasten con otros lenguajes (Python, Java, C#). Notas sobre el modelo de objetos de JS._

## Fase 2: JavaScript Moderno (ES6+) orientado a backend
- [ ] Variables: **let** y **const** vs **var**, alcance de bloque.
- [ ] Funciones flecha (**()=>**) y su impacto en **this** (especialmente en callbacks).
- [ ] Destructuring de objetos/arrays y operadores spread/rest (...).
- [ ] Tempate literals y taggeg templates (útil para consultas SQL parametrizadas).
- [ ] Módulos ES: import/export (named vs default) en Node.js con "type": "module" o .mjs.
- [ ] Métodos funcionales de arrays: map, filter, reduce, find, some/every (fundamentales para transformación de datos).
- [ ] Manejo de asincronía: callbacks (problemas),  Promesas (then/catch), async/await y try/catch.
- [ ] Documentar en el repo: ejemplos prácticos de cada característica aplicadas a procesamiento de datos (listas, objetos).

## Fase 3: Fundamentos de Backend y HTTP
- [ ] Modelo cliente-servidor, peticiones/respuestas, métodos HTTP (GET, POST, PUT, DELETE, PATCH).
- [ ] Códigos de estado (2xx, 3xx, 4xx, 5xx) y cabeceras comunes (Content-Type, Authorization).
- [ ] JSON como formato de intercambio: serialización/deserialización (JSON.stringify, JSON.parse).
- [ ] El método **http** nativo de Node.js: crear un servidor básico y manejar rutas a mano.
- [ ] Comparación con frameworks: por qué Express simplifica el enrutamiento y el middleware.
- [ ] _Documentar en el repo: servidor HTTP mínimo con Node puro, ememplos de curl para probarlo._

## Fase 4: Express.js - Primeros Pasos
- [ ] Inicialización de proyecto con **npm init**, instalación de express.
- [ ] Aplicación mínima: **app.get()**, **app.listen()**, ruta raíz.
- [ ] Manejo de rutas: par+ametros de ruta (**/users/:id**), query strings (**req.query**).
- [ ] Middleware: concepto, **app.use()**, orden de ejecución. Middleware integrados: **express.json()**, **express.urlencoded()**.
- [ ] Envío de respuestas: **res.send(), res.json(), res.status()**.
- [ ] Manejo de errores básico con middleware de error (cuatro parámetros).
- [ ] _Documentar en el repo: API simple de gestión de tareas (CRUD en memoria). Incluir ejemplos de peticiones con Postman o curl_.

## Fase 5: PosgreSQL y Conexión desde Node.js
- [ ] Instalación y gestión de PostgreSQL (local o Docker). Conceptos: base de datos, esquema, tablas, tipos.
- [ ] SQL esencial: SELECT, INSERT, UPDATE, DELETE, JOIN básico.
- [ ] Cliente psql y creación de una base de datos para la API.
- [ ] Librería **pg** (node-postgres): conexión con Pool, ejecución de consultas parametrizadas (evitar inyección SQL).
- [ ] Patrón repositoio: separar la lógica de acceso a daros del controlador.
- [ ] Uso de **async/await** con consultas a PostgreSQL.
- [ ] _Documentar en el repo: script de migración inicial (creación de tabla **items** o similar), ejemplos de **client.query** con parámetros_.

## Fase 6: API REST Completa con Express + PostgreSQL
- [ ] Estructura de proyecto por capas: rutas controladores, servicios, repositorios.
- [ ] Variables de entorno con **dotenv** (puerto, cadena de conexión a BD).
- [ ] Operaciones CRUD completas para un recurso (ej. **/api/productos**).
- [ ] Validación de datos de entrada (manual o con **express-validator**).
- [ ] Manejo de errores asíncronos en Express (**wrapper asyncHandler** o **try/catch**).
- [ ] Documentación básica de la API (puede ser con cimentarios usando Swagger/OpenAPI).
- [ ] _Documentar en el repo: código organizado, colección de Postman, exportada, ejemplos de respuestas exitosas y de error_.

## Fase 7: Buenas Prácticas y Preparación para Entornos Reales
- [ ]  Uso de **nodemon** en desarrollo y **pm2** en producción (gestión de procesos).
- [ ]  Logging con **morgan** (request) y **winston** (logs estructurados).
- [ ]  Pruebas unitarias e integración con Jest o Vitest (para rutas y base de datos).
- [ ]  Autenticación básica: **JWT (JSON Web Tockens)** y middlewares de protección de rutas.
- [ ]  Migraciones y seeders para base de datos (usando **node-pg-migrate** o similar).
- [ ]  Seguridad: helmet, rate limiting, sanitización de entradas.
- [ ]  Integración den GitLab CI/CD básico (ejecutar pruebas, desplegar a servidor de pruebas).
- [ ]  _Documentar en el repo: pipeline de CI, configuración de variables de entorno en producción, script de despliegue_.

___
**Notas de acompañamiento:**
+ Recisión asíncrona vía PR/MR en el repo de evidencias.
+ Retroalimmentación centralizada en **REVISION.md**.
+ Sin presiones de tiempo; se valora la comprensión pfofunda, la calidad del registro y la capacidad de auto-documentación.
+ Acceso libre a documentación oficial (MDN, Node.js docs, Express guide, PostgreSQL tutorial) y entornos de prueba.
+ Se recomienda usar **curl, Postman** o **Insomnia** para probar endpoints.

___
**Elaboró**: Jefatura de Unidad Departamental de Informática.
_Por la soberanía tecnológica_
