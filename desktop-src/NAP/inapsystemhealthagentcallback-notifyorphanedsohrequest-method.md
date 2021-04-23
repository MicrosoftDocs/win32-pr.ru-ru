---
title: Метод Инапсистемхеалсаженткаллбакк Нотифйорфанедсохрекуест (Напсистемхеалсажент. h)
description: Вызывается, если Сохрекуест был получен запрос от SHA, но ответ никогда не был возвращен.
ms.assetid: 9e6fac6c-fb23-4725-ae0f-28ef8a6c4ea6
keywords:
- Метод Нотифйорфанедсохрекуест NAP
- Метод Нотифйорфанедсохрекуест NAP, интерфейс Инапсистемхеалсаженткаллбакк
- Инапсистемхеалсаженткаллбакк интерфейса NAP, метод Нотифйорфанедсохрекуест
topic_type:
- apiref
api_name:
- INapSystemHealthAgentCallback.NotifyOrphanedSoHRequest
api_location:
- NapSystemHealthAgent.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 676b67b61a9375f4fd44ecc41f9e56e92a97b693
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104416065"
---
# <a name="inapsystemhealthagentcallbacknotifyorphanedsohrequest-method"></a><span data-ttu-id="dd0d1-106">Метод Инапсистемхеалсаженткаллбакк:: Нотифйорфанедсохрекуест</span><span class="sxs-lookup"><span data-stu-id="dd0d1-106">INapSystemHealthAgentCallback::NotifyOrphanedSoHRequest method</span></span>

> [!Note]  
> <span data-ttu-id="dd0d1-107">Платформа защиты доступа к сети недоступна начиная с Windows 10</span><span class="sxs-lookup"><span data-stu-id="dd0d1-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="dd0d1-108">Метод **инапсистемхеалсаженткаллбакк:: нотифйорфанедсохрекуест** вызывается, если [**сохрекуест**](/windows/win32/api/naptypes/ns-naptypes-soh) был получен запрос от SHA, но ответ никогда не был возвращен.</span><span class="sxs-lookup"><span data-stu-id="dd0d1-108">The **INapSystemHealthAgentCallback::NotifyOrphanedSoHRequest** method is called if an [**SoHRequest**](/windows/win32/api/naptypes/ns-naptypes-soh) was queried from the SHA, but the response never came back.</span></span>

## <a name="syntax"></a><span data-ttu-id="dd0d1-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="dd0d1-109">Syntax</span></span>


```C++
HRESULT NotifyOrphanedSoHRequest(
  [in] const CorrelationId *correlationId
);
```



## <a name="parameters"></a><span data-ttu-id="dd0d1-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="dd0d1-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dd0d1-111">*correlationId* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="dd0d1-111">*correlationId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dd0d1-112">Указатель на уникальную структуру [**correlationId**](/windows/win32/api/naptypes/ns-naptypes-correlationid) , которая идентифицирует потерянный [**сохрекуест**](/windows/win32/api/naptypes/ns-naptypes-soh).</span><span class="sxs-lookup"><span data-stu-id="dd0d1-112">A pointer to the unique [**CorrelationId**](/windows/win32/api/naptypes/ns-naptypes-correlationid) structure that identifies the orphaned [**SoHRequest**](/windows/win32/api/naptypes/ns-naptypes-soh).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="dd0d1-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="dd0d1-113">Return value</span></span>

<span data-ttu-id="dd0d1-114">Этот метод может возвращать одно из этих значений.</span><span class="sxs-lookup"><span data-stu-id="dd0d1-114">This method can return one of these values.</span></span>



| <span data-ttu-id="dd0d1-115">Код возврата</span><span class="sxs-lookup"><span data-stu-id="dd0d1-115">Return code</span></span>                                                                          | <span data-ttu-id="dd0d1-116">Описание</span><span class="sxs-lookup"><span data-stu-id="dd0d1-116">Description</span></span>                   |
|--------------------------------------------------------------------------------------|-------------------------------|
| <dl> <span data-ttu-id="dd0d1-117"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="dd0d1-117"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="dd0d1-118">Указывает на успешное завершение.</span><span class="sxs-lookup"><span data-stu-id="dd0d1-118">Indicates success.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="dd0d1-119">Комментарии</span><span class="sxs-lookup"><span data-stu-id="dd0d1-119">Remarks</span></span>

<span data-ttu-id="dd0d1-120">Этот метод обратного вызова объявляется системой защиты доступа к сети и реализуется модулем записи SHA.</span><span class="sxs-lookup"><span data-stu-id="dd0d1-120">This callback method is declared by the NAP system and is to be implemented by the SHA writer.</span></span>

<span data-ttu-id="dd0d1-121">Этот метод может быть вызван системой в следующих случаях:</span><span class="sxs-lookup"><span data-stu-id="dd0d1-121">This method can be called by the system in the following cases:</span></span>

