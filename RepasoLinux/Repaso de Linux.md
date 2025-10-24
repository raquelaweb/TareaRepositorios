# Repaso de Linux

[TOC]

## Capitulo 2 - Ficheros y Directorios

Directorios más importantes del sistema Linux:

<img src="./Repaso%20de%20Linux.assets/image-20250925170314445.png" alt="image-20250925170314445" style="zoom:67%;" />

### Comandos pwd, ls, cd, mkdir

## Ejercicios Capitulo 2

3 - Muestra el contenido del directorio actual:

```bash
sudo ls
```

![image-20250925171256782](./Repaso%20de%20Linux.assets/image-20250925171256782.png)



4 - Muestra el contenido del directorio que está justo a un nivel superior:

```bash
cd ..
```

```bash
sudo ls
```

![image-20250925171500859](./Repaso%20de%20Linux.assets/image-20250925171500859.png)



5 - ¿En qué día de la semana naciste?, utiliza la instrucción cal para averiguarlo.

```bash
cal -d 2000-01
```

<img src="./Repaso%20de%20Linux.assets/image-20250929161634961.png" alt="image-20250929161634961" style="zoom:50%;" />



6 - Muestra los archivos del directorio /bin.

```bash
sudo su
cd ..
cd ..
cd bin
ls -la
```

<img src="./Repaso%20de%20Linux.assets/image-20250929161110851.png" alt="image-20250929161110851" style="zoom: 50%;" />



7 - Suponiendo que te encuentras en tu directorio personal (/home/nombre), muestra un listado del contenido de /usr/bin a) con una sola línea de comando, b) moviéndote paso a paso por los directorios y c) con dos líneas de comandos.

a)

```bash
ls -la
```

b)

```bash
cd usr
cd bin
cd ls -la
```

<img src="./Repaso%20de%20Linux.assets/image-20250929161802815.png" alt="image-20250929161802815" style="zoom:50%;" />



8 - Muestra todos los archivos que hay en /etc y todos los que hay dentro de cada subdirectorio, de forma recursiva (con un solo comando).

```bash
ls etc
```

<img src="./Repaso%20de%20Linux.assets/image-20250929162052548.png" alt="image-20250929162052548" style="zoom:50%;" />

```bash
tree etc
```

<img src="./Repaso%20de%20Linux.assets/image-20250929163232699.png" alt="image-20250929163232699" style="zoom:50%;" />



9 - Muestra todos los archivos del directorio /usr/X11R6/bin ordenados por tamaño (de mayor a menor). Sólo debe aparecer el nombre de cada fichero, sin ninguna otra información adicional.

```bash
cd usr

cd bin

dir -S
```

<img src="./Repaso%20de%20Linux.assets/image-20250929163657344.png" alt="image-20250929163657344" style="zoom:50%;" />



10 - Muestra todos los archivos del directorio /etc ordenados por tamaño (de mayor a menor) junto con el resto de características, es decir, permisos, tamaño, fechas de la última modificación, etc. El tamaño de cada fichero debe aparecer en un formato “legible”, o sea, expresado en Kb, Mb, etc.

```bash
tree -p -u -s -D --sort size
```

<img src="./Repaso%20de%20Linux.assets/image-20250929165109206.png" alt="image-20250929165109206" style="zoom:50%;" />



11 - Muestra todos los archivos del directorio /bin ordenados por tamaño (de menor a mayor). Sólo debe aparecer el tamaño y el nombre de cada fichero, sin ninguna otra información adicional. El tamaño de cada fichero debe aparecer en un formato “legible”, o sea, expresado en Kb, Mb, etc.

```bash
ls -lh
```

<img src="./Repaso%20de%20Linux.assets/image-20250929170001399.png" alt="image-20250929170001399" style="zoom:50%;" />



12 - Muestra el contenido del directorio raíz utilizando como argumento de ls una ruta absoluta.

```bash
ls usr/bin
```

<img src="./Repaso%20de%20Linux.assets/image-20250929170300421.png" alt="image-20250929170300421" style="zoom:50%;" />



