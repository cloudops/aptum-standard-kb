---
title: "Cloudflare: Agregar un dominio"
slug: cloudflare-agregar-dominio
---


## Acerca de esta tarea

Este artículo te guiará en el proceso de agregar un nuevo dominio a un entorno de Cloudflare.

## Antes de comenzar

- Tu entorno de Cloudflare debe estar ya configurado.

## Procedimiento

1. Acceda a tu servicio de Cloudflare mediante el menú **Servicios** y haz clic en el entorno de destino en la página del servicio.

2. Haz clic en el botón **Agregar un dominio**. Aparecerá la página **Agregar un dominio**.

3. Ingresa el nombre de dominio completo que deseas agregar.

   No es necesario incluir el punto al final del nombre de dominio. El sistema lo agregará automáticamente.

   Opcionalmente, marca la casilla **Quick Scan for Records** para que el sistema importe los registros de recursos existentes consultando los servidores de nombres actuales.

4. Haz clic en **Aplicar**.

5. Si marcaste la casilla **Quick Scan for Records**, haz clic en tu dominio cuando aparezca la página del entorno y verifique que todos los registros de recursos necesarios se hayan importado correctamente.

   Es posible que algunos registros no se incluyan durante el proceso de búsqueda. Si falta algún registro, agrégalo manualmente.


## Resultados

- El dominio ya aparece en el entorno de destino.
- Si seleccionaste la importación, verifica que se hayan importado todos los registros y que los que faltaban se hayan añadido manualmente.

