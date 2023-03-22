# Backup-Driver-Ubuntu

Para hacer una copia de seguridad (backup) de los controladores (drivers) en Ubuntu, puedes seguir los siguientes pasos:

Abre una terminal (Ctrl+Alt+T).

Escribe el siguiente comando para listar todos los controladores instalados en tu sistema:

<code>
dpkg --get-selections | grep -v deinstall | grep xserver-xorg-video </code>
Este comando te mostrará una lista de los controladores instalados para la tarjeta gráfica.

Ahora, para hacer una copia de seguridad de los controladores, crea una carpeta llamada "drivers_backup" en tu carpeta personal. Para hacer esto, ejecuta el siguiente comando:

<code>
mkdir ~/drivers_backup </code>
Para cada controlador que desees hacer backup, ejecuta el siguiente comando en la terminal:

<code>
sudo cp /usr/lib/xorg/modules/drivers/nombre_del_controlador_drv.so ~/drivers_backup/</code>
Donde "nombre_del_controlador" es el nombre del controlador que deseas hacer backup.

Ahora tienes una copia de seguridad de tus controladores en la carpeta "drivers_backup".

Para instalar los controladores en caso de ser necesario, puedes seguir las siguientes instrucciones:

Abre la terminal (Ctrl+Alt+T).

Ejecuta el siguiente comando para actualizar la lista de paquetes:

<code>
sudo apt-get update</code>
Para instalar un controlador específico, ejecuta el siguiente comando:

<code>
sudo apt-get install nombre_del_paquete </code>
Donde "nombre_del_paquete" es el nombre del paquete del controlador que deseas instalar.

Reinicia el sistema para que los cambios surtan efecto.

Espero que esto te ayude a hacer backup e instalar tus controladores en Ubuntu.
