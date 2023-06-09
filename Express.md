### Express
Es una librería flexible para **Node.js** que va a ser clave para la creación  del *servidor*. 

Dentro del archivo en el que utilicemos **Express** lo vamos a requerir (*required*) y crearemos una variable con la que utilizaremos este framework (por lo general la variable se le llama *app*). También, como estamos trabajando con servidores, vamos a crear un método **listen** para poder reflejar nuestro trabajo en un puerto.

```
const express = required('express');
const app = express();

app.listen(3000);
```

En [este link](https://expressjs.com/en/4x/api.html#express) podremos ver toda la documentación, incluyendo todos los métodos y propiedades que podemos utilizar. Se recomienda ver.


### ORM - Object Relational Model 
Es un modelo de programación que permite mapear las estructuras de una base de datos relacionles. 

- Sequelize
[Link](https://sequelize.org/)
- TypeORM 
[Link](https://typeorm.io/)

### Migraciones 

En Django es la forma en la que django *propaga cambios* en los modelos y los refleja en los esquemas de base de datos. 

Para Seuqelize es un sistema de *control de versiones* para manejar los cambios desde el código y traquear cambios en la base de datos. 

Las migraciones mantienen el historial del esquema que vamos llevando en nuestra base de datos. 