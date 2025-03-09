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
   
bash
   git clone https://github.com/tu-usuario/nombre-del-repositorio.git

2. Instala las dependencias:
   
bash
   cd nombre-del-repositorio
   npm install

3. Configura las variables de entorno en un archivo .env.
4. Inicia el servidor:
   
bash
   npm start


## Cómo iniciar el proyecto

Como primer paso, el usuario o la persona que va a usar el programa tendrá que copiar el link del repositorio, el cual es el siguiente:

[https://github.com/mrodriguez-2023292/PB-2023292.git](https://github.com/mrodriguez-2023292/PB-2023292.git)

Ahora que se haya creado una carpeta con el nombre del repositorio, en esa carpeta que se creó se abre el **cmd** y en el **cmd** se hace lo siguiente:

![image](https://github.com/user-attachments/assets/bd3e11dd-01d1-49c4-bc07-ec87109fdd5f)

![image](https://github.com/user-attachments/assets/782e7597-cb40-4479-9f84-d0f36cc8bf6f)

![image](https://github.com/user-attachments/assets/dc75f640-364f-4615-ae2c-55558b32d8f5)

1. Se instalan las dependencias necesarias del proyecto con el siguiente comando:
   
bash
   npm i


Ya que se hayan instalado todas las dependencias, se puede inicializar el proyecto.

2. Para iniciar el proyecto, usa el siguiente comando:
   
bash
   npm run dev


3. Abrir la colección de endpoints:

En los endpoints, la ruta base para poder hacer todas las peticiones es:

http://127.0.0.1:3000/storeSystem/v1/

Después de la última /, es cuando ya se pueden hacer diferentes acciones o métodos.

## Endpoints

### Carpeta Auth:

| Método | Endpoint               | Descripción |
|---------|------------------------|-------------|
| POST    | /auth/registerClient | Registro del cliente |

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
| POST    | /auth/loginClient    | Login del cliente |

Ejemplo:
```json
{
    "username": "luisperez",
    "password": "Lui$7890"
}
```

| Método | Endpoint               | Descripción |
|---------|------------------------|-------------|
| POST    | /auth/loginAdmin     | Login del admin |

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
| Roberto    | Hernandez    | roberthernandez| roberto.hernandez@example.com | 11223344     | R0b3rto!56       |
| Sofia      | Perez        | sofiaperez     | sofia.perez@example.com       | 55667788     | Sofía123#        |
| David      | Ruiz         | davidruiz      | david.ruiz@example.com        | 99887766     | D@vid2023        |
| Lucia      | Sanchez      | luciasanchez   | lucia.sanchez@example.com     | 66554433     | Luci@2019        |
| Pedro      | Diaz         | pedrodiac      | pedro.diaz@example.com        | 44556677     | P3dro_987        |
| Laura      | Martínez     | lauramartinez  | laura.martinez@example.com    | 22334455     | L@ura1234        |

### Carpeta Admin:

#### Autenticación para Admin

Para acceder a los endpoints de administración, se requiere autenticación mediante token, obtenido al iniciar sesión como admin:

| Método | Endpoint               | Descripción |
|---------|------------------------|-------------|
| POST    | /auth/loginAdmin     | Login del admin |

**Resultado:**
```json
{
    "message": "Inicio de sesión exitoso",
    "userData": {
        "token": "eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJhaWQiOiI2N2M3ZDY2MGU1ZTE3MGJmYWVmZmU3ODQiLCJpYXQiOjE3NDE0ODg3OTcsImV4cCI6MTc0MTQ5MjM5N30.GWu3TOzdgI7p5q-0_aCWlYSIM7qQHDw-Ne9fri_Norw"
    }
}
```

Este token debe incluirse en los encabezados de las solicitudes a los endpoints restringidos para administradores.

![image](https://github.com/user-attachments/assets/64839012-62f3-4f79-bd9c-944cf33109b2)

#### - Usuarios

| Método | Endpoint               | Descripción |
|---------|------------------------|-------------|
| POST    | /admin/addUser | Agregar un usuario (cliente) |

**Ejemplo:**
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
| GET    | /admin/getUsers | Listar todos los usuarios existentes del programa |

#### - Modificación de Usuarios

| Método | Endpoint               | Descripción |
|---------|------------------------|-------------|
| PATCH  | /admin/editRoleUser/:cid | Cambiar el rol de un usuario a ADMIN_ROLE |

**Ejemplo:**
```json
{
    "role": "ADMIN_ROLE"
}
```

| Método | Endpoint               | Descripción |
|---------|------------------------|-------------|
| PUT    | /admin/editUser/:cid     | Editar la información de un usuario |

**Ejemplo:**
```json
{
    "name": "nuevos nombres",
    "surname": "nuevos apellidos",
    "username": "nuevo nombre de usuario",
    "email": "nuevo correo",
    "phone": "nuevo numero",
    "password": "passWo#d123"
}
```

| Método | Endpoint               | Descripción |
|---------|------------------------|-------------|
| DELETE  | /admin/deleteUser/:cid | Eliminar un usuario |

---

### - Categorías

| Método | Endpoint               | Descripción |
|---------|------------------------|-------------|
| POST    | /category/addCategory  | Agregar una categoría |

**Ejemplo:**
```json
{
    "name": "Artículos para el hogar"
}
```

| Método | Endpoint               | Descripción |
|---------|------------------------|-------------|
| GET     | /category/getCategories | Listar todas las categorías |

| Método | Endpoint               | Descripción |
|---------|------------------------|-------------|
| PUT     | /category/editCategory/:id | Editar una categoría |

**Ejemplo:**
```json
{
    "name": "Plomería",
    "description": "En esta categoría solo se encontrarán cosas de plomería"
}
```

| Método | Endpoint               | Descripción |
|---------|------------------------|-------------|
| DELETE  | /category/deleteCategory/:id | Eliminar una categoría |

---

### - Productos

| Método | Endpoint               | Descripción |
|---------|------------------------|-------------|
| POST    | /product/addProduct    | Agregar un producto |

**Ejemplo:**
```json
{
    "name": "Laptop HP",
    "description": "Laptop con procesador Intel Core i7, 16GB RAM, 512GB SSD",
    "price": 1200.99,
    "stock": 50,
    "category": "Electrónica"
}
```

| Método | Endpoint               | Descripción |
|---------|------------------------|-------------|
| GET     | /product/getProducts   | Listar todos los productos |

| Método | Endpoint               | Descripción |
|---------|------------------------|-------------|
| PUT     | /product/editProduct/:id | Editar un producto |

**Ejemplo:**
```json
{
    "name": "Laptop HP ProBook",
    "description": "Modelo actualizado con mejor rendimiento",
    "price": 1300.99,
    "stock": 40,
    "category": "Electrónica"
}
```

| Método | Endpoint               | Descripción |
|---------|------------------------|-------------|
| DELETE  | /product/deleteProduct/:id | Eliminar un producto |

---

Esta documentación detalla los endpoints de la sección de administración, cubriendo usuarios, categorías y productos. Si necesitas agregar más detalles o modificar algo, avísame.

