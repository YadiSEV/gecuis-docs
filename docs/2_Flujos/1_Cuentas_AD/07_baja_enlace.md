# Baja de Enlace Informático
---
### Actores principales: 
Administrador y Enlace Informático 

### Actores secundarios:  
AD, servicio de correo. 

### Precondiciones: 

- La cuenta AD debe existir, estar activa y tener un rol 

### Flujo normal: 

- Seleccionar la cuenta. 

- Elige la opción “Baja de Rol” 

- El sistema muestra la lista de áreas permitidas 

- Se elije el área o áreas en las que se dará de baja . 

- El sistema solicita confirmación de la acción (doble validación). 

- El sistema actualiza  en la BD  

- El sistema sincroniza permisos y servicios según el rol dado de baja. 

- El sistema informa, al correo personal del usuario, la baja del Rol. 

- El sistema registra la operación en la bitácora. 

### Flujos alternos: 

- Si la actualización falla en AD, el sistema no realiza el cambio  y muestra error. 

### Postcondiciones: 

- La cuenta queda sin el rol asignado en las áreas seleccionadas 