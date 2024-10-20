# Prueba Técnica - Desarrollador Junior .NET

## Descripción del Proyecto

Esta es una aplicación web para la gestión de una biblioteca, desarrollada en **ASP.NET MVC** con **C#**. Permite a los usuarios:
- Ver una lista de libros registrados.
- Agregar nuevos libros y autores.
- Relacionar libros con sus autores correspondientes.

La aplicación utiliza **SQL Server** como base de datos y **Entity Framework** para interactuar con ella, manteniendo la relación entre libros y autores a través de claves foráneas.

## Pasos para Configurar y Ejecutar la Aplicación


## 1. Clonar el Repositorio
Clona el repositorio a tu máquina local usando Git:

```bash
git clone https://github.com/carenximem/PruebaTecnica.git
cd PruebaTecnica
```

## 2. Configurar la Base de Datos
1. Dentro del repositorio, localiza el archivo `DBA.sql`.
2. Ejecuta el script SQL en tu servidor SQL Server para crear las tablas `Libros` y `Autores`, así como las relaciones necesarias entre ellas.

   - Si usas **SQL Server Management Studio (SSMS)**:
     - Abre SSMS y conéctate a tu servidor.
     - Haz clic derecho en tu base de datos y selecciona "New Query".
     - Copia y pega el contenido del archivo `DBA.sql` y ejecútalo.

## 3. Actualizar la Cadena de Conexión
1. Abre el archivo `appsettings.json` dentro del proyecto (debería estar dentro de la carpeta `PruebaTecnica`).
2. Actualiza la cadena de conexión con los datos de tu servidor SQL Server. Asegúrate de incluir el nombre de tu servidor, base de datos, usuario y contraseña en la configuración.

 cadena de conexión:
   ```json
   "ConnectionStrings": {
      "DefaultConnection": "server=localhost; database=Biblioteca; integrated security=true; TrustServerCertificate=True;"
   }
   ```

## 4. Configurar Migraciones de Entity Framework 
Si estás utilizando Entity Framework para manejar la base de datos, asegúrate de que las migraciones estén configuradas correctamente. Si no has generado migraciones aún, puedes hacerlo con los siguientes comandos:

1. Abre la terminal en el directorio del proyecto y ejecuta:
   ```bash
   dotnet ef migrations add InitialCreate
   ```
2. Después, actualiza la base de datos con:
   ```bash
   dotnet ef database update
   ```

## 5. Abrir el Proyecto en Visual Studio
1. Abre **Visual Studio**.
2. Ve a **Archivo > Abrir > Proyecto/Solución** y selecciona el archivo `PruebaTecnica.sln` que se encuentra en la carpeta del repositorio.

## 6. Ejecutar la Aplicación
1. En Visual Studio, asegúrate de que la configuración del entorno esté en **Debug**.
2. Presiona `F5` o selecciona **Debug > Start Debugging** para ejecutar la aplicación.
3. La aplicación debería abrirse en tu navegador en la URL `https://localhost:{puerto}`, donde `{puerto}` es el número de puerto configurado en Visual Studio.

## 7. Verificar el Funcionamiento
1. Navega a la aplicación y asegúrate de que las funcionalidades principales, como la inserción y visualización de `Libros` y `Autores`, funcionen correctamente.
2. Si hay problemas con la base de datos o la configuración, revisa la cadena de conexión y los logs de errores para solucionar posibles inconvenientes.

# Funcionalidades de la aplicación
 1. Ingrese a la pagina principal y   de clic en "agregar nuevo autor"  si este aun no existe

![image](https://github.com/user-attachments/assets/ff24b06b-42c1-4207-8c53-7ad97155dcb2)

2. Ingrese el nombre del autor y de clic en "crear"
   
![image](https://github.com/user-attachments/assets/d02df6ff-78db-4c9d-bb22-616b75a15c11)

3.De clic en "volver a la lista" para que puedas ver todos los autores

![image](https://github.com/user-attachments/assets/a3f4d9c8-b9fa-4cd4-9357-a3f2eaf832a5)

4.Regrese a la pagina principal y de clic en "agregar nuevo libro"

![image](https://github.com/user-attachments/assets/9cfd9215-7a6a-4541-8685-b065cd83ab73)

5.Ingrese el nombre del libro y seleccion el autor y de clic en "crear"

![image](https://github.com/user-attachments/assets/cfa25121-c4be-4bbb-a5ca-a45f986cb1ec)

![image](https://github.com/user-attachments/assets/f73a7ce1-ff0a-4fc5-8751-70fde6e5b07a)


# Diagrama Entidad Relacion

![image](https://github.com/user-attachments/assets/c913542f-9dd6-4431-95a3-22a1ae5bc204)



