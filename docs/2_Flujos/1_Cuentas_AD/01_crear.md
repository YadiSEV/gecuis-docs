# Crear

### Actores principales: 
    Administrador y Enlace Informático .

### Actores secundarios: 
    AD, tabla CuentasSEV, Servicio de correo 

### Precondiciones: 

- El usuario, a quien se creará la cuenta, debe ser colaborador de la SEV. 

- El administrador o enlace informático debe haber iniciado sesión con permisos adecuados. 

### Flujo normal: 

- Se ingresa la CURP del usuario 

- El sistema validará la CURP con RENAPO y presentará el nombre completo del usuario a registrar. 

- Se capturará correo personal alterno y teléfono personal (opcional) del usuario. 

- Se genera el registro de la solicitud en pendiente. 

- El sistema validará por CURP si al usuario en algún momento se le asignó una cuenta de directorio activo. Esto en la Tabla CuentasSEV. 

   - Si ya tuvo una cuenta, se valida si no está ocupada, 

- Si la cuenta ya está ocupada, se genera una nueva cuenta. La nueva cuenta se valida y construye hasta que no esté siendo usada y se inserta en CuentasSEV. 

- Si no ha tenido cuenta se genera una nueva cuenta. La nueva cuenta se valida y construye hasta que no esté siendo usada y se inserta en CuentasSEV. 

- El sistema generará las credenciales de acceso cuenta AD y contraseña. 

- El sistema almacena la información en la base del sistema y en la base de sincronización del AD 

- El sistema sincronizará con el AD (por medio de script, de esto depende si es automático o con autorizar). 

- El sistema enviará al correo alterno del usuario las credenciales de acceso (cuenta AD y Contraseña). 

- Se actualiza el registro de la solicitud en atendido. 

- El sistema registrará la operación en la bitácora. 

### Flujos alternos: 

 - Si la cuenta ya existe, el sistema muestra un mensaje de que el usuario ya tiene una cuenta existente y no permite la creación. 

 - Si el registro y la sincronización con AD falla, se actualiza el registro de la solicitud en error, revierte la operación y genera una alerta de error. 

### Postcondiciones: 

- La nueva cuenta de AD queda activa y disponible para su uso. 

- Atender manualmente solicitud con alerta de error. 