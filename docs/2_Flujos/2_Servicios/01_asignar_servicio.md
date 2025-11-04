# Asignar Servicio
---
### Actores principales: 
Administrador y Enlace Informático 

### Actores secundarios: 
AD, Servicios vinculados 

### Precondiciones: 

- La cuenta de AD debe existir y estar activa. 

- Los actores deben tener permisos de gestión de servicios según corresponda. 

### Flujo normal: 

- Se Selecciona al usuario de la lista de cuentas. 

- El sistema muestra los servicios disponibles por (ejemplo: correo institucional, acceso VPN, Telefonía IP, NIP de impresión, bases de datos, etc). 

- Se seleccionan los servicios que desea asignar. 

- El sistema valida dependencias entre servicios. 

- El sistema actualiza los atributos y permisos en AD. 

- El sistema sincroniza la configuración y demás servicios vinculados. 

- El sistema notifica al usuario (correo alterno o institucional) los servicios que se han habilitado. 

- El sistema registra la operación en la bitácora. 

### Flujos alternos: 

- Si la combinación de servicios no es válida, el sistema genera una alerta y no permite la asignación hasta corregir. 

- Si falla la actualización en AD, el sistema revierte los cambios y muestra un mensaje de error. 

- Si algún servicio no se sincroniza, el sistema genera una alerta para atención manual. 

### Postcondiciones: 

- La cuenta del usuario queda con acceso habilitado a los servicios seleccionados. 

- El registro queda registrado para fines de control. 