# Comandos Básicos de Windows


Este documento proporciona una lista de comandos básicos de Windows que pueden ser útiles para principiantes y usuarios intermedios.


## 1. Gestión de Archivos (Comandos de Navegación)


- **`dir`**: Lista el contenido del directorio actual.



- **`cd`**: Cambia el directorio actual.

    - **`cd C:\ruta\al\directorio`**: Ruta absoluta.

    - **`cd directorio`**: Ruta relativa.


- **`chdir`**: Sinónimo de `cd`, cambia el directorio actual.


- **`echo %cd%`**: Muestra la ruta del directorio actual.


## 2. Comandos de Manipulación de Archivos y Directorios


### 2.1 Creación y Eliminación


- **`mkdir`**: Crea un nuevo directorio.

    ```cmd

    mkdir nombre_del_directorio

    ```


- **`rmdir`**: Elimina un directorio vacío.

    ```cmd

    rmdir nombre_del_directorio

    ```


- **`del`**: Elimina archivos.

    ```cmd

    del nombre_del_archivo

    ```


- **`rd`**: Elimina un directorio y su contenido.

    ```cmd

    rd /s nombre_del_directorio

    ```


### 2.2 Copia y Movimiento


- **`copy`**: Copia archivos.

    ```cmd

    copy archivo_origen archivo_destino

    ```


- **`xcopy`**: Copia archivos y directorios.

    ```cmd

    xcopy directorio_origen directorio_destino /E /I  # Para copiar un directorio y su contenido

    ```


- **`move`**: Mueve o renombra archivos o directorios.

    ```cmd

    move archivo_origen archivo_destino

    ```


## 3. Comandos de Visualización y Edición de Archivos


- **`type`**: Muestra el contenido de un archivo.

    ```cmd

    type nombre_del_archivo

    ```


- **`notepad`**: Abre el Bloc de notas para editar archivos.

    ```cmd

    notepad nombre_del_archivo

    ```


## 4. Comandos de Búsqueda y Filtros


- **`findstr`**: Busca texto dentro de archivos.

    ```cmd

    findstr "texto_a_buscar" nombre_del_archivo

    ```


- **`dir /s`**: Busca archivos y directorios en el sistema.

    ```cmd

    dir /s nombre_del_archivo

    ```


## 5. Comandos de Permisos y Propiedad


- **`icacls`**: Muestra o modifica los permisos de archivos y directorios.

    ```cmd

    icacls nombre_del_archivo

    ```


- **`takeown`**: Toma posesión de un archivo o directorio.

    ```cmd

    takeown /f nombre_del_archivo

    ```


## 6. Comandos de Compresión y Descompresión


- **`compact`**: Muestra o cambia el estado de compresión de archivos en NTFS.

    ```cmd

    compact /c nombre_del_archivo  # Para comprimir

    compact /u nombre_del_archivo  # Para descomprimir

    ```


## 7. Comandos de Información del Sistema


- **`systeminfo`**: Muestra información sobre el sistema.



- **`tasklist`**: Muestra los procesos en ejecución.


- **`taskkill`**: Termina un proceso.

    ```cmd

    taskkill /PID pid_del_proceso

    ```


- **`hostname`**: Muestra el nombre del equipo.


## 8. Comandos de Red


- **`ping`**: Comprueba la conectividad con otro host de red.

    ```cmd

    ping direccion_ip_o_hostname

    ```


- **`ipconfig`**: Muestra la configuración de red.



- **`netstat`**: Muestra las conexiones de red y estadísticas.

    ```cmd

    netstat -a

    ```


- **`tracert`**: Muestra la ruta que toma un paquete para llegar a un host.

    ```cmd

    tracert direccion_ip_o_hostname

    ```


## 9. Comandos de Procesos


- **`tasklist`**: Muestra una lista de los procesos en ejecución, incluyendo el nombre del proceso, el ID del proceso (PID) y el uso de memoria.

    ```cmd

    tasklist

    ```


- **`taskkill`**: Termina un proceso específico utilizando su ID de proceso (PID) o su nombre. Este comando requiere permisos de administrador para algunos procesos.

    ```cmd

    taskkill /PID pid_del_proceso  # Termina un proceso por su PID

    taskkill /IM nombre_del_proceso.exe  # Termina un proceso por su nombre

    ```


- **`start`**: Inicia un nuevo proceso o programa en una nueva ventana.

    ```cmd

    start nombre_del_programa

    ```


- **`wmic process`**: Proporciona información detallada sobre los procesos en ejecución y permite realizar acciones sobre ellos.

    ```cmd

    wmic process list brief  # Muestra una lista breve de procesos

    ```


- **`pause`**: Pausa la ejecución de un script o comando hasta que el usuario presione una tecla.

    ```cmd

    pause

    ```

## 10. Comandos de Usuario


- **`whoami`**: Muestra el nombre del usuario actual que ha iniciado sesión en el sistema.

    ```cmd

    whoami

    ```


- **`net user`**: Muestra la lista de usuarios en el sistema, incluyendo información básica sobre cada uno.

    ```cmd

    net user

    ```


- **`net user nombre_del_usuario`**: Muestra información detallada sobre un usuario específico, incluyendo su estado y grupos a los que pertenece.

    ```cmd

    net user nombre_del_usuario

    ```


- **`net localgroup`**: Muestra los grupos locales en el sistema, permitiendo ver qué grupos están disponibles.

    ```cmd

    net localgroup

    ```


- **`net user nombre_del_usuario /add`**: Crea un nuevo usuario en el sistema. Asegúrate de tener permisos de administrador para ejecutar este comando.

    ```cmd

    net user nombre_del_usuario /add

    ```


- **`net user nombre_del_usuario *`**: Cambia la contraseña de un usuario. Se te pedirá que ingreses la nueva contraseña.

    ```cmd

    net user nombre_del_usuario *

    ```


- **`net user nombre_del_usuario /delete`**: Elimina un usuario del sistema. Este comando también requiere permisos de administrador.

    ```cmd

    net user nombre_del_usuario /delete

    ```


- **`net localgroup nombre_del_grupo nombre_del_usuario /add`**: Agrega un usuario a un grupo local específico.

    ```cmd

    net localgroup nombre_del_grupo nombre_del_usuario /add

    ```


- **`net localgroup nombre_del_grupo nombre_del_usuario /delete`**: Elimina un usuario de un grupo local específico.

    ```cmd

    net localgroup nombre_del_grupo nombre_del_usuario /delete

    ```