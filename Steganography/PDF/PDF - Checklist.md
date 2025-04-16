Lista de cosas que hacer para resolver un reto de información oculta en un PDF.

1. `file FILE` - Confirmar que realmente es un PDF
2. `strings FILE` - Buscar información útil
3. `exiftool FILE` - Posible información en los metadatos
4. `binwalk FILE` - Para comprobar si hay algún archivo incrustado (si hay imágenes también se mostrarán las imágenes del PDF lo que complicará el escenario)
5. `peepdf -i FILE` - Muestra objetos del archivo sospechosos y te permite ver todos los objetos del fichero haciendo `object ID`
6. `object ID > archivo` - En caso de encontrar algo y querer extraerlo, intentar decodificarlo con `base64` o el formato que se encuentre