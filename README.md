# Proyecto Final de Programación

## Descripción
Este proyecto se centra en el desarrollo de una **API web** implementada en **NodeJS**, destinada a gestionar el registro de ventas, productos en línea y otras operaciones comerciales de una empresa.

La aplicación está estructurada en dos secciones principales:
- **Administrador**: Gestiona productos, ventas y usuarios.
- **Cliente**: Realiza compras y consulta productos.

## Tecnologías Utilizadas
- **NodeJS** con **Express.js** para la creación de la API.
- **MongoDB** o **MySQL** para la gestión de datos.
- **JWT** para la autenticación y autorización de usuarios.
- **argon2** para el manejo seguro de contraseñas.
- **Swagger** para la documentación de la API.

## Instalación
1. Clona el repositorio:
   ```bash
   git clone https://github.com/tu-usuario/nombre-del-repositorio.git
   ```

2. Instala las dependencias:
   ```bash
   cd nombre-del-repositorio
   npm install
   ```

3. Configura las variables de entorno en un archivo `.env`.
4. Inicia el servidor:
   ```bash
   npm start
   ```

## Cómo iniciar el proyecto

Como primer paso, el usuario o la persona que va a usar el programa tendrá que copiar el siguiente enlace del repositorio:

[https://github.com/mrodriguez-2023292/PB-2023292.git](https://github.com/mrodriguez-2023292/PB-2023292.git)

Después de clonar el repositorio, abre la carpeta creada, y en el **cmd** de esa carpeta, sigue estos pasos:

1. Instalar las dependencias necesarias:
   ```bash
   npm i
   ```

2. Inicializar el proyecto:
   ```bash
   npm run dev
   ```

3. Abrir la colección de endpoints:
   La ruta base para realizar todas las peticiones es:
   ```
   http://127.0.0.1:3000/storeSystem/v1/
   ```
   A partir de esta ruta base, se pueden hacer diferentes acciones o métodos.

## Endpoints

### Carpeta Auth:

| Método | Endpoint               | Descripción |
|--------|------------------------|-------------|
| POST   | `/auth/registerClient`  | Registro del cliente |
| POST   | `/auth/loginClient`     | Login del cliente |
| POST   | `/auth/loginAdmin`      | Login del admin |

**Nota**: El usuario **admin_master** es creado automáticamente al iniciar el proyecto. Las credenciales de acceso para el admin son las siguientes:

```json
{
  "username": "admin_master",
  "password": "Dm@n1234"
}
```

## Datos de Clientes

El proyecto ya incluye los siguientes datos de clientes para su uso:

| **Nombre** | **Apellido** | **Username**   | **Email**                    | **Teléfono** | **Contraseña**   |
|------------|--------------|----------------|------------------------------|--------------|------------------|
| Luis       | Perez        | luisperez      | luis.perez@example.com        | 56473829     | Lui$7890         |
| Carlos     | Gomez        | carlosgomez    | carlos.gomez@example.com      | 75395142     | Carlos1234!      |
| Ana        | Lopez        | analopez       | ana.lopez@example.com         | 87456239     | Ana@2023         |
| Javier     | Martinez     | javiermartinez | javier.martinez@example.com   | 12345678     | Javi#9876        |
| María      | Fernández    | mariafdez      | maria.fernandez@example.com   | 98765432     | Maria_2024       |
| Roberto    | Hernandez    | roberthernandez| roberto.hernandez@example.com | 11223344     | R0b3rto!56       |
| Sofia      | Perez        | sofiaperez     | sofia.perez@example.com       | 55667788     | Sofía123#        |
| David      | Ruiz         | davidruiz      | david.ruiz@example.com        | 99887766     | D@vid2023        |
| Lucia      | Sanchez      | luciasanchez   | lucia.sanchez@example.com     | 66554433     | Luci@2019        |
| Pedro      | Diaz         | pedrodiac      | pedro.diaz@example.com        | 44556677     | P3dro_987        |
| Laura      | Martínez     | lauramartinez  | laura.martinez@example.com    | 22334455     | L@ura1234        |

---

Con este formato, toda la información está más organizada y clara. Si deseas añadir más detalles o modificar algún aspecto del README, no dudes en decírmelo. ¡Espero que te sea útil!
