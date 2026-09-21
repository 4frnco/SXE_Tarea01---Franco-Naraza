# Tarea 01: Instalación de un CMS en un VPS

**Franco Naraza**

## Introducción

En esta práctica se realiza la instalación y configuración de un CMS WordPress en un servidor Ubuntu Server, utilizando una pila LAMP formada por Apache, MariaDB y PHP. La administración del servidor se realiza de forma remota mediante SSH.

## Instalación y configuración de WordPress

A continuación se muestran los pasos realizados durante la instalación y configuración del servidor y de WordPress.

1. Para comenzar la práctica se crea la máquina virtual que funcionará como servidor. En ella se instalará Ubuntu Server y posteriormente todos los servicios necesarios para ejecutar WordPress.

   <p align="center">
   <img src="capturas/1.png" alt="Creación de la máquina virtual">
   <br>
   <em>Creación de la máquina virtual.</em>
   </p>


2. Durante la instalación de Ubuntu Server se configura el perfil del usuario que utilizaremos para administrar el servidor y realizar las diferentes tareas de la práctica.

   <p align="center">
   <img src="capturas/2.png" alt="Configuración del usuario">
   <br>
   <em>Configuración del usuario.</em>
   </p>


3. Una vez terminada la instalación de Ubuntu Server, se comprueba que el servidor está preparado para ser administrado de forma remota desde el equipo anfitrión mediante SSH.

   <p align="center">
   <img src="capturas/3.png" alt="Servidor preparado para SSH">
   <br>
   <em>Servidor preparado para SSH.</em>
   </p>


4. Desde el equipo anfitrión se establece una conexión SSH con la máquina virtual. A partir de este momento, la configuración del servidor se realiza de forma remota desde el ordenador anfitrión.

   <p align="center">
   <img src="capturas/4.png" alt="Conexión mediante SSH">
   <br>
   <em>Conexión mediante SSH.</em>
   </p>


5. Antes de instalar los servicios necesarios, se actualiza la información de los paquetes disponibles en Ubuntu para asegurarnos de trabajar con los repositorios actualizados.

   <p align="center">
   <img src="capturas/5.png" alt="Ejecución de apt update">
   <br>
   <em>Ejecución de apt update.</em>
   </p>


6. Se instalan los diferentes programas necesarios para montar la pila LAMP y ejecutar WordPress. Entre ellos se encuentran Apache como servidor web, MariaDB como sistema de bases de datos y PHP junto con sus módulos.

   <p align="center">
   <img src="capturas/6.png" alt="Instalación de Apache MariaDB y PHP">
   <br>
   <em>Instalación de Apache, MariaDB y PHP.</em>
   </p>


7. Una vez finalizada la instalación, se comprueba que los programas necesarios se han instalado correctamente y que el sistema está preparado para continuar con la configuración.

   <p align="center">
   <img src="capturas/7.png" alt="Programas instalados">
   <br>
   <em>Programas instalados.</em>
   </p>


8. Se consulta el estado del servicio Apache para comprobar que el servidor web se encuentra activo y funcionando correctamente.

   <p align="center">
   <img src="capturas/8.png" alt="Apache activo">
   <br>
   <em>Apache activo.</em>
   </p>


9. Se comprueba el estado del servicio MariaDB, que será utilizado posteriormente para almacenar la información de WordPress.

   <p align="center">
   <img src="capturas/9.png" alt="MariaDB activa">
   <br>
   <em>MariaDB activa.</em>
   </p>


10. Se comprueba la versión de PHP instalada en el servidor para verificar que PHP está disponible y preparado para ejecutar WordPress.

   <p align="center">
   <img src="capturas/10.png" alt="Versión de PHP">
   <br>
   <em>Versión de PHP.</em>
   </p>


11. Se ejecuta la herramienta de configuración segura de MariaDB. En este proceso se eliminan configuraciones y usuarios innecesarios y se aplican diferentes medidas básicas de seguridad.

   <p align="center">
   <img src="capturas/11.png" alt="Seguridad de MariaDB">
   <br>
   <em>Configuración de seguridad de MariaDB.</em>
   </p>


