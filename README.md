# Nagios-Xi-Dashboard
Dashboard Dashlets/Smashing for NagiosXI.<br>Proyecto para implantar un dashboard con smashing y extraer la información desde vuestro Nagios XI mediante API.

Las instrucciones de instalación y puesta en producción se han probado en la última versión de Nagios XI disponible durante el 2017.<br>

Para completar correctamente los pasos de configuración en vuestro sistema de monitorización en vuestro caso teneis que remitiros al documento del fabricante : [http://assets.nagios.com/downloads/nagiosxi/docs/Accessing_The_XI_Backend_API.pdf]

Preparación de la base del servicio

- Descargar la última versión del instalado de ruby.<br>
<code>#\curl -sSL https://get.rvm.io | bash -s stable --ruby</code>
- Ejecutar el ejecutable para cargarlo en las variables del sistema
- Realizar logout de la sesión y entrar de nuevo al sistema
- Instalar las versiones de ruby necesarias 
<code># rvm install 1.9.3</code>
<code># rvm install 2.5.1</code>
- Instalar las gemas necesarias 
<code># gem install bundler</code>
<code># gem install smashing</code>
- Crear un nuevo proyecto para generar los ficheros base
<code># smashing nuevo_proyecto</code>
- Entrar en el directory
<code># cd nuevo_proyecto</code>
- Editar el fichero "Gemfile" y añadir las siguientes lineas al inicio.
<code>gem 'smashing'</code>
<code>gem 'nokogiri'</code>
<code>require 'open-uri'</code>
- Instalar los paquetes requerido
<code># bundle</code>
- Iniciar smashing 
<code># smashing start</code>
- Abrir un navegador e introducir http://<ip>:3030


  
