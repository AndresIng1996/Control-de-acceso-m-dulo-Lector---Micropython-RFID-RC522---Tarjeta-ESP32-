# Control de acceso Modulo RFID RC522
Detecta el carnet al acercarlo al modulo RFID registrando la fecha, hora y persona que se realizó la acción, además realiza un envió de correo con esta información para tener así un control efectivo del cumplimiento de los horarios. 
Para este proyecto y para el funcionamiento de la pantalla Oled se utilizaron las librerías MFRC522 de micropython de otros repositorios.     

•	https://github.com/Tasm-Devil/micropython-mfrc522-esp32
•	https://github.com/micropython/micropython/blob/master/drivers/display/ssd1306.py

#Archivos 
•	read.py (realiza la lectura del chip y valida con los datos guardados para realizar el registro y envío de correo, si el chip no es válido arroja una alerta.
•	write.py (se encarga de asignar ID a los chip o tarjetas para configuración de registros).
•	mfrc522.py (librería para el funcionamiento de read.py y write.py), no se pueden cambiar valores ya que se puede afectar su correcto funcionamiento.
•	ssd1306.py (librería para el funcionamiento de pantalla oled 128x64)

#Hardware
Se requiere el siguiente Hardware:
•	Esp32 (Wifi – Bluetooth)
•	Modulo RFID RC522
•	Pantalla Oled 128x64
Diagrama esquemático 
 

#Tabla de pines 
ESP32	COLOR	CONEXIÓN RFID
Pin 18	Azul	Sck
Pin 23	Naranja	Mosi
Pin 19	Amarillo	Miso
Pin 5	Gris	Sda
DNG	Negro	DNG
3.3 v	Rojo	3.3 v
ESP32	COLOR	CONEXIÓN PANTALLA OLED
Pin 22	Marrón	Scl
Pin 21	Verde	Sda 
DNG	Negro	DNG
3.3v	Rojo	VCC
ESP32	COLOR	CONEXIÓN LED ROJO
Pin 4	Morado	Positivo
GND	negro	GND
ESP32	COLOR	CONEXIÓN LED Azul
Pin 2	Morado	Positivo
GND	Amarillo 	GND

#Componentes físicos 
Imagen con los componentes montados y configurados 
 
#Hojas de cálculo de Google
En esta imagen podemos observar como quedan guardados los registros recibidos del Modulo RFID y la ESP32
 
#Correo GMAIL
En esta imagen podemos observar el correo electrónico que es enviado al realizar el registro. 

