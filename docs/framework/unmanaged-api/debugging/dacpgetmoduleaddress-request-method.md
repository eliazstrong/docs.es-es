---
title: Método DacpGetModuleAddress::Request
ms.date: 01/16/2019
api.name:
- DacpGetModuleAddress::Request Method
api.location:
- mscordacwks.dll
api.type:
- COM
f1.keywords:
- DacpGetModuleAddress::Request Method
helpviewer.keywords:
- DacpGetModuleAddress::Request Method [.NET Framework debugging]
topic_type:
- apiref
author: cshung
ms.author: andrewau
ms.openlocfilehash: 86a51605ad8ea8b394c5b8a5961f32e96baf9e58
ms.sourcegitcommit: b56d59ad42140d277f2acbd003b74d655fdbc9f1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/19/2019
ms.locfileid: "54416616"
---
# <a name="dacpgetmoduleaddressrequest-method"></a><span data-ttu-id="0e3a6-102">Método DacpGetModuleAddress::Request</span><span class="sxs-lookup"><span data-stu-id="0e3a6-102">DacpGetModuleAddress::Request Method</span></span>

<span data-ttu-id="0e3a6-103">Realiza una solicitud para rellenar la estructura de la estructura de tiempo de ejecución determinado.</span><span class="sxs-lookup"><span data-stu-id="0e3a6-103">Performs a request to populate the structure from the given runtime structure.</span></span>

[!INCLUDE[debugging-api-recommended-note](../../../../includes/debugging-api-recommended-note.md)]

## <a name="syntax"></a><span data-ttu-id="0e3a6-104">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="0e3a6-104">Syntax</span></span>

```
HRESULT Request(
    [in] IXCLRDataModule* pDataModule
);
```

### <a name="parameters"></a><span data-ttu-id="0e3a6-105">Parámetros</span><span class="sxs-lookup"><span data-stu-id="0e3a6-105">Parameters</span></span>

<span data-ttu-id="0e3a6-106">`pDataModule` [in] Un puntero al módulo de datos de inicialización.</span><span class="sxs-lookup"><span data-stu-id="0e3a6-106">`pDataModule` [in] A pointer to the seed data module.</span></span>

## <a name="remarks"></a><span data-ttu-id="0e3a6-107">Comentarios</span><span class="sxs-lookup"><span data-stu-id="0e3a6-107">Remarks</span></span>

<span data-ttu-id="0e3a6-108">Esta estructura reside en el tiempo de ejecución y no se expone a través de los encabezados o archivos de biblioteca.</span><span class="sxs-lookup"><span data-stu-id="0e3a6-108">This structure lives inside the runtime and is not exposed through any headers or library files.</span></span> <span data-ttu-id="0e3a6-109">Para ello, la manera más fácil es imitar la implementación:</span><span class="sxs-lookup"><span data-stu-id="0e3a6-109">To use it, the easiest way is to mimic the implementation:</span></span>

- <span data-ttu-id="0e3a6-110">Devolver el valor obtenido del que realiza la llamada la `Request` método en el `IXCLRDataModule*` parámetro con los siguientes parámetros: `((uint32) 0xf0000000, 0, 0, (uint32) sizeof(*this), (uint8*) this)`</span><span class="sxs-lookup"><span data-stu-id="0e3a6-110">Return the value obtained from calling the `Request` method on the `IXCLRDataModule*` parameter with the following parameters: `((uint32) 0xf0000000, 0, 0, (uint32) sizeof(*this), (uint8*) this)`</span></span>


## <a name="requirements"></a><span data-ttu-id="0e3a6-111">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0e3a6-111">Requirements</span></span>

<span data-ttu-id="0e3a6-112">**Plataformas:** Consulte [Requisitos del sistema](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="0e3a6-112">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
<span data-ttu-id="0e3a6-113">**Encabezado**: Ninguna</span><span class="sxs-lookup"><span data-stu-id="0e3a6-113">**Header:** None</span></span>     
<span data-ttu-id="0e3a6-114">**Biblioteca:** Ninguna</span><span class="sxs-lookup"><span data-stu-id="0e3a6-114">**Library:** None</span></span>  
<span data-ttu-id="0e3a6-115">**Versiones de .NET Framework:** [!INCLUDE[net_current_v47plus](../../../../includes/net-current-v47plus.md)]</span><span class="sxs-lookup"><span data-stu-id="0e3a6-115">**.NET Framework Versions:** [!INCLUDE[net_current_v47plus](../../../../includes/net-current-v47plus.md)]</span></span>  

## <a name="see-also"></a><span data-ttu-id="0e3a6-116">Vea también</span><span class="sxs-lookup"><span data-stu-id="0e3a6-116">See Also</span></span>

- [<span data-ttu-id="0e3a6-117">Depuración</span><span class="sxs-lookup"><span data-stu-id="0e3a6-117">Debugging</span></span>](../../../../docs/framework/unmanaged-api/debugging/index.md)
- [<span data-ttu-id="0e3a6-118">Interfaz DacpGetModuleAddress</span><span class="sxs-lookup"><span data-stu-id="0e3a6-118">DacpGetModuleAddress Interface</span></span>](../../../../docs/framework/unmanaged-api/debugging/dacpgetmoduleaddress-structure.md)