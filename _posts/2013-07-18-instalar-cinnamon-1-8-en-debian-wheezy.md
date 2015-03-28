---
ID: 1275
post_title: Instalar Cinnamon 1.8 Debian Wheezy
author: hacktotopo
post_date: 2013-07-18 15:40:34
post_excerpt:
layout: post
permalink: >
  http://gulch.mx/instalar-cinnamon-1-8-en-debian-wheezy/
socialize_text:
  - 
socialize:
  - 1,2,22,24,17,18
fb_fan_page_post_id:
  - 246202975455925_494107617332125
dsq_thread_id:
  - 1510538968
---
<p style="text-align: justify;"><span style="color: #000000;">Cinnamon es un entorno de escritorio para Linux que se desarrolló inicialmente para Linux Mint y más tarde a disposición de todas las distros linux en general. Se deriva del escritorio Gnome 3, pero proporciona el tipo tradicional de entorno de escritorio. Cinnamon utiliza Muffin, un fork de GNOME 3 gestor de ventanas Mutter.</span></p>
<p style="text-align: justify;"><span style="color: #000000;">Cinnamon es una Shell de GNOME Shell,  ofrecer el diseño y la personalización de GNOME 2 .</span></p>
<span style="color: #000000;"><strong>Novedades en la versión 1.8</strong></span>
<p style="text-align: justify;"><span style="color: #000000;">Dentro de las novedades en esta versión 1.8 podemos encontrar las siguientes:</span></p>

<ul>
	<li style="text-align: justify;"><span style="color: #000000;"><strong><span style="line-height: 13px;">Administrador de archivos:</span></strong><span style="line-height: 13px;"> Mejoras en el comportamiento ,funciones nuevas  e integradas para Cinnamon.</span></span></li>
	<li style="text-align: justify;"><span style="color: #000000;"><strong>Screensaver:</strong> Para personalizar y crear Screensavers.</span></li>
	<li style="text-align: justify;"><span style="color: #000000;"><strong>Control Center: </strong>Muchas mejoras significativas.</span></li>
	<li style="text-align: justify;"><span style="color: #000000;"><strong>Desklets: </strong>Aun no existe una lista extensa.</span></li>
</ul>
<p style="text-align: center;"><span style="color: #000000;"><strong>Instalación en Debian Wheezy</strong></span></p>
<p style="text-align: left;"><span style="color: #000000;">1.- Primero vamos a editar la lista de repositorios  en nano /etc/apt/sources.list  , agregar lo siguiente  y guardar. </span></p>

<pre class="lang:sh decode:true">## Cinnamon 1.8 
deb http://packages.linuxmint.com/ debian main upstream import</pre>
<span style="color: #000000;"> 2.- Actualizar la lista de repositorios  ejecutando en comando siguiente (te enviará un error que se resolverá posteriormente).</span>
<pre class="lang:sh decode:true">apt-get update</pre>
3.- Instalar  la llave para el repositorio.
<pre class="lang:sh decode:true">apt-get install linuxmint-keyring</pre>
<span style="color: #000000;">4.- Ejecutar la actualización  (está vez no te enviará errores porque el source ya está firmado) .</span>
<pre>apt-get update</pre>
<span style="color: #000000;"> 5.- Instalamos cinnamon 1.8 (cuando terminé cierra sesión  y elige como entorno cinnamon)  </span>
<pre class="lang:sh decode:true">apt-get install cinnamon cinnamon-session cinnamon-settings</pre>
<p style="text-align: center;"> <img class="aligncenter size-large wp-image-1277" alt="Cinnamon 1.8 Escritorio hacktotopo" src="http://gulch.mx/wp-content/uploads/2013/07/Captura-de-pantalla-de-2013-07-18-004633-700x437.png" /></p>
<p style="text-align: center;"></p>
<p style="text-align: right;"><span style="color: #000000;">Te pareció útil el post , Comenta.</span><img class="size-full wp-image-1198 alignnone" alt="awsm" src="http://gulch.mx/wp-content/uploads/2013/06/awesome.png" width="30" height="30" /></p>