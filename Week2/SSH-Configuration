**Read this in other languages**

- [Español](#configuración-de-ssh)
- [English](#ssh-configuration)


# Configuración de SSH

## 1. Autenticación por claves SSH

En la Semana 1, cuando tratamos de conectarnos al servidor, utilizamos la contraseña del usuario registrado en el mismo, lo cual no es una práctica recomendable por varios motivos. Sin embargo, el que más nos llama la atención es que las contraseñas suelen ser débiles, se pueden adivinar, filtrar o romper con fuerza bruta.

El protocolo **Secure Shell (SSH)**, nos brinda una herramienta que nos ayuda a mejorar la seguridad de la conexión al servidor, permitiendo el uso de claves en lugar de contraseñas.

Las claves SSH son criptográficas y  mucho más complejas que cualquier contraseña común. Tanto es así que romper una clave **ed25519** de 256 bits es prácticamente imposible con la tecnología actual.

Una clave **ed25519** es un tipo de clave criptográfica utilizada en SSH basada en curvas elípticas. Permite autenticarse de forma segura sin usar contraseñas, ofreciendo alta seguridad con claves más cortas, rapidez en la verificación y resistencia a ataques como la fuerza bruta. Se compone de una clave privada (que se guarda en el pc y no se comparte) y una pública (que se sube al servidor) para validar la identidad.

Para configurar las claves ssh ejecutamos los siguientes pasos:

### Paso 1: Generar claves SSH en el cliente

Desde PowerShell ejecuta:

```bash
ssh-keygen -t ed25519 -C "usuario@email.com"
```

Este comando genera un par de claves SSH, una privada y una pública, incluimos el correo electrónico con la finalidad de identificar de quien es la clave, por si se tienen varias.

### Paso 2: Copiar la clave pública al servidor

Ejecutamos dir 
```bash
C:\Users\nombre-de-usuario\.ssh
```
Esto mostrará los archivos de la carpeta '.ssh'. Verifica que exista el archivo 'id_ed25519'.pub, que corresponde a la clave pública.

Luego, para visualizar el contenido de la clave pública:

```bash
type C:\Users\nombre-usuario\.ssh\id_ed25519.pub
```
Copia el resultado.

Después, desde PowerShell ingresa al servidor como normalmente lo hacías con contraseña y crea el directorio .ssh si no existe y el archivo **authorized_keys**:

```bash
mkdir -p ~/.ssh
chmod 700 ~/.ssh
```

Creación de archivo:

```bash
nano ~/.ssh/authorized_keys
```

Pega dentro de este archivo el contenido de la clave pública copiada desde Windows.

Por último, ajusta los permisos y sal del servidor:

```bash
chmod 600 ~/.ssh/authorized_keys
exit
```

### Paso 3: Probar conexión sin contraseña

Como ya compartimos con el servidor la clave pública generada en el cliente, al intentar conectarnos el servidor verificará automáticamente si la clave privada coincide con la clave pública guardada en `authorized_keys`.  

Si coinciden, la conexión será autorizada sin necesidad de ingresar contraseña.  

Para probarlo, ejecuta:

```bash
ssh usuario@ip-del-servidor
```

![Conexión sin contraseña](../Week2/Pictures/Conecction-without-Password.png)

### Paso 4: Endurecer la seguridad en sshd_config

Como buena práctica de seguridad, debemos editar la configuración de SSH para aceptar solo la autenticación por claves y evitar accesos inseguros.

Edita el archivo de configuración:

```bash
sudo nano /etc/ssh/sshd_config
```

Asegúrate de que las siguientes líneas estén configuradas de esta forma:

```bash

PubkeyAuthentication yes
PasswordAuthentication no
PermitRootLogin no
```
**Nota**: Con estas opciones, solo será posible acceder con claves SSH y no con contraseñas. Además, se bloquea el acceso directo como root.

Luego reinicia el servicio para aplicar cambios:

```bash
sudo systemctl restart ssh
```

![Configurando archivo sshd_config](../Week2/Pictures/Edit-sshd-config.png)

Con estos pasos habrás configurado la autenticación por claves ssh de forma segura y aplicando buenas practicas que refuerzan la seguridad del servidor.

# SSH Configuration