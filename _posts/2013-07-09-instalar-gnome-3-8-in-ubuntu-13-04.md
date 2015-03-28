---
ID: 1255
post_title: Instalar GNOME 3.8 in Ubuntu 13.04
author: hacktotopo
post_date: 2013-07-09 12:00:21
post_excerpt:
layout: post
permalink: >
  http://gulch.mx/instalar-gnome-3-8-in-ubuntu-13-04/
socialize_text:
  - 
socialize:
  - 1,2,22,24,17,18
fb_fan_page_post_id:
  - 246202975455925_489916224417931
dsq_thread_id:
  - 1481882605
---
<p style="text-align: justify;">Tras instalar  gnome 3.8 en mi laptop (Toshiba l305) obtuve muchas mejoras significativas  con respecto a la velocidad (hasta el momento va muy bien).</p>
<p style="text-align: justify;">Gnome 3.8 es el resultado de 6 meses trabajo del Proyecto GNOME y contiene 35936 contribuciones hechas por aproximadamente 960 personas.</p>
<p style="text-align: justify;"><strong>Añadir Gnome 3 PPA:</strong></p>
<p style="text-align: justify;">Para agregar la PPA a nuestro sistema abrimos una terminal y ejecutamos :</p>

<pre class="lang:default decode:true">sudo add-apt-repository ppa:gnome3-team/gnome3</pre>
ahora bien actualizamos  los repositorio para poder instalar lo necesario.
<pre class="lang:default decode:true">sudo apt-get update</pre>
<strong>Instalar Gnome-Shell y Gnome</strong>

Ahora bien , debes instalar Gnome-Shell ya que reemplazarás Unity  y lo harás de la siguiente forma:
<pre class="lang:default decode:true">sudo apt-get install gnome-shell</pre>
posteriormente instalar Gnome
<pre class="lang:default decode:true">sudo apt-get install ubuntu-gnome-desktop</pre>
Cuando esté por  terminar  tendrás que elegir el gestor de ventanas "GDM"

<b>Activar</b>

Tras terminar la instalación reinicia el sistema  y en la pantalla de inicio selecciona el entorno "GNOME".
<p style="text-align: center;"><img class="aligncenter  wp-image-1258" alt="Screen Gnome 3.8 hacktotopo" src="http://gulch.mx/wp-content/uploads/2013/07/subir-700x437.jpeg" /></p>
<a href="https://help.gnome.org/misc/release-notes/3.8/">Mas información.</a>

Te fue útil la información , coméntanos que te pareció  <img class=" wp-image-1198 alignnone" alt="awsm" src="http://gulch.mx/wp-content/uploads/2013/06/awesome.png" />