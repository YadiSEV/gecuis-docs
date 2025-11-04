# Bloqueo

Actor principal: Administrador y Enlace Informático 
Precondiciones: 

La cuenta debe existir y estar activa. 

Flujo principal: 

Se Selecciona al usuario de la lista de cuentas AD. 

Se despliega el área de servicios 

Selecciona el servicio “Cuenta de correo Institucional”. 

El sistema muestra las cuentas relacionadas al usuario. (cuenta personal y cuenta PAD si la hubiera) 

El sistema permite seleccionar la o las cuentas a bloquear 

se selecciona la opción “Bloquear”. 

El sistema muestra los datos de la cuenta y solicita confirmación. 

El sistema ejecuta el bloqueo mediante la API del proveedor de correo. 

Se actualiza el estado de la cuenta a “Bloqueada” en la base de datos del sistema. 

Se genera registro en la bitácora. 

Postcondiciones: 

El usuario pierde acceso al correo. 

Se mantiene el registro de la cuenta en la base de datos. 