13 - Muestra el contenido del directorio raíz utilizando como argumento de ls una ruta relativa. Suponemos que el directorio actual es /home/elena/documentos.

```bash
cd ..
cd ..
ls ..
```

<img src="./Repaso%20de%20Linux.assets/image-20250929170937311.png" alt="image-20250929170937311" style="zoom:50%;" />



14 - Crea el directorio gastos dentro del directorio personal.

```bash
mkdir gastos
```

<img src="./Repaso%20de%20Linux.assets/image-20250929171230604.png" alt="image-20250929171230604" style="zoom:50%;" />



15 -  ¿Qué sucede si se intenta crear un directorio dentro de /etc?

Crea el directorio sin ningun problema

<img src="./Repaso%20de%20Linux.assets/image-20250929172215695.png" alt="image-20250929172215695" style="zoom: 67%;" />



16 - Muestra el contenido del fichero /etc/fstab.

```bash
cat fstab
```

<img src="./Repaso%20de%20Linux.assets/image-20250929172414856.png" alt="image-20250929172414856" style="zoom: 50%;" />



17 - Muestra las 10 primeras líneas del fichero /etc/bash.bashrc.

```bash
more -n 10 bash.bashrc
```



18 - Crea la siguiente estructura de directorios dentro del directorio de trabajo personal:

<img src="./Repaso%20de%20Linux.assets/image-20251006162746760.png" alt="image-20251006162746760" style="zoom:50%;" />

```bash
mkdir multimedia
cd multimedia
mkdir musica
mkdir imagenes
mkdir video
mkdir presentaciones
cd imagenes
mkdir personales
mkdir otras
```



19 - Crea un fichero vacío dentro del directorio musica, con nombre estilos_favoritos.txt.

```bash
cd musica
touch estilos_favoritos.txt
```



20 - Utiliza tu editor preferido para abrir el fichero estilos_favoritos.txt e introduce los estilos de música que más te gusten. Guarda los cambios y sal.

```bash
gedit estilos_favoritos.txt
```



21 - Muestra todo el contenido de estilos_favoritos.txt.

```bash
cat estilos_favoritos.txt
```



22 - Muestra las 3 primeras líneas de estilos_favoritos.txt.

```bash
more --lines 3 estilos_favoritos.txt
```



23 - Muestra la última línea de estilos_favoritos.txt.

```bash
tail -n 1 estilos_favoritos.txt
```



24 - Muestra todo el contenido del fichero estilos_favoritos.txt excepto la primera línea. Se supone que no sabemos de antemano el número de líneas del fichero.

```bash
tail -n +2 estilos_favoritos.txt
```



## Ejercicios Capitulo 3

1 - Muestra todos los archivos del directorio actual que son imágenes jpg.

```bash
ls Imágenes/*.jpeg
```



2 - Muestra todos los archivos del directorio /usr/bin que empiecen por la letra j.

```bash
cd usr
cd bin
ls j*
```



3 - Muestra los archivos que empiecen por k y tengan una a en la tercera posición, dentro del directorio /usr/bin.

```bash
ls k?a*
```



4 - Muestra los archivos del directorio /bin que terminen en n.

```bash
ls *n
```



5 - Muestra todos los archivos que hay en /etc y todos los que hay dentro de cada subdirectorio, de forma recursiva.

```bash
cd etc
tree -R
```



6 - Crea un directorio en tu directorio de trabajo con nombre prueba. Copia el archivo gzip del directorio /bin al directorio prueba. Crea un duplicado de gzip con nombre gzip2 dentro de prueba.

```bash

```





## COMANDOS LINUX

1 - Muestra todas las interfaces de red activas y sus direcciones IP en el sistema.

```bash
ifconfig
```



2 - ¿Cómo mostrarías solo la información de la interfaz de red `eth0` usando `ip a`?

```

```



3 - Configura manualmente la dirección IP `192.168.1.100/24` en la interfaz `eth0` con `ifconfig`.

```bash
ifconfig -v eth0 | 192.168.1.100/24
```



4 - Envía 10 paquetes ICMP a la dirección IP `8.8.8.8` usando `ping`.

