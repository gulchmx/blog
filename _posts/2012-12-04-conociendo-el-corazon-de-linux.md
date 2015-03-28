---
ID: 736
post_title: Conociendo el corazón de Linux
author: cyberthrone
post_date: 2012-12-04 23:40:41
post_excerpt:
layout: post
permalink: >
  http://gulch.mx/conociendo-el-corazon-de-linux/
sh5vp-video:
  - 
sh5vp-youtube_video_id:
  - 
sh5vp-vimeo_video_id:
  - 
sh5vp-width:
  - 550
sh5vp-height:
  - 344
sh5vp-preload:
  - yes
sh5vp-autoplay:
  - no
sh5vp-loop:
  - no
socialize_text:
  - 
socialize:
  - 1,2,22,24,17,18
dsq_thread_id:
  - 1460116838
---
<h1 style="text-align: center;"><strong>¿Qué es el kernel/núcleo?</strong></h1>
<p align="justify">El kernel o núcleo de linux se podría definir como el corazón de este sistema operativo. Es el encargado de que el software y el hardware de tu ordenador puedan trabajar juntos.</p>
<p style="text-align: center;"><img class="aligncenter" title="linux-corazon" src="http://farm9.staticflickr.com/8484/8247663952_9a65a9dc20.jpg" alt="linux_corazon" />
<strong>Las funciones más importantes del mismo, aunque no las unicas, son:</strong></p>

<ul>
	<li>Administración de la memoria, para todos los programas en ejecución.</li>
	<li>Administración del tiempo de procesador, que estos programas en ejecución utilizan.</li>
	<li>Es el encargado de que podamos acceder a los periféricos/elementos de nuestro ordenador de una manera comoda.</li>
</ul>
<strong>Existen dos versiones del Linux kernel:</strong>
<p align="justify"><strong>Versión de producción:</strong> La versión de producción, es la versión estable hasta el momento. Esta versión es el resultado final de las versiones de desarrollo o experimentales.</p>
<p align="justify">Cuando el equipo de desarrollo del núcleo experimental, decide que ha conseguido un núcleo estable y con la suficiente calidad, se lanza una nueva versión de producción o estable. Esta versión es la que se debería utilizar para un uso normal del sistema, ya que son las versiones consideradas más estables y libres de fallos en el momento de su lanzamiento.</p>
<p align="justify"><strong>Versión de desarrollo:</strong> Esta versión es experimental y es la que utilizan los desarrolladores para programar, comprobar y verificar nuevas características, correcciones, etc. Estos núcleos suelen ser inestables y no se deberían usar, a no ser que sepas lo que haces.</p>
<p align="justify"><strong>Cómo interpretar los números de las versiones: </strong>Las versiones del núcleo se numeran con 3 números, de la siguiente forma: XX.YY.ZZ</p>
<p align="justify"><strong>XX:</strong> Indica la serie principal del núcleo. Hasta el momento solo existen la 1 y 2. Este numero cambia cuando la manera de funcionamiento del núcleo ha sufrido un cambio muy importante.</p>
<p align="justify"><strong>YY:</strong> Indica si la versión es de desarrollo o de producción. Un número impar, significa que es de desarrollo, uno par, que es de producción.</p>
<p align="justify"><strong>ZZ:</strong> Indica nuevas versiones dentro de una versión, en las que lo unico que se ha modificado, son fallos de programación /bugs.</p>
<strong>Unos ejemplos nos ayudarán a entenderlo mejor:</strong>

ej1: versión del núcleo 2.0.0: Núcleo de la serie 2 (XX=2), versión de producción 0 (YY=0 par), primera versión de 2.0 (ZZ=0)
ej2: versión del núcleo 2.0.1: Núcleo de la serie 2, version 0, en el que se han corregido errores de programación presentes en la versión 2.0.0 (ZZ=1)
ej3: version del nucleo 2.1.100: version 100 del nucleo de desarrollo 2.1.

<strong>¿Dónde consigo el kernel/núcleo?</strong>

