# Comandos Básicos de Linux 

Este documento proporciona una lista de comandos básicos de Linux que pueden ser útiles para principiantes y usuarios intermedios.

## 1. Gestión de Archivos (Comandos de Navegación)


- **`ls`**: Lista el contenido del directorio actual sin archivos ocultos.


- **`ls -l`**: Lista el contenido del directorio actual con archivos ocultos.


- **`cd`**: Cambia el directorio actual.

    - **`cd /etc`**: Ruta absoluta (con `/`).

    - **`cd etc`**: Ruta relativa (sin `/`).


- **`pwd`**: Muestra la ruta del directorio actual.


## 2. Comandos de Manipulación de Archivos y Directorios

### 2.1 Creación y Eliminación

4. **`mkdir`**: Crea un nuevo directorio.
    ```bash
    mkdir nombre_del_directorio
    ```

5. **`rmdir`**: Elimina un directorio vacío.
    ```bash
    rmdir nombre_del_directorio
    ```

6. **`rm`**: Elimina archivos o directorios.
    ```bash
    rm nombre_del_archivo
    rm -r nombre_del_directorio  # Para eliminar un directorio y su contenido
    ```

### 2.2 Copia y Movimiento

7. **`cp`**: Copia archivos o directorios.
    ```bash
    cp archivo_origen archivo_destino
    cp -r directorio_origen directorio_destino  # Para copiar un directorio y su contenido
    ```

8. **`mv`**: Mueve o renombra archivos o directorios.
    ```bash
    mv archivo_origen archivo_destino
    mv directorio_origen directorio_destino  # Para mover o renombrar un directorio
    ```

## 3. Comandos de Visualización y Edición de Archivos

9. **`cat`**: Muestra el contenido de un archivo.
    ```bash
    cat nombre_del_archivo
    ```

10. **`nano`** o **`vim`**: Editores de texto dentro de la terminal.
    ```bash
    nano nombre_del_archivo
    vim nombre_del_archivo
    ```

## 4. Comandos de Búsqueda y Filtros

11. **`grep`**: Busca texto dentro de archivos.
    ```bash
    grep "texto_a_buscar" nombre_del_archivo
    ```

12. **`find`**: Busca archivos y directorios.
    ```bash
    find /ruta/de/busqueda -name "nombre_del_archivo"
    ```

## 5. Comandos de Permisos y Propiedad

13. **`chmod`**: Cambia los permisos de archivos o directorios.
    ```bash
    chmod 755 nombre_del_archivo  # Permisos de lectura, escritura y ejecución para el propietario, y solo lectura y ejecución para el grupo y otros
    ```

14. **`chown`**: Cambia el propietario de archivos o directorios.
    ```bash
    chown nuevo_propietario nombre_del_archivo
    ```

## 6. Comandos de Compresión y Descompresión

15. **`tar`**: Comprime o descomprime archivos tar.
    ```bash
    tar -czvf archivo_comprimido.tar.gz directorio_o_archivo  # Para comprimir
    tar -xzvf archivo_comprimido.tar.gz  # Para descomprimir
    ```

16. **`gzip`**: Comprime archivos.
    ```bash
    gzip nombre_del_archivo
    ```

17. **`gunzip`**: Descomprime archivos comprimidos con gzip.
    ```bash
    gunzip nombre_del_archivo.gz
    ```

18. **`zip`**: Comprime archivos en un archivo zip.
    ```bash
    zip archivo.zip archivo1 archivo2
    ```

19. **`unzip`**: Descomprime archivos zip.
    ```bash
    unzip archivo.zip
    ```

## 7. Comandos de Información del Sistema

20. **`df`**: Muestra el uso del disco.
    ```bash
    df -h
    ```

21. **`top`**: Muestra los procesos en ejecución y el uso de recursos del sistema.
    ```bash
    top
    ```

22. **`uname`**: Muestra información sobre el sistema.
    ```bash
    uname -a
    ```

23. **`uptime`**: Muestra cuánto tiempo ha estado funcionando el sistema.
    ```bash
    uptime
    ```

24. **`dmesg`**: Muestra mensajes del búfer del anillo del kernel.
    ```bash
    dmesg
    ```

## 8. Comandos de Red

25. **`ping`**: Comprueba la conectividad con otro host de red.
    ```bash
    ping direccion_ip_o_hostname
    ```

26. **`ifconfig`**: Muestra o configura las interfaces de red (requiere permisos de superusuario).
    ```bash
    ifconfig
    ```

27. **`netstat`**: Muestra las conexiones de red, tablas de enrutamiento, estadísticas de interfaz, etc.
    ```bash
    netstat -a
    ```

28. **`scp`**: Copia archivos entre hosts en una red.
    ```bash
    scp archivo_origen usuario@servidor:directorio_destino
    ```

29. **`curl`**: Transfiere datos desde o hacia un servidor, utilizando uno de los soportes de los siguientes protocolos: HTTP, HTTPS, FTP, etc.
    ```bash
    curl http://ejemplo.com
    ```

30. **`wget`**: Descarga archivos de la web.
    ```bash
    wget http://ejemplo.com/archivo
    ```

## 9. Comandos de Procesos

31. **`ps`**: Muestra una instantánea de los procesos actuales.
    ```bash
    ps -aux
    ```

32. **`kill`**: Envía una señal a un proceso, generalmente para terminarlo.
    ```bash
    kill pid_del_proceso
    ```

33. **`killall`**: Mata todos los procesos con el nombre especificado.
    ```bash
    killall nombre_del_proceso
    ```

## 10. Comandos de Usuario

34. **`whoami`**: Muestra el nombre del usuario actual.
    ```bash
    whoami
    ```

35. **`sudo`**: Permite a un usuario ejecutar un comando como superusuario o como otro usuario.
    ```bash
    sudo comando
    ```

36. **`useradd`**: Crea un nuevo usuario (requiere permisos de superusuario).
    ```bash
    sudo useradd nombre_del_usuario
    ```

37. **`adduser`**: Crea un nuevo usuario de manera interactiva (requiere permisos de superusuario).
    ```bash
    sudo adduser nombre_del_usuario
    ```

38. **`passwd`**: Cambia la contraseña de un usuario.
    ```bash
    passwd nombre_del_usuario
    ```
    
