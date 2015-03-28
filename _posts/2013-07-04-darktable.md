---
ID: 1247
post_title: darktable
author: Ismael Garcia (@tuxisma)
post_date: 2013-07-04 13:01:52
post_excerpt:
layout: post
permalink: http://gulch.mx/darktable/
socialize_text:
  - 
socialize:
  - 1,2,22,24,17,18
fb_fan_page_post_id:
  - 246202975455925_487333014676252
dsq_thread_id:
  - 1467096146
---
<p style="text-align: justify;">darktable es una aplicación de código abierto para la gestión de fotografías en formato <a href="http://es.wikipedia.org/wiki/RAW_%28formato%29" target="_blank">raw</a>. No funciona como un editor de gráficos rasterizados ( Adobe Photoshop o GIMP), trabaja con una variedad de herramientas enfocadas al procesamiento y postproducción de imágenes raw no destructivo y enfocado principalmente a mejorar el proceso de trabajo del fotógrafo.</p>
<p style="text-align: justify;">Está disponible de manera libre para las principales distribuciones GNU/Linux, OS X y Solaris, distribuido bajo la licencia GPL en su versión 3 o posterior.
En fedora lo puedes instalar de está manera:</p>

<pre class="lang:sh decode:true">yum -y install darktable</pre>
<p style="text-align: justify;">Para recibir las actualizaciones  puedes agregar el siguiente repositorio en la  ruta ( /etc/yum.repos.d/ ) :</p>
<p style="text-align: justify;">Copias las líneas que aparecen en el <strong>repositori<strong>o-darktable  </strong></strong>( lo encuentras al final de este párrafo)<strong><strong> </strong> </strong>y con privilegios de superusuario creas un archivo .repo con nombre:  dt-nightly.repo,  desde consola puedes usar vim /etc/yum.repos.d/dt-nightly.repo , posteriormente pegas las líneas que antes copiaste y presionas Esc , despues tecleas  :wq!  para guardar los cambios en vim, y listo! ya tienes darktable instalado. :)</p>
<strong>repositorio-darktable</strong>
<pre class="lang:sh decode:true">[darktable-nightly]
name=nightly builds of darktable
baseurl=http://dt-nightly.hamsterkollektivet.se/fedora/$releasever/$basearch/packages/
enabled=1
gpgcheck=0

[darktable-nightly-source]
name=nightly builds of darktable - source
baseurl=http://dt-nightly.hamsterkollektivet.se/fedora/$releasever/$basearch/srpms/
enabled=0
gpgcheck=0

[darktable-nightly-debuginfo]
name=nightly builds of darktable - debuginfo
baseurl=http://dt-nightly.hamsterkollektivet.se/fedora/$releasever/$basearch/debug/
enabled=0
gpgcheck=0</pre>
Capturas de pantalla:
Interfaz de Usuario
Imagen 1;
<img alt="" src="http://www.darktable.org/usermanual/images/lighttable_view.jpg" />
Tira de película:
Imagen 2:
<img alt="" src="http://www.darktable.org/usermanual/images/overview/filmstrip.jpg" />
Las imágenes son autoria de <a href="http://www.darktable.org/" target="_blank">http://www.darktable.org/</a>