# 👾[PlayFast.com](https://PlayFast.com) 
# AutoLogin Encriptado


## Paso 1:
Enviar al **url** [https://playfast.com/auth/auto-login/usuario/password](https://playfast.com/auth/auto-login/usuario/password) 

### Parametros: 
- Usuario 
- y password
 
🔐Este usuario que nos envían lo encriptamos de la siguiente manera:

- **AES con clave Playfast**:
El resultado de este encriptado, se encripta en base64 y la url queda de la siguiente manera:

**Ejemplo:**

```
https://playfast.com/auth/auto-login/VTJGc2RHVmtYMS9kMUphRlV3bFkxWGxZTlZ0MnoyeDgxT0hZcmIwVVYxMD0=/VTJGc2RHVmtYMTg2QjF4Y1lwTzQwdmNKNy94Zk5oNzkxeHFucHN2U3Y1MD0=

```
