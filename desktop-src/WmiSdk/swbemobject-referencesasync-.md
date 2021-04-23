---
description: Метод Референцесасинк \_ объекта SWbemObject предоставляет коллекцию всех классов ассоциации или экземпляров, ссылающихся на текущий объект. Этот метод выполняет ту же функцию, что и WQL-ссылки на запрос.
ms.assetid: 44989726-3f68-453b-b9f5-e76fb0fbb152
ms.tgt_platform: multiple
title: Метод SWbemObject.ReferencesAsync_ (Wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemObject.ReferencesAsync_
- ISWbemObject.ReferencesAsync_
- ISWbemObject.ReferencesAsync_
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: aa4b85475a0dc9f736254c8f207469a52897b7ae
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105683144"
---
# <a name="swbemobjectreferencesasync_-method"></a><span data-ttu-id="5c75a-104">SWbemObject. Референцесасинк, \_ метод</span><span class="sxs-lookup"><span data-stu-id="5c75a-104">SWbemObject.ReferencesAsync\_ method</span></span>

<span data-ttu-id="5c75a-105">Метод **референцесасинк \_** объекта [**SWbemObject**](swbemobject.md) предоставляет коллекцию всех классов ассоциации или экземпляров, ссылающихся на текущий объект.</span><span class="sxs-lookup"><span data-stu-id="5c75a-105">The **ReferencesAsync\_** method of [**SWbemObject**](swbemobject.md) supplies a collection of all association classes or instances that refer to the current object.</span></span> <span data-ttu-id="5c75a-106">Этот метод выполняет ту же функцию, что и WQL- [ссылки](references-of-statement.md) на запрос.</span><span class="sxs-lookup"><span data-stu-id="5c75a-106">This method performs the same function that the WQL [REFERENCES OF](references-of-statement.md) query performs.</span></span>

<span data-ttu-id="5c75a-107">Описание этого синтаксиса см. в разделе [соглашения о документе для API скриптов](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="5c75a-107">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="5c75a-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="5c75a-108">Syntax</span></span>


```VB
SWbemObject.ReferencesAsync_( _
  ByVal objWbemSink, _
  [ ByVal strResultClass ], _
  [ ByVal strRole ], _
  [ ByVal bClassesOnly ], _
  [ ByVal bSchemaOnly ], _
  [ ByVal strRequiredQualifier ], _
  [ ByVal iFlags ], _
  [ ByVal objwbemNamedValueSet ], _
  [ ByVal objWbemAsyncContext ] _
)
```



## <a name="parameters"></a><span data-ttu-id="5c75a-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="5c75a-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5c75a-110">*обжвбемсинк* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="5c75a-110">*objWbemSink* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5c75a-111">Обязательный.</span><span class="sxs-lookup"><span data-stu-id="5c75a-111">Required.</span></span> <span data-ttu-id="5c75a-112">Приемник объекта, который асинхронно получает объекты.</span><span class="sxs-lookup"><span data-stu-id="5c75a-112">Object sink that receives the objects asynchronously.</span></span>

</dd> <dt>

<span data-ttu-id="5c75a-113">*стрресулткласс* \[ в необязательное\]</span><span class="sxs-lookup"><span data-stu-id="5c75a-113">*strResultClass* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="5c75a-114">Строка, содержащая имя класса.</span><span class="sxs-lookup"><span data-stu-id="5c75a-114">String that contains a class name.</span></span> <span data-ttu-id="5c75a-115">Если этот параметр указан, он указывает, что возвращаемые объекты ассоциации должны принадлежать или быть производными от класса, указанного в этом параметре.</span><span class="sxs-lookup"><span data-stu-id="5c75a-115">If specified, this parameter indicates that the returned association objects must belong to or be derived from the class specified in this parameter.</span></span>

</dd> <dt>

<span data-ttu-id="5c75a-116">*strRole* \[ в необязательное\]</span><span class="sxs-lookup"><span data-stu-id="5c75a-116">*strRole* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="5c75a-117">Строка, содержащая имя свойства.</span><span class="sxs-lookup"><span data-stu-id="5c75a-117">String that contains a property name.</span></span> <span data-ttu-id="5c75a-118">Если этот параметр задан, он указывает, что возвращаемые объекты связи должны быть ограничены теми, в которых исходный объект играет определенную роль.</span><span class="sxs-lookup"><span data-stu-id="5c75a-118">If specified, this parameter indicates that the returned association objects must be limited to those in which the source object plays a specific role.</span></span> <span data-ttu-id="5c75a-119">Имя указанного свойства ссылки определяет роль ассоциации.</span><span class="sxs-lookup"><span data-stu-id="5c75a-119">The name of a specified reference property defines the role of an association.</span></span>

</dd> <dt>

<span data-ttu-id="5c75a-120">*бклассесонли* \[ в необязательное\]</span><span class="sxs-lookup"><span data-stu-id="5c75a-120">*bClassesOnly* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="5c75a-121">Логическое значение, указывающее, следует ли возвращать список имен классов, а не фактические экземпляры классов.</span><span class="sxs-lookup"><span data-stu-id="5c75a-121">Boolean value that indicates whether or not a list of class names should be returned rather than actual instances of the classes.</span></span> <span data-ttu-id="5c75a-122">Это классы, к которым принадлежат объекты взаимосвязей.</span><span class="sxs-lookup"><span data-stu-id="5c75a-122">These are the classes to which the association objects belong.</span></span> <span data-ttu-id="5c75a-123">Значение по умолчанию для этого параметра — **false**.</span><span class="sxs-lookup"><span data-stu-id="5c75a-123">The default value for this parameter is **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="5c75a-124">*бсчемаонли* \[ в необязательное\]</span><span class="sxs-lookup"><span data-stu-id="5c75a-124">*bSchemaOnly* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="5c75a-125">Логическое значение, указывающее, применяется ли запрос к схеме, а не к данным.</span><span class="sxs-lookup"><span data-stu-id="5c75a-125">Boolean value that indicates whether or not the query applies to the schema rather than the data.</span></span> <span data-ttu-id="5c75a-126">Значение по умолчанию для этого параметра — **false**.</span><span class="sxs-lookup"><span data-stu-id="5c75a-126">The default value for this parameter is **FALSE**.</span></span> <span data-ttu-id="5c75a-127">Можно задать только **значение true** , если объект, для которого вызывается этот метод, является классом.</span><span class="sxs-lookup"><span data-stu-id="5c75a-127">It can only be set to **TRUE** if the object on which this method is invoked is a class.</span></span> <span data-ttu-id="5c75a-128">Если задано **значение true**, набор возвращаемых конечных точек представляет классы, которые связаны с исходным классом в схеме.</span><span class="sxs-lookup"><span data-stu-id="5c75a-128">When set to **TRUE**, the set of returned endpoints represents classes that are suitably associated with the source class in the schema.</span></span>

</dd> <dt>

<span data-ttu-id="5c75a-129">*стррекуиредкуалифиер* \[ в необязательное\]</span><span class="sxs-lookup"><span data-stu-id="5c75a-129">*strRequiredQualifier* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="5c75a-130">Строка, содержащая имя квалификатора.</span><span class="sxs-lookup"><span data-stu-id="5c75a-130">String that contains a qualifier name.</span></span> <span data-ttu-id="5c75a-131">Если этот параметр указан, он указывает, что возвращаемые объекты связи должны включать указанный квалификатор.</span><span class="sxs-lookup"><span data-stu-id="5c75a-131">If specified, this parameter indicates that the returned association objects must include the specified qualifier.</span></span>

</dd> <dt>

<span data-ttu-id="5c75a-132">*ифлагс* \[ в необязательное\]</span><span class="sxs-lookup"><span data-stu-id="5c75a-132">*iFlags* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="5c75a-133">Целое число, указывающее дополнительные флаги для операции.</span><span class="sxs-lookup"><span data-stu-id="5c75a-133">Integer specifying additional flags to the operation.</span></span> <span data-ttu-id="5c75a-134">Этот параметр может принимать следующие значения.</span><span class="sxs-lookup"><span data-stu-id="5c75a-134">This parameter can accept the following values.</span></span>

<dt>

<span id="wbemFlagSendStatus"></span><span id="wbemflagsendstatus"></span><span id="WBEMFLAGSENDSTATUS"></span>

<span data-ttu-id="5c75a-135"><span id="wbemFlagSendStatus"></span><span id="wbemflagsendstatus"></span><span id="WBEMFLAGSENDSTATUS"></span>Вбемфлагсендстатус \* \* \* \* (128 (0x80))</span><span class="sxs-lookup"><span data-stu-id="5c75a-135"><span id="wbemFlagSendStatus"></span><span id="wbemflagsendstatus"></span><span id="WBEMFLAGSENDSTATUS"></span>\*\*\*\*wbemFlagSendStatus\*\*\*\* (128 (0x80))</span></span>


</dt> <dd>

<span data-ttu-id="5c75a-136">Вызывает асинхронные вызовы для отправки обновлений состояния обработчику событий [**свбемсинк. OnProgress**](swbemsink-onprogress.md) для приемника объекта.</span><span class="sxs-lookup"><span data-stu-id="5c75a-136">Causes asynchronous calls to send status updates to the [**SWbemSink.OnProgress**](swbemsink-onprogress.md) event handler for the object sink.</span></span>

</dd> <dt>

<span id="wbemFlagDontSendStatus"></span><span id="wbemflagdontsendstatus"></span><span id="WBEMFLAGDONTSENDSTATUS"></span>

<span data-ttu-id="5c75a-137"><span id="wbemFlagDontSendStatus"></span><span id="wbemflagdontsendstatus"></span><span id="WBEMFLAGDONTSENDSTATUS"></span>Вбемфлагдонтсендстатус \* \* \* \* (0 (0x0))</span><span class="sxs-lookup"><span data-stu-id="5c75a-137"><span id="wbemFlagDontSendStatus"></span><span id="wbemflagdontsendstatus"></span><span id="WBEMFLAGDONTSENDSTATUS"></span>\*\*\*\*wbemFlagDontSendStatus\*\*\*\* (0 (0x0))</span></span>


</dt> <dd>

<span data-ttu-id="5c75a-138">Не позволяет асинхронным вызовам отправлять обновления состояния в обработчик событий [**OnProgress**](swbemsink-onprogress.md) для приемника объекта.</span><span class="sxs-lookup"><span data-stu-id="5c75a-138">Prevents asynchronous calls from sending status updates to the [**OnProgress**](swbemsink-onprogress.md) event handler for the object sink.</span></span>

</dd> <dt>

<span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>

<span data-ttu-id="5c75a-139"><span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>Вбемфлагусеамендедкуалифиерс \* \* \* \* (131072 (0x20000))</span><span class="sxs-lookup"><span data-stu-id="5c75a-139"><span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>\*\*\*\*wbemFlagUseAmendedQualifiers\*\*\*\* (131072 (0x20000))</span></span>


</dt> <dd>

<span data-ttu-id="5c75a-140">Вызывает инструментарий управления Windows (WMI) (WMI) для возврата данных о поправности класса с определением базового класса.</span><span class="sxs-lookup"><span data-stu-id="5c75a-140">Causes Windows Management Instrumentation (WMI) to return class amendment data with the base class definition.</span></span> <span data-ttu-id="5c75a-141">Дополнительные сведения см. в разделе [Локализация сведений о классе WMI](localizing-wmi-class-information.md).</span><span class="sxs-lookup"><span data-stu-id="5c75a-141">For more information, see [Localizing WMI Class Information](localizing-wmi-class-information.md).</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="5c75a-142">*обжвбемнамедвалуесет* \[ в необязательное\]</span><span class="sxs-lookup"><span data-stu-id="5c75a-142">*objwbemNamedValueSet* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="5c75a-143">Как правило, это не определено.</span><span class="sxs-lookup"><span data-stu-id="5c75a-143">Typically, this is undefined.</span></span> <span data-ttu-id="5c75a-144">В противном случае это объект [свбемнамедвалуесет](swbemnamedvalueset.md) , элементы которого представляют сведения о контексте, которые могут использоваться поставщиком, обслуживающим запрос.</span><span class="sxs-lookup"><span data-stu-id="5c75a-144">Otherwise, this is an [SWbemNamedValueSet](swbemnamedvalueset.md) object whose elements represent the context information that can be used by the provider that is servicing the request.</span></span> <span data-ttu-id="5c75a-145">Поставщик, который поддерживает или требует такую информацию, должен документировать распознанные имена значений, тип данных значения, допустимые значения и семантику.</span><span class="sxs-lookup"><span data-stu-id="5c75a-145">A provider that supports or requires such information must document the recognized value names, data type of the value, allowed values, and semantics.</span></span>

</dd> <dt>

<span data-ttu-id="5c75a-146">*обжвбемасинкконтекст* \[ в необязательное\]</span><span class="sxs-lookup"><span data-stu-id="5c75a-146">*objWbemAsyncContext* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="5c75a-147">Это объект [свбемнамедвалуесет](swbemnamedvalueset.md) , который возвращает приемнику объекта, чтобы узнать источник исходного асинхронного вызова.</span><span class="sxs-lookup"><span data-stu-id="5c75a-147">This is an [SWbemNamedValueSet](swbemnamedvalueset.md) object that returns to the object sink to identify the source of the original asynchronous call.</span></span> <span data-ttu-id="5c75a-148">Используйте этот параметр, если вы выполняете несколько асинхронных вызовов, использующих один и тот же приемник объекта.</span><span class="sxs-lookup"><span data-stu-id="5c75a-148">Use this parameter if you are making multiple asynchronous calls using the same object sink.</span></span> <span data-ttu-id="5c75a-149">Чтобы использовать этот параметр, создайте объект Свбемнамедвалуесет и используйте метод [**свбемнамедвалуесет. Add**](swbemnamedvalueset-add.md) , чтобы добавить значение, идентифицирующее выполняемый асинхронный вызов.</span><span class="sxs-lookup"><span data-stu-id="5c75a-149">To use this parameter, create an SWbemNamedValueSet object, and use the [**SWbemNamedValueSet.Add**](swbemnamedvalueset-add.md) method to add a value that identifies the asynchronous call you are making.</span></span> <span data-ttu-id="5c75a-150">Этот объект Свбемнамедвалуесет возвращается в приемник объекта, и источник вызова можно извлечь с помощью метода [**свбемнамедвалуесет. Item**](swbemnamedvalueset-item.md) .</span><span class="sxs-lookup"><span data-stu-id="5c75a-150">This SWbemNamedValueSet object is returned to the object sink and the source of the call can be extracted using the [**SWbemNamedValueSet.Item**](swbemnamedvalueset-item.md) method.</span></span> <span data-ttu-id="5c75a-151">Дополнительные сведения см. [в разделе вызов метода](calling-a-method.md).</span><span class="sxs-lookup"><span data-stu-id="5c75a-151">For more information, see [Calling a Method](calling-a-method.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5c75a-152">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="5c75a-152">Return value</span></span>

<span data-ttu-id="5c75a-153">Этот метод не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="5c75a-153">This method does not return a value.</span></span> <span data-ttu-id="5c75a-154">В случае успешного выполнения приемник получает событие [**онобжектреади**](swbemsink-onobjectready.md) для каждого экземпляра.</span><span class="sxs-lookup"><span data-stu-id="5c75a-154">If successful, the sink receives an [**OnObjectReady**](swbemsink-onobjectready.md) event per instance.</span></span> <span data-ttu-id="5c75a-155">После последнего экземпляра приемник объекта получает событие [**Oncompleteed**](swbemsink-oncompleted.md) .</span><span class="sxs-lookup"><span data-stu-id="5c75a-155">After the last instance, the object sink receives an [**OnCompleted**](swbemsink-oncompleted.md) event.</span></span>

## <a name="error-codes"></a><span data-ttu-id="5c75a-156">Коды ошибок</span><span class="sxs-lookup"><span data-stu-id="5c75a-156">Error codes</span></span>

<span data-ttu-id="5c75a-157">После завершения метода **референцесасинк \_** объект [Err](/previous-versions//sbf5ze0e(v=vs.85)) может содержать один из кодов ошибок из следующего списка.</span><span class="sxs-lookup"><span data-stu-id="5c75a-157">After the completion of the **ReferencesAsync\_** method, the [Err](/previous-versions//sbf5ze0e(v=vs.85)) object may contain one of the error codes in the following list.</span></span>

<dl> <dt>

<span data-ttu-id="5c75a-158">**вбемерракцессдениед** -2147749891 (0x80041003)</span><span class="sxs-lookup"><span data-stu-id="5c75a-158">**wbemErrAccessDenied** - 2147749891 (0x80041003)</span></span>
</dt> <dd>

<span data-ttu-id="5c75a-159">У текущего пользователя нет разрешения на просмотр одного или нескольких классов, возвращенных вызовом.</span><span class="sxs-lookup"><span data-stu-id="5c75a-159">Current user does not have permission to view one or more of the classes returned by the call.</span></span>

</dd> <dt>

<span data-ttu-id="5c75a-160">**вбемеррфаилед** -2147749889 (0x80041001)</span><span class="sxs-lookup"><span data-stu-id="5c75a-160">**wbemErrFailed** - 2147749889 (0x80041001)</span></span>
</dt> <dd>

<span data-ttu-id="5c75a-161">Незаданная ошибка.</span><span class="sxs-lookup"><span data-stu-id="5c75a-161">Unspecified error.</span></span>

</dd> <dt>

<span data-ttu-id="5c75a-162">**вбемерринвалидпараметер** -2147749896 (0x80041008)</span><span class="sxs-lookup"><span data-stu-id="5c75a-162">**wbemErrInvalidParameter** - 2147749896 (0x80041008)</span></span>
</dt> <dd>

<span data-ttu-id="5c75a-163">Указан недопустимый параметр.</span><span class="sxs-lookup"><span data-stu-id="5c75a-163">Invalid parameter was specified.</span></span>

</dd> <dt>

<span data-ttu-id="5c75a-164">**вбемерраутофмемори** -2147749894 (0x80041006)</span><span class="sxs-lookup"><span data-stu-id="5c75a-164">**wbemErrOutOfMemory** - 2147749894 (0x80041006)</span></span>
</dt> <dd>

<span data-ttu-id="5c75a-165">Недостаточно памяти для завершения операции.</span><span class="sxs-lookup"><span data-stu-id="5c75a-165">Not enough memory to complete the operation.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="5c75a-166">Комментарии</span><span class="sxs-lookup"><span data-stu-id="5c75a-166">Remarks</span></span>

<span data-ttu-id="5c75a-167">Этот вызов возвращает немедленно.</span><span class="sxs-lookup"><span data-stu-id="5c75a-167">This call returns immediately.</span></span> <span data-ttu-id="5c75a-168">Запрошенные объекты и состояние возвращаются вызывающему объекту через обратные вызовы, доставляемые в приемник, указанный в *обжвбемсинк*.</span><span class="sxs-lookup"><span data-stu-id="5c75a-168">The requested objects and status are returned to the caller through callbacks delivered to the sink that is specified in *objWbemSink*.</span></span> <span data-ttu-id="5c75a-169">Чтобы обработать каждый объект при поступлении, создайте *обжвбемсинк*. Подпрограммы события [**онобжектреади**](swbemsink-onobjectready.md) .</span><span class="sxs-lookup"><span data-stu-id="5c75a-169">To process each object when it arrives, create an *objWbemSink*.[**OnObjectReady**](swbemsink-onobjectready.md) event subroutine.</span></span> <span data-ttu-id="5c75a-170">После возврата всех объектов можно выполнить окончательную обработку в реализации *обжвбемсинк*. Событие [**Oncompleteed**](swbemsink-oncompleted.md) .</span><span class="sxs-lookup"><span data-stu-id="5c75a-170">After all the objects are returned, you can perform final processing in your implementation of the *objWbemSink*.[**OnCompleted**](swbemsink-oncompleted.md) event.</span></span>

<span data-ttu-id="5c75a-171">Асинхронный обратный вызов позволяет пользователю без проверки подлинности предоставлять данные в приемник.</span><span class="sxs-lookup"><span data-stu-id="5c75a-171">An asynchronous callback allows a non-authenticated user to provide data to the sink.</span></span> <span data-ttu-id="5c75a-172">Это создает угрозы безопасности для сценариев и приложений.</span><span class="sxs-lookup"><span data-stu-id="5c75a-172">This poses security risks to your scripts and applications.</span></span> <span data-ttu-id="5c75a-173">Чтобы устранить риски, используйте либо семисинчронаус связь, либо синхронное взаимодействие.</span><span class="sxs-lookup"><span data-stu-id="5c75a-173">To eliminate the risks, use either semisynchronous communication or synchronous communication.</span></span> <span data-ttu-id="5c75a-174">Дополнительные сведения см. [в разделе вызов метода](calling-a-method.md).</span><span class="sxs-lookup"><span data-stu-id="5c75a-174">For more information, see [Calling a Method](calling-a-method.md).</span></span>

<span data-ttu-id="5c75a-175">Дополнительные сведения о ССЫЛКАх на связанный WQL-запрос, исходные экземпляры и объекты связи см. в разделе [соединители оператора](associators-of-statement.md).</span><span class="sxs-lookup"><span data-stu-id="5c75a-175">For more information about the REFERENCES OF associated WQL query, source instances, and association objects, see [ASSOCIATORS OF Statement](associators-of-statement.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="5c75a-176">Требования</span><span class="sxs-lookup"><span data-stu-id="5c75a-176">Requirements</span></span>



| <span data-ttu-id="5c75a-177">Требование</span><span class="sxs-lookup"><span data-stu-id="5c75a-177">Requirement</span></span> | <span data-ttu-id="5c75a-178">Значение</span><span class="sxs-lookup"><span data-stu-id="5c75a-178">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="5c75a-179">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="5c75a-179">Minimum supported client</span></span><br/> | <span data-ttu-id="5c75a-180">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="5c75a-180">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="5c75a-181">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="5c75a-181">Minimum supported server</span></span><br/> | <span data-ttu-id="5c75a-182">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="5c75a-182">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="5c75a-183">Header</span><span class="sxs-lookup"><span data-stu-id="5c75a-183">Header</span></span><br/>                   | <dl> <span data-ttu-id="5c75a-184"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="5c75a-184"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="5c75a-185">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="5c75a-185">Type library</span></span><br/>             | <dl> <span data-ttu-id="5c75a-186"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="5c75a-186"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="5c75a-187">DLL</span><span class="sxs-lookup"><span data-stu-id="5c75a-187">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5c75a-188"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5c75a-188"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="5c75a-189">CLSID</span><span class="sxs-lookup"><span data-stu-id="5c75a-189">CLSID</span></span><br/>                    | <span data-ttu-id="5c75a-190">\_SWBEMOBJECT CLSID</span><span class="sxs-lookup"><span data-stu-id="5c75a-190">CLSID\_SWbemObject</span></span><br/>                                                           |
| <span data-ttu-id="5c75a-191">IID</span><span class="sxs-lookup"><span data-stu-id="5c75a-191">IID</span></span><br/>                      | <span data-ttu-id="5c75a-192">IID \_ исвбемобжект</span><span class="sxs-lookup"><span data-stu-id="5c75a-192">IID\_ISWbemObject</span></span><br/>                                                            |



## <a name="see-also"></a><span data-ttu-id="5c75a-193">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="5c75a-193">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5c75a-194">**SWbemObject**</span><span class="sxs-lookup"><span data-stu-id="5c75a-194">**SWbemObject**</span></span>](swbemobject.md)
</dt> <dt>

[<span data-ttu-id="5c75a-195">**SWbemObject. соединители\_**</span><span class="sxs-lookup"><span data-stu-id="5c75a-195">**SWbemObject.Associators\_**</span></span>](swbemobject-associators-.md)
</dt> <dt>

[<span data-ttu-id="5c75a-196">**SWbemServices. АссоЦиаторсоф**</span><span class="sxs-lookup"><span data-stu-id="5c75a-196">**SWbemServices.AssociatorsOf**</span></span>](swbemservices-associatorsof.md)
</dt> <dt>

[<span data-ttu-id="5c75a-197">**SWbemServices. Референцесто**</span><span class="sxs-lookup"><span data-stu-id="5c75a-197">**SWbemServices.ReferencesTo**</span></span>](swbemservices-referencesto.md)
</dt> <dt>

[<span data-ttu-id="5c75a-198">**SWbemServices. Референцестоасинк**</span><span class="sxs-lookup"><span data-stu-id="5c75a-198">**SWbemServices.ReferencesToAsync**</span></span>](swbemservices-referencestoasync.md)
</dt> </dl>

 

