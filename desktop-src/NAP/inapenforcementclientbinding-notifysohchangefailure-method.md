---
title: Метод Инапенфорцементклиентбиндинг Нотифисохчанжефаилуре (Напенфорцементклиент. h)
description: Используется клиентом принудительного применения для информирования Напажент о том, что ему не удалось обработать предыдущее Инапенфорцементклиенткаллбакк Нотифисохчанже.
ms.assetid: 2de1626c-ffda-4191-90c4-72d0275965d9
keywords:
- Метод Нотифисохчанжефаилуре NAP
- Метод Нотифисохчанжефаилуре NAP, интерфейс Инапенфорцементклиентбиндинг
- Инапенфорцементклиентбиндинг интерфейса NAP, метод Нотифисохчанжефаилуре
topic_type:
- apiref
api_name:
- INapEnforcementClientBinding.NotifySoHChangeFailure
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: af23fd41e5a8b97064c089062eae13e93cf9ff0d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104493155"
---
# <a name="inapenforcementclientbindingnotifysohchangefailure-method"></a><span data-ttu-id="bb653-106">Метод Инапенфорцементклиентбиндинг:: Нотифисохчанжефаилуре</span><span class="sxs-lookup"><span data-stu-id="bb653-106">INapEnforcementClientBinding::NotifySoHChangeFailure method</span></span>

> [!Note]  
> <span data-ttu-id="bb653-107">Платформа защиты доступа к сети недоступна начиная с Windows 10</span><span class="sxs-lookup"><span data-stu-id="bb653-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="bb653-108">Метод **инапенфорцементклиентбиндинг:: нотифисохчанжефаилуре** используется клиентом принудительного применения для информирования напажент о том, что ему не удалось обработать предыдущий [**Инапенфорцементклиенткаллбакк:: NotifySoHChange**](inapenforcementclientcallback-notifysohchange-method.md).</span><span class="sxs-lookup"><span data-stu-id="bb653-108">The **INapEnforcementClientBinding::NotifySoHChangeFailure** method is used by the enforcement client to inform the NapAgent that it could not process a previous [**INapEnforcementClientCallback::NotifySoHChange**](inapenforcementclientcallback-notifysohchange-method.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="bb653-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="bb653-109">Syntax</span></span>


```C++
HRESULT NotifySoHChangeFailure();
```



## <a name="parameters"></a><span data-ttu-id="bb653-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="bb653-110">Parameters</span></span>

<span data-ttu-id="bb653-111">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="bb653-111">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="bb653-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="bb653-112">Return value</span></span>

<span data-ttu-id="bb653-113">Также могут возвращаться другие коды ошибок, относящиеся к COM.</span><span class="sxs-lookup"><span data-stu-id="bb653-113">Other COM-specific error codes also may be returned.</span></span>



| <span data-ttu-id="bb653-114">Код возврата</span><span class="sxs-lookup"><span data-stu-id="bb653-114">Return code</span></span>                                                                                             | <span data-ttu-id="bb653-115">Описание</span><span class="sxs-lookup"><span data-stu-id="bb653-115">Description</span></span>                                                        |
|---------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <span data-ttu-id="bb653-116"><dt>**С \_ ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="bb653-116"><dt>**S\_OK** </dt></span></span> </dl>                   | <span data-ttu-id="bb653-117">Операция прошла успешно.</span><span class="sxs-lookup"><span data-stu-id="bb653-117">The operation is successful.</span></span><br/>                            |
| <dl> <span data-ttu-id="bb653-118"><dt>**Д \_ ACCESSDENIED**</dt></span><span class="sxs-lookup"><span data-stu-id="bb653-118"><dt>**E\_ACCESSDENIED** </dt></span></span> </dl>         | <span data-ttu-id="bb653-119">Ошибка разрешений, доступ запрещен.</span><span class="sxs-lookup"><span data-stu-id="bb653-119">Permissions error, access denied.</span></span><br/>                       |
| <dl> <span data-ttu-id="bb653-120"><dt>**Д \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="bb653-120"><dt>**E\_OUTOFMEMORY** </dt></span></span> </dl>          | <span data-ttu-id="bb653-121">Не удалось выполнить операцию из – за пределов системных ресурсов.</span><span class="sxs-lookup"><span data-stu-id="bb653-121">System resource limit, could not perform the operation.</span></span><br/> |
| <dl> <span data-ttu-id="bb653-122"><dt>**Защита доступа к сети \_ E \_ не \_ инициализирована**</dt></span><span class="sxs-lookup"><span data-stu-id="bb653-122"><dt>**NAP\_E\_NOT\_INITIALIZED**</dt></span></span> </dl> | <span data-ttu-id="bb653-123">Перед инициализацией не был инициализирован.</span><span class="sxs-lookup"><span data-stu-id="bb653-123">The enforcer has not been previously initialized.</span></span><br/>       |



 

## <a name="remarks"></a><span data-ttu-id="bb653-124">Комментарии</span><span class="sxs-lookup"><span data-stu-id="bb653-124">Remarks</span></span>

