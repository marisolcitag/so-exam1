**1.**
# Examen Parcial 1
**Nombre:** Marisol Giraldo Cobo

**Código:** A00246380

**Correo:** marisol.giraldo@correo.icesi.edu.co

**Curso:** Sistemas Operativos

**Tema:** Comandos de Linux, Virtualización

**Profesor:** Daniel Barragán

**2.**
# Descripción:
Con la realización de este Readme, se pretende mostrar los pasos realizados en la instalación del sistema operativo Debian 9 Server en una máquina virtual. A continuación se mostrará, el paso a paso mediante texto y capturas de pantalla de los aspectos mas relevantes a tener en cuenta.

**3.**
Ingresar a la siguiente página web:  

![descargardebian](https://user-images.githubusercontent.com/35766585/37865154-7835f3f4-2f46-11e8-9193-b43a725bb14e.png)

Escoger la opción arquitectura amd64.
A continuación se descargara la Imagen ISO. Una vez la descarga se haya realizado es necesario verificar mediante el checksum si la imagen es correcta. Mediante el software MD5-SHA-Checksum-Utility que se encuentra en el enlace http://download.cnet.com/MD5-SHA-Checksum-Utility/3001-2092_4-10911445.html, se realiza la verificación: Primero se adjunta la Imagen ISO que se descargo para analizarla y luego se ingresa a la siguiente página para identificar los códigos a comparar:

![enlaceverificardebian](https://user-images.githubusercontent.com/35766585/37865230-854cb28e-2f47-11e8-87d8-4345bcc5aed0.png)

Se ingresa el código que corresponda a la Imagen ISO descargada, y si coincide significa que la Imagen ISO del SO que se descargó  es correcta y puede ser utilizada de manera confiable para instalación.

![debianmatch](https://user-images.githubusercontent.com/35766585/37865253-f5d3b642-2f47-11e8-8e0b-3e3fc7f1d729.png)

**4.**
Para realizar la instalación del SO Debia 9 Server, primero fue necesario hacer uso de una máquina virtual, donde se configuró, el espacio en memoria, en disco duro, se adjuntó la Imagen ISO descargada en la opción de almacenamiento y las configuraciones de red básicas en la opción red donde el adaptador 1 se configuro como NAT y el adaptador 2 como Adaptador Puente.

![13configuracion](https://user-images.githubusercontent.com/35766585/37865361-747a7e1c-2f49-11e8-889c-1d24fd9ad112.png)

Después se procedió a iniciar la máquina virtual y realizar la instalación del SO Debian 9 Server.

![instalacion](https://user-images.githubusercontent.com/35766585/37865393-e1957c68-2f49-11e8-87a8-17768cd8883b.png)

Una vez inicia el proceso de instalación se configura el nombre de la máquina, la contraseña de usuario root, un nombre de usuario adicional con su respectiva contraseña, las particiones del disco, el idioma, la ubicación geográfica, el tipo de teclado y se escogen los programas a instalar. En este caso se escogierón las opciones: Entorno de Escritorio Debian, Web Server, Servidor de Impresión, SSH Server y Utilidades del Sistema.
Una vez se termina el proceso de instalación, el sistema se reinicia y aparece la pantalla de Inicio de Sesión.

![iniciodesesion](https://user-images.githubusercontent.com/35766585/37865580-6e4f9920-2f4c-11e8-99e7-8f93c5bc3a71.png)

Al ingresar aparecerá el entorno de escritorio Debian. Lo que dará por terminado el proceso de Instalación.

![escritoriodebian](https://user-images.githubusercontent.com/35766585/37865602-e6ad68d4-2f4c-11e8-8c2a-cea26ce02893.png)

Para obtener la información  del sistema operativo por medio de comandos linux se debe hacer lo siguiente:

Abrir la Terminal en Debian e Ingreso los siguientes comandos:

-apt-get update: este comando actualiza la lista de paquetes disponibles y sus versiones, pero no instala o actualiza ningún paquete. Esta lista la coge de los servidores con repositorios que están definidos en el sources.list.


-apt-get upgrade: una vez el comando anterior ha descargado la lista de software disponible y la versión en la que se encuentra, podemos actualizar dichos paquetes usando este comando: apt-get upgrade. Instalará las nuevas versiones respetando la configuración del software cuando sea posible.

![update_upgrade](https://user-images.githubusercontent.com/35766585/37866010-6ff5b3b2-2f52-11e8-90ce-e33d2d81fbba.png)

A continuación se muestra por medio de comandos de Linux la información del sistema operativo.

# uname -s
uname -s => Muestra el nombre del sistema.

# uname -n
uname -n => Muestra el nombre por el que se identifica el sistema en la red (el FQDN)

# uname -a
uname -a => Muestra toda la información sobre el tipo de sistema que se esta utilizando.

# uname -m
uname -m => Muestra el tipo de arquitectura que se esta utilizando.

# uname -r
uname -r => Muestra información sobre el kernel.

# uname -v
uname -v => Muestra información sobre la versión del Sistema Operativo.

# uname -p
uname -p => Muestra información sobre el procesador.

![uname](https://user-images.githubusercontent.com/35766585/37866156-b2836be6-2f54-11e8-8317-37d5c0e08014.png)

# lsb_release -a
![lsb_release_a](https://user-images.githubusercontent.com/35766585/37870548-738555e0-2f9e-11e8-888f-18974f4abaf8.png)

**5.**

**CONFIGURACIÓN INTERFAZ PRIVADA**

![10configuracion](https://user-images.githubusercontent.com/35766585/37866510-87baf4ba-2f59-11e8-9449-0b2688af95e9.png)


**CONFIGURACIÓN INTERFAZ PUENTE**

![12configuracion](https://user-images.githubusercontent.com/35766585/37866604-08479d9e-2f5b-11e8-8ac5-51cc34fbf267.png)

**CONEXIÓN SSH A MAQUINA VIRTUAL**

Para acceder a la máquina virtual a través de SSH (Linux)
Primero, se consulta la dirección Ip que tenga asignada el equipo, en este caso:

![verip](https://user-images.githubusercontent.com/35766585/37866593-ca47d8ec-2f5a-11e8-8143-ff05cd7b972e.png)

Después se abre MTPutty y se configura la sesión para hacer la conexión con la Ip.

![mtputty2](https://user-images.githubusercontent.com/35766585/37870405-f3af0166-2f9a-11e8-952a-7eef522621f6.png)

Al configurar la sesión, se da doble clic sobre ella y se ingresa el password de usuario.

![mputty](https://user-images.githubusercontent.com/35766585/37866682-0fdf6270-2f5c-11e8-8b3f-52dd2f7313b2.png)

Si el password ingresado es correcto se establece la conexión con la máquina virtual. De lo contrario, debe volver a digitarse.

![mputty2](https://user-images.githubusercontent.com/35766585/37866711-5c6ae998-2f5c-11e8-859e-27cef03db2d8.png)

Si al realizar la conexión, no está instalado el modulo de SSH en Debian, la conexión será rechazada. Por lo tanto, se debe instalar el SSH en la máquina virtual con 
el comando: apt-get install openssh-server 

**6.**

**INSTALACIÓN GIT**

![aptgit](https://user-images.githubusercontent.com/35766585/37866753-f5d45e70-2f5c-11e8-83ac-cebea5358904.png)

**INSTALACIÓN TIG**

![apttig](https://user-images.githubusercontent.com/35766585/37866962-c25bdd9a-2f5f-11e8-9ab8-307434417984.png)

Inicialmente al ejecutar el comando Tig se obtuvo esta pantalla.
![tig](https://user-images.githubusercontent.com/35766585/37870472-d0c8b514-2f9c-11e8-8470-d49d644ac066.png)

Al final de realizar el parcial, de acuerdo a los cambios que se realizaron, al ejecutar el comando Tig se obtuvo esta pantalla.
![tig2](https://user-images.githubusercontent.com/35766585/37870485-17610ca6-2f9d-11e8-8d32-46aa98df6ae1.png)


**7.**

Para realizar la exportación de la máquina virtual se debe:

1. Ir al menú Archivo y dar clic en la opción Exportar servicio virtualizado

2. Escoger la máquina virtual del SO Debian 9 Server
![exportarmv](https://user-images.githubusercontent.com/35766585/37870453-3f48d47a-2f9c-11e8-8d95-b3b124f1294c.png)

3. Seleccionar la carpeta donde va a guardarse
![exportarmv2](https://user-images.githubusercontent.com/35766585/37870192-91633ab8-2f95-11e8-982b-40f2b7a8f23b.png)

4. Dar click en Exportar
![exportarmv3](https://user-images.githubusercontent.com/35766585/37870234-1d7b8d8e-2f96-11e8-86fe-e257400843d5.png)

![exportarmv4](https://user-images.githubusercontent.com/35766585/37870246-66f747dc-2f96-11e8-922b-24480b53d76c.png)

5. Una vez termina de realizarse la exportación, el archivo queda disponible en la ubicación escogida para cuando se quiera utilizar.
![exportarmv5](https://user-images.githubusercontent.com/35766585/37870281-b7427e7c-2f97-11e8-9537-b8a9832eaf7d.png)



Para importar en un Pc de la Sala de Sistemas en Icesi, se debe :

1. Iniciar sesión en el Pc. 

2. Ejecutar el programa Virtual Box.

3. Ir al menú Archivo y dar clic en la opción importar servicio virtualizado 
![menuimportar](https://user-images.githubusercontent.com/35766585/38325585-07551fb8-3809-11e8-98ee-08af36cd980f.png)

4. Seleccionar la ubicación donde se encuentra la imagen iso a importar.

5. Una vez se seleccione, empezara el proceso de importación
![importando maquina virtual](https://user-images.githubusercontent.com/35766585/38325666-422c58a4-3809-11e8-909b-a84d168a5692.png)

6. Se puede observar en la maquina virtual el SO importado para ser utilizado.
![maquina virtual import exitoso](https://user-images.githubusercontent.com/35766585/38325699-684e9f56-3809-11e8-846b-534980c9f924.png)



**8.**

CARACTERISTICA | DEBIAN |CENTOS
--- | --- | ---
DISTRIBUCIÓN | Libre | GNU/Linux Derivado-Clonado de Red Hat Enterprise Linux
CREADOR      | Ian Murdock |CentOS Project 
PRODUCTOR     |            Debian Project                   |                         CentOS Project
PRIMER LANZAMIENTO     |   16/09/93                        |                          01/12/03
ARQUITECTURAS |    PowerPC, x86 (tanto de 32 como de 64 bits), ARM, SPARC, MIPS, MIPSEL PA-RISC, 68k, S390, System Z, IA-64,DEC Alpha. |En la versión 4.6 CentOS soportaba las arquitecturas siguientes: x86, x86-64, IA-64, Alpha, s390, s390x,PowerPC, y SPARC. Pero a partir de la versión 5, CentOS solo soporta las arquitecturas x86 y x86-64, cuando RHEL da soporte también a las CPU's Itanium y PowerPC.
VERSIONES PRINCIPALES APLICACIONES | •Apache -> 2.2.22  •PHP -> 5.4.4 •MySQL -> 5.5.30 •PostgreSQL -> 9.1.9 | •Apache -> 2.2.15 •PHP -> 5.3.3 •MySQL -> 5.1.66 •PostgreSQL -> 8.4.13
ULTIMA VERSIÓN | 9  |	7
LINUX | 2.6.24  2.6.18
COMPILADOR | GCC 4.1.1, 3.4.6, 3.3.6, 2.95  | GCC 4.1.1
SISTEMA DE FICHEROS POR DEFECTO  | ext4 | ext3
REQUERIMIENTOS MINIMOS  |  •CPU a 1GHz como mínimo  •64MiB de RAM (256MiB recomendados) y 1GiB de espacio en disco para la instalación sin escritorio. •128MiB de RAM (512MiB recomendados) y 5GiB de espacio en disco para la instalación con escritorio. •Tarjeta gráfica VGA, Lector de CD, puerto USB o conexión de red Ethernet. | •CPU a 1GHz como mínimo •128MiB de memoria RAM, 512MiB recomendados •1,2GiB de espacio en disco, recomendados 2GiB. •Tarjeta gráfica VGA y monitor capaz de soportar una resolución de 1024x768. •Lector de CD-ROM o puerto USB.
ENTORNO GRAFICO | •Debian no tiene marcado ningún entorno gráfico predefinido, pudiéndose no instalar ninguno,O instalar, ya sean:GNOME, KDE, Xfce, LXDE o cualquier otro. Incluye configuración automática del sistema gráfico en la mayor parte de hardware existente, soporte completo al sistema de ficheros NTFS, auto configuración de la mayor parte de las teclas multimedia, soporte para el formato de archivos Flash de Adobe a través de los complementos swfdec o Gnash y herramientas propias para ordenadores portátiles (como el soporte integrado del escalado de frecuencia de la CPU), entre otras características. | •GNOME
GESTIÓN DE PAQUETES | •Debian hace uso de su propia herramienta, APT, para administrar los paquetes.  | •addons: Contiene los paquetes necesarios para instalar la distribución. Son paquetes considerados esenciales para el buen funcionamiento del sistema, aunque puede que no sean esenciales para la distribución Red Hat Enterprise Linux. •apt: Exclusivo de CentOS 4, contiene todos los RPM's de la Herramienta APT, útil para realizar actualizaciones usando el sistema APT. Solo funciona para sistemas x86. •centosplus: Todos los paquetes aportados por los desarrolladores y usuarios de CentOS. Puede suponer un riesgo si se reemplazan archivos críticos del sistema. •contrib: Paquetes aportados únicamente por los usuarios, excluyendo los que forman el núcleo del sistema. No han sido probados por los desarrolladores de CentOS, con lo que ello implica. •docs: Contiene los manuales y las notas de la versión de CentOS •extras: Paquetes mantenidos por los desarrolladores de CentOS que añaden funcionalidad a la distribución. •updates: Contiene las actualizaciones de la distribución
No PAQUETES BINARIOS  | Aproximadamente 36.000 | Aproximadamente 1.700
No PAQUETES CÓDIGO FUENTE |  Aproximadamente 18.000  | Aproximadamente 18.000
ACTUALIZACIONES | •La actualización de Debian es mucho más sencilla y menos complicada, basta con tener instalado software estándard y sus repositorios. | •Las actualizaciones pequeñas, como lo son las de seguridad las de una versión x.y a x.w se harán muy fácilmente con yum update && yum upgrade. El problema se da cuando quieres hacer actualización mayor, de X a Y. En este caso, CentOS recomienda hacer una instalación desde cero, y no hacer un upgrade. 
ESTABILIDAD  | Muy Estable | Muy Estable	
COMPATIBILIDAD | •IBM •HP-UX •RED-HAT •SOLARIS •SUSE LINUX •WINDOWS | •Esta basado en una fuente RHEL, Centos adecuados para muchos de los paquetes herramientas creadas de RHEL y sus problemas de compatibilidad son mínimos.
USOS | •Multiuso •Producción | •Servidores •Estaciones de trabajo •Producción
FACILIDAD DE CONFIGURACION | •Sin costo •Sencillo •Multiusuario •Kernel | •Tiene configuración por defecto •Tiene programas incluidos •Incluye navegadores web y utilidades de oficina •Requiere menos mantenimiento
FACILIDAD DE USO | •Fácil de instalación   •Centro de software ubuntu •Almacenamiento en la nube. •Gestión multimedia. | •Funciona bien Para servidores •Fácil de instalar •Es Gratuito,robusto y estable


**9.**


**URL GITHUB** => https://github.com/marisolcitag/so-exam1.git


**BIBLIOGRAFIA**

- DEBIAN
  URL: https://www.debian.org/
  
- REPOSITORIO GITHUB
  URL: https://github.com/ICESI 
  URL: https://github.com/ICESI-Training 
  
- Estudio comparativo de distribuciones GNU/Linux
  URL: http://openaccess.uoc.edu/webapps/o2/bitstream/10609/8190/1/oyerpesTFC0611.pdf
  
- WIKIPEDIA Anexo:Comparación de distribuciones Linux
  URL: https://es.wikipedia.org/wiki/Anexo:Comparaci%C3%B3n_de_distribuciones_Linux

- FRANCISCONI.ORG SOLUCIONES INFORMÁTICAS Comandos Uname
  URL: http://francisconi.org/linux/comandos/uname
  
- LINUX HISPANO  Diferencias entre apt-get-update y apt-get-upgrade
  URL: http://www.linuxhispano.net/2013/05/03/diferencia-entre-apt-get-update-y-apt-get-upgrade/
 
