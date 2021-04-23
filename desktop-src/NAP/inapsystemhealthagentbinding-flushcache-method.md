---
title: Метод Инапсистемхеалсажентбиндинг Флушкаче (Напсистемхеалсажент. h)
description: Вызывается SHA для сброса кэша SoH.
ms.assetid: a771ce03-1922-4e2d-9490-7ee9f693857c
keywords:
- Метод Флушкаче NAP
- Метод Флушкаче NAP, интерфейс Инапсистемхеалсажентбиндинг
- Инапсистемхеалсажентбиндинг интерфейса NAP, метод Флушкаче
topic_type:
- apiref
api_name:
- INapSystemHealthAgentBinding.FlushCache
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5ead6e496d220619439b80fdc5c7601675fdb7ca
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105672459"
---
# <a name="inapsystemhealthagentbindingflushcache-method"></a><span data-ttu-id="959e6-106">Метод Инапсистемхеалсажентбиндинг:: Флушкаче</span><span class="sxs-lookup"><span data-stu-id="959e6-106">INapSystemHealthAgentBinding::FlushCache method</span></span>

> [!Note]  
> <span data-ttu-id="959e6-107">Платформа защиты доступа к сети недоступна начиная с Windows 10</span><span class="sxs-lookup"><span data-stu-id="959e6-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="959e6-108">Метод **инапсистемхеалсажентбиндинг:: флушкаче** вызывается SHA для очистки кэша SoH.</span><span class="sxs-lookup"><span data-stu-id="959e6-108">The **INapSystemHealthAgentBinding::FlushCache** method is called by an SHA to flush its SoH cache.</span></span>

## <a name="syntax"></a><span data-ttu-id="959e6-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="959e6-109">Syntax</span></span>


```C++
HRESULT FlushCache();
```



## <a name="parameters"></a><span data-ttu-id="959e6-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="959e6-110">Parameters</span></span>

<span data-ttu-id="959e6-111">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="959e6-111">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="959e6-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="959e6-112">Return value</span></span>

<span data-ttu-id="959e6-113">Также могут возвращаться другие коды ошибок, относящиеся к COM.</span><span class="sxs-lookup"><span data-stu-id="959e6-113">Other COM-specific error codes also may be returned.</span></span>



| <span data-ttu-id="959e6-114">Код возврата</span><span class="sxs-lookup"><span data-stu-id="959e6-114">Return code</span></span>                                                                                         | <span data-ttu-id="959e6-115">Описание</span><span class="sxs-lookup"><span data-stu-id="959e6-115">Description</span></span>                                                                                                                    |
|-----------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="959e6-116"><dt>**С \_ ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="959e6-116"><dt>**S\_OK** </dt></span></span> </dl>               | <span data-ttu-id="959e6-117">Операция успешно завершена.</span><span class="sxs-lookup"><span data-stu-id="959e6-117">Operation succeeded.</span></span><br/>                                                                                                |
| <dl> <span data-ttu-id="959e6-118"><dt>**Д \_ ACCESSDENIED**</dt></span><span class="sxs-lookup"><span data-stu-id="959e6-118"><dt>**E\_ACCESSDENIED** </dt></span></span> </dl>     | <span data-ttu-id="959e6-119">Ошибка разрешений, доступ запрещен.</span><span class="sxs-lookup"><span data-stu-id="959e6-119">Permissions error, access denied.</span></span><br/>                                                                                   |
| <dl> <span data-ttu-id="959e6-120"><dt>**Д \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="959e6-120"><dt>**E\_OUTOFMEMORY** </dt></span></span> </dl>      | <span data-ttu-id="959e6-121">Не удалось выполнить операцию из – за пределов системных ресурсов.</span><span class="sxs-lookup"><span data-stu-id="959e6-121">System resource limit, could not perform the operation.</span></span><br/>                                                             |
| <dl> <span data-ttu-id="959e6-122"><dt>**RPC \_ E \_ отключен**</dt></span><span class="sxs-lookup"><span data-stu-id="959e6-122"><dt>**RPC\_E\_DISCONNECTED**</dt></span></span> </dl> | <span data-ttu-id="959e6-123">Напажент остановлен.</span><span class="sxs-lookup"><span data-stu-id="959e6-123">The NapAgent has been stopped.</span></span> <span data-ttu-id="959e6-124">После перезапуска этот объект будет автоматически восстановлен и повторно привязан к Напажент.</span><span class="sxs-lookup"><span data-stu-id="959e6-124">This object will recover automatically and rebind to the NapAgent, once it restarts.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="959e6-125">Комментарии</span><span class="sxs-lookup"><span data-stu-id="959e6-125">Remarks</span></span>

