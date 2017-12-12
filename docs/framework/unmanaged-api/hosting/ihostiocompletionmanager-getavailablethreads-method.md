---
title: "IHostIoCompletionManager::GetAvailableThreads (Método)"
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-clr
ms.tgt_pltfrm: 
ms.topic: reference
api_name: IHostIoCompletionManager.GetAvailableThreads
api_location: mscoree.dll
api_type: COM
f1_keywords: IHostIoCompletionManager::GetAvailableThreads
helpviewer_keywords:
- GetAvailableThreads method, IHostIoCompletionManager interface [.NET Framework hosting]
- IHostIoCompletionManager::GetAvailableThreads method [.NET Framework hosting]
ms.assetid: bab363d1-b859-47a4-9884-5661c611cce7
topic_type: apiref
caps.latest.revision: "9"
author: rpetrusha
ms.author: ronpet
manager: wpickett
ms.openlocfilehash: f06e9fe0d07258fca107413d9ad328329b5456b6
ms.sourcegitcommit: 4f3fef493080a43e70e951223894768d36ce430a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/21/2017
---
# <a name="ihostiocompletionmanagergetavailablethreads-method"></a><span data-ttu-id="3e76b-102">IHostIoCompletionManager::GetAvailableThreads (Método)</span><span class="sxs-lookup"><span data-stu-id="3e76b-102">IHostIoCompletionManager::GetAvailableThreads Method</span></span>
<span data-ttu-id="3e76b-103">Obtiene el número de subprocesos de finalización de E/S, del número total de subprocesos administrados por el host, que no están atendiendo solicitudes actualmente.</span><span class="sxs-lookup"><span data-stu-id="3e76b-103">Gets the number of I/O completion threads, of the total number of threads managed by the host, that are not currently servicing requests.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="3e76b-104">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="3e76b-104">Syntax</span></span>  
  
