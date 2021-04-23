---
description: Метод Ексекмесодасинк \_ метода SWbemObject асинхронно выполняет метод, который экспортирует поставщик метода.
ms.assetid: b848b38b-c0c3-49cd-b1e2-b0a440b82d61
ms.tgt_platform: multiple
title: Метод SWbemObject.ExecMethodAsync_ (Wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemObject.ExecMethodAsync_
- ISWbemObject.ExecMethodAsync_
- ISWbemObject.ExecMethodAsync_
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 8af1b7c10eed427423afea8b40a1df5bc237f99e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104272433"
---
# <a name="swbemobjectexecmethodasync_-method"></a><span data-ttu-id="eb507-103">SWbemObject.Exe\_ метод кмесодасинк</span><span class="sxs-lookup"><span data-stu-id="eb507-103">SWbemObject.ExecMethodAsync\_ method</span></span>

<span data-ttu-id="eb507-104">Метод **ексекмесодасинк \_** метода [**SWbemObject**](swbemobject.md) асинхронно выполняет метод, который экспортирует поставщик метода.</span><span class="sxs-lookup"><span data-stu-id="eb507-104">The **ExecMethodAsync\_** method of [**SWbemObject**](swbemobject.md) asynchronously executes a method that a method provider exports.</span></span> <span data-ttu-id="eb507-105">Этот метод аналогичен [**SWbemServices.Exeкмесодасинк**](swbemservices-execmethodasync.md), но работает непосредственно с объектом метода для выполнения.</span><span class="sxs-lookup"><span data-stu-id="eb507-105">This method is similar to [**SWbemServices.ExecMethodAsync**](swbemservices-execmethodasync.md), but operates directly on the object of the method to be executed.</span></span> <span data-ttu-id="eb507-106">Инструментарий управления Windows (WMI) (WMI) не реализует этот метод.</span><span class="sxs-lookup"><span data-stu-id="eb507-106">Windows Management Instrumentation (WMI) does not implement this method.</span></span> <span data-ttu-id="eb507-107">Поставщик реализует этот метод.</span><span class="sxs-lookup"><span data-stu-id="eb507-107">The provider implements this method.</span></span>

<span data-ttu-id="eb507-108">Описание этого синтаксиса см. в разделе [соглашения о документе для API скриптов](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="eb507-108">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="eb507-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="eb507-109">Syntax</span></span>


```VB
objOutParams = .ExecMethodAsync_( _
  ByVal objWbemSink, _
  ByVal strMethodName, _
  [ ByVal objwbemInParams ], _
  [ ByVal iFlags ], _
  [ ByVal objwbemNamedValueSet ], _
  [ ByVal objWbemAsyncContext ] _
)
```



## <a name="parameters"></a><span data-ttu-id="eb507-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="eb507-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="eb507-111">*обжвбемсинк* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="eb507-111">*objWbemSink* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="eb507-112">Обязательный.</span><span class="sxs-lookup"><span data-stu-id="eb507-112">Required.</span></span> <span data-ttu-id="eb507-113">Это приемник объекта, который получает результаты вызова метода.</span><span class="sxs-lookup"><span data-stu-id="eb507-113">This is the object sink that receives the results of the method call.</span></span> <span data-ttu-id="eb507-114">Параметры исходящего трафика отправляются в событие [**свбемсинк. онобжектреади**](swbemsink-onobjectready.md) заданного приемника объекта.</span><span class="sxs-lookup"><span data-stu-id="eb507-114">The outbound parameters are sent to the [**SWbemSink.OnObjectReady**](swbemsink-onobjectready.md) event of the supplied object sink.</span></span> <span data-ttu-id="eb507-115">Результаты механизма вызова отправляются в событие [**свбемсинк. OnComplete**](swbemsink-oncompleted.md) в переданном приемнике объекта.</span><span class="sxs-lookup"><span data-stu-id="eb507-115">The results of the call mechanism are sent to the [**SWbemSink.OnCompleted**](swbemsink-oncompleted.md) event of the supplied object sink.</span></span> <span data-ttu-id="eb507-116">Обратите внимание, что **свбемсинк. OnComplete** не получает код возврата метода.</span><span class="sxs-lookup"><span data-stu-id="eb507-116">Notice that **SWbemSink.OnCompleted** does not receive the return code of the method.</span></span> <span data-ttu-id="eb507-117">Однако он получает код возврата фактического механизма возврата вызовов, и его удобно использовать только для проверки того, что вызов произошел, или его сбой по механическим причинам.</span><span class="sxs-lookup"><span data-stu-id="eb507-117">However, it receives the return code of the actual call-return mechanism, and is only useful for verifying that the call occurred, or that it failed for mechanical reasons.</span></span> <span data-ttu-id="eb507-118">Код результата, возвращенный методом, возвращается в объекте исходящего параметра, переданном в **свбемсинк. онобжектреади**.</span><span class="sxs-lookup"><span data-stu-id="eb507-118">The result code returned from the method is returned in the outbound parameter object supplied to **SWbemSink.OnObjectReady**.</span></span> <span data-ttu-id="eb507-119">Если код ошибки возвращается, указанный объект [**ивбемобжектсинк**](iwbemobjectsink.md) не используется.</span><span class="sxs-lookup"><span data-stu-id="eb507-119">If any error code returns, then the supplied [**IWbemObjectSink**](iwbemobjectsink.md) object is not used.</span></span> <span data-ttu-id="eb507-120">Если вызов выполнен успешно, то для указания результата операции вызывается реализация **ивбемобжектсинк** пользователя.</span><span class="sxs-lookup"><span data-stu-id="eb507-120">If the call is successful, then the user's **IWbemObjectSink** implementation is called to indicate the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="eb507-121">*стрмесоднаме* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="eb507-121">*strMethodName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="eb507-122">Обязательный.</span><span class="sxs-lookup"><span data-stu-id="eb507-122">Required.</span></span> <span data-ttu-id="eb507-123">Это имя метода для объекта.</span><span class="sxs-lookup"><span data-stu-id="eb507-123">This is the name of the method for the object.</span></span>

</dd> <dt>

<span data-ttu-id="eb507-124">*обжвбеминпарамс* \[ в необязательное\]</span><span class="sxs-lookup"><span data-stu-id="eb507-124">*objwbemInParams* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="eb507-125">Это объект [**SWbemObject**](swbemobject.md) , содержащий входные параметры для выполняемого метода.</span><span class="sxs-lookup"><span data-stu-id="eb507-125">This is an [**SWbemObject**](swbemobject.md) object that contains the input parameters for the method being executed.</span></span> <span data-ttu-id="eb507-126">По умолчанию этот параметр не определен.</span><span class="sxs-lookup"><span data-stu-id="eb507-126">By default, this parameter is undefined.</span></span> <span data-ttu-id="eb507-127">Дополнительные сведения см. в разделе [Построение объектов параметров](constructing-inparameters-objects.md) и [анализ объектов параметров](parsing-outparameters-objects.md).</span><span class="sxs-lookup"><span data-stu-id="eb507-127">For more information, see [Constructing InParameters Objects](constructing-inparameters-objects.md) and [Parsing OutParameters Objects](parsing-outparameters-objects.md).</span></span>

</dd> <dt>

<span data-ttu-id="eb507-128">*ифлагс* \[ в необязательное\]</span><span class="sxs-lookup"><span data-stu-id="eb507-128">*iFlags* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="eb507-129">Целое число, определяющее поведение вызова.</span><span class="sxs-lookup"><span data-stu-id="eb507-129">Integer that determines the behavior of the call.</span></span> <span data-ttu-id="eb507-130">Этот параметр может принимать следующие значения.</span><span class="sxs-lookup"><span data-stu-id="eb507-130">This parameter can accept the following values.</span></span>

<dt>

<span id="wbemFlagSendStatus"></span><span id="wbemflagsendstatus"></span><span id="WBEMFLAGSENDSTATUS"></span>

<span data-ttu-id="eb507-131"><span id="wbemFlagSendStatus"></span><span id="wbemflagsendstatus"></span><span id="WBEMFLAGSENDSTATUS"></span>Вбемфлагсендстатус \* \* \* \* (128 (0x80))</span><span class="sxs-lookup"><span data-stu-id="eb507-131"><span id="wbemFlagSendStatus"></span><span id="wbemflagsendstatus"></span><span id="WBEMFLAGSENDSTATUS"></span>\*\*\*\*wbemFlagSendStatus\*\*\*\* (128 (0x80))</span></span>


</dt> <dd>

<span data-ttu-id="eb507-132">Вызывает асинхронные вызовы для отправки обновлений состояния обработчику событий [**свбемсинк. OnProgress**](swbemsink-onprogress.md) для приемника объекта.</span><span class="sxs-lookup"><span data-stu-id="eb507-132">Causes asynchronous calls to send status updates to the [**SWbemSink.OnProgress**](swbemsink-onprogress.md) event handler for the object sink.</span></span>

</dd> <dt>

<span id="wbemFlagDontSendStatus"></span><span id="wbemflagdontsendstatus"></span><span id="WBEMFLAGDONTSENDSTATUS"></span>

<span data-ttu-id="eb507-133"><span id="wbemFlagDontSendStatus"></span><span id="wbemflagdontsendstatus"></span><span id="WBEMFLAGDONTSENDSTATUS"></span>Вбемфлагдонтсендстатус \* \* \* \* (0 (0x0))</span><span class="sxs-lookup"><span data-stu-id="eb507-133"><span id="wbemFlagDontSendStatus"></span><span id="wbemflagdontsendstatus"></span><span id="WBEMFLAGDONTSENDSTATUS"></span>\*\*\*\*wbemFlagDontSendStatus\*\*\*\* (0 (0x0))</span></span>


</dt> <dd>

<span data-ttu-id="eb507-134">Не позволяет асинхронным вызовам отправлять обновления состояния в обработчик событий [**OnProgress**](swbemsink-onprogress.md) для приемника объекта.</span><span class="sxs-lookup"><span data-stu-id="eb507-134">Prevents asynchronous calls from sending status updates to the [**OnProgress**](swbemsink-onprogress.md) event handler for the object sink.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="eb507-135">*обжвбемнамедвалуесет* \[ в необязательное\]</span><span class="sxs-lookup"><span data-stu-id="eb507-135">*objwbemNamedValueSet* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="eb507-136">Как правило, он не определен.</span><span class="sxs-lookup"><span data-stu-id="eb507-136">Typically, it is undefined.</span></span> <span data-ttu-id="eb507-137">В противном случае это объект [**свбемнамедвалуесет**](swbemnamedvalueset.md) , элементы которого представляют сведения о контексте, которые могут использоваться поставщиком, обслуживающим запрос.</span><span class="sxs-lookup"><span data-stu-id="eb507-137">Otherwise, this is an [**SWbemNamedValueSet**](swbemnamedvalueset.md) object whose elements represent the context information that can be used by the provider that is servicing the request.</span></span> <span data-ttu-id="eb507-138">Поставщик, который поддерживает или требует такую информацию, должен документировать распознанные имена значений, тип данных значения, допустимые значения и семантику.</span><span class="sxs-lookup"><span data-stu-id="eb507-138">A provider that supports or requires such information must document the recognized value names, data type of the value, allowed values, and semantics.</span></span>

</dd> <dt>

<span data-ttu-id="eb507-139">*обжвбемасинкконтекст* \[ в необязательное\]</span><span class="sxs-lookup"><span data-stu-id="eb507-139">*objWbemAsyncContext* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="eb507-140">Это объект [**свбемнамедвалуесет**](swbemnamedvalueset.md) , который возвращает приемнику объекта, чтобы узнать источник исходного асинхронного вызова.</span><span class="sxs-lookup"><span data-stu-id="eb507-140">This is an [**SWbemNamedValueSet**](swbemnamedvalueset.md) object that returns to the object sink to identify the source of the original asynchronous call.</span></span> <span data-ttu-id="eb507-141">Используйте этот параметр, если вы выполняете несколько асинхронных вызовов, использующих один и тот же приемник объекта.</span><span class="sxs-lookup"><span data-stu-id="eb507-141">Use this parameter if you are making multiple asynchronous calls using the same object sink.</span></span> <span data-ttu-id="eb507-142">Чтобы использовать этот параметр, создайте объект **свбемнамедвалуесет** и используйте метод [**свбемнамедвалуесет. Add**](swbemnamedvalueset-add.md) , чтобы добавить значение, идентифицирующее выполняемый асинхронный вызов.</span><span class="sxs-lookup"><span data-stu-id="eb507-142">To use this parameter, create an **SWbemNamedValueSet** object and use the [**SWbemNamedValueSet.Add**](swbemnamedvalueset-add.md) method to add a value that identifies the asynchronous call you are making.</span></span> <span data-ttu-id="eb507-143">Этот объект **свбемнамедвалуесет** возвращается в приемник объекта, и источник вызова можно извлечь с помощью метода [**свбемнамедвалуесет. Item**](swbemnamedvalueset-item.md) .</span><span class="sxs-lookup"><span data-stu-id="eb507-143">This **SWbemNamedValueSet** object is returned to the object sink and the source of the call can be extracted using the [**SWbemNamedValueSet.Item**](swbemnamedvalueset-item.md) method.</span></span> <span data-ttu-id="eb507-144">Дополнительные сведения см. [в разделе вызов метода](calling-a-method.md).</span><span class="sxs-lookup"><span data-stu-id="eb507-144">For more information, see [Calling a Method](calling-a-method.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="eb507-145">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="eb507-145">Return value</span></span>

<span data-ttu-id="eb507-146">Этот метод не имеет возвращаемых значений.</span><span class="sxs-lookup"><span data-stu-id="eb507-146">This method has no return values.</span></span> <span data-ttu-id="eb507-147">Если вызов выполнен успешно, объект [**параметров**](swbemmethod-outparameters.md) , который также является объектом [**SWbemObject**](swbemobject.md) , предоставляется приемнику, указанному в *обжвбемсинк*.</span><span class="sxs-lookup"><span data-stu-id="eb507-147">If the call is successful, an [**OutParameters**](swbemmethod-outparameters.md) object, which is also an [**SWbemObject**](swbemobject.md) object, is supplied to the sink specified in *objWbemSink*.</span></span> <span data-ttu-id="eb507-148">Возвращаемый объект **параметров** содержит выходные параметры и возвращаемое значение для выполняемого метода.</span><span class="sxs-lookup"><span data-stu-id="eb507-148">The returned **OutParameters** object contains the output parameters and return value for the method being executed.</span></span>

## <a name="error-codes"></a><span data-ttu-id="eb507-149">Коды ошибок</span><span class="sxs-lookup"><span data-stu-id="eb507-149">Error codes</span></span>

<span data-ttu-id="eb507-150">После завершения метода **ексекмесодасинк \_** объект [Err](/previous-versions//sbf5ze0e(v=vs.85)) может содержать один из кодов ошибок из следующего списка.</span><span class="sxs-lookup"><span data-stu-id="eb507-150">After completion of the **ExecMethodAsync\_** method, the [Err](/previous-versions//sbf5ze0e(v=vs.85)) object may contain one of the error codes in the following list.</span></span>

<dl> <dt>

<span data-ttu-id="eb507-151">**вбемеррфаилед** -2147749889 (0x80041001)</span><span class="sxs-lookup"><span data-stu-id="eb507-151">**wbemErrFailed** - 2147749889 (0x80041001)</span></span>
</dt> <dd>

<span data-ttu-id="eb507-152">Незаданная ошибка.</span><span class="sxs-lookup"><span data-stu-id="eb507-152">Unspecified error.</span></span>

</dd> <dt>

<span data-ttu-id="eb507-153">**вбемерринвалидкласс** -2147749904 (0x80041010)</span><span class="sxs-lookup"><span data-stu-id="eb507-153">**wbemErrInvalidClass** - 2147749904 (0x80041010)</span></span>
</dt> <dd>

<span data-ttu-id="eb507-154">Указан недопустимый класс.</span><span class="sxs-lookup"><span data-stu-id="eb507-154">Specified class was not valid.</span></span>

</dd> <dt>

<span data-ttu-id="eb507-155">**вбемерринвалидпараметер** -2147749896 (0x80041008)</span><span class="sxs-lookup"><span data-stu-id="eb507-155">**wbemErrInvalidParameter** - 2147749896 (0x80041008)</span></span>
</dt> <dd>

<span data-ttu-id="eb507-156">Указан недопустимый параметр.</span><span class="sxs-lookup"><span data-stu-id="eb507-156">A specified parameter is not valid.</span></span>

</dd> <dt>

<span data-ttu-id="eb507-157">**вбемерраутофмемори** -2147749894 (0x80041006)</span><span class="sxs-lookup"><span data-stu-id="eb507-157">**wbemErrOutOfMemory** - 2147749894 (0x80041006)</span></span>
</dt> <dd>

<span data-ttu-id="eb507-158">Недостаточно памяти для завершения операции.</span><span class="sxs-lookup"><span data-stu-id="eb507-158">Not enough memory to complete the operation.</span></span>

</dd> <dt>

<span data-ttu-id="eb507-159">**вбемерринвалидмесод** -2147749934 (0x8004102E)</span><span class="sxs-lookup"><span data-stu-id="eb507-159">**wbemErrInvalidMethod** - 2147749934 (0x8004102E)</span></span>
</dt> <dd>

<span data-ttu-id="eb507-160">Запрошенный метод недоступен.</span><span class="sxs-lookup"><span data-stu-id="eb507-160">Requested method was not available.</span></span>

</dd> <dt>

<span data-ttu-id="eb507-161">**вбемерракцессдениед** -2147749891 (0x80041003)</span><span class="sxs-lookup"><span data-stu-id="eb507-161">**wbemErrAccessDenied** - 2147749891 (0x80041003)</span></span>
</dt> <dd>

<span data-ttu-id="eb507-162">Текущий пользователь не имеет разрешения на выполнение метода.</span><span class="sxs-lookup"><span data-stu-id="eb507-162">Current user was not authorized to execute the method.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="eb507-163">Комментарии</span><span class="sxs-lookup"><span data-stu-id="eb507-163">Remarks</span></span>

<span data-ttu-id="eb507-164">Используйте **SWbemObject.Exeметод кмесодасинк \_** в качестве альтернативы для прямого доступа к [*методу поставщика*](gloss-p.md) , когда невозможно выполнить метод напрямую.</span><span class="sxs-lookup"><span data-stu-id="eb507-164">Use the **SWbemObject.ExecMethodAsync\_** method as an alternative to direct access for executing a [*provider method*](gloss-p.md) when you cannot execute a method directly.</span></span> <span data-ttu-id="eb507-165">Например, если метод имеет выходные параметры, используйте метод **SWbemObject.Exeкмесодасинк \_** с языком сценариев, который не поддерживает выходные параметры.</span><span class="sxs-lookup"><span data-stu-id="eb507-165">For example, if your method has out parameters, use the **SWbemObject.ExecMethodAsync\_** method with a scripting language that does not support output parameters.</span></span> <span data-ttu-id="eb507-166">В противном случае рекомендуется вызывать метод с помощью прямого доступа.</span><span class="sxs-lookup"><span data-stu-id="eb507-166">Otherwise, it is recommended that you invoke a method using direct access.</span></span> <span data-ttu-id="eb507-167">Дополнительные сведения см. в разделе [Управление сведениями о классе и экземпляре](manipulating-class-and-instance-information.md).</span><span class="sxs-lookup"><span data-stu-id="eb507-167">For more information, see [Manipulating Class and Instance Information](manipulating-class-and-instance-information.md).</span></span>

<span data-ttu-id="eb507-168">Этот вызов возвращает немедленно.</span><span class="sxs-lookup"><span data-stu-id="eb507-168">This call returns immediately.</span></span> <span data-ttu-id="eb507-169">Запрошенные объекты и состояние возвращаются вызывающему объекту через обратные вызовы, доставляемые в приемник, указанный в *обжвбемсинк*.</span><span class="sxs-lookup"><span data-stu-id="eb507-169">The requested objects and status are returned to the caller through callbacks delivered to the sink that is specified in *objWbemSink*.</span></span> <span data-ttu-id="eb507-170">Чтобы обработать каждый объект при поступлении, создайте *обжвбемсинк*. Подпрограммы события [**онобжектреади**](swbemsink-onobjectready.md) .</span><span class="sxs-lookup"><span data-stu-id="eb507-170">To process each object when it arrives, create an *objWbemSink*.[**OnObjectReady**](swbemsink-onobjectready.md) event subroutine.</span></span> <span data-ttu-id="eb507-171">После возврата всех объектов можно выполнить окончательную обработку в реализации *обжвбемсинк*. Событие [**Oncompleteed**](swbemsink-oncompleted.md) .</span><span class="sxs-lookup"><span data-stu-id="eb507-171">After all the objects are returned, you can perform final processing in your implementation of the *objWbemSink*.[**OnCompleted**](swbemsink-oncompleted.md) event.</span></span>

<span data-ttu-id="eb507-172">Асинхронный обратный вызов позволяет пользователю без проверки подлинности предоставлять данные в приемник.</span><span class="sxs-lookup"><span data-stu-id="eb507-172">An asynchronous callback allows a non-authenticated user to provide data to the sink.</span></span> <span data-ttu-id="eb507-173">Это создает угрозы безопасности для сценариев и приложений.</span><span class="sxs-lookup"><span data-stu-id="eb507-173">This poses security risks to your scripts and applications.</span></span> <span data-ttu-id="eb507-174">Чтобы устранить риски, используйте либо семисинчронаус связь, либо синхронное взаимодействие.</span><span class="sxs-lookup"><span data-stu-id="eb507-174">To eliminate the risks, use either semisynchronous communication or synchronous communication.</span></span> <span data-ttu-id="eb507-175">Дополнительные сведения см. [в разделе вызов метода](calling-a-method.md).</span><span class="sxs-lookup"><span data-stu-id="eb507-175">For more information, see [Calling a Method](calling-a-method.md).</span></span>

<span data-ttu-id="eb507-176">Если выполняемый метод имеет входные параметры, необходимо создать объект [**параметров**](swbemmethod-inparameters.md) и параметр *обжвбеминпарам* , как описано в разделе [Создание объектов параметров](constructing-inparameters-objects.md) и [анализ объектов параметров](parsing-outparameters-objects.md).</span><span class="sxs-lookup"><span data-stu-id="eb507-176">If the method being executed has input parameters, the [**InParameters**](swbemmethod-inparameters.md) object and *objWbemInParam* parameter must be constructed as described in [Constructing InParameters Objects](constructing-inparameters-objects.md) and [Parsing OutParameters Objects](parsing-outparameters-objects.md).</span></span>

<span data-ttu-id="eb507-177">Метод **SWbemObject.Exeкмесодасинк \_** предполагает, что объект, представленный [**SWbemObject**](swbemobject.md) , содержит метод для выполнения.</span><span class="sxs-lookup"><span data-stu-id="eb507-177">The **SWbemObject.ExecMethodAsync\_** method assumes the object represented by [**SWbemObject**](swbemobject.md) contains the method to execute.</span></span> <span data-ttu-id="eb507-178">Для метода [**SWbemServices.Exeкмесодасинк**](swbemservices-execmethodasync.md) требуется путь к объекту.</span><span class="sxs-lookup"><span data-stu-id="eb507-178">The [**SWbemServices.ExecMethodAsync**](swbemservices-execmethodasync.md) method requires an object path.</span></span>

## <a name="examples"></a><span data-ttu-id="eb507-179">Примеры</span><span class="sxs-lookup"><span data-stu-id="eb507-179">Examples</span></span>

<span data-ttu-id="eb507-180">В следующем примере показан метод [**ексекмесодасинк**](swbemservices-execmethodasync.md) .</span><span class="sxs-lookup"><span data-stu-id="eb507-180">The following example shows the [**ExecMethodAsync**](swbemservices-execmethodasync.md) method.</span></span> <span data-ttu-id="eb507-181">Скрипт создает объект [**\_ процесса Win32**](/windows/desktop/CIMWin32Prov/win32-process) , который представляет процесс, выполняющий программу «Блокнот».</span><span class="sxs-lookup"><span data-stu-id="eb507-181">The script creates a [**Win32\_Process**](/windows/desktop/CIMWin32Prov/win32-process) object that represents a process that is running Notepad.</span></span> <span data-ttu-id="eb507-182">Он показывает, как настроить [**объект параметров**](swbemmethod-inparameters.md) и как получить результаты из объекта [**параметров**](swbemmethod-outparameters.md) .</span><span class="sxs-lookup"><span data-stu-id="eb507-182">It shows setting up of [**InParameters**](swbemmethod-inparameters.md) object, and how to obtain results from an [**OutParameters**](swbemmethod-outparameters.md) object.</span></span>

<span data-ttu-id="eb507-183">Сведения о скрипте, который показывает те же операции, выполняемые синхронно, см. в разделе [**SWbemObject.Exeкмесод**](swbemobject-execmethod-.md).</span><span class="sxs-lookup"><span data-stu-id="eb507-183">For a script that shows the same operations performed synchronously, see [**SWbemObject.ExecMethod**](swbemobject-execmethod-.md).</span></span> <span data-ttu-id="eb507-184">Пример использования прямого доступа см. в разделе [**Создание метода в классе Win32 \_ процесс**](/windows/desktop/CIMWin32Prov/create-method-in-class-win32-process).</span><span class="sxs-lookup"><span data-stu-id="eb507-184">For an example using direct access, see [**Create Method in Class Win32\_Process**](/windows/desktop/CIMWin32Prov/create-method-in-class-win32-process).</span></span> <span data-ttu-id="eb507-185">Пример той же операции с помощью объекта [**SwbemServices**](swbemservices.md) см. в разделе [**SWbemServices.Exeкмесодасинк**](swbemservices-execmethodasync.md).</span><span class="sxs-lookup"><span data-stu-id="eb507-185">For an example of the same operation using an [**SWbemServices**](swbemservices.md) object, see [**SWbemServices.ExecMethodAsync**](swbemservices-execmethodasync.md).</span></span>


```VB
On Error Resume Next

'Get a Win32_Process class description
Set oProcess = GetObject("winmgmts:Win32_Process")

' Create the SWbemMethod.InParameters object
' to hold the input parameter needed
' for the Win32_Process.Create method call.
' The oProcess.Methods_("Create") call
' obtains a class object that defines
' the correct input parameters
' for the Win32_Process.Create call.
' The InParameters object is an 
' SWbemObject object so SWbemObject.SpawnInstance_
' can be called to create it.
Set oInParams = oProcess.Methods_("Create"). _
    InParameters.SpawnInstance_

' Specify the name of the process to be run.
oInParams.CommandLine = "Notepad.exe"

' Create a sink to receive event resulting
' from the ExecMethodAsync call.
Set Sink = wscript.CreateObject( _
    "WbemScripting.SWbemSink", "Sink_")

' Call the Win32_Process.Create method asynchronously. Set up a 
' wait so the results of the method execution can be returned to 
' the sink subroutines.
bDone = false

' Call SWbemObject.ExecMethodAsync on the oProcess object.
oProcess.ExecMethodAsync_ Sink, "Create", oInParams, 0 
' 
while not bDone
    wscript.sleep 1000
wend

' Sink subroutines
sub Sink_OnObjectReady(oOutParams, oContext)
    wscript.echo "Sink_OnObjectReady subroutine " _
    & VBNewLine & "ReturnValue = " _
    & oOutParams.ReturnValue & VBNewLine & _
    "ProcessId = " & oOutParams.ProcessId
end sub

sub Sink_OnCompleted(HResult, LastErrorObj, oContext)
    wscript.echo "Sink_OnCompleted subroutine, hresult = " _
    & hex(HResult)
    bdone = true
end sub
```



## <a name="requirements"></a><span data-ttu-id="eb507-186">Требования</span><span class="sxs-lookup"><span data-stu-id="eb507-186">Requirements</span></span>



| <span data-ttu-id="eb507-187">Требование</span><span class="sxs-lookup"><span data-stu-id="eb507-187">Requirement</span></span> | <span data-ttu-id="eb507-188">Значение</span><span class="sxs-lookup"><span data-stu-id="eb507-188">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="eb507-189">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="eb507-189">Minimum supported client</span></span><br/> | <span data-ttu-id="eb507-190">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="eb507-190">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="eb507-191">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="eb507-191">Minimum supported server</span></span><br/> | <span data-ttu-id="eb507-192">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="eb507-192">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="eb507-193">Header</span><span class="sxs-lookup"><span data-stu-id="eb507-193">Header</span></span><br/>                   | <dl> <span data-ttu-id="eb507-194"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="eb507-194"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="eb507-195">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="eb507-195">Type library</span></span><br/>             | <dl> <span data-ttu-id="eb507-196"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="eb507-196"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="eb507-197">DLL</span><span class="sxs-lookup"><span data-stu-id="eb507-197">DLL</span></span><br/>                      | <dl> <span data-ttu-id="eb507-198"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="eb507-198"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="eb507-199">CLSID</span><span class="sxs-lookup"><span data-stu-id="eb507-199">CLSID</span></span><br/>                    | <span data-ttu-id="eb507-200">\_SWBEMOBJECT CLSID</span><span class="sxs-lookup"><span data-stu-id="eb507-200">CLSID\_SWbemObject</span></span><br/>                                                           |
| <span data-ttu-id="eb507-201">IID</span><span class="sxs-lookup"><span data-stu-id="eb507-201">IID</span></span><br/>                      | <span data-ttu-id="eb507-202">IID \_ исвбемобжект</span><span class="sxs-lookup"><span data-stu-id="eb507-202">IID\_ISWbemObject</span></span><br/>                                                            |



## <a name="see-also"></a><span data-ttu-id="eb507-203">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="eb507-203">See also</span></span>

<dl> <dt>

[<span data-ttu-id="eb507-204">**SWbemObject**</span><span class="sxs-lookup"><span data-stu-id="eb507-204">**SWbemObject**</span></span>](swbemobject.md)
</dt> <dt>

[<span data-ttu-id="eb507-205">**SWbemServices.ExeКмесодасинк**</span><span class="sxs-lookup"><span data-stu-id="eb507-205">**SWbemServices.ExecMethodAsync**</span></span>](swbemservices-execmethodasync.md)
</dt> </dl>

 

