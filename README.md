Linux Commands
=========================================================================================================================

Backup
***********************************************************************************************

Backup toda la unidad: # dd if=/dev/sda of=/dev/sdb
Crear imagen del disco: # dd if=/dev/hda of=~/hdadisk.img
Restaurar usando disco duro: # dd if=hdadisk.img of=/dev/hdb
Backup una partición: # dd if=/dev/hda1 of=~/partition1.img
CDROM backup: # dd if=/dev/cdrom of=tgsservice.iso bs=2048


Comandos frecuentes
************************************************************************************************

Crear archivo tar: $ tar cvf archive_name.tar dirname/
Extrer de un archivo tar: $ tar xvf archive_name.tar
Ver archivo tar: $ tar tvf archive_name.tar
Buscar string en un fichero: $ grep -i "the" demo_file
Buscar string en ficheros recursivamente: $ grep -r "ramesh" *
Imprimir string encontrado, máx. 3 línias: $ grep -A 3 -i "example" demo_text
Buscar ficheros por nombre: # find -iname "MyCProgram.c"
Ejecutar comando en ficheros encontradors: $ find -iname "MyCProgram.c" -exec md5sum {} \;
Buscar ficheros vacíos en directorio: # find ~ -empty
Login servidor remoto SSH: $ ssh -l jsmith remotehost.example.com
Debug cliente SSH: $ ssh -v -l jsmith remotehost.example.com
Ver versión cliente SSH: $ ssh -V
Convertir fichero DOS a UNIX: $sed 's/.$//' filename
Eliminar línias duplicadas con AWK: $ awk '!($0 in array) { array[$0]; print }' temp
Imprimir celda fichero con AWK: $ awk '{print $2,$5;}' employee.txt
Comparar ficheros (obviando espacios): # diff -w name_list.txt name_list_new.txt
Organizar por nombre ascendiente: $ sort names.txt
Organizar por nombre descendente: $ sort -r names.txt
Organitzar por la tercera fila: $ sort -t: -k 3n /etc/passwd | more
Ver crontab: # crontab -u usuario -l
Ver estado de un servicio: # service servicio status
Ver estado todos los servicios: service --status-all
Reiniciar un servicio: # service ssh restart
Ver procesos en ejecución: $ ps -ef | more
Ver procesos en ejecución (modo en árbol): $ ps -efH | more
Memoria libre, usada y en swap: $ free
Ver espacio de filesystem: $ df -h
Matar proceso: $ kill -9
Eliminar fichero: $ rm -i filename.txt
Ver múltiples ficheros: $ cat file1 file2
Cambiar permissos directorio: $ chmod -R ug+rwx file.txt
Cambiar password usuario: $ passwd
Parar / arrancar adaptador de red: $ ifconfig eth0 up      $ ifconfig eth0 down
Localizar comando: $ locate
Información al respecto de un comando: $ whatis ls
Imprimir últimas diez linias fichero: $ tail filename.txt
Download sw de internet: $ wget http://prdownloads.sourceforge.net/sourceforge/nagios/nagios-3.2.1.tar.gz

Sincronización
***********************************************************************************************************

Sincronizar dos directorios: $ rsync -zvr /var/opt/installation/inventory/ /root/temp
Sincronizar un fichero: $ rsync -v /var/lib/rpm/Pubkeys /root/temp/
Sincronizar de local a remoto: $ rsync -avz /root/temp/ thegeekstuff@192.168.200.10:/home/thegeekstuff/temp/
Sincronizar de remoto a local: $ rsync -avz thegeekstuff@192.168.200.10:/var/lib/rpm /root/temp


Boot Up
**************************************************************************************************************
Ver mensajes BootUp: # dmesg | more
Ver estado ethernet durante arranque: # dmesg  | grep eth




