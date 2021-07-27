# Control de acceso Modulo RFID RC522

Detecta el carnet al acercarlo al modulo RFID registrando la fecha, hora y persona que se realizó la acción, además realiza un envió de correo con esta información para tener así un control efectivo del cumplimiento de los horarios. 
Para este proyecto y para el funcionamiento de la pantalla Oled se utilizaron las librerías MFRC522 de micropython de otros repositorios.    
 
• https://github.com/Tasm-Devil/micropython-mfrc522-esp32
• https://github.com/micropython/micropython/blob/master/drivers/display/ssd1306.py

## Archivos 

• read.py (realiza la lectura del chip y valida con los datos guardados para realizar el registro y envío de correo, si el chip no es válido arroja una alerta.
• write.py (se encarga de asignar ID a los chip o tarjetas para configuración de registros).
• mfrc522.py (librería para el funcionamiento de read.py y write.py), no se pueden cambiar valores ya que se puede afectar su correcto funcionamiento.
• ssd1306.py (librería para el funcionamiento de pantalla oled 128x64)
