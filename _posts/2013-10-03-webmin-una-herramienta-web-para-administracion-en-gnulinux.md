---
ID: 1440
post_title: >
  Webmin, una herramienta web para
  administración en GNULinux
author: Ismael Garcia (@tuxisma)
post_date: 2013-10-03 14:28:34
post_excerpt:
layout: post
permalink: >
  http://gulch.mx/webmin-una-herramienta-web-para-administracion-en-gnulinux/
socialize_text:
  - 
socialize:
  - 1,2,22,24,17,18
fb_fan_page_post_id:
  - 246202975455925_531012860308267
dsq_thread_id:
  - 1821792050
---
<p style="text-align: justify;"><img class="size-full wp-image-1443 aligncenter" alt="webminlogo" src="http://gulch.mx/wp-content/uploads/2013/10/webminlogo.png" />Webmin es una herramienta de administración en GNULinux,  cuenta con una herramienta vía Web para gestionar diversas acciones sobre el sistema, como es la gestión de cuentas de usuario, además de permitir gestionar las contraseñas, lograr un respaldo de todos los usuarios, en caso de que el sistema se llegue a dañar lo único que se haría es  importar los archivos que se habían exportado desde webmin.</p>
<p style="text-align: justify;">Con Webmin puedes gestionar:</p>

<ul style="text-align: justify;">
	<li>Archivos del sistema.</li>
	<li>Archivos de configuración de los servicios que esta corriendo el servidor.</li>
	<li>Networking.</li>
	<li>Hardware.</li>
	<li>Cluster</li>
</ul>
<p style="text-align: justify;">Para instalarlo:</p>

<ul style="text-align: justify;">
	<li>Descargar el archivo de instalación de la siguiente url ----&gt; <a title="Descargar Webmin" href="http://www.webmin.com/download.html" target="_blank">Webmin</a> (En mi caso usé el archivo .rpm )</li>
	<li>Se instala de la siguiente manera:
<pre class="lang:sh decode:true">rpm -iv /home/tuxisma/Documentos/webmin/webmin-1.650-1.noarch.rpm</pre>
Específica la ruta en donde fue guardado el archivo que se descargó.</li>
	<li>Aparecerá lo siguiente al proceder con la instalación:</li>
</ul>
<pre class="lang:sh decode:true">[root@localhost webmin]# rpm -iv /home/tuxisma/Documentos/webmin/webmin-1.650-1.noarch.rpm 

advertencia:webmin-1.650-1.noarch.rpm: EncabezadoV3 DSA/SHA1 Signature, ID de clave 11f63c51: NOKEY
Preparando paquetes...
Operating system is Fedora Linux
webmin-1.650-1.noarch
Webmin install complete. You can now login to https://localhost:10000/
as root with your root password.</pre>
<ul style="text-align: justify;">
	<li> Acceder al sitio de gestión en el navegador web tal y como se indica durante la instalación,  loguearse como root y la respectiva contraseña:</li>
</ul>
<p style="text-align: justify;"><a href="https://localhost:10000/" target="_blank">https://localhost:10000/</a></p>
<p style="text-align: justify;">Webmin trae una variedad de utilidades, descubre y quedarás sorprendido de lo mucho que puedes hacer con ello.</p>
<img class="wp-image-1441 aligncenter" alt="webmin" src="http://gulch.mx/wp-content/uploads/2013/10/webmin.png" width="744" height="418" />