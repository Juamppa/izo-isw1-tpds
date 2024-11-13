**Caso de Uso**

**Actor Primario:**  
Cámaras

**Actores Secundarios:**  
No tiene 

**Precondiciones:**  
Ninguna

**Camino básico:**

1. La cámara detecta el paso del vehículo, y envía los datos del vehículo fecha y hora, id de la cámara, patente y velocidad.  
2. El sistema evalúa los datos recibidos por la cámara, y los registra  
   

**Caminos Alternativos:**  
2.A Si la velocidad envíada por la cámara es mayor o igual a 70km/h y menor o igual a 100km/h.   
2.A.1 El sistema registra los datos, envía los datos a una API y un correo con los datos a la cuenta "avisos@ciudad".  
2.A.2 Fin de Caso de uso.

2.B Si la velocidad recibida de la cámara es mayor a 100km/h:  
2.B.1 El sistema envía los datos a una API,  un correo con los datos a la cuenta "alertas@ciudad", y  envía 3 veces los datos a una impresora.  
2.B.2 Fin de caso de uso

**Escenario de éxito:**

* El sistema registra con éxito el paso de los vehículos.	

**Escenario de fracaso:**

* El sistema falla al registrar los datos del paso de los vehículos.

