# 📗 Instalacion de SSH
#### 📘 Vamos a la terminal y ponemos:

📜 

Sudo apt install openssh-server -y

>  es para instalar paquetes de uso SSH a la maquina

####  Luego verificamos si todo esta bien debe de decir que el SSH este Active (running)

📜 

sudo systemctl status ssh

>Verificamos Active (running)

##### 🧧🧧 Se verifica que esta instalado pero se observa que no esta activado, para ello debemos de activarlo. (END) para Salir devemos de presiona la letra ´q´ y volvemos al terminal de comandos.

📜

sudo systemctl enable ssh

sudo systemctl start ssh

> Es para que active los paquetes del SSH si en caso no se pudo inicialmente

##### 🎄 Se soluciono el problema (END) y se activo correctamente el SSH *Active (running)*

