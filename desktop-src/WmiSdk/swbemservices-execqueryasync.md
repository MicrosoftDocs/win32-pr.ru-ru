---
description: SWbemServices.Exeметод Ккуерясинк — выполняет запрос для получения объектов.
ms.assetid: 50c7f62b-dd83-4117-b10e-acee1690ce8c
ms.tgt_platform: multiple
title: SWbemServices.Exeметод Ккуерясинк (Wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemServices.ExecQueryAsync
- ISWbemServices.ExecQueryAsync
- ISWbemServices.ExecQueryAsync
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 5cd3fe778ca7338df6b2674a4930458ef9113a1d
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108118382"
---
# <a name="swbemservicesexecqueryasync-method"></a><span data-ttu-id="4a477-103">SWbemServices.Exeметод Ккуерясинк</span><span class="sxs-lookup"><span data-stu-id="4a477-103">SWbemServices.ExecQueryAsync method</span></span>

<span data-ttu-id="4a477-104">Метод **ексеккуерясинк** объекта [**SwbemServices**](swbemservices.md) выполняет запрос для получения объектов.</span><span class="sxs-lookup"><span data-stu-id="4a477-104">The **ExecQueryAsync** method of the [**SWbemServices**](swbemservices.md) object executes a query to retrieve objects.</span></span> <span data-ttu-id="4a477-105">Вызов этого метода немедленно возвращает результат, а результаты и состояние возвращаются вызывающему через события, доставляемые в приемник, указанный в *обжвбемсинк*.</span><span class="sxs-lookup"><span data-stu-id="4a477-105">The call to this method returns immediately, and the results and status are returned to the caller through events delivered to the sink that is specified in *objWbemSink*.</span></span> <span data-ttu-id="4a477-106">Чтобы выполнить обработку каждого возвращенного объекта, создайте *обжвбемсинк*. Подпрограммы события [**онобжектреади**](swbemsink-onobjectready.md) .</span><span class="sxs-lookup"><span data-stu-id="4a477-106">To handle each returned object, create an *objWbemSink*.[**OnObjectReady**](swbemsink-onobjectready.md) event subroutine.</span></span>

<span data-ttu-id="4a477-107">Метод вызывается в асинхронном режиме.</span><span class="sxs-lookup"><span data-stu-id="4a477-107">The method is called in the asynchronous mode.</span></span> <span data-ttu-id="4a477-108">Дополнительные сведения см. [в разделе вызов метода](calling-a-method.md).</span><span class="sxs-lookup"><span data-stu-id="4a477-108">For more information, see [Calling a Method](calling-a-method.md).</span></span>

<span data-ttu-id="4a477-109">Описание этого синтаксиса см. в разделе [соглашения о документе для API скриптов](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="4a477-109">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="4a477-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="4a477-110">Syntax</span></span>


```VB
objWbemObjectSet = .ExecQueryAsync( _
  [ ByVal objWbemSink ], _
  ByVal strQuery, _
  [ ByVal strQueryLanguage ], _
  [ ByVal iFlags ], _
  [ ByVal objwbemNamedValueSet ], _
  [ ByVal objWbemAsyncContext ] _
)
```



## <a name="parameters"></a><span data-ttu-id="4a477-111">Параметры</span><span class="sxs-lookup"><span data-stu-id="4a477-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4a477-112">*обжвбемсинк* \[ используемых\]</span><span class="sxs-lookup"><span data-stu-id="4a477-112">*objWbemSink* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="4a477-113">Приемник объекта, выполняющий запрос асинхронно.</span><span class="sxs-lookup"><span data-stu-id="4a477-113">Object sink that executes the query asynchronously.</span></span> <span data-ttu-id="4a477-114">Создайте объект [**свбемсинк**](swbemsink.md) для получения объектов.</span><span class="sxs-lookup"><span data-stu-id="4a477-114">Create an [**SWbemSink**](swbemsink.md) object to receive the objects.</span></span>

</dd> <dt>

<span data-ttu-id="4a477-115">*стркуери*</span><span class="sxs-lookup"><span data-stu-id="4a477-115">*strQuery*</span></span> 
</dt> <dd>

<span data-ttu-id="4a477-116">Обязательный элемент.</span><span class="sxs-lookup"><span data-stu-id="4a477-116">Required.</span></span> <span data-ttu-id="4a477-117">Строка, содержащая текст запроса.</span><span class="sxs-lookup"><span data-stu-id="4a477-117">String that contains the text of the query.</span></span> <span data-ttu-id="4a477-118">Этот параметр не может быть пустым.</span><span class="sxs-lookup"><span data-stu-id="4a477-118">This parameter cannot be blank.</span></span> <span data-ttu-id="4a477-119">Дополнительные сведения о создании строк запросов WMI см. в разделе [запросы с помощью WQL](querying-with-wql.md) и Справочник по [WQL](wql-sql-for-wmi.md) .</span><span class="sxs-lookup"><span data-stu-id="4a477-119">For more information on building WMI query strings, see [Querying with WQL](querying-with-wql.md) and the [WQL](wql-sql-for-wmi.md) reference.</span></span>

</dd> <dt>

<span data-ttu-id="4a477-120">*стркуерилангуаже* \[ используемых\]</span><span class="sxs-lookup"><span data-stu-id="4a477-120">*strQueryLanguage* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="4a477-121">Строка, содержащая используемый язык запросов.</span><span class="sxs-lookup"><span data-stu-id="4a477-121">String that contains the query language to be used.</span></span> <span data-ttu-id="4a477-122">Если указано, значение должно быть "WQL".</span><span class="sxs-lookup"><span data-stu-id="4a477-122">If specified, the value must be "WQL".</span></span>

</dd> <dt>

<span data-ttu-id="4a477-123">*ифлагс* \[ используемых\]</span><span class="sxs-lookup"><span data-stu-id="4a477-123">*iFlags* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="4a477-124">Целое число, определяющее поведение запроса.</span><span class="sxs-lookup"><span data-stu-id="4a477-124">Integer that determines the behavior of the query.</span></span> <span data-ttu-id="4a477-125">Этот параметр может принимать следующие значения.</span><span class="sxs-lookup"><span data-stu-id="4a477-125">This parameter can accept the following values.</span></span>

<dt>

<span id="wbemFlagSendStatus"></span><span id="wbemflagsendstatus"></span><span id="WBEMFLAGSENDSTATUS"></span>

<span data-ttu-id="4a477-126"><span id="wbemFlagSendStatus"></span><span id="wbemflagsendstatus"></span><span id="WBEMFLAGSENDSTATUS"></span>Вбемфлагсендстатус \* \* \* \* (128 (0x80))</span><span class="sxs-lookup"><span data-stu-id="4a477-126"><span id="wbemFlagSendStatus"></span><span id="wbemflagsendstatus"></span><span id="WBEMFLAGSENDSTATUS"></span>\*\*\*\*wbemFlagSendStatus\*\*\*\* (128 (0x80))</span></span>


</dt> <dd>

<span data-ttu-id="4a477-127">Вызывает асинхронные вызовы для отправки обновлений состояния обработчику событий [**OnProgress**](swbemsink-onprogress.md) для приемника объекта.</span><span class="sxs-lookup"><span data-stu-id="4a477-127">Causes asynchronous calls to send status updates to the [**OnProgress**](swbemsink-onprogress.md) event handler for the object sink.</span></span>

</dd> <dt>

<span id="wbemFlagDontSendStatus"></span><span id="wbemflagdontsendstatus"></span><span id="WBEMFLAGDONTSENDSTATUS"></span>

<span data-ttu-id="4a477-128"><span id="wbemFlagDontSendStatus"></span><span id="wbemflagdontsendstatus"></span><span id="WBEMFLAGDONTSENDSTATUS"></span>Вбемфлагдонтсендстатус \* \* \* \* (0 (0x0))</span><span class="sxs-lookup"><span data-stu-id="4a477-128"><span id="wbemFlagDontSendStatus"></span><span id="wbemflagdontsendstatus"></span><span id="WBEMFLAGDONTSENDSTATUS"></span>\*\*\*\*wbemFlagDontSendStatus\*\*\*\* (0 (0x0))</span></span>


</dt> <dd>

<span data-ttu-id="4a477-129">Не позволяет асинхронным вызовам отправлять обновления состояния в обработчик событий [**OnProgress**](swbemsink-onprogress.md) для приемника объекта.</span><span class="sxs-lookup"><span data-stu-id="4a477-129">Prevents asynchronous calls from sending status updates to the [**OnProgress**](swbemsink-onprogress.md) event handler for the object sink.</span></span>

</dd> <dt>

<span id="wbemQueryFlagPrototype"></span><span id="wbemqueryflagprototype"></span><span id="WBEMQUERYFLAGPROTOTYPE"></span>

<span data-ttu-id="4a477-130"><span id="wbemQueryFlagPrototype"></span><span id="wbemqueryflagprototype"></span><span id="WBEMQUERYFLAGPROTOTYPE"></span>Вбемкуерифлагпрототипе \* \* \* \* (0x2)</span><span class="sxs-lookup"><span data-stu-id="4a477-130"><span id="wbemQueryFlagPrototype"></span><span id="wbemqueryflagprototype"></span><span id="WBEMQUERYFLAGPROTOTYPE"></span>\*\*\*\*wbemQueryFlagPrototype\*\*\*\* (2 (0x2))</span></span>


</dt> <dd>

<span data-ttu-id="4a477-131">Используется для прототипа.</span><span class="sxs-lookup"><span data-stu-id="4a477-131">Used for a prototype.</span></span> <span data-ttu-id="4a477-132">Он останавливает выполнение запроса и вместо этого возвращает объект, который выглядит как типичный результирующий объект.</span><span class="sxs-lookup"><span data-stu-id="4a477-132">It stops the query from happening and instead, returns an object that looks like a typical result object.</span></span>

</dd> <dt>

<span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>

<span data-ttu-id="4a477-133"><span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>Вбемфлагусеамендедкуалифиерс \* \* \* \* (131072 (0x20000))</span><span class="sxs-lookup"><span data-stu-id="4a477-133"><span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>\*\*\*\*wbemFlagUseAmendedQualifiers\*\*\*\* (131072 (0x20000))</span></span>


</dt> <dd>

<span data-ttu-id="4a477-134">Заставляет WMI возвращать данные о поправности класса с определением базового класса.</span><span class="sxs-lookup"><span data-stu-id="4a477-134">Causes WMI to return class amendment data with the base class definition.</span></span> <span data-ttu-id="4a477-135">Дополнительные сведения см. в разделе [Локализация сведений о классе WMI](localizing-wmi-class-information.md).</span><span class="sxs-lookup"><span data-stu-id="4a477-135">For more information, see [Localizing WMI Class Information](localizing-wmi-class-information.md).</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="4a477-136">*обжвбемнамедвалуесет* \[ используемых\]</span><span class="sxs-lookup"><span data-stu-id="4a477-136">*objwbemNamedValueSet* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="4a477-137">Как правило, это не определено.</span><span class="sxs-lookup"><span data-stu-id="4a477-137">Typically, this is undefined.</span></span> <span data-ttu-id="4a477-138">В противном случае это объект [**свбемнамедвалуесет**](swbemnamedvalueset.md) , элементы которого представляют сведения о контексте, которые могут использоваться поставщиком, который служб запрашивает.</span><span class="sxs-lookup"><span data-stu-id="4a477-138">Otherwise, this is an [**SWbemNamedValueSet**](swbemnamedvalueset.md) object whose elements represent the context information that can be used by the provider that services the request.</span></span> <span data-ttu-id="4a477-139">Поставщик, который поддерживает или требует сведения о контексте, должен документировать распознанные имена значений, тип данных значения, допустимые значения и семантику.</span><span class="sxs-lookup"><span data-stu-id="4a477-139">A provider that supports or requires context information must document the recognized value names, data type of the value, allowed values, and semantics.</span></span>

</dd> <dt>

<span data-ttu-id="4a477-140">*обжвбемасинкконтекст* \[ используемых\]</span><span class="sxs-lookup"><span data-stu-id="4a477-140">*objWbemAsyncContext* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="4a477-141">Объект [**свбемнамедвалуесет**](swbemnamedvalueset.md) , возвращающий приемник объекта для обнаружения источника исходного асинхронного вызова.</span><span class="sxs-lookup"><span data-stu-id="4a477-141">An [**SWbemNamedValueSet**](swbemnamedvalueset.md) object that returns to the object sink to identify the source of the original asynchronous call.</span></span> <span data-ttu-id="4a477-142">Этот параметр используется для выполнения нескольких асинхронных вызовов с использованием одного и того же приемника объекта.</span><span class="sxs-lookup"><span data-stu-id="4a477-142">Use this parameter to make multiple asynchronous calls using the same object sink.</span></span> <span data-ttu-id="4a477-143">Чтобы использовать этот параметр, создайте объект **свбемнамедвалуесет** и используйте метод [**свбемнамедвалуесет. Add**](swbemnamedvalueset-add.md) , чтобы добавить значение, идентифицирующее выполняемый асинхронный вызов.</span><span class="sxs-lookup"><span data-stu-id="4a477-143">To use this parameter, create an **SWbemNamedValueSet** object, and use the [**SWbemNamedValueSet.Add**](swbemnamedvalueset-add.md) method to add a value that identifies the asynchronous call you are making.</span></span> <span data-ttu-id="4a477-144">Этот объект **свбемнамедвалуесет** возвращается в приемник объекта, и источник вызова можно извлечь с помощью метода [**свбемнамедвалуесет. Item**](swbemnamedvalueset-item.md) .</span><span class="sxs-lookup"><span data-stu-id="4a477-144">This **SWbemNamedValueSet** object is returned to the object sink and the source of the call can be extracted using the [**SWbemNamedValueSet.Item**](swbemnamedvalueset-item.md) method.</span></span> <span data-ttu-id="4a477-145">Дополнительные сведения см. [в разделе вызов метода](calling-a-method.md).</span><span class="sxs-lookup"><span data-stu-id="4a477-145">For more information, see [Calling a Method](calling-a-method.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4a477-146">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="4a477-146">Return value</span></span>

<span data-ttu-id="4a477-147">Этот метод не имеет возвращаемых значений.</span><span class="sxs-lookup"><span data-stu-id="4a477-147">This method has no return values.</span></span> <span data-ttu-id="4a477-148">В случае успешного выполнения приемник получает событие [**онобжектреади**](swbemsink-onobjectready.md) для каждого экземпляра.</span><span class="sxs-lookup"><span data-stu-id="4a477-148">If successful, the sink receives an [**OnObjectReady**](swbemsink-onobjectready.md) event per instance.</span></span> <span data-ttu-id="4a477-149">После последнего экземпляра приемник объекта получает событие [**Oncompleteed**](swbemsink-oncompleted.md) .</span><span class="sxs-lookup"><span data-stu-id="4a477-149">After the last instance, the object sink receives an [**OnCompleted**](swbemsink-oncompleted.md) event.</span></span>

## <a name="error-codes"></a><span data-ttu-id="4a477-150">Коды ошибок</span><span class="sxs-lookup"><span data-stu-id="4a477-150">Error codes</span></span>

<span data-ttu-id="4a477-151">После завершения метода **ексеккуерясинк** объект [Err](/previous-versions//sbf5ze0e(v=vs.85)) может содержать один из кодов ошибок из следующего списка.</span><span class="sxs-lookup"><span data-stu-id="4a477-151">After the completion of the **ExecQueryAsync** method, the [Err](/previous-versions//sbf5ze0e(v=vs.85)) object can contain one of the error codes in the following list.</span></span>

<dl> <dt>

<span data-ttu-id="4a477-152">**вбемерракцессдениед** -2147749891 (0x80041003)</span><span class="sxs-lookup"><span data-stu-id="4a477-152">**wbemErrAccessDenied** - 2147749891 (0x80041003)</span></span>
</dt> <dd>

<span data-ttu-id="4a477-153">У текущего пользователя нет разрешения на Просмотр результирующего набора.</span><span class="sxs-lookup"><span data-stu-id="4a477-153">Current user does not have the permission to view the result set.</span></span>

</dd> <dt>

<span data-ttu-id="4a477-154">**вбемеррфаилед** -2147749889 (0x80041001)</span><span class="sxs-lookup"><span data-stu-id="4a477-154">**wbemErrFailed** - 2147749889 (0x80041001)</span></span>
</dt> <dd>

<span data-ttu-id="4a477-155">Незаданная ошибка.</span><span class="sxs-lookup"><span data-stu-id="4a477-155">Unspecified error.</span></span>

</dd> <dt>

<span data-ttu-id="4a477-156">**вбемерринвалидпараметер** -2147749896 (0x80041008)</span><span class="sxs-lookup"><span data-stu-id="4a477-156">**wbemErrInvalidParameter** - 2147749896 (0x80041008)</span></span>
</dt> <dd>

<span data-ttu-id="4a477-157">Указан недопустимый параметр.</span><span class="sxs-lookup"><span data-stu-id="4a477-157">Invalid parameter was specified.</span></span>

</dd> <dt>

<span data-ttu-id="4a477-158">**вбемерринвалидкуери** -2147749911 (0x80041017)</span><span class="sxs-lookup"><span data-stu-id="4a477-158">**wbemErrInvalidQuery** - 2147749911 (0x80041017)</span></span>
</dt> <dd>

<span data-ttu-id="4a477-159">Недопустимый синтаксис запроса.</span><span class="sxs-lookup"><span data-stu-id="4a477-159">Query syntax is not valid.</span></span>

</dd> <dt>

<span data-ttu-id="4a477-160">**вбемерринвалидкуеритипе** -2147749912 (0x80041018)</span><span class="sxs-lookup"><span data-stu-id="4a477-160">**wbemErrInvalidQueryType** - 2147749912 (0x80041018)</span></span>
</dt> <dd>

<span data-ttu-id="4a477-161">Запрошенный язык запросов не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="4a477-161">Requested query language is not supported.</span></span>

</dd> <dt>

<span data-ttu-id="4a477-162">**вбемерраутофмемори** -2147749894 (0x80041006)</span><span class="sxs-lookup"><span data-stu-id="4a477-162">**wbemErrOutOfMemory** - 2147749894 (0x80041006)</span></span>
</dt> <dd>

<span data-ttu-id="4a477-163">Недостаточно памяти для завершения операции.</span><span class="sxs-lookup"><span data-stu-id="4a477-163">Not enough memory to complete the operation.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="4a477-164">Remarks</span><span class="sxs-lookup"><span data-stu-id="4a477-164">Remarks</span></span>

<span data-ttu-id="4a477-165">Этот вызов возвращает немедленно.</span><span class="sxs-lookup"><span data-stu-id="4a477-165">This call returns immediately.</span></span> <span data-ttu-id="4a477-166">Запрошенные объекты и состояние возвращаются вызывающему объекту через обратные вызовы, доставляемые в приемник, указанный в *обжвбемсинк*.</span><span class="sxs-lookup"><span data-stu-id="4a477-166">The requested objects and status are returned to the caller through callbacks delivered to the sink that is specified in *objWbemSink*.</span></span> <span data-ttu-id="4a477-167">Чтобы обработать каждый объект при его возврате, создайте *обжвбемсинк*. Подпрограммы события [**онобжектреади**](swbemsink-onobjectready.md) .</span><span class="sxs-lookup"><span data-stu-id="4a477-167">To process each object when it returns, create an *objWbemSink*.[**OnObjectReady**](swbemsink-onobjectready.md) event subroutine.</span></span> <span data-ttu-id="4a477-168">После возврата всех объектов выполните окончательную обработку в реализации *обжвбемсинк*. Событие [**Oncompleteed**](swbemsink-oncompleted.md) .</span><span class="sxs-lookup"><span data-stu-id="4a477-168">After all the objects are returned, perform the final processing in your implementation of the *objWbemSink*.[**OnCompleted**](swbemsink-oncompleted.md) event.</span></span>

<span data-ttu-id="4a477-169">Асинхронный обратный вызов позволяет пользователю без проверки подлинности предоставлять данные в приемник.</span><span class="sxs-lookup"><span data-stu-id="4a477-169">An asynchronous callback allows a non-authenticated user to provide data to the sink.</span></span> <span data-ttu-id="4a477-170">Это создает угрозы безопасности для сценариев и приложений.</span><span class="sxs-lookup"><span data-stu-id="4a477-170">This poses security risks to your scripts and applications.</span></span> <span data-ttu-id="4a477-171">Сведения об устранении рисков см. в разделе [Настройка безопасности при асинхронном вызове](setting-security-on-an-asynchronous-call.md) .</span><span class="sxs-lookup"><span data-stu-id="4a477-171">To eliminate the risks, see [Setting Security on an Asynchronous Call](setting-security-on-an-asynchronous-call.md)</span></span>

<span data-ttu-id="4a477-172">Метод **ексеккуерясинк** возвращает пустой результирующий набор при отсутствии объектов, соответствующих критериям в запросе.</span><span class="sxs-lookup"><span data-stu-id="4a477-172">The **ExecQueryAsync** method returns an empty result set when there are no objects to match the criteria in the query.</span></span> <span data-ttu-id="4a477-173">Этот метод возвращает ключевые свойства независимо от того, запрашивалось ли свойство [**Key**](standard-qualifiers.md) в параметре *стркуери* .</span><span class="sxs-lookup"><span data-stu-id="4a477-173">This method returns key properties whether or not the [**Key**](standard-qualifiers.md) property is requested in the *strQuery* parameter.</span></span>

<span data-ttu-id="4a477-174">Существует ряд ограничений на количество ключевых слов **and** и **or** , которые могут использоваться в запросах WQL.</span><span class="sxs-lookup"><span data-stu-id="4a477-174">There are limits to the number of **AND** and **OR** keywords that can be used in WQL queries.</span></span> <span data-ttu-id="4a477-175">Большое количество ключевых слов WQL, используемых в сложном запросе, может привести к тому, \_ что WMI вернет \_ код ошибки нарушения квоты WBEM E \_ как значение **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="4a477-175">Large numbers of WQL keywords used in a complex query can cause WMI to return the WBEM\_E\_QUOTA\_VIOLATION error code as an **HRESULT** value.</span></span> <span data-ttu-id="4a477-176">Ограничение ключевых слов WQL зависит от того, насколько сложным является запрос.</span><span class="sxs-lookup"><span data-stu-id="4a477-176">The limit of WQL keywords depends on how complex the query is.</span></span>

## <a name="requirements"></a><span data-ttu-id="4a477-177">Требования</span><span class="sxs-lookup"><span data-stu-id="4a477-177">Requirements</span></span>



| <span data-ttu-id="4a477-178">Требование</span><span class="sxs-lookup"><span data-stu-id="4a477-178">Requirement</span></span> | <span data-ttu-id="4a477-179">Значение</span><span class="sxs-lookup"><span data-stu-id="4a477-179">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="4a477-180">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="4a477-180">Minimum supported client</span></span><br/> | <span data-ttu-id="4a477-181">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="4a477-181">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="4a477-182">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="4a477-182">Minimum supported server</span></span><br/> | <span data-ttu-id="4a477-183">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="4a477-183">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="4a477-184">Header</span><span class="sxs-lookup"><span data-stu-id="4a477-184">Header</span></span><br/>                   | <dl> <span data-ttu-id="4a477-185"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="4a477-185"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="4a477-186">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="4a477-186">Type library</span></span><br/>             | <dl> <span data-ttu-id="4a477-187"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="4a477-187"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="4a477-188">DLL</span><span class="sxs-lookup"><span data-stu-id="4a477-188">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4a477-189"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4a477-189"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="4a477-190">CLSID</span><span class="sxs-lookup"><span data-stu-id="4a477-190">CLSID</span></span><br/>                    | <span data-ttu-id="4a477-191">\_SWBEMSERVICES CLSID</span><span class="sxs-lookup"><span data-stu-id="4a477-191">CLSID\_SWbemServices</span></span><br/>                                                         |
| <span data-ttu-id="4a477-192">IID</span><span class="sxs-lookup"><span data-stu-id="4a477-192">IID</span></span><br/>                      | <span data-ttu-id="4a477-193">IID \_ исвбемсервицес</span><span class="sxs-lookup"><span data-stu-id="4a477-193">IID\_ISWbemServices</span></span><br/>                                                          |



## <a name="see-also"></a><span data-ttu-id="4a477-194">См. также</span><span class="sxs-lookup"><span data-stu-id="4a477-194">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4a477-195">**SWbemServices**</span><span class="sxs-lookup"><span data-stu-id="4a477-195">**SWbemServices**</span></span>](swbemservices.md)
</dt> <dt>

[<span data-ttu-id="4a477-196">Вызов метода</span><span class="sxs-lookup"><span data-stu-id="4a477-196">Calling a Method</span></span>](calling-a-method.md)
</dt> <dt>

[<span data-ttu-id="4a477-197">**SWbemServices. Get**</span><span class="sxs-lookup"><span data-stu-id="4a477-197">**SWbemServices.Get**</span></span>](swbemservices-get.md)
</dt> </dl>

 

