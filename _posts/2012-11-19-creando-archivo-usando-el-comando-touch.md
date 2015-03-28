---
ID: 625
post_title: Creando archivo usando el comando touch
author: Ismael Garcia (@tuxisma)
post_date: 2012-11-19 06:07:08
post_excerpt:
layout: post
permalink: >
  http://gulch.mx/creando-archivo-usando-el-comando-touch/
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
fb_fan_page_post_id:
  - 246202975455925_471884502850377
facebook_status_messages:
  - 'a:1:{i:0;a:2:{s:7:"message";s:96:"Posted to <a href="https://www.facebook.com/471884502850377" target="_blank">GNU Linux Latam</a>";s:5:"error";s:0:"";}}'
dsq_thread_id:
  - 1462846359
gx2014_side_layout:
  - default
gx2014_thumb_show:
  - off
gx2014_ppslider_show:
  - off
gx2014_video_type:
  - youtube
gx2014_video_show:
  - off
gx_review_enable:
  - 0
gx_user_ratings_visibility:
  - 0
gx_review_type:
  - stars
gx_criteria_display:
  - t
---
<p style="text-align: justify;" align="justify"><img class="aligncenter wp-image-1859" src="http://gulch.mx/wp-content/uploads/2012/11/Touch.png" alt="Touch GulchMX" width="600" height="450" /></p>
<p style="text-align: justify;" align="justify">Cada archivo en GNU/LINUX es asociado con la marca de tiempo, cuando se especifica la hora del último acceso, hora de la última modificación y hora de último cambio.</p>
<p style="text-align: justify;">Cuando se crea un nuevo archivo o se modifica un archivo existente o los atributos, el tiempo debe de ser actualizado automáticamente.</p>
<p style="text-align: justify;">El comando touch es usado para cambiar estos tiempos ( hora de acceso, hora de modificación, el tiempo de cambio de un archivo).</p>

<ul style="text-align: justify;">
	<li><strong>Crear un archivo vacío usando el comando touch.</strong></li>
</ul>
<p style="text-align: justify;" align="justify">Se puede crear un archivo vacío usando el comando touch. El siguiente ejemplo crea un archivo vacío con cero bytes de tamaño llamado archivo.txt.</p>

<pre class="lang:sh decode:true">$touch archivo.txt</pre>
<p style="text-align: justify;">Se puede usar la opción <strong>-c </strong>para evitar crear nuevos archivos. Si usamos la opción <strong>-c</strong>  y si el archivo no existe, el comando touch no va a crear el archivo.</p>

<pre class="lang:sh decode:true">$touch -c archivo.txt</pre>
<p style="text-align: justify;">Podemos crear más de un archivo usando solamente una vez el comando touch. El siguiente ejemplo muestra como crear 4 archivos con nombre a, b, c  y d.</p>

<pre class="lang:sh decode:true">$touch a b c d</pre>
<ul style="text-align: justify;">
	<li><strong>Cambiar el tiempo de acceso a los archivos usando  la opción</strong> <strong>-a</strong></li>
</ul>
<div style="text-align: justify;"><strong>
</strong></div>
<p align="justify">Cambiamos el tiempo de acceso de un archivo con la opción <strong>-a. </strong>Por default este debería de tomar la hora actual del sistema.</p>

<div style="text-align: justify;">Antes de ejecutar el comando touch:</div>
<div style="text-align: justify;">
<pre class="lang:sh decode:true">[Ismael@tuxisma pruebas]$ stat archivo.txt
Fichero: «archivo.txt»
Tamaño: 0 Bloques: 0 Bloque E/S: 4096 fichero regular vacío
Dispositivo: 805h/2053d Nodo-i: 926098 Enlaces: 1
Acceso: (0664/-rw-rw-r--) Uid: ( 500/ Ismael) Gid: ( 500/ Ismael)
Contexto: unconfined_u:object_r:user_home_t:s0
Acceso: 2012-11-22 13:17:05.340652891 -0600
Modificación: 2012-11-22 13:17:05.340652891 -0600
Cambio: 2012-11-22 13:17:05.340652891 -0600
Creación: -</pre>
&nbsp;

Después podemos ejecutar el comando touch:
<pre class="lang:default decode:true">$touch -a archivo.txt</pre>
Ejecutamos:
<pre class="lang:sh decode:true">$stat archivo.txt</pre>
&nbsp;

Quedaría de esta manera, si se observa los tiempos han cambiado:
<pre class="lang:sh decode:true">[Ismael@tuxisma pruebas]$ stat archivo.txt
Fichero: «archivo.txt»
Tamaño: 0 Bloques: 0 Bloque E/S: 4096 fichero regular vacío
Dispositivo: 805h/2053d Nodo-i: 926098 Enlaces: 1
Acceso: (0664/-rw-rw-r--) Uid: ( 500/ Ismael) Gid: ( 500/ Ismael)
Contexto: unconfined_u:object_r:user_home_t:s0
Acceso: 2012-11-22 13:18:11.725908136 -0600
Modificación: 2012-11-22 13:17:05.340652891 -0600
Cambio: 2012-11-22 13:18:11.725908136 -0600
Creación: -</pre>
&nbsp;
<ul>
	<li> Cambiar el la hora de modificación de los archivos, usando -m.</li>
