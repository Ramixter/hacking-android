Para configurar un servidor Apache debemos seguir diferentes pasos según el sistema operativo en el que te encuentres.

- [[#Linux (Debian/Ubuntu)]]
- [[#Linux (Red Hat/CentOS)]]
- [[#Windows]]
- [[#MacOS]]

---
## Linux (Debian/Ubuntu)

1. **Instala Apache**:
    Si Apache no está instalado, puedes instalarlo utilizando el siguiente comando:
	```shell
	sudo apt-get update sudo apt-get install apache2
	```

2. **Inicia Apache**:
    Después de la instalación, inicia Apache con el siguiente comando:
	```shell
	sudo systemctl start apache2
	```

3. **Habilita el servicio Apache para que se inicie automáticamente en el arranque**:
	```shell
	sudo systemctl enable apache2
	```

4. **Copia tus archivos al directorio de documentos web de Apache**:
    Los archivos que deseas compartir deben copiarse al directorio de documentos web de Apache. Por defecto, este directorio es `/var/www/html`. Utiliza el comando `cp` o `mv` para copiar o mover tus archivos a este directorio.
	```shell
	sudo cp /ruta/a/tu/carpeta /var/www/html/
	```
	o
	```shell
	sudo mv /ruta/a/tu/carpeta /var/www/html/
	```

5. **Accede a tu sitio web**:
    Puedes acceder a tus archivos compartidos en un navegador web ingresando la dirección IP de tu servidor o su nombre de dominio (si lo tienes) en la barra de direcciones.

## Linux (Red Hat/CentOS)

1. **Instala Apache**:
    Si Apache no está instalado, puedes instalarlo utilizando el siguiente comando:
	```shell
	sudo yum install httpd
	```

2. **Inicia Apache**:
    Después de la instalación, inicia Apache con el siguiente comando:
	```shell
	sudo systemctl start httpd
	```

3. **Habilita el servicio Apache para que se inicie automáticamente en el arranque**:
	```shell
	sudo systemctl enable httpd
	```

4. **Copia tus archivos al directorio de documentos web de Apache**:
    Los archivos que deseas compartir deben copiarse al directorio de documentos web de Apache. Por defecto, este directorio es `/var/www/html`. Utiliza el comando `cp` o `mv` para copiar o mover tus archivos a este directorio.
    ```shell
	sudo cp /ruta/a/tu/carpeta /var/www/html/
	```
	o
	```shell
	sudo mv /ruta/a/tu/carpeta /var/www/html/
	```

5. **Accede a tu sitio web**:
    Puedes acceder a tus archivos compartidos en un navegador web ingresando la dirección IP de tu servidor o su nombre de dominio (si lo tienes) en la barra de direcciones.

## Windows

1. **Instala Apache**:
    Descarga el instalador de Apache para Windows desde el sitio web oficial de Apache ([https://httpd.apache.org/download.cgi](https://httpd.apache.org/download.cgi)). Sigue las instrucciones del instalador para instalar Apache en tu sistema.

2. **Inicia Apache**:
    Abre el "Símbolo del sistema" como administrador y ejecuta el siguiente comando para iniciar Apache:
	```shell
	httpd -k start
	```

3. **Copia tus archivos al directorio de documentos web de Apache**:
    Los archivos que deseas compartir deben copiarse al directorio de documentos web de Apache. Por defecto, este directorio es `C:\Apache24\htdocs`. Utiliza el Explorador de archivos para copiar tus archivos a este directorio.

4. **Accede a tu sitio web**:
    Puedes acceder a tus archivos compartidos en un navegador web ingresando la dirección IP de tu servidor o su nombre de dominio (si lo tienes) en la barra de direcciones.
## MacOS

En macOS, Apache suele estar preinstalado y deshabilitado por defecto en versiones más recientes del sistema operativo. Para habilitarlo y configurarlo:

1. **Habilita Apache**:
    Abre la "Terminal" y ejecuta el siguiente comando para habilitar Apache:
	```shell
	sudo apachectl start
	```

2. **Copia tus archivos al directorio de documentos web de Apache**:
    Los archivos que deseas compartir deben copiarse al directorio de documentos web de Apache. Por defecto, este directorio es `/Library/WebServer/Documents`. Utiliza el comando `cp` o `mv` para copiar o mover tus archivos a este directorio.
    ```shell
	sudo cp /ruta/a/tu/carpeta /Library/WebServer/Documents/
	```
	o
	```shell
	sudo mv /ruta/a/tu/carpeta /Library/WebServer/Documents/
	```

3. **Accede a tu sitio web**:
    Puedes acceder a tus archivos compartidos en un navegador web ingresando la dirección IP de tu servidor o su nombre de dominio (si lo tienes) en la barra de direcciones.

---
## Notas

>Ten en cuenta que después de copiar los archivos al directorio de documentos web de Apache, estarán disponibles para su acceso a través de un navegador web en la dirección base del servidor. Puedes crear subdirectorios dentro del directorio de documentos web para organizar tus archivos según sea necesario.
