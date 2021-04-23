---
title: Метод Инапенфорцементклиенткаллбакк Нотифисохчанже (Напенфорцементклиент. h)
description: Используется Напажент для информирования клиента принудительного применения об изменениях состояния работоспособности.
ms.assetid: da8b9238-6371-4a6a-a9e7-ab791391ffc2
keywords:
- Метод Нотифисохчанже NAP
- Метод Нотифисохчанже NAP, интерфейс Инапенфорцементклиенткаллбакк
- Инапенфорцементклиенткаллбакк интерфейса NAP, метод Нотифисохчанже
topic_type:
- apiref
api_name:
- INapEnforcementClientCallback.NotifySoHChange
api_location:
- NapEnforcementClient.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6b405bca5ae27a68eea780dfcb922d1f986f475c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104137734"
---
# <a name="inapenforcementclientcallbacknotifysohchange-method"></a><span data-ttu-id="929ae-106">Метод Инапенфорцементклиенткаллбакк:: Нотифисохчанже</span><span class="sxs-lookup"><span data-stu-id="929ae-106">INapEnforcementClientCallback::NotifySoHChange method</span></span>

> [!Note]  
> <span data-ttu-id="929ae-107">Платформа защиты доступа к сети недоступна начиная с Windows 10</span><span class="sxs-lookup"><span data-stu-id="929ae-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="929ae-108">Метод обратного вызова **инапенфорцементклиенткаллбакк:: нотифисохчанже** используется напажент для информирования клиента принудительного применения об изменениях состояния работоспособности.</span><span class="sxs-lookup"><span data-stu-id="929ae-108">The **INapEnforcementClientCallback::NotifySoHChange** callback method is used by the NapAgent to inform the enforcement client of SoH changes.</span></span>

## <a name="syntax"></a><span data-ttu-id="929ae-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="929ae-109">Syntax</span></span>


```C++
HRESULT NotifySoHChange();
```



## <a name="parameters"></a><span data-ttu-id="929ae-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="929ae-110">Parameters</span></span>

<span data-ttu-id="929ae-111">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="929ae-111">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="929ae-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="929ae-112">Return value</span></span>

<span data-ttu-id="929ae-113">Этот метод обратного вызова должен возвращать один из следующих кодов ошибок.</span><span class="sxs-lookup"><span data-stu-id="929ae-113">This callback method must return one the following error codes.</span></span>



| <span data-ttu-id="929ae-114">Код возврата</span><span class="sxs-lookup"><span data-stu-id="929ae-114">Return code</span></span>                                                                                                | <span data-ttu-id="929ae-115">Описание</span><span class="sxs-lookup"><span data-stu-id="929ae-115">Description</span></span>                                                                                                                                                                                                           |
|------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="929ae-116"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="929ae-116"><dt>**S\_OK**</dt></span></span> </dl>                       | <span data-ttu-id="929ae-117">Верните это значение, если операция завершилась удачно.</span><span class="sxs-lookup"><span data-stu-id="929ae-117">Return this value if the operation succeeded.</span></span><br/>                                                                                                                                                              |
| <dl> <span data-ttu-id="929ae-118"><dt>**\_сервер RPC \_ S \_ недоступен**</dt></span><span class="sxs-lookup"><span data-stu-id="929ae-118"><dt>**RPC\_S\_SERVER\_UNAVAILABLE**</dt></span></span> </dl> | <span data-ttu-id="929ae-119">Возврат этого значения приводит к удалению принудительного применения из списка связанных-SHA и соответствующей записи кэша Напажент для записи на диск.</span><span class="sxs-lookup"><span data-stu-id="929ae-119">Returning this value causes the enforcer to be removed from the bound-SHA list, and the corresponding NapAgent cache entry to be flushed.</span></span> <span data-ttu-id="929ae-120">После этого сбой SHA может повторно инициализироваться с помощью Напажент.</span><span class="sxs-lookup"><span data-stu-id="929ae-120">The failing SHA can then re-initialize itself with the NapAgent.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="929ae-121">Комментарии</span><span class="sxs-lookup"><span data-stu-id="929ae-121">Remarks</span></span>

