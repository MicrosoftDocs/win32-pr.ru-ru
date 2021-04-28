---
description: SWbemServices.Exeметод Кмесодасинк — выполняет метод, экспортируемый поставщиком метода.
ms.assetid: 933a4c64-7538-474e-9f6f-f94da6066b46
ms.tgt_platform: multiple
title: SWbemServices.Exeметод Кмесодасинк (Wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemServices.ExecMethodAsync
- ISWbemServices.ExecMethodAsync
- ISWbemServices.ExecMethodAsync
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: fcdcd70b567a737cb8686ac841dc1ce0b55d3996
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108105592"
---
# <a name="swbemservicesexecmethodasync-method"></a><span data-ttu-id="42afd-103">SWbemServices.Exeметод Кмесодасинк</span><span class="sxs-lookup"><span data-stu-id="42afd-103">SWbemServices.ExecMethodAsync method</span></span>

<span data-ttu-id="42afd-104">Метод **ексекмесодасинк** объекта [**SwbemServices**](swbemservices.md) выполняет метод, который экспортируется поставщиком метода.</span><span class="sxs-lookup"><span data-stu-id="42afd-104">The **ExecMethodAsync** method of the [**SWbemServices**](swbemservices.md) object executes a method that is exported by a method provider.</span></span> <span data-ttu-id="42afd-105">Вызов немедленно возвращается клиенту, в то время как входящие параметры перенаправляются соответствующему поставщику, где выполняется метод.</span><span class="sxs-lookup"><span data-stu-id="42afd-105">The call immediately returns to the client while the inbound parameters are forwarded to the appropriate provider where the method executes.</span></span> <span data-ttu-id="42afd-106">Сведения и состояние возвращаются вызывающему через события, доставляемые в приемник, указанный в *обжвбемсинк*.</span><span class="sxs-lookup"><span data-stu-id="42afd-106">Information and status are returned to the caller through events delivered to the sink that is specified in *objWbemSink*.</span></span> <span data-ttu-id="42afd-107">Поставщик, а не инструментарий управления Windows (WMI) (WMI), реализует метод.</span><span class="sxs-lookup"><span data-stu-id="42afd-107">The provider, rather than Windows Management Instrumentation (WMI), implements the method.</span></span>

<span data-ttu-id="42afd-108">Метод вызывается в асинхронном режиме.</span><span class="sxs-lookup"><span data-stu-id="42afd-108">The method is called in the asynchronous mode.</span></span> <span data-ttu-id="42afd-109">Дополнительные сведения см. [в разделе вызов метода](calling-a-method.md).</span><span class="sxs-lookup"><span data-stu-id="42afd-109">For more information, see [Calling a Method](calling-a-method.md).</span></span>

<span data-ttu-id="42afd-110">Дополнительные сведения и описание этого синтаксиса см. в разделе [соглашения о документе для API скриптов](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="42afd-110">For more information and an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="42afd-111">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="42afd-111">Syntax</span></span>


```VB
SWbemServices.ExecMethodAsync( _
  ByVal objWbemSink, _
  ByVal strObjectPath, _
  ByVal strMethodName, _
  [ ByVal objWbemInParams ], _
  [ ByVal iFlags ], _
  [ ByVal objWbemNamedValueSet ], _
  [ ByVal objWbemAsyncContext ] _
)
```



## <a name="parameters"></a><span data-ttu-id="42afd-112">Параметры</span><span class="sxs-lookup"><span data-stu-id="42afd-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="42afd-113">*обжвбемсинк*</span><span class="sxs-lookup"><span data-stu-id="42afd-113">*objWbemSink*</span></span> 
</dt> <dd>

<span data-ttu-id="42afd-114">Обязательный элемент.</span><span class="sxs-lookup"><span data-stu-id="42afd-114">Required.</span></span> <span data-ttu-id="42afd-115">Создайте объект [**свбемсинк**](swbemsink.md) для получения объектов.</span><span class="sxs-lookup"><span data-stu-id="42afd-115">Create an [**SWbemSink**](swbemsink.md) object to receive the objects.</span></span> <span data-ttu-id="42afd-116">Приемник объекта, который получает результат вызова метода.</span><span class="sxs-lookup"><span data-stu-id="42afd-116">Object sink that receives the result of the method call.</span></span> <span data-ttu-id="42afd-117">Параметры исходящего трафика отправляются в событие [**свбемсинк. онобжектреади**](swbemsink-onobjectready.md) заданного приемника объекта.</span><span class="sxs-lookup"><span data-stu-id="42afd-117">The outbound parameters are sent to the [**SWbemSink.OnObjectReady**](swbemsink-onobjectready.md) event of the supplied object sink.</span></span> <span data-ttu-id="42afd-118">Результаты механизма вызова отправляются в событие [**свбемсинк. OnComplete**](swbemsink-oncompleted.md) в переданном приемнике объекта.</span><span class="sxs-lookup"><span data-stu-id="42afd-118">The results of the call mechanism are sent to the [**SWbemSink.OnCompleted**](swbemsink-oncompleted.md) event of the supplied object sink.</span></span> <span data-ttu-id="42afd-119">Имейте в виду, что **свбемсинк. OnComplete** не получает код возврата метода WMI.</span><span class="sxs-lookup"><span data-stu-id="42afd-119">Be aware that **SWbemSink.OnCompleted** does not receive the return code of the WMI method.</span></span> <span data-ttu-id="42afd-120">Однако он получает код возврата фактического механизма возврата вызовов, и его удобно использовать только для проверки того, что вызов произошел, или что его не удалось выполнить по механическим причинам.</span><span class="sxs-lookup"><span data-stu-id="42afd-120">However, it receives the return code of the actual call-return mechanism, and is only useful for verifying that the call occurred or that it failed for mechanical reasons.</span></span> <span data-ttu-id="42afd-121">Код результата, возвращаемый из метода WMI, возвращается в объекте исходящего параметра, переданном в **свбемсинк. онобжектреади**.</span><span class="sxs-lookup"><span data-stu-id="42afd-121">The result code that is returned from the WMI method is returned in the outbound parameter object supplied to **SWbemSink.OnObjectReady**.</span></span> <span data-ttu-id="42afd-122">Если возвращается любой код ошибки, указанный объект [**ивбемобжектсинк**](iwbemobjectsink.md) не используется.</span><span class="sxs-lookup"><span data-stu-id="42afd-122">If any error code is returned, then the supplied [**IWbemObjectSink**](iwbemobjectsink.md) object is not used.</span></span> <span data-ttu-id="42afd-123">Если вызов выполнен успешно, то для указания результата операции вызывается реализация **ивбемобжектсинк** пользователя.</span><span class="sxs-lookup"><span data-stu-id="42afd-123">If the call is successful, then the user's **IWbemObjectSink** implementation is called to indicate the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="42afd-124">*стробжектпас*</span><span class="sxs-lookup"><span data-stu-id="42afd-124">*strObjectPath*</span></span> 
</dt> <dd>

<span data-ttu-id="42afd-125">Обязательный элемент.</span><span class="sxs-lookup"><span data-stu-id="42afd-125">Required.</span></span> <span data-ttu-id="42afd-126">Строка, содержащая путь к объекту, для которого выполняется метод.</span><span class="sxs-lookup"><span data-stu-id="42afd-126">A string that contains the object path of the object for which the method is executed.</span></span> <span data-ttu-id="42afd-127">Дополнительные сведения см. [в разделе Описание расположения объекта WMI](describing-the-location-of-a-wmi-object.md).</span><span class="sxs-lookup"><span data-stu-id="42afd-127">For more information, see [Describing the Location of a WMI Object](describing-the-location-of-a-wmi-object.md).</span></span>

</dd> <dt>

<span data-ttu-id="42afd-128">*стрмесоднаме*</span><span class="sxs-lookup"><span data-stu-id="42afd-128">*strMethodName*</span></span> 
</dt> <dd>

<span data-ttu-id="42afd-129">Обязательный элемент.</span><span class="sxs-lookup"><span data-stu-id="42afd-129">Required.</span></span> <span data-ttu-id="42afd-130">Имя метода, который необходимо выполнить.</span><span class="sxs-lookup"><span data-stu-id="42afd-130">The name of the method to execute.</span></span>

</dd> <dt>

<span data-ttu-id="42afd-131">*обжвбеминпарамс* \[ используемых\]</span><span class="sxs-lookup"><span data-stu-id="42afd-131">*objWbemInParams* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="42afd-132">Объект [**SWbemObject**](swbemobject.md) , содержащий входные параметры для выполняемого метода.</span><span class="sxs-lookup"><span data-stu-id="42afd-132">An [**SWbemObject**](swbemobject.md) object that contains the input parameters for the method that is executed.</span></span> <span data-ttu-id="42afd-133">По умолчанию этот параметр не определен.</span><span class="sxs-lookup"><span data-stu-id="42afd-133">By default, this parameter is undefined.</span></span> <span data-ttu-id="42afd-134">Дополнительные сведения см. в разделе [Построение объектов параметров и анализ объектов параметров](constructing-inparameters-objects-and-parsing-outparameters-objects.md).</span><span class="sxs-lookup"><span data-stu-id="42afd-134">For more information, see [Constructing InParameters Objects and Parsing OutParameters Objects](constructing-inparameters-objects-and-parsing-outparameters-objects.md).</span></span>

</dd> <dt>

<span data-ttu-id="42afd-135">*ифлагс* \[ используемых\]</span><span class="sxs-lookup"><span data-stu-id="42afd-135">*iFlags* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="42afd-136">Целое число, определяющее поведение вызова.</span><span class="sxs-lookup"><span data-stu-id="42afd-136">Integer that determines the behavior of the call.</span></span> <span data-ttu-id="42afd-137">Этот параметр может принимать следующие значения.</span><span class="sxs-lookup"><span data-stu-id="42afd-137">This parameter can accept the following values.</span></span>

<dt>

<span id="wbemFlagSendStatus"></span><span id="wbemflagsendstatus"></span><span id="WBEMFLAGSENDSTATUS"></span>

<span data-ttu-id="42afd-138"><span id="wbemFlagSendStatus"></span><span id="wbemflagsendstatus"></span><span id="WBEMFLAGSENDSTATUS"></span>Вбемфлагсендстатус \* \* \* \* (128 (0x80))</span><span class="sxs-lookup"><span data-stu-id="42afd-138"><span id="wbemFlagSendStatus"></span><span id="wbemflagsendstatus"></span><span id="WBEMFLAGSENDSTATUS"></span>\*\*\*\*wbemFlagSendStatus\*\*\*\* (128 (0x80))</span></span>


</dt> <dd>

<span data-ttu-id="42afd-139">Вызывает асинхронные вызовы для отправки обновлений состояния обработчику событий [**OnProgress**](swbemsink-onprogress.md) для приемника объекта.</span><span class="sxs-lookup"><span data-stu-id="42afd-139">Causes asynchronous calls to send status updates to the [**OnProgress**](swbemsink-onprogress.md) event handler for the object sink.</span></span>

</dd> <dt>

<span id="wbemFlagDontSendStatus"></span><span id="wbemflagdontsendstatus"></span><span id="WBEMFLAGDONTSENDSTATUS"></span>

<span data-ttu-id="42afd-140"><span id="wbemFlagDontSendStatus"></span><span id="wbemflagdontsendstatus"></span><span id="WBEMFLAGDONTSENDSTATUS"></span>Вбемфлагдонтсендстатус \* \* \* \* (0 (0x0))</span><span class="sxs-lookup"><span data-stu-id="42afd-140"><span id="wbemFlagDontSendStatus"></span><span id="wbemflagdontsendstatus"></span><span id="WBEMFLAGDONTSENDSTATUS"></span>\*\*\*\*wbemFlagDontSendStatus\*\*\*\* (0 (0x0))</span></span>


</dt> <dd>

<span data-ttu-id="42afd-141">Не позволяет асинхронным вызовам отправлять обновления состояния в обработчик событий [**OnProgress**](swbemsink-onprogress.md) для приемника объекта.</span><span class="sxs-lookup"><span data-stu-id="42afd-141">Prevents asynchronous calls from sending status updates to the [**OnProgress**](swbemsink-onprogress.md) event handler for the object sink.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="42afd-142">*обжвбемнамедвалуесет* \[ используемых\]</span><span class="sxs-lookup"><span data-stu-id="42afd-142">*objWbemNamedValueSet* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="42afd-143">Как правило, это не определено.</span><span class="sxs-lookup"><span data-stu-id="42afd-143">Typically, this is undefined.</span></span> <span data-ttu-id="42afd-144">В противном случае это объект [**свбемнамедвалуесет**](swbemnamedvalueset.md) , элементы которого представляют сведения о контексте, которые могут использоваться поставщиком, обслуживающим запрос.</span><span class="sxs-lookup"><span data-stu-id="42afd-144">Otherwise, this is an [**SWbemNamedValueSet**](swbemnamedvalueset.md) object whose elements represent the context information that can be used by the provider that is servicing the request.</span></span> <span data-ttu-id="42afd-145">Поставщик, который поддерживает или требует такую информацию, должен документировать распознанные имена значений, тип данных значения, допустимые значения и семантику.</span><span class="sxs-lookup"><span data-stu-id="42afd-145">A provider that supports or requires such information must document the recognized value names, data type of the value, allowed values, and semantics.</span></span>

</dd> <dt>

<span data-ttu-id="42afd-146">*обжвбемасинкконтекст* \[ используемых\]</span><span class="sxs-lookup"><span data-stu-id="42afd-146">*objWbemAsyncContext* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="42afd-147">Объект [**свбемнамедвалуесет**](swbemnamedvalueset.md) , возвращающий приемник объекта для обнаружения источника исходного асинхронного вызова.</span><span class="sxs-lookup"><span data-stu-id="42afd-147">A [**SWbemNamedValueSet**](swbemnamedvalueset.md) object that returns to the object sink to identify the source of the original asynchronous call.</span></span> <span data-ttu-id="42afd-148">Используйте этот параметр, если вы выполняете несколько асинхронных вызовов, использующих один и тот же приемник объекта.</span><span class="sxs-lookup"><span data-stu-id="42afd-148">Use this parameter if you are making multiple asynchronous calls using the same object sink.</span></span> <span data-ttu-id="42afd-149">Чтобы использовать этот параметр, создайте объект **свбемнамедвалуесет** и используйте метод [**свбемнамедвалуесет. Add**](swbemnamedvalueset-add.md) , чтобы добавить значение, идентифицирующее выполняемый асинхронный вызов.</span><span class="sxs-lookup"><span data-stu-id="42afd-149">To use this parameter, create an **SWbemNamedValueSet** object and use the [**SWbemNamedValueSet.Add**](swbemnamedvalueset-add.md) method to add a value that identifies the asynchronous call you are making.</span></span> <span data-ttu-id="42afd-150">Этот объект **свбемнамедвалуесет** возвращается в приемник объекта, и источник вызова можно извлечь с помощью метода [**свбемнамедвалуесет. Item**](swbemnamedvalueset-item.md) .</span><span class="sxs-lookup"><span data-stu-id="42afd-150">This **SWbemNamedValueSet** object is returned to the object sink and the source of the call can be extracted using the [**SWbemNamedValueSet.Item**](swbemnamedvalueset-item.md) method.</span></span> <span data-ttu-id="42afd-151">Дополнительные сведения см. в разделе [выполнение асинхронного вызова с помощью VBScript](making-an-asynchronous-call-with-vbscript.md).</span><span class="sxs-lookup"><span data-stu-id="42afd-151">For more information, see [Making an Asynchronous Call with VBScript](making-an-asynchronous-call-with-vbscript.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="42afd-152">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="42afd-152">Return value</span></span>

<span data-ttu-id="42afd-153">Этот метод не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="42afd-153">This method does not return a value.</span></span> <span data-ttu-id="42afd-154">Если вызов выполнен успешно, объект [**параметров**](swbemmethod-outparameters.md) , который также является [**SWbemObject**](swbemobject.md) , предоставляется приемнику, указанному в *обжвбемсинк*.</span><span class="sxs-lookup"><span data-stu-id="42afd-154">If the call is successful, an [**OutParameters**](swbemmethod-outparameters.md) object, which is also an [**SWbemObject**](swbemobject.md) is supplied to the sink that is specified in *objWbemSink*.</span></span> <span data-ttu-id="42afd-155">Возвращаемый объект **параметров** содержит выходные параметры и возвращаемое значение для выполняемого метода.</span><span class="sxs-lookup"><span data-stu-id="42afd-155">The returned **OutParameters** object contains the output parameters and return value for the method being executed.</span></span> <span data-ttu-id="42afd-156">Дополнительные сведения см. в разделе [Построение объектов параметров и анализ объектов параметров](constructing-inparameters-objects-and-parsing-outparameters-objects.md).</span><span class="sxs-lookup"><span data-stu-id="42afd-156">For more information, see [Constructing InParameters Objects and Parsing OutParameters Objects](constructing-inparameters-objects-and-parsing-outparameters-objects.md).</span></span>

## <a name="error-codes"></a><span data-ttu-id="42afd-157">Коды ошибок</span><span class="sxs-lookup"><span data-stu-id="42afd-157">Error codes</span></span>

<span data-ttu-id="42afd-158">После завершения метода **ексекмесодасинк** объект [Err](/previous-versions//sbf5ze0e(v=vs.85)) может содержать один из кодов ошибок, перечисленных в следующем списке.</span><span class="sxs-lookup"><span data-stu-id="42afd-158">After the completion of the **ExecMethodAsync** method, the [Err](/previous-versions//sbf5ze0e(v=vs.85)) object may contain one of the error codes listed in the following list.</span></span>

<dl> <dt>

<span data-ttu-id="42afd-159">**вбемеррфаилед** -2147749889 (0x80041001)</span><span class="sxs-lookup"><span data-stu-id="42afd-159">**wbemErrFailed** - 2147749889 (0x80041001)</span></span>
</dt> <dd>

<span data-ttu-id="42afd-160">Незаданная ошибка.</span><span class="sxs-lookup"><span data-stu-id="42afd-160">Unspecified error.</span></span>

</dd> <dt>

<span data-ttu-id="42afd-161">**вбемерринвалидкласс** -2147749904 (0x80041010)</span><span class="sxs-lookup"><span data-stu-id="42afd-161">**wbemErrInvalidClass** - 2147749904 (0x80041010)</span></span>
</dt> <dd>

<span data-ttu-id="42afd-162">Указан недопустимый класс.</span><span class="sxs-lookup"><span data-stu-id="42afd-162">Specified class was not valid.</span></span>

</dd> <dt>

<span data-ttu-id="42afd-163">**вбемерринвалидпараметер** -2147749896 (0x80041008)</span><span class="sxs-lookup"><span data-stu-id="42afd-163">**wbemErrInvalidParameter** - 2147749896 (0x80041008)</span></span>
</dt> <dd>

<span data-ttu-id="42afd-164">Указан недопустимый параметр.</span><span class="sxs-lookup"><span data-stu-id="42afd-164">A specified parameter is not valid.</span></span>

</dd> <dt>

<span data-ttu-id="42afd-165">**вбемерраутофмемори** -2147749894 (0x80041006)</span><span class="sxs-lookup"><span data-stu-id="42afd-165">**wbemErrOutOfMemory** - 2147749894 (0x80041006)</span></span>
</dt> <dd>

<span data-ttu-id="42afd-166">Недостаточно памяти для завершения операции.</span><span class="sxs-lookup"><span data-stu-id="42afd-166">Not enough memory to complete the operation.</span></span>

</dd> <dt>

<span data-ttu-id="42afd-167">**вбемерринвалидмесод** -2147749934 (0x8004102E)</span><span class="sxs-lookup"><span data-stu-id="42afd-167">**wbemErrInvalidMethod** - 2147749934 (0x8004102E)</span></span>
</dt> <dd>

<span data-ttu-id="42afd-168">Запрошенный метод недоступен.</span><span class="sxs-lookup"><span data-stu-id="42afd-168">Requested method was not available.</span></span>

</dd> <dt>

<span data-ttu-id="42afd-169">**вбемерракцессдениед** -2147749891 (0x80041003)</span><span class="sxs-lookup"><span data-stu-id="42afd-169">**wbemErrAccessDenied** - 2147749891 (0x80041003)</span></span>
</dt> <dd>

<span data-ttu-id="42afd-170">Текущий пользователь не имеет разрешения на выполнение метода.</span><span class="sxs-lookup"><span data-stu-id="42afd-170">Current user was not authorized to execute the method.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="42afd-171">Remarks</span><span class="sxs-lookup"><span data-stu-id="42afd-171">Remarks</span></span>

<span data-ttu-id="42afd-172">Если выполняемый метод имеет входные параметры, то объект с [**параметрами**](swbemmethod-inparameters.md) в параметре *обжвбеминпарам* должен быть таким же, как и описание в разделах конструирование непараметризованных [объектов и синтаксический анализ объектов параметров](constructing-inparameters-objects-and-parsing-outparameters-objects.md) .</span><span class="sxs-lookup"><span data-stu-id="42afd-172">If the method executed has input parameters, the [**InParameters**](swbemmethod-inparameters.md) object in the *objWbemInParam* parameter must be the same as the description in the [Constructing InParameters Objects and Parsing OutParameters Objects](constructing-inparameters-objects-and-parsing-outparameters-objects.md) topics.</span></span>

<span data-ttu-id="42afd-173">Используйте **SWbemServices.Exeкмесодасинк** в качестве альтернативы для прямого доступа к [*методу поставщика*](gloss-p.md) , когда невозможно выполнить метод напрямую.</span><span class="sxs-lookup"><span data-stu-id="42afd-173">Use **SWbemServices.ExecMethodAsync** as an alternative to direct access for executing a [*provider method*](gloss-p.md) when it is not possible to execute a method directly.</span></span> <span data-ttu-id="42afd-174">Например, используйте его с языком сценариев, который не поддерживает выходные параметры, то есть если метод имеет параметры OUT.</span><span class="sxs-lookup"><span data-stu-id="42afd-174">For example, use it with a scripting language that does not support output parameters, that is, if your method has OUT parameters.</span></span> <span data-ttu-id="42afd-175">В противном случае рекомендуется использовать прямой доступ для вызова метода.</span><span class="sxs-lookup"><span data-stu-id="42afd-175">Otherwise, it is recommended that you use direct access to invoke a method.</span></span> <span data-ttu-id="42afd-176">Дополнительные сведения см. в разделе [Управление сведениями о классе и экземпляре](manipulating-class-and-instance-information.md).</span><span class="sxs-lookup"><span data-stu-id="42afd-176">For more information, see [Manipulating Class and Instance Information](manipulating-class-and-instance-information.md).</span></span>

<span data-ttu-id="42afd-177">Для метода **SWbemServices.Exeкмесодасинк** требуется путь к объекту.</span><span class="sxs-lookup"><span data-stu-id="42afd-177">The **SWbemServices.ExecMethodAsync** method requires an object path.</span></span> <span data-ttu-id="42afd-178">Если скрипт уже содержит объект [**SWbemObject**](swbemobject.md) , можно вызвать метод [**SWbemObject.Exeкмесодасинк**](swbemobject-execmethodasync-.md).</span><span class="sxs-lookup"><span data-stu-id="42afd-178">If the script already contains an [**SWbemObject**](swbemobject.md) object, you can call [**SWbemObject.ExecMethodAsync**](swbemobject-execmethodasync-.md).</span></span>

<span data-ttu-id="42afd-179">Этот вызов возвращает немедленно.</span><span class="sxs-lookup"><span data-stu-id="42afd-179">This call returns immediately.</span></span> <span data-ttu-id="42afd-180">Сведения о состоянии возвращаются вызывающему объекту через обратные вызовы, доставляемые в приемник, указанный в *обжвбемсинк*.</span><span class="sxs-lookup"><span data-stu-id="42afd-180">The status information is returned to the caller through call-backs delivered to the sink that is specified in *objWbemSink*.</span></span> <span data-ttu-id="42afd-181">Чтобы продолжить обработку после завершения вызова, реализуйте подпрограммы для *обжвбемсинк*. Событие [**Oncompleteed**](swbemsink-oncompleted.md) .</span><span class="sxs-lookup"><span data-stu-id="42afd-181">To continue processing when the call is completed, implement a subroutine for the *objWbemSink*.[**OnCompleted**](swbemsink-oncompleted.md) event.</span></span>

<span data-ttu-id="42afd-182">Асинхронный обратный вызов позволяет пользователю без проверки подлинности предоставлять данные в приемник.</span><span class="sxs-lookup"><span data-stu-id="42afd-182">An asynchronous callback allows a non-authenticated user to provide data to the sink.</span></span> <span data-ttu-id="42afd-183">Это создает угрозы безопасности для сценариев и приложений.</span><span class="sxs-lookup"><span data-stu-id="42afd-183">This poses security risks to your scripts and applications.</span></span> <span data-ttu-id="42afd-184">Дополнительные сведения об устранении рисков см. в разделе [Настройка безопасности при асинхронном вызове](setting-security-on-an-asynchronous-call.md).</span><span class="sxs-lookup"><span data-stu-id="42afd-184">For more information about how to eliminate the risks, see [Setting Security on an Asynchronous Call](setting-security-on-an-asynchronous-call.md).</span></span>

<span data-ttu-id="42afd-185">Используйте параметр *обжвбемасинкконтекст* для проверки источника вызова.</span><span class="sxs-lookup"><span data-stu-id="42afd-185">Use the *objWbemAsyncContext* parameter to verify the source of a call.</span></span>

## <a name="examples"></a><span data-ttu-id="42afd-186">Примеры</span><span class="sxs-lookup"><span data-stu-id="42afd-186">Examples</span></span>

<span data-ttu-id="42afd-187">В следующем примере кода показан метод **ексекмесодасинк** .</span><span class="sxs-lookup"><span data-stu-id="42afd-187">The following code example shows the **ExecMethodAsync** method.</span></span> <span data-ttu-id="42afd-188">Скрипт создает объект [**\_ процесса Win32**](/windows/desktop/CIMWin32Prov/win32-process) , который представляет процесс, выполняющий программу «Блокнот».</span><span class="sxs-lookup"><span data-stu-id="42afd-188">The script creates a [**Win32\_Process**](/windows/desktop/CIMWin32Prov/win32-process) object that represents a process that is running Notepad.</span></span> <span data-ttu-id="42afd-189">Он показывает [**настройку объекта параметров**](swbemmethod-inparameters.md) и способ получения результатов из объекта [**параметров**](swbemmethod-outparameters.md) .</span><span class="sxs-lookup"><span data-stu-id="42afd-189">It shows the setting up of an [**InParameters**](swbemmethod-inparameters.md) object and how to obtain results from an [**OutParameters**](swbemmethod-outparameters.md) object.</span></span> <span data-ttu-id="42afd-190">Сведения о скрипте, который показывает те же операции, выполняемые синхронно, см. в разделе [**SWbemServices.Exeкмесод**](swbemservices-execmethod.md).</span><span class="sxs-lookup"><span data-stu-id="42afd-190">For a script that shows the same operations performed synchronously, see [**SWbemServices.ExecMethod**](swbemservices-execmethod.md).</span></span> <span data-ttu-id="42afd-191">Пример использования прямого доступа см. [в разделе Создание метода в классе Win32 \_ процесс](/windows/desktop/CIMWin32Prov/create-method-in-class-win32-process).</span><span class="sxs-lookup"><span data-stu-id="42afd-191">For an example of using direct access, see [Create Method in Class Win32\_Process](/windows/desktop/CIMWin32Prov/create-method-in-class-win32-process).</span></span> <span data-ttu-id="42afd-192">Пример той же операции с помощью [**SWbemObject**](swbemobject.md)см. в разделе [**SWbemObject.Exeкмесодасинк**](swbemobject-execmethodasync-.md).</span><span class="sxs-lookup"><span data-stu-id="42afd-192">For an example of the same operation using [**SWbemObject**](swbemobject.md), see [**SWbemObject.ExecMethodAsync**](swbemobject-execmethodasync-.md).</span></span>


```VB
' Connect to WMI.
set Services = getobject("winmgmts:root\cimv2")

' Obtain the class definition object
' of a Win32_Process object.
Set oProcess = Services.Get("Win32_Process")

' Create the SWbemMethod.InParameters object
' to hold the input parameter required
' for the Win32_Process.Create method call.
' The oProcess.Methods_("Create") call
' obtains a class object that defines
' the correct input parameters
' for the Win32_Process.Create call.
' The InParameters object is an 
' SWbemObject object, so SWbemObject.SpawnInstance_ 
' can be called to create it.

Set oInParams = oProcess.Methods_("Create"). _
    InParameters.SpawnInstance_
oInParams.CommandLine = "Notepad.exe"

' Create sink to receive event resulting
' from the ExecMethodAsync call.
set Sink = wscript.CreateObject( _
    "WbemScripting.SWbemSink","Sink_")

' Call SWbemServices.ExecMethodAsync
' with the WMI path Win32_Process.

bDone = false
Services.ExecMethodAsync Sink, _
     "Win32_Process", "Create", oInParams

' Call the Win32_Process.Create method asynchronously.
' Set up a wait so the results of the method
' execution can be returned to 
' the sink subroutines.

while not bDone    
    wscript.sleep 1000  
wend

' Sink subroutines
sub Sink_OnObjectReady(oOutParams, oContext)
    wscript.echo "Sink_OnObjectReady subroutine " _ 
        &VBCR & "ReturnValue = " _
        & oOutParams.ReturnValue &VBCR & _
        "ProcessId = " & oOutParams.ProcessId
end sub

sub Sink_OnCompleted(HResult, LastErrorObj, oContext)
    wscript.echo "Sink_OnCompleted subroutine, hresult = " _
        & hex(HResult)
    bdone = true
end sub
```



## <a name="requirements"></a><span data-ttu-id="42afd-193">Требования</span><span class="sxs-lookup"><span data-stu-id="42afd-193">Requirements</span></span>



| <span data-ttu-id="42afd-194">Требование</span><span class="sxs-lookup"><span data-stu-id="42afd-194">Requirement</span></span> | <span data-ttu-id="42afd-195">Значение</span><span class="sxs-lookup"><span data-stu-id="42afd-195">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="42afd-196">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="42afd-196">Minimum supported client</span></span><br/> | <span data-ttu-id="42afd-197">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="42afd-197">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="42afd-198">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="42afd-198">Minimum supported server</span></span><br/> | <span data-ttu-id="42afd-199">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="42afd-199">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="42afd-200">Header</span><span class="sxs-lookup"><span data-stu-id="42afd-200">Header</span></span><br/>                   | <dl> <span data-ttu-id="42afd-201"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="42afd-201"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="42afd-202">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="42afd-202">Type library</span></span><br/>             | <dl> <span data-ttu-id="42afd-203"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="42afd-203"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="42afd-204">DLL</span><span class="sxs-lookup"><span data-stu-id="42afd-204">DLL</span></span><br/>                      | <dl> <span data-ttu-id="42afd-205"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="42afd-205"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="42afd-206">CLSID</span><span class="sxs-lookup"><span data-stu-id="42afd-206">CLSID</span></span><br/>                    | <span data-ttu-id="42afd-207">\_SWBEMSERVICES CLSID</span><span class="sxs-lookup"><span data-stu-id="42afd-207">CLSID\_SWbemServices</span></span><br/>                                                         |
| <span data-ttu-id="42afd-208">IID</span><span class="sxs-lookup"><span data-stu-id="42afd-208">IID</span></span><br/>                      | <span data-ttu-id="42afd-209">IID \_ исвбемсервицес</span><span class="sxs-lookup"><span data-stu-id="42afd-209">IID\_ISWbemServices</span></span><br/>                                                          |



## <a name="see-also"></a><span data-ttu-id="42afd-210">См. также</span><span class="sxs-lookup"><span data-stu-id="42afd-210">See also</span></span>

<dl> <dt>

[<span data-ttu-id="42afd-211">**SWbemServices**</span><span class="sxs-lookup"><span data-stu-id="42afd-211">**SWbemServices**</span></span>](swbemservices.md)
</dt> <dt>

[<span data-ttu-id="42afd-212">**SWbemObject.ExeКмесод\_**</span><span class="sxs-lookup"><span data-stu-id="42afd-212">**SWbemObject.ExecMethod\_**</span></span>](swbemobject-execmethod-.md)
</dt> <dt>

[<span data-ttu-id="42afd-213">**SWbemObject.ExeКмесодасинк\_**</span><span class="sxs-lookup"><span data-stu-id="42afd-213">**SWbemObject.ExecMethodAsync\_**</span></span>](swbemobject-execmethodasync-.md)
</dt> <dt>

[<span data-ttu-id="42afd-214">**SWbemServices.ExeКмесод**</span><span class="sxs-lookup"><span data-stu-id="42afd-214">**SWbemServices.ExecMethod**</span></span>](swbemservices-execmethod.md)
</dt> <dt>

[<span data-ttu-id="42afd-215">Вызов метода поставщика</span><span class="sxs-lookup"><span data-stu-id="42afd-215">Calling a Provider Method</span></span>](calling-a-provider-method.md)
</dt> <dt>

[<span data-ttu-id="42afd-216">Управление сведениями о классе и экземпляре</span><span class="sxs-lookup"><span data-stu-id="42afd-216">Manipulating Class and Instance Information</span></span>](manipulating-class-and-instance-information.md)
</dt> </dl>

 