-   <span data-ttu-id="dd0d1-122">Не удалось отправить [**сохрекуест**](/windows/win32/api/naptypes/ns-naptypes-soh) по сети.</span><span class="sxs-lookup"><span data-stu-id="dd0d1-122">A [**SoHRequest**](/windows/win32/api/naptypes/ns-naptypes-soh) could not be sent on the wire.</span></span>
-   <span data-ttu-id="dd0d1-123">[**Сохрекуест**](/windows/win32/api/naptypes/ns-naptypes-soh) был отправлен по сети, но ни один из **сохреспонсе** не был возвращен, т. е. истекло время ожидания принудительного применения или нет соответствующего SHV на стороне сервера.</span><span class="sxs-lookup"><span data-stu-id="dd0d1-123">A [**SoHRequest**](/windows/win32/api/naptypes/ns-naptypes-soh) was sent on the wire, but no **SoHResponse** came back, i.e. the enforcer timed out or there was no corresponding SHV on the server-side.</span></span>
-   <span data-ttu-id="dd0d1-124">Подключение остановлено, или не был включен режим принудительной работы.</span><span class="sxs-lookup"><span data-stu-id="dd0d1-124">The connection went down or an enforcer went offline.</span></span>

<span data-ttu-id="dd0d1-125">Это наиболее актуальное уведомление, поэтому SHA не должен полагаться на эти сведения для очистки состояния.</span><span class="sxs-lookup"><span data-stu-id="dd0d1-125">This is only a best effort notification, so SHAs must not rely on this information to clean up state.</span></span> <span data-ttu-id="dd0d1-126">Существует несколько ситуаций, в которых SHA не будет уведомлен:</span><span class="sxs-lookup"><span data-stu-id="dd0d1-126">There are several situations in which an SHA will not be notified:</span></span>

-   <span data-ttu-id="dd0d1-127">Если поведение не действует, то есть не уведомляет SHA о том, что состояние подключения не работает.</span><span class="sxs-lookup"><span data-stu-id="dd0d1-127">If an enforcer misbehaves, i.e. it does not notify the SHA when the connection state is down.</span></span>
-   <span data-ttu-id="dd0d1-128">В случае сбоя принудительного применения.</span><span class="sxs-lookup"><span data-stu-id="dd0d1-128">If an enforcer crashes.</span></span>
-   <span data-ttu-id="dd0d1-129">В условиях ошибки, т. е. Напажент не хватает памяти.</span><span class="sxs-lookup"><span data-stu-id="dd0d1-129">In error conditions, i.e. the NapAgent is out of memory.</span></span>

<span data-ttu-id="dd0d1-130">SHA может получить некоторые ложные уведомления при первой привязке к Напажент, например, если происходит обмен данными о состоянии работоспособности при выполнении привязки SHA, а затем истекает время ожидания.</span><span class="sxs-lookup"><span data-stu-id="dd0d1-130">SHAs may get some spurious notifications when they first bind to the NapAgent, for instance, if an SoH exchange is in progress when the SHA bound, and then it times out.</span></span>

## <a name="requirements"></a><span data-ttu-id="dd0d1-131">Требования</span><span class="sxs-lookup"><span data-stu-id="dd0d1-131">Requirements</span></span>



| <span data-ttu-id="dd0d1-132">Требование</span><span class="sxs-lookup"><span data-stu-id="dd0d1-132">Requirement</span></span> | <span data-ttu-id="dd0d1-133">Значение</span><span class="sxs-lookup"><span data-stu-id="dd0d1-133">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="dd0d1-134">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="dd0d1-134">Minimum supported client</span></span><br/> | <span data-ttu-id="dd0d1-135">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="dd0d1-135">Windows Vista \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="dd0d1-136">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="dd0d1-136">Minimum supported server</span></span><br/> | <span data-ttu-id="dd0d1-137">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="dd0d1-137">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="dd0d1-138">Header</span><span class="sxs-lookup"><span data-stu-id="dd0d1-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="dd0d1-139"><dt>Напсистемхеалсажент. h</dt></span><span class="sxs-lookup"><span data-stu-id="dd0d1-139"><dt>NapSystemHealthAgent.h</dt></span></span> </dl>   |
| <span data-ttu-id="dd0d1-140">IDL</span><span class="sxs-lookup"><span data-stu-id="dd0d1-140">IDL</span></span><br/>                      | <dl> <span data-ttu-id="dd0d1-141"><dt>Напсистемхеалсажент. idl</dt></span><span class="sxs-lookup"><span data-stu-id="dd0d1-141"><dt>NapSystemHealthAgent.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="dd0d1-142">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="dd0d1-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dd0d1-143">**инапсистемхеалсаженткаллбакк**</span><span class="sxs-lookup"><span data-stu-id="dd0d1-143">**INapSystemHealthAgentCallback**</span></span>](inapsystemhealthagentcallback.md)
</dt> </dl>

 

 