```  
HRESULT GetAvailableThreads (  
    [out] DWORD *pdwAvailableIoCompletionThreads  
);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="3e76b-105">Parámetros</span><span class="sxs-lookup"><span data-stu-id="3e76b-105">Parameters</span></span>  
 `pdwAvailableIoCompletionThreads`  
 <span data-ttu-id="3e76b-106">[out] Un puntero al número de subprocesos de finalización de E/S administrados por el host que están actualmente disponibles para atender las solicitudes.</span><span class="sxs-lookup"><span data-stu-id="3e76b-106">[out] A pointer to the number of I/O completion threads managed by the host that are currently available to service requests.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="3e76b-107">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="3e76b-107">Return Value</span></span>  
  
|<span data-ttu-id="3e76b-108">HRESULT</span><span class="sxs-lookup"><span data-stu-id="3e76b-108">HRESULT</span></span>|<span data-ttu-id="3e76b-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="3e76b-109">Description</span></span>|  
|-------------|-----------------|  
|<span data-ttu-id="3e76b-110">S_OK</span><span class="sxs-lookup"><span data-stu-id="3e76b-110">S_OK</span></span>|<span data-ttu-id="3e76b-111">`GetAvailableThreads`se devolvió correctamente.</span><span class="sxs-lookup"><span data-stu-id="3e76b-111">`GetAvailableThreads` returned successfully.</span></span>|  
|<span data-ttu-id="3e76b-112">HOST_E_CLRNOTAVAILABLE</span><span class="sxs-lookup"><span data-stu-id="3e76b-112">HOST_E_CLRNOTAVAILABLE</span></span>|<span data-ttu-id="3e76b-113">Common language runtime (CLR) no se han cargado en un proceso o el CLR está en un estado en el que no se puede ejecutar código administrado o procesar la llamada correctamente.</span><span class="sxs-lookup"><span data-stu-id="3e76b-113">The common language runtime (CLR) has not been loaded into a process, or the CLR is in a state in which it cannot run managed code or process the call successfully.</span></span>|  
|<span data-ttu-id="3e76b-114">HOST_E_TIMEOUT</span><span class="sxs-lookup"><span data-stu-id="3e76b-114">HOST_E_TIMEOUT</span></span>|<span data-ttu-id="3e76b-115">La llamada agotó el tiempo de espera.</span><span class="sxs-lookup"><span data-stu-id="3e76b-115">The call timed out.</span></span>|  
|<span data-ttu-id="3e76b-116">HOST_E_NOT_OWNER</span><span class="sxs-lookup"><span data-stu-id="3e76b-116">HOST_E_NOT_OWNER</span></span>|<span data-ttu-id="3e76b-117">El llamador no posee el bloqueo.</span><span class="sxs-lookup"><span data-stu-id="3e76b-117">The caller does not own the lock.</span></span>|  
|<span data-ttu-id="3e76b-118">HOST_E_ABANDONED</span><span class="sxs-lookup"><span data-stu-id="3e76b-118">HOST_E_ABANDONED</span></span>|<span data-ttu-id="3e76b-119">Se canceló un evento mientras un subproceso bloqueado o fibra esperó en él.</span><span class="sxs-lookup"><span data-stu-id="3e76b-119">An event was canceled while a blocked thread or fiber was waiting on it.</span></span>|  
|<span data-ttu-id="3e76b-120">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="3e76b-120">E_FAIL</span></span>|<span data-ttu-id="3e76b-121">Se ha producido un error catastrófico desconocido.</span><span class="sxs-lookup"><span data-stu-id="3e76b-121">An unknown catastrophic failure occurred.</span></span> <span data-ttu-id="3e76b-122">Cuando un método devuelve E_FAIL, CLR ya no es utilizable dentro del proceso.</span><span class="sxs-lookup"><span data-stu-id="3e76b-122">When a method returns E_FAIL, the CLR is no longer usable within the process.</span></span> <span data-ttu-id="3e76b-123">Las llamadas posteriores a métodos de hospedaje devuelven HOST_E_CLRNOTAVAILABLE.</span><span class="sxs-lookup"><span data-stu-id="3e76b-123">Subsequent calls to hosting methods return HOST_E_CLRNOTAVAILABLE.</span></span>|  
|<span data-ttu-id="3e76b-124">E_NOTIMPL</span><span class="sxs-lookup"><span data-stu-id="3e76b-124">E_NOTIMPL</span></span>|<span data-ttu-id="3e76b-125">El host no proporciona una implementación de `GetAvailableThreads`.</span><span class="sxs-lookup"><span data-stu-id="3e76b-125">The host does not provide an implementation of `GetAvailableThreads`.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="3e76b-126">Comentarios</span><span class="sxs-lookup"><span data-stu-id="3e76b-126">Remarks</span></span>  
 <span data-ttu-id="3e76b-127">Un host podría desear el control exclusivo sobre el tamaño del grupo de subprocesos de finalización de E/S, por razones de implementación, rendimiento o escalabilidad.</span><span class="sxs-lookup"><span data-stu-id="3e76b-127">A host might want exclusive control over the size of the I/O completion thread pool, for reasons such as implementation, performance, or scalability.</span></span> <span data-ttu-id="3e76b-128">Por lo tanto, el host no tiene que implementar `GetAvailableThreads`.</span><span class="sxs-lookup"><span data-stu-id="3e76b-128">Therefore, the host is not required to implement `GetAvailableThreads`.</span></span> <span data-ttu-id="3e76b-129">En este caso, el host debe devolver E_NOTIMPL desde este método.</span><span class="sxs-lookup"><span data-stu-id="3e76b-129">In this case, the host should return E_NOTIMPL from this method.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="3e76b-130">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3e76b-130">Requirements</span></span>  
 <span data-ttu-id="3e76b-131">**Plataformas:** vea [requisitos del sistema](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="3e76b-131">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="3e76b-132">**Encabezado:** MSCorEE.h</span><span class="sxs-lookup"><span data-stu-id="3e76b-132">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="3e76b-133">**Biblioteca:** incluye como recurso en MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="3e76b-133">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="3e76b-134">**Versiones de .NET framework:**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="3e76b-134">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="3e76b-135">Vea también</span><span class="sxs-lookup"><span data-stu-id="3e76b-135">See Also</span></span>  
 [<span data-ttu-id="3e76b-136">ICLRIoCompletionManager (interfaz)</span><span class="sxs-lookup"><span data-stu-id="3e76b-136">ICLRIoCompletionManager Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/iclriocompletionmanager-interface.md)  
 [<span data-ttu-id="3e76b-137">IHostIoCompletionManager (interfaz)</span><span class="sxs-lookup"><span data-stu-id="3e76b-137">IHostIoCompletionManager Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/ihostiocompletionmanager-interface.md)