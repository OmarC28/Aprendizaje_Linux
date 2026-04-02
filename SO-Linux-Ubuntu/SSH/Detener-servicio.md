# 📗 Detener el servicio SSH Temporalmente

#### 📘 Esto apaga SSH hasta el Siguiente Reinicio de la PC.

    sudo systemctl stop ssh

> Este script detendra el servidor inmediatamente y nadie podra conectarse mientra este detenido.

# 📗 Desactivar SSh Permanentemente

#### 📘 Esto desacativa el SSH en arranque automatico al prender la PC.

    sudo systemctl disable ssh

> Este script hara que se descative el arranque automatico del servicio y para activarlo nesecitas poner un scrip de activacion en la terminal.

# 📗 Activacion de los servicios en cada caso.

#### 📘 En cada caso tendras scripts para activarlos primero en orden si encaso de desactiva el SSH.

    sudo systemctl enbale ssh

    sudo systemctl start ssh

#### 📘 Por ultimo verificas siempre el estatus que tiene el servicio de SSH.

    sudo systemctl status ssh

> con todo estos scripts verificaras, activaras y desactivaras los servicios de SSH servidor de la pc donde se instalo.

