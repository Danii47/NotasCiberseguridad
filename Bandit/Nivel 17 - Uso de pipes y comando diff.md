#BanditChallenge #diff #pipes
### Enunciado
Hay 2 archivos en el homedirectory: passwords.old y passwords.new. La contraseña para el siguiente nivel está en passwords.new y es la única línea que ha cambiado entre `passwords.old` y `passwords.new`.

**NOTA:** si has resuelto este nivel y ves «¡Adiós!» cuando intentas entrar en `bandit18`, esto está relacionado con el siguiente nivel, `bandit19`.
### Solución
Para completar este nivel voy a proponer 2 métodos.
#### Método 1 - Comando diff
Usando el comando `diff` podemos ver la diferencia entre 2 archivos pasados por argumento.

```bash
diff passwords.old passwords.new
42c42
< x2gLTTjFwMOhQ8oWNbMN362QKxfRqGlO
---
> ktfgBvpMzWKR5ENj26IbLGSblgUG9CzB
```

Y ahora comprobamos cual es el que se encuentra en el archivo `passwords.new`.

`grep x2gLTTjFwMOhQ8oWNbMN362QKxfRqGlO passwords.new`

Por lo tanto esa es la contraseña.

#### Método 2 - Uso de tuberías
Es posible concatenar varios comandos para eliminar las entradas repetidas entre los dos archivos.

`cat passwords.new passwords.old | sort | uniq -u`

> [!TIP]
> El argumento `-u` del comando `uniq` sirve para solo mostrar las lineas que no están repetidas.

Y de la misma forma, obtenemos la contraseña.

`x2gLTTjFwMOhQ8oWNbMN362QKxfRqGlO`

[[Nivel 18 - Ejecutar comandos con SSH y SCP|Siguiente nivel]]