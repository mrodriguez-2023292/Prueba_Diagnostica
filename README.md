# Proyecto Final de Programación

## Descripción
Este proyecto se centra en el desarrollo de una API web implementada en **NodeJS**, destinada a gestionar el registro de ventas, productos en línea y otras operaciones comerciales de una empresa. 

La aplicación se estructura en dos secciones principales:
- **Administrador**: Gestiona productos, ventas y usuarios.
- **Cliente**: Realiza compras y consulta productos.

## Tecnologías Utilizadas
- **NodeJS** con **Express.js** para la creación de la API.
- **MongoDB** o **MySQL** para la gestión de datos.
- **JWT** para la autenticación y autorización de usuarios.
- **argon2** para el manejo seguro de contraseñas.
- **Swagger** para documentación de la API.

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

Como primer paso, el usuario o la persona que va a usar el programa tendrá que copiar el link del repositorio, el cual es el siguiente:

[https://github.com/mrodriguez-2023292/PB-2023292.git](https://github.com/mrodriguez-2023292/PB-2023292.git)

Ahora que se haya creado una carpeta con el nombre del repositorio, en esa carpeta que se creó se abre el **cmd** y en el **cmd** se hace lo siguiente:

1. Se instalan las dependencias necesarias del proyecto con el siguiente comando:
   ```bash
   npm i
   ```

Ya que se hayan instalado todas las dependencias, se puede inicializar el proyecto.

2. Para iniciar el proyecto, usa el siguiente comando:
   ```bash
   npm run dev
   ```

3. Abrir la colección de endpoints:

En los endpoints, la ruta base para poder hacer todas las peticiones es:

```
http://127.0.0.1:3000/storeSystem/v1/
```

Después de la última `/`, es cuando ya se pueden hacer diferentes acciones o métodos.

## Endpoints

### Carpeta Auth:

| Método | Endpoint               | Descripción |
|---------|------------------------|-------------|
| POST    | `/auth/registerClient` | Registro del cliente |

Ejemplo:
```json
{
    "name": "Luis",
    "surname": "Perez",
    "username": "luisperez",
    "email": "luis.perez@example.com",
    "phone": "56473829",
    "password": "Lui$7890"
}
```

| Método | Endpoint               | Descripción |
|---------|------------------------|-------------|
| POST    | `/auth/loginClient`    | Login del cliente |

Ejemplo:
```json
{
    "username": "luisperez",
    "password": "Lui$7890"
}
```

| Método | Endpoint               | Descripción |
|---------|------------------------|-------------|
| POST    | `/auth/loginAdmin`     | Login del admin |

Ahora bien, el admin se crea al iniciar el proyecto. Su usuario y contraseña son los siguientes:
| **Nombre** | **Apellido** | **Username**   | **Email**                    | **Teléfono** | **Contraseña**   |
|------------|--------------|----------------|------------------------------|--------------|------------------|
| Admin       | Principal        | admin_master      | admin@example.com        | 12345678     | Dm@n1234         |

## Datos de Clientes

El proyecto ya incluye los siguientes datos de clientes para su uso:

| **Nombre** | **Apellido** | **Username**   | **Email**                    | **Teléfono** | **Contraseña**   |
|------------|--------------|----------------|------------------------------|--------------|------------------|
| Luis       | Perez        | luisperez      | luis.perez@example.com        | 56473829     | Lui$7890         |
| Carlos     | Gomez        | carlosgomez    | carlos.gomez@example.com      | 75395142     | Carlos1234!      |
| Ana        | Lopez        | analopez       | ana.lopez@example.com         | 87456239     | Ana@2023         |
| Javier     | Martinez     | javiermartinez | javier.martinez@example.com   | 12345678     | Javi#9876        |
| María      | Fernández    | mariafdez      | maria.fernandez@example.com   | 98765432     | Maria_2024       |

---

## Carpeta Admin:

### Usuarios

| Método | Endpoint               | Descripción |
|---------|------------------------|-------------|
| POST    | `/admin/addUser` | Agregar un usuario(cliente) |

Ejemplo:
```json
{
    "name": "Carlos",
    "surname": "Gomez",
    "username": "carlosgomez",
    "email": "carlos.gomez@example.com",
    "phone": "12345678",
    "password": "passWo#d123"
}
```

| Método | Endpoint               | Descripción |
|---------|------------------------|-------------|
| GET    | `/admin/getUsers` | Listar todos los usuarios existentes del programa |

Para las operaciones de admin, se requiere autenticación con token. El token se obtiene tras el login del admin:

Ejemplo de respuesta:
```json
{
    "message": "Inicio de sesión exitoso",
    "userData": {
        "token": "<TOKEN_AQUI>"
    }
}
```

Este token se debe incluir en las peticiones para endpoints de admin.

| Método | Endpoint               | Descripción |
|---------|------------------------|-------------|
| PATCH    | `/admin/editRoleUser/:cid` | Cambiar rol de usuario |

Ejemplo:
```json
{
    "role": "ADMIN_ROLE"
}
```

| Método | Endpoint               | Descripción |
|---------|------------------------|-------------|
| DELETE  | `/admin/deleteUser/:cid` | Eliminar un usuario |

