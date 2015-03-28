---
ID: 1555
post_title: Linux Remote Control (lrc)
author: mattdark
post_date: 2014-02-23 04:36:29
post_excerpt:
layout: post
permalink: http://gulch.mx/linux-remote-control/
post_to_facebook_timeline:
  - 1
socialize_text:
  - 
socialize:
  - 1,2,22,24,17,18
fb_fan_page_post_id:
  - 246202975455925_413089435502218
dsq_thread_id:
  - 2307491036
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
<img class="wp-image-1582 aligncenter" src="http://gulch.mx/wp-content/uploads/2014/02/mobile_devices_ubuntu.jpg" alt="Linux Remote Control" width="745" height="418" />
<p style="text-align: justify;"><strong>Linux Remote Control</strong> (lrc) es una aplicación web de código abierto que permite usar cualquier dispositivo (con soporte para HTML5) como control remoto de equipos con GNU/Linux instalado, siempre que estén conectados a la misma red.</p>
<p style="text-align: justify;">lrc está divido en dos partes, cliente (lrc-client) y servidor (lrc-server). lrc-client es la parte de la aplicación que está almacenada en el dispositivo que quieres usar como control remoto. Está desarrollado en HTML5, CSS y Javascript. Es la parte de la aplicación que envía comandos al servidor para ser ejecutados. lrc-server es la parte de la aplicación alojada en el equipo que quieres controlar. Está desarrollado en Node.js y es responsable de ejecutar los comandos recibidos del cliente.</p>
<span style="font-size: medium;"><strong>¿Que puedes hacer con Linux Remote Control?</strong></span>
<ul>
	<li>Controlar la música y el sonido de tu computadora (reproducir, pausar, detener, siguiente, previo, silenciar y volumen).</li>
	<li>Controlar la reproducción de vídeos (reproducir, pausar, siguiente, previo, silenciar, volumen y pantalla completa).</li>
	<li>Controlar el mouse (click y mover).</li>
	<li>Bloquear y desbloquear la pantalla.</li>
	<li>Reiniciar y apagar tu computadora.</li>
	<li>Incrementar y reducir el brillo de la pantalla.</li>
	<li>Controlar las diapositivas de una presentación.</li>
	<li>Enviar comandos para que se ejecuten en tu GNU/Linux.</li>
</ul>
<p style="text-align: center;"><img class=" wp-image-1561 aligncenter" src="http://gulch.mx/wp-content/uploads/2014/02/device.jpg" alt="Linux Remote Control" /></p>
<strong><span style="font-size: medium;">¿Como instalar?</span></strong>

Dependencias:
<ul>
	<li>Node.js</li>
</ul>
<strong>Si usas Debian, Ubuntu o derivados:</strong>
<ol>
	<li>Descarga lrc en tu equipo con GNU/Linux.</li>
</ol>
<pre prompt="$" lang="shell"> wget http://www.linuxremotecontrol.com/lrc.deb</pre>
<ol start="2">
	<li>Instala el paquete.</li>
</ol>
<pre prompt="$" lang="shell"> sudo dpkg -i lrc.deb</pre>
<ol start="3">
	<li>Mueve el directorio <strong>lrc-client</strong> que se encuentra en <strong>/opt</strong> a tu dispositivo. Puede ser a la memoria SD.</li>
</ol>
<pre prompt="$" lang="shell"> sudo mv /opt/lrc-client tu-dispositivo/lrc</pre>
<ol start="4">
	<li>Inicia el servidor Node.js</li>
</ol>
<pre prompt="$" lang="shell"> node /opt/lrc-server/lrc.js</pre>
<ol start="5">
	<li style="text-align: justify;">¡Listo! Abre el archivo <strong>index.html</strong> del directorio <strong>lrc-client</strong> de tu dispositivo en un navegador y usalo.</li>
</ol>
Si usas un dispositivo Firefox OS:
<ol start="3">
	<li>Instala Linux Remote Control desde el Marketplace.</li>
</ol>
<ol start="4">
	<li>¡Listo! Abre la aplicación en tu dispositivo Firefox OS.</li>
</ol>

<hr />

