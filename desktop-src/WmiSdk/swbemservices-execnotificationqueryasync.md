---
description: Выполняет запрос для получения событий.
ms.assetid: 0b0e8313-4ffd-4d4a-8965-d2c6743e7573
ms.tgt_platform: multiple
title: SWbemServices.Exeметод Кнотификатионкуерясинк (Wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemServices.ExecNotificationQueryAsync
- ISWbemServices.ExecNotificationQueryAsync
- ISWbemServices.ExecNotificationQueryAsync
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 8e2ecddf290d83583b3108620b8b4bb23be7c957
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105711624"
---
# <a name="swbemservicesexecnotificationqueryasync-method"></a><span data-ttu-id="d1c0e-103">SWbemServices.Exeметод Кнотификатионкуерясинк</span><span class="sxs-lookup"><span data-stu-id="d1c0e-103">SWbemServices.ExecNotificationQueryAsync method</span></span>

<span data-ttu-id="d1c0e-104">Метод **ExecNotificationQueryAsync** объекта [**SwbemServices**](swbemservices.md) выполняет запрос для получения событий.</span><span class="sxs-lookup"><span data-stu-id="d1c0e-104">The **ExecNotificationQueryAsync** method of the [**SWbemServices**](swbemservices.md) object executes a query to receive events.</span></span> <span data-ttu-id="d1c0e-105">Этот вызов возвращает немедленно, а результаты и состояние возвращаются вызывающему через события, доставляемые в приемник, указанный в *обжвбемсинк*.</span><span class="sxs-lookup"><span data-stu-id="d1c0e-105">This call returns immediately and the results and status are returned to the caller through events delivered to the sink that is specified in *objWbemSink*.</span></span>

<span data-ttu-id="d1c0e-106">События, указанные в запросе, могут быть встроенными событиями инструментарий управления Windows (WMI) (WMI), такими как [**\_ \_ инстанцекреатионевент**](--instancecreationevent.md)или внешние события, такие как [**Win32 \_ IP4RouteTableEvent**](/previous-versions/windows/desktop/wmiiprouteprov/win32-ip4routetableevent) или [**регистрикэйчанжеевент**](/previous-versions/windows/desktop/regprov/registrykeychangeevent).</span><span class="sxs-lookup"><span data-stu-id="d1c0e-106">The events that are specified in the query can be intrinsic Windows Management Instrumentation (WMI) events, such as [**\_\_InstanceCreationEvent**](--instancecreationevent.md), or extrinsic events, such as [**Win32\_IP4RouteTableEvent**](/previous-versions/windows/desktop/wmiiprouteprov/win32-ip4routetableevent) or [**RegistryKeyChangeEvent**](/previous-versions/windows/desktop/regprov/registrykeychangeevent).</span></span> <span data-ttu-id="d1c0e-107">Дополнительные сведения см. [в разделе Определение типа получаемого события](determining-the-type-of-event-to-receive.md).</span><span class="sxs-lookup"><span data-stu-id="d1c0e-107">For more information, see [Determining the Type of Event to Receive](determining-the-type-of-event-to-receive.md).</span></span>

<span data-ttu-id="d1c0e-108">Метод вызывается в асинхронном режиме.</span><span class="sxs-lookup"><span data-stu-id="d1c0e-108">The method is called in the asynchronous mode.</span></span> <span data-ttu-id="d1c0e-109">Дополнительные сведения см. [в разделе вызов метода](calling-a-method.md).</span><span class="sxs-lookup"><span data-stu-id="d1c0e-109">For more information, see [Calling a Method](calling-a-method.md).</span></span>

<span data-ttu-id="d1c0e-110">Описание этого синтаксиса см. в разделе [соглашения о документе для API скриптов](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="d1c0e-110">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="d1c0e-111">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="d1c0e-111">Syntax</span></span>


```VB
SWbemServices.ExecNotificationQueryAsync( _
  ByVal objWbemSink, _
  ByVal strQuery, _
  [ ByVal strQueryLanguage ], _
  [ ByVal iFlags ], _
  [ ByVal objwbemNamedValueSet ], _
  [ ByVal objWbemAsyncContext ] _
)
```



## <a name="parameters"></a><span data-ttu-id="d1c0e-112">Параметры</span><span class="sxs-lookup"><span data-stu-id="d1c0e-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d1c0e-113">*обжвбемсинк*</span><span class="sxs-lookup"><span data-stu-id="d1c0e-113">*objWbemSink*</span></span> 
</dt> <dd>

<span data-ttu-id="d1c0e-114">Обязательный.</span><span class="sxs-lookup"><span data-stu-id="d1c0e-114">Required.</span></span> <span data-ttu-id="d1c0e-115">Приемник объекта, который асинхронно получает уведомления о событиях.</span><span class="sxs-lookup"><span data-stu-id="d1c0e-115">Object sink that receives the notification of events asynchronously.</span></span> <span data-ttu-id="d1c0e-116">Создайте объект [**свбемсинк**](swbemsink.md) для получения объектов.</span><span class="sxs-lookup"><span data-stu-id="d1c0e-116">Create a [**SWbemSink**](swbemsink.md) object to receive the objects.</span></span>

</dd> <dt>

<span data-ttu-id="d1c0e-117">*стркуери*</span><span class="sxs-lookup"><span data-stu-id="d1c0e-117">*strQuery*</span></span> 
</dt> <dd>

<span data-ttu-id="d1c0e-118">Обязательный.</span><span class="sxs-lookup"><span data-stu-id="d1c0e-118">Required.</span></span> <span data-ttu-id="d1c0e-119">Строка, содержащая текст запроса, связанного с событием.</span><span class="sxs-lookup"><span data-stu-id="d1c0e-119">String that contains the text of the event-related query.</span></span> <span data-ttu-id="d1c0e-120">Этот параметр не может быть пустым.</span><span class="sxs-lookup"><span data-stu-id="d1c0e-120">This parameter cannot be blank.</span></span> <span data-ttu-id="d1c0e-121">Дополнительные сведения о создании строк запросов WMI см. в разделе [запросы с помощью WQL](querying-with-wql.md) и Справочник по [WQL](wql-sql-for-wmi.md) .</span><span class="sxs-lookup"><span data-stu-id="d1c0e-121">For more information on building WMI query strings, see [Querying with WQL](querying-with-wql.md) and the [WQL](wql-sql-for-wmi.md) reference.</span></span>

</dd> <dt>

<span data-ttu-id="d1c0e-122">*стркуерилангуаже* \[ используемых\]</span><span class="sxs-lookup"><span data-stu-id="d1c0e-122">*strQueryLanguage* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="d1c0e-123">Строка, содержащая используемый язык запросов.</span><span class="sxs-lookup"><span data-stu-id="d1c0e-123">String that contains the query language to be used.</span></span> <span data-ttu-id="d1c0e-124">Если указано, это значение должно быть "WQL".</span><span class="sxs-lookup"><span data-stu-id="d1c0e-124">If specified, this value must be "WQL".</span></span>

</dd> <dt>

<span data-ttu-id="d1c0e-125">*ифлагс* \[ используемых\]</span><span class="sxs-lookup"><span data-stu-id="d1c0e-125">*iFlags* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="d1c0e-126">Целое число, определяющее поведение запроса.</span><span class="sxs-lookup"><span data-stu-id="d1c0e-126">Integer that determines the behavior of the query.</span></span> <span data-ttu-id="d1c0e-127">Для этого параметра можно задать следующие значения.</span><span class="sxs-lookup"><span data-stu-id="d1c0e-127">This parameter can be set to the following values.</span></span>

<dt>

<span id="wbemFlagSendStatus"></span><span id="wbemflagsendstatus"></span><span id="WBEMFLAGSENDSTATUS"></span>

<span data-ttu-id="d1c0e-128"><span id="wbemFlagSendStatus"></span><span id="wbemflagsendstatus"></span><span id="WBEMFLAGSENDSTATUS"></span>Вбемфлагсендстатус \* \* \* \* (128 (0x80))</span><span class="sxs-lookup"><span data-stu-id="d1c0e-128"><span id="wbemFlagSendStatus"></span><span id="wbemflagsendstatus"></span><span id="WBEMFLAGSENDSTATUS"></span>\*\*\*\*wbemFlagSendStatus\*\*\*\* (128 (0x80))</span></span>


</dt> <dd>

<span data-ttu-id="d1c0e-129">Вызывает асинхронные вызовы для отправки обновлений состояния обработчику событий [**OnProgress**](swbemsink-onprogress.md) для приемника объекта.</span><span class="sxs-lookup"><span data-stu-id="d1c0e-129">Causes asynchronous calls to send status updates to the [**OnProgress**](swbemsink-onprogress.md) event handler for the object sink.</span></span>

</dd> <dt>

<span id="wbemFlagDontSendStatus"></span><span id="wbemflagdontsendstatus"></span><span id="WBEMFLAGDONTSENDSTATUS"></span>

<span data-ttu-id="d1c0e-130"><span id="wbemFlagDontSendStatus"></span><span id="wbemflagdontsendstatus"></span><span id="WBEMFLAGDONTSENDSTATUS"></span>Вбемфлагдонтсендстатус \* \* \* \* (0 (0x0))</span><span class="sxs-lookup"><span data-stu-id="d1c0e-130"><span id="wbemFlagDontSendStatus"></span><span id="wbemflagdontsendstatus"></span><span id="WBEMFLAGDONTSENDSTATUS"></span>\*\*\*\*wbemFlagDontSendStatus\*\*\*\* (0 (0x0))</span></span>


</dt> <dd>

<span data-ttu-id="d1c0e-131">Не позволяет асинхронным вызовам отправлять обновления состояния в обработчик событий [**OnProgress**](swbemsink-onprogress.md) для приемника объекта.</span><span class="sxs-lookup"><span data-stu-id="d1c0e-131">Prevents asynchronous calls from sending status updates to the [**OnProgress**](swbemsink-onprogress.md) event handler for the object sink.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="d1c0e-132">*обжвбемнамедвалуесет* \[ используемых\]</span><span class="sxs-lookup"><span data-stu-id="d1c0e-132">*objwbemNamedValueSet* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="d1c0e-133">Как правило, это не определено.</span><span class="sxs-lookup"><span data-stu-id="d1c0e-133">Typically, this is undefined.</span></span> <span data-ttu-id="d1c0e-134">В противном случае это объект [**свбемнамедвалуесет**](swbemnamedvalueset.md) , элементы которого представляют сведения о контексте, которые могут использоваться поставщиком, который служб запрашивает.</span><span class="sxs-lookup"><span data-stu-id="d1c0e-134">Otherwise, this is an [**SWbemNamedValueSet**](swbemnamedvalueset.md) object whose elements represent the context information that can be used by the provider that services the request.</span></span> <span data-ttu-id="d1c0e-135">Поставщик, который поддерживает или требует такую информацию, должен документировать распознанные имена значений, тип данных значения, допустимые значения и семантику.</span><span class="sxs-lookup"><span data-stu-id="d1c0e-135">A provider that supports or requires such information must document the recognized value names, data type of the value, allowed values, and semantics.</span></span>

</dd> <dt>

<span data-ttu-id="d1c0e-136">*обжвбемасинкконтекст* \[ используемых\]</span><span class="sxs-lookup"><span data-stu-id="d1c0e-136">*objWbemAsyncContext* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="d1c0e-137">Это объект [**свбемнамедвалуесет**](swbemnamedvalueset.md) , который возвращает приемнику объекта, чтобы узнать источник исходного асинхронного вызова.</span><span class="sxs-lookup"><span data-stu-id="d1c0e-137">This is an [**SWbemNamedValueSet**](swbemnamedvalueset.md) object that returns to the object sink to identify the source of the original asynchronous call.</span></span> <span data-ttu-id="d1c0e-138">Этот параметр используется для выполнения нескольких асинхронных вызовов с использованием одного и того же приемника объекта.</span><span class="sxs-lookup"><span data-stu-id="d1c0e-138">Use this parameter to make multiple asynchronous calls using the same object sink.</span></span> <span data-ttu-id="d1c0e-139">Чтобы использовать этот параметр, создайте объект **свбемнамедвалуесет** и используйте метод [**свбемнамедвалуесет. Add**](swbemnamedvalueset-add.md) , чтобы добавить значение, идентифицирующее выполняемый асинхронный вызов.</span><span class="sxs-lookup"><span data-stu-id="d1c0e-139">To use this parameter, create an **SWbemNamedValueSet** object and use the [**SWbemNamedValueSet.Add**](swbemnamedvalueset-add.md) method to add a value that identifies the asynchronous call you are making.</span></span> <span data-ttu-id="d1c0e-140">Объект **свбемнамедвалуесет** возвращается в приемник объекта, и источник вызова можно извлечь с помощью метода [**свбемнамедвалуесет. Item**](swbemnamedvalueset-item.md) .</span><span class="sxs-lookup"><span data-stu-id="d1c0e-140">The **SWbemNamedValueSet** object is returned to the object sink and the source of the call can be extracted using the [**SWbemNamedValueSet.Item**](swbemnamedvalueset-item.md) method.</span></span> <span data-ttu-id="d1c0e-141">Дополнительные сведения см. [в разделе вызов метода](calling-a-method.md).</span><span class="sxs-lookup"><span data-stu-id="d1c0e-141">For more information, see [Calling a Method](calling-a-method.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d1c0e-142">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="d1c0e-142">Return value</span></span>

<span data-ttu-id="d1c0e-143">Этот метод не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="d1c0e-143">This method does not return a value.</span></span> <span data-ttu-id="d1c0e-144">В случае успешного выполнения приемник получает событие [**онобжектреади**](swbemsink-onobjectready.md) для каждого экземпляра.</span><span class="sxs-lookup"><span data-stu-id="d1c0e-144">If successful, the sink receives an [**OnObjectReady**](swbemsink-onobjectready.md) event per instance.</span></span> <span data-ttu-id="d1c0e-145">После последнего экземпляра приемник объекта получает событие [**Oncompleteed**](swbemsink-oncompleted.md) .</span><span class="sxs-lookup"><span data-stu-id="d1c0e-145">After the last instance, the object sink receives an [**OnCompleted**](swbemsink-oncompleted.md) event.</span></span>

## <a name="error-codes"></a><span data-ttu-id="d1c0e-146">Коды ошибок</span><span class="sxs-lookup"><span data-stu-id="d1c0e-146">Error codes</span></span>

<span data-ttu-id="d1c0e-147">После завершения метода **ExecNotificationQueryAsync** объект [Err](/previous-versions//sbf5ze0e(v=vs.85)) может содержать один из кодов ошибок, указанных в следующем списке.</span><span class="sxs-lookup"><span data-stu-id="d1c0e-147">After the completion of the **ExecNotificationQueryAsync** method, the [Err](/previous-versions//sbf5ze0e(v=vs.85)) object may contain one of the error codes identified in the following list.</span></span>

<dl> <dt>

<span data-ttu-id="d1c0e-148">**вбемерракцессдениед** -2147749891 (0x80041003)</span><span class="sxs-lookup"><span data-stu-id="d1c0e-148">**wbemErrAccessDenied** - 2147749891 (0x80041003)</span></span>
</dt> <dd>

<span data-ttu-id="d1c0e-149">Текущий пользователь не имеет права на Просмотр результирующего набора.</span><span class="sxs-lookup"><span data-stu-id="d1c0e-149">Current user is not authorized to view the result set.</span></span>

</dd> <dt>

<span data-ttu-id="d1c0e-150">**вбемеррфаилед** -2147749889 (0x80041001)</span><span class="sxs-lookup"><span data-stu-id="d1c0e-150">**wbemErrFailed** - 2147749889 (0x80041001)</span></span>
</dt> <dd>

<span data-ttu-id="d1c0e-151">Незаданная ошибка.</span><span class="sxs-lookup"><span data-stu-id="d1c0e-151">Unspecified error.</span></span>

</dd> <dt>

<span data-ttu-id="d1c0e-152">**вбемерринвалидпараметер** -2147749896 (0x80041008)</span><span class="sxs-lookup"><span data-stu-id="d1c0e-152">**wbemErrInvalidParameter** - 2147749896 (0x80041008)</span></span>
</dt> <dd>

<span data-ttu-id="d1c0e-153">Указан недопустимый параметр.</span><span class="sxs-lookup"><span data-stu-id="d1c0e-153">Invalid parameter is specified.</span></span>

</dd> <dt>

<span data-ttu-id="d1c0e-154">**вбемерринвалидкуери** -2147749911 (0x80041017)</span><span class="sxs-lookup"><span data-stu-id="d1c0e-154">**wbemErrInvalidQuery** - 2147749911 (0x80041017)</span></span>
</dt> <dd>

<span data-ttu-id="d1c0e-155">Недопустимый синтаксис запроса.</span><span class="sxs-lookup"><span data-stu-id="d1c0e-155">Query syntax is not valid.</span></span>

</dd> <dt>

<span data-ttu-id="d1c0e-156">**вбемерринвалидкуеритипе** -2147749912 (0x80041018)</span><span class="sxs-lookup"><span data-stu-id="d1c0e-156">**wbemErrInvalidQueryType** - 2147749912 (0x80041018)</span></span>
</dt> <dd>

<span data-ttu-id="d1c0e-157">Запрошенный язык запросов не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="d1c0e-157">Requested query language is not supported.</span></span>

</dd> <dt>

<span data-ttu-id="d1c0e-158">**вбемерраутофмемори** -2147749894 (0x80041006)</span><span class="sxs-lookup"><span data-stu-id="d1c0e-158">**wbemErrOutOfMemory** - 2147749894 (0x80041006)</span></span>
</dt> <dd>

<span data-ttu-id="d1c0e-159">Недостаточно памяти для завершения операции.</span><span class="sxs-lookup"><span data-stu-id="d1c0e-159">Not enough memory to complete the operation.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="d1c0e-160">Комментарии</span><span class="sxs-lookup"><span data-stu-id="d1c0e-160">Remarks</span></span>

<span data-ttu-id="d1c0e-161">Метод **ExecNotificationQueryAsync** возвращает объекты типа события, создаваемые будущими событиями.</span><span class="sxs-lookup"><span data-stu-id="d1c0e-161">The **ExecNotificationQueryAsync** method returns event type objects that future events generate.</span></span> <span data-ttu-id="d1c0e-162">Объекты событий, **ExecNotificationQueryAsync** запросы, могут быть встроенными (например, [**\_ \_ инстанцекреатионевент**](--instancecreationevent.md)) или внешние (например, события [**регистрикэйчанжеевент**](/previous-versions/windows/desktop/regprov/registrykeychangeevent) или SNMP).</span><span class="sxs-lookup"><span data-stu-id="d1c0e-162">The event objects that **ExecNotificationQueryAsync** requests can be intrinsic (for example, [**\_\_InstanceCreationEvent**](--instancecreationevent.md)), or extrinsic (for example, [**RegistryKeyChangeEvent**](/previous-versions/windows/desktop/regprov/registrykeychangeevent) or SNMP events).</span></span> <span data-ttu-id="d1c0e-163">Дополнительные сведения см. [в разделе Определение типа получаемого события](determining-the-type-of-event-to-receive.md).</span><span class="sxs-lookup"><span data-stu-id="d1c0e-163">For more information, see [Determining the Type of Event to Receive](determining-the-type-of-event-to-receive.md).</span></span>

<span data-ttu-id="d1c0e-164">Вызов **ExecNotificationQueryAsync** немедленно возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="d1c0e-164">The call to **ExecNotificationQueryAsync** returns immediately.</span></span> <span data-ttu-id="d1c0e-165">Запрошенные объекты и состояние возвращаются вызывающему объекту через обратные вызовы, доставляемые в приемник, указанный в *обжвбемсинк*.</span><span class="sxs-lookup"><span data-stu-id="d1c0e-165">The requested objects and status are returned to the caller through callbacks delivered to the sink that is specified in *objWbemSink*.</span></span> <span data-ttu-id="d1c0e-166">Чтобы обработать каждый объект при его возвращении, создайте *обжвбемсинк*. Подпрограммы события [**онобжектреади**](swbemsink-onobjectready.md) .</span><span class="sxs-lookup"><span data-stu-id="d1c0e-166">To process each object when it is returned, create an *objWbemSink*.[**OnObjectReady**](swbemsink-onobjectready.md) event subroutine.</span></span> <span data-ttu-id="d1c0e-167">После возврата всех объектов выполните окончательную обработку для реализации *обжвбемсинк*. Событие [**Oncompleteed**](swbemsink-oncompleted.md) .</span><span class="sxs-lookup"><span data-stu-id="d1c0e-167">After all the objects are returned, perform the final processing to implement the *objWbemSink*.[**OnCompleted**](swbemsink-oncompleted.md) event.</span></span>

<span data-ttu-id="d1c0e-168">Асинхронный обратный вызов позволяет пользователю без проверки подлинности предоставлять данные в приемник.</span><span class="sxs-lookup"><span data-stu-id="d1c0e-168">An asynchronous callback allows a non-authenticated user to provide data to the sink.</span></span> <span data-ttu-id="d1c0e-169">Это создает угрозы безопасности для сценариев и приложений.</span><span class="sxs-lookup"><span data-stu-id="d1c0e-169">This poses security risks to your scripts and applications.</span></span> <span data-ttu-id="d1c0e-170">Сведения об устранении рисков см. в разделе [Настройка безопасности при асинхронном вызове](setting-security-on-an-asynchronous-call.md).</span><span class="sxs-lookup"><span data-stu-id="d1c0e-170">To eliminate the risks, see [Setting Security on an Asynchronous Call](setting-security-on-an-asynchronous-call.md).</span></span>

<span data-ttu-id="d1c0e-171">Существует ряд ограничений на количество ключевых слов **and** и **or** , которые могут использоваться в запросах WQL.</span><span class="sxs-lookup"><span data-stu-id="d1c0e-171">There are limits to the number of **AND** and **OR** keywords that can be used in WQL queries.</span></span> <span data-ttu-id="d1c0e-172">Большое количество ключевых слов WQL, используемых в сложном запросе, может привести к тому, что инструментарий WMI возвращает значение **HRESULT** с кодом ошибки **\_ \_ \_ нарушения квоты E** Асан.</span><span class="sxs-lookup"><span data-stu-id="d1c0e-172">Large numbers of WQL keywords used in a complex query can cause WMI to return the **WBEM\_E\_QUOTA\_VIOLATION** error code asan **HRESULT** value.</span></span> <span data-ttu-id="d1c0e-173">Ограничение ключевых слов WQL зависит от того, насколько сложным является запрос.</span><span class="sxs-lookup"><span data-stu-id="d1c0e-173">The limit of WQL keywords depends on how complex the query is.</span></span>

## <a name="examples"></a><span data-ttu-id="d1c0e-174">Примеры</span><span class="sxs-lookup"><span data-stu-id="d1c0e-174">Examples</span></span>

<span data-ttu-id="d1c0e-175">В следующем примере кода VBScript показан скрипт, ожидающий уведомления о событии WMI, указывающий на завершение процесса.</span><span class="sxs-lookup"><span data-stu-id="d1c0e-175">The following VBScript code example shows a script that is waiting for a WMI event notification that indicates that a process has terminated.</span></span> <span data-ttu-id="d1c0e-176">Он ожидает встроенного события WMI, экземпляра класса событий [**\_ \_ инстанцеделетионевент**](--instancedeletionevent.md).</span><span class="sxs-lookup"><span data-stu-id="d1c0e-176">It is waiting for a WMI intrinsic event, an instance of the event class [**\_\_InstanceDeletionEvent**](--instancedeletionevent.md).</span></span> <span data-ttu-id="d1c0e-177">**\_ \_ Инстанцеделетионевент** должен представлять удаление экземпляра [**\_ процесса Win32**](/windows/desktop/CIMWin32Prov/win32-process).</span><span class="sxs-lookup"><span data-stu-id="d1c0e-177">The **\_\_InstanceDeletionEvent** must represent the deletion of an instance of [**Win32\_Process**](/windows/desktop/CIMWin32Prov/win32-process).</span></span> <span data-ttu-id="d1c0e-178">Дополнительные сведения о встроенных событиях WMI см. [в разделе Определение типа получаемого события](determining-the-type-of-event-to-receive.md).</span><span class="sxs-lookup"><span data-stu-id="d1c0e-178">For more information about WMI intrinsic events, see [Determining the Type of Event to Receive](determining-the-type-of-event-to-receive.md).</span></span>

<span data-ttu-id="d1c0e-179">Следующий скрипт выполняется неограниченно до перезагрузки компьютера, Инструментарий WMI остановлен или сценарий остановлен.</span><span class="sxs-lookup"><span data-stu-id="d1c0e-179">The following script runs indefinitely until the computer is rebooted, WMI is stopped, or the script is stopped.</span></span> <span data-ttu-id="d1c0e-180">Чтобы прерывать выполнение скрипта вручную, используйте диспетчер задач, чтобы прерывать процесс.</span><span class="sxs-lookup"><span data-stu-id="d1c0e-180">To stop the script manually, use Task Manager to stop the process.</span></span> <span data-ttu-id="d1c0e-181">Чтобы остановить его программно, используйте метод [**Terminate**](/windows/desktop/CIMWin32Prov/terminate-method-in-class-win32-process) в \_ классе процесса Win32.</span><span class="sxs-lookup"><span data-stu-id="d1c0e-181">To stop it programmatically, use the [**Terminate**](/windows/desktop/CIMWin32Prov/terminate-method-in-class-win32-process) method in the Win32\_Process class.</span></span>


```VB
strComputer = "." 
Set objWMIService = GetObject("winmgmts:\\" & _strComputer & "\root\CIMV2") 
Set MySink = WScript.CreateObject("WbemScripting.SWbemSink","SINK_")

objWMIservice.ExecNotificationQueryAsync MySink, "SELECT * FROM __InstanceCreationEvent WITHIN 1 " _
                                               & "WHERE TargetInstance ISA 'Win32_Process'"

WScript.Echo "Waiting for events..."

While (True)
    Wscript.Sleep(1000)
Wend

Sub SINK_OnObjectReady(objObject, objAsyncContext)
    WScript.Echo "Event occurred."
End Sub

Sub SINK_OnCompleted(objObject, objAsyncContext)
    WScript.Echo "Event call complete."
End Sub
```



## <a name="requirements"></a><span data-ttu-id="d1c0e-182">Требования</span><span class="sxs-lookup"><span data-stu-id="d1c0e-182">Requirements</span></span>



| <span data-ttu-id="d1c0e-183">Требование</span><span class="sxs-lookup"><span data-stu-id="d1c0e-183">Requirement</span></span> | <span data-ttu-id="d1c0e-184">Значение</span><span class="sxs-lookup"><span data-stu-id="d1c0e-184">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="d1c0e-185">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="d1c0e-185">Minimum supported client</span></span><br/> | <span data-ttu-id="d1c0e-186">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="d1c0e-186">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="d1c0e-187">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="d1c0e-187">Minimum supported server</span></span><br/> | <span data-ttu-id="d1c0e-188">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="d1c0e-188">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="d1c0e-189">Header</span><span class="sxs-lookup"><span data-stu-id="d1c0e-189">Header</span></span><br/>                   | <dl> <span data-ttu-id="d1c0e-190"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="d1c0e-190"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="d1c0e-191">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="d1c0e-191">Type library</span></span><br/>             | <dl> <span data-ttu-id="d1c0e-192"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="d1c0e-192"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="d1c0e-193">DLL</span><span class="sxs-lookup"><span data-stu-id="d1c0e-193">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d1c0e-194"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d1c0e-194"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="d1c0e-195">CLSID</span><span class="sxs-lookup"><span data-stu-id="d1c0e-195">CLSID</span></span><br/>                    | <span data-ttu-id="d1c0e-196">\_SWBEMSERVICES CLSID</span><span class="sxs-lookup"><span data-stu-id="d1c0e-196">CLSID\_SWbemServices</span></span><br/>                                                         |
| <span data-ttu-id="d1c0e-197">IID</span><span class="sxs-lookup"><span data-stu-id="d1c0e-197">IID</span></span><br/>                      | <span data-ttu-id="d1c0e-198">IID \_ исвбемсервицес</span><span class="sxs-lookup"><span data-stu-id="d1c0e-198">IID\_ISWbemServices</span></span><br/>                                                          |



## <a name="see-also"></a><span data-ttu-id="d1c0e-199">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="d1c0e-199">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d1c0e-200">**SWbemServices**</span><span class="sxs-lookup"><span data-stu-id="d1c0e-200">**SWbemServices**</span></span>](swbemservices.md)
</dt> <dt>

[<span data-ttu-id="d1c0e-201">**SWbemServices.ExeКкуери**</span><span class="sxs-lookup"><span data-stu-id="d1c0e-201">**SWbemServices.ExecQuery**</span></span>](swbemservices-execquery.md)
</dt> <dt>

[<span data-ttu-id="d1c0e-202">**SWbemServices.ExeКкуерясинк**</span><span class="sxs-lookup"><span data-stu-id="d1c0e-202">**SWbemServices.ExecQueryAsync**</span></span>](swbemservices-execqueryasync.md)
</dt> <dt>

[<span data-ttu-id="d1c0e-203">Регистрация для событий системного реестра</span><span class="sxs-lookup"><span data-stu-id="d1c0e-203">Registering for System Registry Events</span></span>](registering-for-system-registry-events.md)
</dt> <dt>

[<span data-ttu-id="d1c0e-204">Определение типа получаемого события</span><span class="sxs-lookup"><span data-stu-id="d1c0e-204">Determining the Type of Event to Receive</span></span>](determining-the-type-of-event-to-receive.md)
</dt> <dt>

[<span data-ttu-id="d1c0e-205">Вызов метода</span><span class="sxs-lookup"><span data-stu-id="d1c0e-205">Calling a Method</span></span>](calling-a-method.md)
</dt> <dt>

[<span data-ttu-id="d1c0e-206">Настройка безопасности при асинхронном вызове</span><span class="sxs-lookup"><span data-stu-id="d1c0e-206">Setting Security on an Asynchronous Call</span></span>](setting-security-on-an-asynchronous-call.md)
</dt> </dl>

 

