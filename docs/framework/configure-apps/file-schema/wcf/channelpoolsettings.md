---
title: <channelPoolSettings>
ms.date: 03/30/2017
ms.assetid: 4755f3d3-4213-4c68-ae7f-45b67d744459
ms.openlocfilehash: dd6cf74560694e7e16103c624b33a4c590ce5d50
ms.sourcegitcommit: 14355b4b2fe5bcf874cac96d0a9e6376b567e4c7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/30/2019
ms.locfileid: "55266928"
---
# <a name="channelpoolsettings"></a>\<channelPoolSettings>
Especifica los valores de grupo de canal para un enlace personalizado.  
  
 \<system.serviceModel>  
\<bindings>  
\<customBinding>  
\<binding>  
\<oneWay>  
\<channelPoolSettings>  
  
## <a name="syntax"></a>Sintaxis  
  
```xml  
<channelPoolSettings idleTimeout="TimeSpan"
                     leaseTimeout="TimeSpan"
                     maxOutboundConnectionsPerEndpopint="Integer" />
```  
  
## <a name="attributes-and-elements"></a>Atributos y elementos  
 En las siguientes secciones se describen los atributos, los elementos secundarios y los elementos primarios.  
  
### <a name="attributes"></a>Atributos  
  
|Atributo|Descripción|  
|---------------|-----------------|  
|`idleTimeout`|<xref:System.TimeSpan> positivo que especifica el tiempo máximo que los canales del grupo pueden estar inactivos antes de que desconectarse. El valor predeterminado es 00:02:00.|  
|`leaseTimeout`|<xref:System.TimeSpan> que especifica el intervalo de tiempo después del cual un canal, cuando se devuelve al grupo, se cierra. El valor predeterminado es 00:10:00.|  
|`maxOutboundChannelsPerEndpoint`|Entero positivo que especifica el número máximo de canales que se pueden almacenar en el grupo para cada extremo remoto. El valor predeterminado es 10.|  
  
### <a name="child-elements"></a>Elementos secundarios  
 Ninguno.  
  
### <a name="parent-elements"></a>Elementos primarios  
  
|Elemento|Descripción|  
|-------------|-----------------|  
|[\<oneWay>](../../../../../docs/framework/configure-apps/file-schema/wcf/oneway.md)|Habilita el enrutamiento del paquete para un enlace personalizado.|  
  
## <a name="remarks"></a>Comentarios  
 Las cuotas se utilizan como un mecanismo de la directiva para evitar el consumo excesivo de recursos . Evitan los ataques por denegación de servicio (DoS), tanto malintencionados como involuntarios. Utilice este elemento al establecer las cuotas del canal en un canal personalizado.  
  
 `ChannelPoolSettings` especifica tres cuotas:  
  
-   La cuota `idleTimeout` se utiliza para mitigar los ataques por denegación de servicio (DoS) en el servidor basados en acaparar los recursos durante un período de tiempo extendido. Por parte del cliente, establecer el valor correcto puede aumentar la confiabilidad de conectar con el servicio. El valor predeterminado está basado en una asignación de recursos conservadoramente modesta. Es conveniente para un entorno de desarrollo y escenarios de instalación pequeños. Los administradores del servicio deberían revisar el valor si una instalación se está quedando sin recursos o si las conexiones se limitan a pesar de la disponibilidad de recursos adicionales.  
  
-   La cuota `leaseTimeout` se utiliza a para la integración con equilibradores de carga y para mejorar la confiabilidad. El valor predeterminado está basado en una asignación de recursos conservadora. Es conveniente para un entorno de desarrollo y escenarios de instalación pequeños. Los administradores del servicio deberían revisar el valor si una instalación se está quedando sin recursos o si las conexiones se limitan a pesar de la disponibilidad de recursos adicionales.  
  
-   La cuota `maxOutboundChannelsPerEndpoint` establece los límites de la caché en el servidor y el cliente y se utiliza para mejorar la confiabilidad. El valor predeterminado está basado en una asignación de recursos conservadoramente modesta que es conveniente para un entorno de desarrollo y para escenarios de instalación pequeños. Los administradores del servicio deberían revisar el valor si una instalación se está quedando sin recursos o si las conexiones se limitan a pesar de la disponibilidad de recursos adicionales.  
  
## <a name="see-also"></a>Vea también
- <xref:System.ServiceModel.Channels.OneWayBindingElement.ChannelPoolSettings%2A>
- <xref:System.ServiceModel.Channels.ChannelPoolSettings>
- <xref:System.ServiceModel.Configuration.OneWayElement.ChannelPoolSettings%2A>
- <xref:System.ServiceModel.Configuration.ChannelPoolSettingsElement>
- <xref:System.ServiceModel.Channels.CustomBinding>
- [\<oneWay>](../../../../../docs/framework/configure-apps/file-schema/wcf/oneway.md)
- [Enlaces](../../../../../docs/framework/wcf/bindings.md)
- [Extensión de enlaces](../../../../../docs/framework/wcf/extending/extending-bindings.md)
- [Enlaces personalizados](../../../../../docs/framework/wcf/extending/custom-bindings.md)
- [\<customBinding>](../../../../../docs/framework/configure-apps/file-schema/wcf/custombinding.md)
