# Mini Curso de Nodejs
## Documento para llevar a cabo el minicurso de nodejs

Se pegan los fragmentos de codigos que surgen del avance en el curso.

* Sobre el módulo `http`

```
import http, { request } from "http";

const server = http.createServer((req, res)=>{
    console.log("Un cliente se ha conectado")
    res.end("La conexión ha sido correcta")
})

server.listen(3000, ()=>{
    console.log("Servidor a la espera de conexiones")
})
``` 
* Sobre `express`

```
import express from "express"

const app = express()

app.get('/', (req, res)=>{
    res.send('La conexión ha sido correcta')
})

app.listen(3000, ()=>{
    console.log("Servidor a la espera de conexiones")
})
```
*Sobre como modularizar la app

El siguente código no funcionó.

```
import router from "./src/routes/index.routes"

const routes = router()
const app = express()

// routes
//const routes = require('.src/routes/index.routes')
app.use(routes)
//app.use(require('./src/routes/index.routes'))

app.listen(3000, ()=>{
    console.log("Servidor a la espera de conexiones")
})
```



