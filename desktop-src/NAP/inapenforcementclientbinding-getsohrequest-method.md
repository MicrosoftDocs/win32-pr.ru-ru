---
title: Метод Инапенфорцементклиентбиндинг Жетсохрекуест (Напенфорцементклиент. h)
description: Используется клиентом принудительного применения для получения запроса SoH об определенном соединении.
ms.assetid: 6fce6e84-ce03-48f2-957b-a41efe044fc5
keywords:
- Метод Жетсохрекуест NAP
- Метод Жетсохрекуест NAP, интерфейс Инапенфорцементклиентбиндинг
- Инапенфорцементклиентбиндинг интерфейса NAP, метод Жетсохрекуест
topic_type:
- apiref
api_name:
- INapEnforcementClientBinding.GetSoHRequest
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b9fed4872df7ab328ab241b070a9eeb07907de85
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103988446"
---
# <a name="inapenforcementclientbindinggetsohrequest-method"></a><span data-ttu-id="18fe3-106">Метод Инапенфорцементклиентбиндинг:: Жетсохрекуест</span><span class="sxs-lookup"><span data-stu-id="18fe3-106">INapEnforcementClientBinding::GetSoHRequest method</span></span>

> [!Note]  
> <span data-ttu-id="18fe3-107">Платформа защиты доступа к сети недоступна начиная с Windows 10</span><span class="sxs-lookup"><span data-stu-id="18fe3-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="18fe3-108">Метод **инапенфорцементклиентбиндинг:: жетсохрекуест** используется клиентом принудительного применения для получения запроса SoH для определенного соединения.</span><span class="sxs-lookup"><span data-stu-id="18fe3-108">The **INapEnforcementClientBinding::GetSoHRequest** method is used by the enforcement client to retrieve an SoH-request for a particular connection.</span></span>

## <a name="syntax"></a><span data-ttu-id="18fe3-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="18fe3-109">Syntax</span></span>


```C++
HRESULT GetSoHRequest(
  [in]  INapEnforcementClientConnection *connection,
  [out] BOOL                            *retriggerHint
);
```



## <a name="parameters"></a><span data-ttu-id="18fe3-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="18fe3-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="18fe3-111">*Подключение к* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="18fe3-111">*connection* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="18fe3-112">Указатель COM на интерфейс [**инапенфорцементклиентконнектион**](inapenforcementclientconnection.md) .</span><span class="sxs-lookup"><span data-stu-id="18fe3-112">A COM pointer to an [**INapEnforcementClientConnection**](inapenforcementclientconnection.md) interface.</span></span> <span data-ttu-id="18fe3-113">Напажент не хранит ссылки на объект, связанный с этим интерфейсом после завершения метода.</span><span class="sxs-lookup"><span data-stu-id="18fe3-113">The NapAgent does not hold references to the object associated with this interface after the method completes.</span></span>

</dd> <dt>

<span data-ttu-id="18fe3-114">*ретригжерхинт* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="18fe3-114">*retriggerHint* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="18fe3-115">Указатель на **логическое** значение, указывающее, следует ли повторно активировать соединение.</span><span class="sxs-lookup"><span data-stu-id="18fe3-115">A pointer to a **BOOL** that indicates if the connection should be re-triggered.</span></span> <span data-ttu-id="18fe3-116">Имеет **значение true** , если [**сохрекуест**](/windows/win32/api/naptypes/ns-naptypes-soh) изменился с момента последнего вызова функции или если срок действия [**пробатионтиме**](nap-datatypes.md) истек.</span><span class="sxs-lookup"><span data-stu-id="18fe3-116">It is **TRUE** if the [**SoHRequest**](/windows/win32/api/naptypes/ns-naptypes-soh) has changed since this function was last called or if [**ProbationTime**](nap-datatypes.md) has expired.</span></span> <span data-ttu-id="18fe3-117">В противном случае возвращается **значение false** .</span><span class="sxs-lookup"><span data-stu-id="18fe3-117">Otherwise, **FALSE** is returned.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="18fe3-118">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="18fe3-118">Return value</span></span>

<span data-ttu-id="18fe3-119">Также могут возвращаться другие коды ошибок, относящиеся к COM.</span><span class="sxs-lookup"><span data-stu-id="18fe3-119">Other COM-specific error codes also may be returned.</span></span>



| <span data-ttu-id="18fe3-120">Код возврата</span><span class="sxs-lookup"><span data-stu-id="18fe3-120">Return code</span></span>                                                                                             | <span data-ttu-id="18fe3-121">Описание</span><span class="sxs-lookup"><span data-stu-id="18fe3-121">Description</span></span>                                                        |
|---------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <span data-ttu-id="18fe3-122"><dt>**С \_ ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="18fe3-122"><dt>**S\_OK** </dt></span></span> </dl>                   | <span data-ttu-id="18fe3-123">Операция прошла успешно.</span><span class="sxs-lookup"><span data-stu-id="18fe3-123">The operation is successful.</span></span><br/>                            |
| <dl> <span data-ttu-id="18fe3-124"><dt>**Д \_ ACCESSDENIED**</dt></span><span class="sxs-lookup"><span data-stu-id="18fe3-124"><dt>**E\_ACCESSDENIED** </dt></span></span> </dl>         | <span data-ttu-id="18fe3-125">Ошибка разрешений, доступ запрещен.</span><span class="sxs-lookup"><span data-stu-id="18fe3-125">Permissions error, access denied.</span></span><br/>                       |
| <dl> <span data-ttu-id="18fe3-126"><dt>**Д \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="18fe3-126"><dt>**E\_OUTOFMEMORY** </dt></span></span> </dl>          | <span data-ttu-id="18fe3-127">Не удалось выполнить операцию из – за пределов системных ресурсов.</span><span class="sxs-lookup"><span data-stu-id="18fe3-127">System resource limit, could not perform the operation.</span></span><br/> |
| <dl> <span data-ttu-id="18fe3-128"><dt>**Защита доступа к сети \_ E \_ не \_ инициализирована**</dt></span><span class="sxs-lookup"><span data-stu-id="18fe3-128"><dt>**NAP\_E\_NOT\_INITIALIZED**</dt></span></span> </dl> | <span data-ttu-id="18fe3-129">Перед инициализацией не был инициализирован.</span><span class="sxs-lookup"><span data-stu-id="18fe3-129">The enforcer has not been previously initialized.</span></span><br/>       |



 

