# Alta de Enlace Informático
---
### Actores principales: 
Administrador y Enlace Informático 

### Actores secundarios:  
AD, servicio de correo. 

### Precondiciones: 

- La cuenta AD debe existir y estar activa. 

### Flujo normal: 

- Seleccionar la cuenta. 

- Elige la opción “Asignar Rol” 

- El sistema muestra la lista de Roles 

- Se elije el rol correspondiente 

- El sistema muestra la lista de áreas permitidas  

- Se elije el área o áreas en las que fungirá con el rol seleccionado. 

- El sistema solicita confirmación de la acción (doble validación). 

- El sistema actualiza el rol en la BD  

- El sistema sincroniza permisos y servicios según el rol asignado. 

- El sistema informa, al correo personal del usuario, la asignación del Rol. 

- El sistema registra la operación en la bitácora. 

### Flujos alternos: 

- Si la actualización falla en AD, el sistema no realiza el cambio y muestra error. 

### Postcondiciones: 

- La cuenta queda con los permisos del rol asignado. 