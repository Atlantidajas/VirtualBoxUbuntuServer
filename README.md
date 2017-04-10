# Instalar Ubuntu Desktop 16.04 sobre VirtualBox

## Descargar imagen de Ubuntu 16.04

El tutorial está hecho con la versión de Ubuntu 16.04.2. Descargar la imagen ISO de la siguiente dirección:

* [http://releases.ubuntu.com/16.04/ubuntu-16.04.2-server-amd64.iso](http://releases.ubuntu.com/16.04/ubuntu-16.04.2-server-amd64.iso)

## Creación de la Máquina Virtual

Abrir el VirtualBox y crear una nueva máquina virtual pulsando en el botón _Nueva_:

<kbd>![img01](/images/01_config_vbox/img01.png)</kbd>

Configuramos el nombre de la máquina virtual:

* **Nombre**: Ubuntu16-server
* **Tipo**: Linux
* **Versión**: Ubuntu (64 bits)

<kbd>![img02](/images/01_config_vbox/img02.png)</kbd>

Configurar la cantidad de memoria RAM que se le va a asignar, en este caso, 1GB=1024MB (depende de la cantidad de memoria RAM de nuestor ordenador, para ordenadores con pocos recursos asignar 512MB de memoria RAM):

<kbd>![img03](/images/01_config_vbox/img03.png)</kbd>

Creamos el disco duro virtual:

<kbd>![img04](/images/01_config_vbox/img04.png)</kbd>

Elegimos el tipo de disco duro _VDI_, tal y como viene por defecto:

<kbd>![img05](/images/01_config_vbox/img05.png)</kbd>

Marcar la opción _Reservado dinámicamente_, esto significa que el disco que acabamos de crear crecerá a medida que se vaya llenando:

<kbd>![img06](/images/01_config_vbox/img06.png)</kbd>

Seleccionar el nombre del disco duro, en este caso dejamos el valor por defecto (coincide con el nombre de la máquina virtual) y asignar 16GB de tamaño al disco y pulsamos en **Crear**:

<kbd>![img07](/images/01_config_vbox/img07.png)</kbd>

Montar la imagen de Ubuntu 16.04 en la Unidad de CD-ROM virtual de la máquina virtual:

<kbd>![img08](/images/01_config_vbox/img08.png)</kbd>

En _Almacenamiento_, seleccionar el icono del CD-ROM vacío para configurar la unidad de CD-ROM virtual:

<kbd>![img09](/images/01_config_vbox/img09.png)</kbd>

Pulsamos sobre el icono del CD-ROM:

<kbd>![img10](/images/01_config_vbox/img10.png)</kbd>

Pulsar en el menú desplegable la opción _Seleccione archivo de disco óptico virtual..._:

<kbd>![img11](/images/01_config_vbox/img11.png)</kbd>

Navegar por el sistema de ficheros y seleccionar la imagen descargada de Ubuntu 16.04 previamente:

<kbd>![img12](/images/01_config_vbox/img12.png)</kbd>

Ahora en unidad de CD-ROM virtual aparece la imagen de Ubuntu 16.04 montada:

<kbd>![img13](/images/01_config_vbox/img13.png)</kbd>

En la pestaña **Sistema** seleccionar la etiqueta _Red_, pulsar en avanzadas y seleccionar _Reenvío de puertos_  para mapear el puerto SSH y poder acceder a la Máquina Virtual desde nuestro equipo usando el client Putty:

<kbd>![img14](/images/01_config_vbox/img14.png)</kbd>

Crear una nueva regla con los siguientes valores y pulsamos Ok:
* **Puerto Anfitrión**: 2222
* **Puerto Invitado**: 22

<kbd>![img15](/images/01_config_vbox/img15.png)</kbd>

## Instalar Ubuntu Server 16.04

Iniciar la máquina virtual Ubuntu16 que creamos anteriormente:

<kbd>![img01](/images/02_install_ubuntu/img01.png)</kbd>

Seleccionamos _Español_ y pulsamos _Enter_:

<kbd>![img02](/images/02_install_ubuntu/img02.png)</kbd>

Pulsamos en _Instalar Ubuntu Server_:

<kbd>![img03](/images/02_install_ubuntu/img03.png)</kbd>

Seleccionamos _España_ como ubicación (se utilizará para fijar posteriormente la zona horaria y localización del sistema):

<kbd>![img04](/images/02_install_ubuntu/img04.png)</kbd>

¿Detectar la disposición del teclado? Seleccionar _No_ y pulsar _Enter_:

<kbd>![img05](/images/02_install_ubuntu/img05.png)</kbd>

Seleccionar _Spanish_ como distribución de teclado y pulsar _Enter_:

<kbd>![img06](/images/02_install_ubuntu/img06.png)</kbd>

Seleccionar como distribución del teclado _Spanish_ y pulsar _Enter_ (esto es importante ya que si no el teclado se configurará en inglés):

<kbd>![img07](/images/02_install_ubuntu/img07.png)</kbd>

Configurar el nombre de la Máquina Virtual y pulsar _Enter_:

<kbd>![img08](/images/02_install_ubuntu/img08.png)</kbd>

Configurar el nombre completo para el nuevo usuario y pulsar _Enter_ (el nombre completo puede empezar con mayúsculas y contener espacios en blanco):

<kbd>![img09](/images/02_install_ubuntu/img09.png)</kbd>

Configurar el nombre de usuario para la cuenta (es el usuario con el que accederemos al sistema a posterior. El nombre de usuario debe empezar por minuscula y no debe contener espacios):

<kbd>![img10](/images/02_install_ubuntu/img10.png)</kbd>

Introducir el password del usuario creado y _Enter_:

<kbd>![img11](/images/02_install_ubuntu/img11.png)</kbd>

Volver a introducir el password del usuario creado y _Enter_ (debe coincidir con el password anterior):

<kbd>![img12](/images/02_install_ubuntu/img12.png)</kbd>

Si hemos introducido una contraseña que tiene menos de 8 caracteres nos saldrá este mensaje. Seleccionar _Sí_ y pulsar _Enter_:

<kbd>![img13](/images/02_install_ubuntu/img13.png)</kbd>

La instalación da la opción de cifrar la carpeta personal. Seleccionar _No_ y pulsar _Enter_:

<kbd>![img14](/images/02_install_ubuntu/img14.png)</kbd>

Detecta la zona horaria Atlantic/Canary. Seleccionar _Sí_ y pulsar _Enter_:

<kbd>![img15](/images/02_install_ubuntu/img15.png)</kbd>

Seleccionar el método de particionado automático _Guiado - utilizar el disco completo y configurar LVM_, que es el que viene por defecto y pulsar _Enter_:

<kbd>![img16](/images/02_install_ubuntu/img16.png)</kbd>

En esta pantalla aparece el disco que se va a particionar, sólo aparece uno porque creamos la Máquina Virtual con un solo disco. Pulsar _Enter_:

<kbd>![img17](/images/02_install_ubuntu/img17.png)</kbd>

¿Desea guardar los cambios a los discos y configurar LVM? Seleccionar _Sí_ y pulsar _Enter_:

<kbd>![img18](/images/02_install_ubuntu/img18.png)</kbd>

Cantidad en el grupo de volumen a usar en el particionado: por defecto, usará todo el tamaño del disco. Lo dejamos como está, seleccionar _Continuar_ y pulsar _Enter_:

<kbd>![img19](/images/02_install_ubuntu/img19.png)</kbd>

¿Desea escribir los cambios en los discos? Seleccionar _Sí_ y pulsar _Enter_:

<kbd>![img20](/images/02_install_ubuntu/img20.png)</kbd>

En esta pantalla nos pide información del proxy. En este caso lo dejamos en blanco, seleccionar _Continuar_ y pulsar _Enter_:

<kbd>![img21](/images/02_install_ubuntu/img21.png)</kbd>

¿Cómo desea adminsitrar las actualizaciones en este sistema? En este caso, seleccionar _Sin actualizaciones automáticas_, que es la opción por que viene por defecto y pulsar _Enter_:

<kbd>![img22](/images/02_install_ubuntu/img22.png)</kbd>

En programas a instalar, a parte de _standard system utilities_, marcar la opción _OpenSSH Server_ (para ello nos movemos con los cursores hasta llevar a la opción indicada y la seleciconamos pulsando la barra espaciadora):

<kbd>![img23](/images/02_install_ubuntu/img23.png)</kbd>

¿Desea instalar el cargador de arranque GRUB en el registro principal de arranque? Seleccionar _Sí_ y pulsar _Enter_:

<kbd>![img24](/images/02_install_ubuntu/img24.png)</kbd>

Una vez instalados todos los paquetes, sale el mensaje _Instalación completada_, seleccionar _Continuar_ y pulsar _Enter_:

<kbd>![img25](/images/02_install_ubuntu/img25.png)</kbd>

Después de reiniciar la Máquina Virtual, nos aparece la pantalla solicitando usuario para acceder al sistema:

<kbd>![img26](/images/02_install_ubuntu/img26.png)</kbd>

## Acceder a la Máquina Virtual desde nuestro equipo utilizando SSH

Para acceder a la Máquina Virtual por SSH lo haremos mediante el cliente Putty, que podemos descargar de la siguiente URL:
* [https://the.earth.li/~sgtatham/putty/latest/w64/putty.exe](https://the.earth.li/~sgtatham/putty/latest/w64/putty.exe)

Abrir el Putty, y para acceder a la Máquina Virtual ponemos los siguientes datos:

* **Host Name (or IP address)**: localhost
* **Port**: 2222

El puerto 2222 debe coincidir con el _Puerto Anfitrión_ configurado en la regla de _Reenvío de puertos_ configurada anteriormente. Pulsar _Open_:

<kbd>![img01](/images/03_access_ssh/img01.png)</kbd>

Aparece un mensaje indicando que es la primera vez que accedemos a la Máquina Virtual por SSH, seleccionar _Sí_ y pulsar _Enter_:

<kbd>![img02](/images/03_access_ssh/img02.png)</kbd>

Introducir el usuario y password que pusimos durante el proceso de instalación:

<kbd>![img03](/images/03_access_ssh/img03.png)</kbd>

Si todo ha ido bien, aparece la pantalla de que hemos accedido correctamente a la Máquina Virtual:
<kbd>![img04](/images/03_access_ssh/img04.png)</kbd>
