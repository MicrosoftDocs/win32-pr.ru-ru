---
description: Возвращает все классы или экземпляры взаимосвязей, которые ссылаются на конкретный исходный класс или экземпляр.
ms.assetid: 2ad66ea1-b8f0-4b6b-b68f-29496afbe4bf
ms.tgt_platform: multiple
title: SWbemServices. Референцестоасинк, метод (Wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemServices.ReferencesToAsync
- ISWbemServices.ReferencesToAsync
- ISWbemServices.ReferencesToAsync
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 64a8b9b336a1e7aa6007b17d2e878f1ace5e6163
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105711623"
---
# <a name="swbemservicesreferencestoasync-method"></a><span data-ttu-id="b84fe-103">SWbemServices. Референцестоасинк, метод</span><span class="sxs-lookup"><span data-stu-id="b84fe-103">SWbemServices.ReferencesToAsync method</span></span>

<span data-ttu-id="b84fe-104">Метод **референцестоасинк** объекта [**SwbemServices**](swbemservices.md) возвращает все классы ассоциации или экземпляры, ссылающиеся на конкретный исходный класс или экземпляр.</span><span class="sxs-lookup"><span data-stu-id="b84fe-104">The **ReferencesToAsync** method of the [**SWbemServices**](swbemservices.md) object returns all association classes or instances that refer to a specific source class or instance.</span></span> <span data-ttu-id="b84fe-105">Этот метод выполняет ту же функцию, что и [ссылки на](references-of-statement.md) WQL-запросы.</span><span class="sxs-lookup"><span data-stu-id="b84fe-105">This method performs the same function that the [REFERENCES OF](references-of-statement.md) WQL query performs.</span></span>

<span data-ttu-id="b84fe-106">Дополнительные сведения об асинхронном режиме см. в разделе [вызов метода](calling-a-method.md).</span><span class="sxs-lookup"><span data-stu-id="b84fe-106">For more information about the asynchronous mode, see [Calling a Method](calling-a-method.md).</span></span>

<span data-ttu-id="b84fe-107">Описание этого синтаксиса см. в разделе [соглашения о документе для API скриптов](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="b84fe-107">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="b84fe-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="b84fe-108">Syntax</span></span>


```VB
SWbemServices.ReferencesToAsync( _
  ByVal ObjWbemSink, _
  ByVal strObjectPath, _
  [ ByVal strResultClass ], _
  [ ByVal strRole ], _
  [ ByVal bClassesOnly ], _
  [ ByVal bSchemaOnly ], _
  [ ByVal strRequiredQualifier ], _
  [ ByVal iFlags ], _
  [ ByVal objWbemNamedValueSet ], _
  [ ByVal objWbemAsyncContext ] _
)
```



## <a name="parameters"></a><span data-ttu-id="b84fe-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="b84fe-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b84fe-110">*обжвбемсинк*</span><span class="sxs-lookup"><span data-stu-id="b84fe-110">*ObjWbemSink*</span></span> 
</dt> <dd>

<span data-ttu-id="b84fe-111">Обязательный.</span><span class="sxs-lookup"><span data-stu-id="b84fe-111">Required.</span></span> <span data-ttu-id="b84fe-112">Приемник объекта, который асинхронно получает объекты.</span><span class="sxs-lookup"><span data-stu-id="b84fe-112">Object sink that receives the objects asynchronously.</span></span> <span data-ttu-id="b84fe-113">Создайте объект [**свбемсинк**](swbemsink.md) для получения объектов.</span><span class="sxs-lookup"><span data-stu-id="b84fe-113">Create a [**SWbemSink**](swbemsink.md) object to receive the objects.</span></span>

</dd> <dt>

<span data-ttu-id="b84fe-114">*стробжектпас*</span><span class="sxs-lookup"><span data-stu-id="b84fe-114">*strObjectPath*</span></span> 
</dt> <dd>

<span data-ttu-id="b84fe-115">Обязательный.</span><span class="sxs-lookup"><span data-stu-id="b84fe-115">Required.</span></span> <span data-ttu-id="b84fe-116">Строка, содержащая путь к объекту источника для этого метода.</span><span class="sxs-lookup"><span data-stu-id="b84fe-116">String that contains the object path of the source for this method.</span></span> <span data-ttu-id="b84fe-117">Дополнительные сведения см. в разделе [Локализация сведений о классе WMI](localizing-wmi-class-information.md).</span><span class="sxs-lookup"><span data-stu-id="b84fe-117">For more information, see [Localizing WMI Class Information](localizing-wmi-class-information.md).</span></span>

</dd> <dt>

<span data-ttu-id="b84fe-118">*стрресулткласс* \[ используемых\]</span><span class="sxs-lookup"><span data-stu-id="b84fe-118">*strResultClass* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="b84fe-119">Строка, содержащая имя класса.</span><span class="sxs-lookup"><span data-stu-id="b84fe-119">String that contains a class name.</span></span> <span data-ttu-id="b84fe-120">Если этот параметр указан, то возвращаемые объекты ассоциации должны принадлежать классу, указанному в этом параметре, или быть производным от него.</span><span class="sxs-lookup"><span data-stu-id="b84fe-120">If specified, this parameter indicates that the returned association objects must belong to or be derived from the class that is specified in this parameter.</span></span>

</dd> <dt>

<span data-ttu-id="b84fe-121">*strRole* \[ используемых\]</span><span class="sxs-lookup"><span data-stu-id="b84fe-121">*strRole* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="b84fe-122">Строка, содержащая имя свойства.</span><span class="sxs-lookup"><span data-stu-id="b84fe-122">String that contains a property name.</span></span> <span data-ttu-id="b84fe-123">Если этот параметр задан, он указывает, что возвращаемые объекты связи должны быть ограничены теми, в которых исходный объект играет определенную роль.</span><span class="sxs-lookup"><span data-stu-id="b84fe-123">If specified, this parameter indicates that the returned association objects must be limited to those in which the source object plays a specific role.</span></span> <span data-ttu-id="b84fe-124">Роль определяется именем указанного ссылочного свойства ассоциации.</span><span class="sxs-lookup"><span data-stu-id="b84fe-124">The role is defined by the name of a specified reference property of an association.</span></span>

</dd> <dt>

<span data-ttu-id="b84fe-125">*бклассесонли* \[ используемых\]</span><span class="sxs-lookup"><span data-stu-id="b84fe-125">*bClassesOnly* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="b84fe-126">Логическое значение, указывающее, следует ли возвращать список имен классов, а не фактические экземпляры классов.</span><span class="sxs-lookup"><span data-stu-id="b84fe-126">Boolean value that indicates whether or not a list of class names should be returned rather than actual instances of the classes.</span></span> <span data-ttu-id="b84fe-127">Это классы, к которым принадлежат объекты взаимосвязей.</span><span class="sxs-lookup"><span data-stu-id="b84fe-127">These are the classes to which the association objects belong.</span></span> <span data-ttu-id="b84fe-128">Значение по умолчанию для этого параметра — **false**.</span><span class="sxs-lookup"><span data-stu-id="b84fe-128">The default value for this parameter is **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="b84fe-129">*бсчемаонли* \[ используемых\]</span><span class="sxs-lookup"><span data-stu-id="b84fe-129">*bSchemaOnly* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="b84fe-130">Логическое значение, указывающее, применяется ли запрос к схеме, а не к данным.</span><span class="sxs-lookup"><span data-stu-id="b84fe-130">Boolean value that indicates whether or not the query applies to the schema rather than the data.</span></span> <span data-ttu-id="b84fe-131">Значение по умолчанию для этого параметра — **false**.</span><span class="sxs-lookup"><span data-stu-id="b84fe-131">The default value for this parameter is **FALSE**.</span></span> <span data-ttu-id="b84fe-132">Можно задать только **значение true** , если параметр *стробжектпас* указывает путь к объекту класса.</span><span class="sxs-lookup"><span data-stu-id="b84fe-132">It can only be set to **TRUE** if the *strObjectPath* parameter specifies the object path of a class.</span></span> <span data-ttu-id="b84fe-133">Если задано **значение true**, то набор возвращаемых конечных точек представляет классы, связанные с исходным классом в схеме.</span><span class="sxs-lookup"><span data-stu-id="b84fe-133">When set to **TRUE**, the set of returned endpoints represents classes that are associated with the source class in schema.</span></span>

</dd> <dt>

<span data-ttu-id="b84fe-134">*стррекуиредкуалифиер* \[ используемых\]</span><span class="sxs-lookup"><span data-stu-id="b84fe-134">*strRequiredQualifier* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="b84fe-135">Строка, содержащая имя квалификатора.</span><span class="sxs-lookup"><span data-stu-id="b84fe-135">String that contains a qualifier name.</span></span> <span data-ttu-id="b84fe-136">Если этот параметр указан, он указывает, что возвращаемые объекты связи должны включать указанный квалификатор.</span><span class="sxs-lookup"><span data-stu-id="b84fe-136">If specified, this parameter indicates that the returned association objects must include the specified qualifier.</span></span>

</dd> <dt>

<span data-ttu-id="b84fe-137">*ифлагс* \[ используемых\]</span><span class="sxs-lookup"><span data-stu-id="b84fe-137">*iFlags* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="b84fe-138">Целое число, задающее дополнительные флаги для операции.</span><span class="sxs-lookup"><span data-stu-id="b84fe-138">Integer that specifies additional flags to the operation.</span></span> <span data-ttu-id="b84fe-139">Значение по умолчанию для этого параметра — **вбемфлагбидиректионал**.</span><span class="sxs-lookup"><span data-stu-id="b84fe-139">The default for this parameter is **wbemFlagBidirectional**.</span></span> <span data-ttu-id="b84fe-140">Этот параметр может принимать следующие значения.</span><span class="sxs-lookup"><span data-stu-id="b84fe-140">This parameter can accept the following values.</span></span>

<dt>

<span id="wbemFlagSendStatus"></span><span id="wbemflagsendstatus"></span><span id="WBEMFLAGSENDSTATUS"></span>

<span data-ttu-id="b84fe-141"><span id="wbemFlagSendStatus"></span><span id="wbemflagsendstatus"></span><span id="WBEMFLAGSENDSTATUS"></span>Вбемфлагсендстатус \* \* \* \* (128 (0x80))</span><span class="sxs-lookup"><span data-stu-id="b84fe-141"><span id="wbemFlagSendStatus"></span><span id="wbemflagsendstatus"></span><span id="WBEMFLAGSENDSTATUS"></span>\*\*\*\*wbemFlagSendStatus\*\*\*\* (128 (0x80))</span></span>


</dt> <dd>

<span data-ttu-id="b84fe-142">Вызывает асинхронные вызовы для отправки обновлений состояния обработчику событий [**OnProgress**](swbemsink-onprogress.md) для приемника объекта.</span><span class="sxs-lookup"><span data-stu-id="b84fe-142">Causes asynchronous calls to send status updates to the [**OnProgress**](swbemsink-onprogress.md) event handler for the object sink.</span></span>

</dd> <dt>

<span id="wbemFlagDontSendStatus"></span><span id="wbemflagdontsendstatus"></span><span id="WBEMFLAGDONTSENDSTATUS"></span>

<span data-ttu-id="b84fe-143"><span id="wbemFlagDontSendStatus"></span><span id="wbemflagdontsendstatus"></span><span id="WBEMFLAGDONTSENDSTATUS"></span>Вбемфлагдонтсендстатус \* \* \* \* (0 (0x0))</span><span class="sxs-lookup"><span data-stu-id="b84fe-143"><span id="wbemFlagDontSendStatus"></span><span id="wbemflagdontsendstatus"></span><span id="WBEMFLAGDONTSENDSTATUS"></span>\*\*\*\*wbemFlagDontSendStatus\*\*\*\* (0 (0x0))</span></span>


</dt> <dd>

<span data-ttu-id="b84fe-144">Не позволяет асинхронным вызовам отправлять обновления состояния в обработчик событий [**OnProgress**](swbemsink-onprogress.md) для приемника объекта.</span><span class="sxs-lookup"><span data-stu-id="b84fe-144">Prevents asynchronous calls from sending status updates to the [**OnProgress**](swbemsink-onprogress.md) event handler for the object sink.</span></span>

</dd> <dt>

<span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>

<span data-ttu-id="b84fe-145"><span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>Вбемфлагусеамендедкуалифиерс \* \* \* \* (131072 (0x20000))</span><span class="sxs-lookup"><span data-stu-id="b84fe-145"><span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>\*\*\*\*wbemFlagUseAmendedQualifiers\*\*\*\* (131072 (0x20000))</span></span>


</dt> <dd>

<span data-ttu-id="b84fe-146">Приводит к тому, что инструментарий управления Windows (WMI) (WMI) возвращает данные о поправности класса вместе с определением базового класса.</span><span class="sxs-lookup"><span data-stu-id="b84fe-146">Causes Windows Management Instrumentation (WMI) to return class amendment data along with the base class definition.</span></span> <span data-ttu-id="b84fe-147">Дополнительные сведения см. в разделе [Локализация сведений о классе WMI](localizing-wmi-class-information.md).</span><span class="sxs-lookup"><span data-stu-id="b84fe-147">For more information, see [Localizing WMI Class Information](localizing-wmi-class-information.md).</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="b84fe-148">*обжвбемнамедвалуесет* \[ используемых\]</span><span class="sxs-lookup"><span data-stu-id="b84fe-148">*objWbemNamedValueSet* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="b84fe-149">Как правило, это не определено.</span><span class="sxs-lookup"><span data-stu-id="b84fe-149">Typically, this is undefined.</span></span> <span data-ttu-id="b84fe-150">В противном случае это объект [**свбемнамедвалуесет**](swbemnamedvalueset.md) , элементы которого представляют сведения о контексте, которые могут использоваться поставщиком, обслуживающим запрос.</span><span class="sxs-lookup"><span data-stu-id="b84fe-150">Otherwise, this is an [**SWbemNamedValueSet**](swbemnamedvalueset.md) object whose elements represent the context information that can be used by the provider that is servicing the request.</span></span> <span data-ttu-id="b84fe-151">Поставщик, который поддерживает или требует сведения о контексте, должен документировать распознанные имена значений, тип данных значения, допустимые значения и семантику.</span><span class="sxs-lookup"><span data-stu-id="b84fe-151">A provider that supports or requires context information must document the recognized value names, data type of the value, allowed values, and semantics.</span></span>

</dd> <dt>

<span data-ttu-id="b84fe-152">*обжвбемасинкконтекст* \[ используемых\]</span><span class="sxs-lookup"><span data-stu-id="b84fe-152">*objWbemAsyncContext* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="b84fe-153">Это объект [**свбемнамедвалуесет**](swbemnamedvalueset.md) , который возвращает приемнику объекта, чтобы узнать источник исходного асинхронного вызова.</span><span class="sxs-lookup"><span data-stu-id="b84fe-153">This is an [**SWbemNamedValueSet**](swbemnamedvalueset.md) object that returns to the object sink to identify the source of the original asynchronous call.</span></span> <span data-ttu-id="b84fe-154">Этот параметр используется для выполнения нескольких асинхронных вызовов с использованием одного и того же приемника объекта.</span><span class="sxs-lookup"><span data-stu-id="b84fe-154">Use this parameter to make multiple asynchronous calls using the same object sink.</span></span> <span data-ttu-id="b84fe-155">Чтобы использовать этот параметр, создайте объект **свбемнамедвалуесет** и используйте метод [**свбемнамедвалуесет. Add**](swbemnamedvalueset-add.md) , чтобы добавить значение, идентифицирующее выполняемый асинхронный вызов.</span><span class="sxs-lookup"><span data-stu-id="b84fe-155">To use this parameter, create an **SWbemNamedValueSet** object, and use the [**SWbemNamedValueSet.Add**](swbemnamedvalueset-add.md) method to add a value that identifies the asynchronous call you are making.</span></span> <span data-ttu-id="b84fe-156">Этот объект **свбемнамедвалуесет** возвращается в приемник объекта, и источник вызова можно извлечь с помощью метода [**свбемнамедвалуесет. Item**](swbemnamedvalueset-item.md) .</span><span class="sxs-lookup"><span data-stu-id="b84fe-156">This **SWbemNamedValueSet** object is returned to the object sink, and the source of the call can be extracted using the [**SWbemNamedValueSet.Item**](swbemnamedvalueset-item.md) method.</span></span> <span data-ttu-id="b84fe-157">Дополнительные сведения см. [в разделе вызов метода](calling-a-method.md).</span><span class="sxs-lookup"><span data-stu-id="b84fe-157">For more information, see [Calling a Method](calling-a-method.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b84fe-158">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="b84fe-158">Return value</span></span>

<span data-ttu-id="b84fe-159">Этот метод не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="b84fe-159">This method does not return a value.</span></span> <span data-ttu-id="b84fe-160">В случае успешного выполнения приемник получает событие [**онобжектреади**](swbemsink-onobjectready.md) для каждого экземпляра.</span><span class="sxs-lookup"><span data-stu-id="b84fe-160">If successful, the sink receives an [**OnObjectReady**](swbemsink-onobjectready.md) event per instance.</span></span> <span data-ttu-id="b84fe-161">После последнего экземпляра приемник объекта получает событие [**Oncompleteed**](swbemsink-oncompleted.md) .</span><span class="sxs-lookup"><span data-stu-id="b84fe-161">After the last instance, the object sink receives an [**OnCompleted**](swbemsink-oncompleted.md) event.</span></span>

## <a name="error-codes"></a><span data-ttu-id="b84fe-162">Коды ошибок</span><span class="sxs-lookup"><span data-stu-id="b84fe-162">Error codes</span></span>

<span data-ttu-id="b84fe-163">После завершения метода **референцестоасинк** объект [Err](/previous-versions//sbf5ze0e(v=vs.85)) может содержать один из кодов ошибок из следующего списка.</span><span class="sxs-lookup"><span data-stu-id="b84fe-163">After the completion of the **ReferencesToAsync** method, the [Err](/previous-versions//sbf5ze0e(v=vs.85)) object may contain one of the error codes in the following list.</span></span>

> [!Note]  
> <span data-ttu-id="b84fe-164">Возвращенная коллекция с нулевым числом элементов не является ошибкой.</span><span class="sxs-lookup"><span data-stu-id="b84fe-164">A returned collection with zero elements is not an error.</span></span>

 

<dl> <dt>

<span data-ttu-id="b84fe-165">**вбемерракцессдениед** -2147749891 (0x80041003)</span><span class="sxs-lookup"><span data-stu-id="b84fe-165">**wbemErrAccessDenied** - 2147749891 (0x80041003)</span></span>
</dt> <dd>

<span data-ttu-id="b84fe-166">У текущего пользователя нет разрешения на просмотр одного или нескольких классов, возвращенных вызовом.</span><span class="sxs-lookup"><span data-stu-id="b84fe-166">Current user does not have the permission to view one or more of the classes returned by the call.</span></span>

</dd> <dt>

<span data-ttu-id="b84fe-167">**вбемеррфаилед** -2147749889 (0x80041001)</span><span class="sxs-lookup"><span data-stu-id="b84fe-167">**wbemErrFailed** - 2147749889 (0x80041001)</span></span>
</dt> <dd>

<span data-ttu-id="b84fe-168">Незаданная ошибка.</span><span class="sxs-lookup"><span data-stu-id="b84fe-168">Unspecified error.</span></span>

</dd> <dt>

<span data-ttu-id="b84fe-169">**вбемерринвалидпараметер** -2147749896 (0x80041008)</span><span class="sxs-lookup"><span data-stu-id="b84fe-169">**wbemErrInvalidParameter** - 2147749896 (0x80041008)</span></span>
</dt> <dd>

<span data-ttu-id="b84fe-170">Указан недопустимый параметр.</span><span class="sxs-lookup"><span data-stu-id="b84fe-170">Invalid parameter was specified.</span></span>

</dd> <dt>

<span data-ttu-id="b84fe-171">**вбемерраутофмемори** -2147749894 (0x80041006)</span><span class="sxs-lookup"><span data-stu-id="b84fe-171">**wbemErrOutOfMemory** - 2147749894 (0x80041006)</span></span>
</dt> <dd>

<span data-ttu-id="b84fe-172">Недостаточно памяти для завершения операции.</span><span class="sxs-lookup"><span data-stu-id="b84fe-172">Not enough memory to complete the operation.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="b84fe-173">Комментарии</span><span class="sxs-lookup"><span data-stu-id="b84fe-173">Remarks</span></span>

<span data-ttu-id="b84fe-174">Этот вызов возвращает немедленно.</span><span class="sxs-lookup"><span data-stu-id="b84fe-174">This call returns immediately.</span></span> <span data-ttu-id="b84fe-175">Запрошенные объекты и состояние возвращаются вызывающему объекту через обратные вызовы, доставляемые в приемник, указанный в *обжвбемсинк*.</span><span class="sxs-lookup"><span data-stu-id="b84fe-175">The requested objects and status are returned to the caller through callbacks delivered to the sink that is specified in *objWbemSink*.</span></span> <span data-ttu-id="b84fe-176">Чтобы обработать каждый объект при его возврате, создайте *обжвбемсинк*. Подпрограммы события [**онобжектреади**](swbemsink-onobjectready.md) .</span><span class="sxs-lookup"><span data-stu-id="b84fe-176">To process each object when it returns, create an *objWbemSink*.[**OnObjectReady**](swbemsink-onobjectready.md) event subroutine.</span></span> <span data-ttu-id="b84fe-177">После возврата всех объектов можно выполнить окончательную обработку в реализации *обжвбемсинк*. Событие [**Oncompleteed**](swbemsink-oncompleted.md) .</span><span class="sxs-lookup"><span data-stu-id="b84fe-177">After all the objects are returned, you can perform final processing in your implementation of the *objWbemSink*.[**OnCompleted**](swbemsink-oncompleted.md) event.</span></span>

<span data-ttu-id="b84fe-178">Асинхронный обратный вызов позволяет пользователю без проверки подлинности предоставлять данные в приемник.</span><span class="sxs-lookup"><span data-stu-id="b84fe-178">An asynchronous callback allows a non-authenticated user to provide data to the sink.</span></span> <span data-ttu-id="b84fe-179">Это создает угрозы безопасности для сценариев и приложений.</span><span class="sxs-lookup"><span data-stu-id="b84fe-179">This poses security risks to your scripts and applications.</span></span> <span data-ttu-id="b84fe-180">Сведения об устранении рисков см. в разделе [Настройка безопасности при асинхронном вызове](setting-security-on-an-asynchronous-call.md).</span><span class="sxs-lookup"><span data-stu-id="b84fe-180">To eliminate the risks, see [Setting Security on an Asynchronous Call](setting-security-on-an-asynchronous-call.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="b84fe-181">Требования</span><span class="sxs-lookup"><span data-stu-id="b84fe-181">Requirements</span></span>



| <span data-ttu-id="b84fe-182">Требование</span><span class="sxs-lookup"><span data-stu-id="b84fe-182">Requirement</span></span> | <span data-ttu-id="b84fe-183">Значение</span><span class="sxs-lookup"><span data-stu-id="b84fe-183">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="b84fe-184">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="b84fe-184">Minimum supported client</span></span><br/> | <span data-ttu-id="b84fe-185">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="b84fe-185">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="b84fe-186">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="b84fe-186">Minimum supported server</span></span><br/> | <span data-ttu-id="b84fe-187">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="b84fe-187">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="b84fe-188">Header</span><span class="sxs-lookup"><span data-stu-id="b84fe-188">Header</span></span><br/>                   | <dl> <span data-ttu-id="b84fe-189"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="b84fe-189"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="b84fe-190">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="b84fe-190">Type library</span></span><br/>             | <dl> <span data-ttu-id="b84fe-191"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="b84fe-191"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="b84fe-192">DLL</span><span class="sxs-lookup"><span data-stu-id="b84fe-192">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b84fe-193"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b84fe-193"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="b84fe-194">CLSID</span><span class="sxs-lookup"><span data-stu-id="b84fe-194">CLSID</span></span><br/>                    | <span data-ttu-id="b84fe-195">\_SWBEMSERVICES CLSID</span><span class="sxs-lookup"><span data-stu-id="b84fe-195">CLSID\_SWbemServices</span></span><br/>                                                         |
| <span data-ttu-id="b84fe-196">IID</span><span class="sxs-lookup"><span data-stu-id="b84fe-196">IID</span></span><br/>                      | <span data-ttu-id="b84fe-197">IID \_ исвбемсервицес</span><span class="sxs-lookup"><span data-stu-id="b84fe-197">IID\_ISWbemServices</span></span><br/>                                                          |



## <a name="see-also"></a><span data-ttu-id="b84fe-198">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="b84fe-198">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b84fe-199">**SWbemServices**</span><span class="sxs-lookup"><span data-stu-id="b84fe-199">**SWbemServices**</span></span>](swbemservices.md)
</dt> <dt>

[<span data-ttu-id="b84fe-200">**SWbemObject. соединители\_**</span><span class="sxs-lookup"><span data-stu-id="b84fe-200">**SWbemObject.Associators\_**</span></span>](swbemobject-associators-.md)
</dt> <dt>

[<span data-ttu-id="b84fe-201">**SWbemObject. References\_**</span><span class="sxs-lookup"><span data-stu-id="b84fe-201">**SWbemObject.References\_**</span></span>](swbemobject-references-.md)
</dt> <dt>

[<span data-ttu-id="b84fe-202">**SWbemServices. АссоЦиаторсоф**</span><span class="sxs-lookup"><span data-stu-id="b84fe-202">**SWbemServices.AssociatorsOf**</span></span>](swbemservices-referencesto.md)
</dt> </dl>

 

