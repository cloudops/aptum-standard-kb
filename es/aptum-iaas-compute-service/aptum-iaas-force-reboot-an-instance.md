---
title: "Aptum IaaS: Forzar el cierre de una instancia"
slug: aptum-iaas-forzar-el-cierre-de-una-instancia
---


Si una instancia deja de responder, sigue estos pasos para forzar el cierre de la instancia:

   - Recopilar ID de la instancia: en la vista detallada de una instancia, toma nota del campo **ID**
   - Configurar el entorno de CloudMonkey: [procedimiento](../cloudstack-compute-service/cloudstack-install-and-config-cloudmonkey.md)
   - En CloudMonkey, ejecute: `stop id de máquina virtual=ID forzado=verdadero`

Para iniciar la instancia, use CloudMonkey y ejecute: `start virtualmachine id=ID`
