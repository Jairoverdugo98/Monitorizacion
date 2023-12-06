# Herramientas propias del sistemas

A continuación podremos ver algunos de los comandos más útiles para monitorizar el sistema.

## 1. TOP 
Top es un comando que proporciona una vista de los procesos en ejecución como por ejemplo la carga del sistema , la memoria utilizada y los procesos activos.

## Opciones:
- top -d : Especifica el intervalo de actualización en segundos

- top -u : Filtra los procesos por usuario

- top -p : Muestra los procesos con IDs

- Shift + E: Cambia la unidad de medida de CPU a porcentaje de tiempo en lugar por núcleo

- Shift + M: Ordena la lista de procesos por uso de memoria

- Shift + P : Ordena la lista de procesos por uso de CPU

![image](/img/top.png)


## 2. Atop
Es un comando que nos muestra información detallada sobre los recursos del sistema y los procesos en ejecuación.
Puedes instalar atop en Debian/Ubuntu utilizando: **apt install atop**

## Opciones:
- atop -a : Muestra la actividad de todos los procesos, aunque no esten activos
- atop -d : Cambia el intervalo de actualización
- atop -n : Especifica el número de actualizaciones antes de salir
- atop -u : Filtra los procesos por usuario

- C : Cambia la visualización de procesos

- D : Cambia la visualizacion de discos

- N : Cambia la visualización de red

- Q : Sale de la aplicacion 

![image](/img/atop.png)

## 3.Htop
Htop es un comando que nos muestra una versión mejorada del comando top , con una interfaz mas sencilla que contiene funciones adicionales

## Opciones
- F2 : Abre el menú de configuración

- F4 : Filtra los procesos por usuario

- F5 : Ordena la lista de procesos por criterios

- F9 : Abre el menú de señales para enviarlas a los procesos

- F10 : Sale de htop

![image](/img/htop.png)


## 4. Comandos para la Monitorización de Procesos
- Ps : Muestra una lista de procesos en ejecución

- Ps Aux : Lista todos los procesos en ejecución detalladamente.

- Free -m : Muestra la utilización de memoria.

- Df -h : Muestra el uso del disco.

- Netstat -i : Muestra estadísticas de red

## 5. Comandos para Discos y Redes

- **Iostat** : Se utiliza para monitorizar el rendimiento del sistema y los dispositivos de entrada y salida
Para utilizar este comando debes instalarlo previamente utilizando:
**"sudo apt install sysstat"**

  **Ejemplo: iostat sda 5 3 >io.out &**
  
    Este ejemplo da información de este disco , cada 5 segundos , 3 veces y lo redirecciona a io.out en segundo plano.


- **Tcpdump** : Es una herramienta de lína de comandos que permite capturar y mostrar el tráfico de red en tiempo real. 
Opciones de tcpdump:
- n : No realiza la resolucion inversa de direcciones IP a nombres de host

- i --interfaz-- : Especifica la interfaz de red que tcpdump debe utilizar para capturar el trafico.

- net 192.168.0.0/24 : Filtro para capturar el tráfico de red de la ted 192.168.0.0.
Solo puede capturar el tráfico de la red que indiquemos

- **tcptrack** -i interfaz:
Es otro comando para monitorizar la actividad de red en sistemas Linux.
Con este comando podemos obtener una visión rápida de conexiones TCP están activas en tu sistema en un momento dado.

- **netstat (ss)** : Muestra las conexiones activas de una computadora , tanto entrantes como salientes. 
**_Ejemplo: netstat -plunt_**





