---
description: Метод Субклассесасинк \_ метода SWbemObject асинхронно предоставляет подклассы текущего объекта, который должен быть классом.
ms.assetid: 14d4a609-3aa4-49bd-bea4-6a71bc24d9dd
ms.tgt_platform: multiple
title: Метод SWbemObject.SubclassesAsync_ (Wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemObject.SubclassesAsync_
- ISWbemObject.SubclassesAsync_
- ISWbemObject.SubclassesAsync_
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 6e922953e9f25aae2e47ea572678790b1228a581
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104272563"
---
# <a name="swbemobjectsubclassesasync_-method"></a><span data-ttu-id="a0e45-103">SWbemObject. Субклассесасинк, \_ метод</span><span class="sxs-lookup"><span data-stu-id="a0e45-103">SWbemObject.SubclassesAsync\_ method</span></span>

<span data-ttu-id="a0e45-104">Метод **субклассесасинк \_** метода [**SWbemObject**](swbemobject.md) асинхронно предоставляет подклассы текущего объекта, который должен быть классом.</span><span class="sxs-lookup"><span data-stu-id="a0e45-104">The **SubclassesAsync\_** method of [**SWbemObject**](swbemobject.md) asynchronously supplies the subclasses of the current object, which must be a class.</span></span>

<span data-ttu-id="a0e45-105">Описание этого синтаксиса см. в разделе [соглашения о документе для API скриптов](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="a0e45-105">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="a0e45-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="a0e45-106">Syntax</span></span>


```VB
SWbemObject.SubclassesAsync_( _
  ByVal objWbemSink, _
  [ ByVal iFlags ], _
  [ ByVal objWbemNamedValueSet ], _
  [ ByVal objWbemAsyncContext ] _
)
```



## <a name="parameters"></a><span data-ttu-id="a0e45-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="a0e45-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a0e45-108">*обжвбемсинк* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="a0e45-108">*objWbemSink* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a0e45-109">Обязательный.</span><span class="sxs-lookup"><span data-stu-id="a0e45-109">Required.</span></span> <span data-ttu-id="a0e45-110">Приемник объекта, который асинхронно получает объекты.</span><span class="sxs-lookup"><span data-stu-id="a0e45-110">Object sink that receives the objects asynchronously.</span></span>

</dd> <dt>

<span data-ttu-id="a0e45-111">*ифлагс* \[ в необязательное\]</span><span class="sxs-lookup"><span data-stu-id="a0e45-111">*iFlags* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="a0e45-112">Определяет, как детализированный вызов перечисляет.</span><span class="sxs-lookup"><span data-stu-id="a0e45-112">Determines how detailed the call enumerates.</span></span> <span data-ttu-id="a0e45-113">Этот параметр может принимать следующие значения.</span><span class="sxs-lookup"><span data-stu-id="a0e45-113">This parameter can accept the following values.</span></span>

<dt>

<span id="wbemQueryFlagDeep"></span><span id="wbemqueryflagdeep"></span><span id="WBEMQUERYFLAGDEEP"></span>

<span data-ttu-id="a0e45-114"><span id="wbemQueryFlagDeep"></span><span id="wbemqueryflagdeep"></span><span id="WBEMQUERYFLAGDEEP"></span>Вбемкуерифлагдип \* \* \* \* (0 (0x0))</span><span class="sxs-lookup"><span data-stu-id="a0e45-114"><span id="wbemQueryFlagDeep"></span><span id="wbemqueryflagdeep"></span><span id="WBEMQUERYFLAGDEEP"></span>\*\*\*\*wbemQueryFlagDeep\*\*\*\* (0 (0x0))</span></span>


</dt> <dd>

<span data-ttu-id="a0e45-115">Активирует рекурсивное перечисление во всех подклассах, производных от указанного родительского класса.</span><span class="sxs-lookup"><span data-stu-id="a0e45-115">Forces recursive enumeration into all subclasses derived from the specified parent class.</span></span> <span data-ttu-id="a0e45-116">Сам родительский класс не возвращается в перечислении.</span><span class="sxs-lookup"><span data-stu-id="a0e45-116">The parent class itself is not returned in the enumeration.</span></span>

</dd> <dt>

<span id="wbemQueryFlagShallow"></span><span id="wbemqueryflagshallow"></span><span id="WBEMQUERYFLAGSHALLOW"></span>

<span data-ttu-id="a0e45-117"><span id="wbemQueryFlagShallow"></span><span id="wbemqueryflagshallow"></span><span id="WBEMQUERYFLAGSHALLOW"></span>Вбемкуерифлагшаллов \* \* \* \* (1 (0x1))</span><span class="sxs-lookup"><span data-stu-id="a0e45-117"><span id="wbemQueryFlagShallow"></span><span id="wbemqueryflagshallow"></span><span id="WBEMQUERYFLAGSHALLOW"></span>\*\*\*\*wbemQueryFlagShallow\*\*\*\* (1 (0x1))</span></span>


</dt> <dd>

<span data-ttu-id="a0e45-118">Значение по умолчанию для этого параметра.</span><span class="sxs-lookup"><span data-stu-id="a0e45-118">Default for this parameter.</span></span> <span data-ttu-id="a0e45-119">Он заставляет перечисление включать только непосредственные подклассы указанного родительского класса.</span><span class="sxs-lookup"><span data-stu-id="a0e45-119">It forces the enumeration to include only immediate subclasses of the specified parent class.</span></span>

</dd> <dt>

<span id="wbemFlagSendStatus"></span><span id="wbemflagsendstatus"></span><span id="WBEMFLAGSENDSTATUS"></span>

<span data-ttu-id="a0e45-120"><span id="wbemFlagSendStatus"></span><span id="wbemflagsendstatus"></span><span id="WBEMFLAGSENDSTATUS"></span>Вбемфлагсендстатус \* \* \* \* (128 (0x80))</span><span class="sxs-lookup"><span data-stu-id="a0e45-120"><span id="wbemFlagSendStatus"></span><span id="wbemflagsendstatus"></span><span id="WBEMFLAGSENDSTATUS"></span>\*\*\*\*wbemFlagSendStatus\*\*\*\* (128 (0x80))</span></span>


</dt> <dd>

<span data-ttu-id="a0e45-121">Вызывает асинхронные вызовы для отправки обновлений состояния обработчику событий [**свбемсинк. OnProgress**](swbemsink-onprogress.md) для приемника объекта.</span><span class="sxs-lookup"><span data-stu-id="a0e45-121">Causes asynchronous calls to send status updates to the [**SWbemSink.OnProgress**](swbemsink-onprogress.md) event handler for the object sink.</span></span>

</dd> <dt>

<span id="wbemFlagDontSendStatus"></span><span id="wbemflagdontsendstatus"></span><span id="WBEMFLAGDONTSENDSTATUS"></span>

<span data-ttu-id="a0e45-122"><span id="wbemFlagDontSendStatus"></span><span id="wbemflagdontsendstatus"></span><span id="WBEMFLAGDONTSENDSTATUS"></span>Вбемфлагдонтсендстатус \* \* \* \* (0 (0x0))</span><span class="sxs-lookup"><span data-stu-id="a0e45-122"><span id="wbemFlagDontSendStatus"></span><span id="wbemflagdontsendstatus"></span><span id="WBEMFLAGDONTSENDSTATUS"></span>\*\*\*\*wbemFlagDontSendStatus\*\*\*\* (0 (0x0))</span></span>


</dt> <dd>

<span data-ttu-id="a0e45-123">Не позволяет асинхронным вызовам отправлять обновления состояния в обработчик событий [**OnProgress**](swbemsink-onprogress.md) для приемника объекта.</span><span class="sxs-lookup"><span data-stu-id="a0e45-123">Prevents asynchronous calls from sending status updates to the [**OnProgress**](swbemsink-onprogress.md) event handler for the object sink.</span></span>

</dd> <dt>

<span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>

<span data-ttu-id="a0e45-124"><span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>Вбемфлагусеамендедкуалифиерс \* \* \* \* (131072 (0x20000))</span><span class="sxs-lookup"><span data-stu-id="a0e45-124"><span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>\*\*\*\*wbemFlagUseAmendedQualifiers\*\*\*\* (131072 (0x20000))</span></span>


</dt> <dd>

<span data-ttu-id="a0e45-125">Заставляет WMI возвращать данные о поправности класса с определением базового класса.</span><span class="sxs-lookup"><span data-stu-id="a0e45-125">Causes WMI to return class amendment data with the base class definition.</span></span> <span data-ttu-id="a0e45-126">Дополнительные сведения об измененных квалификаторах см. в разделе [Локализация сведений о классе WMI](localizing-wmi-class-information.md).</span><span class="sxs-lookup"><span data-stu-id="a0e45-126">For more information about amended qualifiers, see [Localizing WMI Class Information](localizing-wmi-class-information.md).</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="a0e45-127">*обжвбемнамедвалуесет* \[ в необязательное\]</span><span class="sxs-lookup"><span data-stu-id="a0e45-127">*objWbemNamedValueSet* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="a0e45-128">Как правило, это не определено.</span><span class="sxs-lookup"><span data-stu-id="a0e45-128">Typically, this is undefined.</span></span> <span data-ttu-id="a0e45-129">В противном случае это объект [**свбемнамедвалуесет**](swbemnamedvalueset.md) , элементы которого представляют сведения о контексте, которые могут использоваться поставщиком, обслуживающим запрос.</span><span class="sxs-lookup"><span data-stu-id="a0e45-129">Otherwise, this is an [**SWbemNamedValueSet**](swbemnamedvalueset.md) object whose elements represent the context information that can be used by the provider that is servicing the request.</span></span> <span data-ttu-id="a0e45-130">Поставщик, который поддерживает или требует такую информацию, должен документировать распознанные имена значений, тип данных значения, допустимые значения и семантику.</span><span class="sxs-lookup"><span data-stu-id="a0e45-130">A provider that supports or requires such information must document the recognized value names, data type of the value, allowed values, and semantics.</span></span>

</dd> <dt>

<span data-ttu-id="a0e45-131">*обжвбемасинкконтекст* \[ в необязательное\]</span><span class="sxs-lookup"><span data-stu-id="a0e45-131">*objWbemAsyncContext* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="a0e45-132">Это объект [**свбемнамедвалуесет**](swbemnamedvalueset.md) , который возвращает приемнику объекта, чтобы узнать источник исходного асинхронного вызова.</span><span class="sxs-lookup"><span data-stu-id="a0e45-132">This is an [**SWbemNamedValueSet**](swbemnamedvalueset.md) object that returns to the object sink to identify the source of the original asynchronous call.</span></span> <span data-ttu-id="a0e45-133">Используйте этот параметр при выполнении нескольких асинхронных вызовов с помощью одного и того же приемника объекта.</span><span class="sxs-lookup"><span data-stu-id="a0e45-133">Use this parameter when you make multiple asynchronous calls using the same object sink.</span></span> <span data-ttu-id="a0e45-134">Чтобы использовать этот параметр, создайте объект **свбемнамедвалуесет** и используйте метод [**свбемнамедвалуесет. Add**](swbemnamedvalueset-add.md) , чтобы добавить значение, идентифицирующее выполняемый асинхронный вызов.</span><span class="sxs-lookup"><span data-stu-id="a0e45-134">To use this parameter, create an **SWbemNamedValueSet** object, and use the [**SWbemNamedValueSet.Add**](swbemnamedvalueset-add.md) method to add a value that identifies the asynchronous call you are making.</span></span> <span data-ttu-id="a0e45-135">Этот объект **свбемнамедвалуесет** возвращается в приемник объекта, и источник вызова можно извлечь с помощью метода [**свбемнамедвалуесет. Item**](swbemnamedvalueset-item.md) .</span><span class="sxs-lookup"><span data-stu-id="a0e45-135">This **SWbemNamedValueSet** object is returned to the object sink, and the source of the call can be extracted using the [**SWbemNamedValueSet.Item**](swbemnamedvalueset-item.md) method.</span></span> <span data-ttu-id="a0e45-136">Дополнительные сведения см. [в разделе вызов метода](calling-a-method.md).</span><span class="sxs-lookup"><span data-stu-id="a0e45-136">For more information, see [Calling a Method](calling-a-method.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a0e45-137">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="a0e45-137">Return value</span></span>

<span data-ttu-id="a0e45-138">Этот метод не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="a0e45-138">This method does not return a value.</span></span> <span data-ttu-id="a0e45-139">В случае успешного выполнения приемник получает событие [**онобжектреади**](swbemsink-onobjectready.md) для каждого экземпляра.</span><span class="sxs-lookup"><span data-stu-id="a0e45-139">If successful, the sink receives an [**OnObjectReady**](swbemsink-onobjectready.md) event for each instance.</span></span> <span data-ttu-id="a0e45-140">После последнего экземпляра приемник объекта получает событие [**Oncompleteed**](swbemsink-oncompleted.md) .</span><span class="sxs-lookup"><span data-stu-id="a0e45-140">After the last instance, the object sink receives an [**OnCompleted**](swbemsink-oncompleted.md) event.</span></span>

## <a name="error-codes"></a><span data-ttu-id="a0e45-141">Коды ошибок</span><span class="sxs-lookup"><span data-stu-id="a0e45-141">Error codes</span></span>

<span data-ttu-id="a0e45-142">После завершения метода **субклассесасинк \_** объект [Err](/previous-versions//sbf5ze0e(v=vs.85)) может содержать один из кодов ошибок из следующего списка.</span><span class="sxs-lookup"><span data-stu-id="a0e45-142">After the completion of the **SubclassesAsync\_** method, the [Err](/previous-versions//sbf5ze0e(v=vs.85)) object may contain one of the error codes in the following list.</span></span>

<dl> <dt>

<span data-ttu-id="a0e45-143">**вбемерракцессдениед** -2147749891 (0x80041003)</span><span class="sxs-lookup"><span data-stu-id="a0e45-143">**wbemErrAccessDenied** - 2147749891 (0x80041003)</span></span>
</dt> <dd>

<span data-ttu-id="a0e45-144">У текущего пользователя нет разрешения на просмотр одного или нескольких классов, возвращенных вызовом.</span><span class="sxs-lookup"><span data-stu-id="a0e45-144">Current user does not have permission to view one or more of the classes returned by the call.</span></span>

</dd> <dt>

<span data-ttu-id="a0e45-145">**вбемеррфаилед** -2147749889 (0x80041001)</span><span class="sxs-lookup"><span data-stu-id="a0e45-145">**wbemErrFailed** - 2147749889 (0x80041001)</span></span>
</dt> <dd>

<span data-ttu-id="a0e45-146">Незаданная ошибка.</span><span class="sxs-lookup"><span data-stu-id="a0e45-146">Unspecified error.</span></span>

</dd> <dt>

<span data-ttu-id="a0e45-147">**вбемерринвалидкласс** -2147749904 (0x80041010)</span><span class="sxs-lookup"><span data-stu-id="a0e45-147">**wbemErrInvalidClass** - 2147749904 (0x80041010)</span></span>
</dt> <dd>

<span data-ttu-id="a0e45-148">Указанный класс не существует.</span><span class="sxs-lookup"><span data-stu-id="a0e45-148">Specified class does not exist.</span></span>

</dd> <dt>

<span data-ttu-id="a0e45-149">**вбемерринвалидпараметер** -2147749896 (0x80041008)</span><span class="sxs-lookup"><span data-stu-id="a0e45-149">**wbemErrInvalidParameter** - 2147749896 (0x80041008)</span></span>
</dt> <dd>

<span data-ttu-id="a0e45-150">Указан недопустимый параметр.</span><span class="sxs-lookup"><span data-stu-id="a0e45-150">Invalid parameter was specified.</span></span>

</dd> <dt>

<span data-ttu-id="a0e45-151">**вбемерраутофмемори** -2147749894 (0x80041006)</span><span class="sxs-lookup"><span data-stu-id="a0e45-151">**wbemErrOutOfMemory** - 2147749894 (0x80041006)</span></span>
</dt> <dd>

<span data-ttu-id="a0e45-152">Недостаточно памяти для завершения операции.</span><span class="sxs-lookup"><span data-stu-id="a0e45-152">Not enough memory to complete the operation.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="a0e45-153">Комментарии</span><span class="sxs-lookup"><span data-stu-id="a0e45-153">Remarks</span></span>

<span data-ttu-id="a0e45-154">Этот вызов возвращает немедленно.</span><span class="sxs-lookup"><span data-stu-id="a0e45-154">This call returns immediately.</span></span> <span data-ttu-id="a0e45-155">Запрошенные объекты и состояние возвращаются вызывающему объекту через обратные вызовы, доставляемые в приемник, указанный в *обжвбемсинк*.</span><span class="sxs-lookup"><span data-stu-id="a0e45-155">The requested objects and status are returned to the caller through callbacks delivered to the sink that is specified in *objWbemSink*.</span></span> <span data-ttu-id="a0e45-156">Чтобы обработать каждый объект при поступлении, создайте *обжвбемсинк*. Подпрограммы события [**онобжектреади**](swbemsink-onobjectready.md) .</span><span class="sxs-lookup"><span data-stu-id="a0e45-156">To process each object when it arrives, create an *objWbemSink*.[**OnObjectReady**](swbemsink-onobjectready.md) event subroutine.</span></span> <span data-ttu-id="a0e45-157">После возврата всех объектов можно выполнить окончательную обработку в реализации *обжвбемсинк*. Событие [**Oncompleteed**](swbemsink-oncompleted.md) .</span><span class="sxs-lookup"><span data-stu-id="a0e45-157">After all the objects are returned, you can perform final processing in your implementation of the *objWbemSink*.[**OnCompleted**](swbemsink-oncompleted.md) event.</span></span>

<span data-ttu-id="a0e45-158">Асинхронный обратный вызов позволяет пользователю без проверки подлинности предоставлять данные в приемник.</span><span class="sxs-lookup"><span data-stu-id="a0e45-158">An asynchronous callback allows a non-authenticated user to provide data to the sink.</span></span> <span data-ttu-id="a0e45-159">Это создает угрозы безопасности для сценариев и приложений.</span><span class="sxs-lookup"><span data-stu-id="a0e45-159">This poses security risks to your scripts and applications.</span></span> <span data-ttu-id="a0e45-160">Чтобы устранить риски, используйте либо семисинчронаус связь, либо синхронное взаимодействие.</span><span class="sxs-lookup"><span data-stu-id="a0e45-160">To eliminate the risks, use either semisynchronous communication or synchronous communication.</span></span> <span data-ttu-id="a0e45-161">Дополнительные сведения см. [в разделе вызов метода](calling-a-method.md).</span><span class="sxs-lookup"><span data-stu-id="a0e45-161">For more information, see [Calling a Method](calling-a-method.md).</span></span>

<span data-ttu-id="a0e45-162">Рекомендуется, чтобы скрипты проверяли источник вызова с помощью параметра *обжвбемасинкконтекст* .</span><span class="sxs-lookup"><span data-stu-id="a0e45-162">It is recommended that scripts verify the source of the call by using an *objWbemAsyncContext* parameter.</span></span>

<span data-ttu-id="a0e45-163">Если в возвращаемой коллекции нет подклассов текущего объекта, то не будет возвращать нулевые элементы.</span><span class="sxs-lookup"><span data-stu-id="a0e45-163">It is not an error for the returned collection to have zero elements if there are no subclasses of the current object.</span></span> <span data-ttu-id="a0e45-164">Метод **субклассесасинк \_** работает только для объектов класса.</span><span class="sxs-lookup"><span data-stu-id="a0e45-164">The **SubclassesAsync\_** method only works for class objects.</span></span>

## <a name="requirements"></a><span data-ttu-id="a0e45-165">Требования</span><span class="sxs-lookup"><span data-stu-id="a0e45-165">Requirements</span></span>



| <span data-ttu-id="a0e45-166">Требование</span><span class="sxs-lookup"><span data-stu-id="a0e45-166">Requirement</span></span> | <span data-ttu-id="a0e45-167">Значение</span><span class="sxs-lookup"><span data-stu-id="a0e45-167">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="a0e45-168">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="a0e45-168">Minimum supported client</span></span><br/> | <span data-ttu-id="a0e45-169">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="a0e45-169">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="a0e45-170">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="a0e45-170">Minimum supported server</span></span><br/> | <span data-ttu-id="a0e45-171">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="a0e45-171">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="a0e45-172">Header</span><span class="sxs-lookup"><span data-stu-id="a0e45-172">Header</span></span><br/>                   | <dl> <span data-ttu-id="a0e45-173"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="a0e45-173"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="a0e45-174">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="a0e45-174">Type library</span></span><br/>             | <dl> <span data-ttu-id="a0e45-175"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="a0e45-175"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="a0e45-176">DLL</span><span class="sxs-lookup"><span data-stu-id="a0e45-176">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a0e45-177"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a0e45-177"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="a0e45-178">CLSID</span><span class="sxs-lookup"><span data-stu-id="a0e45-178">CLSID</span></span><br/>                    | <span data-ttu-id="a0e45-179">\_SWBEMOBJECT CLSID</span><span class="sxs-lookup"><span data-stu-id="a0e45-179">CLSID\_SWbemObject</span></span><br/>                                                           |
| <span data-ttu-id="a0e45-180">IID</span><span class="sxs-lookup"><span data-stu-id="a0e45-180">IID</span></span><br/>                      | <span data-ttu-id="a0e45-181">IID \_ исвбемобжект</span><span class="sxs-lookup"><span data-stu-id="a0e45-181">IID\_ISWbemObject</span></span><br/>                                                            |



## <a name="see-also"></a><span data-ttu-id="a0e45-182">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="a0e45-182">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a0e45-183">**SWbemObject**</span><span class="sxs-lookup"><span data-stu-id="a0e45-183">**SWbemObject**</span></span>](swbemobject.md)
</dt> <dt>

[<span data-ttu-id="a0e45-184">**SWbemObjectSet**</span><span class="sxs-lookup"><span data-stu-id="a0e45-184">**SWbemObjectSet**</span></span>](swbemobjectset.md)
</dt> <dt>

[<span data-ttu-id="a0e45-185">**свбемрефрешаблеитем**</span><span class="sxs-lookup"><span data-stu-id="a0e45-185">**SWbemRefreshableItem**</span></span>](swbemrefreshableitem.md)
</dt> </dl>

 