<span data-ttu-id="959e6-126">Напажент поддерживает кэш последних SoH, предоставляемых различными SHA.</span><span class="sxs-lookup"><span data-stu-id="959e6-126">The NapAgent maintains a cache of recent SoHs provided by different SHAs.</span></span> <span data-ttu-id="959e6-127">Этот кэш полезен для оптимизации производительности во время загрузки, когда SHA может быть привязан к системе.</span><span class="sxs-lookup"><span data-stu-id="959e6-127">This cache is useful to optimize boot-time performance, when SHAs may or may not be bound to the system.</span></span>

<span data-ttu-id="959e6-128">SHA должен вызвать метод [**Initialize**](inapsystemhealthagentbinding-initialize-method.md) перед вызовом этого метода или любого другого метода интерфейса [**INapSystemHealthAgentBinding2**](inapsystemhealthagentbinding2.md) .</span><span class="sxs-lookup"><span data-stu-id="959e6-128">The SHA must call [**Initialize**](inapsystemhealthagentbinding-initialize-method.md) before calling this method or any other method of the [**INapSystemHealthAgentBinding2**](inapsystemhealthagentbinding2.md) interface.</span></span>

## <a name="requirements"></a><span data-ttu-id="959e6-129">Требования</span><span class="sxs-lookup"><span data-stu-id="959e6-129">Requirements</span></span>



| <span data-ttu-id="959e6-130">Требование</span><span class="sxs-lookup"><span data-stu-id="959e6-130">Requirement</span></span> | <span data-ttu-id="959e6-131">Значение</span><span class="sxs-lookup"><span data-stu-id="959e6-131">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="959e6-132">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="959e6-132">Minimum supported client</span></span><br/> | <span data-ttu-id="959e6-133">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="959e6-133">Windows Vista \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="959e6-134">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="959e6-134">Minimum supported server</span></span><br/> | <span data-ttu-id="959e6-135">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="959e6-135">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="959e6-136">Header</span><span class="sxs-lookup"><span data-stu-id="959e6-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="959e6-137"><dt>Напсистемхеалсажент. h</dt></span><span class="sxs-lookup"><span data-stu-id="959e6-137"><dt>NapSystemHealthAgent.h</dt></span></span> </dl>   |
| <span data-ttu-id="959e6-138">IDL</span><span class="sxs-lookup"><span data-stu-id="959e6-138">IDL</span></span><br/>                      | <dl> <span data-ttu-id="959e6-139"><dt>Напсистемхеалсажент. idl</dt></span><span class="sxs-lookup"><span data-stu-id="959e6-139"><dt>NapSystemHealthAgent.idl</dt></span></span> </dl> |
| <span data-ttu-id="959e6-140">DLL</span><span class="sxs-lookup"><span data-stu-id="959e6-140">DLL</span></span><br/>                      | <dl> <span data-ttu-id="959e6-141"><dt>Qagent.dll</dt></span><span class="sxs-lookup"><span data-stu-id="959e6-141"><dt>Qagent.dll</dt></span></span> </dl>               |



## <a name="see-also"></a><span data-ttu-id="959e6-142">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="959e6-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="959e6-143">**инапсистемхеалсажентбиндинг**</span><span class="sxs-lookup"><span data-stu-id="959e6-143">**INapSystemHealthAgentBinding**</span></span>](inapsystemhealthagentbinding.md)
</dt> </dl>

 

 





