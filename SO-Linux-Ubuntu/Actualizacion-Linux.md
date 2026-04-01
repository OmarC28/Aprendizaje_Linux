# 📗 Instalacion de Linux Ubuntu

### 📘 Descargar ISO y bootearlo en Rufus 

# 📗 Actualiza el Sistema de Linux en la Terminal
## Terminal
📜

Sudo apt update 

> Descarga paquetes de actualización buscando en servidores de software (Solo es una revisión si falta una versión más nueva)

📜

Sudo apt upgrade -y 

> Comando donde realmente instala y actualiza, Parámetro (-y) que da la consigna de aceptar las actualizaciones e instalaciones.

### 🧧🧧 Se actualizo e instalo correctamente los paquetes, pero ahora tengo otro problema cuando inicia no corre automaticamente.

# 📗 Solucionando Problemas de Arranque al esperar (GRUB)

### 📘 Configuracion para Arranque Automatico

### 📘 Entraremos al Bash donde esta el script del Arranque y configuraremos

## 📕 Bash:
📜

sudo nano /etc/default/grub

> Buscaremos El TIMEOUT y configuraremos de 20 segundos que estaba a 1s

📜

GRUB_TIMEOUT=1
GRUB_TIMEOUT_STYLE=hidden      
GRUB_DEFAULT=0

> el hidden significa oculto hara que no se vea el menu 

> ahora ^o para guardar los cambios o ^x para salir y afuera pondremos

📜

sudo update-grub

> Hara que se actualice lo que hemos hecho 

📜

sudo reboot

> Para reniiciar la pc desde la terminal

### 🧧🧧Solucionado el problema de arranque ahora hay otro problema lo que es ocultar el GRUB

### 📘 Entraremos al Bash donde esta el script del Arranque y configuraremos

## 📕 Bash:

📜

sudo nano /etc/default/grub

> escribiremos lo que es una linea mas para forzar el ocultar el Menu 

📜

GRUB_TIMEOUT=0

GRUB_TIMEOUT_STYLE=hidden

GRUB_DEFAULT=0

GRUB_DISABLE_OS_PROBER=true 

> Es para que el menu se oculte forzadamente

##### 🎄Solucionado el problema de arranque y ocultar el menu de GRUB de linux

##### 📒📒 Apartir de Aca ya esta listo para que se haga laboratorios y navegar por todo linux 