El núcleo se puede bajar de un gran número de servidores en internet. El servidor principal es <a href="http://www.kernel.org/" target="_blank">http://www.kernel.org/</a> y la página de servidores espejos es <a href="http://www.kernel.org/mirrors/" target="_blank">http://www.kernel.org/mirrors/</a>.

Si tienes problemas accediendo a estas páginas, aquí tienes una copia en otro servidor <a href="http://www.linux-es.com/lista_kernel.html" target="_blank">http://www.linux-es.com/lista_kernel.html</a>

<strong>¿Cómo se configura e instala el kernel/núcleo?</strong>
<p align="justify">Este es uno de los temas que más asustan a los nuevos usuarios de linux. Lo primero deciros que no hay razón para asustarse, la configuración e instalación de un nuevo núcleo en nuestro sistema es más fácil de lo que suena NO LE TENGAN MIEDO!!</p>
<p align="justify">Lo que si hay que hacer, es tener claro una serie de cosas antes de ponernos a trabajar, para asi evitar problemas. A continuación tienens una pequeña guia sobre como configurar e instalar un nuevo núcleo en tu sistema.</p>
<strong>Si habeis decidido instalar un nuevo núcleo en tu sistema, esto es lo que teneis que hacer:</strong>

<strong>Bajarse la última versión. De donde? Leerse la subsección anterior.</strong>
<p align="justify"><strong>NOTA:</strong> Si vais a instalar un núcleo de la serie 2.2.x, teneis que tener en cuenta que algunas distribuciones no están/estaban preparadas para hacer uso de esta serie. Si vuestra distribución no es de las que vienen preparadas, teneis que actualizar una serie de paquetes/programas antes de instalar el nuevo núcleo (mas información en la documentación que acompaña al nucleo). Las últimas distribuciones vienen todas preparadas para los núcleos de la serie 2.2.x y posteriores, esta nota solo es para los que tengan una distribución antigüa.</p>
Tener claro lo que vamos a hacer, leerse el documento HOWTO sobre el núcleo ( Ingles / Castellano)
<p align="justify">Tener claro las opciones que tenemos que configurar, para poder utilizar el hardware de nuestro sistema, asi como las características que queremos utilizar. Por ejemplo, si no utilizamos un dispositivo SCSI, no tenemos que configurar nada en el apartado SCSI de nuestro núcleo. Asi nos ahorramos espacio y tiempo.</p>
Entrar como root: su root (en caso de estar bajo fedora, redhat)
Ir al directorio /usr/src/: cd /usr/src/

Copiar el archivo que os habeis bajado al directorio /usr/src: cp linux-xx.yy.zz.tar.gz .

Descomprimirlo y desempaquetar: tar -xvzpf linux-xx.yy.zz.tar.gz
<p align="justify"><strong>NOTA</strong>: El archivo linux-xx.yy.zz.tar.gz se desempaquetará en el directorio /usr/src/linux. Si ya existe un directorio llamado /usr/src/linux en tu sistema, renombrarlo, p.ej: mv linux linux-old .
En algunas distribuciones, usr/src/linux es un enlace simbólico a linux-x.y.z, borrar este enlace simbólico. Es importante que no exista ningún directorio/enlace simbólico llamado linux, antes de desempaquetar la nueva versión. Si te has bajado el kernel comprimido con bzip2, tendras que descomprimirlo con bunzip2 linux-xx.yy.zz.tar.bz2 antes de desempaquetarlo con tar -xvf linux-xx.yy.zz.tar</p>
Entrar en /usr/src/linux: cd /usr/src/linux

<strong>Configurar el núcleo, esto se puede hacer de tres maneras diferentes:</strong>
<pre class="lang:ps decode:true">make config (modo texto)
make menuconfig (modo texto con menus)
make xconfig (XWindow version)</pre>
Si teneis XWindow instalado, os recomiendo el último comando, si no, el segundo. Os recomiendo que las opciones que vienen por defecto no las toqueis si no sabeis lo que haceis, podeis pulsar Help en cada opción para obtener una descripción de la misma. Configurar las opciones que querais tener en vuestro nuevo núcleo. Una vez terminada la configuración, grabar los cambios y salir del programa de configuración.