<span data-ttu-id="bb653-125">В результате вызова этого метода Напажент повторные попытки применить изменение состояния работоспособности позже, вызвав [**инапенфорцементклиенткаллбакк:: нотифисохчанже**](inapenforcementclientcallback-notifysohchange-method.md) еще раз.</span><span class="sxs-lookup"><span data-stu-id="bb653-125">As a result of this method call the NapAgent retries applying the SoH change at a later time by calling [**INapEnforcementClientCallback::NotifySoHChange**](inapenforcementclientcallback-notifysohchange-method.md) again.</span></span> <span data-ttu-id="bb653-126">После того как клиент принудительного применения вызвал [**инапенфорцементклиентбиндинг:: жетсохрекуест**](inapenforcementclientbinding-getsohrequest-method.md), он должен применить изменение, т. е. сбои не обрабатываются напажент после этой точки.</span><span class="sxs-lookup"><span data-stu-id="bb653-126">Once the enforcement client has called [**INapEnforcementClientBinding::GetSoHRequest**](inapenforcementclientbinding-getsohrequest-method.md), it then must apply the change, i.e. no failures are handled by the NapAgent after this point.</span></span>

<span data-ttu-id="bb653-127">Клиент принудительного применения должен вызвать метод [**инапенфорцементклиентбиндинг:: Initialize**](inapenforcementclientbinding-initialize-method.md) перед вызовом этого или любого другого метода интерфейса [**инапенфорцементклиентбиндинг**](inapenforcementclientbinding.md) .</span><span class="sxs-lookup"><span data-stu-id="bb653-127">The enforcement client must call the [**INapEnforcementClientBinding::Initialize**](inapenforcementclientbinding-initialize-method.md) method before calling this or any other method of the [**INapEnforcementClientBinding**](inapenforcementclientbinding.md) interface.</span></span>

## <a name="requirements"></a><span data-ttu-id="bb653-128">Требования</span><span class="sxs-lookup"><span data-stu-id="bb653-128">Requirements</span></span>



| <span data-ttu-id="bb653-129">Требование</span><span class="sxs-lookup"><span data-stu-id="bb653-129">Requirement</span></span> | <span data-ttu-id="bb653-130">Значение</span><span class="sxs-lookup"><span data-stu-id="bb653-130">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bb653-131">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="bb653-131">Minimum supported client</span></span><br/> | <span data-ttu-id="bb653-132">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="bb653-132">Windows Vista \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="bb653-133">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="bb653-133">Minimum supported server</span></span><br/> | <span data-ttu-id="bb653-134">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="bb653-134">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="bb653-135">Header</span><span class="sxs-lookup"><span data-stu-id="bb653-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="bb653-136"><dt>Напенфорцементклиент. h</dt></span><span class="sxs-lookup"><span data-stu-id="bb653-136"><dt>NapEnforcementClient.h</dt></span></span> </dl>   |
| <span data-ttu-id="bb653-137">IDL</span><span class="sxs-lookup"><span data-stu-id="bb653-137">IDL</span></span><br/>                      | <dl> <span data-ttu-id="bb653-138"><dt>Напенфорцементклиент. idl</dt></span><span class="sxs-lookup"><span data-stu-id="bb653-138"><dt>NapEnforcementClient.idl</dt></span></span> </dl> |
| <span data-ttu-id="bb653-139">DLL</span><span class="sxs-lookup"><span data-stu-id="bb653-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="bb653-140"><dt>Qagent.dll</dt></span><span class="sxs-lookup"><span data-stu-id="bb653-140"><dt>Qagent.dll</dt></span></span> </dl>               |



## <a name="see-also"></a><span data-ttu-id="bb653-141">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="bb653-141">See also</span></span>

<dl> <span data-ttu-id="bb653-142"><dt>


</dt> <dt></span><span class="sxs-lookup"><span data-stu-id="bb653-142"><dt>


</dt> <dt></span></span>

[<span data-ttu-id="bb653-143">**инапенфорцементклиентбиндинг**</span><span class="sxs-lookup"><span data-stu-id="bb653-143">**INapEnforcementClientBinding**</span></span>](inapenforcementclientbinding.md)
</dt> <dt>

[<span data-ttu-id="bb653-144">**Инапенфорцементклиентбиндинг:: Жетсохрекуест**</span><span class="sxs-lookup"><span data-stu-id="bb653-144">**INapEnforcementClientBinding::GetSoHRequest**</span></span>](inapenforcementclientbinding-getsohrequest-method.md)
</dt> <dt>

[<span data-ttu-id="bb653-145">**Инапенфорцементклиенткаллбакк:: Нотифисохчанже**</span><span class="sxs-lookup"><span data-stu-id="bb653-145">**INapEnforcementClientCallback::NotifySoHChange**</span></span>](inapenforcementclientcallback-notifysohchange-method.md)
</dt> </dl>

 

 





