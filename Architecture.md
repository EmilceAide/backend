## The Clean Architecture

Forma de estructurar las aplicaciones, se puede usar tanto en frontend como en backend. 
![](https://miro.medium.com/v2/resize:fit:1400/1*0u-ekVHFu7Om7Z-VTwFHvg.png)

- [Onion Architecture](https://dz2cdn1.dzone.com/storage/temp/4436217-kolka.png)
- [DCI Architecture](https://1.bp.blogspot.com/_txlKc91hcCk/TF6xq1pBvSI/AAAAAAAAAE4/N-fnCNd4RRs/s1600/DCI_MetaModel_Modified.png)
- [Hexagonal Architecture](https://www.happycoders.eu/wp-content/uploads/2023/01/hexagonal-architecture-vs-clean-architecture-2.v4-800x310.png)

Aunque todas estas arquitecturas varían un poco en sus detalles, son muy similares. Todos tienen un mismo objetivo, que es la separación de responsabilidades. Todos logran esta separación dividiendo el software en capas. Cada uno tiene al menos una capa para logica de negocio y otra para interfaces.

### Cada una de estas arquitecturas produce sistemas que son:

- Independiente de Frameworks. La arquitectura no depende de la existencia de alguna biblioteca de software cargado de funciones. Esto le permite utilizar dichos marcos como herramientas.
- Comprobable. La lógica de negocio se pueden probar sin la interfaz de usuario, la base de datos, el servidor web o cualquier otro elemento externo.
- Independiente de la IU. La interfaz de usuario puede cambiar fácilmente, sin cambiar el resto del sistema. Una interfaz de usuario web podría reemplazarse con una interfaz de usuario de consola, por ejemplo, sin cambiar las logica de negocio.
- Independiente de la base de datos. Puede cambiar Oracle o SQL Server por Mongo, BigTable, CouchDB o cualquier otra cosa. Sus reglas comerciales no están vinculadas a la base de datos.
[...más información](https://blog.cleancoder.com/uncle-bob/2012/08/13/the-clean-architecture.html)

### Hexagonal Architecture
![](https://i.ibb.co/6ZMrCq2/1.png)
![](https://i.ibb.co/wLStYq7/2.png)
![](https://i.ibb.co/dsZqjHJ/3.png)
![](https://i.ibb.co/rpyXZvJ/5.png)
![](https://i.ibb.co/HH1wyQY/6.png)
![](https://i.ibb.co/R3tM44j/7.png)
![](https://i.ibb.co/rdwk9pj/8-quien-eres-y-que-tipo.png)
![](https://i.ibb.co/wWPPrT2/9.png)