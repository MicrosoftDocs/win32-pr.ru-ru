---
description: Метод АссоЦиаторсасинк \_ объекта SWbemObject получает объекты (классы или экземпляры), связанные с текущим объектом. Эти объекты называются конечными точками. Этот метод выполняет ту же функцию, что и СОЕДИНИТЕЛи WQL-запроса.
ms.assetid: c71e11cd-39a5-40d8-b279-f5ee9ff3ae04
ms.tgt_platform: multiple
title: Метод SWbemObject.AssociatorsAsync_ (Wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemObject.AssociatorsAsync_
- ISWbemObject.AssociatorsAsync_
- ISWbemObject.AssociatorsAsync_
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: fe7a592327b6952308e44ac054fb94e21aa6d6b9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105701960"
---
# <a name="swbemobjectassociatorsasync_-method"></a><span data-ttu-id="01611-105">SWbemObject. АссоЦиаторсасинк, \_ метод</span><span class="sxs-lookup"><span data-stu-id="01611-105">SWbemObject.AssociatorsAsync\_ method</span></span>

<span data-ttu-id="01611-106">Метод **ассоЦиаторсасинк \_** объекта [**SWbemObject**](swbemobject.md) получает объекты (классы или экземпляры), связанные с текущим объектом.</span><span class="sxs-lookup"><span data-stu-id="01611-106">The **AssociatorsAsync\_** method of [**SWbemObject**](swbemobject.md) obtains objects (classes or instances) that are associated with the current object.</span></span> <span data-ttu-id="01611-107">Эти объекты называются конечными точками.</span><span class="sxs-lookup"><span data-stu-id="01611-107">These objects are called endpoints.</span></span> <span data-ttu-id="01611-108">Этот метод выполняет ту же функцию, что и СОЕДИНИТЕЛи WQL-запроса.</span><span class="sxs-lookup"><span data-stu-id="01611-108">This method performs the same function that the ASSOCIATORS OF WQL query performs.</span></span>

<span data-ttu-id="01611-109">Описание этого синтаксиса см. в разделе [соглашения о документе для API скриптов](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="01611-109">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="01611-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="01611-110">Syntax</span></span>


```VB
SWbemObject.AssociatorsAsync_( _
  ByVal objWbemSink, _
  [ ByVal strAssocClass ], _
  [ ByVal strResultClass ], _
  [ ByVal strResultRole ], _
  [ ByVal strRole ], _
  [ ByVal bClassesOnly ], _
  [ ByVal bSchemaOnly ], _
  [ ByVal strRequiredAssocQualifier ], _
  [ ByVal strRequiredQualifier ], _
  [ ByVal iFlags ], _
  [ ByVal objwbemNamedValueSet ], _
  [ ByVal objWbemAsyncContext ] _
)
```



## <a name="parameters"></a><span data-ttu-id="01611-111">Параметры</span><span class="sxs-lookup"><span data-stu-id="01611-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="01611-112">*обжвбемсинк* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="01611-112">*objWbemSink* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="01611-113">Обязательный.</span><span class="sxs-lookup"><span data-stu-id="01611-113">Required.</span></span> <span data-ttu-id="01611-114">Приемник объекта, который асинхронно получает объекты в качестве обратного вызова.</span><span class="sxs-lookup"><span data-stu-id="01611-114">Object sink that receives the objects asynchronously as a callback.</span></span>

</dd> <dt>

<span data-ttu-id="01611-115">*страссоккласс* \[ в необязательное\]</span><span class="sxs-lookup"><span data-stu-id="01611-115">*strAssocClass* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="01611-116">Строка, содержащая класс ассоциации.</span><span class="sxs-lookup"><span data-stu-id="01611-116">String that contains an association class.</span></span> <span data-ttu-id="01611-117">Если этот параметр указан, он указывает, что возвращенные конечные точки должны быть связаны с источником через указанный класс ассоциации или класс, производный от этого класса ассоциации.</span><span class="sxs-lookup"><span data-stu-id="01611-117">If specified, this parameter indicates that the returned endpoints must be associated with the source through the specified association class or a class derived from this association class.</span></span>

</dd> <dt>

<span data-ttu-id="01611-118">*стрресулткласс* \[ в необязательное\]</span><span class="sxs-lookup"><span data-stu-id="01611-118">*strResultClass* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="01611-119">Строка, содержащая имя класса.</span><span class="sxs-lookup"><span data-stu-id="01611-119">String that contains a class name.</span></span> <span data-ttu-id="01611-120">Если этот параметр указан, он указывает, что возвращаемые конечные точки должны принадлежать или быть производными от класса, указанного в этом параметре.</span><span class="sxs-lookup"><span data-stu-id="01611-120">If specified, this parameter indicates that the returned endpoints must belong to or be derived from the class specified in this parameter.</span></span>

</dd> <dt>

<span data-ttu-id="01611-121">*стрресултроле* \[ в необязательное\]</span><span class="sxs-lookup"><span data-stu-id="01611-121">*strResultRole* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="01611-122">Строка, содержащая имя свойства.</span><span class="sxs-lookup"><span data-stu-id="01611-122">String that contains a property name.</span></span> <span data-ttu-id="01611-123">Если этот параметр указан, он указывает, что возвращаемые конечные точки должны играть определенную роль в связи с исходным объектом.</span><span class="sxs-lookup"><span data-stu-id="01611-123">If specified, this parameter indicates that the returned endpoints must play a particular role in their association with the source object.</span></span> <span data-ttu-id="01611-124">Роль определяется именем указанного свойства (которое должно быть ссылочным свойством) ассоциации.</span><span class="sxs-lookup"><span data-stu-id="01611-124">The role is defined by the name of a specified property (which must be a reference property) of an association.</span></span>

</dd> <dt>

<span data-ttu-id="01611-125">*strRole* \[ в необязательное\]</span><span class="sxs-lookup"><span data-stu-id="01611-125">*strRole* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="01611-126">Строка, содержащая имя свойства.</span><span class="sxs-lookup"><span data-stu-id="01611-126">String that contains a property name.</span></span> <span data-ttu-id="01611-127">Если этот параметр задан, он указывает, что возвращенные конечные точки должны участвовать в связи с исходным объектом, в котором исходный объект играет определенную роль.</span><span class="sxs-lookup"><span data-stu-id="01611-127">If specified, this parameter indicates that the returned endpoints must participate in an association with the source object in which the source object plays a particular role.</span></span> <span data-ttu-id="01611-128">Роль определяется именем указанного свойства (которое должно быть ссылочным свойством) ассоциации.</span><span class="sxs-lookup"><span data-stu-id="01611-128">The role is defined by the name of a specified property (which must be a reference property) of an association.</span></span>

</dd> <dt>

<span data-ttu-id="01611-129">*бклассесонли* \[ в необязательное\]</span><span class="sxs-lookup"><span data-stu-id="01611-129">*bClassesOnly* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="01611-130">Логическое значение, указывающее, следует ли возвращать список имен классов, а не фактические экземпляры классов.</span><span class="sxs-lookup"><span data-stu-id="01611-130">Boolean value that indicates whether a list of class names should be returned rather than actual instances of the classes.</span></span> <span data-ttu-id="01611-131">Это классы, к которым относятся экземпляры конечных точек.</span><span class="sxs-lookup"><span data-stu-id="01611-131">These are the classes to which the endpoint instances belong.</span></span> <span data-ttu-id="01611-132">Значение по умолчанию для этого параметра — **false**.</span><span class="sxs-lookup"><span data-stu-id="01611-132">The default value for this parameter is **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="01611-133">*бсчемаонли* \[ в необязательное\]</span><span class="sxs-lookup"><span data-stu-id="01611-133">*bSchemaOnly* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="01611-134">Логическое значение, указывающее, применяется ли запрос к схеме, а не к данным.</span><span class="sxs-lookup"><span data-stu-id="01611-134">Boolean value that indicates whether the query applies to the schema rather than the data.</span></span> <span data-ttu-id="01611-135">Значение по умолчанию для этого параметра — **false**.</span><span class="sxs-lookup"><span data-stu-id="01611-135">The default value for this parameter is **FALSE**.</span></span> <span data-ttu-id="01611-136">Можно задать только **значение true** , если объект, для которого вызывается этот метод, является классом.</span><span class="sxs-lookup"><span data-stu-id="01611-136">It can only be set to **TRUE** if the object on which this method is invoked is a class.</span></span> <span data-ttu-id="01611-137">Если задано **значение true**, набор возвращаемых конечных точек представляет классы, которые связаны с исходным классом в схеме.</span><span class="sxs-lookup"><span data-stu-id="01611-137">When set to **TRUE**, the set of returned endpoints represent classes that are suitably associated with the source class in the schema.</span></span>

</dd> <dt>

<span data-ttu-id="01611-138">*стррекуиредассоккуалифиер* \[ в необязательное\]</span><span class="sxs-lookup"><span data-stu-id="01611-138">*strRequiredAssocQualifier* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="01611-139">Строка, содержащая имя квалификатора.</span><span class="sxs-lookup"><span data-stu-id="01611-139">String that contains a qualifier name.</span></span> <span data-ttu-id="01611-140">Если этот параметр указан, он указывает, что возвращенные конечные точки должны быть связаны с исходным объектом через класс ассоциации, включающий указанный квалификатор.</span><span class="sxs-lookup"><span data-stu-id="01611-140">If specified, this parameter indicates that the returned endpoints must be associated with the source object through an association class that includes the specified qualifier.</span></span>

</dd> <dt>

<span data-ttu-id="01611-141">*стррекуиредкуалифиер* \[ в необязательное\]</span><span class="sxs-lookup"><span data-stu-id="01611-141">*strRequiredQualifier* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="01611-142">Строка, содержащая имя квалификатора.</span><span class="sxs-lookup"><span data-stu-id="01611-142">String that contains a qualifier name.</span></span> <span data-ttu-id="01611-143">Если этот параметр указан, он указывает, что возвращаемые конечные точки должны включать указанный квалификатор.</span><span class="sxs-lookup"><span data-stu-id="01611-143">If specified, this parameter indicates that the returned endpoints must include the specified qualifier.</span></span>

</dd> <dt>

<span data-ttu-id="01611-144">*ифлагс* \[ в необязательное\]</span><span class="sxs-lookup"><span data-stu-id="01611-144">*iFlags* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="01611-145">Целое число, указывающее дополнительные флаги для операции.</span><span class="sxs-lookup"><span data-stu-id="01611-145">Integer specifying additional flags to the operation.</span></span> <span data-ttu-id="01611-146">Этот параметр может принимать следующие значения.</span><span class="sxs-lookup"><span data-stu-id="01611-146">This parameter can accept the following values.</span></span>

<dt>

<span id="wbemFlagSendStatus"></span><span id="wbemflagsendstatus"></span><span id="WBEMFLAGSENDSTATUS"></span>

<span data-ttu-id="01611-147"><span id="wbemFlagSendStatus"></span><span id="wbemflagsendstatus"></span><span id="WBEMFLAGSENDSTATUS"></span>Вбемфлагсендстатус \* \* \* \* (128 (0x80))</span><span class="sxs-lookup"><span data-stu-id="01611-147"><span id="wbemFlagSendStatus"></span><span id="wbemflagsendstatus"></span><span id="WBEMFLAGSENDSTATUS"></span>\*\*\*\*wbemFlagSendStatus\*\*\*\* (128 (0x80))</span></span>


</dt> <dd>

<span data-ttu-id="01611-148">Вызывает асинхронные вызовы для отправки обновлений состояния обработчику событий [**свбемсинк. OnProgress**](swbemsink-onprogress.md) для приемника объекта.</span><span class="sxs-lookup"><span data-stu-id="01611-148">Causes asynchronous calls to send status updates to the [**SWbemSink.OnProgress**](swbemsink-onprogress.md) event handler for the object sink.</span></span>

</dd> <dt>

<span id="wbemFlagDontSendStatus"></span><span id="wbemflagdontsendstatus"></span><span id="WBEMFLAGDONTSENDSTATUS"></span>

<span data-ttu-id="01611-149"><span id="wbemFlagDontSendStatus"></span><span id="wbemflagdontsendstatus"></span><span id="WBEMFLAGDONTSENDSTATUS"></span>Вбемфлагдонтсендстатус \* \* \* \* (0 (0x0))</span><span class="sxs-lookup"><span data-stu-id="01611-149"><span id="wbemFlagDontSendStatus"></span><span id="wbemflagdontsendstatus"></span><span id="WBEMFLAGDONTSENDSTATUS"></span>\*\*\*\*wbemFlagDontSendStatus\*\*\*\* (0 (0x0))</span></span>


</dt> <dd>

<span data-ttu-id="01611-150">Не позволяет асинхронным вызовам отправлять обновления состояния в обработчик событий [**OnProgress**](swbemsink-onprogress.md) для приемника объекта.</span><span class="sxs-lookup"><span data-stu-id="01611-150">Prevents asynchronous calls from sending status updates to the [**OnProgress**](swbemsink-onprogress.md) event handler for the object sink.</span></span>

</dd> <dt>

<span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>

<span data-ttu-id="01611-151"><span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>Вбемфлагусеамендедкуалифиерс \* \* \* \* (131072 (0x20000))</span><span class="sxs-lookup"><span data-stu-id="01611-151"><span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>\*\*\*\*wbemFlagUseAmendedQualifiers\*\*\*\* (131072 (0x20000))</span></span>


</dt> <dd>

<span data-ttu-id="01611-152">Заставляет Инструментарий WMI возвращать локализованные описания классов и свойств.</span><span class="sxs-lookup"><span data-stu-id="01611-152">Causes WMI to return the localized class and property descriptions.</span></span> <span data-ttu-id="01611-153">Дополнительные сведения см. в разделе [Локализация сведений о классе WMI](localizing-wmi-class-information.md).</span><span class="sxs-lookup"><span data-stu-id="01611-153">For more information, see [Localizing WMI Class Information](localizing-wmi-class-information.md).</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="01611-154">*обжвбемнамедвалуесет* \[ в необязательное\]</span><span class="sxs-lookup"><span data-stu-id="01611-154">*objwbemNamedValueSet* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="01611-155">Как правило, это не определено.</span><span class="sxs-lookup"><span data-stu-id="01611-155">Typically, this is undefined.</span></span> <span data-ttu-id="01611-156">В противном случае это объект [**свбемнамедвалуесет**](swbemnamedvalueset.md) , элементы которого представляют сведения о контексте, которые могут использоваться поставщиком, обслуживающим запрос.</span><span class="sxs-lookup"><span data-stu-id="01611-156">Otherwise, this is an [**SWbemNamedValueSet**](swbemnamedvalueset.md) object whose elements represent the context information that can be used by the provider that is servicing the request.</span></span> <span data-ttu-id="01611-157">Поставщик, который поддерживает или требует такую информацию, должен документировать распознанные имена значений, тип данных значения, допустимые значения и семантику.</span><span class="sxs-lookup"><span data-stu-id="01611-157">A provider that supports or requires such information must document the recognized value names, data type of the value, allowed values, and semantics.</span></span>

</dd> <dt>

<span data-ttu-id="01611-158">*обжвбемасинкконтекст* \[ в необязательное\]</span><span class="sxs-lookup"><span data-stu-id="01611-158">*objWbemAsyncContext* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="01611-159">Это объект [**свбемнамедвалуесет**](swbemnamedvalueset.md) , который возвращает приемнику объекта, чтобы узнать источник исходного асинхронного вызова.</span><span class="sxs-lookup"><span data-stu-id="01611-159">This is an [**SWbemNamedValueSet**](swbemnamedvalueset.md) object that returns to the object sink to identify the source of the original asynchronous call.</span></span> <span data-ttu-id="01611-160">Используйте этот параметр, если вы выполняете несколько асинхронных вызовов, использующих один и тот же приемник объекта.</span><span class="sxs-lookup"><span data-stu-id="01611-160">Use this parameter if you are making multiple asynchronous calls using the same object sink.</span></span> <span data-ttu-id="01611-161">Чтобы использовать этот параметр, создайте объект **свбемнамедвалуесет** и используйте метод [**свбемнамедвалуесет. Add**](swbemnamedvalueset-add.md) , чтобы добавить значение, идентифицирующее выполняемый асинхронный вызов.</span><span class="sxs-lookup"><span data-stu-id="01611-161">To use this parameter, create an **SWbemNamedValueSet** object and use the [**SWbemNamedValueSet.Add**](swbemnamedvalueset-add.md) method to add a value that identifies the asynchronous call you are making.</span></span> <span data-ttu-id="01611-162">Этот объект **свбемнамедвалуесет** возвращается в приемник объекта, и источник вызова можно извлечь с помощью метода [**свбемнамедвалуесет. Item**](swbemnamedvalueset-item.md) .</span><span class="sxs-lookup"><span data-stu-id="01611-162">This **SWbemNamedValueSet** object is returned to the object sink and the source of the call can be extracted using the [**SWbemNamedValueSet.Item**](swbemnamedvalueset-item.md) method.</span></span> <span data-ttu-id="01611-163">Дополнительные сведения см. [в разделе вызов метода](calling-a-method.md).</span><span class="sxs-lookup"><span data-stu-id="01611-163">For more information, see [Calling a Method](calling-a-method.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="01611-164">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="01611-164">Return value</span></span>

<span data-ttu-id="01611-165">Этот метод не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="01611-165">This method does not return a value.</span></span> <span data-ttu-id="01611-166">В случае успешного выполнения приемник получает событие [**онобжектреади**](swbemsink-onobjectready.md) для каждого экземпляра.</span><span class="sxs-lookup"><span data-stu-id="01611-166">If successful, the sink receives an [**OnObjectReady**](swbemsink-onobjectready.md) event per instance.</span></span> <span data-ttu-id="01611-167">После последнего экземпляра приемник объекта получает событие [**Oncompleteed**](swbemsink-oncompleted.md) .</span><span class="sxs-lookup"><span data-stu-id="01611-167">After the last instance, the object sink receives an [**OnCompleted**](swbemsink-oncompleted.md) event.</span></span>

## <a name="error-codes"></a><span data-ttu-id="01611-168">Коды ошибок</span><span class="sxs-lookup"><span data-stu-id="01611-168">Error codes</span></span>

<span data-ttu-id="01611-169">После завершения метода **ассоЦиаторсасинк \_** объект [Err](/previous-versions//sbf5ze0e(v=vs.85)) может содержать один из кодов ошибок из следующего списка.</span><span class="sxs-lookup"><span data-stu-id="01611-169">After completion of the **AssociatorsAsync\_** method, the [Err](/previous-versions//sbf5ze0e(v=vs.85)) object may contain one of the error codes in the following list.</span></span>

<dl> <dt>

<span data-ttu-id="01611-170">**вбемерракцессдениед** -2147749891 (0x80041003)</span><span class="sxs-lookup"><span data-stu-id="01611-170">**wbemErrAccessDenied** - 2147749891 (0x80041003)</span></span>
</dt> <dd>

<span data-ttu-id="01611-171">Текущий пользователь не имеет разрешения на просмотр одного или нескольких классов, возвращенных вызовом.</span><span class="sxs-lookup"><span data-stu-id="01611-171">The current user does not have permission to view one or more of the classes returned by the call.</span></span>

</dd> <dt>

<span data-ttu-id="01611-172">**вбемеррфаилед** -2147449889 (0x7FFF7C21)</span><span class="sxs-lookup"><span data-stu-id="01611-172">**wbemErrFailed** - 2147449889 (0x7FFF7C21)</span></span>
</dt> <dd>

<span data-ttu-id="01611-173">Незаданная ошибка.</span><span class="sxs-lookup"><span data-stu-id="01611-173">Unspecified error.</span></span>

</dd> <dt>

<span data-ttu-id="01611-174">**вбемерринвалидпараметер** -2147749896 (0x80041008)</span><span class="sxs-lookup"><span data-stu-id="01611-174">**wbemErrInvalidParameter** - 2147749896 (0x80041008)</span></span>
</dt> <dd>

<span data-ttu-id="01611-175">Указан недопустимый параметр.</span><span class="sxs-lookup"><span data-stu-id="01611-175">A specified parameter is not valid.</span></span>

</dd> <dt>

<span data-ttu-id="01611-176">**вбемерраутофмемори** -2147749894 (0x80041006)</span><span class="sxs-lookup"><span data-stu-id="01611-176">**wbemErrOutOfMemory** - 2147749894 (0x80041006)</span></span>
</dt> <dd>

<span data-ttu-id="01611-177">Недостаточно памяти для завершения операции.</span><span class="sxs-lookup"><span data-stu-id="01611-177">Not enough memory to complete the operation.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="01611-178">Комментарии</span><span class="sxs-lookup"><span data-stu-id="01611-178">Remarks</span></span>

<span data-ttu-id="01611-179">Этот вызов возвращает немедленно.</span><span class="sxs-lookup"><span data-stu-id="01611-179">This call returns immediately.</span></span> <span data-ttu-id="01611-180">Запрошенные объекты и состояние возвращаются вызывающему объекту через обратные вызовы, доставляемые в приемник, указанный в *обжвбемсинк*.</span><span class="sxs-lookup"><span data-stu-id="01611-180">The requested objects and status are returned to the caller through call-backs delivered to the sink that is specified in *objWbemSink*.</span></span> <span data-ttu-id="01611-181">Чтобы обработать каждый объект при поступлении, создайте *обжвбемсинк*. Подпрограммы события [**онобжектреади**](swbemsink-onobjectready.md) .</span><span class="sxs-lookup"><span data-stu-id="01611-181">To process each object when it arrives, create an *objWbemSink*.[**OnObjectReady**](swbemsink-onobjectready.md) event subroutine.</span></span> <span data-ttu-id="01611-182">После возврата всех объектов можно выполнить окончательную обработку в реализации *обжвбемсинк*. Событие [**Oncompleteed**](swbemsink-oncompleted.md) .</span><span class="sxs-lookup"><span data-stu-id="01611-182">After all the objects are returned, you can perform final processing in your implementation of the *objWbemSink*.[**OnCompleted**](swbemsink-oncompleted.md) event.</span></span>

<span data-ttu-id="01611-183">Асинхронный обратный вызов позволяет пользователю без проверки подлинности предоставлять данные в приемник.</span><span class="sxs-lookup"><span data-stu-id="01611-183">An asynchronous callback allows a non-authenticated user to provide data to the sink.</span></span> <span data-ttu-id="01611-184">Это создает угрозы безопасности для сценариев и приложений.</span><span class="sxs-lookup"><span data-stu-id="01611-184">This poses security risks to your scripts and applications.</span></span> <span data-ttu-id="01611-185">Чтобы устранить риски, используйте либо семисинчронаус связь, либо синхронное взаимодействие.</span><span class="sxs-lookup"><span data-stu-id="01611-185">To eliminate the risks, use either semisynchronous communication or synchronous communication.</span></span> <span data-ttu-id="01611-186">Дополнительные сведения см. [в разделе вызов метода](calling-a-method.md).</span><span class="sxs-lookup"><span data-stu-id="01611-186">For more information, see [Calling a Method](calling-a-method.md).</span></span>

<span data-ttu-id="01611-187">Дополнительные сведения о СОЕДИНИТЕЛях связанных WQL-запросов, исходных экземпляров и конечных точек см. в разделе [соединители оператора](associators-of-statement.md).</span><span class="sxs-lookup"><span data-stu-id="01611-187">For more information about the ASSOCIATORS OF associated WQL queries, source instances, and endpoints, see [ASSOCIATORS OF Statement](associators-of-statement.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="01611-188">Требования</span><span class="sxs-lookup"><span data-stu-id="01611-188">Requirements</span></span>



| <span data-ttu-id="01611-189">Требование</span><span class="sxs-lookup"><span data-stu-id="01611-189">Requirement</span></span> | <span data-ttu-id="01611-190">Значение</span><span class="sxs-lookup"><span data-stu-id="01611-190">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="01611-191">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="01611-191">Minimum supported client</span></span><br/> | <span data-ttu-id="01611-192">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="01611-192">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="01611-193">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="01611-193">Minimum supported server</span></span><br/> | <span data-ttu-id="01611-194">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="01611-194">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="01611-195">Header</span><span class="sxs-lookup"><span data-stu-id="01611-195">Header</span></span><br/>                   | <dl> <span data-ttu-id="01611-196"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="01611-196"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="01611-197">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="01611-197">Type library</span></span><br/>             | <dl> <span data-ttu-id="01611-198"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="01611-198"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="01611-199">DLL</span><span class="sxs-lookup"><span data-stu-id="01611-199">DLL</span></span><br/>                      | <dl> <span data-ttu-id="01611-200"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="01611-200"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="01611-201">CLSID</span><span class="sxs-lookup"><span data-stu-id="01611-201">CLSID</span></span><br/>                    | <span data-ttu-id="01611-202">\_SWBEMOBJECT CLSID</span><span class="sxs-lookup"><span data-stu-id="01611-202">CLSID\_SWbemObject</span></span><br/>                                                           |
| <span data-ttu-id="01611-203">IID</span><span class="sxs-lookup"><span data-stu-id="01611-203">IID</span></span><br/>                      | <span data-ttu-id="01611-204">IID \_ исвбемобжект</span><span class="sxs-lookup"><span data-stu-id="01611-204">IID\_ISWbemObject</span></span><br/>                                                            |



## <a name="see-also"></a><span data-ttu-id="01611-205">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="01611-205">See also</span></span>

<dl> <dt>

[<span data-ttu-id="01611-206">**SWbemObject**</span><span class="sxs-lookup"><span data-stu-id="01611-206">**SWbemObject**</span></span>](swbemobject.md)
</dt> <dt>

[<span data-ttu-id="01611-207">**SWbemServices. АссоЦиаторсофасинк**</span><span class="sxs-lookup"><span data-stu-id="01611-207">**SWbemServices.AssociatorsOfAsync**</span></span>](swbemservices-associatorsofasync.md)
</dt> <dt>

[<span data-ttu-id="01611-208">**SWbemObject. References\_**</span><span class="sxs-lookup"><span data-stu-id="01611-208">**SWbemObject.References\_**</span></span>](swbemobject-references-.md)
</dt> <dt>

[<span data-ttu-id="01611-209">**SWbemServices. Референцесто**</span><span class="sxs-lookup"><span data-stu-id="01611-209">**SWbemServices.ReferencesTo**</span></span>](swbemservices-referencesto.md)
</dt> </dl>

 

