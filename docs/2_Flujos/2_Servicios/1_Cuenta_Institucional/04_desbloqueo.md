# Desbloqueo
Actor principal: Administrador y Enlace Informático 
Precondiciones: 

La cuenta debe existir y tener estado “Bloqueada”. 

Flujo principal: 

Se Selecciona al usuario de la lista de cuentas AD. 

Se despliega el área de servicios 

Selecciona el servicio “Cuenta de correo Institucional”. 

El sistema muestra las cuentas relacionadas al usuario. (cuenta personal y cuenta PAD si la hubiera) 

El sistema permite seleccionar la o las cuentas a bloquear 

se selecciona la opción “Desbloquear”. 

El sistema muestra los datos de la cuenta y solicita confirmación. 

El sistema restablece el acceso mediante la API del proveedor de correo. 

Se actualiza el estado de la cuenta a “Activa” en la base de datos del sistema. 

Se genera registro en la bitácora. 

Flujo alterno: 

Si la cuenta no se puede desbloquear por error de proveedor, el sistema registra el incidente. 

Postcondiciones: 

La cuenta vuelve al estado “Activa”. 

El usuario puede acceder nuevamente al correo 

🔓 Caso de Uso: Desbloqueo de Cuenta

Actor principal:
Administrador y Enlace Informático

🧩 Precondiciones

La cuenta debe existir.

La cuenta debe tener estado "Bloqueada".

🚀 Flujo principal

Se selecciona al usuario de la lista de cuentas AD.

El sistema despliega el área de servicios.

Se selecciona el servicio “Cuenta de correo institucional”.

El sistema muestra las cuentas relacionadas al usuario (cuenta personal y cuenta PAD, si la hubiera).

El sistema permite seleccionar una o varias cuentas a desbloquear.

Se selecciona la opción “Desbloquear”.

El sistema muestra los datos de la cuenta y solicita confirmación.

El sistema restablece el acceso mediante la API del proveedor de correo.

Se actualiza el estado de la cuenta a “Activa” en la base de datos del sistema.

Se genera un registro en la bitácora.

⚠️ Flujo alterno

Si la cuenta no se puede desbloquear por un error del proveedor, el sistema registra el incidente en la bitácora y notifica al administrador.

✅ Postcondiciones

La cuenta vuelve al estado “Activa”.

El usuario puede acceder nuevamente a su correo institucional.