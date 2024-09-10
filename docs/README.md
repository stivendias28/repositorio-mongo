
# Proyecto MongoDB NoSQL

## Descripción

Este proyecto implementa una base de datos NoSQL utilizando MongoDB. A lo largo del proyecto, se trabajó con diversas colecciones que representan empleados, departamentos, proyectos y tareas dentro de una empresa ficticia. Las operaciones CRUD (Crear, Leer, Actualizar y Eliminar) se implementaron de manera eficiente y se realizaron consultas avanzadas para analizar los datos almacenados.

## Estructura del Proyecto

1. **Base de Datos**: `pequena_empresa`
   - Colecciones:
     - `empleados`: Información de los empleados (nombre, edad, cargo, etc.).
     - `departamentos`: Detalles sobre los departamentos.
     - `proyectos`: Proyectos asignados a los empleados.
     - `tareas`: Tareas asociadas a cada proyecto.

2. **Consultas**: 
   - Operaciones CRUD para la gestión de datos.
   - Consultas avanzadas para extraer datos específicos de las colecciones.

## Requisitos

- **MongoDB**: Se utilizó para la creación y administración de la base de datos.
- **MongoDB Shell**: Para la ejecución de comandos y consultas.
- **MongoDB Compass**: Para la visualización y gestión gráfica de la base de datos.
- **Git**: Para la clonación y gestión del repositorio.

## Instalación

1. Clonar el repositorio:

   ```bash
   git clone https://github.com/stivendias28/repositorio-NOSql.git
   ```

2. Exportar la base de datos MongoDB:

   ```bash
   mongodump --db pequena_empresa --out "C:\Users\Stiven_Lopez\OneDrive\Documentos\BASE_SQL\repositorio-mongo\repositorio-mongo\backups"
   ```

## Uso

### Consultas CRUD

- **Leer todos los empleados**:
  
  ```bash
  db.empleados.find().pretty()
  ```

- **Actualizar salario de un empleado**:

  ```bash
  db.empleados.updateOne({ "nombre": "María Gómez" }, { "$set": { "salario": 45000 } })
  ```

- **Eliminar un departamento**:

  ```bash
  db.departamentos.deleteOne({ "nombre": "Ventas" })
  ```

- **Insertar nuevo empleado**:

  ```bash
  db.empleados.insertOne({
    "nombre": "Luis Martínez",
    "edad": 32,
    "departamento_id": ObjectId(),
    "email": "luis.martinez@empresa.com",
    "telefono": "555-7890",
    "cargo": "Diseñador",
    "salario": 45000,
    "fecha_contratacion": "2022-02-20",
    "proyectos_asignados": [ObjectId()]
  })
  ```

## Conclusiones

MongoDB ha demostrado ser una herramienta poderosa para manejar bases de datos NoSQL, permitiendo una gran flexibilidad y escalabilidad. Se logró implementar con éxito las operaciones CRUD y consultas avanzadas. La estructura de los datos permitió gestionar relaciones de manera sencilla a través de `ObjectId`, facilitando el manejo de colecciones sin la necesidad de esquemas rígidos.

## Recomendaciones

1. Implementar índices para optimizar las consultas.
2. Realizar copias de seguridad periódicas.
3. Monitorear la escalabilidad conforme crezca el número de registros.

## Referencias

- [Documentación de MongoDB](https://docs.mongodb.com/)
- [Repositorio GitHub](https://github.com/stivendias28/repositorio-NOSql.git)
