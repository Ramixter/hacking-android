Aquí tenemos las instrucciones para levantar un servidor web simple utilizando el módulo `http.server` de Python. Este servidor web es adecuado para propósitos de desarrollo o para compartir archivos localmente.

- [[#Linux (Debian/Ubuntu)]]
- [[#Linux (Red Hat/CentOS)]]
- [[#Windows]]
- [[#MacOS]]

---
## Linux (Debian/Ubuntu)

1. **Abre una terminal**:
	Abre una terminal en tu sistema Debian o Ubuntu.

2. **Navega al directorio que contiene la carpeta que deseas compartir**:
    Utiliza el comando `cd` para navegar al directorio que contiene los archivos que deseas compartir. Por ejemplo:
    ```shell
    cd /ruta/a/tu/carpeta
	```

3. **Inicia el servidor web**:
    Ejecuta el siguiente comando para iniciar el servidor web en un puerto específico (reemplaza `<PUERTO>` con el número de puerto que desees utilizar, como 8080):
    ```shell
    python3 -m http.server <PUERTO>
	```
    Por ejemplo, para usar el puerto 8080:
    ```shell
    python3 -m http.server 8080
	```

4. **Acceder al servidor web**:
	 Una vez que el servidor esté en funcionamiento, podrás acceder a él desde un navegador web ingresando la dirección `http://localhost:http://localhost:<PUERTO>` en la barra de direcciones del navegador. Esto te permitirá ver y descargar los archivos en la carpeta que estás compartiendo a través del servidor web.
## Linux  (Red Hat/CentOS)

1. **Abre una terminal**:
    Abre una terminal en tu sistema Red Hat o CentOS.
    
2. **Navega al directorio que contiene la carpeta que deseas compartir**:
    Utiliza el comando `cd` para navegar al directorio que contiene los archivos que deseas compartir. Por ejemplo:
    ```shell
    cd /ruta/a/tu/carpeta
	```

3. **Inicia el servidor web**:
    Ejecuta el siguiente comando para iniciar el servidor web en un puerto específico (reemplaza `<PUERTO>` con el número de puerto que desees utilizar, como 8080):
    ```shell
    python3 -m http.server <PUERTO>
	```
    Por ejemplo, para usar el puerto 8080:
    ```shell
    python3 -m http.server 8080
	```

4. **Acceder al servidor web**:
	 Una vez que el servidor esté en funcionamiento, podrás acceder a él desde un navegador web ingresando la dirección `http://localhost:http://localhost:<PUERTO>` en la barra de direcciones del navegador. Esto te permitirá ver y descargar los archivos en la carpeta que estás compartiendo a través del servidor web.
## Windows

1. **Abre el "Símbolo del sistema"**:
    Presiona `Win` + `S` para abrir la barra de búsqueda, escribe "cmd", y selecciona "Símbolo del sistema" o "Command Prompt" cuando aparezca en los resultados.
    
2. **Navega al directorio que contiene la carpeta que deseas compartir**:
    Utiliza el comando `cd` para navegar al directorio que contiene los archivos que deseas compartir. Por ejemplo:
    ```shell
    cd C:\ruta\a\tu\carpeta
	```

3. **Inicia el servidor web**:
    Ejecuta el siguiente comando para iniciar el servidor web en un puerto específico (reemplaza `<PUERTO>` con el número de puerto que desees utilizar, como 8080):
    ```shell
    python -m http.server <PUERTO>
	```
    Por ejemplo, para usar el puerto 8080:
    ```shell
    python -m http.server 8080
	```

4. **Acceder al servidor web**:
	 Una vez que el servidor esté en funcionamiento, podrás acceder a él desde un navegador web ingresando la dirección `http://localhost:http://localhost:<PUERTO>` en la barra de direcciones del navegador. Esto te permitirá ver y descargar los archivos en la carpeta que estás compartiendo a través del servidor web.
## MacOS

1. **Abre la "Terminal"**:
    Abre la aplicación "Terminal" en tu Mac.

2. **Navega al directorio que contiene la carpeta que deseas compartir**:
    Utiliza el comando `cd` para navegar al directorio que contiene los archivos que deseas compartir. Por ejemplo:
    ```shell
    cd /ruta/a/tu/carpeta
	```

3. **Inicia el servidor web**:
    Ejecuta el siguiente comando para iniciar el servidor web en un puerto específico (reemplaza `<PUERTO>` con el número de puerto que desees utilizar, como 8080):
    ```shell
    python3 -m http.server <PUERTO>
	```
    Por ejemplo, para usar el puerto 8080:
    ```shell
    python3 -m http.server 8080
	```

4. **Acceder al servidor web**:
	 Una vez que el servidor esté en funcionamiento, podrás acceder a él desde un navegador web ingresando la dirección `http://localhost:http://localhost:<PUERTO>` en la barra de direcciones del navegador. Esto te permitirá ver y descargar los archivos en la carpeta que estás compartiendo a través del servidor web.




