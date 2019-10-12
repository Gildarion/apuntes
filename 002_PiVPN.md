# LEVANTAR PIVPN 

Para el servivor se usaran dos saltos, el propio de la raspberry y otro con el proveedor protonVPN.
En [ProtonVPN](https://protonvpn.com/support/linux-vpn-setup/) se puede encontrar toda la informacion para levantar el servicio a traves de ProtonVPN.

## INSTRUCCIONES

Se debe tener previamente el ssh activado en la raspberry.

Instalas pivpn ` curl -L https://install.pivpn.io | bash `

La instalacion preguntara que ip estatica deseamos usar, que usuario explotara el servicio y si deseamos activar las actualizaciones desatendidas (**ojo-- para aplicar hace falta reiniciar).

Si mas tarde deseamos añadir otro usuario ` pivpn add `

Despues de esto preguntara el tipo de protocolo (UDP por defecto), puerto (1194 por defecto), la fortaleza del certificado y como se haran las conexiones exteriores (IP o public DNS).

En mi caso uso public DNS con [DuckDNS](https://www.duckdns.org) tiene hasta 5 dominios gratuitos.

Por ultimo nos pedira que reiniciemos y una vez hecho añadiremos el perfil creado a pivpn ` pivpn add `
