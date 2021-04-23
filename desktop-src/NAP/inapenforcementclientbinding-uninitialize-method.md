---
title: Метод Uninitialize Инапенфорцементклиентбиндинг (Напенфорцементклиент. h)
description: Завершает службу Напажент.
ms.assetid: 792600e5-586f-4858-8439-75761c928745
keywords:
- Отмена инициализации метода NAP
- Отмена инициализации метода NAP, интерфейс Инапенфорцементклиентбиндинг
- Инапенфорцементклиентбиндинг интерфейс NAP, метод Uninitialize
topic_type:
- apiref
api_name:
- INapEnforcementClientBinding.Uninitialize
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4132ff1a498a598483758623a588fa26e8b75021
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105661991"
---
# <a name="inapenforcementclientbindinguninitialize-method"></a><span data-ttu-id="9ae4d-106">Метод Инапенфорцементклиентбиндинг:: Uninitialize</span><span class="sxs-lookup"><span data-stu-id="9ae4d-106">INapEnforcementClientBinding::Uninitialize method</span></span>

> [!Note]  
> <span data-ttu-id="9ae4d-107">Платформа защиты доступа к сети недоступна начиная с Windows 10</span><span class="sxs-lookup"><span data-stu-id="9ae4d-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="9ae4d-108">Метод **инапенфорцементклиентбиндинг:: Uninitialize** завершает службу напажент.</span><span class="sxs-lookup"><span data-stu-id="9ae4d-108">The **INapEnforcementClientBinding::Uninitialize** method concludes the NapAgent service.</span></span>

## <a name="syntax"></a><span data-ttu-id="9ae4d-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="9ae4d-109">Syntax</span></span>


```C++
HRESULT Uninitialize();
```



## <a name="parameters"></a><span data-ttu-id="9ae4d-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="9ae4d-110">Parameters</span></span>

<span data-ttu-id="9ae4d-111">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="9ae4d-111">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="9ae4d-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="9ae4d-112">Return value</span></span>

<span data-ttu-id="9ae4d-113">Также могут возвращаться другие коды ошибок, относящиеся к COM.</span><span class="sxs-lookup"><span data-stu-id="9ae4d-113">Other COM-specific error codes also may be returned.</span></span>



| <span data-ttu-id="9ae4d-114">Код возврата</span><span class="sxs-lookup"><span data-stu-id="9ae4d-114">Return code</span></span>                                                                                     | <span data-ttu-id="9ae4d-115">Описание</span><span class="sxs-lookup"><span data-stu-id="9ae4d-115">Description</span></span>                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <span data-ttu-id="9ae4d-116"><dt>**С \_ ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="9ae4d-116"><dt>**S\_OK** </dt></span></span> </dl>           | <span data-ttu-id="9ae4d-117">Операция прошла успешно.</span><span class="sxs-lookup"><span data-stu-id="9ae4d-117">The operation is successful.</span></span><br/>                            |
| <dl> <span data-ttu-id="9ae4d-118"><dt>**Д \_ ACCESSDENIED**</dt></span><span class="sxs-lookup"><span data-stu-id="9ae4d-118"><dt>**E\_ACCESSDENIED** </dt></span></span> </dl> | <span data-ttu-id="9ae4d-119">Ошибка разрешений, доступ запрещен.</span><span class="sxs-lookup"><span data-stu-id="9ae4d-119">Permissions error, access denied.</span></span><br/>                       |
| <dl> <span data-ttu-id="9ae4d-120"><dt>**Д \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="9ae4d-120"><dt>**E\_OUTOFMEMORY** </dt></span></span> </dl>  | <span data-ttu-id="9ae4d-121">Не удалось выполнить операцию из – за пределов системных ресурсов.</span><span class="sxs-lookup"><span data-stu-id="9ae4d-121">System resource limit, could not perform the operation.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="9ae4d-122">Комментарии</span><span class="sxs-lookup"><span data-stu-id="9ae4d-122">Remarks</span></span>

<span data-ttu-id="9ae4d-123">Напажент блокирует дальнейшую обработку до завершения всех существующих вызовов интерфейсов [**инапенфорцементклиентбиндинг**](inapenforcementclientbinding.md) и [**инапенфорцементклиенткаллбакк**](inapenforcementclientcallback.md) .</span><span class="sxs-lookup"><span data-stu-id="9ae4d-123">The NapAgent blocks further processing until all existing calls on the [**INapEnforcementClientBinding**](inapenforcementclientbinding.md) and [**INapEnforcementClientCallback**](inapenforcementclientcallback.md) interfaces complete.</span></span> <span data-ttu-id="9ae4d-124">В конце этого вызова Напажент освобождает все ссылки на клиентские указатели COM на принудительное применение.</span><span class="sxs-lookup"><span data-stu-id="9ae4d-124">At the end of this call, the NapAgent releases all its references on enforcement client COM pointers.</span></span>

