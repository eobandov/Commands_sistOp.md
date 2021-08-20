### Repositorio sobre comandos aprendidos en el Curso de SO 🌟


##### ✨ Hecho por Emily Massielle Obando Vargas ✨

En este repositorio se sumarizan los comandos aprendidos divididos por las clases donde se aprendieron

#### Semana 2 🗺️ 🥽
```markdown
_Para ver ruta en la que se encuentra_
  pwd

_Actualizar repositorios_
  apt-get update

_Dar permisos de super usuario a cualquier comando_
  sudo

_Instalar software desde repositorios_
  apt install
  snap  `tambien se puede usar`

_Limpiar terminal_
  clear

_Revisar posibilidades de comandos o software_
  apt search
```

#### Semana 3 🥅 🌳 🔪 🐈
```markdown
_Ver datos de red_
ip addr

_Ver IP de maquina_
nmap [IP]

_Hacer ping de alguna maquina_
ping [IP]

_Crear directorios_
mkdir

_Ver procesos, con parametro -aux se ven procesos activos_ 
_Con top se ven procesos en tiempo real, es mas interactivo_
ps -aux
top
pstree
htop `debe instalarse`

_Concatenar comandos_
|

_Buscar_
grep 
find 

_Matar procesos_
kill -9 [nombre]

_Ver que usuario esta usando el sistema_
whoami

_Entrar como super usuario `root`_
sudo su
sudo -i
su root

_Establecer contraseñas_
sudo passwd [usuario]

_Crear archivos_
touch

_Editar archivos de texto_
vim
nano

_Enlistar lo que contiene el directorio actual_
ls -l

_Mostrar contenido del archivo_
cat 
more
less

_Ver usuarios y sus datos_
cat /etc/passwd
```
#### Semana 6 🧠 📑
```markdown
_Ver datos de la memoria_
  sudo dmidecode --type 17
  cat/proc/meminfo

_Recorrer procesos actuales y leer cuantos KB/s usa cada uno_
  for file in /proc/*/status ; do awk '/VmSwap|Name/{printf $2 " " $3}END{ print ""}' $file; done | sort -k 2 -n -r | less

_Comando para leer memoria disponible_
  free -h

_Comando para dar prioridad a la memoria swap_
  swapon

_Comando Swampiness: editar # de cuanto porcentaje de memoria usa en RAM_
  cat /proc/sys/vm/swappiness
  
_Crear un disco de memoria RAM_
sudo mkdir /mnt/ram_disk

_Montar un sistema de archivos usando RAM_
sudo mount -t tmpfs -o size=1024m new_ram_disk /mnt/ram_disk

_Ver detalles de directorios_
df -h
```

Markdown is a lightweight and easy-to-use syntax for styling your writing. It includes conventions for

```markdown
Syntax highlighted code block

# Header 1
## Header 2
### Header 3

- Bulleted
- List

1. Numbered
2. List

**Bold** and _Italic_ and `Code` text

[Link](url) and ![Image](src)
```

For more details see [GitHub Flavored Markdown](https://guides.github.com/features/mastering-markdown/).

### Jekyll Themes

Your Pages site will use the layout and styles from the Jekyll theme you have selected in your [repository settings](https://github.com/eobandov001/Commands_sistOp.md/settings/pages). The name of this theme is saved in the Jekyll `_config.yml` configuration file.

### Support or Contact

Having trouble with Pages? Check out our [documentation](https://docs.github.com/categories/github-pages-basics/) or [contact support](https://support.github.com/contact) and we’ll help you sort it out.
