🐳 Contenedor creado con Docker

Este contenedor tiene como función principal crear y gestionar la base de datos MySQL necesaria para que el proyecto funcione correctamente.

Incluye toda la estructura inicial de tablas, usuarios y configuraciones requeridas por la aplicación.

📦 Requisitos

Antes de utilizar este contenedor, es necesario tener instalado:

Docker

📁 Carpeta de datos para MySQL (/data)

Este proyecto utiliza un contenedor Docker con MySQL.
Para que la base de datos pueda guardar información de forma persistente (es decir, que no se borre cuando el contenedor se reinicia), es necesario crear una carpeta local donde se almacenarán los archivos internos de MySQL.

🗂 ¿Para qué sirve esta carpeta?

La carpeta data/ actúa como un volumen local donde Docker guarda:

Tablas

Índices

Registros

Metadatos internos de MySQL

Sin esta carpeta, toda la información se perdería cada vez que se reinicia o elimina el contenedor.


🚀 ¿Qué hace este contenedor?

Levanta un servidor MySQL dentro de Docker.

Crea automáticamente la base de datos requerida por el proyecto.

Aplica la estructura necesaria (tablas, relaciones, índices, etc.).

Deja lista la conexión para que la aplicación funcione sin configuraciones adicionales.

▶️ Cómo utilizarlo

Ejecuta:

docker build -t nombre-contenedor .

docker run -d --name mysql-app -p 3306:3306 nombre-contenedor
