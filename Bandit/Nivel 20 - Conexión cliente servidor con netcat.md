#BanditChallenge #setuid #Netcat 
### Enunciado
Hay un binario `setuid` en el `homedirectory` que hace lo siguiente: establece una conexión con `localhost` en el puerto que especifiques como argumento en la línea de comandos. Luego lee una línea de texto de la conexión y la compara con la contraseña del nivel anterior (`bandit20`). Si la contraseña es correcta, transmitirá la contraseña para el siguiente nivel (`bandit21`).

**NOTA:** Prueba a conectarte a tu propio `daemon` de red para ver si funciona como crees
### Solución
En este ejercicio nos explica lo que hace el nuevo archivo `setuid`. Al intentar hacer `./suconnect <PORT>` nos dice `Could not connect`. Esto se debe a que ese puerto que pongamos o no está abierto o no esta esperando ninguna conexión, por lo tanto tenemos que ponernos a escuchar desde el puerto que decidamos y luego conectarnos.

Para ello usaremos el comando `nc` con el argumento `-l` para que escuche en un puerto (modo servidor) y `-p` para especificar el puerto. A continuación le pasamos la contraseña, que será la que se transmita cuando ejecutemos `./suconnect`.

```
nc -l -p 4000
0qXahG8ZjOVMN9Ghs7iOWsCfZyXOUbYO
```

Ahora en otra terminal ejecutamos el siguiente comando.

`./suconnect 4000`

Y listo, con esto leeremos del puerto 4000 el mensaje enviado (la contraseña) y así el cliente (`./suconnect`) enviará la respuesta (la contraseña).

`EeoULMCra2q0dSkYj561DX7s1CpBuOBt`

[[Nivel 19 - Archivo setuid|Siguiente nivel]]