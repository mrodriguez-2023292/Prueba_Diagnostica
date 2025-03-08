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

![image](https://github.com/user-attachments/assets/bd3e11dd-01d1-49c4-bc07-ec87109fdd5f)

![image](https://github.com/user-attachments/assets/782e7597-cb40-4479-9f84-d0f36cc8bf6f)

![image](https://github.com/user-attachments/assets/dc75f640-364f-4615-ae2c-55558b32d8f5)

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

## Contribuir
Si deseas contribuir al proyecto, puedes hacer un **fork** del repositorio y enviar un **pull request** con tus mejoras.

## Licencia
Este proyecto está bajo la licencia MIT. Para más detalles, revisa el archivo LICENSE en el repositorio.

