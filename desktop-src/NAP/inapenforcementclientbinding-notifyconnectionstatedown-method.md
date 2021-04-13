---
title: Метод Инапенфорцементклиентбиндинг Нотификоннектионстатедовн (Напенфорцементклиент. h)
description: Используется для информирования Напажент о том, что подключение к клиенту принудительного применения было прервано.
ms.assetid: 504c61c1-c8f9-46b8-87cd-c1f04846f0b3
keywords:
- Метод Нотификоннектионстатедовн NAP
- Метод Нотификоннектионстатедовн NAP, интерфейс Инапенфорцементклиентбиндинг
- Инапенфорцементклиентбиндинг интерфейса NAP, метод Нотификоннектионстатедовн
topic_type:
- apiref
api_name:
- INapEnforcementClientBinding.NotifyConnectionStateDown
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3129883342f493fd56a4cc81513910e8789ca4f1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104535609"
---
# <a name="inapenforcementclientbindingnotifyconnectionstatedown-method"></a><span data-ttu-id="b2724-106">Метод Инапенфорцементклиентбиндинг:: Нотификоннектионстатедовн</span><span class="sxs-lookup"><span data-stu-id="b2724-106">INapEnforcementClientBinding::NotifyConnectionStateDown method</span></span>

> [!Note]  
> <span data-ttu-id="b2724-107">Платформа защиты доступа к сети недоступна начиная с Windows 10</span><span class="sxs-lookup"><span data-stu-id="b2724-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="b2724-108">Метод **инапенфорцементклиентбиндинг:: нотификоннектионстатедовн** используется для информирования напажент о том, что подключение к клиенту принудительного применения было прервано.</span><span class="sxs-lookup"><span data-stu-id="b2724-108">The **INapEnforcementClientBinding::NotifyConnectionStateDown** method is used to inform the NapAgent that a connection to an enforcement client has gone down.</span></span>

## <a name="syntax"></a><span data-ttu-id="b2724-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="b2724-109">Syntax</span></span>


```C++
HRESULT NotifyConnectionStateDown(
  [in] INapEnforcementClientConnection *downCxn
);
```



## <a name="parameters"></a><span data-ttu-id="b2724-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="b2724-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b2724-111">*довнкксн* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="b2724-111">*downCxn* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b2724-112">Указатель COM на интерфейс [**инапенфорцементклиентконнектион**](inapenforcementclientconnection.md) соединения.</span><span class="sxs-lookup"><span data-stu-id="b2724-112">A COM pointer to the [**INapEnforcementClientConnection**](inapenforcementclientconnection.md) interface of the down connection.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b2724-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="b2724-113">Return value</span></span>

<span data-ttu-id="b2724-114">Также могут возвращаться другие коды ошибок, относящиеся к COM.</span><span class="sxs-lookup"><span data-stu-id="b2724-114">Other COM-specific error codes also may be returned.</span></span>



| <span data-ttu-id="b2724-115">Код возврата</span><span class="sxs-lookup"><span data-stu-id="b2724-115">Return code</span></span>                                                                                             | <span data-ttu-id="b2724-116">Описание</span><span class="sxs-lookup"><span data-stu-id="b2724-116">Description</span></span>                                                        |
|---------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <span data-ttu-id="b2724-117"><dt>**С \_ ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="b2724-117"><dt>**S\_OK** </dt></span></span> </dl>                   | <span data-ttu-id="b2724-118">Операция прошла успешно.</span><span class="sxs-lookup"><span data-stu-id="b2724-118">The operation is successful.</span></span><br/>                            |
| <dl> <span data-ttu-id="b2724-119"><dt>**Д \_ ACCESSDENIED**</dt></span><span class="sxs-lookup"><span data-stu-id="b2724-119"><dt>**E\_ACCESSDENIED** </dt></span></span> </dl>         | <span data-ttu-id="b2724-120">Ошибка разрешений, доступ запрещен.</span><span class="sxs-lookup"><span data-stu-id="b2724-120">Permissions error, access denied.</span></span><br/>                       |
| <dl> <span data-ttu-id="b2724-121"><dt>**Д \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="b2724-121"><dt>**E\_OUTOFMEMORY** </dt></span></span> </dl>          | <span data-ttu-id="b2724-122">Не удалось выполнить операцию из – за пределов системных ресурсов.</span><span class="sxs-lookup"><span data-stu-id="b2724-122">System resource limit, could not perform the operation.</span></span><br/> |
| <dl> <span data-ttu-id="b2724-123"><dt>**Защита доступа к сети \_ E \_ не \_ инициализирована**</dt></span><span class="sxs-lookup"><span data-stu-id="b2724-123"><dt>**NAP\_E\_NOT\_INITIALIZED**</dt></span></span> </dl> | <span data-ttu-id="b2724-124">Перед инициализацией не был инициализирован.</span><span class="sxs-lookup"><span data-stu-id="b2724-124">The enforcer has not been previously initialized.</span></span><br/>       |



 