Una vez terminado el proceso de configuración, tenemos que compilar nuestro nuevo núcleo. Para ello hay que hacer lo siguiente:
<pre class="lang:ps decode:true">make dep
make clean
make bzImage</pre>
Si en el proceso de configuración, elegimos alguna opción como módulo, tendremos que compilar/instalar dichos módulos:
<pre class="lang:ps decode:true">make modules
make modules_install</pre>
&nbsp;

<strong>NOTA:</strong> No olvidar ejecutar como root el comando depmod -a la primera vez que arranqueis con vuestro nuevo núcleo, para computar las dependencias entre módulos.
<p align="justify">Ya tenemos el núcleo y los módulos compilados, ahora tenemos que instalarlo. Casi todo el mundo utiliza LILO para arrancar el sistema, por ello explicaré como instalarlo utilizando LILO.</p>
<p align="justify">Todavia estamos en /usr/src/linux , ejecutar el comando make install , esto copiará el núcleo que acabamos de crear, a el directorio /boot de nuestro sistema, con el nombre vmlinuz, o como un enlace simbóolico vmlinuz -&gt; vmlinuz-xx.yy.zz</p>
<p align="justify">Ahora tenemos que configurar LILO para que reconozca el nuevo núcleo. Tendremos que modificar el fichero /etc/lilo.conf. Aquí teneis un ejemplo, del fichero /etc/lilo.conf antes de modificarlo:</p>
boot=/dev/hda
prompt
timeout=50
image=/boot/vmlinuz-2.0.34
label=linux
root=/dev/hda1
read-only

Y aqui como quedaría despues de la modificación, para que reconozca nuestro nuevo núcleo al arrancar:

boot=/dev/hda
prompt
timeout=50
image=/boot/vmlinuz
label=nuevokernel
root=/dev/hda1
read-only
image=/boot/vmlinuz-2.0.34
label=linux
root=/dev/hda1
read-only
<p align="justify">Ahora solo tenemos que ejecutar el comando /sbin/lilo y arrancar el sistema de nuevo. Si tuviesemos algún problema con el nuevo núcleo, siempre podriamos arrancar con el antiguo escribiendo linux y pulsando ENTER cuando arrancamos y nos sale en pantalla lilo: De esta manera podemos entrar y ver que es lo que ha fallado.</p>
<p align="justify">NOTA: Recordar que existen multitud de opciones para configurar LILO, y que los ejemplos anteriores, son ejemplos. Puede que vuestro sistema necesite diferentes parámetros y opciones. Leeros los documentos HOWTOS sobre el núcleo y LILO antes de cambiar nada en nuestro sistema. Al final de esta sección tienen enlaces a los mismos.
Suerte y espero que tengas las cosas un poco mas claras.</p>
<strong>Qué son los parches (patchs)? ¿Cómo se instalan?</strong>

