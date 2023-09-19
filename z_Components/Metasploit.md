## Introducción: Descubriendo Metasploit

Bienvenidos a la guía completa de **Metasploit** para principiantes. En este viaje, exploraremos una de las herramientas más potentes y versátiles en el mundo de la ciberseguridad y el hacking ético. **Metasploit**, desarrollado por Rapid7, es una suite de software de código abierto que te permite llevar a cabo pruebas de penetración y evaluar la seguridad de sistemas informáticos de manera ética.

Es importante destacar que esta guía tiene un enfoque firme en la ética y la legalidad en el uso de Metasploit. Antes de embarcarte en este viaje de descubrimiento, es fundamental comprender que el objetivo principal de **Metasploit** es fortalecer la seguridad de los sistemas, no comprometerla.

### Advertencia Ética:

- **Metasploit** debe utilizarse únicamente con permiso explícito y autorización legal para evaluar y mejorar la seguridad de sistemas y redes.
- Cualquier uso no autorizado o ilegal de **Metasploit** es estrictamente condenable y puede tener graves consecuencias legales.

### ¿Quién Debería Leer Esta Guía?

Esta guía está diseñada para personas que nunca han utilizado **Metasploit** y desean comprender su funcionamiento desde cero. No se requieren conocimientos previos en hacking o ciberseguridad, pero se recomienda tener una comprensión básica de redes y sistemas operativos.

### Estructura de la Guía:

A lo largo de esta guía, te llevaré paso a paso a través del proceso de instalación, uso y mejores prácticas de **Metasploit**. Aprenderás cómo llevar a cabo pruebas de penetración de manera ética y segura, explorando sus capacidades de reconocimiento, explotación, escalación de privilegios y más.

Te animo a leer con atención, practicar de manera responsable y siempre mantener la ética y la legalidad en mente mientras te sumerges en el fascinante mundo de **Metasploit**.

¡Comencemos nuestro viaje hacia el conocimiento de Metasploit!




>Nota importante: Metasploit es una herramienta de seguridad que se utiliza con fines legítimos, como pruebas de penetración y auditorías de seguridad. Utilizar Metasploit para actividades ilegales o sin autorización puede tener graves consecuencias legales. Asegúrate de tener permiso para usar Metasploit antes de instalarlo y utilizarlo.
## Instalar Metasploit

### Ubuntu

1. Abre una terminal en tu sistema Ubuntu.

2. Asegúrate de que tu sistema esté actualizado ejecutando los siguientes comandos:

	```bash
	sudo apt update
	sudo apt upgrade
	```

3. Instala las dependencias necesarias ejecutando el siguiente comando:

	```bash
	sudo apt install curl gpg
	```

4. Importa la clave GPG de Rapid7, que es el equipo detrás de **Metasploit**, ejecutando el siguiente comando:

	```bash
	curl https://apt.metasploit.com/metasploit-framework.gpg.key | sudo gpg --dearmor -o /usr/share/keyrings/metasploit-archive-keyring.gpg
	```

5. Agrega el repositorio de **Metasploit** a tu sistema ejecutando el siguiente comando:

	```bash
	echo "deb [signed-by=/usr/share/keyrings/metasploit-archive-keyring.gpg] https://apt.metasploit.com/ jessie main" | sudo tee /etc/apt/sources.list.d/metasploit-framework.list
	```

	Este comando agrega el repositorio de Metasploit a tu lista de fuentes de paquetes.

6. Actualiza la información de los paquetes ejecutando:

	```bash
	sudo apt update
	```

7. Finalmente, instala **Metasploit Framework** con el siguiente comando:

	```bash
	sudo apt install metasploit-framework
	```

8. Una vez que se complete la instalación, puedes iniciar **Metasploit** ejecutando:

	```bash
	msfconsole
	```

	Esto abrirá la interfaz de **Metasploit Framework** en la terminal.

### Arch Linux

1. Abre una terminal en tu sistema Arch Linux.

2.  Asegúrate de que tu sistema esté actualizado ejecutando los siguientes comandos:

	```bash
	sudo pacman -Syu
	```

3. Instala `yay` si aún no lo tienes instalado. Puedes hacerlo siguiendo las instrucciones en el sitio web oficial de `yay`: [https://github.com/Jguer/yay](https://github.com/Jguer/yay)

`````ad-info
title: Instalar `yay`
collapse: close

1. Abre una terminal en tu sistema Arch Linux o Manjaro.

2. Verifica si `yay` ya está instalado en tu sistema ejecutando el siguiente comando:

	```bash
	yay --version
	```

	Si obtienes una salida que muestra la versión de `yay`, significa que ya está instalado. Puedes continuar con el paso 4 de la respuesta anterior para instalar Metasploit.

3. Si `yay` no está instalado, puedes instalarlo de la siguiente manera:

	1. Descarga el archivo PKGBUILD y los archivos relacionados de `yay` desde el AUR ejecutando el siguiente comando:

		```bash
		git clone https://aur.archlinux.org/yay.git
		```

	2. Navega al directorio `yay` recién creado:

		```bash
		cd yay
		```

	3. Compila e instala `yay` usando `makepkg`:

		```bash
		makepkg -si
		```

		Este comando descargará las dependencias necesarias, compilará `yay` y luego lo instalará en tu sistema.
`````

4. Una vez que `yay` esté instalado, puedes instalar **Metasploit Framework** ejecutando el siguiente comando:

	```bash
	yay -S metasploit
	```

	`yay` buscará **Metasploit** en el repositorio AUR y te pedirá confirmación antes de instalarlo.

5. Durante la instalación, `yay` descargará y compilará **Metasploit** y sus dependencias desde el AUR.

6. Una vez que la instalación esté completa, puedes iniciar **Metasploit** ejecutando:

	```bash
	msfconsole
	```

	Esto abrirá la interfaz de **Metasploit Framework** en la terminal.

## Uso de Metasploit

### Módulos

Para listar todos los módulos disponibles en **Metasploit Framework**, puedes utilizar el comando `search` con un término de búsqueda amplio, como un asterisco (\*), que coincidirá con todos los módulos disponibles. Sigue estos pasos:

1. Abre una terminal en la que **Metasploit Framework** esté instalado.

2. Inicia la interfaz de Metasploit Framework ejecutando el siguiente comando:

	```bash
	msfconsole
	```

3. Una vez dentro de msfconsole, utiliza el comando `search` con un asterisco (\*) como término de búsqueda para listar todos los módulos disponibles:

```bash
search *
```

4. 
5. Esto buscará y mostrará una lista completa de todos los módulos disponibles en Metasploit Framework.
