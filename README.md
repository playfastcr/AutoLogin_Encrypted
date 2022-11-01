# 👾[PlayFast.com](https://PlayFast.com) 
# AutoLogin Encriptado

## Paso 1: Formato 

La URL tiene el siguiente formato: [https://playfast.com/auth/auto-login/usuario/password](https://playfast.com/auth/auto-login/usuario/password) 

**Donde:**
- "usuario" es el username GBS de los jugadores, 
- y "password" es la clave de la cuenta del jugador,
 
**estos deben ser reemplazados por los resultados de las encriptaciones descritas más adelante.**

De esta forma una URL luciria de la siguiente manera:

```
https://playfast.com/auth/auto-login/VTJGc2RHVmtYMTlpaisvaGNjSi9LQ2s1Z2VOMmtNRGhrY0dBQ3VKS2pSdz0=/VTJGc2RHVmtYMTgyRWZQMnJuTHUrZkNMZDlvUTMyaUxqOW5XSTIxQUpQdz0= 
```

En la URL anterior, luego de **"/auto-login/"** se encuentra el usuario encriptado:

- **VTJGc2RHVmtYMTlpaisvaGNjSi9LQ2s1Z2VOMmtNRGhrY0dBQ3VKS2pSdz0=** que fue generado a partir del username: "LK1453" 

- y seguidamente se encuentra el password encriptado: **VTJGc2RHVmtYMTgyRWZQMnJuTHUrZkNMZDlvUTMyaUxqOW5XSTIxQUpQdz0=**  que fue generado a partir de la clave: "12345678".

## Paso 2: Encriptación
Los metodos utilizados para encriptar los parametros de la URL son **AES** y **Base64**. 

- La clave utilizada en AES para realizar la encriptacion es **Playfast**.

De esta manera, con el ejemplo anterior, el username se encripto de la siguiente manera:

```
"LK1453" -> (AES + clave) ->
"U2FsdGVkX19ij+/hccJ/KCk5geN2kMDhkcGACuJKjRw=" -> (Base64) ->
"VTJGc2RHVmtYMTlpaisvaGNjSi9LQ2s1Z2VOMmtNRGhrY0dBQ3VKS2pSdz0="

"12345678" -> (AES + clave) ->
"U2FsdGVkX182EfP2rnLu+fCLd9oQ32iLj9nWI21AJPw=" -> (Base64) ->
"VTJGc2RHVmtYMTgyRWZQMnJuTHUrZkNMZDlvUTMyaUxqOW5XSTIxQUpQdz0="
```

## Paso 3: Resultado
Al generar la URL correctamente se redireccionara al Home (https://playfast.com/home), de lo contrario la pantalla queda en blanco y no es redirigida.


## Paso 4: Versión iframe (Opción)
Insertar en los sites de GBS, el siguiente fragmento de código, donde se envíen el usuario y password encriptados, como se detalló anteriormente. 

```
<iframe width="950" height="650" src="https://playfast.com/auth/auto-login/usuario/password" name="PlayFastAutologin"></iframe>
```