</ul>
</div>
<div style="text-align: justify;">Se puede cambiar la fecha de modificación  de un archivo usando -m.</div>
<div style="text-align: justify;">
<pre class="lang:sh decode:true">$touch -m *.o</pre>
&nbsp;

</div>
<div style="text-align: justify;">No es posible cambiar la hora usando el comando touch.</div>
<div style="text-align: justify;">
<ul>
	<li>Establecer explícitamente el acceso y hora de modificación con -t y -d.</li>
</ul>
<div>EL formato para especificar con -t es: [[CC]YY]MMDDhhmm[.SS]</div>
<div>$touch -t [[CC]YY]MMDDhhmm[.SS]</div>
</div>
<div style="text-align: justify;"></div>
<div style="text-align: justify;"><strong>CC</strong> Especifica los primeros dos digitos del año.</div>
<div style="text-align: justify;"><strong>YY</strong> Especifica los ultimos dos digitos del año. Si el valor de la YY esta entre el 70 Y 99, los valores de CC debe de ser 19. Si el valor de la YY esta entre 00 y 37 el valor de la CC debe de ser 20.No es posible asignar dato de 13 de enero de 2038.</div>
<div style="text-align: justify;"><strong>MM </strong>Especifica el mes.</div>
<div style="text-align: justify;"><strong>DD </strong>Especifica el día</div>
<div style="text-align: justify;"><strong>hh</strong> Especifica la hora.</div>
<div style="text-align: justify;"><strong>mm</strong> Especifica los minutos</div>
<div style="text-align: justify;"><strong>SS</strong> Especifica los segundos.</div>
<div style="text-align: justify;"></div>
<div style="text-align: justify;">Ejemplo:</div>
<div style="text-align: justify;">
<pre class="lang:sh decode:true">$ touch -a -m -t 203010191300.00 archivo.txt</pre>
&nbsp;

Le decimos que el acceso y la modificación fue el año 2030, dia 19 del mes de Octubre con hora 13,minuto 00 y segundos 00.

</div>
<div style="text-align: justify;">

 Tecleamos el comando :
<pre class="lang:sh decode:true ">$ stat archivo.txt</pre>
<pre class="lang:sh decode:true">Fichero: «archivo.txt»
Tamaño: 0 Bloques: 0 Bloque E/S: 4096 fichero regular vacío
Dispositivo: 805h/2053d Nodo-i: 926098 Enlaces: 1
Acceso: (0664/-rw-rw-r--) Uid: ( 500/ Ismael) Gid: ( 500/ Ismael)
Contexto: unconfined_u:object_r:user_home_t:s0
Acceso: 2030-10-19 13:00:00.000000000 -0500
Modificación: 2030-10-19 13:00:00.000000000 -0500
Cambio: 2012-11-22 14:18:48.256156941 -0600
Creación: -</pre>
&nbsp;

También se puede usar cadenas para establecer la hora.

Ejemplo:
<pre class="lang:sh decode:true ">$touch -d "2020-10-19 12:20:20.000000000 +0530" archivo.txt</pre>
Introducimos :
<pre class="lang:sh decode:true">$stat archivo.txt</pre>
<pre class="lang:sh decode:true">Fichero: «archivo.txt»
Tamaño: 0 Bloques: 0 Bloque E/S: 4096 fichero regular vacío
Dispositivo: 805h/2053d Nodo-i: 926098 Enlaces: 1
Acceso: (0664/-rw-rw-r--) Uid: ( 500/ Ismael) Gid: ( 500/ Ismael)
Contexto: unconfined_u:object_r:user_home_t:s0
Acceso: 2020-10-19 01:50:20.000000000 -0500
Modificación: 2020-10-19 01:50:20.000000000 -0500
Cambio: 2012-11-22 14:31:38.346508743 -0600
Creación: -</pre>
&nbsp;

Copiar la marca de tiempo desde otro archivo usando <strong>-r</strong>.

Se puede tomar un archivo como referencia y actualizar la hora para otros archivos.

Ejemplo:
<pre class="lang:sh decode:true ">$ touch archi.txt -r archivo.txt</pre>
&nbsp;

Copiamos la fecha y hora del archivo archivo.txt y se lo pasamos al archivo archi.txt.
<pre class="lang:sh decode:true ">$stat archi.txt</pre>
&nbsp;
<pre class="lang:sh decode:true ">Fichero: «archi.txt»
Tamaño: 0 Bloques: 0 Bloque E/S: 4096 fichero regular vacío
Dispositivo: 805h/2053d Nodo-i: 926100 Enlaces: 1
Acceso: (0664/-rw-rw-r--) Uid: ( 500/ Ismael) Gid: ( 500/ Ismael)
Contexto: unconfined_u:object_r:user_home_t:s0
Acceso: 2020-10-19 01:50:20.000000000 -0500
Modificación: 2020-10-19 01:50:20.000000000 -0500
Cambio: 2012-11-22 14:46:28.997306269 -0600
Creación: -</pre>
&nbsp;

</div>