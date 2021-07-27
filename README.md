# Control de acceso Modulo RFID RC522

Detecta el carnet al acercarlo al modulo RFID registrando la fecha, hora y persona que se realizó la acción, además realiza un envió de correo con esta información para tener así un control efectivo del cumplimiento de los horarios. 
Para este proyecto y para el funcionamiento de la pantalla Oled se utilizaron las librerías MFRC522 de micropython de otros repositorios.      
•	https://github.com/Tasm-Devil/micropython-mfrc522-esp32

•	https://github.com/micropython/micropython/blob/master/drivers/display/ssd1306.py

# Archivos

•	read.py (realiza la lectura del chip y valida con los datos guardados para realizar el registro y envío de correo, si el chip no es válido arroja una alerta.

•	write.py (se encarga de asignar ID a los chip o tarjetas para configuración de registros).

•	mfrc522.py (librería para el funcionamiento de read.py y write.py), no se pueden cambiar valores ya que se puede afectar su correcto funcionamiento.

•	ssd1306.py (librería para el funcionamiento de pantalla oled 128x64)

# Hardware
Se requiere el siguiente Hardware:
•	Esp32 (Wifi – Bluetooth)

•	Modulo RFID RC522

•	Pantalla Oled 128x64

# Diagrama esquemático 

![Circuito control de acceso](https://user-images.githubusercontent.com/86446435/127217041-d98898ce-b07b-40f2-9292-63c7fd51e0d5.png)

# Tabla de pines 

![Tabla](https://user-images.githubusercontent.com/86446435/127217419-3ef17d19-4cea-4bb4-b3a3-6c4a8e2276b0.PNG)

# Componentes físicos 
Imagen con los componentes montados y configurados 

![Foto Proyecto](https://user-images.githubusercontent.com/86446435/127217125-533d5171-a248-4843-816b-6e7394ba1293.jpg)


# Hojas de cálculo de Google
En esta imagen podemos observar como quedan guardados los registros recibidos del Modulo RFID y la ESP32

![Google](https://user-images.githubusercontent.com/86446435/127220732-234a173c-b126-4dd4-8f76-3d74a9c79366.jpg)

# Correo GMAIL
En esta imagen podemos observar el correo electrónico que es enviado al realizar el registro. 

![Corore](https://user-images.githubusercontent.com/86446435/127217096-d4496ca6-0096-4dcb-a850-3bf0ea9d198c.jpg)
