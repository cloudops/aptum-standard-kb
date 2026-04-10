---
title: "Cloudflare: Agregar un registro DNS"
slug: cloudflare-agregar-registro-dns
---


## Acerca de esta tarea

Este artículo te guiará a través del proceso para agregar un nuevo registro DNS a un dominio DNS de Cloudflare.

## Antes de comenzar

- Tu entorno de Cloudflare debe estar configurado
- El dominio de destino debe existir en el entorno
- El registrador donde está alojado este nombre de dominio debe apuntar a los servidores DNS de Cloudflare
- El estado del dominio debe ser `Activo`

## Procedimiento

1. Acceda a tu servicio de Cloudflare mediante el menú **Servicios**, haz clic en el entorno de destino en la página del servicio y, a continuación, haz clic en el dominio de destino.

2. Haz clic en el botón **Agregar registro DNS**.

3. En el cuadro de diálogo **Agregar registro DNS**, selecciona el tipo de registro e introduce los valores correspondientes.

Cada tipo de registro de recurso tiene sus propios campos; por lo tanto, al cambiar el campo **Tipo**, se modificarán los campos que se muestran.

4. Selecciona un valor de tiempo de vida (TTL) para este registro.

   Esta opción controla cuánto tiempo un cliente DNS almacenará en caché el registro antes de solicitarlo de nuevo al sistema DNS.

5. (Opcional) Introduce un comentario que se añadirá al registro. Este comentario es interno y no se mostrará en la lista de registros.

6. Haz clic en el botón **Aplicar**.


## Resultados

- El nuevo registro DNS ya aparece en la página del dominio de destino
- El registro ahora se resuelve al consultarlo a través del sistema DNS