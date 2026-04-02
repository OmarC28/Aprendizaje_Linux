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
> -t = Tipo de llave
> 
> ed25519 = Algoritmo para creacion de llaves (Moderno)
>
> rsa = 
>
> -C 