<span data-ttu-id="9ae4d-125">Перед вызовом этой функции необходимо вызвать [**инапенфорцементклиентбиндинг:: нотификоннектионстатедовн**](inapenforcementclientbinding-notifyconnectionstatedown-method.md) для всех активных соединений, чтобы SHA мог получать уведомления, если какие-либо из их SoH-Requests были потеряны.</span><span class="sxs-lookup"><span data-stu-id="9ae4d-125">Before this function is called, the enforcer must call [**INapEnforcementClientBinding::NotifyConnectionStateDown**](inapenforcementclientbinding-notifyconnectionstatedown-method.md) on all its active connections, so the SHAs can be notified if any of their SoH-Requests were orphaned.</span></span>

<span data-ttu-id="9ae4d-126">Клиент принудительного применения должен вызвать метод [**инапенфорцементклиентбиндинг:: Initialize**](inapenforcementclientbinding-initialize-method.md) перед вызовом этого или любого другого метода интерфейса [**инапенфорцементклиентбиндинг**](inapenforcementclientbinding.md) .</span><span class="sxs-lookup"><span data-stu-id="9ae4d-126">The enforcement client must call the [**INapEnforcementClientBinding::Initialize**](inapenforcementclientbinding-initialize-method.md) method before calling this or any other method of the [**INapEnforcementClientBinding**](inapenforcementclientbinding.md) interface.</span></span>

## <a name="requirements"></a><span data-ttu-id="9ae4d-127">Требования</span><span class="sxs-lookup"><span data-stu-id="9ae4d-127">Requirements</span></span>



| <span data-ttu-id="9ae4d-128">Требование</span><span class="sxs-lookup"><span data-stu-id="9ae4d-128">Requirement</span></span> | <span data-ttu-id="9ae4d-129">Значение</span><span class="sxs-lookup"><span data-stu-id="9ae4d-129">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9ae4d-130">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="9ae4d-130">Minimum supported client</span></span><br/> | <span data-ttu-id="9ae4d-131">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="9ae4d-131">Windows Vista \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="9ae4d-132">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="9ae4d-132">Minimum supported server</span></span><br/> | <span data-ttu-id="9ae4d-133">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="9ae4d-133">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="9ae4d-134">Header</span><span class="sxs-lookup"><span data-stu-id="9ae4d-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="9ae4d-135"><dt>Напенфорцементклиент. h</dt></span><span class="sxs-lookup"><span data-stu-id="9ae4d-135"><dt>NapEnforcementClient.h</dt></span></span> </dl>   |
| <span data-ttu-id="9ae4d-136">IDL</span><span class="sxs-lookup"><span data-stu-id="9ae4d-136">IDL</span></span><br/>                      | <dl> <span data-ttu-id="9ae4d-137"><dt>Напенфорцементклиент. idl</dt></span><span class="sxs-lookup"><span data-stu-id="9ae4d-137"><dt>NapEnforcementClient.idl</dt></span></span> </dl> |
| <span data-ttu-id="9ae4d-138">DLL</span><span class="sxs-lookup"><span data-stu-id="9ae4d-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9ae4d-139"><dt>Qagent.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9ae4d-139"><dt>Qagent.dll</dt></span></span> </dl>               |



## <a name="see-also"></a><span data-ttu-id="9ae4d-140">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="9ae4d-140">See also</span></span>

<dl> <span data-ttu-id="9ae4d-141"><dt>


</dt> <dt></span><span class="sxs-lookup"><span data-stu-id="9ae4d-141"><dt>


</dt> <dt></span></span>

[<span data-ttu-id="9ae4d-142">**инапенфорцементклиентбиндинг**</span><span class="sxs-lookup"><span data-stu-id="9ae4d-142">**INapEnforcementClientBinding**</span></span>](inapenforcementclientbinding.md)
</dt> <dt>

[<span data-ttu-id="9ae4d-143">**Инапенфорцементклиентбиндинг:: Нотификоннектионстатедовн**</span><span class="sxs-lookup"><span data-stu-id="9ae4d-143">**INapEnforcementClientBinding::NotifyConnectionStateDown**</span></span>](inapenforcementclientbinding-notifyconnectionstatedown-method.md)
</dt> <dt>

[<span data-ttu-id="9ae4d-144">**инапенфорцементклиенткаллбакк**</span><span class="sxs-lookup"><span data-stu-id="9ae4d-144">**INapEnforcementClientCallback**</span></span>](inapenforcementclientcallback.md)
</dt> </dl>

 

 