## <a name="remarks"></a><span data-ttu-id="b2724-125">Комментарии</span><span class="sxs-lookup"><span data-stu-id="b2724-125">Remarks</span></span>

<span data-ttu-id="b2724-126">При отключении любого из подключений, установленных клиентом принудительного применения, клиент принудительного применения должен удалить подключение из активного списка и уведомить Напажент с помощью этого метода.</span><span class="sxs-lookup"><span data-stu-id="b2724-126">When any of the connections established by an enforcement client go down, the enforcement client should remove the connection from its active list and inform the NapAgent using this method.</span></span> <span data-ttu-id="b2724-127">Как только этот вызов возвращает, объект соединения может быть освобожден и освобожден.</span><span class="sxs-lookup"><span data-stu-id="b2724-127">As soon as this call returns, the connection object can be released and freed.</span></span> <span data-ttu-id="b2724-128">Напажент не будет содержать ссылки на объект Connection.</span><span class="sxs-lookup"><span data-stu-id="b2724-128">The NapAgent will not hold references to the connection object.</span></span>

<span data-ttu-id="b2724-129">В результате этого уведомления Напажент обновляет состояние NAP системы соответствующим образом.</span><span class="sxs-lookup"><span data-stu-id="b2724-129">As a result of this notification, the NapAgent updates its system NAP state as appropriate.</span></span>

<span data-ttu-id="b2724-130">Клиент принудительного применения должен вызвать метод [**инапенфорцементклиентбиндинг:: Initialize**](inapenforcementclientbinding-initialize-method.md) перед вызовом этого или любого другого метода интерфейса [**инапенфорцементклиентбиндинг**](inapenforcementclientbinding.md) .</span><span class="sxs-lookup"><span data-stu-id="b2724-130">The enforcement client must call the [**INapEnforcementClientBinding::Initialize**](inapenforcementclientbinding-initialize-method.md) method before calling this or any other method of the [**INapEnforcementClientBinding**](inapenforcementclientbinding.md) interface.</span></span>

## <a name="requirements"></a><span data-ttu-id="b2724-131">Требования</span><span class="sxs-lookup"><span data-stu-id="b2724-131">Requirements</span></span>



| <span data-ttu-id="b2724-132">Требование</span><span class="sxs-lookup"><span data-stu-id="b2724-132">Requirement</span></span> | <span data-ttu-id="b2724-133">Значение</span><span class="sxs-lookup"><span data-stu-id="b2724-133">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b2724-134">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="b2724-134">Minimum supported client</span></span><br/> | <span data-ttu-id="b2724-135">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="b2724-135">Windows Vista \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="b2724-136">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="b2724-136">Minimum supported server</span></span><br/> | <span data-ttu-id="b2724-137">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="b2724-137">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="b2724-138">Header</span><span class="sxs-lookup"><span data-stu-id="b2724-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="b2724-139"><dt>Напенфорцементклиент. h</dt></span><span class="sxs-lookup"><span data-stu-id="b2724-139"><dt>NapEnforcementClient.h</dt></span></span> </dl>   |
| <span data-ttu-id="b2724-140">IDL</span><span class="sxs-lookup"><span data-stu-id="b2724-140">IDL</span></span><br/>                      | <dl> <span data-ttu-id="b2724-141"><dt>Напенфорцементклиент. idl</dt></span><span class="sxs-lookup"><span data-stu-id="b2724-141"><dt>NapEnforcementClient.idl</dt></span></span> </dl> |
| <span data-ttu-id="b2724-142">DLL</span><span class="sxs-lookup"><span data-stu-id="b2724-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b2724-143"><dt>Qagent.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b2724-143"><dt>Qagent.dll</dt></span></span> </dl>               |



## <a name="see-also"></a><span data-ttu-id="b2724-144">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="b2724-144">See also</span></span>

<dl> <span data-ttu-id="b2724-145"><dt>


</dt> <dt></span><span class="sxs-lookup"><span data-stu-id="b2724-145"><dt>


</dt> <dt></span></span>

[<span data-ttu-id="b2724-146">**инапенфорцементклиентбиндинг**</span><span class="sxs-lookup"><span data-stu-id="b2724-146">**INapEnforcementClientBinding**</span></span>](inapenforcementclientbinding.md)
</dt> </dl>

 

 





