---
ID: 1312
post_title: >
  Whatsapp vía Pidgin en Archlinux y
  derivados
author: mattdark
post_date: 2013-07-26 18:10:14
post_excerpt:
layout: post
permalink: >
  http://gulch.mx/whatsapp-via-pidgin-en-archlinux-y-derivados/
socialize_text:
  - 
socialize:
  - 1,2,22,24,17,18
fb_author_post_id:
  - 100004034954197_305972969547199
fb_fan_page_post_id:
  - 246202975455925_498010030275217
dsq_thread_id:
  - 1535755131
---
<img class="aligncenter size-large wp-image-1314" alt="WhatsApp" src="http://gulch.mx/wp-content/uploads/2013/07/whatsapp-700x341.jpg" />
<p style="text-align: justify;">WhatsApp es una aplicación de mensajería multiplataforma disponible para  IPhone, Blackberry, Windows Phone, Android y Nokia, muy popular en estos días y cuyo número de adeptos ha superado los 250 millones. Pero, con plataformas emergentes como Firefox OS (recomendado), recien lanzado en España y Polonia; Ubuntu Edge, primer smartphone con Ubuntu for phones que Canonical busca lanzar al mercado; Jolla, un smartphone con Sailfish OS (derivado del proyecto Meego) y que además es compatible con aplicaciones Android; esperemos pronto ver clientes oficiales o en el mejor de los casos que los desarrolladores apuesten por crear alternativas, como sucede con Open WhatsApp, cliente de WhatsApp para Blackberry Z10, Blackberry Q10 y Nokia N9 (smartphone con Meego).</p>
<p style="text-align: justify;">Sin embargo, pese al exito de esta aplicación y otras similares como Line o WeChat, aún hay muchas personas que por diferentes razones no usan estos servicios, como no tener un smartphone, para ellos una excelente noticia y es por eso que escribo este artículo. Pueden usar WhatsApp desde su equipo con GNU/Linux, sin necesidad de instalar el SDK de Android para emularlo e instalar la aplicación. Y la solución es Pidgin, el cual con una librería puede funcionar como cliente de Whatsapp en GNU/Linux.</p>
<p style="text-align: justify;">Lo siguiente lo he probado en Manjaro, una distro basada en Archlinux, pero no dudo que funcione en cualquier otra distribución. Para empezar, instalamos Yowsup, una librería escrita en Python que nos permite usar Whatsapp y es la que usaremos para registrarnos:</p>

<pre id="terminal">  yaourt -S python2-yowsup-git python2-argparse yowsup-client-git</pre>
Ya que hemos instalado Yowsup, creamos el archivo de configuración con la información de nuestro número de celuar:
<pre id="terminal">  nano ~/my_whatsapp_config.txt</pre>
<pre class="lang:default decode:true">cc=20  #replace with your country code
phone=123456789  #replace with your phone number
id=FF:FF:FF:FF:FF:FF  #IMEI or MAC address for iOS
password=PASSWORD #your account's real password. If you don't know it just leave it blank until you do.</pre>
<p style="text-align: justify;">Donde cc es codigo de país, phone es nuestro número de celular con codigo de país, id es el IMEI de nuestro celular, aunque no es necesario modificar este valor, password es la contraseña que nos asigna WhatsApp al registrarnos, por lo que de momento dejamos este campo vacío. Ya que hemos colocado nuestra información, solicitamos código de registro:</p>

<pre id="terminal"> yowsup-cli -c ~/my_whatsapp_config.txt --requestcode sms</pre>
Nota: Si aparece lo siguiente cuando intentan solicitar el código de registro

<img class="aligncenter size-full wp-image-1328" alt="Error Yowsup" src="http://gulch.mx/wp-content/uploads/2013/07/error.png" />
<p style="text-align: justify;">soliciten el código en esta página: <a title="Solicitar código de registro WhatsApp" href="http://whitesoft.dyndns.org:2222/whatsapp_sms">http://whitesoft.dyndns.org:2222/whatsapp_sms</a></p>
<img class="aligncenter size-full wp-image-1327" alt="Código de WhatsApp" src="http://gulch.mx/wp-content/uploads/2013/07/whatsappcode.png" />
<p style="text-align: justify;">Colocan su número con código de país. Ejemplo, si están en México y su número es 123456789, quedaría como se ve en la imagen, los valores de MCC y MNC quedan igual. Esperamos a recibir en nuestro celular el código de registro. Ya que tenemos el código, solicitamos la contraseña con la que iniciaremos sesión en WhatsApp:</p>

<pre id="terminal"> yowsup-cli -c ~/my_whatsapp_config.txt --register XXXXXX</pre>
Donde reemplazamos las X por el código recibido. Y esperamos a que nos devuelva la contraseña.
<p style="text-align: justify;">Por ultimo nos asegurarnos de tener instalado Pidgin, sino desde la terminal hacemos lo siguiente:</p>

<pre id="terminal">  sudo pacman -S pidgin</pre>
<p style="text-align: justify;">En seguida instalamos la librería que ocuparemos para conectarnos a WhatsApp desde Pidgin:</p>

<pre id="terminal">  yaourt -S purple-whatsapp-git</pre>
<p style="text-align: justify;">Estamos listos. Ahora creamos una cuenta en Pidgin. En nombre de usuario colocamos nuestro número de celular, por ejemplo, si estamos en México y el número es 123456789, nuestro usuario sería como sigue y por último colocamos la contraseña obtenida.</p>
<img class="aligncenter size-full wp-image-1322" alt="WhatsApp en Pidgin" src="http://gulch.mx/wp-content/uploads/2013/07/cuenta.png" />
<p style="text-align: justify;">Hemos terminado. A disfrutar. Cualquier pregunta tengas sobre el procedimiento, no olvides dejar tus comentarios aquí. Nos vemos en el próximo artículo.</p>