12. Se crea la base de datos que utilizará WordPress y también un usuario específico con permisos sobre ella. De esta forma, WordPress podrá almacenar y consultar su información en MariaDB.

   <p align="center">
   <img src="capturas/12.png" alt="Creación de la base de datos">
   <br>
   <em>Creación de la base de datos.</em>
   </p>


13. Después de crear la base de datos, se utiliza `SHOW DATABASES` para comprobar que la base de datos llamada `wordpress` se ha creado correctamente.

   <p align="center">
   <img src="capturas/13.png" alt="Comprobación de la base de datos">
   <br>
   <em>Comprobación de la base de datos.</em>
   </p>


14. Se prepara la ubicación donde se almacenarán los archivos de WordPress y se descarga el paquete desde la página oficial. Los archivos quedan situados en `/srv/www/wordpress`.

   <p align="center">
   <img src="capturas/14.png" alt="Descarga de WordPress">
   <br>
   <em>Descarga de WordPress.</em>
   </p>


15. Se crea un archivo de configuración para Apache en el que se indica la ubicación de los archivos de WordPress y se permite que Apache pueda servir correctamente el sitio web.

   <p align="center">
   <img src="capturas/15.png" alt="Configuración de Apache">
   <br>
   <em>Configuración de Apache.</em>
   </p>


16. Se activa la configuración creada para WordPress y los módulos necesarios de Apache. También se desactiva la configuración predeterminada para que Apache utilice la configuración de nuestro sitio.

   <p align="center">
   <img src="capturas/16.png" alt="Activación de WordPress en Apache">
   <br>
   <em>Activación de WordPress en Apache.</em>
   </p>


17. Se prepara el archivo `wp-config.php`, que contiene los datos necesarios para que WordPress pueda conectarse con la base de datos MariaDB creada anteriormente.

   <p align="center">
   <img src="capturas/17.png" alt="Configuración de wp-config.php">
   <br>
   <em>Configuración de wp-config.php.</em>
   </p>


18. Dentro del archivo se introducen los datos de conexión correspondientes a la base de datos, el usuario y la contraseña creados anteriormente. Después se guarda la configuración.

   <p align="center">
   <img src="capturas/18.png" alt="Datos de conexión configurados">
   <br>
   <em>Datos de conexión configurados.</em>
   </p>


19. Una vez configurado el servidor, se accede desde el navegador del equipo anfitrión utilizando la dirección IP de la máquina virtual. Esto permite comprobar que WordPress está disponible desde el navegador.

   <p align="center">
   <img src="capturas/19.png" alt="Acceso a WordPress">
   <br>
   <em>Acceso a WordPress.</em>
   </p>


20. En el instalador web de WordPress se completan los datos iniciales del sitio, como el título, el usuario administrador y la contraseña que se utilizará para acceder al panel de administración.

   <p align="center">
   <img src="capturas/20.png" alt="Configuración inicial">
   <br>
   <em>Configuración inicial de WordPress.</em>
   </p>

21. Finalmente, WordPress muestra que la instalación se ha completado correctamente. A partir de este momento el sitio ya está instalado y listo para ser utilizado.

   <p align="center">
   <img src="capturas/21.png" alt="WordPress instalado">
   <br>
   <em>WordPress instalado correctamente.</em>
   </p>


## Bibliografía

- [Ubuntu – Install and configure WordPress](https://ubuntu.com/tutorials/install-and-configure-wordpress)
- [Ubuntu – OpenSSH Server](https://ubuntu.com/server/docs/how-to/security/openssh-server/)
- [Apache HTTP Server – Virtual Hosts](https://httpd.apache.org/docs/2.4/vhosts/)
- [WordPress – Installation FAQ](https://wordpress.org/documentation/article/faq-installation/)
- [MariaDB – CREATE DATABASE](https://mariadb.com/docs/server/reference/sql-statements/data-definition/create/create-database)

### Prompt importante utilizado en Chatgpt

> He instalado Apache y WordPress en mi Ubuntu Server. WordPress está situado en `/srv/www/wordpress`, pero al introducir la IP del servidor en el navegador aparece la página predeterminada de Apache en lugar de WordPress. He creado `wordpress.conf` en `/etc/apache2/sites-available/`. Explícame qué puede estar ocurriendo y qué comandos debo ejecutar para activar la configuración de WordPress, desactivar `000-default.conf` y recargar Apache. También dime cómo comprobar que la configuración no tiene errores.