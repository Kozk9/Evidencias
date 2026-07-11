# Mini Curso de Nodejs
## Documento para llevar a cabo el minicurso de nodejs

Se pegan los fragmentos de codigos que surgen del avance en el curso.

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
