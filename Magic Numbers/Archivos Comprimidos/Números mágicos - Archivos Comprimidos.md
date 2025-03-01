#Compressed #Files #MagicNumbers #Cryptography #Information #Hexadecimal 

**GZIP (`.gz`):** 1F 8B
**BZIP (`.bz`, `.bz2`):** 42 5A XX (el último byte indica la versión de `bzip`)
**XZ (`.xz`):** FD 37 7A 58 5A (los últimos 4 es la palabra `7zXZ`)
**ZIP (`.zip`):** 50 4B XX XX (los últimos 2 bytes indican la versión y tipo de archivo)
**TAR (`.tar`):** No es un método de compresión, si no de agrupación de archivos. Se identifica si el inicio del archivo es un nombre (el nombre del archivo)