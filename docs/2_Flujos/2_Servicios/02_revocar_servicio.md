---
sidebar_position: 1
---

# Revocar Servicio
---
### Actores principales: 
Administrador y Enlace Informático 

### Actores secundarios: 
AD, Servicios vinculados 

### Precondiciones: 

- La cuenta AD debe existir y estar activa. 

- Los actores deben tener permisos de gestión de servicios según corresponda. 

### Flujo normal: 

- Se Selecciona al usuario de la lista de cuentas. 

- El sistema muestra los servicios actualmente asignados al usuario. 

- El administrador desmarca los servicios que desea revocar. 

- El sistema valida que la revocación no afecte dependencias   

- El sistema actualiza los atributos y permisos en AD para reflejar la revocación. 

- El sistema sincroniza la configuración en AD y servicios relacionados. 

- El sistema notifica al usuario los servicios que han sido revocados. 

- El sistema registra la operación en la bitácora. 

### Flujos alternos: 

- Si la revocación no es posible por dependencias no resueltas, el sistema manda una alerta y detiene la operación. 

- Si ocurre un error al actualizar en AD, el sistema cancela la revocación y muestra un mensaje de error. 

- Si la sincronización con AD falla, el sistema genera un aviso para revisión manual. 

### Postcondiciones: 

- La cuenta del usuario queda sin acceso a los servicios revocados. 

- La operación queda registrada para fines de control 

 