## <a name="remarks"></a><span data-ttu-id="18fe3-130">Комментарии</span><span class="sxs-lookup"><span data-stu-id="18fe3-130">Remarks</span></span>

<span data-ttu-id="18fe3-131">Напажент задает [**сохрекуест**](/windows/win32/api/naptypes/ns-naptypes-soh) для объекта соединения.</span><span class="sxs-lookup"><span data-stu-id="18fe3-131">The NapAgent sets the [**SoHRequest**](/windows/win32/api/naptypes/ns-naptypes-soh) on the connection object.</span></span>

<span data-ttu-id="18fe3-132">Если [**сохрекуест**](/windows/win32/api/naptypes/ns-naptypes-soh) был недоступен для этого подключения, он отбрасывается, а SHA получает уведомления о потерянном **сохрекуестс**.</span><span class="sxs-lookup"><span data-stu-id="18fe3-132">If an [**SoHRequest**](/windows/win32/api/naptypes/ns-naptypes-soh) was outstanding on this connection, then it is discarded, and the SHAs are notified of orphaned **SoHRequests**.</span></span>

<span data-ttu-id="18fe3-133">Клиент принудительного применения должен вызвать метод [**инапенфорцементклиентбиндинг:: Initialize**](inapenforcementclientbinding-initialize-method.md) перед вызовом этого или любого другого метода интерфейса [**инапенфорцементклиентбиндинг**](inapenforcementclientbinding.md) .</span><span class="sxs-lookup"><span data-stu-id="18fe3-133">The enforcement client must call the [**INapEnforcementClientBinding::Initialize**](inapenforcementclientbinding-initialize-method.md) method before calling this or any other method of the [**INapEnforcementClientBinding**](inapenforcementclientbinding.md) interface.</span></span>

## <a name="requirements"></a><span data-ttu-id="18fe3-134">Требования</span><span class="sxs-lookup"><span data-stu-id="18fe3-134">Requirements</span></span>



| <span data-ttu-id="18fe3-135">Требование</span><span class="sxs-lookup"><span data-stu-id="18fe3-135">Requirement</span></span> | <span data-ttu-id="18fe3-136">Значение</span><span class="sxs-lookup"><span data-stu-id="18fe3-136">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="18fe3-137">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="18fe3-137">Minimum supported client</span></span><br/> | <span data-ttu-id="18fe3-138">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="18fe3-138">Windows Vista \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="18fe3-139">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="18fe3-139">Minimum supported server</span></span><br/> | <span data-ttu-id="18fe3-140">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="18fe3-140">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="18fe3-141">Header</span><span class="sxs-lookup"><span data-stu-id="18fe3-141">Header</span></span><br/>                   | <dl> <span data-ttu-id="18fe3-142"><dt>Напенфорцементклиент. h</dt></span><span class="sxs-lookup"><span data-stu-id="18fe3-142"><dt>NapEnforcementClient.h</dt></span></span> </dl>   |
| <span data-ttu-id="18fe3-143">IDL</span><span class="sxs-lookup"><span data-stu-id="18fe3-143">IDL</span></span><br/>                      | <dl> <span data-ttu-id="18fe3-144"><dt>Напенфорцементклиент. idl</dt></span><span class="sxs-lookup"><span data-stu-id="18fe3-144"><dt>NapEnforcementClient.idl</dt></span></span> </dl> |
| <span data-ttu-id="18fe3-145">DLL</span><span class="sxs-lookup"><span data-stu-id="18fe3-145">DLL</span></span><br/>                      | <dl> <span data-ttu-id="18fe3-146"><dt>Qagent.dll</dt></span><span class="sxs-lookup"><span data-stu-id="18fe3-146"><dt>Qagent.dll</dt></span></span> </dl>               |



## <a name="see-also"></a><span data-ttu-id="18fe3-147">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="18fe3-147">See also</span></span>

<dl> <span data-ttu-id="18fe3-148"><dt>


</dt> <dt></span><span class="sxs-lookup"><span data-stu-id="18fe3-148"><dt>


</dt> <dt></span></span>

[<span data-ttu-id="18fe3-149">**инапенфорцементклиентбиндинг**</span><span class="sxs-lookup"><span data-stu-id="18fe3-149">**INapEnforcementClientBinding**</span></span>](inapenforcementclientbinding.md)
</dt> </dl>

 

 





