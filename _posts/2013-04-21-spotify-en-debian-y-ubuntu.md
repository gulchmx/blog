---
ID: 1128
post_title: Spotify en Debian y Ubuntu
author: hacktotopo
post_date: 2013-04-21 11:40:49
post_excerpt:
layout: post
permalink: >
  http://gulch.mx/spotify-en-debian-y-ubuntu/
socialize_text:
  - 
socialize:
  - 1,2,22,24,17,18
fb_fan_page_post_id:
  - 246202975455925_455876817821872
dsq_thread_id:
  - 1461335658
---
<p style="text-align: justify;"><img class="aligncenter size-full wp-image-1133" alt="spotify" src="http://gulch.mx/wp-content/uploads/2013/04/spotify1.jpg" /></p>
<p style="text-align: justify;"><span style="color: #333333;">Spotify se ha convertido en la plataforma musical más conocida ya que permite escuchar música de manera “legal” por medio de streaming gracias a los acuerdos con las disqueras.</span></p>
<p style="text-align: justify;"><span style="color: #333333;">Existen varias alternativas más económicas, incluso gratuitas (nuvular player o Grooveshark).En México (donde vivo) no tiene mucho su estreno y su popularidad ha aumentado mucho.</span></p>
<p style="text-align: justify;">Spotify  (Mientras escribo este post) solo tiene disponible la aplicación de tipo desktop para Windows y Mac de manera Oficial , se sugiere  que para usarlo en Linux  se instale con Wine ( Lo que veo horrible si se trata de un software de audio) o usar el  Preestreno de Spotify para Linux (versión Beta supongo).</p>
Para ser un Preestreno lo veo bastante bien funcionando en mi Debian Squeeze, para instalarlo hacer lo siguiente.

1.- Añadir el repositorio ( /etc/apt/sources.list ).
<pre class="theme:terminal toolbar-overlay:false lang:sh decode:true" title="Añadir Repositorio">## Spotify
deb http://repository.spotify.com stable non-free</pre>
2.- Añadir la llave Publica.
<pre class="theme:terminal lang:sh decode:true" title="Llave Publica">sudo apt-key adv --keyserver keyserver.ubuntu.com --recv-keys 94558F59</pre>
3.-Actualizar Repositorios.
<pre class="theme:terminal lang:sh decode:true" title="Actualizar Repositorios ">apt-get update</pre>
4.- Instalarlo.
<pre class="theme:terminal lang:sh decode:true" title="Instalar Spotify">apt-get install spotify-client</pre>
<img class="aligncenter size-large wp-image-1132" alt="Spotify desktop hacktotopo" src="http://gulch.mx/wp-content/uploads/2013/04/spotify-700x437.jpg" />

<a title="Fuente:" href="https://www.spotify.com/mx/download">Fuente:</a>