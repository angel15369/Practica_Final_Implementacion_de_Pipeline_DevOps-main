🛠️ Proyecto Final: Diseño e Implementación de un Pipeline DevOps
📌 Descripción General
Este proyecto tuvo como objetivo principal diseñar e implementar un pipeline DevOps funcional para una aplicación web sencilla, integrando los conocimientos adquiridos a lo largo del curso. La solución final incluyó control de versiones, integración y despliegue continuo (CI/CD), pruebas automatizadas, contenedores Docker, y monitoreo básico del sistema.

🎯 Objetivos del Proyecto
Desarrollar una aplicación web simple (frontend + backend + base de datos).

Implementar un pipeline CI/CD automatizado mediante GitHub Actions.

Integrar pruebas automatizadas para validar la calidad del código.

Contenerizar la solución completa usando Docker.

Habilitar monitoreo básico para evaluar el desempeño de la aplicación.

⚙️ Estructura del Workflow CI/CD (deploy.yml)
El archivo deploy.yml define el pipeline automatizado con los siguientes pasos:

Clonado del repositorio: Uso de actions/checkout.

Configuración del entorno .NET: Instalación del SDK .NET 8.0.

Restauración de dependencias: Comando dotnet restore.

Compilación del proyecto: dotnet build en modo Release.

Publicación de la app: Empaquetado con dotnet publish.

Ejecución local de la app: En el puerto 8080.

Verificación con curl: Para comprobar la respuesta HTTP.

Detención del proceso (opcional): Uso de pkill.

🔍 Resultados del pipeline
Clonado y configuración del entorno: ✔️

Restauración, compilación y publicación: ✔️

Verificación: ❌ Error HTTP 500 (requiere revisión del backend).

Limpieza del entorno: ✔️

🐳 Implementación con Docker, ASP.NET Core y SQL Server
Se usó Docker para crear un entorno aislado y reproducible, tanto para la base de datos como para la aplicación. Los pasos realizados fueron:

🔹 1. Base de datos en Docker
Uso de la imagen oficial de SQL Server desde Docker Hub.

Configuración de credenciales, puertos y persistencia.

Conexión verificada con SSMS.

🔹 2. Aplicación conectada a la base de datos
Desarrollada con C# y ASP.NET Core.

Conexión configurada en appsettings.json.

Entity Framework Core para manejo de datos.

🔹 3. Inventario funcional
Interfaz con funciones de agregar, editar y eliminar elementos.

Tabla dinámica con DataTables (paginación, búsqueda y ordenamiento).

🔹 4. Despliegue completo con Docker
Contenedor adicional para la app web.

Red Docker para comunicación entre contenedores.

Uso de docker-compose.yml para orquestar servicios.

📁 Archivos Clave
Dockerfile

docker-compose.yml

deploy.yml (Workflow CI/CD)

✨ Características adicionales
Validaciones en frontend y backend.

Manejo de excepciones.

Interfaz responsiva con Bootstrap.

✅ Beneficios de la arquitectura aplicada
Escalabilidad: Docker permite mover la app fácilmente.

Mantenimiento: Servicios desacoplados y organizados.

Portabilidad: Configuración replicable en otros entornos.

📄 Entregables del Proyecto
Código fuente en GitHub con documentación y scripts.

Dockerfile y archivo de configuración del pipeline.

Manual técnico con guía de instalación y operación.

Presentación con demo funcional y lecciones aprendidas.
