# Deshabilitar

---

### Actores principales: 
    Administrador y Enlace Informático 

### Actores secundarios:
    AD, Servicio de correo 

### Precondiciones: 

- La cuenta debe existir en el sistema, en el AD y estar activa. 

- Enlace Informático debe tener permisos de deshabilitación de esa cuenta. 

### Flujo normal: 

- Se Selecciona la cuenta del usuario. 

- Elige la opción “Deshabilitar”. 

- El sistema solicita confirmación de la acción (doble validación). 

- El sistema actualiza el estado de la cuenta en el sistema y en la BD AD a “Inactive” 

- El sistema Deshabilita los servicios vinculados a la cuenta AD 

- El sistema sincroniza con el AD y los servicios vinculados. 

- El sistema informa, al correo personal del usuario, la Deshabilitación de la cuenta AD y servicios vinculados. 

- El sistema registra la acción en la bitácora. 

### Flujos alternos: 

 - Si no es posible deshabilitar en AD, el sistema revierte la operación y muestra un error. 

### Postcondiciones: 

- La cuenta queda deshabilitada temporalmente, sin acceso a servicios. 