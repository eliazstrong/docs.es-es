---
title: Procedimiento Exportar metadatos desde puntos de conexión de servicio
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
ms.assetid: b6c4dfd0-f270-43ec-961a-e16eb6af2f2c
ms.openlocfilehash: 86ad062f7b7ee3dd2927f8b5b103adfd719a963d
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/23/2019
ms.locfileid: "54530001"
---
# <a name="how-to-export-metadata-from-service-endpoints"></a>Procedimiento Exportar metadatos desde puntos de conexión de servicio
En este tema se explica cómo exportar los metadatos desde los puntos de conexión de servicio.  
  
### <a name="to-export-metadata-from-service-endpoints"></a>Exportar metadatos desde extremos de servicio  
  
1.  Cree un nuevo Proyecto App de Consola de Visual Studio. Agregue el código que se muestra en los pasos siguientes en el archivo Program.cs generado dentro del método main().  
  
2.  Creará un control <xref:System.ServiceModel.Description.WsdlExporter>.  
  
     [!code-csharp[S_UEWsdlExporter#1](../../../../samples/snippets/csharp/VS_Snippets_CFX/s_uewsdlexporter/cs/program.cs#1)]
     [!code-vb[S_UEWsdlExporter#1](../../../../samples/snippets/visualbasic/VS_Snippets_CFX/s_uewsdlexporter/vb/program.vb#1)]  
  
3.  Establezca la propiedad <xref:System.ServiceModel.Description.MetadataExporter.PolicyVersion%2A> en uno de los valores de enumeración desde <xref:System.ServiceModel.Description.PolicyVersion>. Este ejemplo establece el valor en <xref:System.ServiceModel.Description.PolicyVersion.Policy15%2A> que corresponde a WS-Policy 1.5.  
  
     [!code-csharp[S_UEWsdlExporter#2](../../../../samples/snippets/csharp/VS_Snippets_CFX/s_uewsdlexporter/cs/program.cs#2)]
     [!code-vb[S_UEWsdlExporter#2](../../../../samples/snippets/visualbasic/VS_Snippets_CFX/s_uewsdlexporter/vb/program.vb#2)]  
  
4.  Cree una matriz de objetos <xref:System.ServiceModel.Description.ServiceEndpoint>.  
  
     [!code-csharp[S_UEWsdlExporter#3](../../../../samples/snippets/csharp/VS_Snippets_CFX/s_uewsdlexporter/cs/program.cs#3)]
     [!code-vb[S_UEWsdlExporter#3](../../../../samples/snippets/visualbasic/VS_Snippets_CFX/s_uewsdlexporter/vb/program.vb#3)]  
  
5.  Exporte los metadatos para cada extremo de servicio.  
  
     [!code-csharp[S_UEWsdlExporter#4](../../../../samples/snippets/csharp/VS_Snippets_CFX/s_uewsdlexporter/cs/program.cs#4)]
     [!code-vb[S_UEWsdlExporter#4](../../../../samples/snippets/visualbasic/VS_Snippets_CFX/s_uewsdlexporter/vb/program.vb#4)]  
  
6.  Compruebe para asegurarse de que no se produjo ningún error durante el proceso de exportación y recupere los metadatos.  
  
     [!code-csharp[S_UEWsdlExporter#5](../../../../samples/snippets/csharp/VS_Snippets_CFX/s_uewsdlexporter/cs/program.cs#5)]
     [!code-vb[S_UEWsdlExporter#5](../../../../samples/snippets/visualbasic/VS_Snippets_CFX/s_uewsdlexporter/vb/program.vb#5)]  
  
7.  Ahora puede utilizar los metadatos, de manera que puede escribirlos en un archivo llamando al método <xref:System.ServiceModel.Description.MetadataSet.WriteTo%28System.Xml.XmlWriter%29>.  
  
## <a name="example"></a>Ejemplo  
 A continuación, se muestra una lista de código completa para este ejemplo.  
  
 [!code-csharp[S_UEWsdlExporter#0](../../../../samples/snippets/csharp/VS_Snippets_CFX/s_uewsdlexporter/cs/program.cs#0)]
 [!code-vb[S_UEWsdlExporter#0](../../../../samples/snippets/visualbasic/VS_Snippets_CFX/s_uewsdlexporter/vb/program.vb#0)]  
  
## <a name="compiling-the-code"></a>Compilar el código  
 Al compilar Program.cs, haga referencia a System.ServiceModel.dll.  
  
## <a name="see-also"></a>Vea también
- [Información general de la arquitectura de metadatos](../../../../docs/framework/wcf/feature-details/metadata-architecture-overview.md)
- [Utilización de los metadatos](../../../../docs/framework/wcf/feature-details/using-metadata.md)
- [Puntos de conexión: Las direcciones, enlaces y contratos](../../../../docs/framework/wcf/feature-details/endpoints-addresses-bindings-and-contracts.md)
