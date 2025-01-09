# Tipos de Prompt en Sistemas Operativos Linux 


Este documento describe los diferentes tipos de prompts que puedes encontrar en sistemas operativos basados en Linux, así como en otros entornos de línea de comandos.


## 1. Prompt de Usuario Normal

- **Descripción**: Este es el prompt que aparece cuando un usuario estándar inicia sesión en el sistema. Los usuarios normales tienen permisos limitados y no pueden realizar acciones que requieran privilegios de superusuario.

- **Ejemplo**:

    ```bash
    usuario@maquina:~$
    ```



## 2. Prompt de Superusuario (Root)

- **Descripción**: Este prompt aparece cuando un usuario tiene acceso a la cuenta de superusuario (root). El superusuario tiene permisos completos para realizar cualquier acción en el sistema, incluyendo la modificación de archivos del sistema y la gestión de usuarios.

- **Ejemplo**:

    ```bash
    root@maquina:~#
    ```



## 3. Prompt de Sudo

- **Descripción**: Cuando un usuario normal utiliza el comando `sudo` para ejecutar un comando con privilegios de superusuario, el prompt puede cambiar temporalmente para indicar que se están utilizando permisos elevados. Sin embargo, el prompt en sí no cambia, pero el usuario puede ser solicitado a ingresar su contraseña.

- **Ejemplo**:

    ```bash
    usuario@maquina:~$ sudo comando [sudo] contraseña para usuario:
    ```

## 4. Prompt de Shell Interactiva

- **Descripción**: Este prompt aparece en una sesión de shell interactiva, donde el usuario puede ingresar comandos y recibir respuestas en tiempo real. Puede ser un prompt de Bash, Zsh, Fish, entre otros.

- **Ejemplo**:

    ```bash
    usuario@maquina:~$
    ``` 

## 5. Prompt de Shell No Interactiva

- **Descripción**: Este tipo de prompt se utiliza en scripts o en situaciones donde no se espera la interacción del usuario. Los comandos se ejecutan secuencialmente sin necesidad de entrada del usuario.

- **Ejemplo**:

No hay un "prompt" visible, ya que los comandos se ejecutan automáticamente.


## 6. Prompt de Errores

- **Descripción**: Cuando un comando falla, el sistema puede mostrar un mensaje de error en el prompt, indicando que la acción no se pudo completar. Esto no es un tipo de prompt en sí, pero es importante para la interacción del usuario.

- **Ejemplo**:

    ```bash
    usuario@maquina:~$ comando_inexistente bash: comando_inexistente: no se encontró la orden

    ```


## 7. Prompt Personalizado

- **Descripción**: Los usuarios pueden personalizar su prompt de shell para que muestre información adicional, como el directorio actual, el nombre de la máquina, el estado del repositorio de Git, etc. Esto se puede hacer modificando variables de entorno como `PS1` en Bash.

- **Ejemplo**:

    ```bash
    [usuario@maquina ~/proyecto]$
    ```


## Resumen

Cada tipo de prompt tiene su propio propósito y contexto de uso. La distinción entre ellos es importante para entender los niveles de acceso y las capacidades del usuario en un sistema operativo.