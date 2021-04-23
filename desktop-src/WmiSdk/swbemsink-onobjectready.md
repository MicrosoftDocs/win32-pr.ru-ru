---
description: Событие Онобжектреади объекта Свбемсинк активируется, когда асинхронная операция возвращает объект.
ms.assetid: 14110ee7-a808-4786-b695-2ce54189d826
ms.tgt_platform: multiple
title: 'Событие Исвбемсинкевентс:: Онобжектреади (Wbemdisp. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemSink.OnObjectReady
- ISWbemSinkEvents.OnObjectReady
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 1fa803339e7007a030881c3d5b47d67f354b5661
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104155807"
---
# <a name="iswbemsinkeventsonobjectready-event"></a><span data-ttu-id="263ae-103">Событие Исвбемсинкевентс:: Онобжектреади</span><span class="sxs-lookup"><span data-stu-id="263ae-103">ISWbemSinkEvents::OnObjectReady event</span></span>

<span data-ttu-id="263ae-104">Событие **онобжектреади** объекта [**свбемсинк**](swbemsink.md) активируется, когда асинхронная операция возвращает объект.</span><span class="sxs-lookup"><span data-stu-id="263ae-104">The **OnObjectReady** event of an [**SWbemSink**](swbemsink.md) object is triggered when an asynchronous operation returns an object.</span></span> <span data-ttu-id="263ae-105">Это событие используется для обработки объектов из асинхронных вызовов, таких как [**SWbemObject \_ . инстанцесасинк**](swbemobject-instancesasync-.md) или [**SWbemServices.Exeккуерясинк**](swbemservices-execqueryasync.md).</span><span class="sxs-lookup"><span data-stu-id="263ae-105">Use this event to process objects from asynchronous calls such as [**SWbemObject.InstancesAsync\_**](swbemobject-instancesasync-.md) or [**SWbemServices.ExecQueryAsync**](swbemservices-execqueryasync.md).</span></span> <span data-ttu-id="263ae-106">**Онобжектреади** возвращает один [**SWbemObject**](swbemobject.md) каждый раз, пока перечисление не будет завершено.</span><span class="sxs-lookup"><span data-stu-id="263ae-106">**OnObjectReady** returns one [**SWbemObject**](swbemobject.md) each time until the enumeration is complete.</span></span>

