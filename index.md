## Bienvenid@s a mi repositorio sobre el Curso de Sistemas Operativos

#### Hecho por Emily Massielle Obando Vargas

En este repositorio se sumarizan los comandos aprendidos divididos por las clases donde se aprendieron

### Semana 2
```markdown
**Para ver ruta en la que se encuentra**
  pwd

**Actualizar repositorios** 
  apt-get update

**Dar permisos de super usuario a cualquier comando**
  sudo

**Instalar software desde repositorios**
  apt install
  snap  `tambien se puede usar`

**Limpiar terminal**
  clear

**Revisar posibilidades de comandos o software**
  apt search
```

### Semana 3
```markdown
_Ver datos de red_
ip addr

_Ver IP de maquina_
nmap [IP]

_Hacer ping de alguna maquina_
ping [IP]

_Crear diirectorios_
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
