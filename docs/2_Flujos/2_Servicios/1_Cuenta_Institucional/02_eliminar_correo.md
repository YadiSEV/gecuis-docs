# Eliminar

Actor principal: Administrador y Enlace Informático 

Actores secundarios: Usuario solicitante, Proveedor de correo (API o interfaz) 
Precondiciones: 

La cuenta de correo debe existir  

Flujo principal: 

Se Selecciona al usuario de la lista de cuentas AD. 

Se despliega el área de servicios 

Selecciona el servicio “Cuenta de correo Institucional”. 

El sistema muestra las cuentas relacionadas al usuario. (cuenta personal y cuenta PAD si la hubiera) 

El sistema permite seleccionar la o las cuentas a eliminar 

Se selecciona la opción “Eliminar” 

El sistema muestra los datos de la cuenta y solicita confirmación. 

Tras confirmar, el sistema ejecuta la eliminación mediante la API del proveedor de correo.  

El sistema elimina la cuenta de correo institucional de la base de datos y de la plantilla de personal. 

Se registra el evento en la bitácora. 

Flujo alterno: 

Si el proveedor no permite la eliminación inmediata, el sistema marca la cuenta como “Pendiente de eliminación”. 

Si ocurre un error, se almacena el incidente en la bitácora de errores. 

Postcondiciones: 

La cuenta queda eliminada o marcada como pendiente de Eliminar. 

Se registra la acción en la Bitácora. 