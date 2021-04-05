---
description: Метод Инстанцесасинк \_ объекта SWbemObject асинхронно предоставляет экземпляры текущего объекта класса. Этот метод реализует простой запрос. Более сложные запросы могут потребовать использования SWbemServices.ExeКкуери.
ms.assetid: d10fcbbf-6110-4152-8201-db43dc7a3c14
ms.tgt_platform: multiple
title: Метод SWbemObject.InstancesAsync_ (Wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemObject.InstancesAsync_
- ISWbemObject.InstancesAsync_
- ISWbemObject.InstancesAsync_
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 800e28184593e339f739fb52d488803666f552c6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103898549"
---
# <a name="swbemobjectinstancesasync_-method"></a><span data-ttu-id="3bb44-105">SWbemObject. Инстанцесасинк, \_ метод</span><span class="sxs-lookup"><span data-stu-id="3bb44-105">SWbemObject.InstancesAsync\_ method</span></span>

<span data-ttu-id="3bb44-106">Метод **инстанцесасинк \_** объекта [**SWbemObject**](swbemobject.md) асинхронно предоставляет экземпляры текущего объекта класса.</span><span class="sxs-lookup"><span data-stu-id="3bb44-106">The **InstancesAsync\_** method of [**SWbemObject**](swbemobject.md) asynchronously supplies the instances of the current class object.</span></span> <span data-ttu-id="3bb44-107">Этот метод реализует простой запрос.</span><span class="sxs-lookup"><span data-stu-id="3bb44-107">This method implements a simple query.</span></span> <span data-ttu-id="3bb44-108">Более сложные запросы могут потребовать использования [**SWbemServices.Exeккуери**](swbemservices-execquery.md).</span><span class="sxs-lookup"><span data-stu-id="3bb44-108">More complex queries may require the use of [**SWbemServices.ExecQuery**](swbemservices-execquery.md).</span></span>

<span data-ttu-id="3bb44-109">Описание этого синтаксиса см. в разделе [соглашения о документе для API скриптов](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="3bb44-109">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="3bb44-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="3bb44-110">Syntax</span></span>


```VB
SWbemObject.InstancesAsync_( _
  ByVal objWbemSink, _
  [ ByVal iFlags ], _
  [ ByVal objwbemNamedValueSet ], _
  [ ByVal objWbemAsyncContext ] _
)
```



## <a name="parameters"></a><span data-ttu-id="3bb44-111">Параметры</span><span class="sxs-lookup"><span data-stu-id="3bb44-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3bb44-112">*обжвбемсинк* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="3bb44-112">*objWbemSink* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3bb44-113">Приемник объекта, который возвращает экземпляры.</span><span class="sxs-lookup"><span data-stu-id="3bb44-113">Object sink that returns the instances.</span></span>

</dd> <dt>

<span data-ttu-id="3bb44-114">*ифлагс* \[ в необязательное\]</span><span class="sxs-lookup"><span data-stu-id="3bb44-114">*iFlags* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="3bb44-115">Целое число, определяющее поведение вызова.</span><span class="sxs-lookup"><span data-stu-id="3bb44-115">Integer that determines the behavior of the call.</span></span> <span data-ttu-id="3bb44-116">Этот параметр может принимать следующие значения.</span><span class="sxs-lookup"><span data-stu-id="3bb44-116">This parameter can accept the following values.</span></span>

<dt>

<span id="wbemFlagSendStatus"></span><span id="wbemflagsendstatus"></span><span id="WBEMFLAGSENDSTATUS"></span>

<span data-ttu-id="3bb44-117"><span id="wbemFlagSendStatus"></span><span id="wbemflagsendstatus"></span><span id="WBEMFLAGSENDSTATUS"></span>Вбемфлагсендстатус \* \* \* \* (128 (0x80))</span><span class="sxs-lookup"><span data-stu-id="3bb44-117"><span id="wbemFlagSendStatus"></span><span id="wbemflagsendstatus"></span><span id="WBEMFLAGSENDSTATUS"></span>\*\*\*\*wbemFlagSendStatus\*\*\*\* (128 (0x80))</span></span>


</dt> <dd>

<span data-ttu-id="3bb44-118">Вызывает асинхронные вызовы для отправки обновлений состояния обработчику событий [**свбемсинк. OnProgress**](swbemsink-onprogress.md) для приемника объекта.</span><span class="sxs-lookup"><span data-stu-id="3bb44-118">Causes asynchronous calls to send status updates to the [**SWbemSink.OnProgress**](swbemsink-onprogress.md) event handler for the object sink.</span></span>

</dd> <dt>

<span id="wbemFlagDontSendStatus"></span><span id="wbemflagdontsendstatus"></span><span id="WBEMFLAGDONTSENDSTATUS"></span>

<span data-ttu-id="3bb44-119"><span id="wbemFlagDontSendStatus"></span><span id="wbemflagdontsendstatus"></span><span id="WBEMFLAGDONTSENDSTATUS"></span>Вбемфлагдонтсендстатус \* \* \* \* (0 (0x0))</span><span class="sxs-lookup"><span data-stu-id="3bb44-119"><span id="wbemFlagDontSendStatus"></span><span id="wbemflagdontsendstatus"></span><span id="WBEMFLAGDONTSENDSTATUS"></span>\*\*\*\*wbemFlagDontSendStatus\*\*\*\* (0 (0x0))</span></span>


</dt> <dd>

<span data-ttu-id="3bb44-120">Не позволяет асинхронным вызовам отправлять обновления состояния в обработчик событий [**OnProgress**](swbemsink-onprogress.md) для приемника объекта.</span><span class="sxs-lookup"><span data-stu-id="3bb44-120">Prevents asynchronous calls from sending status updates to the [**OnProgress**](swbemsink-onprogress.md) event handler for the object sink.</span></span>

</dd> <dt>

<span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>

<span data-ttu-id="3bb44-121"><span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>Вбемфлагусеамендедкуалифиерс \* \* \* \* (131072 (0x20000))</span><span class="sxs-lookup"><span data-stu-id="3bb44-121"><span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>\*\*\*\*wbemFlagUseAmendedQualifiers\*\*\*\* (131072 (0x20000))</span></span>


</dt> <dd>

<span data-ttu-id="3bb44-122">Заставляет Инструментарий WMI возвращать локализованные описания классов и свойств.</span><span class="sxs-lookup"><span data-stu-id="3bb44-122">Causes WMI to return the localized class and property descriptions.</span></span> <span data-ttu-id="3bb44-123">Дополнительные сведения см. в разделе [Локализация сведений о классе WMI](localizing-wmi-class-information.md).</span><span class="sxs-lookup"><span data-stu-id="3bb44-123">For more information, see [Localizing WMI Class Information](localizing-wmi-class-information.md).</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="3bb44-124">*обжвбемнамедвалуесет* \[ в необязательное\]</span><span class="sxs-lookup"><span data-stu-id="3bb44-124">*objwbemNamedValueSet* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="3bb44-125">Как правило, это не определено.</span><span class="sxs-lookup"><span data-stu-id="3bb44-125">Typically, this is undefined.</span></span> <span data-ttu-id="3bb44-126">В противном случае это объект [**свбемнамедвалуесет**](swbemnamedvalueset.md) , элементы которого представляют сведения о контексте, которые могут использоваться поставщиком, обслуживающим запрос.</span><span class="sxs-lookup"><span data-stu-id="3bb44-126">Otherwise, this is an [**SWbemNamedValueSet**](swbemnamedvalueset.md) object whose elements represent the context information that can be used by the provider that is servicing the request.</span></span> <span data-ttu-id="3bb44-127">Поставщик, который поддерживает или требует такую информацию, должен документировать распознанные имена значений, тип данных значения, допустимые значения и семантику.</span><span class="sxs-lookup"><span data-stu-id="3bb44-127">A provider that supports or requires such information must document the recognized value names, data type of the value, allowed values, and semantics.</span></span>

</dd> <dt>

<span data-ttu-id="3bb44-128">*обжвбемасинкконтекст* \[ в необязательное\]</span><span class="sxs-lookup"><span data-stu-id="3bb44-128">*objWbemAsyncContext* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="3bb44-129">Это объект [**свбемнамедвалуесет**](swbemnamedvalueset.md) , который возвращает приемнику объекта, чтобы узнать источник исходного асинхронного вызова.</span><span class="sxs-lookup"><span data-stu-id="3bb44-129">This is an [**SWbemNamedValueSet**](swbemnamedvalueset.md) object that returns to the object sink to identify the source of the original asynchronous call.</span></span> <span data-ttu-id="3bb44-130">Используйте этот параметр, если вы выполняете несколько асинхронных вызовов, использующих один и тот же приемник объекта.</span><span class="sxs-lookup"><span data-stu-id="3bb44-130">Use this parameter if you are making multiple asynchronous calls using the same object sink.</span></span> <span data-ttu-id="3bb44-131">Чтобы использовать этот параметр, создайте объект **свбемнамедвалуесет** и используйте метод [**свбемнамедвалуесет. Add**](swbemnamedvalueset-add.md) , чтобы добавить значение, идентифицирующее выполняемый асинхронный вызов.</span><span class="sxs-lookup"><span data-stu-id="3bb44-131">To use this parameter, create an **SWbemNamedValueSet** object and use the [**SWbemNamedValueSet.Add**](swbemnamedvalueset-add.md) method to add a value that identifies the asynchronous call you are making.</span></span> <span data-ttu-id="3bb44-132">Этот объект **свбемнамедвалуесет** возвращается в приемник объекта, и источник вызова можно извлечь с помощью метода [**свбемнамедвалуесет. Item**](swbemnamedvalueset-item.md) .</span><span class="sxs-lookup"><span data-stu-id="3bb44-132">This **SWbemNamedValueSet** object is returned to the object sink and the source of the call can be extracted using the [**SWbemNamedValueSet.Item**](swbemnamedvalueset-item.md) method.</span></span> <span data-ttu-id="3bb44-133">Дополнительные сведения см. [в разделе вызов метода](calling-a-method.md).</span><span class="sxs-lookup"><span data-stu-id="3bb44-133">For more information, see [Calling a Method](calling-a-method.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3bb44-134">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="3bb44-134">Return value</span></span>

<span data-ttu-id="3bb44-135">Этот метод не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="3bb44-135">This method does not return a value.</span></span> <span data-ttu-id="3bb44-136">В случае успешного выполнения приемник получает событие [**онобжектреади**](swbemsink-onobjectready.md) для каждого экземпляра.</span><span class="sxs-lookup"><span data-stu-id="3bb44-136">If successful, the sink receives an [**OnObjectReady**](swbemsink-onobjectready.md) event per instance.</span></span> <span data-ttu-id="3bb44-137">После последнего экземпляра приемник объекта получит событие [**Oncompleteed**](swbemsink-oncompleted.md) .</span><span class="sxs-lookup"><span data-stu-id="3bb44-137">After the last instance, the object sink will receive an [**OnCompleted**](swbemsink-oncompleted.md) event.</span></span>

## <a name="error-codes"></a><span data-ttu-id="3bb44-138">Коды ошибок</span><span class="sxs-lookup"><span data-stu-id="3bb44-138">Error codes</span></span>

<span data-ttu-id="3bb44-139">После завершения метода **инстанцесасинк \_** объект [Err](/previous-versions//sbf5ze0e(v=vs.85)) может содержать один из кодов ошибок из следующего списка.</span><span class="sxs-lookup"><span data-stu-id="3bb44-139">After the completion of the **InstancesAsync\_** method, the [Err](/previous-versions//sbf5ze0e(v=vs.85)) object may contain one of the error codes in the following list.</span></span>

<dl> <dt>

<span data-ttu-id="3bb44-140">**вбемерракцессдениед** -2147749891 (0x80041003)</span><span class="sxs-lookup"><span data-stu-id="3bb44-140">**wbemErrAccessDenied** - 2147749891 (0x80041003)</span></span>
</dt> <dd>

<span data-ttu-id="3bb44-141">У текущего пользователя нет разрешения на просмотр экземпляров указанного класса.</span><span class="sxs-lookup"><span data-stu-id="3bb44-141">Current user does not have permission to view instances of the specified class.</span></span>

</dd> <dt>

<span data-ttu-id="3bb44-142">**вбемеррфаилед** -2147749889 (0x80041001)</span><span class="sxs-lookup"><span data-stu-id="3bb44-142">**wbemErrFailed** - 2147749889 (0x80041001)</span></span>
</dt> <dd>

<span data-ttu-id="3bb44-143">Произошла неопределенная ошибка.</span><span class="sxs-lookup"><span data-stu-id="3bb44-143">Unspecified error occurred.</span></span>

</dd> <dt>

<span data-ttu-id="3bb44-144">**вбемерринвалидкласс** -2147749904 (0x80041010)</span><span class="sxs-lookup"><span data-stu-id="3bb44-144">**wbemErrInvalidClass** - 2147749904 (0x80041010)</span></span>
</dt> <dd>

<span data-ttu-id="3bb44-145">Указан недопустимый класс.</span><span class="sxs-lookup"><span data-stu-id="3bb44-145">Specified class is not valid.</span></span>

</dd> <dt>

<span data-ttu-id="3bb44-146">**вбемерринвалидпараметер** -2147749896 (0x80041008)</span><span class="sxs-lookup"><span data-stu-id="3bb44-146">**wbemErrInvalidParameter** - 2147749896 (0x80041008)</span></span>
</dt> <dd>

<span data-ttu-id="3bb44-147">Указан недопустимый параметр.</span><span class="sxs-lookup"><span data-stu-id="3bb44-147">A specified parameter is not valid.</span></span>

</dd> <dt>

<span data-ttu-id="3bb44-148">**вбемерраутофмемори** -2147749894 (0x80041006)</span><span class="sxs-lookup"><span data-stu-id="3bb44-148">**wbemErrOutOfMemory** - 2147749894 (0x80041006)</span></span>
</dt> <dd>

<span data-ttu-id="3bb44-149">Недостаточно памяти для завершения операции.</span><span class="sxs-lookup"><span data-stu-id="3bb44-149">Not enough memory to complete the operation.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="3bb44-150">Комментарии</span><span class="sxs-lookup"><span data-stu-id="3bb44-150">Remarks</span></span>

<span data-ttu-id="3bb44-151">Этот вызов возвращает немедленно.</span><span class="sxs-lookup"><span data-stu-id="3bb44-151">This call returns immediately.</span></span> <span data-ttu-id="3bb44-152">Запрошенные объекты и состояние возвращаются вызывающему объекту через обратные вызовы, доставляемые в приемник, указанный в *обжвбемсинк*.</span><span class="sxs-lookup"><span data-stu-id="3bb44-152">The requested objects and status are returned to the caller through callbacks delivered to the sink that is specified in *objWbemSink*.</span></span> <span data-ttu-id="3bb44-153">Чтобы обработать каждый объект при поступлении, создайте *обжвбемсинк*.</span><span class="sxs-lookup"><span data-stu-id="3bb44-153">To process each object when it arrives, create an *objWbemSink*.</span></span> <span data-ttu-id="3bb44-154">Подпрограммы события [**онобжектреади**](swbemsink-onobjectready.md) .</span><span class="sxs-lookup"><span data-stu-id="3bb44-154">[**OnObjectReady**](swbemsink-onobjectready.md) event subroutine.</span></span> <span data-ttu-id="3bb44-155">После возврата всех объектов можно выполнить окончательную обработку в реализации *обжвбемсинк*.</span><span class="sxs-lookup"><span data-stu-id="3bb44-155">After all the objects are returned, you can perform final processing in your implementation of the *objWbemSink*.</span></span> <span data-ttu-id="3bb44-156">Событие [**Oncompleteed**](swbemsink-oncompleted.md) .</span><span class="sxs-lookup"><span data-stu-id="3bb44-156">[**OnCompleted**](swbemsink-oncompleted.md) event.</span></span>

<span data-ttu-id="3bb44-157">Асинхронный обратный вызов позволяет пользователю без проверки подлинности предоставлять данные в приемник.</span><span class="sxs-lookup"><span data-stu-id="3bb44-157">An asynchronous callback allows a non-authenticated user to provide data to the sink.</span></span> <span data-ttu-id="3bb44-158">Это создает угрозы безопасности для сценариев и приложений.</span><span class="sxs-lookup"><span data-stu-id="3bb44-158">This poses security risks to your scripts and applications.</span></span> <span data-ttu-id="3bb44-159">Чтобы устранить риски, используйте либо семисинчронаус связь, либо синхронное взаимодействие.</span><span class="sxs-lookup"><span data-stu-id="3bb44-159">To eliminate the risks, use either semisynchronous communication or synchronous communication.</span></span> <span data-ttu-id="3bb44-160">Дополнительные сведения см. [в разделе вызов метода](calling-a-method.md).</span><span class="sxs-lookup"><span data-stu-id="3bb44-160">For more information, see [Calling a Method](calling-a-method.md).</span></span>

<span data-ttu-id="3bb44-161">Метод **инстанцесасинк \_** работает только для объектов класса.</span><span class="sxs-lookup"><span data-stu-id="3bb44-161">The **InstancesAsync\_** method only works for class objects.</span></span> <span data-ttu-id="3bb44-162">Возвращаемая коллекция не может содержать нулевые (0) элементы.</span><span class="sxs-lookup"><span data-stu-id="3bb44-162">It is not an error for the returned collection to have zero (0) elements.</span></span>

## <a name="requirements"></a><span data-ttu-id="3bb44-163">Требования</span><span class="sxs-lookup"><span data-stu-id="3bb44-163">Requirements</span></span>



| <span data-ttu-id="3bb44-164">Требование</span><span class="sxs-lookup"><span data-stu-id="3bb44-164">Requirement</span></span> | <span data-ttu-id="3bb44-165">Значение</span><span class="sxs-lookup"><span data-stu-id="3bb44-165">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="3bb44-166">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="3bb44-166">Minimum supported client</span></span><br/> | <span data-ttu-id="3bb44-167">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="3bb44-167">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="3bb44-168">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="3bb44-168">Minimum supported server</span></span><br/> | <span data-ttu-id="3bb44-169">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="3bb44-169">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="3bb44-170">Header</span><span class="sxs-lookup"><span data-stu-id="3bb44-170">Header</span></span><br/>                   | <dl> <span data-ttu-id="3bb44-171"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="3bb44-171"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="3bb44-172">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="3bb44-172">Type library</span></span><br/>             | <dl> <span data-ttu-id="3bb44-173"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="3bb44-173"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="3bb44-174">DLL</span><span class="sxs-lookup"><span data-stu-id="3bb44-174">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3bb44-175"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3bb44-175"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="3bb44-176">CLSID</span><span class="sxs-lookup"><span data-stu-id="3bb44-176">CLSID</span></span><br/>                    | <span data-ttu-id="3bb44-177">\_SWBEMOBJECT CLSID</span><span class="sxs-lookup"><span data-stu-id="3bb44-177">CLSID\_SWbemObject</span></span><br/>                                                           |
| <span data-ttu-id="3bb44-178">IID</span><span class="sxs-lookup"><span data-stu-id="3bb44-178">IID</span></span><br/>                      | <span data-ttu-id="3bb44-179">IID \_ исвбемобжект</span><span class="sxs-lookup"><span data-stu-id="3bb44-179">IID\_ISWbemObject</span></span><br/>                                                            |



## <a name="see-also"></a><span data-ttu-id="3bb44-180">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="3bb44-180">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3bb44-181">**SWbemObject**</span><span class="sxs-lookup"><span data-stu-id="3bb44-181">**SWbemObject**</span></span>](swbemobject.md)
</dt> <dt>

[<span data-ttu-id="3bb44-182">**SWbemObjectSet**</span><span class="sxs-lookup"><span data-stu-id="3bb44-182">**SWbemObjectSet**</span></span>](swbemobjectset.md)
</dt> </dl>

 

