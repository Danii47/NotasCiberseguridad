#BanditChallenge #SSH #SCP
### Enunciado
La contraseña para el siguiente nivel se almacena en un archivo readme en el homedirectory. Desafortunadamente, alguien ha modificado .bashrc para cerrar la sesión cuando te conectas con SSH.
### Solución
Para este ejercicio se ve la utilidad del archivo `.bashrc`, que es un archivo que se ejecuta cada vez que se abre una sesión interactiva de la terminal. Esto hace que al conectarnos instantáneamente nos expulse de la sesión.

Una posible solución al ejercicio es tener el conocimiento de que el comando `ssh` permite la ejecución de comandos en la maquina destino, así que se podría abrir una terminal **no** interactiva llamando a `/bin/bash`.

`ssh bandit18@bandit.labs.overthewire.org -p 2220 /bin/bash`

Y ya simplemente obtenemos el archivo `readme`. Se podría haber ejecutado el comando `cat readme` también.

O incluso, se podría haber usado el comando `scp`.

`scp -P 2220 bandit18@bandit.labs.overthewire.org:~/readme .`

Para coger el archivo.

Usando cualquiera de esas soluciones, obtenemos la contraseña.

`cGWpMaKXVwDUNgPAVJbWYuGHVn9zl3j8`

[[Nivel 19 - Archivo setuid|Siguiente nivel]]