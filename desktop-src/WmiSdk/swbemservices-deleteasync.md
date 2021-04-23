---
description: Удаляет класс или экземпляр, указанный в пути объекта.
ms.assetid: f5ed170e-d002-4dd9-b8b6-b764a7a41a27
ms.tgt_platform: multiple
title: SWbemServices. DeleteAsync, метод (Wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemServices.DeleteAsync
- ISWbemServices.DeleteAsync
- ISWbemServices.DeleteAsync
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: adc8811c11f67b9fc92628740bd15df2086948d9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105711626"
---
# <a name="swbemservicesdeleteasync-method"></a><span data-ttu-id="7907a-103">SWbemServices. DeleteAsync, метод</span><span class="sxs-lookup"><span data-stu-id="7907a-103">SWbemServices.DeleteAsync method</span></span>

<span data-ttu-id="7907a-104">Метод **DeleteAsync** объекта [**SwbemServices**](swbemservices.md) удаляет класс или экземпляр, указанный в пути объекта.</span><span class="sxs-lookup"><span data-stu-id="7907a-104">The **DeleteAsync** method of the [**SWbemServices**](swbemservices.md) object deletes the class or instance specified in the object path.</span></span> <span data-ttu-id="7907a-105">Вызов **DeleteAsync** немедленно возвращает результат, а результаты и состояние возвращаются вызывающему через события, доставляемые в приемник, указанный в *обжвбемсинк*.</span><span class="sxs-lookup"><span data-stu-id="7907a-105">The call to **DeleteAsync** returns immediately and the results and status are returned to the caller through events delivered to the sink that is specified in *objWbemSink*.</span></span> <span data-ttu-id="7907a-106">Дополнительные сведения о создании приемника см. [в разделе Получение WMI-события](receiving-a-wmi-event.md).</span><span class="sxs-lookup"><span data-stu-id="7907a-106">For more information about creating a sink, see [Receiving a WMI Event](receiving-a-wmi-event.md).</span></span> <span data-ttu-id="7907a-107">Удалять можно только объекты из пространства имен, к которому вы подключены.</span><span class="sxs-lookup"><span data-stu-id="7907a-107">You can only delete objects in the namespace to which you are connected.</span></span>

<span data-ttu-id="7907a-108">Если в динамическом поставщике предоставлен класс или экземпляр, то иногда невозможно удалить этот объект, если поставщик не поддерживает удаление класса или экземпляра.</span><span class="sxs-lookup"><span data-stu-id="7907a-108">If a dynamic provider supplies the class or instance, sometimes it is not possible to delete this object unless the provider supports class or instance deletion.</span></span>

<span data-ttu-id="7907a-109">Метод вызывается в асинхронном режиме.</span><span class="sxs-lookup"><span data-stu-id="7907a-109">The method is called in the asynchronous mode.</span></span> <span data-ttu-id="7907a-110">Дополнительные сведения см. [в разделе вызов метода](calling-a-method.md).</span><span class="sxs-lookup"><span data-stu-id="7907a-110">For more information, see [Calling a Method](calling-a-method.md).</span></span>

<span data-ttu-id="7907a-111">Описание этого синтаксиса см. в разделе [соглашения о документе для API скриптов](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="7907a-111">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="7907a-112">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="7907a-112">Syntax</span></span>


```VB
SWbemServices.DeleteAsync( _
  [ ByVal ObjWbemSink ], _
  ByVal strObjectPath, _
  [ ByVal iFlags ], _
  [ ByVal objWbemNamedValueSet ], _
  [ ByVal objWbemAsyncContext ] _
)
```



## <a name="parameters"></a><span data-ttu-id="7907a-113">Параметры</span><span class="sxs-lookup"><span data-stu-id="7907a-113">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7907a-114">*Обжвбемсинк* \[ используемых\]</span><span class="sxs-lookup"><span data-stu-id="7907a-114">*ObjWbemSink* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="7907a-115">Приемник объекта, который получает результаты удаления.</span><span class="sxs-lookup"><span data-stu-id="7907a-115">Object sink that receives the results of the deletion.</span></span> <span data-ttu-id="7907a-116">Создайте объект [**свбемсинк**](swbemsink.md) для получения объектов.</span><span class="sxs-lookup"><span data-stu-id="7907a-116">Create an [**SWbemSink**](swbemsink.md) object to receive the objects.</span></span>

</dd> <dt>

<span data-ttu-id="7907a-117">*стробжектпас*</span><span class="sxs-lookup"><span data-stu-id="7907a-117">*strObjectPath*</span></span> 
</dt> <dd>

<span data-ttu-id="7907a-118">Обязательный.</span><span class="sxs-lookup"><span data-stu-id="7907a-118">Required.</span></span> <span data-ttu-id="7907a-119">Строка, содержащая путь к объекту, который необходимо удалить.</span><span class="sxs-lookup"><span data-stu-id="7907a-119">String that contains the object path to the object that you want to delete.</span></span> <span data-ttu-id="7907a-120">Дополнительные сведения см. [в разделе Описание расположения объекта WMI](describing-the-location-of-a-wmi-object.md).</span><span class="sxs-lookup"><span data-stu-id="7907a-120">For more information, see [Describing the Location of a WMI Object](describing-the-location-of-a-wmi-object.md).</span></span>

</dd> <dt>

<span data-ttu-id="7907a-121">*ифлагс* \[ используемых\]</span><span class="sxs-lookup"><span data-stu-id="7907a-121">*iFlags* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="7907a-122">Определяет, возвращаются ли обновления состояния.</span><span class="sxs-lookup"><span data-stu-id="7907a-122">Determines if status updates are returned.</span></span> <span data-ttu-id="7907a-123">Этот параметр может принимать следующие значения.</span><span class="sxs-lookup"><span data-stu-id="7907a-123">This parameter can accept the following values.</span></span>

<dt>

<span id="wbemFlagSendStatus"></span><span id="wbemflagsendstatus"></span><span id="WBEMFLAGSENDSTATUS"></span>

<span data-ttu-id="7907a-124"><span id="wbemFlagSendStatus"></span><span id="wbemflagsendstatus"></span><span id="WBEMFLAGSENDSTATUS"></span>Вбемфлагсендстатус \* \* \* \* (128 (0x80))</span><span class="sxs-lookup"><span data-stu-id="7907a-124"><span id="wbemFlagSendStatus"></span><span id="wbemflagsendstatus"></span><span id="WBEMFLAGSENDSTATUS"></span>\*\*\*\*wbemFlagSendStatus\*\*\*\* (128 (0x80))</span></span>


</dt> <dd>

<span data-ttu-id="7907a-125">Вызывает асинхронные вызовы для отправки обновлений состояния обработчику событий [**OnProgress**](swbemsink-onprogress.md) для приемника объекта.</span><span class="sxs-lookup"><span data-stu-id="7907a-125">Causes asynchronous calls to send status updates to the [**OnProgress**](swbemsink-onprogress.md) event handler for the object sink.</span></span>

</dd> <dt>

<span id="wbemFlagDontSendStatus"></span><span id="wbemflagdontsendstatus"></span><span id="WBEMFLAGDONTSENDSTATUS"></span>

<span data-ttu-id="7907a-126"><span id="wbemFlagDontSendStatus"></span><span id="wbemflagdontsendstatus"></span><span id="WBEMFLAGDONTSENDSTATUS"></span>Вбемфлагдонтсендстатус \* \* \* \* (0 (0x0))</span><span class="sxs-lookup"><span data-stu-id="7907a-126"><span id="wbemFlagDontSendStatus"></span><span id="wbemflagdontsendstatus"></span><span id="WBEMFLAGDONTSENDSTATUS"></span>\*\*\*\*wbemFlagDontSendStatus\*\*\*\* (0 (0x0))</span></span>


</dt> <dd>

<span data-ttu-id="7907a-127">Не позволяет асинхронным вызовам отправлять обновления состояния в обработчик событий [**OnProgress**](swbemsink-onprogress.md) для приемника объекта.</span><span class="sxs-lookup"><span data-stu-id="7907a-127">Prevents asynchronous calls from sending status updates to the [**OnProgress**](swbemsink-onprogress.md) event handler for the object sink.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="7907a-128">*обжвбемнамедвалуесет* \[ используемых\]</span><span class="sxs-lookup"><span data-stu-id="7907a-128">*objWbemNamedValueSet* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="7907a-129">Как правило, это не определено.</span><span class="sxs-lookup"><span data-stu-id="7907a-129">Typically, this is undefined.</span></span> <span data-ttu-id="7907a-130">В противном случае это объект [**свбемнамедвалуесет**](swbemnamedvalueset.md) , элементы которого представляют сведения о контексте, которые могут использоваться поставщиком, обслуживающим запрос.</span><span class="sxs-lookup"><span data-stu-id="7907a-130">Otherwise, this is an [**SWbemNamedValueSet**](swbemnamedvalueset.md) object whose elements represent the context information that can be used by the provider that is servicing the request.</span></span> <span data-ttu-id="7907a-131">Поставщик, который поддерживает или требует такую информацию, должен документировать распознанные имена значений, тип данных значения, допустимые значения и семантику.</span><span class="sxs-lookup"><span data-stu-id="7907a-131">A provider that supports or requires such information must document the recognized value names, data type of the value, allowed values, and semantics.</span></span>

</dd> <dt>

<span data-ttu-id="7907a-132">*обжвбемасинкконтекст* \[ используемых\]</span><span class="sxs-lookup"><span data-stu-id="7907a-132">*objWbemAsyncContext* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="7907a-133">Объект [**свбемнамедвалуесет**](swbemnamedvalueset.md) , возвращающий приемник объекта для обнаружения источника исходного асинхронного вызова.</span><span class="sxs-lookup"><span data-stu-id="7907a-133">An [**SWbemNamedValueSet**](swbemnamedvalueset.md) object that returns to the object sink to identify the source of the original asynchronous call.</span></span> <span data-ttu-id="7907a-134">Используйте этот параметр, если вы выполняете несколько асинхронных вызовов, использующих один и тот же приемник объекта.</span><span class="sxs-lookup"><span data-stu-id="7907a-134">Use this parameter if you are making multiple asynchronous calls using the same object sink.</span></span> <span data-ttu-id="7907a-135">Чтобы использовать этот параметр, создайте объект **свбемнамедвалуесет** и используйте метод [**свбемнамедвалуесет. Add**](swbemnamedvalueset-add.md) , чтобы добавить значение, идентифицирующее выполняемый асинхронный вызов.</span><span class="sxs-lookup"><span data-stu-id="7907a-135">To use this parameter, create an **SWbemNamedValueSet** object and use the [**SWbemNamedValueSet.Add**](swbemnamedvalueset-add.md) method to add a value that identifies the asynchronous call you are making.</span></span> <span data-ttu-id="7907a-136">Этот объект **свбемнамедвалуесет** возвращается в приемник объекта, и источник вызова можно извлечь с помощью метода [**свбемнамедвалуесет. Item**](swbemnamedvalueset-item.md) .</span><span class="sxs-lookup"><span data-stu-id="7907a-136">This **SWbemNamedValueSet** object is returned to the object sink and the source of the call can be extracted using the [**SWbemNamedValueSet.Item**](swbemnamedvalueset-item.md) method.</span></span> <span data-ttu-id="7907a-137">Дополнительные сведения см. [в разделе вызов метода](calling-a-method.md).</span><span class="sxs-lookup"><span data-stu-id="7907a-137">For more information, see [Calling a Method](calling-a-method.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7907a-138">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="7907a-138">Return value</span></span>

<span data-ttu-id="7907a-139">Этот метод не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="7907a-139">This method does not return a value.</span></span> <span data-ttu-id="7907a-140">Если вызов выполнен успешно, приемник объекта получает уведомление об удалении.</span><span class="sxs-lookup"><span data-stu-id="7907a-140">If the call is successful, the object sink receives notification of the deletion.</span></span>

## <a name="error-codes"></a><span data-ttu-id="7907a-141">Коды ошибок</span><span class="sxs-lookup"><span data-stu-id="7907a-141">Error codes</span></span>

<span data-ttu-id="7907a-142">После завершения метода **DeleteAsync** объект [Err](/previous-versions//sbf5ze0e(v=vs.85)) может содержать один из кодов ошибок из следующего списка.</span><span class="sxs-lookup"><span data-stu-id="7907a-142">After the completion of the **DeleteAsync** method, the [Err](/previous-versions//sbf5ze0e(v=vs.85)) object may contain one of the error codes in the following list.</span></span>

<dl> <dt>

<span data-ttu-id="7907a-143">**вбемеррфаилед** -2147749889 (0x80041001)</span><span class="sxs-lookup"><span data-stu-id="7907a-143">**wbemErrFailed** - 2147749889 (0x80041001)</span></span>
</dt> <dd>

<span data-ttu-id="7907a-144">Незаданная ошибка.</span><span class="sxs-lookup"><span data-stu-id="7907a-144">Unspecified error.</span></span>

</dd> <dt>

<span data-ttu-id="7907a-145">**вбемерринвалидпараметер** -2147749896 (0x80041008)</span><span class="sxs-lookup"><span data-stu-id="7907a-145">**wbemErrInvalidParameter** - 2147749896 (0x80041008)</span></span>
</dt> <dd>

<span data-ttu-id="7907a-146">Указан недопустимый параметр.</span><span class="sxs-lookup"><span data-stu-id="7907a-146">Invalid parameter was specified.</span></span>

</dd> <dt>

<span data-ttu-id="7907a-147">**вбемерраутофмемори** -2147749894 (0x80041006)</span><span class="sxs-lookup"><span data-stu-id="7907a-147">**wbemErrOutOfMemory** - 2147749894 (0x80041006)</span></span>
</dt> <dd>

<span data-ttu-id="7907a-148">Недостаточно памяти для завершения операции.</span><span class="sxs-lookup"><span data-stu-id="7907a-148">Not enough memory to complete the operation.</span></span>

</dd> <dt>

<span data-ttu-id="7907a-149">**вбемерртранспортфаилуре** -2147749909 (0x80041015)</span><span class="sxs-lookup"><span data-stu-id="7907a-149">**wbemErrTransportFailure** - 2147749909 (0x80041015)</span></span>
</dt> <dd>

<span data-ttu-id="7907a-150">Произошла сетевая ошибка, препятствующая нормальной работе.</span><span class="sxs-lookup"><span data-stu-id="7907a-150">Networking error occurred, preventing normal operation.</span></span>

</dd> <dt>

<span data-ttu-id="7907a-151">**вбемерракцессдениед** -2147749891 (0x80041003)</span><span class="sxs-lookup"><span data-stu-id="7907a-151">**wbemErrAccessDenied** - 2147749891 (0x80041003)</span></span>
</dt> <dd>

<span data-ttu-id="7907a-152">Текущее или указанное имя пользователя и пароль не являются допустимыми или разрешены для создания подключения.</span><span class="sxs-lookup"><span data-stu-id="7907a-152">Current or specified user name and password are not valid or authorized to make the connection.</span></span>

</dd> <dt>

<span data-ttu-id="7907a-153">**вбемеррнотфаунд** -2147749890 (0x80041002)</span><span class="sxs-lookup"><span data-stu-id="7907a-153">**wbemErrNotFound** - 2147749890 (0x80041002)</span></span>
</dt> <dd>

<span data-ttu-id="7907a-154">Запрошенный элемент не найден.</span><span class="sxs-lookup"><span data-stu-id="7907a-154">Requested item was not found.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="7907a-155">Комментарии</span><span class="sxs-lookup"><span data-stu-id="7907a-155">Remarks</span></span>

<span data-ttu-id="7907a-156">Этот вызов возвращает немедленно.</span><span class="sxs-lookup"><span data-stu-id="7907a-156">This call returns immediately.</span></span> <span data-ttu-id="7907a-157">Состояние операции удаления возвращается вызывающему объекту через обратный вызов, доставленный в приемник, указанный в *обжвбемсинк*.</span><span class="sxs-lookup"><span data-stu-id="7907a-157">The status of the delete operation is returned to the caller through a callback delivered to the sink that is specified in *objWbemSink*.</span></span> <span data-ttu-id="7907a-158">Вы можете выполнить окончательную обработку в реализации *обжвбемсинк*. Событие [**Oncompleteed**](swbemsink-oncompleted.md) .</span><span class="sxs-lookup"><span data-stu-id="7907a-158">You can perform final processing in your implementation of the *objWbemSink*.[**OnCompleted**](swbemsink-oncompleted.md) event.</span></span>

<span data-ttu-id="7907a-159">Асинхронный обратный вызов позволяет пользователю без проверки подлинности предоставлять данные в приемник.</span><span class="sxs-lookup"><span data-stu-id="7907a-159">An asynchronous callback allows a non-authenticated user to provide data to the sink.</span></span> <span data-ttu-id="7907a-160">Это создает угрозы безопасности для сценариев и приложений.</span><span class="sxs-lookup"><span data-stu-id="7907a-160">This poses security risks to your scripts and applications.</span></span> <span data-ttu-id="7907a-161">Сведения об устранении рисков см. в разделе [Настройка безопасности при асинхронном вызове](setting-security-on-an-asynchronous-call.md).</span><span class="sxs-lookup"><span data-stu-id="7907a-161">To eliminate the risks, see [Setting Security on an Asynchronous Call](setting-security-on-an-asynchronous-call.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="7907a-162">Требования</span><span class="sxs-lookup"><span data-stu-id="7907a-162">Requirements</span></span>



| <span data-ttu-id="7907a-163">Требование</span><span class="sxs-lookup"><span data-stu-id="7907a-163">Requirement</span></span> | <span data-ttu-id="7907a-164">Значение</span><span class="sxs-lookup"><span data-stu-id="7907a-164">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="7907a-165">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="7907a-165">Minimum supported client</span></span><br/> | <span data-ttu-id="7907a-166">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="7907a-166">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="7907a-167">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="7907a-167">Minimum supported server</span></span><br/> | <span data-ttu-id="7907a-168">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="7907a-168">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="7907a-169">Header</span><span class="sxs-lookup"><span data-stu-id="7907a-169">Header</span></span><br/>                   | <dl> <span data-ttu-id="7907a-170"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="7907a-170"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="7907a-171">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="7907a-171">Type library</span></span><br/>             | <dl> <span data-ttu-id="7907a-172"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="7907a-172"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="7907a-173">DLL</span><span class="sxs-lookup"><span data-stu-id="7907a-173">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7907a-174"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7907a-174"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="7907a-175">CLSID</span><span class="sxs-lookup"><span data-stu-id="7907a-175">CLSID</span></span><br/>                    | <span data-ttu-id="7907a-176">\_SWBEMSERVICES CLSID</span><span class="sxs-lookup"><span data-stu-id="7907a-176">CLSID\_SWbemServices</span></span><br/>                                                         |
| <span data-ttu-id="7907a-177">IID</span><span class="sxs-lookup"><span data-stu-id="7907a-177">IID</span></span><br/>                      | <span data-ttu-id="7907a-178">IID \_ исвбемсервицес</span><span class="sxs-lookup"><span data-stu-id="7907a-178">IID\_ISWbemServices</span></span><br/>                                                          |



## <a name="see-also"></a><span data-ttu-id="7907a-179">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="7907a-179">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7907a-180">**SWbemServices**</span><span class="sxs-lookup"><span data-stu-id="7907a-180">**SWbemServices**</span></span>](swbemservices.md)
</dt> <dt>

[<span data-ttu-id="7907a-181">**свбемобжектпас**</span><span class="sxs-lookup"><span data-stu-id="7907a-181">**SWbemObjectPath**</span></span>](swbemobjectpath.md)
</dt> </dl>

 

