#Hexadecimal #View #Tools #xxd

Para poder ver un archivo en formato hexadecimal existe el comando `xxd`

Simplemente le pasamos el archivo que queremos ver en formato hexadecimal.

`xxd compressed_file.gzip`

Y te muestra por `stdout` el formato hexadecimal.

Además, si el archivo está ya en formato hexadecimal podemos revertirlo con el argumento `-r` o `-revert` y mostrará por `stdout` el archivo sin el formato hexadecimal.

`xxd -r hexadecimal_file`