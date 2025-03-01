#BanditChallenge #Telnet #Netcat
### Enunciado
La contraseña para el siguiente nivel se puede recuperar enviando la contraseña del nivel actual al puerto `30000` en `localhost`.
### Solución
Nos dicen que hay que enviar la contraseña del nivel actual a `localhost` en el puerto `30000`. Pues simplemente podemos usar Telnet para hacer el intercambio de mensajes.

`telnet localhost 30000`

Y ya estamos conectados, ahora simplemente introducimos la contraseña del nivel anterior.

```
MU4VWeTyJk8ROof1qqmcBPaLh7lDCPvS
Correct!
8xCjnmgoKbGLhHFAZlGE5Tmu4M2tKJQo
```

[[Nivel 15 - Conexión SSL-TLS|Siguiente nivel]]