<strong>Si usas otra distribución:</strong>
<ol>
	<li>Descarga lrc en tu equipo con GNU/Linux.</li>
</ol>
<pre prompt="$" lang="shell"> git clone https://github.com/Agneli/linux-remote-control.git</pre>
<ol start="2">
	<li>Mueve el directorio <strong>lrc-client</strong> que se encuentra en <strong>linux-remote-control/</strong><strong>opt</strong> a tu dispositivo. Puede ser a la memoria SD.</li>
</ol>
<pre prompt="$" lang="shell"> sudo mv linux-remote-control/lrc-client tu-dispositivo/lrc</pre>
<ol start="3">
	<li>Inicia el servidor Node.js</li>
</ol>
<pre prompt="$" lang="shell"> node linux-remote-control/lrc-server/lrc.js</pre>
<ol start="4">
	<li>¡Listo! Abre el archivo <strong>index.html</strong> del directorio <strong>lrc-client</strong> de tu dispositivo en un navegador y usalo.</li>
</ol>
Si usas un dispositivo Firefox OS:
<ol start="2">
	<li>Instala Linux Remote Control desde el Marketplace.</li>
</ol>
<ol start="4">
	<li>¡Listo! Abre la aplicación en tu dispositivo Firefox OS.</li>
</ol>
<strong><span style="font-size: medium;">Primeras impresiones</span></strong>
<p style="text-align: justify;">He probado la aplicación en un equipo con Manjaro 0.8.9rc2 y Node.js 0.10.25 como servidor y un Geeksphone Peak con Firefox OS 1.3 como cliente, en general funcionó bien, excepto por algunas funcionalidades que no han ido del todo bien, pese a esto, me parece una herramienta bastante util y muy completa. Existen otras implementaciones con Go y Node.js, pero están enfocadas unicamente al control de presentaciones en HTML5.</p>
<strong>¿Que funcionó?</strong>
<ul>
	<li>Controlar la música y el sonido de tu computadora (VLC).</li>
	<li>Controlar el mouse.</li>
	<li>Reiniciar y apagar tu computadora.</li>
	<li>Incrementar y reducir el brillo de la pantalla.</li>
	<li>Controlar las diapositivas de una presentación.</li>
	<li>Enviar comandos para que se ejecuten en tu GNU/Linux.</li>
</ul>
<strong>¿Que no funcionó?</strong>
<ul>
	<li>Controlar la reproducción de videos.</li>
	<li>Bloquear y desbloquear la pantalla.</li>
</ul>
<h2 style="text-align: center;"><strong><span style="font-size: medium;">Linux Remote Control en Firefox OS</span></strong></h2>
<p style="text-align: center;"><img class="wp-image-1568 aligncenter" src="http://gulch.mx/wp-content/uploads/2014/02/2014-02-23-03-09-15.png" alt="LRC en Firefox OS" width="170" height="300" /><img class="wp-image-1569 aligncenter" src="http://gulch.mx/wp-content/uploads/2014/02/2014-02-23-03-07-20.png" alt="LRC en Firefox OS - Menu" width="170" height="300" /><img class="size-full wp-image-1570 aligncenter" src="http://gulch.mx/wp-content/uploads/2014/02/2014-02-23-03-07-48.png" alt="LRC en Firefox OS - Música" width="170" height="300" /><img class="size-full wp-image-1575 aligncenter" src="http://gulch.mx/wp-content/uploads/2014/02/2014-02-23-03-07-56.png" alt="LRC en Firefox OS - Comandos" width="170" height="300" /><img class=" size-full wp-image-1576 aligncenter" src="http://gulch.mx/wp-content/uploads/2014/02/2014-02-23-03-08-10.png" alt="LRC en Firefox OS - Mouse" width="170" height="300" /><img class=" size-full wp-image-1577 aligncenter" src="http://gulch.mx/wp-content/uploads/2014/02/2014-02-23-03-08-19.png" alt="LRC en Firefox OS - Presentación" width="170" height="300" /></p>
<p style="text-align: center;"><a title="Linux Remote Control" href="http://linuxremotecontrol.com">Convierte cualquier dispositivo en un completo control remoto para tu GNU/Linux</a></p>