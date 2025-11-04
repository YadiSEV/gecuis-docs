# Eliminar

### Actores principales:
    Administrador y Enlace Informático 

### Actores secundarios:
    AD, Servicio de correo 

### Precondiciones: 

- La cuenta debe existir en el sistema y en el AD 

- Enlace Informático debe tener permisos de eliminación de esa cuenta. 

### Flujo normal: 

- Se Selecciona al usuario a eliminar. 

- El sistema solicita confirmación de la acción (doble validación). 

- Se genera el registro de la solicitud en pendiente. 

- El sistema elimina la cuenta en la BD AD, en el sistema y cambia estatus a Eliminada. 

- El sistema sincroniza la eliminación en el AD y demás servicios vinculados. 

- El sistema informa, al correo personal del usuario, la eliminación de la cuenta AD. 

- Se actualiza el registro de la solicitud en atendido. 

- El sistema registra la operación en la bitácora. 

### Flujos alternos: 

 Si la eliminación en AD falla, se actualiza el registro de la solicitud en error, el sistema revierte la operación y muestra una alerta de error. 

### Postcondiciones: 

- La cuenta es eliminada permanentemente del AD y con ello de los servicios vinculados (¿y la cuenta msev valdría la pena eliminarla?) 

- Atender manualmente solicitud con alerta de error. 

 
