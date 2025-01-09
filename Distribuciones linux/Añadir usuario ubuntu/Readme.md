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
---
# Ejemplos de Uso


## Crear un Usuario Llamado «nuevo_usuario» con `useradd`

```bash

useradd -m -p "contraseña_segura" nuevo_usuario
```
- 
  - m: Crea el directorio de inicio del usuario, como un constructor diligente.
  - p: Establece la contraseña del usuario, fortaleciendo la seguridad como un ninja sigiloso.

---
## Crear un Usuario Llamado «nuevo_usuario» con `adduser`

```bash

useradd -m -p "contraseña_segura" nuevo_usuario
```
- Explicación
  - adduser te pedirá una contraseña para el usuario y creará automáticamente el directorio de inicio, como un maestro Jedi que guía al nuevo usuario.
---
# ¿Cuándo Usar Cada Comando?


## Utiliza `useradd` cuando:

- Necesitas un control granular sobre la configuración de la cuenta del usuario, como un guerrero que afina su espada.

- Creas scripts automatizados para la creación masiva de usuarios, como un ejército de guerreros.

- La distribución de Linux no tiene disponible `adduser`, como un guerrero que se adapta a cualquier terreno.


## Utiliza `adduser` cuando:

- Prefieres una interfaz interactiva y amigable para la creación de usuarios, como un maestro Jedi que facilita el aprendizaje.

- Deseas aprovechar la configuración predeterminada para el directorio de inicio y otros parámetros, como un constructor que utiliza planos predefinidos.

- No necesitas especificar opciones de configuración complejas, como un guerrero que busca la simplicidad.


## Tabla Comparativa


|  Característica                     | `adduser`                                          | `useradd`                                                  | Ejemplo                                                 |

|------------------------------------|-----------------------------------------------------|------------------------------------------------------------|---------------------------------------------------------|

| Interactividad                     | Interactivo, solicita información detallada.        | No interactivo, requiere opciones manuales.                | `sudo adduser nuevo_usuario`                            |

| Facilidad de uso                   | Diseñado para ser más amigable y sencillo.          | Requiere conocimientos más avanzados.                      | `sudo useradd -m -s /bin/bash nuevo_usuario`            |

| Crea directorio de inicio          | Automáticamente crea el directorio home.            | Requiere la opción `-m` para crearlo.                      | `sudo adduser nuevo_usuario`                            |

| Shell predeterminada               | Utiliza la shell predeterminada del sistema.        | Requiere la especificación con `-s`.                       | `sudo useradd -m -s /bin/bash nuevo_usuario`            |

| Grupos adicionales                 | Ofrece opciones para agregar a grupos adicionales.  | Necesita comandos adicionales para esto.                   | `sudo adduser nuevo_usuario grupo_adicional`            |

| Configuración por defecto          | Configura valores por defecto automáticamente.      | Requiere especificación manual de opciones.                | `sudo useradd -m -s /bin/bash nuevo_usuario`            |

| Bloquea la cuenta                  | Puede bloquear una cuenta recién creada.            | No tiene opción directa para bloquear.                     | `sudo adduser --lock nuevo_usuario`                     |

| Mensaje de bienvenida              | Puede mostrar un mensaje de bienvenida.             | No proporciona directamente esta opción.                   | `sudo adduser --gecos "Bienvenido" nuevo_usuario`       |

| Mensajes de error                  | Ofrece mensajes de error más informativos.          | Las opciones incorrectas pueden ser menos descriptivas.    | `sudo adduser usuario_existente`                        |

| Auditoría de comandos              | Puede registrar la creación del usuario.            | Menos propenso a mantener registros automáticamente.       | No hay una opción directa para la auditoría.            |

| Uso de scripts                     | Apto para ser utilizado en scripts.                 | Menos adecuado para su uso en scripts.                     | Puede ser utilizado con precaución en scripts.          |  

| Comentarios en `/etc/passwd`       | Puede incluir comentarios en `/etc/passwd`.         | No permite comentarios en ese archivo.                     | `sudo adduser --gecos "Usuario de prueba" nuevo_usuario`|


Estos ejemplos te brindan una guía práctica sobre cómo utilizar los comandos `adduser` y `useradd` con diferentes opciones. Ten en cuenta que los ejemplos pueden variar según la distribución de Linux que estés utilizando.
---

---

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