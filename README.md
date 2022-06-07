# Práctica 4: Maquinas Virtuales 
## **Primer Paso:**  
Irnos al [portal.azure.com](https://portal.azure.com), después de ello buscamos en el Marketplace máquina virtual, para después crear MV (Máquina Virtual)

![Marketplace](https://github.com/aldodanielle/p5_Maquinas_virtuales/blob/main/Imagenes/1.png)
----------------------------------------------------------------------------------------------
## **Paso 2:**  

Seleccionamos crear y nos despliega una lista de maquinas que se pueden crear, para este ejemplo seleccionamos la primera opción de Maquina Virtual de Azure hospedad por Azure, después de ello nos mandara a crear la máquina.  

![Maquina virtual de Azure](https://github.com/aldodanielle/p5_Maquinas_virtuales/blob/main/Imagenes/2.png)

----------------------------------------------------------------------------------------------
## **Paso 3:**

Nos despliega como el que a continuación se despliega los cuales son básicamente los básicos para crear un recurso o proyecto como el tipo de suscripción, el grupo de recursos, la región de donde queremos que encuentre la MV y el nombre de la Maquina Virtual. Como también podemos observar nos salen otras 2 opciones en donde podemos elegir el tipo de seguridad así mismo como el tipo de imagen (ISO) que va a tener la maquina para este ejemplo elegimos la imagen en Windows 10 pro versión 21H2-Ge2.  

![Creacion de maquina virual](https://github.com/aldodanielle/p5_Maquinas_virtuales/blob/main/Imagenes/3.png)
----------------------------------------------------------------------------------------------
## **Paso 4:**

Pasamos a la siguiente parte para continuar con nuestra maquina en donde elegimos el tipo de tamaño así mismo como un usuario y contraseña para la misma maquina y solo le daremos revisar y crear, y tendremos que esperara que se cree la maquina  

![User and pass](https://github.com/aldodanielle/p5_Maquinas_virtuales/blob/main/Imagenes/4.png)
----------------------------------------------------------------------------------------------
## **Paso 5:**  

Cuando se terminé de crear la maquina nos que se completó la implementación como se muestra en la siguiente imagen, el siguiente paso será hacer otra MV con las mimas características a esta que se acaba de crear   

![se completo la implementacio](https://github.com/aldodanielle/p5_Maquinas_virtuales/blob/main/Imagenes/5.png)
----------------------------------------------------------------------------------------------
## **Paso 6:**

Al igual la maquina anterior tendrá las misma característica que la anterior y solo se diferenciara por el nombre, sin embrago esta nueva máquina antes de crearla le realizaremos una modificación en el apartado de redes y puesto que tenemos que asegurarlos que las dos maquinas estén en la misma red vital que por defecto se encontraran con el nombre de grupo de recursos que colocamos agregando un -vnet que por defecto se coloca solo y solo tendríamos que verificar que si estén las dos maquinas en la misma red virtual antes de darle en el botón de revisar y crear.  

![secod MV](https://github.com/aldodanielle/p5_Maquinas_virtuales/blob/main/Imagenes/6.png)
----------------------------------------------------------------------------------------------
## **Paso 7:**

Y si observamos en nuestros recursos recientes podemos ver las dos maquina virtuales con los nombres de seccion4-mv1 y seccion4-vm2 y de la misma manera podemos ingresar al grupo de recursos y estarán las dos máquinas ahí y como se muestra en la segunda imagen.  

![recurces](https://github.com/aldodanielle/p5_Maquinas_virtuales/blob/main/Imagenes/7.png)
![MV creadas](https://github.com/aldodanielle/p5_Maquinas_virtuales/blob/main/Imagenes/8.png)
----------------------------------------------------------------------------------------------
## **Paso 8:**  

Una vez ya teniendo nuestras dos MV entramos a un maquina virtual y seleccionamos el botón de conectar con RDP nos mandara una pantalla como se muestra a continuación y lo único que tendríamos que hacer seria descargar el archivo RDP en nuestra computadora.
Y para poder acceder a un escritorio remoto de Azure en necesitamos un programa en el escritorio para su acceso en el caso de Windows el programa lleva por nombre [Escritorio Remoto de Microsoft](https://apps.microsoft.com/store/detail/escritorio-remoto-demicrosoft/9WZDNCRFJ3PS?hl=es-mx&gl=MX) el cual se puede encontrar en su tienda de aplicaciones.  

![RDP](https://github.com/aldodanielle/p5_Maquinas_virtuales/blob/main/Imagenes/9.png)
----------------------------------------------------------------------------------------------
## **Paso 9:**
Una descargado el archivo RDP y el programa para acceso remoto, el siguiente paso sería abrir el archivo con el programa se acceso remoto, una vez ejecutado este nos pedirá el nombre de usuario y contraseña que le dimos a la máquina virtual para acceder a ella, los ingresamos y le damos los permisos que nos pide y nos tendría que arrogar la interfaz como se muestra en la siguiente imagen ya con nuestro sistema totalmente cargado.  

![VM corriendo](https://github.com/aldodanielle/p5_Maquinas_virtuales/blob/main/Imagenes/10.png)
----------------------------------------------------------------------------------------------
## **Paso 10:**

Después verificamos que nuestros dos equipos virtuales estén conectados entres si para ello necesitamos ir a dispositivos conectados y ver que los dos se encuentre ahí como se muestra a continuación.  

![misma red](https://github.com/aldodanielle/p5_Maquinas_virtuales/blob/main/Imagenes/11.png)
----------------------------------------------------------------------------------------------
## **Paso 11:**  

Una vez comprobado que las dos está conectada entre y en la misma red realizamos in ping con la IP del otro equipo por medio del CMD si este no se realiza abrimos la PowerShell y ejecutamos el siguiente comando “New-NetFirewallRule -DisplayName "Allow ICMPv4-In" -Protocol ICMPv4 “ y este comandando nos podrá permitir abrir la maquina virtual dentro la misma maquina virtual.  

![PowerShell](https://github.com/aldodanielle/p5_Maquinas_virtuales/blob/main/Imagenes/12.png)
----------------------------------------------------------------------------------------------
## **Paso 12:**

Por ultimo ejecutamos el siguiente comando en la PowerShell mstsc  /v:10.0.0.5 para abrir la máquina virtual en otra máquina virtual, este último número del comandado es la IP de la máquina virtual número 2.  

![MV dentro de MV](https://github.com/aldodanielle/p5_Maquinas_virtuales/blob/main/Imagenes/13.png)
----------------------------------------------------------------------------------------------
