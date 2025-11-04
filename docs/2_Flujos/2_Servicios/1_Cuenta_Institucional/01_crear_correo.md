# Crear

Actor principal: Administrador y Enlace Informático 
Actores secundarios: Usuario solicitante, Proveedor de correo (API o interfaz) 
Precondiciones: 

La cuenta AD debe existir y estar activa. No debe existir cuenta de correo institucional 

El dominio o proveedor de correo debe estar configurado y autorizado en el sistema. 

Flujo principal: 

Se Selecciona al usuario de la lista de cuentas AD. 

Se despliega el área de servicios 

Selecciona el servicio “Cuenta de correo Institucional”. 

Selecciona la opción “Crear cuenta de correo” 

El sistema validará y tratará de homologar la cuenta de correo con la de AD  

Si la cuenta no está ocupada se inserta en CuentasSEV. 

El sistema usa los datos requeridos: nombre de usuario, dominio. 

El sistema crea la cuenta mediante una API o interfaz del proveedor. 

Se guarda el registro de la nueva cuenta en la base de datos del sistema y se actualiza el dato en la plantilla de personal. 

Se notifica al usuario sobre la creación de su cuenta y se envía la información de acceso. (Cuenta y contraseña) 

Se registra la acción en la bitácora. 

Flujos alternos: 

Si la cuenta está ocupada, se genera una nueva cuenta. La nueva cuenta se valida y se construye hasta que no esté siendo ocupada y se inserta en CuentasSEV. 

Si ocurre un error con el proveedor, se guarda el evento en la bitácora de errores. 

Postcondiciones: 

La cuenta de correo queda activa y registrada en el sistema GECUIS. 

El usuario puede autenticarse con las credenciales generadas. 