---
title: "Aptum IaaS:  Conectar a una VPC mediante una VPN de acceso remoto"
slug: aptum-iaas-conectar-a-una-vpc-con-vpn
---

Aptum IaaS brinda la capacidad de conectarte de forma segura desde tu hogar u oficina a tu VPC. Usando un cliente VPN y una clave precompartida sobre IPSec en tu plataforma preferida (por ejemplo, Windows, macOS, Ubuntu...), podrás acceder a tus instancias sin tener que pasar por el reenvío de puertos en direcciones IP públicas.

## Configuración de VPC
**Nota:** Para realizar las siguientes operaciones, tu cuenta de usuario debe tener asignada la función de **Editor** o **Propietario** en el entorno de destino.

#### Habilitar acceso VPN
Antes de poder conectarte a tu VPC a través de una conexión VPN de cliente, debes habilitar el acceso VPN en la VPC.

1. Navega hasta el entorno de Aptum IaaS de destino.
1. Selecciona la pestaña *Redes*.
1. Localiza la VPC de destino. Esta es la VPC a la que deseas conectarte a través de la VPN.
1. Haz clic en el icono de engranaje de *VPN de acceso remoto* para la VPC de destino. Aparecerá la página *VPN de acceso remoto*.
1. Haz clic en el menú acciones ocultas y selecciona *Habilitar* para activar el acceso a la VPN.
1. Tras unos instantes, se mostrará una clave precompartida en la página, en la sección *Atributos*.
1. La dirección IP a la que conectarte se muestra en la parte superior de la tarjeta. Copia y pega esta dirección en tu cliente VPN.
1. Copia y pega esta clave precompartida en tu cliente VPN.

#### Crear cuenta VPN
1. En la página VPN de una VPC, la lista de usuarios de VPN también se muestra debajo del certificado.
1. Haz clic en *Agregar usuario de VPN*.
1. Rellena el formulario *Agregar usuario de VPN*.
1. Haz clic en *Aplicar*.
1. Repite los pasos anteriores para cada usuario de VPN deseado.


## Conexión a VPN
Una vez que hayas configurado correctamente tu VPC para el acceso a VPN y hayas creado al menos un usuario de VPN, ahora estás listo para conectarte a esta VPN para acceder a tus instancias y aplicaciones. Cuando se conecta a una VPC a través de VPN, los clientes tienen acceso a todos sus niveles (hasta 4 subredes).

Se requiere la siguiente información para configurar el cliente VPN:

- **IP pública:** La dirección IP pública de la VPC con la etiqueta con el propósito de `VPN`.
- **Clave precompartida:** La cadena que se muestra en la sección *Atributos* de la página *VPN de acceso remoto*.
- **Nombre de usuario:** Un nombre de usuario de cuenta VPN válido.
- **Contraseña:** Una contraseña de cuenta VPN válida.
