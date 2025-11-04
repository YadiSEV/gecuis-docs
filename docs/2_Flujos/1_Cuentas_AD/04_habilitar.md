# Habilitar
---
### Actores principales:
     - Administrador y Enlace Informático 

### Actores secundarios: 
    - AD, Servicio de correo 

### Precondiciones: 

- La cuenta debe existir en el sistema, en el AD y y estar en estado “Inactive”. 

### Flujo normal: 

- Se Selecciona la cuenta deshabilitada. 

- Elige la opción “Habilitar”. 

- El sistema solicita confirmación de la acción (doble validación). 

- El sistema actualiza el estado de la cuenta en el sistema y en la BD AD a “Active”. 

- El sistema habilita los servicios vinculados a la cuenta AD 

- El sistema sincroniza con el AD y servicios vinculados 

- El sistema informa, al correo personal del usuario, la Habilitación de la cuenta AD y servicios vinculados. 

- El sistema registra la acción en la bitácora. 

### Flujos alternos: 

- Si la habilitación falla en AD, el sistema lo notifica y revierte la operación y no aplica los cambios en otros servicios. 

### Postcondiciones: 

- El usuario recupera el acceso normal a su cuenta AD y a sus servicios. 