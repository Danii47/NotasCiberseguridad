#BanditChallenge #SSH #PrivateKey
### Enunciado
La contraseña para el siguiente nivel se almacena en `/etc/bandit_pass/bandit14` y sólo puede ser leída por el usuario `bandit14`.Para este nivel, no obtienes la siguiente contraseña, pero obtienes una clave SSH privada que puede ser usada para iniciar sesión en el siguiente nivel.Nota: `localhost` es un nombre de host que se refiere a la máquina en la que estás trabajando.
### Solución
Te dan una clave privada para realizar la conexión SSH en el directorio `~/sshkey.private`.

Simplemente hay que saber que para realizar una conexión SSH con la clave privada se necesita usar el argumento `-i` seguido del archivo con la clave.

`ssh -p 2220 -i sshkey.private bandit14@bandit.labs.overthewire.org`

Y con eso estás dentro, ahora a miras el archivo del directorio que te dicen.

`cat /etc/bandit_pass/bandit14`

Y listo, tienes acceso a la contraseña.

`MU4VWeTyJk8ROof1qqmcBPaLh7lDCPvS`

[[Nivel 14 - Envío de mensajes a través de Telnet|Siguiente nivel]]