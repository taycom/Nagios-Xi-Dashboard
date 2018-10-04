# Nagios-Xi-Dashboard
Dashboard Dashlets/Smashing for NagiosXI.<br>Proyecto para implantar un dashboard con smashing y extraer la información desde vuestro Nagios XI mediante API.

Las instrucciones de instalación y puesta en producción se han probado en la última versión de Nagios XI disponible durante el 2017.<br>

Para completar correctamente los pasos de configuración en vuestro sistema de monitorización en vuestro caso teneis que remitiros al documento del fabricante : [http://assets.nagios.com/downloads/nagiosxi/docs/Accessing_The_XI_Backend_API.pdf]

Preparación de la base del servicio

- Descargar la última versión del instalado de ruby. 
    #\curl -sSL https://get.rvm.io | bash -s stable --ruby
- Ejecutar el ejecutable para cargarlo en las variables del sistema
- Realizar logout de la sesión y entrar de nuevo al sistema
- Instalar las versiones de ruby necesarias 
    # rvm install 1.9.3
    # rvm install 2.5.1
- Instalar las gemas necesarias 
    # gem install bundler
    # gem install smashing
- Crear un nuevo proyecto para generar los ficheros base
    # smashing nuevo_proyecto
- Entrar en el directory
    # cd nuevo_proyecto
- Editar el fichero "Gemfile" y añadir las siguientes lineas al inicio.
    gem 'smashing'
    gem 'nokogiri'
    require 'open-uri'
- Instalar los paquetes requerido
    # bundle
- Iniciar smashing 
    # smashing start
- Abrir un navegador e introducir http://<ip>:3030


  
