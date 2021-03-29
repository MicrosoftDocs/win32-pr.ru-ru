---
description: Извлекает экземпляры указанного класса в соответствии с заданным пользователем критерием.
ms.assetid: 631cd749-9a39-4606-9a38-0b4bb5b4b2cd
ms.tgt_platform: multiple
title: SWbemServices. Инстанцесофасинк, метод (Wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemServices.InstancesOfAsync
- ISWbemServices.InstancesOfAsync
- ISWbemServices.InstancesOfAsync
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: c518cb38a0ecb221f4fcb0d0e7f9ce6dfc226ba9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103898526"
---
# <a name="swbemservicesinstancesofasync-method"></a><span data-ttu-id="07c75-103">SWbemServices. Инстанцесофасинк, метод</span><span class="sxs-lookup"><span data-stu-id="07c75-103">SWbemServices.InstancesOfAsync method</span></span>

<span data-ttu-id="07c75-104">Метод **инстанцесофасинк** объекта [**SwbemServices**](swbemservices.md) извлекает экземпляры указанного класса в соответствии с заданным пользователем условием.</span><span class="sxs-lookup"><span data-stu-id="07c75-104">The **InstancesOfAsync** method of the [**SWbemServices**](swbemservices.md) object retrieves instances of a specified class according to user-specified criteria.</span></span>

<span data-ttu-id="07c75-105">Метод вызывается в асинхронном режиме.</span><span class="sxs-lookup"><span data-stu-id="07c75-105">The method is called in the asynchronous mode.</span></span> <span data-ttu-id="07c75-106">Дополнительные сведения см. [в разделе вызов метода](calling-a-method.md).</span><span class="sxs-lookup"><span data-stu-id="07c75-106">For more information, see [Calling a Method](calling-a-method.md).</span></span>

<span data-ttu-id="07c75-107">Описание синтаксиса см. в разделе [соглашения о документе для API скриптов](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="07c75-107">For the syntax explanation, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="07c75-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="07c75-108">Syntax</span></span>


```VB
SWbemServices.InstancesOfAsync( _
  ByVal ObjWbemSink, _
  ByVal strClass, _
  [ ByVal iFlags ], _
  [ ByVal objWbemNamedValueSet ], _
  [ ByVal objWbemAsyncContext ] _
)
```



## <a name="parameters"></a><span data-ttu-id="07c75-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="07c75-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="07c75-110">*обжвбемсинк*</span><span class="sxs-lookup"><span data-stu-id="07c75-110">*ObjWbemSink*</span></span> 
</dt> <dd>

<span data-ttu-id="07c75-111">Приемник объекта, который асинхронно получает экземпляры.</span><span class="sxs-lookup"><span data-stu-id="07c75-111">Object sink that receives the instances asynchronously.</span></span> <span data-ttu-id="07c75-112">Создайте объект [**свбемсинк**](swbemsink.md) для получения объектов.</span><span class="sxs-lookup"><span data-stu-id="07c75-112">Create a [**SWbemSink**](swbemsink.md) object to receive the objects.</span></span>

</dd> <dt>

<span data-ttu-id="07c75-113">*стркласс*</span><span class="sxs-lookup"><span data-stu-id="07c75-113">*strClass*</span></span> 
</dt> <dd>

<span data-ttu-id="07c75-114">Обязательный.</span><span class="sxs-lookup"><span data-stu-id="07c75-114">Required.</span></span> <span data-ttu-id="07c75-115">Строка, содержащая имя класса для нужных экземпляров.</span><span class="sxs-lookup"><span data-stu-id="07c75-115">String that contains the name of the class for the instances that you want.</span></span> <span data-ttu-id="07c75-116">Этот параметр не может быть пустым.</span><span class="sxs-lookup"><span data-stu-id="07c75-116">This parameter cannot be blank.</span></span>

</dd> <dt>

<span data-ttu-id="07c75-117">*ифлагс* \[ используемых\]</span><span class="sxs-lookup"><span data-stu-id="07c75-117">*iFlags* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="07c75-118">Определяет глубину перечисления вызовов, а также указывает, будет ли вызов немедленно возвращен.</span><span class="sxs-lookup"><span data-stu-id="07c75-118">Determines the depth of the call enumeration, and whether or not the call returns immediately.</span></span> <span data-ttu-id="07c75-119">Этот параметр может принимать следующие значения.</span><span class="sxs-lookup"><span data-stu-id="07c75-119">This parameter can accept the following values.</span></span>

<dt>

<span id="wbemQueryFlagShallow"></span><span id="wbemqueryflagshallow"></span><span id="WBEMQUERYFLAGSHALLOW"></span>

<span data-ttu-id="07c75-120"><span id="wbemQueryFlagShallow"></span><span id="wbemqueryflagshallow"></span><span id="WBEMQUERYFLAGSHALLOW"></span>Вбемкуерифлагшаллов \* \* \* \* (1 (0x1))</span><span class="sxs-lookup"><span data-stu-id="07c75-120"><span id="wbemQueryFlagShallow"></span><span id="wbemqueryflagshallow"></span><span id="WBEMQUERYFLAGSHALLOW"></span>\*\*\*\*wbemQueryFlagShallow\*\*\*\* (1 (0x1))</span></span>


</dt> <dd>

<span data-ttu-id="07c75-121">Заставляет перечисление включать только непосредственные подклассы указанного родительского класса.</span><span class="sxs-lookup"><span data-stu-id="07c75-121">Forces the enumeration to include only immediate subclasses of the specified parent class.</span></span>

</dd> <dt>

<span id="wbemQueryFlagDeep"></span><span id="wbemqueryflagdeep"></span><span id="WBEMQUERYFLAGDEEP"></span>

<span data-ttu-id="07c75-122"><span id="wbemQueryFlagDeep"></span><span id="wbemqueryflagdeep"></span><span id="WBEMQUERYFLAGDEEP"></span>Вбемкуерифлагдип \* \* \* \* (0 (0x0))</span><span class="sxs-lookup"><span data-stu-id="07c75-122"><span id="wbemQueryFlagDeep"></span><span id="wbemqueryflagdeep"></span><span id="WBEMQUERYFLAGDEEP"></span>\*\*\*\*wbemQueryFlagDeep\*\*\*\* (0 (0x0))</span></span>


</dt> <dd>

<span data-ttu-id="07c75-123">Значение по умолчанию для этого параметра.</span><span class="sxs-lookup"><span data-stu-id="07c75-123">Default for this parameter.</span></span> <span data-ttu-id="07c75-124">Это значение приводит к включению в перечисление всех классов в иерархии.</span><span class="sxs-lookup"><span data-stu-id="07c75-124">This value forces the enumeration to include all classes in the hierarchy.</span></span>

</dd> <dt>

<span id="wbemFlagSendStatus"></span><span id="wbemflagsendstatus"></span><span id="WBEMFLAGSENDSTATUS"></span>

<span data-ttu-id="07c75-125"><span id="wbemFlagSendStatus"></span><span id="wbemflagsendstatus"></span><span id="WBEMFLAGSENDSTATUS"></span>Вбемфлагсендстатус \* \* \* \* (128 (0x80))</span><span class="sxs-lookup"><span data-stu-id="07c75-125"><span id="wbemFlagSendStatus"></span><span id="wbemflagsendstatus"></span><span id="WBEMFLAGSENDSTATUS"></span>\*\*\*\*wbemFlagSendStatus\*\*\*\* (128 (0x80))</span></span>


</dt> <dd>

<span data-ttu-id="07c75-126">Вызывает асинхронные вызовы для отправки обновлений состояния обработчику событий [**OnProgress**](swbemsink-onprogress.md) для приемника объекта.</span><span class="sxs-lookup"><span data-stu-id="07c75-126">Causes asynchronous calls to send status updates to the [**OnProgress**](swbemsink-onprogress.md) event handler for the object sink.</span></span>

</dd> <dt>

<span id="wbemFlagDontSendStatus"></span><span id="wbemflagdontsendstatus"></span><span id="WBEMFLAGDONTSENDSTATUS"></span>

<span data-ttu-id="07c75-127"><span id="wbemFlagDontSendStatus"></span><span id="wbemflagdontsendstatus"></span><span id="WBEMFLAGDONTSENDSTATUS"></span>Вбемфлагдонтсендстатус \* \* \* \* (0 (0x0))</span><span class="sxs-lookup"><span data-stu-id="07c75-127"><span id="wbemFlagDontSendStatus"></span><span id="wbemflagdontsendstatus"></span><span id="WBEMFLAGDONTSENDSTATUS"></span>\*\*\*\*wbemFlagDontSendStatus\*\*\*\* (0 (0x0))</span></span>


</dt> <dd>

<span data-ttu-id="07c75-128">Не позволяет асинхронным вызовам отправлять обновления состояния в обработчик событий [**OnProgress**](swbemsink-onprogress.md) для приемника объекта.</span><span class="sxs-lookup"><span data-stu-id="07c75-128">Prevents asynchronous calls from sending status updates to the [**OnProgress**](swbemsink-onprogress.md) event handler for the object sink.</span></span>

</dd> <dt>

<span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>

<span data-ttu-id="07c75-129"><span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>Вбемфлагусеамендедкуалифиерс \* \* \* \* (131072 (0x20000))</span><span class="sxs-lookup"><span data-stu-id="07c75-129"><span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>\*\*\*\*wbemFlagUseAmendedQualifiers\*\*\*\* (131072 (0x20000))</span></span>


</dt> <dd>

<span data-ttu-id="07c75-130">Заставляет WMI возвращать данные о поправности класса с определением базового класса.</span><span class="sxs-lookup"><span data-stu-id="07c75-130">Causes WMI to return class amendment data with the base class definition.</span></span> <span data-ttu-id="07c75-131">Дополнительные сведения см. в разделе [Локализация сведений о классе WMI](localizing-wmi-class-information.md).</span><span class="sxs-lookup"><span data-stu-id="07c75-131">For more information, see [Localizing WMI Class Information](localizing-wmi-class-information.md).</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="07c75-132">*обжвбемнамедвалуесет* \[ используемых\]</span><span class="sxs-lookup"><span data-stu-id="07c75-132">*objWbemNamedValueSet* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="07c75-133">Как правило, это не определено.</span><span class="sxs-lookup"><span data-stu-id="07c75-133">Typically, this is undefined.</span></span> <span data-ttu-id="07c75-134">В противном случае это объект [**свбемнамедвалуесет**](swbemnamedvalueset.md) , элементы которого представляют сведения о контексте, которые могут использоваться поставщиком, обслуживающим запрос.</span><span class="sxs-lookup"><span data-stu-id="07c75-134">Otherwise, this is an [**SWbemNamedValueSet**](swbemnamedvalueset.md) object whose elements represent the context information that can be used by the provider that is servicing the request.</span></span> <span data-ttu-id="07c75-135">Поставщик, поддерживающий или требующий сведения о контексте, должен документировать распознанные имена значений, тип данных значения, допустимые значения и семантику.</span><span class="sxs-lookup"><span data-stu-id="07c75-135">A provider that supports or requires context information information must document the recognized value names, data type of the value, allowed values, and semantics.</span></span>

</dd> <dt>

<span data-ttu-id="07c75-136">*обжвбемасинкконтекст* \[ используемых\]</span><span class="sxs-lookup"><span data-stu-id="07c75-136">*objWbemAsyncContext* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="07c75-137">Объект [**свбемнамедвалуесет**](swbemnamedvalueset.md) , возвращающий приемник объекта для обнаружения источника исходного асинхронного вызова.</span><span class="sxs-lookup"><span data-stu-id="07c75-137">An [**SWbemNamedValueSet**](swbemnamedvalueset.md) object that returns to the object sink to identify the source of the original asynchronous call.</span></span> <span data-ttu-id="07c75-138">Используйте этот параметр, если вы выполняете несколько асинхронных вызовов, использующих один и тот же приемник объекта.</span><span class="sxs-lookup"><span data-stu-id="07c75-138">Use this parameter if you are making multiple asynchronous calls using the same object sink.</span></span> <span data-ttu-id="07c75-139">Чтобы использовать этот параметр, создайте объект **свбемнамедвалуесет** и используйте метод [**свбемнамедвалуесет. Add**](swbemnamedvalueset-add.md) , чтобы добавить значение, идентифицирующее выполняемый асинхронный вызов.</span><span class="sxs-lookup"><span data-stu-id="07c75-139">To use this parameter, create an **SWbemNamedValueSet** object and use the [**SWbemNamedValueSet.Add**](swbemnamedvalueset-add.md) method to add a value that identifies the asynchronous call you are making.</span></span> <span data-ttu-id="07c75-140">Этот объект **свбемнамедвалуесет** возвращается в приемник объекта, и источник вызова можно извлечь с помощью метода [**свбемнамедвалуесет. Item**](swbemnamedvalueset-item.md) .</span><span class="sxs-lookup"><span data-stu-id="07c75-140">This **SWbemNamedValueSet** object is returned to the object sink and the source of the call can be extracted using the [**SWbemNamedValueSet.Item**](swbemnamedvalueset-item.md) method.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="07c75-141">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="07c75-141">Return value</span></span>

<span data-ttu-id="07c75-142">Этот метод не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="07c75-142">This method does not return a value.</span></span> <span data-ttu-id="07c75-143">В случае успешного выполнения приемник получает событие [**онобжектреади**](swbemsink-onobjectready.md) для каждого экземпляра.</span><span class="sxs-lookup"><span data-stu-id="07c75-143">If successful, the sink receives an [**OnObjectReady**](swbemsink-onobjectready.md) event per instance.</span></span> <span data-ttu-id="07c75-144">После последнего экземпляра приемник объекта получает событие [**Oncompleteed**](swbemsink-oncompleted.md) .</span><span class="sxs-lookup"><span data-stu-id="07c75-144">After the last instance, the object sink receives an [**OnCompleted**](swbemsink-oncompleted.md) event.</span></span>

## <a name="error-codes"></a><span data-ttu-id="07c75-145">Коды ошибок</span><span class="sxs-lookup"><span data-stu-id="07c75-145">Error codes</span></span>

<span data-ttu-id="07c75-146">После завершения метода **инстанцесофасинк** объект [Err](/previous-versions//sbf5ze0e(v=vs.85)) может содержать один из кодов ошибок из следующего списка.</span><span class="sxs-lookup"><span data-stu-id="07c75-146">Upon the completion of the **InstancesOfAsync** method, the [Err](/previous-versions//sbf5ze0e(v=vs.85)) object may contain one of the error codes in the following list.</span></span>

<dl> <dt>

<span data-ttu-id="07c75-147">**вбемерракцессдениед** -2147749891 (0x80041003)</span><span class="sxs-lookup"><span data-stu-id="07c75-147">**wbemErrAccessDenied** - 2147749891 (0x80041003)</span></span>
</dt> <dd>

<span data-ttu-id="07c75-148">У текущего пользователя нет разрешения на просмотр экземпляров указанного класса.</span><span class="sxs-lookup"><span data-stu-id="07c75-148">Current user does not have the permission to view instances of the specified class.</span></span>

</dd> <dt>

<span data-ttu-id="07c75-149">**вбемеррфаилед** -2147749889 (0x80041001)</span><span class="sxs-lookup"><span data-stu-id="07c75-149">**wbemErrFailed** - 2147749889 (0x80041001)</span></span>
</dt> <dd>

<span data-ttu-id="07c75-150">Произошла неопределенная ошибка.</span><span class="sxs-lookup"><span data-stu-id="07c75-150">Unspecified error occurred.</span></span>

</dd> <dt>

<span data-ttu-id="07c75-151">**вбемерринвалидкласс** -2147749904 (0x80041010)</span><span class="sxs-lookup"><span data-stu-id="07c75-151">**wbemErrInvalidClass** - 2147749904 (0x80041010)</span></span>
</dt> <dd>

<span data-ttu-id="07c75-152">Указан недопустимый класс.</span><span class="sxs-lookup"><span data-stu-id="07c75-152">Specified class is not valid.</span></span>

</dd> <dt>

<span data-ttu-id="07c75-153">**вбемерринвалидпараметер** -2147749896 (0x80041008)</span><span class="sxs-lookup"><span data-stu-id="07c75-153">**wbemErrInvalidParameter** - 2147749896 (0x80041008)</span></span>
</dt> <dd>

<span data-ttu-id="07c75-154">Указан недопустимый параметр.</span><span class="sxs-lookup"><span data-stu-id="07c75-154">A specified parameter is not valid.</span></span>

</dd> <dt>

<span data-ttu-id="07c75-155">**вбемерраутофмемори** -2147749894 (0x80041006)</span><span class="sxs-lookup"><span data-stu-id="07c75-155">**wbemErrOutOfMemory** - 2147749894 (0x80041006)</span></span>
</dt> <dd>

<span data-ttu-id="07c75-156">Недостаточно памяти для завершения операции.</span><span class="sxs-lookup"><span data-stu-id="07c75-156">Not enough memory to complete the operation.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="07c75-157">Комментарии</span><span class="sxs-lookup"><span data-stu-id="07c75-157">Remarks</span></span>

<span data-ttu-id="07c75-158">Этот вызов возвращает немедленно.</span><span class="sxs-lookup"><span data-stu-id="07c75-158">This call returns immediately.</span></span> <span data-ttu-id="07c75-159">Запрошенные объекты и состояние возвращаются вызывающему объекту через обратные вызовы, доставляемые в приемник, указанный в *обжвбемсинк*.</span><span class="sxs-lookup"><span data-stu-id="07c75-159">The requested objects and status are returned to the caller through callbacks delivered to the sink that is specified in *objWbemSink*.</span></span> <span data-ttu-id="07c75-160">Чтобы обработать каждый объект при его возврате, создайте *обжвбемсинк*. Подпрограммы события [**онобжектреади**](swbemsink-onobjectready.md) .</span><span class="sxs-lookup"><span data-stu-id="07c75-160">To process each object when it returns, create an *objWbemSink*.[**OnObjectReady**](swbemsink-onobjectready.md) event subroutine.</span></span> <span data-ttu-id="07c75-161">После возврата всех объектов можно выполнить окончательную обработку в реализации *обжвбемсинк*. Событие [**Oncompleteed**](swbemsink-oncompleted.md) .</span><span class="sxs-lookup"><span data-stu-id="07c75-161">After all the objects are returned, you can perform the final processing in your implementation of the *objWbemSink*.[**OnCompleted**](swbemsink-oncompleted.md) event.</span></span>

<span data-ttu-id="07c75-162">Асинхронный обратный вызов позволяет пользователю без проверки подлинности предоставлять данные в приемник.</span><span class="sxs-lookup"><span data-stu-id="07c75-162">An asynchronous callback allows a non-authenticated user to provide data to the sink.</span></span> <span data-ttu-id="07c75-163">Это создает угрозы безопасности для сценариев и приложений.</span><span class="sxs-lookup"><span data-stu-id="07c75-163">This poses security risks to your scripts and applications.</span></span> <span data-ttu-id="07c75-164">Сведения об устранении рисков см. в разделе [Настройка безопасности при асинхронном вызове](setting-security-on-an-asynchronous-call.md) .</span><span class="sxs-lookup"><span data-stu-id="07c75-164">To eliminate the risks, see [Setting Security on an Asynchronous Call](setting-security-on-an-asynchronous-call.md)</span></span>

<span data-ttu-id="07c75-165">Метод **инстанцесофасинк** работает только для объектов класса.</span><span class="sxs-lookup"><span data-stu-id="07c75-165">The **InstancesOfAsync** method only works for class objects.</span></span> <span data-ttu-id="07c75-166">Не является ошибкой, когда возвращаемый перечислитель не имеет нулевых (0) элементов.</span><span class="sxs-lookup"><span data-stu-id="07c75-166">It is not an error for the returned enumerator to have zero (0) elements.</span></span>

## <a name="requirements"></a><span data-ttu-id="07c75-167">Требования</span><span class="sxs-lookup"><span data-stu-id="07c75-167">Requirements</span></span>



| <span data-ttu-id="07c75-168">Требование</span><span class="sxs-lookup"><span data-stu-id="07c75-168">Requirement</span></span> | <span data-ttu-id="07c75-169">Значение</span><span class="sxs-lookup"><span data-stu-id="07c75-169">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="07c75-170">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="07c75-170">Minimum supported client</span></span><br/> | <span data-ttu-id="07c75-171">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="07c75-171">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="07c75-172">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="07c75-172">Minimum supported server</span></span><br/> | <span data-ttu-id="07c75-173">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="07c75-173">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="07c75-174">Header</span><span class="sxs-lookup"><span data-stu-id="07c75-174">Header</span></span><br/>                   | <dl> <span data-ttu-id="07c75-175"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="07c75-175"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="07c75-176">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="07c75-176">Type library</span></span><br/>             | <dl> <span data-ttu-id="07c75-177"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="07c75-177"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="07c75-178">DLL</span><span class="sxs-lookup"><span data-stu-id="07c75-178">DLL</span></span><br/>                      | <dl> <span data-ttu-id="07c75-179"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="07c75-179"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="07c75-180">CLSID</span><span class="sxs-lookup"><span data-stu-id="07c75-180">CLSID</span></span><br/>                    | <span data-ttu-id="07c75-181">\_SWBEMSERVICES CLSID</span><span class="sxs-lookup"><span data-stu-id="07c75-181">CLSID\_SWbemServices</span></span><br/>                                                         |
| <span data-ttu-id="07c75-182">IID</span><span class="sxs-lookup"><span data-stu-id="07c75-182">IID</span></span><br/>                      | <span data-ttu-id="07c75-183">IID \_ исвбемсервицес</span><span class="sxs-lookup"><span data-stu-id="07c75-183">IID\_ISWbemServices</span></span><br/>                                                          |



## <a name="see-also"></a><span data-ttu-id="07c75-184">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="07c75-184">See also</span></span>

<dl> <dt>

[<span data-ttu-id="07c75-185">**SWbemServices**</span><span class="sxs-lookup"><span data-stu-id="07c75-185">**SWbemServices**</span></span>](swbemservices.md)
</dt> <dt>

[<span data-ttu-id="07c75-186">Вызов метода</span><span class="sxs-lookup"><span data-stu-id="07c75-186">Calling a Method</span></span>](calling-a-method.md)
</dt> </dl>

 