<span data-ttu-id="929ae-122">Завершение системного исправления — это событие изменения работоспособности системы.</span><span class="sxs-lookup"><span data-stu-id="929ae-122">The completion of system fix-up is a system health change event.</span></span> <span data-ttu-id="929ae-123">Это означает, что необходимо вызвать **нотифисохчанже** , когда уведомление [**Инапсистемхеалсаженткаллбакк:: жетфиксупинфо**](inapsystemhealthagentcallback-getfixupinfo-method.md) указывает на то, что клиент является фиксированным.</span><span class="sxs-lookup"><span data-stu-id="929ae-123">That means you must call **NotifySoHChange** when a [**INapSystemHealthAgentCallback::GetFixupInfo**](inapsystemhealthagentcallback-getfixupinfo-method.md) notification indicates that the client is fixed.</span></span> <span data-ttu-id="929ae-124">При фиксировании клиента элемент **State** структуры [**фиксупинфо**](/windows/win32/api/naptypes/ns-naptypes-fixupinfo) , возвращаемый **жетфиксупинфо** , имеет значение **фиксупстатесукцесс**.</span><span class="sxs-lookup"><span data-stu-id="929ae-124">When a client is fixed, the **state** member of the [**FixupInfo**](/windows/win32/api/naptypes/ns-naptypes-fixupinfo) structure returned by **GetFixupInfo** has a value of **fixupStateSuccess**.</span></span>

<span data-ttu-id="929ae-125">После вызова Напажент через этот обратный вызов агент принудительного применения должен вызвать [**инапенфорцементклиентбиндинг:: жетсохрекуест**](inapenforcementclientbinding-getsohrequest-method.md) , чтобы получить новый запрос.</span><span class="sxs-lookup"><span data-stu-id="929ae-125">After being called by the NapAgent via this callback, the enforcement agent must then call [**INapEnforcementClientBinding::GetSoHRequest**](inapenforcementclientbinding-getsohrequest-method.md) to retrieve the new request.</span></span> <span data-ttu-id="929ae-126">Этот вызов можно выполнить в том же потоке, что и **инапенфорцементклиенткаллбакк:: нотифисохчанже**.</span><span class="sxs-lookup"><span data-stu-id="929ae-126">This call can be made on the same thread as **INapEnforcementClientCallback::NotifySoHChange**.</span></span>

## <a name="requirements"></a><span data-ttu-id="929ae-127">Требования</span><span class="sxs-lookup"><span data-stu-id="929ae-127">Requirements</span></span>



| <span data-ttu-id="929ae-128">Требование</span><span class="sxs-lookup"><span data-stu-id="929ae-128">Requirement</span></span> | <span data-ttu-id="929ae-129">Значение</span><span class="sxs-lookup"><span data-stu-id="929ae-129">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="929ae-130">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="929ae-130">Minimum supported client</span></span><br/> | <span data-ttu-id="929ae-131">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="929ae-131">Windows Vista \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="929ae-132">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="929ae-132">Minimum supported server</span></span><br/> | <span data-ttu-id="929ae-133">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="929ae-133">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="929ae-134">Header</span><span class="sxs-lookup"><span data-stu-id="929ae-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="929ae-135"><dt>Напенфорцементклиент. h</dt></span><span class="sxs-lookup"><span data-stu-id="929ae-135"><dt>NapEnforcementClient.h</dt></span></span> </dl>   |
| <span data-ttu-id="929ae-136">IDL</span><span class="sxs-lookup"><span data-stu-id="929ae-136">IDL</span></span><br/>                      | <dl> <span data-ttu-id="929ae-137"><dt>Напенфорцементклиент. idl</dt></span><span class="sxs-lookup"><span data-stu-id="929ae-137"><dt>NapEnforcementClient.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="929ae-138">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="929ae-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="929ae-139">**инапенфорцементклиенткаллбакк**</span><span class="sxs-lookup"><span data-stu-id="929ae-139">**INapEnforcementClientCallback**</span></span>](inapenforcementclientcallback.md)
</dt> </dl>

 

 





