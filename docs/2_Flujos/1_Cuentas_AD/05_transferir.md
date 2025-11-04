# Transferir
---
### Actores principales:
 Administrador y Enlace Informático 

### Actores secundarios:
 AD, servicio de correo. 

### Precondiciones: 

- La cuenta AD debe existir y estar activa. 

### Flujo normal: 

- Selecciona la cuenta a transferir. 

- Elige la opción “Transferir” 

- El sistema muestra la lista de áreas que el enlace informático administra  

- El Enlace Informático elije el área correspondiente. 

- El sistema solicita confirmación de la acción (doble validación). 

- El sistema actualiza el área en la BD y en los atributos de la cuenta en AD (ruta de la OU). 

- El sistema sincroniza permisos y servicios según el nuevo destino. 

- El sistema informa, al correo personal del usuario, la Transferencia de la cuenta AD. 

- El sistema registra la operación en la bitácora. 

### Flujos alternos: 

- Si la actualización de Ruta/OU falla en AD, el sistema no realiza la transferencia y muestra error. 

### Postcondiciones: 

- La cuenta queda asociada al nuevo grupo/área y con los permisos correspondientes. 
