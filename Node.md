### NodeJS  
[Node.JS](https://nodejs.org/en/docs)

 Estorno que nos permite ejecutar javascript sin necesidad de un navegador web. 
 -  Es recomendado usar versión LTS de NodeJS 
 -  Cuando se instala Node, se instala NPM que es un gestor de paquetes. 
 - Funciona a base de Módulos
 - Orientado a eventos, hay un un bucle de eventos que se ejecuta constantemente. 
 - Corre en el Motor V8
 - Es single thread (monohilo), por eso por ejemplo detiene el programa por completo al encontrar un error
##### Node vs Navegador 
  - Node
 Codigo JS ---> Motor V8 (Call Stack) <----> Bindings (API C/C++) <---> HTTP, crypto, etc <----> Libuv (gestionar tareas --- event loop )
 ![](https://codeahoy.com/img/books/libuv/nodejs-event-loop-architecture.png)
  - Navegador  (Chrome)
 Codigo JS ---> Motor V8 <----> WEBAPI <----> LIBEVENT( event loop )
 ![](https://res.cloudinary.com/practicaldev/image/fetch/s--eVmWSWwq--/c_limit%2Cf_auto%2Cfl_progressive%2Cq_auto%2Cw_880/https://github.com/khaosdoctor/my-notes/raw/master/node/assets/v8-real.png)
 
 
 #### Global
 Mientras que en el navegador JS posee un objeto window, en Nodejs pueden echar mano de algunas variables.
- process
- global
- module.exports and exports

#### ¿Qué es la variable global de Nodejs?
Es una variable global que es accesible por cualquier script de o programa de node. Se refiere al objeto global. Este tiene propiedades por ejemplo ```global.process```, ```global.require``` y ```global.console```.

Cualquier propiedad de primer nivel de global es accesible sin tener que referirse al prefijo global, por ejemplo para global.process se puede hacer referencia directa a process.
 
 #### CommonJS vs ModuleJS
 Sistema de módulos: Conjunto de utilidades que nos permite comunicar diferentes partes del código. Habitualmente cada parte se encuentra en archivos y carpetas separadas que necesitamos comunicar entre ellas. 
 
 Módulo: No es mas que una parte de código la cual puede ser utilizada por otros módulos.
 
 Con un sistema de Módulos nos permite: 
 - Encapsular funcionalidades e incrementar la reusabilidad +
 - Mejorar la estructura del proyecto 
 - Mejora la seguridad solo dispondremos en los distinytos modulos solo la funcionalidad que sea necesaria. 
 
 Sistema de Módulo CommonJS(CJS) : Sistema por defecto utilizado en NodeJs
 Sistema  ECMAScript ModuleJS(ESM): Sistema oficial de JS para la gestión de módulos. 
 
#### Protocolo HTTP
[Link - Protocolo HTTP](https://developer.mozilla.org/es/docs/Web/HTTP/Overview)
 La comunicación se basa en establecer un lenguaje y un medio común entre los diferentes participantes.  El módelo OSI es un estándar de interconexión de sistemas, se compone de 7 capas.  Capas de host/anfitrión (aplicación, presentación, sesión, transporte) y Capas del medio (Red, Enlace de datos, Física). 

 ![](https://i.ibb.co/48FhRfr/qq.png)

El protocolo HTTP es el estándar de la capa de transporte que nos permitira comunicarnos con los clientes. 
Se basa en petición/respuesta. El cliente pide primero y  el  servidor responde.  Un servidor también puede ser  tener el rol de cliente y hacer peticiones a otros servidores. 

Para comunicarnos utilizamos una cadena de texto (URL ) como identificador del host y del recurso. 

![](https://i.ibb.co/zZvPBL5/url.png)

Nos va a permitir solicitar o enviar diferentes tipos de datos o recursos. 

##### Solicitud HTTP
Se transforma la información de la URL en una solicitud, que es lo que se envía

![](https://i.ibb.co/TMmv5Kg/Sin-t-tulo.png)
##### Respuesta HTTP
EL servidor procesa la solicitu y emite una respuesta.

![](https://i.ibb.co/kgLchzs/respuestra.png)

[Métodos HTTP](https://developer.mozilla.org/es/docs/Web/HTTP/Methods)

[Status Codes](https://developer.mozilla.org/en-US/docs/Web/HTTP/Status)

##### Herramientas utiles
- nodemon (para desarrollo)
- PM2 (para producción)

##### NPM: Gestor de paquetes 


##### Promesas 
- Callback
- Calback Hell 
- Promesas
- Async/ await 
- try/catch 

#### Más
- Procesos hijos
- console (.log, .info, .error, .warn , .table, .count, .time, .timeEnd, .group, .groupEnd, .clear, .countReset)
- Módulos nativos en C++ (npm i -g node-gyp)
- File System
- Process
- Os (.arch, .platform, .cpus, etc)

#### Módulos utiles 
- bcrypt 
- moment 
- sharp 
 ##### Buffers - espacio en memoria RAM
 ##### Streams - proceso de consumir datos al tiempo que se recibe 
 ##### Benchmarking 
 ##### Debugger - node -- inspect archivo_name  | chrome://inspect/#divices |npx nodemon --inspect archivo_name
 ##### Error First Callback - el error es el primer caso 
 ##### Scraping en Node - web scraping es una técnica utilizada mediante programas de software para extraer información de sitios web 
 ##### Automatización de procesos - npm i gulp gulp-server-livereload
 ##### Electron - sirve para crear app de escritorio

 #### package.json
 #### gitignore
 #### editorConfig 
 #### eslintrc


 ### RESTfulAPI - Representational State Transfer
 Es una convención que comunmente se utiliza para desarrollar servicios web, que al final se comunican por el protocolo HTTP. Algunos de los métodos: GET, PUT, POST, DELETE. 
 - GET: Recibir parametros ( req.params)
 - GET: parametros query (req.query)
 - POST: (req.body)


 ### API
 Una API ​es una pieza de código que permite a diferentes aplicaciones comunicarse entre sí y compartir información y funcionalidades. Una API es un intermediario entre dos sistemas, que permite que una aplicación se comunique con otra y pida datos o acciones específicas. Las API permiten que sus productos y servicios se comuniquen con otros, sin necesidad de saber cómo están implementados.


 ###  Principios SOLID 

 [SOLID](https://www.freecodecamp.org/espanol/news/los-principios-solid-explicados-en-espanol/)


### Middlewares
Se encarga de ejecutar una funcióndde forma previa
Se prodia decir que es una función que esta entre Request y Response 
Resquest ---> Middleware ----> Response 

- Uses cases:
  - Funcionar como pipes
  - Validar datos
  - Capturar Errores 
  - Validar permisos 
  - Controlar accesos

- Middlewares más comunes
  - CORS
  - MORGAN
  - HELMET
  - EXPRESS DEBUG 
  - EXPRESS SLASH
  - PASSPORT

- Consideraciones para producción 
  - Cors
  - https
  - procesos de build
  - remover logs
  - seguridad (helmet)
  - testing 


 