<strong>¿Qué son los parches y para qué sirven?:</strong>
<p align="justify">Un parche para el núcleo no es más, que un fichero que solamente contiene información, sobre las lineas de código que han cambiado desde la versión precedente del núcleo. De esta manera, solamente os teneis que bajar un fichero con los cambios, en vez, del núcleo al completo. El ahorro en cantidad de Mb bajados es bastante considerable, sobre todo para aquellos que dependen del módem y no tienen una conexión buena a internet.</p>
<p align="justify">Algo a tener muy en cuenta si van a actualizar el núcleo por medio de parches, en vez de bajaros el núcleo al completo, es que tienes que ir actualizando de versión a versión. Para que se entienda un poco mejor, aqui tienes un ejemplo:</p>
<p align="justify">Si tienes el núcleo 2.2.0 y vas a actualizarlo al 2.2.1, los podes bajar el fichero patch-2.2.1.gz [70Kb] en vez, del núcleo 2.2.1 al completo [12.5Mb].</p>
<p align="justify">Si la diferencia entre la versión que tienes y la que quieres instalar, es muy grande (p.ej: del 2.2.0 al 2.2.10), no os merece la pena actualizar por medio de parches, en este caso aconsejo que bajes la versión completa.</p>
<strong>¿Qué hacer con un fichero patch-XX.YY.ZZ.gz?:</strong>
<p align="justify">Ya despues de tener el fichero patch (se pueden bajar del mismo subdirectorio donde está la versión completa), que necesitas para actualizar el núcleo, y ahora, ¿qué hacemos?. Ahora, hay que aplicarlo al núcleo que tienes y compilar de nuevo. El procedimiento para actualizar el núcleo por medio de ficheros patch es el siguiente:</p>
Copiar el fichero patch-XX.YY.ZZ.gz al directorio /usr/src/ : cp patch-XX.YY.ZZ.gz /usr/src/
Cambiar a este subdirectorio y descomprimir el fichero: cd /usr/src/; gunzip patch-XX.YY.ZZ.gz
Aplicar el parche: patch -s -p0 &lt; patch-XX.YY.ZZ
La opción -s hara que solo se impriman mensajes de error. Si no recibes ningún mensaje de error (como debería de ser ;-)) solamente os queda entrar en /usr/src/linux: cd /usr/src/linux
Y ejecutar make clean, make xconfig, make dep, make bzImage

<strong>¿Algún consejo sobre el kernel/núcleo?</strong>

Pregunta: ¿Necesito actualizar el núcleo que utilizo, cada vez que una nueva versión aparece?
Respuesta: No. ¿Porqué? La explicación es la siguiente:

Cuando un nuevo núcleo aparece, puede ser por las siguientes causas:

Nuevas características se han añadido.
Fallos de programación se han corregido.
Fallos de seguridad se han corregido.
Nuevo hardware es soportado.
<p align="justify">Si las características que se han añadido, no las vamos a utilizar, es evidente que no necesitamos actualizar. Si los fallos de programación que se han corregido afectan a características/drivers que no utilizamos, no necesitamos actualizar. Si no utilizamos el nuevo hardware soportado, tampoco necesitamos actualizar.</p>
<p align="justify">De todas maneras es recomendable, actualizar de vez en cuando, sobre todo cuando se corrigen fallos de seguridad o cuando los cambios en el nuevo núcleo afectan a características/funciones/hardware que utilicemos. El código esta ahí, libre y esperando a ser compilado en un nuevo ordenador, cada usuario debe de decidir cuando es hora de una actualización.</p>
<p align="justify">Pregunta: <strong>¿Soy nuevo en Linux y acabo de instalar una distribución, como actualizo el núcleo?</strong>
Respuesta: Te aconsejo que esperes un poquito. La distribución que acabas de instalar (si es de las últimas) viene con un núcleo de los "últimos", totalmente funcional y que te sirve sin problemas. Utiliza el sistema un tiempo, familiarizate con el nuevo sistema que acabas de instalar, y cuando comprendas un poco más como funcionan las cosas, actualiza el núcleo. Un buen punto de partida para encontrar información sobre el núcleo, lo tienes en estas páginas.</p>
Enlaces sobre el kernel

<a href="http://www.kernel.org/" target="_blank">The LinuxKernel Archives: Página principal/oficial sobre el núcleo.</a>
<a href="http://kt.linuxcare.com/" target="_blank"> Kernel Traffic: Información sobre la lista de correo sobre el núcleo.</a>
<a href="http://www.kernelnotes.org/" target="_blank"> KernelNotes: Mucha información sobre núcleo.</a>
<a href="http://linuxmafia.com/" target="_blank"> LinuxMafia: Actualizaciones no oficiales.</a>
<a href="http://linuxmafia.com/" target="_blank">Guía de programación: de módulos para el núcleo (Inglés)</a>
<a href="http://www.tldp.org/LDP/tlk/tlk.html" target="_blank">The Linux Kernel: Libro (Inglés)</a>