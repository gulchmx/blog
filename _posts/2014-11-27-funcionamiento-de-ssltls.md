---
ID: 1825
post_title: Funcionamiento de protocolo SSL/TLS
author: Ismael Garcia (@tuxisma)
post_date: 2014-11-27 16:05:23
post_excerpt:
layout: post
permalink: >
  http://gulch.mx/funcionamiento-de-ssltls/
post_to_facebook_page:
  - 1
fb_fan_page_message:
  - Funcionamiento de protocolo SSL/TLS
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
dsq_thread_id:
  - 3269071792
---
<p style="text-align: justify;">SSL y TLS son protocolos criptográficos que ayudan a proteger la capa de transporte en la comunicación entre el cliente y el servidor en una red, por lo general Internet.</p>
<p style="text-align: justify;">SSL se desarrolló en los 90, fue desarrollado inicialmente por Netscape, la versión 1.0 no se publicó por su inestabilidad, la versión 2.0 salió  a la luz pública en febrero de 1995 pero continuaba con fallas de seguridad,  esto llevó a que se desarrollara la versión 3.0 presentada en 1996,  que presumía de ser estable y bastante confiable.</p>
<p style="text-align: justify;">TLS surge a partir de la vulnerabilidad que se descubrió  a SSL en su versión 3.0, a las mejoras se le denomina SSL/TLS haciendo hincapie en que SSL/TLS está basado en SSL 3.0. Actualmente SSL/TLS se encuentra en su versión 1.2 estable y en borrador la versión 1.3.</p>
<p style="text-align: justify;">Un ejemplo mediante el cual se nota el funcionamiento del protocolo SSL/TLS es visitando un sitio web usando https, suponinedo visitar el sitio facebook  ( https://www.facebook.com ), se observa un candado antes de la url:</p>
<p style="text-align: center;"><img class=" size-full wp-image-1847 aligncenter" src="http://gulch.mx/wp-content/uploads/2014/11/ssl.png" alt="Url SSL" width="259" height="47" /></p>
&nbsp;
<h5><strong>Así funciona SSL/TLS :</strong></h5>
<p style="text-align: center;"><img class=" size-full wp-image-1845 aligncenter" src="http://gulch.mx/wp-content/uploads/2014/11/Cliente-Servidor.png" alt="Modelo Cliente Servidor" width="718" height="410" /></p>
&nbsp;
<p style="text-align: justify;"><strong>1.-</strong> El navegador envía versión de protocolo SSL/TLS que soporta y otros parámetros para lograr la conexión.</p>
<p style="text-align: justify;"><strong>2.-</strong> El servidor recibe la solicitud , junto con ello la información que es proporcionada por el navegador del cliente, después responde con un certificado que se envía hacia el cliente para informar que es un sitio seguro y que el servidor está dispuesto a establecer una conexión segura.</p>
<p style="text-align: justify;"><strong>3.-</strong> El navegador web (cliente) comprueba el certificado , descifrando la firma digital  incluida en el certificado que se ha recibido por el servidor, mediante una llave pública que es generado por una A.C. (Autoridad Certificadora) de parte del servidor, todo esto se hace comparando la llave pública de la A.C. con la firma generada en ese momento , si son iguales el certificado es válido.</p>
<p style="text-align: justify;"><strong>4.-</strong> El navegador confia plenamente en el sitio e inician una comunicación cifrada.</p>
&nbsp;