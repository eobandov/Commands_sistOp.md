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

#### Semana 7 🖼️ 🔐
```markdown
_Ver tamaño de archivo_
  du -h archivo.png

_Ver fecha de creación, último acceso_
  stat archivo.png

_Tipo de archivo_
  file archivo.png
  
_Propietario y grupo, lista de permisos. Cambio de propietario, otorgar permisos_
  chown user1 archivo.png
  chmod 777 archivo.png 
  
_Mostrar el espacio en disco usado_ 
  df -h
  
_Mount: Montaje de dispositivos en el sistema de archivos_
  /etc/fstab 
  mount /dev/cdrom /mnt

_Gparted: Administra las particiones_
  sudo apt install gparted
  
_gnome-disk-utility: Muestra información sobre el disco_
  sudo apt install gnome-disk-utility

_Matar un proceso_
  kill -9 $PID
```

#### Semana 9 🎮 🐚 🧑‍⚖️ 📥
```markdown
_Ver version de bash_
  bash --version

_Ver ubicación de los intérpretes_ 
  echo $SHELL

_Ver todos los shells instalados_
  cat /etc/shells
 
_Cambiar bash a ksh_
  chsh -s /bin/zsh 

_Ejecutarlo scripts_
./script.sh
bash script.sh

_Imprimir_
echo

_Inicio de scripts en bash: `shebang`_
#!/bin/bash

_Dar permisos de ejecutar a scripts_
chmod +x script.sh
chmod 755 script.sh

_Declarar variables y asignarles un valor_
NAME=$(hostname)

_Debugg_
~/scripts> bash -x script.sh 

_Instalar paquetes_
dpkg -t [nombre]

_Formato basico de programacion en bash_
**if** [ condicion ];
then
 accion1
else
 accion2
fi

**for** i in variable
do
 accion1 $i
done

**while** [ variable ]
do
  accion1
  accion2
done

**function** F1()
{
accion1
}
F1

_Entrada de usuario_
read variable

```

#### Semana 10: Docker images 🧙 ✨
```markdown
_Servidor de Software_
  docker pull store/gitlab/gitlab-ce:10.2.4-ce.0

_Servidor DHCP_
  docker pull sw4iot/isc-dhcp
  docker pull gartz/simple-dns

_Servidor SSH, FTP, SAMBA_
  docker pull itsthenetwork/nfs-server-alpine
  docker pull stanback/alpine-samba

_Servidor FTP y Servidor Web_
  docker pull stilliard/pure-ftpd
  docker pull inwt/r-shiny

_Servidor de Respaldos_
  docker pull nextcloud

_Servidor Proxy_
  docker pull minimum2scp/squid

_Servidor de Logs_
  docker pull splunk/splunk 
_Kali Linux_
  docker pull kalilinux/kali-linux-docker
_Ubuntu_
  docker pull ubuntu

```

#### Semana 11 🛂 📚
```markdown
_Ver contraseñas en linux_
  /etc/passwd
  /etc/shadow
  sudo passwd root
  
_Ver contraseñas en windows_
  lsadump::sam sam3.hiv system.hiv
  `revisar editor de registro HKEY LOCAL MACHINE SAM export`
  
_Cracking Hashes_
  john --show passwords.txt
  cat hashes.txt

_Ver version de GUI de nmap_
  zenmap

_uso de firewall_
  sudo apt-get install iptables
  sudo iptables -L -v
  sudo iptables -A INPUT -p tcp --dport [numero de puerto] ACCEPT
  sudo iptables -A INPUT -j DROP
  sudo iptables -A INPUT -s [IP] -j ACCEPT
  sudo iptables -A INPUT -s [IP] -j DROP

_Descargar ICMP /Broadcast_
/etc/sysctl.conf
net.ipv4.icmp_echo_ignore_all = 1
net.ipv4.icmp_echo_ignore_broadcasts = 1
sysctl -p

_Ejecucion de parches_
sudo apt update / sudo ap upgrade
sudo pacman -Syuu
yum -y update
`Windows Update`

_Gestion de logs_
/var/log/auth.log
/var/log/message # Todos los logs disponibles del sistema 
/var/log/auth.log # logs de autentificacion
/var/log/kern.log # Logs del Kernel
/var/log/cron.log # logs de crond 
/var/log/maillog # logs del correo del servidor
/var/log/boot.log # Logs de inicio del sistema
/var/log/mysqld.log # Logs de MySQL 
/var/log/apache/access.log # Logs de Apache
/var/log/secure # logs de autentificacion
/var/log/utmp # registro de inicios de sesion
/var/log/wtmp 
/var/log/yum.log # Log de Yum

```

#### Manjaro 
`Traducción: Manjaro es una palabra swahili que significa "No puedo configurar Arch".`
![GitHub Logo](/manjaro.PNG)

```markdown
_Actualizar repositorios_
sudo pacman -Syuu

_Instalar zip_
sudo pacman -S unrar zip unzip p7zip gzip bzip2

_Instalar repositorio AUR_
sudo pacman -S yay
sudo yay -S --needed base-devel

_Agregar usuarios_
sudo useradd -m nombredeusuario -G wheel -p passworddelusuario

_Eliminar subdirectorios_
rmdir

_Eliminar archivos_
rm

_Ver historial de comandos escritos en la terminal_
history

_Ver número de inodo_
ls -li archivo.txt

_Crear el enlace duro_
ln prueba.txt nuevaRutaArchivo

_Crear enlace simbólico_
ln -s ruta/prueba.txt nuevaRuta/prueba2 

_Para acceder a contrab_
contrab -e

_`Así se ve el formato dentro del archivo crontab`_
m h dom mon dow user command 
```


### Soporte o contacto

Teniendo problemas con Paginas? Revisa la documentación [documentation](https://docs.github.com/categories/github-pages-basics/) o [contact support](https://support.github.com/contact) y te ayudaremos a solucionarlo.
