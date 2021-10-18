# [WiP]Práctica Global GBD 2º Trim 1ASIR
Repositorio que contiene los archivos de la práctica global de Gestión de Bases de Datos de 1º ASIR

## Contenido del repositorio
 - Descripción de casuística ([a continuación](#descripción-de-la-cusuística))
 - [Esquema E-R](https://github.com/gonzaleztroyano/asir1-gbd-practicaglobal/raw/main/DiagramaEntidadRelacion.png)
 - [Modelo Relacional](./ModeloRelacional.pdf)
 - [Diagrama de dependencias](./Dependencias.pdf)
 - [Normalización](./Normalización.pdf)
 - [Creación de tablas e inserción de datos](#Creación-de-tablas-e-inserción-de-datos)
 - [Sentencias SQL de ejemplo](#Sentencias-SQL-de-ejemplo)

### Descripción de la cusuística
Se solicita el diseño de una Base de Datos relacional que se adapte a la situación que se describe a continuación:
> Una tienda de librerías desea gestionar de forma centralizada sus datos. 
> Desean mantener un listado de los clientes y de los empleados que tiene en nómina. Se gestionará un listado de libros disponibles, escritos por autores (no se realiza sobre estos seguimiento de *stock*). Los clientes realizarán pedidos de estos libros, 1 pedido = 1 libro, con el apoyo de un trabajador. 
> A su vez, la compañía cuenta con una serie de locales en los que se celebran eventos. 

### Datos mínimos a mantener.
 - Sobre los clientes:
   - DNI u otro documento identificativo
   - Su nombre y su(s) apellido(s).
   - Fecha en la que se convirió en socio del establecimiento
   - El email de contacto.
 - Sobre los autores:
   - DNI o similar
   - Nombre y apellidos
   - Nacionalidad
- Sobre los libros:
  - ISBN, com identificador único de los libros
  - Autor o autora que lo ha escrito
  - Título del libro
  - Resumen del mismo
  - PVP del libro en ese momento
  - Fecha de publicación
  - Editorial que edita el libro. 
  - Número de páginas del mismo.
- Sobre las tiendas
  - ID de la oficina o local
  - Ciudad donde se encuentra
  - Región (agrupación mayor de tiendas. Ej, Norte, Centro, Este).
  - Se reservará un campo para almacenar las ventas de la oficina.
- Sobre los trabajadores:
  - Identificador del empleado/a
  - Nombre y apellidos de empleado/a
  - Fecha de contratación
  - Puesto que ocupa
  - Ventas que ha realizado
  - Oficina en la que desempeña su puesto. 
- Sobre los pedidos:
  - Número de pedido (puede ser un autoincremental u otro que se defina)
  - Cliente que ha realizado el mismo
  - Vendedor que ha asistido la venta
  - Libro que se ha adquirido
  - Fecha de adquisición
  - Importe del libro en el momento de la adquisición
- Sobre los eventos celebraados:
  - Identificador único del evento
  - Fecha del evento
  - Autor invitado al mismo
  - Oficina o local propiedad de la empresa en el que se ha celebrado
  - Coste, de tenerlo, que supone para la empresa la asistencia del autor
  - IMPORTANTE: Se desea guardar un registro de la asistencia a los eventos. Para ello es necesario tener en cuenta que un mismo cliente puede acudir a más de uno (siendo necesario guardar todos). También se desa guardar la butaca en la que se ha situado el asistente con el fin de reconocer contactos estrechos en caso de resultado positivo, motivado por la situación pandémica.  


# Creación de tablas e inserción de datos
En base a lo anteriormente expuesto se propone la creación de las tablas que se pueden ver en [este documento](./creacion_tablas-libros.txt).
A su vez, se insertan [estos datos](./inserciones-libros.txt) para facilitar el trabajo y la práctica. 

Para crear las inserciones en la base de datos se ha utilizado [esta Hoja de Cálculo de Google](https://docs.google.com/spreadsheets/d/e/2PACX-1vRTuZgZKcHg35HDMT9gsCXMrqt1-WcHcI21dyb-phopM0MM-CRkt8QwqzMp2MkmdpS7h2i5SHkEiioN/pubhtml). Mención especial merece el complemento HdC+ para Google Sheets de Pablo Felip, que se puede conseguir desde [este enlace](https://workspace.google.com/marketplace/app/hdc+/410659432888) hacia Google Workspace Marcketplace.


# Sentencias SQL de ejemplo
Se proponen [estos ejercicios](./SentenciasSQL-1.pdf) a nivel general: sentencias SELECT sencillas, con condicionales WHERE simples y el uso de ORDER BY para obtención de resultados. 
En tanto a funciones y procedimientos, se proponen estos [otros ejercicios](./SentenciasSQL-2.pdf) especializados. 
