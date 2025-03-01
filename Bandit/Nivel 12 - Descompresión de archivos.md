#BanditChallenge #Compressed #Files #Hexadecimal 
### Enunciado
La contraseña para el siguiente nivel se almacena en el archivo data.txt, que es un hexdump de un archivo que ha sido comprimido repetidamente. Para este nivel puede ser útil crear un directorio bajo /tmp en el que puedas trabajar. Utilice mkdir con un nombre de directorio difícil de adivinar. O mejor, utilice el comando «mktemp -d». Luego copia el archivo de datos usando cp, y renómbralo usando mv (¡lee las páginas de manual!)
### Solución
Para poder resolver este ejercicio es necesario tener conocimiento sobre el funcionamiento del comando `xxd` y conocer los tipos de `magic numbers` de cada formato de compresión para saber que herramienta usar para descomprimirlos.

##### Comando `xxd`
Sirve para mostrar un archivo en formato hexadecimal, muy útil para ver el tipo de formato de un archivo en este caso. Con el argumento `-r` hace la operación inversa.

##### Números mágicos (`magic numbers`)
Cada formato de compresión tiene unos bytes en la cabecera llamados `magic numbers`, los cuales sirven para identificar el tipo de compresión.

[[Números mágicos - Archivos Comprimidos]]

<hr>

Por lo tanto, la forma de resolver este ejercicio es primero hacer `xxd -r` para obtener el archivo sin formato hexadecimal y después ir descomprimiendo el archivo viendo el tipo de compresión que tiene hasta llegar a la solución.

`The password is FO5dwFsc0cbaIiH0h8J2eUks2vdTDwAn`

[[Nivel 13 - Conexión SSH con clave privada|Siguiente nivel]]