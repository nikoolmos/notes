# Esquema de particiones de un disco en Linux

> El objetivo es crear un sistema seguro y fiable.


* 1 partición para `SWAP` de 32 GB.
* 1 partición para `boot` de 1 GB.
* 1 partición para `/`.
* 1 partición para `var`.
* 1 partición para `home`.
* 1 partición para `tmp`.


Otras posibles particiones:

* /var/www
* /var/lib/mysql
* /var/log
* /boot
* /boot/efi

Revisar las opciones de seguridad más pertinentes para cada partición.


## Sobre el cifrado de una partición Linux
https://en.wikipedia.org/wiki/Linux_Unified_Key_Setup


Fuentes:

https://www.daniloaz.com/es/blog/la-importancia-de-particionar-correctamente-un-disco-en-linux
https://docs.redhat.com/es/documentation/red_hat_enterprise_linux/6/html/installation_guide/s2-diskpartrecommend-x86
