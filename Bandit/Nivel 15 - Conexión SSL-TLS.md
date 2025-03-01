#BanditChallenge #SSL/TLS
### Enunciado
La contraseña para el siguiente nivel se puede recuperar enviando la contraseña del nivel actual al puerto 30001 en localhost utilizando encriptación SSL/TLS.

Nota útil: ¿Recibes «DONE», «RENEGOTIATING» o «KEYUPDATE»? Lea la sección «CONNECTED COMMANDS» en la página de manual.
### Solución
Para poder conectarnos a `localhost` con la encriptación SSL/TLS podemos ejecutar el siguiente comando.

`openssl s_client -connect localhost:30001`

Con esto obtenemos la conexión con encriptación SSL/TLS. Ahora simplemente ponemos la contraseña del ejercicio anterior.

```
8xCjnmgoKbGLhHFAZlGE5Tmu4M2tKJQo
Correct!
kSkvUpMQ7lBYyCM4GBPvCvT1BfWRy0Dx
```
