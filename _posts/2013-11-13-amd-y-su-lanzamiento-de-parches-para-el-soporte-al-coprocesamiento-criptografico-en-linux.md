---
ID: 1504
post_title: >
  AMD y su lanzamiento de parches para el
  soporte al coprocesamiento
  criptográfico en GNU/Linux
author: Ismael Garcia (@tuxisma)
post_date: 2013-11-13 09:56:47
post_excerpt:
layout: post
permalink: >
  http://gulch.mx/amd-y-su-lanzamiento-de-parches-para-el-soporte-al-coprocesamiento-criptografico-en-linux/
socialize_text:
  - 
socialize:
  - 1,2,22,24,17,18
fb_fan_page_post_id:
  - 246202975455925_550423005033919
dsq_thread_id:
  - 1962930978
---
<img class=" wp-image-1506 aligncenter" alt="AMD-Linux" src="http://gulch.mx/wp-content/uploads/2013/11/AMD-Linux.jpg" width="343" height="343" />
<p style="text-align: justify;">AMD ha publicado parches con la finalidad de dar soporte al coprocesamiento criptográfico en GNU/Linux.</p>
<p style="text-align: justify;">AMD CCP (AMD Cryptograph Coprocessor) brindará soporte para la encriptación de hardware, de igual manera otros procesos de cifrado-hashing en GNU/Linux. Los nuevos drivers AMD CCP soportan las interfaces  AES Crypto API, AES CMAC crypto, XTS-AES crypto y SHA.</p>
<p style="text-align: justify;">Tom Lendacky publicó diez parches en total y tomó como base el kernel linux 3.12, en la descripción mediante Kconfig  se interpreta lo siguiente:</p>
<p style="text-align: justify;">"Soporte para usar el API criptográfico con el coprocesador criptográfico de AMD. Este módulo soporta aceleración y descargas de algoritmo SHA y AES".</p>
<p style="text-align: justify;">Se espera que en el APU13 se revelen muchos más funcionalidades, el evento se llevará acabo en esta semana.</p>
<p style="text-align: justify;">Fuente: <a href="http://lkml.indiana.edu/hypermail/linux/kernel/1311.1/02158.html" target="_blank">Anuncio Oficial.</a></p>