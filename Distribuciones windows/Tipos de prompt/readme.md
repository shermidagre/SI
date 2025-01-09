# Tipos de Prompt en Sistemas Operativos windows


Este documento describe los diferentes tipos de prompts que puedes encontrar en sistemas operativos basados en windows, así como en otros entornos de línea de comandos.


## 1. Prompt de Usuario Normal

**Descripción**: Este es el prompt que aparece cuando un usuario estándar inicia sesión en el sistema. Los usuarios normales tienen permisos limitados y no pueden realizar acciones que requieran privilegios de administrador.

**Ejemplo**:

   ```bash
    C:\Users\Usuario>
   ```


## 2. Prompt de Administrador

**Descripción**: Este prompt aparece cuando un usuario tiene acceso a la cuenta de administrador. El administrador tiene permisos completos para realizar cualquier acción en el sistema, incluyendo la modificación de archivos del sistema y la gestión de usuarios.

**Ejemplo**:

   ```bash
    C:\Windows\System32>  
   ```


## 3. Prompt de UAC (Control de Cuentas de Usuario)

**Descripción**: Cuando un usuario normal intenta ejecutar un comando que requiere privilegios de administrador, se puede mostrar un cuadro de diálogo de UAC que solicita confirmación. El prompt en sí no cambia, pero el usuario debe aceptar la elevación de privilegios.

**Ejemplo**:

   ```bash
    C:\Users\Usuario> runas /user:Administrador comando Introduce la contraseña para Administrador:
   ```


## 4. Prompt de PowerShell

**Descripción**: Este prompt aparece en una sesión de PowerShell, que es un entorno de línea de comandos más avanzado que el Command Prompt. Permite la ejecución de scripts y comandos más complejos.

**Ejemplo**:

   ```bash
    PS C:\Users\Usuario>   
   ``` 


## 5. Prompt de Script No Interactivo

**Descripción**: Este tipo de prompt se utiliza en scripts de PowerShell o Batch donde no se espera la interacción del usuario. Los comandos se ejecutan secuencialmente sin necesidad de entrada del usuario.


**Ejemplo**:

(No hay un "prompt" visible, ya que los comandos se ejecutan automáticamente).



## 6. Prompt de Errores

**Descripción**: Cuando un comando falla, el sistema puede mostrar un mensaje de error en el prompt, indicando que la acción no se pudo completar. Esto no es un tipo de prompt en sí, pero es importante para la interacción del usuario.


**Ejemplo**:

   ```bash
    C:\Users\Usuario> comando_inexistente 'comando_inexistente' no se reconoce como un comando interno o externo, programa o archivo por lotes ejecutable.
   ```


## 7. Prompt Personalizado

**Descripción**: Los usuarios pueden personalizar su prompt de PowerShell o Command Prompt para que muestre información adicional, como el directorio actual, el nombre de la máquina, el estado del repositorio de Git, etc. Esto se puede hacer modificando variables de entorno.


**Ejemplo**:

   ```bash
    [Usuario@Maquina C:\Proyecto]>   
   ```


## Resumen

Los diferentes tipos de prompt en Windows permiten a los usuarios interactuar con el sistema operativo de diversas maneras, desde tareas básicas hasta operaciones avanzadas que requieren permisos especiales. Familiarizarse con estos prompts puede mejorar la eficiencia y la efectividad al trabajar en entornos de línea de comandos.