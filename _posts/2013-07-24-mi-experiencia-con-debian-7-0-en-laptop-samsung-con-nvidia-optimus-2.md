---
ID: 1177
post_title: >
  Mi experiencia con Debian 7.0 en laptop
  samsung con Nvidia Optimus
author: Mauricio Vargas
post_date: 2013-07-24 13:13:02
post_excerpt:
layout: post
permalink: >
  http://gulch.mx/mi-experiencia-con-debian-7-0-en-laptop-samsung-con-nvidia-optimus-2/
socialize_text:
  - >
    debian wheezy nvidia optimus laptop
    bumblebee
socialize:
  - 21,1,2,24
fb_fan_page_post_id:
  - 246202975455925_496911560385064
dsq_thread_id:
  - 1527455050
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
<p style="text-align: justify;">A finales del año pasado compré un laptop Samsung NP500p4c -i5 intel- con gráficos Intel integrados y la tarjeta discreta Nvidia 630M con tecnología Optimus.</p>
<p style="text-align: justify;">Al principio me angustié, pues no había soporte oficial para esta tecnología por parte de Nvidia. Mi portátil se calentaba muchísimo pues mientras trabajaba con las tarjeta gráfica intel, quedaba encendida la otra tarjeta -nvidia-. No conocía ninguna opción, la BIOS no permite elegir o desactivar alguna de las dos tarjetas,  pues la tecnología Optimus consiste precisamente en detectar automáticamente los procesos y activar la tarjeta Nvidia y desactivarla automáticamente (en Windows 7 por ejemplo).</p>
<p style="text-align: justify;">Paralelamente me fui desencantando de Ubuntu con sus nuevas funciones de búsqueda que involucran la polémica inclusión de Amazon como destinatario de las palabras puestas en el dash de unity. Sobre todo la privacidad y la tendencia de esta empresa -Canonical-  en alejarse de la comunidad, en particular de la comunidad desarrolladora de Debian, sistema operativo del que se basan para ofrecer sus propuestas.</p>
<p style="text-align: justify;">Probando y experimentando, dí con Crunchbang, una distribución basada en Debian cuya particularidad consiste en ofrecer un escritorio basado en Openbox y tint2  "out of the box" osea  "listo para usarse", que no requiere configuración adicional del usuario, pues ya viene estructurado por defecto.</p>

<h2 style="text-align: center;"><strong>Aquí empieza la guía práctica para quienes tengan una laptop con Nvidia tecnología Optimus.</strong></h2>
<p style="text-align: justify;"><strong>1)</strong> Bajan e instalan la última versión de Crunchbang http://crunchbang.org/download/</p>
<p style="text-align: justify;"><strong>2)</strong>Hay dos opciones, para instalar Bumblebee (Administrador de Optimus y sistemas gráficos híbrido) y los drivers Nvidia: La tradicional es agregar el repositorio (seguir la guía o manual) de http://suwako.nomanga.net/, es decir, los paquetes compilados y distribuidos no oficiales por un usuario.</p>
<p style="text-align: justify;">O pueden probar una opción un poco más reciente, es agregar los <strong>repositorios Oficiales</strong> de Debian Sid -unstable- y hacer un apt pinning.</p>
<p style="text-align: right;">(esta es una guía más detallada: <a href="http://crunchbang.org/forums/viewtopic.php?id=12081">http://crunchbang.org/forums/viewtopic.php?id=12081</a>)</p>
yo simplemente agregué en el archivo...:

sudo -i
Agregar repositorios de Debian Sid -inestable-
<pre class="lang:default decode:true">echo "deb http://http.debian.net/debian sid main contrib non-free" &gt;&gt; /etc/apt/sources.list</pre>
Establecer opciones para instalar paquetes inestables unicamente por petición específica, es decir con la opción -t sid, ejemplo:

#apt-get -t sid install bbswitch-dkms bumblebee bumblebee-nvidia primus
Para esto es necesario editar el archivo /etc/apt/preferences :
<pre class="lang:default decode:true">nano /etc/apt/preferences</pre>
y agrego al final
<pre class="lang:default decode:true">Package: *
Pin: release a=sid
Pin-Priority: 100</pre>
Guardo cambios.

Notese la prioridad, la menor es la de SID y la mayor la de Weezy -estable-, esto establece que primero se instale la versión estable -mayor pin- y se deje la inestable -sid- como última opción o solo por comando específico.

Actualizamos la base de datos
<pre class="lang:default decode:true">apt-get update</pre>
Luego instalamos archivos necesarios del kernel para cargar el módulo bbswitch-dkms, que se encarga de encender o apagar la tarjeta gráfica discreta -nvidia-)
<pre class="lang:default decode:true">apt-get install linux-headers-3.2.0-4-amd64</pre>
Deben cambia la versión -3.2.0-4-amd64 por su versión, ejemplo:
<pre class="lang:default decode:true">apt-get install linux-headers-3.9.0-1-i686-pae</pre>
Luego se instalan los paquetes que manejarán el sistema gráfico, que logrará sacar provecho de la tecnología Optimus o gráficos híbridos (dos tarjetas gráficas).
<pre class="lang:default decode:true">apt-get install -t sid bbswitch-dkms bumblebee bumblebee-nvidia primus</pre>
Si todo salió bien y no hay error, entonces solo queda reiniciar
<pre class="lang:default decode:true">reboot</pre>
Nota importante:

Si agregan los siguientes parámetros en grub, /etc/default/grub :
<pre class="lang:default decode:true">GRUB_CMDLINE_LINUX_DEFAULT="i915.i915_enable_rc6=4 i915.i915_enable_fbc=1 i915.lvds_downclock=1"</pre>
Perderán la función de controlar el brillo de la pantalla -backlight- con las teclas FN+F2, FN+F3 y tampoco tendrán las instancias de control: <strong>/sys/class/backlight/</strong> que contiene los archivos necesarios para administrar el brillo del monitor: <strong>acpi_video0  acpi_video1  intel_backlight</strong>