# 📗 Conexion de SSH
#### 📘 Tenemos que saber la IP de la maquina para la conexion. Con el comando de:

📜

ip a

> Sirve para saber la ip e informacion de ip local de la maquina
> *Importante hay otras formas para saber la ip pero se necesita instalar algunos paquetes*
> 
> 📜
>
> sudo apt install net-tools
>
> Sirve para instalar paquetes de uso de comandos clasicos *ifconfig*

#### Recuerda que saber la ip es solo para verificar que estemos en la misma Red localmente ya que otras maquinas se podran conectar a la terminal donde se instalo los paquetes del servidor de ssh.

#### 📒 Terminado esto ya podras conectarte desde otra maquina poniendo en la terminal o Powersell (Caso Windows):

📜

ssh tu_usuario@IP_de_la_pc

ssh tu_usuario@Nombre_de_la_PC

> 📒🎄 Son dos formas para que puedas conectarte conociendo la IP de la maquina o el nombre especifico que se le puso al equipo.
> Recuerda que don de se instalo el SSH sirve como servidor (openssh-server) y las maquinas que se quieran conectar seran como Cliente y no es necesario instalar paquetes importantes.






