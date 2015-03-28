---
ID: 1176
post_title: >
  Mi experiencia con Debian 7.0 en laptop
  samsung con Nvidia Optimus
author: Mauricio Vargas
post_date: 2013-05-21 21:22:01
post_excerpt:
layout: post
permalink: >
  http://gulch.mx/mi-experiencia-con-debian-7-0-en-laptop-samsung-con-nvidia-optimus/
socialize_text:
  - 
socialize:
  - 1,2,22,24,17,18
fb_fan_page_post_id:
  - 246202975455925_468360279906859
dsq_thread_id:
  - 1459839881
---
<p style="text-align: justify;">A finales del año pasado compré un laptop Samsung NP500p4c -i5 intel- con gráficos Intel integrados u la tarjeta discreta Nvidia 630M con tecnología Optimus.</p>
<p style="text-align: justify;">Al principio me angustié, pues no hay soporte oficial para esta tecnología por parte de Nvidia. Mi portátil se calentaba muchísimo pues mientras trabajaba con las tarjeta gráfica intel, debaja encendida la otra tarjeta -nvidia-. No conocía ninguna opción, la BIOS no permitía elegir o desactivar alguna de las dos tarjetas,  pues la tecnología Optimus consiste precisamente en detectar automáticamente los procesos y activar la tarjeta Nvidia y desactivarla automáticamente (en Windows 7 por ejemplo).</p>
<p style="text-align: justify;">Paralelamente me fui desencantando de Ubuntu con sus nuevas funciones de búsqueda que involucran la polémica inclusión de Amazon como destinatario de las palabras puestas en el dash de unity. Sobre todo la privacidad y la tendencia de esta empresa -Canonical-  en alejarse de la comunidad, en particular de la comunidad desarrolladora de Debian, sistema operativo del que se basan para ofrecer su propuesta.</p>
<p style="text-align: justify;">Probando y experimentando, dí con Crunchbang, una distribución basada en Debian cuya particularidad consiste en ofrecer un escritorio basado en Openbox y tint2  "out of the box" que traduce algo así como: listo para usarse, es decir no requiere configuración adicional del usuario, pues ya viene estructurado por defecto.</p>
<p style="text-align: justify;">Aquí empieza la guía práctica para quienes tengan una laptop con Nvidia tecnología Optimus.</p>
<p style="text-align: justify;">1) Bajan e instalan la última versión de Crunchbang <a href="http://crunchbang.org/download/" target="_blank">http://crunchbang.org/download/</a></p>
<p style="text-align: justify;">2)Hay dos opciones, para instalar Bumblebee (Administrador de Optimus y sistemas gráficos híbrido) y los drivers Nvidia: La tradicional es agregar el repositorio (seguir la guía o manual) de <a href="http://suwako.nomanga.net/" target="_blank">http://suwako.nomanga.net/</a>, es decir, los paquetes compilados y distribuidos no oficiales por un usuario.
O pueden probar una opción un poco más reciente, es agregar los repositorios de Debian Sid -unstable- y hacer un apt pinning,  es decir, instalar bbswitch-dkms bumblebee bumblebee-nvidia primus , desde el servidor oficial de debian.
esta es una guía más detallada:<a href="http://crunchbang.org/forums/viewtopic.php?id=12081" target="_blank"> http://crunchbang.org/forums/viewtopic.php?id=12081</a></p>
<p style="text-align: justify;">yo simplemente agregué en el archivo:
#sudo -i
Agregar repositorios de Debian Sid -inestable-
#echo "deb http://http.debian.net/debian sid main contrib non-free" &gt;&gt; /etc/apt/sources.list
Establecer opciones para instalar paquetes inestables unicamente por petición específica, es decir con la opción -t sid, ejemplo:
#apt-get<strong> -t sid</strong> install bbswitch-dkms bumblebee bumblebee-nvidia primus
Para esto es necesario editar el archivo<strong> /etc/apt/preferences </strong>:
#nano /etc/apt/preferences
y agrego al final</p>
<p style="text-align: justify;">Package: *
Pin: release a=sid
Pin-Priority: 100</p>
<p style="text-align: justify;">guardo cambios.
Notece la prioridad, la menor es la de SID y la mayor la de Weezy -estable-, esto establece que primero se instale la versión estable -mayor pin- y se deje la inestable -sid- como última opción o solo por comando específico.</p>
<p style="text-align: justify;">Actualizamos la base de datos
#apt-get update
Luego instalamos archivos necesarios del kernel para cargar el módulo bbswitch-dkms, que se encarga de encender o apagar la tarjeta gráfica discreta -nvidia-)
#apt-get install linux-headers-3.2.0-4-amd64
Deben cambia la versión -3.2.0-4-amd64 por su versión, ejemplo:
#apt-get install linux-headers-3.9.0-1-i686-pae
Luego se instalan los paquetes que manejarán el sistema gráfico, que logrará sacar provecho de la tecnología Optimus o gráficos híbridos (dos tarjetas gráficas).
#apt-get install -t sid bbswitch-dkms bumblebee bumblebee-nvidia primus
Si todo salió bien y no hay error, entonces solo queda reiniciar
#reboot</p>