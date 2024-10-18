# Prueba Técnica - Desarrollador Junior .NET

## Descripción del Proyecto

Esta es una aplicación web para la gestión de una biblioteca, desarrollada en **ASP.NET MVC** con **C#**. Permite a los usuarios:
- Ver una lista de libros registrados.
- Agregar nuevos libros y autores.
- Relacionar libros con sus autores correspondientes.

La aplicación utiliza **SQL Server** como base de datos y **Entity Framework** para interactuar con ella, manteniendo la relación entre libros y autores a través de claves foráneas.

## Pasos para Configurar y Ejecutar la Aplicación

1. **Clonar el repositorio**:
   ```bash
   git clone https://github.com/carenximem/PruebaTecnica.git
   ### Configurar la base de datos:

1. Ejecuta el script SQL proporcionado en `database-script.sql` para crear las tablas **Libros** y **Autores**, y establecer la relación entre ellas en tu servidor SQL Server.

### Actualizar la cadena de conexión:

1. Abre el archivo `appsettings.json` y actualiza la cadena de conexión con los datos de tu servidor SQL Server.

### Ejecutar la aplicación:

1. Abre el proyecto en Visual Studio.
2. Ejecuta la aplicación presionando `F5` o seleccionando `Debug > Start Debugging`.
