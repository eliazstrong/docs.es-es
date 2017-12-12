---
title: "IMethodMalloc::Alloc (Método)"
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-clr
ms.tgt_pltfrm: 
ms.topic: reference
api_name: IMethodMalloc.Alloc
api_location: mscorwks.dll
api_type: COM
f1_keywords: IMethodMalloc::Alloc
helpviewer_keywords:
- IMethodMalloc::Alloc method [.NET Framework profiling]
- Alloc method, IMethodMalloc interface [.NET Framework profiling]
ms.assetid: 8653bd4c-2290-43d2-a3e1-cbbd50033f4f
topic_type: apiref
caps.latest.revision: "15"
author: mairaw
ms.author: mairaw
manager: wpickett
ms.openlocfilehash: ae0fa84c08cb8e366db36b6727a3058f24789801
ms.sourcegitcommit: bd1ef61f4bb794b25383d3d72e71041a5ced172e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/18/2017
---
# <a name="imethodmallocalloc-method"></a><span data-ttu-id="2569e-102">IMethodMalloc::Alloc (Método)</span><span class="sxs-lookup"><span data-stu-id="2569e-102">IMethodMalloc::Alloc Method</span></span>
<span data-ttu-id="2569e-103">Intenta asignar una cantidad específica de memoria para un nuevo cuerpo de función del lenguaje intermedio (MSIL) de Microsoft.</span><span class="sxs-lookup"><span data-stu-id="2569e-103">Attempts to allocate a specified amount of memory for a new Microsoft intermediate language (MSIL) function body.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="2569e-104">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="2569e-104">Syntax</span></span>  
  
```  
PVOID Alloc (  
    [in] ULONG   cb  
);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="2569e-105">Parámetros</span><span class="sxs-lookup"><span data-stu-id="2569e-105">Parameters</span></span>  
 `cb`  
 <span data-ttu-id="2569e-106">[in] El número de bytes que se va a asignar para el cuerpo del método.</span><span class="sxs-lookup"><span data-stu-id="2569e-106">[in] The number of bytes to allocate for the method body.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="2569e-107">Comentarios</span><span class="sxs-lookup"><span data-stu-id="2569e-107">Remarks</span></span>  
 <span data-ttu-id="2569e-108">La memoria asignada comenzará en una dirección mayor que la dirección base del módulo que está asociado a este asignador.</span><span class="sxs-lookup"><span data-stu-id="2569e-108">The allocated memory will begin at an address greater than the base address of the module that is associated with this allocator.</span></span> <span data-ttu-id="2569e-109">En otras palabras, cada asignador se crea para un módulo determinado e intentará asignar memoria en un desplazamiento positivo respecto a su dirección base.</span><span class="sxs-lookup"><span data-stu-id="2569e-109">In other words, each allocator is created for a particular module, and will attempt to allocate memory at a positive offset from its base address.</span></span> <span data-ttu-id="2569e-110">Si `Alloc` no puede asignar el número solicitado de bytes en una dirección mayor que la dirección base del módulo, devolverá E_OUTOFMEMORY, independientemente de la cantidad real de espacio de memoria disponible.</span><span class="sxs-lookup"><span data-stu-id="2569e-110">If `Alloc` fails to allocate the requested number of bytes at an address greater than the base address of the module, it returns E_OUTOFMEMORY, regardless of the actual amount of memory space available.</span></span>  
  
 <span data-ttu-id="2569e-111">El `Alloc` método debe utilizarse junto con la [ICorProfilerInfo:: SetILFunctionBody](../../../../docs/framework/unmanaged-api/profiling/icorprofilerinfo-setilfunctionbody-method.md) método.</span><span class="sxs-lookup"><span data-stu-id="2569e-111">The `Alloc` method should be used in conjunction with the [ICorProfilerInfo::SetILFunctionBody](../../../../docs/framework/unmanaged-api/profiling/icorprofilerinfo-setilfunctionbody-method.md) method.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="2569e-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2569e-112">Requirements</span></span>  
 <span data-ttu-id="2569e-113">**Plataformas:** WindSee [requisitos del sistema](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="2569e-113">**Platforms:** WindSee [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="2569e-114">**Encabezado:** CorProf.idl, CorProf.h</span><span class="sxs-lookup"><span data-stu-id="2569e-114">**Header:** CorProf.idl, CorProf.h</span></span>  
  
 <span data-ttu-id="2569e-115">**Biblioteca:** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="2569e-115">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="2569e-116">**Versiones de .NET framework:**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="2569e-116">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="2569e-117">Vea también</span><span class="sxs-lookup"><span data-stu-id="2569e-117">See Also</span></span>  
 [<span data-ttu-id="2569e-118">IMethodMalloc (interfaz)</span><span class="sxs-lookup"><span data-stu-id="2569e-118">IMethodMalloc Interface</span></span>](../../../../docs/framework/unmanaged-api/profiling/imethodmalloc-interface.md)