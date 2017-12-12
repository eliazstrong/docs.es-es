---
title: Interfaz ICorDebugVariableHomeEnum
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-clr
ms.tgt_pltfrm: 
ms.topic: article
api_name: ICorDebugVariableHomeEnum
api_location: mscordbi.dll
api_type: COM
f1_keywords: ICorDebugVariableHomeEnum
helpviewer_keywords: ICorDebugVariableHomeEnum interface [.NET Framework debugging]
ms.assetid: c312ae6d-c8dc-48d6-9f1e-ead515c88fdf
topic_type: apiref
caps.latest.revision: "4"
author: rpetrusha
ms.author: ronpet
manager: wpickett
ms.openlocfilehash: 7e64a52ca70606f83138b636f7ccb62ba18908f5
ms.sourcegitcommit: 4f3fef493080a43e70e951223894768d36ce430a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/21/2017
---
# <a name="icordebugvariablehomeenum-interface"></a><span data-ttu-id="b24bf-102">Interfaz ICorDebugVariableHomeEnum</span><span class="sxs-lookup"><span data-stu-id="b24bf-102">ICorDebugVariableHomeEnum Interface</span></span>
<span data-ttu-id="b24bf-103">Proporciona un enumerador para las variables locales y argumentos en una función.</span><span class="sxs-lookup"><span data-stu-id="b24bf-103">Provides an enumerator to the local variables and arguments in a function.</span></span>  
  
## <a name="methods"></a><span data-ttu-id="b24bf-104">Métodos</span><span class="sxs-lookup"><span data-stu-id="b24bf-104">Methods</span></span>  
  
|<span data-ttu-id="b24bf-105">Método</span><span class="sxs-lookup"><span data-stu-id="b24bf-105">Method</span></span>|<span data-ttu-id="b24bf-106">Descripción</span><span class="sxs-lookup"><span data-stu-id="b24bf-106">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="b24bf-107">Next (método)</span><span class="sxs-lookup"><span data-stu-id="b24bf-107">Next Method</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugvariablehomeenum-next-method.md)|<span data-ttu-id="b24bf-108">Obtiene el número especificado de [ICorDebugVariableHome](../../../../docs/framework/unmanaged-api/debugging/icordebugvariablehome-interface.md) instancias que contienen información sobre las variables locales y argumentos en una función.</span><span class="sxs-lookup"><span data-stu-id="b24bf-108">Gets the specified number of [ICorDebugVariableHome](../../../../docs/framework/unmanaged-api/debugging/icordebugvariablehome-interface.md) instances that contain information about the local variables and arguments in a function.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="b24bf-109">Comentarios</span><span class="sxs-lookup"><span data-stu-id="b24bf-109">Remarks</span></span>  
 <span data-ttu-id="b24bf-110">El `ICorDebugVariableHomeEnum` interfaz implementa ICorDebugEnum (interfaz).</span><span class="sxs-lookup"><span data-stu-id="b24bf-110">The `ICorDebugVariableHomeEnum` interface implements the ICorDebugEnum interface.</span></span>  
  
 <span data-ttu-id="b24bf-111">Un `ICorDebugVariableHomeEnum` instancia se rellena con [ICorDebugVariableHome](../../../../docs/framework/unmanaged-api/debugging/icordebugvariablehome-interface.md) instancias mediante una llamada a la [ICorDebugCode4::EnumerateVariableHomes](../../../../docs/framework/unmanaged-api/debugging/icordebugcode4-enumeratevariablehomes-method.md) método.</span><span class="sxs-lookup"><span data-stu-id="b24bf-111">An `ICorDebugVariableHomeEnum` instance is populated with [ICorDebugVariableHome](../../../../docs/framework/unmanaged-api/debugging/icordebugvariablehome-interface.md) instances by calling the [ICorDebugCode4::EnumerateVariableHomes](../../../../docs/framework/unmanaged-api/debugging/icordebugcode4-enumeratevariablehomes-method.md) method.</span></span> <span data-ttu-id="b24bf-112">Cada [ICorDebugVariableHome](../../../../docs/framework/unmanaged-api/debugging/icordebugvariablehome-interface.md) instancias de la colección representa una variable local o un argumento en una función.</span><span class="sxs-lookup"><span data-stu-id="b24bf-112">Each [ICorDebugVariableHome](../../../../docs/framework/unmanaged-api/debugging/icordebugvariablehome-interface.md) instance in the collection represents a local variable or argument in a function.</span></span> <span data-ttu-id="b24bf-113">El [ICorDebugVariableHome](../../../../docs/framework/unmanaged-api/debugging/icordebugvariablehome-interface.md) pueden enumerar objetos de la colección mediante una llamada a la [ICorDebugVariableHomeEnum::Next](../../../../docs/framework/unmanaged-api/debugging/icordebugvariablehomeenum-next-method.md) método.</span><span class="sxs-lookup"><span data-stu-id="b24bf-113">The  [ICorDebugVariableHome](../../../../docs/framework/unmanaged-api/debugging/icordebugvariablehome-interface.md) objects in the collection can be enumerated by calling the [ICorDebugVariableHomeEnum::Next](../../../../docs/framework/unmanaged-api/debugging/icordebugvariablehomeenum-next-method.md) method.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="b24bf-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b24bf-114">Requirements</span></span>  
 <span data-ttu-id="b24bf-115">**Plataformas:** vea [requisitos del sistema](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="b24bf-115">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="b24bf-116">**Encabezado:** CorDebug.idl, CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="b24bf-116">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="b24bf-117">**Biblioteca:** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="b24bf-117">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="b24bf-118">**Versiones de .NET framework:**[!INCLUDE[net_current_v462plus](../../../../includes/net-current-v462plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="b24bf-118">**.NET Framework Versions:** [!INCLUDE[net_current_v462plus](../../../../includes/net-current-v462plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="b24bf-119">Vea también</span><span class="sxs-lookup"><span data-stu-id="b24bf-119">See Also</span></span>  
 [<span data-ttu-id="b24bf-120">Interfaz ICorDebugVariableHome</span><span class="sxs-lookup"><span data-stu-id="b24bf-120">ICorDebugVariableHome Interface</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugvariablehome-interface.md)  
 [<span data-ttu-id="b24bf-121">Interfaces de depuración</span><span class="sxs-lookup"><span data-stu-id="b24bf-121">Debugging Interfaces</span></span>](../../../../docs/framework/unmanaged-api/debugging/debugging-interfaces.md)