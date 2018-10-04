# Nagios-Xi-Dashboard
Dashboard Dashlets/Smashing for NagiosXI.<br>
Proyecto para implantar un dashboard con smashing y extraer la información desde vuestro Nagios XI mediante API.

Las instrucciones de instalación y puesta en producción se han probado en la última versión de Nagios XI disponible durante el 2017.<br>

Para completar correctamente los pasos de configuración en vuestro sistema de monitorización en vuestro caso teneis que remitiros al documento del fabricante : [http://assets.nagios.com/downloads/nagiosxi/docs/Accessing_The_XI_Backend_API.pdf]

<h2>Preparación</h2>

- Descargar la última versión del instalado de ruby.<br>
<code>#\curl -sSL https://get.rvm.io | bash -s stable --ruby</code>
- Ejecutar el ejecutable para cargarlo en las variables del sistema
- Realizar logout de la sesión y entrar de nuevo al sistema
- Instalar las versiones de ruby necesarias<br>
<code># rvm install 1.9.3</code><br>
<code># rvm install 2.5.1</code>
- Instalar las gemas necesarias<br> 
<code># gem install bundler</code><br>
<code># gem install smashing</code>
- Crear un nuevo proyecto para generar los ficheros base<br>
<code># smashing nuevo_proyecto</code><br>
- Entrar en el directory<br>
<code># cd nuevo_proyecto</code><br>
- Editar el fichero "Gemfile" y añadir las siguientes lineas al inicio.<br>
<code>gem 'smashing'</code>
<code>gem 'nokogiri'</code>
<code>require 'open-uri'</code><br>
- Instalar los paquetes requerido<br>
<code># bundle</code><br>
- Iniciar smashing<p> 
<code># smashing start</code>
- Abrir un navegador e introducir http://<ip>:3030
<p>
<br>
<h2>Instalación de los ficheros</h2> 

Una vez descargado los ficheros y descomprimidos situaremos todos los ficheros en cada uno de las carpetas que ha generado nuestro proyecto con la misma estructura.<br>

<code># cp -r <ruta_de_la_descarga>/nagios-dashboard/* <ruta_de_tu_proyecto>/*</code>
  
Volveremos a entrar dentro de nuestro proyecto y ejecutaremos nuevamente smashing
<code>smashing start</code>
<p>
<h2>Tips</h2>
Podemos lanzar el proceso de smashing en background utilizando nohub para el proposito. Descargaremos el paquete si fuera necesario.<br>
<code>yum install nohup</code><br>
Y lanzaremos smashing con nohub
<code>nohub smashing start &</code>



  
