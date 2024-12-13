# Como añadir un usuario a unan distribucion linux

---
- **Añadir un usuario mediante consola**
---
## **Cracion del usuario**
- _
    - En la terminal, puedes usar el siguiente comando para crear un nuevo usuario. Reemplaza nombre_usuario con el nombre que deseas darle al nuevo usuario:

```bash

sudo adduser nombre_usuario.


```
- _
  - Se te pedirá que ingreses tu contraseña de administrador (la contraseña de tu usuario actual).

  - Luego, se te pedirá que ingreses y confirmes una nueva contraseña para el nuevo usuario.

  - También puedes proporcionar información adicional (como nombre completo, número de teléfono, etc.), pero puedes presionar Enter para omitir estos campos.

---
## **Agregar el Usuario a Grupos (Opcional)**
- _
    - Si deseas que el nuevo usuario tenga privilegios de sudo (es decir, que pueda ejecutar comandos como administrador), debes agregarlo al grupo `sudo`. Puedes hacerlo con el siguiente comando:


```bash

sudo usermod -aG sudo nombre_usuario
```
---
# **Verificar la creacion del usuario**
- _
    - Puedes verificar que el usuario se ha creado correctamente ejecutando el siguiente comando:


```bash

cat /etc/passwd | grep nombre_usuario
```

---
# Como eliminar un usuario a unan distribucion linux

---
- **Eliminar un usuario mediante consola**
---
## **Eliminacion del usuario**

- _
    - Para eliminar un usuario, utiliza el siguiente comando. Reemplaza nombre_usuario con el nombre del usuario que deseas eliminar:
```bash

sudo deluser nombre_usuario.

```
- _
    - Se te pedirá que ingreses tu contraseña de administrador (la contraseña de tu usuario actual)

---
## **Eliminar el Directorio Home del Usuario (Opcional)**
- _
    - Si también deseas eliminar el directorio home del usuario (donde se almacenan sus archivos personales), puedes usar el siguiente comando:


```bash

sudo deluser --remove-home nombre_usuario
```
---
# **Verificar la eliminacion del usuario**
- _
    - Puedes verificar que el usuario ha sido eliminado ejecutando el siguiente comando:


```bash

cat /etc/passwd | grep nombre_usuario
```