<span data-ttu-id="263ae-107">Описание этого синтаксиса см. в разделе [соглашения о документе для API скриптов](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="263ae-107">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="263ae-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="263ae-108">Syntax</span></span>


```VB
SWbemSink.OnObjectReady( _
  ByVal objWbemObject, _
  ByVal objWbemAsyncContext _
)
```



## <a name="parameters"></a><span data-ttu-id="263ae-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="263ae-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="263ae-110">*обжвбемобжект*</span><span class="sxs-lookup"><span data-stu-id="263ae-110">*objWbemObject*</span></span> 
</dt> <dd>

<span data-ttu-id="263ae-111">Объект [**SWbemObject**](swbemobject.md) .</span><span class="sxs-lookup"><span data-stu-id="263ae-111">An [**SWbemObject**](swbemobject.md) object.</span></span> <span data-ttu-id="263ae-112">Это похоже на то, что возвращается синхронным эквивалентом асинхронного вызова, который запускает это событие.</span><span class="sxs-lookup"><span data-stu-id="263ae-112">This is similar to what is returned by the synchronous equivalent of the asynchronous call that triggers this event.</span></span> <span data-ttu-id="263ae-113">Например, вызов метода [**SwbemServices. Async**](swbemservices-getasync.md) возвращает **SWbemObject** в параметре *обжвбемобжект* события **онобжектреади** объекта [**свбемсинк**](swbemsink.md) , который передается как параметр *обжвбемобжект* исходного вызова.</span><span class="sxs-lookup"><span data-stu-id="263ae-113">For example, a call to the [**SWbemServices.GetAsync**](swbemservices-getasync.md) method returns an **SWbemObject** in the *objWbemObject* parameter of the **OnObjectReady** event of the [**SWbemSink**](swbemsink.md) object, which is passed as the *objWbemObject* parameter of the original call.</span></span> <span data-ttu-id="263ae-114">Один и тот же объект **SWbemObject** можно получить с помощью эквивалентного синхронного вызова [**SwbemServices. Get**](swbemservices-get.md).</span><span class="sxs-lookup"><span data-stu-id="263ae-114">The same **SWbemObject** object can be obtained by using an equivalent synchronous call to [**SWbemServices.Get**](swbemservices-get.md).</span></span>

</dd> <dt>

<span data-ttu-id="263ae-115">*обжвбемасинкконтекст*</span><span class="sxs-lookup"><span data-stu-id="263ae-115">*objWbemAsyncContext*</span></span> 
</dt> <dd>

<span data-ttu-id="263ae-116">Объект [**свбемнамедвалуесет**](swbemnamedvalueset.md) , который передается в исходный асинхронный вызов.</span><span class="sxs-lookup"><span data-stu-id="263ae-116">An [**SWbemNamedValueSet**](swbemnamedvalueset.md) object that is passed to the original asynchronous call.</span></span> <span data-ttu-id="263ae-117">Используйте этот параметр, чтобы указать происхождение асинхронного вызова, который активирует это событие, когда с помощью этого приемника объектов выполняется несколько асинхронных вызовов.</span><span class="sxs-lookup"><span data-stu-id="263ae-117">Use this parameter to identify the origin of the asynchronous call that triggers this event when multiple asynchronous calls are made using this object sink.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="263ae-118">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="263ae-118">Return value</span></span>

<span data-ttu-id="263ae-119">Это событие не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="263ae-119">This event does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="263ae-120">Коды ошибок</span><span class="sxs-lookup"><span data-stu-id="263ae-120">Error codes</span></span>

<span data-ttu-id="263ae-121">После завершения события **онобжектреади** объект [Err](/previous-versions//sbf5ze0e(v=vs.85)) может содержать один из кодов ошибок, приведенных ниже.</span><span class="sxs-lookup"><span data-stu-id="263ae-121">After the completion of the **OnObjectReady** event, the [Err](/previous-versions//sbf5ze0e(v=vs.85)) object may contain one of the error codes below.</span></span>

<dl> <dt>

<span data-ttu-id="263ae-122">**вбемеррфаилед** -2147749889 (0x80041001)</span><span class="sxs-lookup"><span data-stu-id="263ae-122">**wbemErrFailed** - 2147749889 (0x80041001)</span></span>
</dt> <dd>

<span data-ttu-id="263ae-123">Незаданная ошибка.</span><span class="sxs-lookup"><span data-stu-id="263ae-123">Unspecified error.</span></span>

</dd> <dt>

<span data-ttu-id="263ae-124">**вбемерраутофмемори** -2147749894 (0x80041006)</span><span class="sxs-lookup"><span data-stu-id="263ae-124">**wbemErrOutOfMemory** - 2147749894 (0x80041006)</span></span>
</dt> <dd>

<span data-ttu-id="263ae-125">Недостаточно памяти для завершения операции.</span><span class="sxs-lookup"><span data-stu-id="263ae-125">Not enough memory to complete the operation.</span></span>

</dd> <dt>

<span data-ttu-id="263ae-126">**вбемерртранспортфаилуре** -2147749909 (0x80041015)</span><span class="sxs-lookup"><span data-stu-id="263ae-126">**wbemErrTransportFailure** - 2147749909 (0x80041015)</span></span>
</dt> <dd>

<span data-ttu-id="263ae-127">Произошла сетевая ошибка, препятствующая нормальной работе.</span><span class="sxs-lookup"><span data-stu-id="263ae-127">Networking error occurred, preventing normal operation.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="263ae-128">Комментарии</span><span class="sxs-lookup"><span data-stu-id="263ae-128">Remarks</span></span>

<span data-ttu-id="263ae-129">Асинхронный обратный вызов позволяет пользователю без проверки подлинности предоставлять данные в приемник.</span><span class="sxs-lookup"><span data-stu-id="263ae-129">An asynchronous callback allows a non-authenticated user to provide data to the sink.</span></span> <span data-ttu-id="263ae-130">Это создает угрозы безопасности для сценариев и приложений.</span><span class="sxs-lookup"><span data-stu-id="263ae-130">This poses security risks to your scripts and applications.</span></span> <span data-ttu-id="263ae-131">Чтобы устранить риски, используйте либо частично синхронное соединение, либо синхронное взаимодействие.</span><span class="sxs-lookup"><span data-stu-id="263ae-131">To eliminate the risks, use either semi-synchronous communication or synchronous communication.</span></span> <span data-ttu-id="263ae-132">Дополнительные сведения см. [в разделе вызов метода](calling-a-method.md).</span><span class="sxs-lookup"><span data-stu-id="263ae-132">For more information, see [Calling a Method](calling-a-method.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="263ae-133">Требования</span><span class="sxs-lookup"><span data-stu-id="263ae-133">Requirements</span></span>



| <span data-ttu-id="263ae-134">Требование</span><span class="sxs-lookup"><span data-stu-id="263ae-134">Requirement</span></span> | <span data-ttu-id="263ae-135">Значение</span><span class="sxs-lookup"><span data-stu-id="263ae-135">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="263ae-136">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="263ae-136">Minimum supported client</span></span><br/> | <span data-ttu-id="263ae-137">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="263ae-137">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="263ae-138">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="263ae-138">Minimum supported server</span></span><br/> | <span data-ttu-id="263ae-139">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="263ae-139">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="263ae-140">Header</span><span class="sxs-lookup"><span data-stu-id="263ae-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="263ae-141"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="263ae-141"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="263ae-142">IDL</span><span class="sxs-lookup"><span data-stu-id="263ae-142">IDL</span></span><br/>                      | <dl> <span data-ttu-id="263ae-143"><dt>Wbemdisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="263ae-143"><dt>Wbemdisp.idl</dt></span></span> </dl> |
| <span data-ttu-id="263ae-144">DLL</span><span class="sxs-lookup"><span data-stu-id="263ae-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="263ae-145"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="263ae-145"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="263ae-146">CLSID</span><span class="sxs-lookup"><span data-stu-id="263ae-146">CLSID</span></span><br/>                    | <span data-ttu-id="263ae-147">\_СВБЕМСИНК CLSID</span><span class="sxs-lookup"><span data-stu-id="263ae-147">CLSID\_SWbemSink</span></span><br/>                                                             |
| <span data-ttu-id="263ae-148">IID</span><span class="sxs-lookup"><span data-stu-id="263ae-148">IID</span></span><br/>                      | <span data-ttu-id="263ae-149">IID \_ исвбемсинкевентс</span><span class="sxs-lookup"><span data-stu-id="263ae-149">IID\_ISWbemSinkEvents</span></span><br/>                                                        |



## <a name="see-also"></a><span data-ttu-id="263ae-150">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="263ae-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="263ae-151">**свбемсинк**</span><span class="sxs-lookup"><span data-stu-id="263ae-151">**SWbemSink**</span></span>](swbemsink.md)
</dt> </dl>

 

