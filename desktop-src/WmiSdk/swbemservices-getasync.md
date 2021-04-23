---
description: Извлекает объект, который является определением класса или экземпляром, на основе пути к объекту.
ms.assetid: 8da46851-52b8-4b5a-8c9d-1d492f57f4b6
ms.tgt_platform: multiple
title: Метод SWbemServices. async (Wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemServices.GetAsync
- ISWbemServices.GetAsync
- ISWbemServices.GetAsync
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 451f13bde9458e7d57ec393f42b92a4092c99924
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103898529"
---
# <a name="swbemservicesgetasync-method"></a><span data-ttu-id="448fe-103">SWbemServices. async, метод</span><span class="sxs-lookup"><span data-stu-id="448fe-103">SWbemServices.GetAsync method</span></span>

<span data-ttu-id="448fe-104">Метод **Async** объекта [**SwbemServices**](swbemservices.md) извлекает объект, который является определением класса или экземпляром, на основе пути к объекту.</span><span class="sxs-lookup"><span data-stu-id="448fe-104">The **GetAsync** method of the [**SWbemServices**](swbemservices.md) object retrieves an object, that is a class definition or an instance, based on the object path.</span></span>

<span data-ttu-id="448fe-105">Этот метод извлекает только объекты из пространства имен, связанного с текущим объектом [**SwbemServices**](swbemservices.md) .</span><span class="sxs-lookup"><span data-stu-id="448fe-105">This method retrieves only objects from the namespace that is associated with the current [**SWbemServices**](swbemservices.md) object.</span></span>

<span data-ttu-id="448fe-106">Этот метод вызывается в асинхронном режиме.</span><span class="sxs-lookup"><span data-stu-id="448fe-106">This method is called in the asynchronous mode.</span></span> <span data-ttu-id="448fe-107">Дополнительные сведения см. [в разделе вызов метода](calling-a-method.md).</span><span class="sxs-lookup"><span data-stu-id="448fe-107">For more information, see [Calling a Method](calling-a-method.md).</span></span>

<span data-ttu-id="448fe-108">Описание этого синтаксиса см. в разделе [соглашения о документе для API скриптов](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="448fe-108">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="448fe-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="448fe-109">Syntax</span></span>


```VB
SWbemServices.GetAsync( _
  ByVal objWbemSink, _
  [ ByVal strObjectPath ], _
  [ ByVal iFlags ], _
  [ ByVal objwbemNamedValueSet ], _
  [ ByVal objWbemAsyncContext ] _
)
```



## <a name="parameters"></a><span data-ttu-id="448fe-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="448fe-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="448fe-111">*обжвбемсинк*</span><span class="sxs-lookup"><span data-stu-id="448fe-111">*objWbemSink*</span></span> 
</dt> <dd>

<span data-ttu-id="448fe-112">Обязательный.</span><span class="sxs-lookup"><span data-stu-id="448fe-112">Required.</span></span> <span data-ttu-id="448fe-113">Приемник объекта, который получает объекты асинхронно.</span><span class="sxs-lookup"><span data-stu-id="448fe-113">Object sink that gets objects asynchronously.</span></span> <span data-ttu-id="448fe-114">Создайте объект [**свбемсинк**](swbemsink.md) для получения объектов.</span><span class="sxs-lookup"><span data-stu-id="448fe-114">Create a [**SWbemSink**](swbemsink.md) object to receive the objects.</span></span>

</dd> <dt>

<span data-ttu-id="448fe-115">*стробжектпас* \[ используемых\]</span><span class="sxs-lookup"><span data-stu-id="448fe-115">*strObjectPath* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="448fe-116">Путь к объекту, который требуется получить.</span><span class="sxs-lookup"><span data-stu-id="448fe-116">Path of the object that you want to retrieve.</span></span> <span data-ttu-id="448fe-117">Если это значение пустое, возвращаемый пустой объект может стать новым классом.</span><span class="sxs-lookup"><span data-stu-id="448fe-117">If this value is empty, the empty object that is returned can become a new class.</span></span> <span data-ttu-id="448fe-118">Дополнительные сведения см. [в разделе Описание расположения объекта WMI](describing-the-location-of-a-wmi-object.md).</span><span class="sxs-lookup"><span data-stu-id="448fe-118">For more information, see [Describing the Location of a WMI Object](describing-the-location-of-a-wmi-object.md).</span></span>

</dd> <dt>

<span data-ttu-id="448fe-119">*ифлагс* \[ используемых\]</span><span class="sxs-lookup"><span data-stu-id="448fe-119">*iFlags* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="448fe-120">Целое число, определяющее поведение вызова.</span><span class="sxs-lookup"><span data-stu-id="448fe-120">Integer that determines the behavior of the call.</span></span> <span data-ttu-id="448fe-121">Этот параметр может принимать следующие значения.</span><span class="sxs-lookup"><span data-stu-id="448fe-121">This parameter can accept the following values.</span></span>

<dt>

<span id="wbemFlagSendStatus"></span><span id="wbemflagsendstatus"></span><span id="WBEMFLAGSENDSTATUS"></span>

<span data-ttu-id="448fe-122"><span id="wbemFlagSendStatus"></span><span id="wbemflagsendstatus"></span><span id="WBEMFLAGSENDSTATUS"></span>Вбемфлагсендстатус \* \* \* \* (128 (0x80))</span><span class="sxs-lookup"><span data-stu-id="448fe-122"><span id="wbemFlagSendStatus"></span><span id="wbemflagsendstatus"></span><span id="WBEMFLAGSENDSTATUS"></span>\*\*\*\*wbemFlagSendStatus\*\*\*\* (128 (0x80))</span></span>


</dt> <dd>

<span data-ttu-id="448fe-123">Вызывает асинхронные вызовы для отправки обновлений состояния обработчику событий [**OnProgress**](swbemsink-onprogress.md) для приемника объекта.</span><span class="sxs-lookup"><span data-stu-id="448fe-123">Causes asynchronous calls to send status updates to the [**OnProgress**](swbemsink-onprogress.md) event handler for the object sink.</span></span>

</dd> <dt>

<span id="wbemFlagDontSendStatus"></span><span id="wbemflagdontsendstatus"></span><span id="WBEMFLAGDONTSENDSTATUS"></span>

<span data-ttu-id="448fe-124"><span id="wbemFlagDontSendStatus"></span><span id="wbemflagdontsendstatus"></span><span id="WBEMFLAGDONTSENDSTATUS"></span>Вбемфлагдонтсендстатус \* \* \* \* (0 (0x0))</span><span class="sxs-lookup"><span data-stu-id="448fe-124"><span id="wbemFlagDontSendStatus"></span><span id="wbemflagdontsendstatus"></span><span id="WBEMFLAGDONTSENDSTATUS"></span>\*\*\*\*wbemFlagDontSendStatus\*\*\*\* (0 (0x0))</span></span>


</dt> <dd>

<span data-ttu-id="448fe-125">Не позволяет асинхронным вызовам отправлять обновления состояния в обработчик событий [**OnProgress**](swbemsink-onprogress.md) для приемника объекта.</span><span class="sxs-lookup"><span data-stu-id="448fe-125">Prevents asynchronous calls from sending status updates to the [**OnProgress**](swbemsink-onprogress.md) event handler for the object sink.</span></span>

</dd> <dt>

<span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>

<span data-ttu-id="448fe-126"><span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>Вбемфлагусеамендедкуалифиерс \* \* \* \* (131072 (0x20000))</span><span class="sxs-lookup"><span data-stu-id="448fe-126"><span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>\*\*\*\*wbemFlagUseAmendedQualifiers\*\*\*\* (131072 (0x20000))</span></span>


</dt> <dd>

<span data-ttu-id="448fe-127">Заставляет WMI возвращать данные о поправности класса с определением базового класса.</span><span class="sxs-lookup"><span data-stu-id="448fe-127">Causes WMI to return class amendment data with the base class definition.</span></span> <span data-ttu-id="448fe-128">Дополнительные сведения см. в разделе [Локализация сведений о классе WMI](localizing-wmi-class-information.md).</span><span class="sxs-lookup"><span data-stu-id="448fe-128">For more information, see [Localizing WMI Class Information](localizing-wmi-class-information.md).</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="448fe-129">*обжвбемнамедвалуесет* \[ используемых\]</span><span class="sxs-lookup"><span data-stu-id="448fe-129">*objwbemNamedValueSet* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="448fe-130">Как правило, это значение не определено.</span><span class="sxs-lookup"><span data-stu-id="448fe-130">Typically, this value is undefined.</span></span> <span data-ttu-id="448fe-131">В противном случае это объект [**свбемнамедвалуесет**](swbemnamedvalueset.md) , элементы которого представляют сведения о контексте, которые могут использоваться поставщиком, обслуживающим запрос.</span><span class="sxs-lookup"><span data-stu-id="448fe-131">Otherwise, this is an [**SWbemNamedValueSet**](swbemnamedvalueset.md) object whose elements represent the context information that can be used by the provider that is servicing the request.</span></span> <span data-ttu-id="448fe-132">Поставщик, который поддерживает или требует такую информацию, должен документировать распознанные имена значений, тип данных значения, допустимые значения и семантику.</span><span class="sxs-lookup"><span data-stu-id="448fe-132">A provider that supports or requires such information must document the recognized value names, data type of the value, allowed values, and semantics.</span></span>

</dd> <dt>

<span data-ttu-id="448fe-133">*обжвбемасинкконтекст* \[ используемых\]</span><span class="sxs-lookup"><span data-stu-id="448fe-133">*objWbemAsyncContext* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="448fe-134">Объект [**свбемнамедвалуесет**](swbemnamedvalueset.md) , возвращающий приемник объекта для обнаружения источника исходного асинхронного вызова.</span><span class="sxs-lookup"><span data-stu-id="448fe-134">An [**SWbemNamedValueSet**](swbemnamedvalueset.md) object that returns to the object sink to identify the source of the original asynchronous call.</span></span> <span data-ttu-id="448fe-135">Используйте этот параметр, если вы выполняете несколько асинхронных вызовов, использующих один и тот же приемник объекта.</span><span class="sxs-lookup"><span data-stu-id="448fe-135">Use this parameter if you are making multiple asynchronous calls using the same object sink.</span></span> <span data-ttu-id="448fe-136">Чтобы использовать этот параметр, создайте объект **свбемнамедвалуесет** и используйте метод [**свбемнамедвалуесет. Add**](swbemnamedvalueset-add.md) , чтобы добавить значение, идентифицирующее выполняемый асинхронный вызов.</span><span class="sxs-lookup"><span data-stu-id="448fe-136">To use this parameter, create an **SWbemNamedValueSet** object and use the [**SWbemNamedValueSet.Add**](swbemnamedvalueset-add.md) method to add a value that identifies the asynchronous call you are making.</span></span> <span data-ttu-id="448fe-137">Этот объект **свбемнамедвалуесет** возвращается в приемник объекта, и источник вызова можно извлечь с помощью метода [**свбемнамедвалуесет. Item**](swbemnamedvalueset-item.md) .</span><span class="sxs-lookup"><span data-stu-id="448fe-137">This **SWbemNamedValueSet** object is returned to the object sink and the source of the call can be extracted using the [**SWbemNamedValueSet.Item**](swbemnamedvalueset-item.md) method.</span></span> <span data-ttu-id="448fe-138">Дополнительные сведения см. [в разделе вызов метода](calling-a-method.md).</span><span class="sxs-lookup"><span data-stu-id="448fe-138">For more information, see [Calling a Method](calling-a-method.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="448fe-139">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="448fe-139">Return value</span></span>

<span data-ttu-id="448fe-140">Этот метод не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="448fe-140">This method does not return a value.</span></span> <span data-ttu-id="448fe-141">В случае успешного выполнения приемник получает событие [**онобжектреади**](swbemsink-onobjectready.md) , когда объект доступен.</span><span class="sxs-lookup"><span data-stu-id="448fe-141">If successful, the sink receives an [**OnObjectReady**](swbemsink-onobjectready.md) event when the object is available.</span></span>

## <a name="error-codes"></a><span data-ttu-id="448fe-142">Коды ошибок</span><span class="sxs-lookup"><span data-stu-id="448fe-142">Error codes</span></span>

<span data-ttu-id="448fe-143">После завершения метода с методом **Async** объект [Err](/previous-versions//sbf5ze0e(v=vs.85)) может содержать один из кодов ошибок из следующего списка.</span><span class="sxs-lookup"><span data-stu-id="448fe-143">After the completion of the **GetAsync** method, the [Err](/previous-versions//sbf5ze0e(v=vs.85)) object may contain one of the error codes in the following list.</span></span>

<dl> <dt>

<span data-ttu-id="448fe-144">**вбемерракцессдениед** -2147749891 (0x80041003)</span><span class="sxs-lookup"><span data-stu-id="448fe-144">**wbemErrAccessDenied** - 2147749891 (0x80041003)</span></span>
</dt> <dd>

<span data-ttu-id="448fe-145">У текущего пользователя нет разрешения на доступ к объекту.</span><span class="sxs-lookup"><span data-stu-id="448fe-145">Current user does not have the permission to access the object.</span></span>

</dd> <dt>

<span data-ttu-id="448fe-146">**вбемеррфаилед** -2147749889 (0x80041001)</span><span class="sxs-lookup"><span data-stu-id="448fe-146">**wbemErrFailed** - 2147749889 (0x80041001)</span></span>
</dt> <dd>

<span data-ttu-id="448fe-147">Незаданная ошибка.</span><span class="sxs-lookup"><span data-stu-id="448fe-147">Unspecified error.</span></span>

</dd> <dt>

<span data-ttu-id="448fe-148">**вбемерринвалидпараметер** -2147749896 (0x80041008)</span><span class="sxs-lookup"><span data-stu-id="448fe-148">**wbemErrInvalidParameter** - 2147749896 (0x80041008)</span></span>
</dt> <dd>

<span data-ttu-id="448fe-149">Указан недопустимый параметр.</span><span class="sxs-lookup"><span data-stu-id="448fe-149">A specified parameter is not valid.</span></span>

</dd> <dt>

<span data-ttu-id="448fe-150">**вбемерринвалидобжектпас** -2147749946 (0x8004103A)</span><span class="sxs-lookup"><span data-stu-id="448fe-150">**wbemErrInvalidObjectPath** - 2147749946 (0x8004103A)</span></span>
</dt> <dd>

<span data-ttu-id="448fe-151">Указан недопустимый путь.</span><span class="sxs-lookup"><span data-stu-id="448fe-151">Specified path was not valid.</span></span>

</dd> <dt>

<span data-ttu-id="448fe-152">**вбемеррнотфаунд** -2147749890 (0x80041002)</span><span class="sxs-lookup"><span data-stu-id="448fe-152">**wbemErrNotFound** - 2147749890 (0x80041002)</span></span>
</dt> <dd>

<span data-ttu-id="448fe-153">Не удалось найти запрошенный объект.</span><span class="sxs-lookup"><span data-stu-id="448fe-153">Requested object could not be found.</span></span>

</dd> <dt>

<span data-ttu-id="448fe-154">**вбемерраутофмемори** -2147749894 (0x80041006)</span><span class="sxs-lookup"><span data-stu-id="448fe-154">**wbemErrOutOfMemory** - 2147749894 (0x80041006)</span></span>
</dt> <dd>

<span data-ttu-id="448fe-155">Недостаточно памяти для завершения операции.</span><span class="sxs-lookup"><span data-stu-id="448fe-155">Not enough memory to complete the operation.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="448fe-156">Комментарии</span><span class="sxs-lookup"><span data-stu-id="448fe-156">Remarks</span></span>

<span data-ttu-id="448fe-157">Этот вызов возвращает немедленно.</span><span class="sxs-lookup"><span data-stu-id="448fe-157">This call returns immediately.</span></span> <span data-ttu-id="448fe-158">Запрошенный объект и состояние возвращаются вызывающему через обратный вызов, доставленный в приемник, указанный в *обжвбемсинк*.</span><span class="sxs-lookup"><span data-stu-id="448fe-158">The requested object and status are returned to the caller through a callback delivered to the sink that is specified in *objWbemSink*.</span></span> <span data-ttu-id="448fe-159">Чтобы обработать объект при его возврате, создайте *обжвбемсинк*. [**Онобжектреади**](swbemsink-onobjectready.md)или *обжвбемсинк*. Подпрограммы [**Oncompleteed**](swbemsink-oncompleted.md) Event.</span><span class="sxs-lookup"><span data-stu-id="448fe-159">To process the object when it returns, create an *objWbemSink*.[**OnObjectReady**](swbemsink-onobjectready.md), or an *objWbemSink*.[**OnCompleted**](swbemsink-oncompleted.md) event subroutine.</span></span>

<span data-ttu-id="448fe-160">Асинхронный обратный вызов позволяет пользователю без проверки подлинности предоставлять данные в приемник.</span><span class="sxs-lookup"><span data-stu-id="448fe-160">An asynchronous callback allows a non-authenticated user to provide data to the sink.</span></span> <span data-ttu-id="448fe-161">Это создает угрозы безопасности для сценариев и приложений.</span><span class="sxs-lookup"><span data-stu-id="448fe-161">This poses security risks to your scripts and applications.</span></span> <span data-ttu-id="448fe-162">Чтобы устранить риски, используйте семисинчронаус или синхронный обмен данными.</span><span class="sxs-lookup"><span data-stu-id="448fe-162">To eliminate the risks, use semisynchronous or synchronous communication.</span></span> <span data-ttu-id="448fe-163">Дополнительные сведения см. [в разделе Настройка безопасности при асинхронном вызове](setting-security-on-an-asynchronous-call.md).</span><span class="sxs-lookup"><span data-stu-id="448fe-163">For more information, see [Setting Security on an Asynchronous Call](setting-security-on-an-asynchronous-call.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="448fe-164">Требования</span><span class="sxs-lookup"><span data-stu-id="448fe-164">Requirements</span></span>



| <span data-ttu-id="448fe-165">Требование</span><span class="sxs-lookup"><span data-stu-id="448fe-165">Requirement</span></span> | <span data-ttu-id="448fe-166">Значение</span><span class="sxs-lookup"><span data-stu-id="448fe-166">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="448fe-167">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="448fe-167">Minimum supported client</span></span><br/> | <span data-ttu-id="448fe-168">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="448fe-168">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="448fe-169">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="448fe-169">Minimum supported server</span></span><br/> | <span data-ttu-id="448fe-170">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="448fe-170">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="448fe-171">Header</span><span class="sxs-lookup"><span data-stu-id="448fe-171">Header</span></span><br/>                   | <dl> <span data-ttu-id="448fe-172"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="448fe-172"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="448fe-173">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="448fe-173">Type library</span></span><br/>             | <dl> <span data-ttu-id="448fe-174"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="448fe-174"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="448fe-175">DLL</span><span class="sxs-lookup"><span data-stu-id="448fe-175">DLL</span></span><br/>                      | <dl> <span data-ttu-id="448fe-176"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="448fe-176"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="448fe-177">CLSID</span><span class="sxs-lookup"><span data-stu-id="448fe-177">CLSID</span></span><br/>                    | <span data-ttu-id="448fe-178">\_SWBEMSERVICES CLSID</span><span class="sxs-lookup"><span data-stu-id="448fe-178">CLSID\_SWbemServices</span></span><br/>                                                         |
| <span data-ttu-id="448fe-179">IID</span><span class="sxs-lookup"><span data-stu-id="448fe-179">IID</span></span><br/>                      | <span data-ttu-id="448fe-180">IID \_ исвбемсервицес</span><span class="sxs-lookup"><span data-stu-id="448fe-180">IID\_ISWbemServices</span></span><br/>                                                          |



## <a name="see-also"></a><span data-ttu-id="448fe-181">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="448fe-181">See also</span></span>

<dl> <dt>

[<span data-ttu-id="448fe-182">**SWbemServices**</span><span class="sxs-lookup"><span data-stu-id="448fe-182">**SWbemServices**</span></span>](swbemservices.md)
</dt> <dt>

[<span data-ttu-id="448fe-183">**SWbemObject**</span><span class="sxs-lookup"><span data-stu-id="448fe-183">**SWbemObject**</span></span>](swbemobject.md)
</dt> </dl>

 

