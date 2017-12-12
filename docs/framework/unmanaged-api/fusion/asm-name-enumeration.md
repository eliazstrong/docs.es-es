---
title: "ASM_NAME (Enumeración)"
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-clr
ms.tgt_pltfrm: 
ms.topic: reference
api_name: ASM_NAME
api_location: fusion.dll
api_type: COM
f1_keywords: ASM_NAME
helpviewer_keywords: ASM_NAME enumeration [.NET Framework fusion]
ms.assetid: c8b65b19-d777-428f-bc0c-0d84c78a37bc
topic_type: apiref
caps.latest.revision: "8"
author: rpetrusha
ms.author: ronpet
manager: wpickett
ms.openlocfilehash: fb247f85984cff167e9e0ce729a5143633a3f7c9
ms.sourcegitcommit: 4f3fef493080a43e70e951223894768d36ce430a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/21/2017
---
# <a name="asmname-enumeration"></a><span data-ttu-id="914dc-102">ASM_NAME (Enumeración)</span><span class="sxs-lookup"><span data-stu-id="914dc-102">ASM_NAME Enumeration</span></span>
<span data-ttu-id="914dc-103">Indica la versión, compilación, referencia cultural, firma etc., del ensamblado cuyas propiedades se recuperarán o establecer [IAssemblyName](../../../../docs/framework/unmanaged-api/fusion/iassemblyname-interface.md) métodos.</span><span class="sxs-lookup"><span data-stu-id="914dc-103">Indicates the version, build, culture, signature, and so on, of the assembly whose properties will be retrieved or set by [IAssemblyName](../../../../docs/framework/unmanaged-api/fusion/iassemblyname-interface.md) methods.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="914dc-104">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="914dc-104">Syntax</span></span>  
  
```  
typedef enum {  
  
    ASM_NAME_PUBLIC_KEY = 0,  
    ASM_NAME_PUBLIC_KEY_TOKEN,  
    ASM_NAME_HASH_VALUE,  
    ASM_NAME_NAME,  
    ASM_NAME_MAJOR_VERSION,  
    ASM_NAME_MINOR_VERSION,  
    ASM_NAME_BUILD_NUMBER,  
    ASM_NAME_REVISION_NUMBER,  
    ASM_NAME_CULTURE,  
    ASM_NAME_PROCESSOR_ID_ARRAY,  
    ASM_NAME_OSINFO_ARRAY,  
    ASM_NAME_HASH_ALGID,  
    ASM_NAME_ALIAS,  
    ASM_NAME_CODEBASE_URL,  
    ASM_NAME_CODEBASE_LASTMOD,  
    ASM_NAME_NULL_PUBLIC_KEY,  
    ASM_NAME_NULL_PUBLIC_KEY_TOKEN,  
    ASM_NAME_CUSTOM,  
    ASM_NAME_NULL_CUSTOM,   
    ASM_NAME_MVID,  
    ASM_NAME_FILE_MAJOR_VERSION,  
    ASM_NAME_FILE_MINOR_VERSION,  
    ASM_NAME_FILE_BUILD_NUMBER,  
    ASM_NAME_FILE_REVISION_NUMBER,  
    ASM_NAME_RETARGET,  
    ASM_NAME_SIGNATURE_BLOB,  
    ASM_NAME_CONFIG_MASK,  
    ASM_NAME_ARCHITECTURE,  
    ASM_NAME_MAX_PARAMS  
  
} ASM_NAME;  
```  
  
## <a name="requirements"></a><span data-ttu-id="914dc-105">Requisitos</span><span class="sxs-lookup"><span data-stu-id="914dc-105">Requirements</span></span>  
 <span data-ttu-id="914dc-106">**Plataformas:** vea [requisitos del sistema](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="914dc-106">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="914dc-107">**Encabezado:** Fusion.h</span><span class="sxs-lookup"><span data-stu-id="914dc-107">**Header:** Fusion.h</span></span>  
  
 <span data-ttu-id="914dc-108">**Biblioteca:** incluye como recurso en MsCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="914dc-108">**Library:** Included as a resource in MsCorEE.dll</span></span>  
  
 <span data-ttu-id="914dc-109">**Versiones de .NET framework:**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="914dc-109">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="914dc-110">Vea también</span><span class="sxs-lookup"><span data-stu-id="914dc-110">See Also</span></span>  
 [<span data-ttu-id="914dc-111">IAssemblyName (interfaz)</span><span class="sxs-lookup"><span data-stu-id="914dc-111">IAssemblyName Interface</span></span>](../../../../docs/framework/unmanaged-api/fusion/iassemblyname-interface.md)  
 [<span data-ttu-id="914dc-112">Enumeraciones de fusión</span><span class="sxs-lookup"><span data-stu-id="914dc-112">Fusion Enumerations</span></span>](../../../../docs/framework/unmanaged-api/fusion/fusion-enumerations.md)