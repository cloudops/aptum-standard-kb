---
title: "Cloudflare: Cómo comenzar"
slug: cloudflare-como-comenzar
---


Este artículo ofrece información sobre un cambio importante en tus servicios de DNS. Aptum va a retirar su plataforma DNS heredada y trasladará todos los servicios a Cloudflare para mejorar el rendimiento y la fiabilidad. Aquí se explican los cambios, las acciones que debes realizar y la fecha límite para llevarlas a cabo.

## Acceso al nuevo portal

Si eres el responsable técnico pero no has recibido las credenciales, coordínate con el contacto principal de tu cuenta. Dicho contacto ha recibido un correo electrónico con acceso a Aptum Portal, donde ahora se alojan tus servicios de DNS. El correo también indica la fecha límite para la migración.

Si no has recibido el mensaje o necesitas acceso para otros miembros del equipo, por favor comunícate con tu gestor de cuenta o con nuestro equipo de soporte en support@aptum.com.

## Lo que ya hemos hecho

Tus zonas DNS y tus registros se han importado a la nueva plataforma. Tu servicio DNS actual sigue funcionando sin cambios durante la migración; por tanto, ambos sistemas operan en paralelo y no se producen interrupciones en el servicio. El correo electrónico enviado a tu contacto principal incluye un enlace para configurar el acceso al nuevo Aptum Portal, donde ahora se alojan sus datos DNS.

**Importante:** La importación automática copia la mayoría de los registros, pero no siempre captura la totalidad de la información. Es posible que los registros TXT \(SPF, DKIM, DMARC\), algunas configuraciones de correo (MX) y los tipos de registro menos comunes se omitan o se importen de manera diferente. Por favor, considera la zona importada como un punto de partida que debe verificarse, no como una copia definitiva. Los pasos que figuran a continuación incluyen una fase de verificación precisamente por este motivo.

## Qué debes hacer

### Antes de comenzar

-   Debes disponer de las credenciales de inicio de sesión para Aptum Portal
-   Debes tener la URL y las credenciales de acceso de tu registrador de dominios

### Acerca de esta tarea

Tus dominios deben configurarse para utilizar los servidores de nombres de Cloudflare.

Sigue estos pasos para actualizar la configuración en tu registrador de dominios y completar la migración de DNS. Calcula aproximadamente entre 15 y 20 minutos de trabajo activo por dominio, además de un plazo de hasta 24 horas para que cada dominio se active tras el cambio, sumado al tiempo habitual de propagación de DNS.

### Procedimiento

1.  Inicia sesión en Aptum Portal utilizando los datos de acceso que configuraste a partir del correo electrónico de invitación.

2.  En el menú **Servicios**, selecciona **Cloudflare**.

    ![Captura de pantalla de la página de inicio con el menú de servicios abierto](img/cloudflare-services-menu.png)

3.  Cuando aparezca la página **Entornos**, selecciona el entorno donde se han añadido tus dominios. 

    **Consejo:** El nombre del entorno que contiene tus dominios migrados seguirá el formato `imported-[YYYY-MM-DD]`.

4.  Para cada dominio migrado, verifica los registros antes de cambiar los servidores de nombres. 

    1.  Compara los registros que aparecen en el portal con tu zona DNS actual y activa. 

        Presta especial atención a los registros MX y TXT \(SPF, DKIM, DMARC\). Si falta alguno o es incorrecto, añádelo o corrígelo en el portal ahora mismo. Si cambias los servidores de nombres antes de solucionar esto, el correo electrónico y otros servicios podrían dejar de funcionar. 

    2.  Comprueba el estado del proxy. 

        Los registros importados como `Proxied` \(con el icono de la nube naranja\) enrutan el tráfico a través de Cloudflare y modifican la dirección de resolución. Esto suele ser adecuado para sitios web, pero afectará negativamente a los servidores de correo, FTP y cualquier servicio que requiera acceso directo a tu dirección IP real. Configura como "DNS only" (nube gris) cualquier elemento que no deba pasar por el proxy antes de realizar el cambio. 

    3.  Verifica la configuración de DNSSEC. 

        Esta es la causa más frecuente de que un dominio deje de funcionar durante la migración. Si DNSSEC está habilitado actualmente para el dominio en tu registrador, debes eliminar el registro DS existente en dicho registrador como parte del proceso de cambio. Si cambias los servidores de nombres mientras el registro DS antiguo sigue activo, el dominio no superará la validación y dejará de resolverse por completo, aunque todo parezca correcto.

        Si no está seguro de si DNSSEC está habilitado, contáctenos y le ayudaremos a comprobarlo.

5.  Para cada dominio migrado con el estado **Actualización de servidor de nombres pendiente**, identifica tu registrador de dominios. 

    Si aún no conoce el registrador de un dominio, utiliza la función **Registrador probable** (*Likely registrar*) o visita [lookup.icann.org](http://lookup.icann.org/) para identificarlo.

6.  Localiza y anota las nuevas asignaciones de servidores de nombres para cada dominio en Aptum Portal. 

    Estas nuevas asignaciones apuntan a los servidores de nombres de Cloudflare. Necesitarás esta información para actualizar tu dominio.

7.  En una pestaña o ventana del navegador independiente, inicia sesión en el portal de tu registrador de dominios y localiza los registros de servidores de nombres correspondientes a tu dominio.

8.  Configura el dominio para que utilice los servidores de nombres de Cloudflare. 

    Actualiza los registros de servidores de nombres para que apunten a los servidores de Cloudflare que anotaste en el paso 6.

9.  Regresa a Aptum Portal y selecciona el icono **…** junto a la entrada del dominio para iniciar un escaneo de servidores de nombres. 

    El escaneo puede tardar hasta 24 horas en completarse.

10. Una vez que el dominio se encuentre en estado **Activo** en Aptum Portal, confirma que tu sitio web, tu correo electrónico y cualquier otro servicio asociado a dicho dominio funcionen con normalidad. 

    Si detectas algún problema, puedes revertir el proceso de forma segura redirigiendo los servidores de nombres a los que utilizaba anteriormente \(mientras ambas plataformas sigan operativas\) y poniéndote en contacto con nosotros para que te ayudemos a solucionarlo.

11. Deberás repetir los pasos del 4 al 10 para cada dominio que presente el estado **Actualización de servidor de nombres pendiente** en el entorno `imported-YYYY-MM-DD`.


## Fecha límite

Por favor, completa las actualizaciones de tus servidores de nombres antes de la fecha indicada en tu correo electrónico. Nuestra plataforma DNS heredada se retirará próximamente. Una vez que se desactive, cualquier dominio que aún apunte a los servidores de nombres antiguos dejará de resolverse; esto significa que los sitios web, el correo electrónico y cualquier otro servicio vinculado a dichos dominios dejarán de funcionar. Te recomendamos no esperar hasta el último día, para así disponer de tiempo suficiente para solucionar cualquier inconveniente mientras ambos sistemas siguen operativos.

## Estamos aquí para ayudarte

El equipo de soporte de Aptum está a tu disposición para asistirte durante este proceso. Si no has recibido el correo electrónico con los datos de acceso al portal, necesitas ayuda con los servidores de nombres o con DNSSEC, o tienes alguna pregunta, contáctanos en support@aptum.com. También puedes consultar nuestra documentación sobre la migración aquí: [https://portal.aptum.com/hc/cloudflare-service](https://portal.aptum.com/hc/cloudflare-service)

Gracias por seguir confiando en nosotros.