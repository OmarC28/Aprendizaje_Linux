# 📗 Que es la Clave SSH
###  📘 En SSH usas las claves privadas y publicas.

🔑 Clave Privada: Se queda en otra masquinas donde quieras conectarte(No se comparte)
 
🔓 Clave Publica: Se copia a la PC del Servidor SSH (La maquina a la que quieras acceder)
 
> El servidor verificara tu clave y si coincide entraras sin contraseña.

### 📘 Creacion de claves SSH (En la  PC cliente) (por buenas practicas)

## 📕 Powersheel

No es necesario entrar como administrador

    ssh-keygen -t ed25519 -C "mi_llave_ssh"

> Puedes poner " " cualquier nombre representativo
> 
> -t = *Tipo de llave*
> 
> ed25519 = *Algoritmo para creacion de llaves (Moderno)*
>
> -C = *Comentario* 

Hay algoritmos de llaves que se usa como *dsa* (Antiguo obsoleto), *rsa* (compatible antiguo), *ecdsa* (bueno poco usado) y *ed25519* (moderno y usado)

🟢 Generara la llave tipo ed25519 confirmas el archivo creado (Enter)

🟡 Te pedira si quieres generar una contraseña *passphrase*  (Es una contraseña extra para las llaves)

> Digitas tu contraseña o lo dejas en blanco presionando enter
> 
> Recuerda que si no digitas una contraseña la Llave qe crearas sera vulnerable y podran entrar al servidor

🟢 En la creacion de la llave  te dara dos tipos de archivo uno normal y el otro con *.pub* ese sera la llave publica

### 📘 Llevar la clave publica al servidor 

## 📕 Powersheel

    ssh-copy-id usuario@IP_DEL_SERVIDOR

> El usuario e ip del servidor debes de tenerlo.

### 🧧🧧 Si en caso sale error es por que en powersheel no esta soportado para copiar como en la terminal de linux, en todo caso tendras que buscar el archivo donde se creo

    type $env:USERPROFILE\.ssh\id_ed25519.pub

> Te saldra la llave ssh-ed25519 aaa..... "Mi_llave_ssh" (el nombre que le pusistes)

En este punto lo haremos manual el copiado de la llave publica.

#### 📘 Entramos a la terminal del servidor:

    ssh usuario@IP_DEL_SERVIDOR

Crearemos una carpeta con:

    mkdir -p ~/.ssh

> -p = Crea rutas completas si no existe, es decir la carpeta .ssh si no existe, la crea.
>
> ~ = la Ruta en la Carpeta Personal (home)

Luego le crearemos permisos a esa carpeta que solo el dueño(Usuario administrador) pueda configurar.

    chmod 700 ~/.ssh

> esto hace que la carpeta tenga perimdo en todo
>
> 700 = rwx (4= lectura(r) + 2=escritura(w) + 1= ejecucion(x)) para el dueño, 0 = grupo, 0 = otros

Luego crearemos y modificaremos un archivo con el script de "nano" el archivo creado se llamara 
 
    nano ~/.ssh/authorized_keys

> no olvidar poner toda la ruta, el archivo que se creo es "authorized_keys"

Ahora dentro de ese archivo se copia la llave publica que se creo

> doble click derecho para pegar, recuerda que es la terminal de linux y es diferente al de windows de powersheel.
>
> ctrl + x, Para salir del archivo.

Hasta lo ultimo que nos queda es ponerle permiso alrchivo 

    chmod 600 ~/.ssh

> Archivo con permisos solo para lectura y escritura no Ejecutable

    exit

#### 📒🎄 Por ultimo se sale ya podras probar el inicio de sesion ssh sin clave


 
