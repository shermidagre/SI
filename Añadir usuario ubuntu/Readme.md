# Como añadir un usuario a unan distribucion linux

---
- **Añadir un usuario mediante consola**
---
**El usuario se puede añadir de dos maneras en la barra de comandos, cada manera tiene sus diferentes funciones**

# Diferencias Clave entre `useradd` y `adduser`


## 1. Configuración Predeterminada

- **useradd**: No establece configuraciones predeterminadas. Te obliga a especificar todos los detalles de la cuenta usando opciones de comando, como un verdadero guerrero que afina su espada.

- **adduser**: Aplica valores predeterminados para grupos, directorios de inicio y otros parámetros. Te facilita la vida, como un sabio maestro que te guía en el camino.


## 2. Solicitud de Contraseña

- **useradd**: No te pide una contraseña para el usuario recién creado. Si quieres proteger la cuenta, deberás usar la opción `-p` para establecer una contraseña como un ninja sigiloso.

- **adduser**: Te solicita que introduzcas una contraseña durante el proceso de creación de la cuenta, garantizando la seguridad desde el inicio.


## 3. Creación del Directorio de Inicio

- **useradd**: No crea automáticamente el directorio de inicio del usuario. Si lo necesitas, usa la opción `-m` para crear un hogar para el nuevo usuario.

- **adduser**: Crea automáticamente el directorio de inicio del usuario en la ubicación predeterminada, como un constructor diligente que prepara un nuevo hogar.


## 4. Interfaz de Usuario

- **useradd**: Te exige usar opciones de línea de comandos específicas para definir las características de la cuenta, como un guerrero que domina su arma.

- **adduser**: Te ofrece una interfaz interactiva que facilita la configuración de la cuenta del usuario, permitiéndote navegar por el proceso con la fluidez de un maestro Jedi.


## 5. Disponibilidad

- **useradd**: Disponible en todas las distribuciones de Linux, como un guerrero omnipresente.

- **adduser**: Puede no estar disponible en todas las distribuciones. En algunas, como Arch Linux, `useradd` es el comando central para la creación de usuarios, como un líder que toma el control.
---
## **Cracion del usuario mediante adduser (manera mas completa)**
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