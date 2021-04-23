---
description: Если событие доступно, метод Некстевент объекта Свбемевентсаурце извлекает событие из запроса события.
ms.assetid: ff2d54d4-b8ee-4bb8-b6f7-081a1ca20489
ms.tgt_platform: multiple
title: Свбемевентсаурце. Некстевент, метод (Wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemEventSource.NextEvent
- ISWbemEventSource.NextEvent
- ISWbemEventSource.NextEvent
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 02fbc32557ab29c66849a4249d26cc2ca41564e6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105703173"
---
# <a name="swbemeventsourcenextevent-method"></a><span data-ttu-id="e655f-103">Свбемевентсаурце. Некстевент, метод</span><span class="sxs-lookup"><span data-stu-id="e655f-103">SWbemEventSource.NextEvent method</span></span>

<span data-ttu-id="e655f-104">Если событие доступно, метод **некстевент** объекта [**свбемевентсаурце**](swbemeventsource.md) извлекает событие из запроса события.</span><span class="sxs-lookup"><span data-stu-id="e655f-104">If an event is available, the **NextEvent** method of the [**SWbemEventSource**](swbemeventsource.md) object retrieves the event from an event query.</span></span>

<span data-ttu-id="e655f-105">Описание этого синтаксиса см. в разделе [соглашения о документе для API скриптов](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="e655f-105">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="e655f-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="e655f-106">Syntax</span></span>


```VB
objWbemObject = .NextEvent( _
  [ ByVal iTimeoutMs ] _
)
```



## <a name="parameters"></a><span data-ttu-id="e655f-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="e655f-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e655f-108">*итимеаутмс* \[ в необязательное\]</span><span class="sxs-lookup"><span data-stu-id="e655f-108">*iTimeoutMs* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="e655f-109">Число миллисекунд, в течение которых вызов ожидает события, прежде чем возвращать ошибку времени ожидания.</span><span class="sxs-lookup"><span data-stu-id="e655f-109">Number of milliseconds the call waits for an event before returning a time-out error.</span></span> <span data-ttu-id="e655f-110">Значение по умолчанию для этого параметра — **вбемтимеаутинфините** (-1), которое направляет вызов на неограниченное время ожидания.</span><span class="sxs-lookup"><span data-stu-id="e655f-110">The default value for this parameter is **wbemTimeoutInfinite** (-1), which directs the call to wait indefinitely.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e655f-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="e655f-111">Return value</span></span>

<span data-ttu-id="e655f-112">Если метод **некстевент** успешно выполнен, он возвращает объект [**SWbemObject**](swbemobject.md) , содержащий запрошенное событие.</span><span class="sxs-lookup"><span data-stu-id="e655f-112">If the **NextEvent** method is successful, it returns an [**SWbemObject**](swbemobject.md) object that contains the requested event.</span></span> <span data-ttu-id="e655f-113">Если время ожидания вызова истекло, возвращаемый объект имеет **значение NULL** и возникает ошибка.</span><span class="sxs-lookup"><span data-stu-id="e655f-113">If the call times out, the returned object is **NULL** and an error is raised.</span></span>

## <a name="error-codes"></a><span data-ttu-id="e655f-114">Коды ошибок</span><span class="sxs-lookup"><span data-stu-id="e655f-114">Error codes</span></span>

<span data-ttu-id="e655f-115">После завершения метода **некстевент** объект **Err** может содержать код ошибки из следующего списка.</span><span class="sxs-lookup"><span data-stu-id="e655f-115">Upon the completion of the **NextEvent** method, the **Err** object may contain the error code in the following list.</span></span>

<dl> <dt>

<span data-ttu-id="e655f-116">**вбемерртимедаут** — 0x80043001</span><span class="sxs-lookup"><span data-stu-id="e655f-116">**wbemErrTimedOut** - 0x80043001</span></span>
</dt> <dd>

<span data-ttu-id="e655f-117">Запрошенное событие не поступало в течение времени, указанного в *итимеаутмс.*</span><span class="sxs-lookup"><span data-stu-id="e655f-117">Requested event did not arrive in the amount of time specified in *iTimeoutMs.*</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="e655f-118">Требования</span><span class="sxs-lookup"><span data-stu-id="e655f-118">Requirements</span></span>



| <span data-ttu-id="e655f-119">Требование</span><span class="sxs-lookup"><span data-stu-id="e655f-119">Requirement</span></span> | <span data-ttu-id="e655f-120">Значение</span><span class="sxs-lookup"><span data-stu-id="e655f-120">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="e655f-121">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="e655f-121">Minimum supported client</span></span><br/> | <span data-ttu-id="e655f-122">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="e655f-122">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="e655f-123">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="e655f-123">Minimum supported server</span></span><br/> | <span data-ttu-id="e655f-124">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="e655f-124">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="e655f-125">Header</span><span class="sxs-lookup"><span data-stu-id="e655f-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="e655f-126"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="e655f-126"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="e655f-127">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="e655f-127">Type library</span></span><br/>             | <dl> <span data-ttu-id="e655f-128"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="e655f-128"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="e655f-129">DLL</span><span class="sxs-lookup"><span data-stu-id="e655f-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e655f-130"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e655f-130"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="e655f-131">CLSID</span><span class="sxs-lookup"><span data-stu-id="e655f-131">CLSID</span></span><br/>                    | <span data-ttu-id="e655f-132">\_СВБЕМЕВЕНТСАУРЦЕ CLSID</span><span class="sxs-lookup"><span data-stu-id="e655f-132">CLSID\_SWbemEventSource</span></span><br/>                                                      |
| <span data-ttu-id="e655f-133">IID</span><span class="sxs-lookup"><span data-stu-id="e655f-133">IID</span></span><br/>                      | <span data-ttu-id="e655f-134">IID \_ исвбемевентсаурце</span><span class="sxs-lookup"><span data-stu-id="e655f-134">IID\_ISWbemEventSource</span></span><br/>                                                       |



 

 




