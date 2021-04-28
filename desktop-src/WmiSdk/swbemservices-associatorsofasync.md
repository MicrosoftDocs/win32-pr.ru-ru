---
description: SWbemServices. АссоЦиаторсофасинк, метод возвращает коллекцию объектов (классов или экземпляров), называемых конечными точками, которые связаны с указанным объектом.
ms.assetid: 3969d90f-d39c-40f1-9328-fc1afbaa53b1
ms.tgt_platform: multiple
title: SWbemServices. АссоЦиаторсофасинк, метод (Wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemServices.AssociatorsOfAsync
- ISWbemServices.AssociatorsOfAsync
- ISWbemServices.AssociatorsOfAsync
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 4b16eed97c891b4b4f5bd283496868d99f9e0fbc
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108103672"
---
# <a name="swbemservicesassociatorsofasync-method"></a><span data-ttu-id="214cf-103">SWbemServices. АссоЦиаторсофасинк, метод</span><span class="sxs-lookup"><span data-stu-id="214cf-103">SWbemServices.AssociatorsOfAsync method</span></span>

<span data-ttu-id="214cf-104">Метод **ассоЦиаторсофасинк** объекта [**SwbemServices**](swbemservices.md) Возвращает коллекцию объектов (классов или экземпляров), называемых конечными точками, которые связаны с указанным объектом.</span><span class="sxs-lookup"><span data-stu-id="214cf-104">The **AssociatorsOfAsync** method of the [**SWbemServices**](swbemservices.md) object returns a collection of objects (classes or instances) called endpoints that are associated with a specified object.</span></span> <span data-ttu-id="214cf-105">Вызов **ассоЦиаторсофасинк** немедленно возвращает результат, а результаты и состояние возвращаются вызывающему через события, доставляемые в приемник, указанный в *обжвбемсинк*.</span><span class="sxs-lookup"><span data-stu-id="214cf-105">The call to **AssociatorsOfAsync** returns immediately, and the results and status are returned to the caller through events delivered to the sink that is specified in *objWbemSink*.</span></span> <span data-ttu-id="214cf-106">Чтобы выполнить обработку каждого возвращенного объекта, создайте *обжвбемсинк*. Обработчик событий [**онобжектреади**](swbemsink-onobjectready.md) .</span><span class="sxs-lookup"><span data-stu-id="214cf-106">To handle each returned object, create an *objWbemSink*.[**OnObjectReady**](swbemsink-onobjectready.md) event handler.</span></span>

<span data-ttu-id="214cf-107">После прибытия всех объектов обработка выполняется в *обжвбемсинк*. Событие [**Oncompleteed**](swbemsink-oncompleted.md) .</span><span class="sxs-lookup"><span data-stu-id="214cf-107">After all the objects arrive, processing is done in the *objWbemSink*.[**OnCompleted**](swbemsink-oncompleted.md) event.</span></span> <span data-ttu-id="214cf-108">Этот метод выполняет ту же функцию, что и СОЕДИНИТЕЛи WQL-запроса.</span><span class="sxs-lookup"><span data-stu-id="214cf-108">This method performs the same function that the ASSOCIATORS OF WQL query performs.</span></span> <span data-ttu-id="214cf-109">Дополнительные сведения о создании приемника см. [в разделе Получение WMI-события](receiving-a-wmi-event.md).</span><span class="sxs-lookup"><span data-stu-id="214cf-109">For more information about creating a sink, see [Receiving a WMI Event](receiving-a-wmi-event.md).</span></span>

<span data-ttu-id="214cf-110">Метод вызывается в асинхронном режиме.</span><span class="sxs-lookup"><span data-stu-id="214cf-110">The method is called in the asynchronous mode.</span></span> <span data-ttu-id="214cf-111">Дополнительные сведения см. [в разделе вызов метода](calling-a-method.md).</span><span class="sxs-lookup"><span data-stu-id="214cf-111">For more information, see [Calling a Method](calling-a-method.md).</span></span>

<span data-ttu-id="214cf-112">Описание этого синтаксиса см. в разделе [соглашения о документе для API скриптов](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="214cf-112">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="214cf-113">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="214cf-113">Syntax</span></span>


```VB
SWbemServices.AssociatorsOfAsync( _
  ByVal objWbemSink, _
  ByVal strObjectPath, _
  [ ByVal strAssocClass ], _
  [ ByVal strResultClass ], _
  [ ByVal strResultRole ], _
  [ ByVal strRole ], _
  [ ByVal bClassesOnly ], _
  [ ByVal bSchemaOnly ], _
  [ ByVal strRequiredAssocQualifier ], _
  [ ByVal strRequiredQualifier ], _
  [ ByVal iFlags ], _
  [ ByVal objWbemNamedValueSet ], _
  [ ByVal objWbemAsyncContext ] _
)
```



## <a name="parameters"></a><span data-ttu-id="214cf-114">Параметры</span><span class="sxs-lookup"><span data-stu-id="214cf-114">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="214cf-115">*обжвбемсинк*</span><span class="sxs-lookup"><span data-stu-id="214cf-115">*objWbemSink*</span></span> 
</dt> <dd>

<span data-ttu-id="214cf-116">Обязательный элемент.</span><span class="sxs-lookup"><span data-stu-id="214cf-116">Required.</span></span> <span data-ttu-id="214cf-117">Приемник объекта, который асинхронно получает объекты.</span><span class="sxs-lookup"><span data-stu-id="214cf-117">Object sink that receives the objects asynchronously.</span></span> <span data-ttu-id="214cf-118">Создайте объект [**свбемсинк**](swbemsink.md) для получения объектов.</span><span class="sxs-lookup"><span data-stu-id="214cf-118">Create an [**SWbemSink**](swbemsink.md) object to receive the objects.</span></span>

</dd> <dt>

<span data-ttu-id="214cf-119">*стробжектпас*</span><span class="sxs-lookup"><span data-stu-id="214cf-119">*strObjectPath*</span></span> 
</dt> <dd>

<span data-ttu-id="214cf-120">Обязательный элемент.</span><span class="sxs-lookup"><span data-stu-id="214cf-120">Required.</span></span> <span data-ttu-id="214cf-121">Строка, содержащая путь к объекту исходного класса или экземпляра.</span><span class="sxs-lookup"><span data-stu-id="214cf-121">String that contains the object path of the source class or instance.</span></span> <span data-ttu-id="214cf-122">Дополнительные сведения см. [в разделе Описание расположения объекта WMI](describing-the-location-of-a-wmi-object.md).</span><span class="sxs-lookup"><span data-stu-id="214cf-122">For more information, see [Describing the Location of a WMI Object](describing-the-location-of-a-wmi-object.md).</span></span>

</dd> <dt>

<span data-ttu-id="214cf-123">*страссоккласс* \[ используемых\]</span><span class="sxs-lookup"><span data-stu-id="214cf-123">*strAssocClass* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="214cf-124">Строка, содержащая класс ассоциации.</span><span class="sxs-lookup"><span data-stu-id="214cf-124">String that contains an association class.</span></span> <span data-ttu-id="214cf-125">Если этот параметр указан, он указывает, что возвращенные конечные точки должны быть связаны с источником через указанный класс ассоциации или класс, производный от этого класса ассоциации.</span><span class="sxs-lookup"><span data-stu-id="214cf-125">When specified, this parameter indicates that the returned endpoints must be associated with the source through the specified association class or a class derived from this association class.</span></span>

</dd> <dt>

<span data-ttu-id="214cf-126">*стрресулткласс* \[ используемых\]</span><span class="sxs-lookup"><span data-stu-id="214cf-126">*strResultClass* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="214cf-127">Строка, содержащая имя класса.</span><span class="sxs-lookup"><span data-stu-id="214cf-127">String that contains a class name.</span></span> <span data-ttu-id="214cf-128">Если этот необязательный параметр указан, то возвращаемые конечные точки должны принадлежать классу, указанному в этом параметре, или быть производным от него.</span><span class="sxs-lookup"><span data-stu-id="214cf-128">If specified, this optional parameter indicates that the returned endpoints must belong to or be derived from the class specified in this parameter.</span></span>

</dd> <dt>

<span data-ttu-id="214cf-129">*стрресултроле* \[ используемых\]</span><span class="sxs-lookup"><span data-stu-id="214cf-129">*strResultRole* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="214cf-130">Строка, содержащая имя свойства.</span><span class="sxs-lookup"><span data-stu-id="214cf-130">String that contains a property name.</span></span> <span data-ttu-id="214cf-131">Если этот параметр указан, он указывает, что возвращаемые конечные точки должны играть определенную роль в связи с исходным объектом.</span><span class="sxs-lookup"><span data-stu-id="214cf-131">If specified, this parameter indicates that the returned endpoints must play a particular role in their association with the source object.</span></span> <span data-ttu-id="214cf-132">Роль определяется именем указанного свойства (которое должно быть ссылочным свойством) ассоциации.</span><span class="sxs-lookup"><span data-stu-id="214cf-132">The role is defined by the name of a specified property (which must be a reference property) of an association.</span></span>

</dd> <dt>

<span data-ttu-id="214cf-133">*strRole* \[ используемых\]</span><span class="sxs-lookup"><span data-stu-id="214cf-133">*strRole* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="214cf-134">Строка, содержащая имя свойства.</span><span class="sxs-lookup"><span data-stu-id="214cf-134">String that contains a property name.</span></span> <span data-ttu-id="214cf-135">Если этот параметр задан, он указывает, что возвращенные конечные точки должны участвовать в связи с исходным объектом, в котором исходный объект играет определенную роль.</span><span class="sxs-lookup"><span data-stu-id="214cf-135">If specified, this parameter indicates that the returned endpoints must participate in an association with the source object in which the source object plays a particular role.</span></span> <span data-ttu-id="214cf-136">Роль определяется именем указанного свойства (которое должно быть ссылочным свойством) ассоциации.</span><span class="sxs-lookup"><span data-stu-id="214cf-136">The role is defined by the name of a specified property (which must be a reference property) of an association.</span></span>

</dd> <dt>

<span data-ttu-id="214cf-137">*бклассесонли* \[ используемых\]</span><span class="sxs-lookup"><span data-stu-id="214cf-137">*bClassesOnly* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="214cf-138">Логическое значение, указывающее, следует ли возвращать список имен классов, а не фактические экземпляры классов.</span><span class="sxs-lookup"><span data-stu-id="214cf-138">Boolean value that indicates whether a list of class names should be returned rather than actual instances of the classes.</span></span> <span data-ttu-id="214cf-139">Это классы, к которым относятся экземпляры конечных точек.</span><span class="sxs-lookup"><span data-stu-id="214cf-139">These are the classes to which the endpoint instances belong.</span></span> <span data-ttu-id="214cf-140">Значение по умолчанию для этого параметра — **false**.</span><span class="sxs-lookup"><span data-stu-id="214cf-140">The default value for this parameter is **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="214cf-141">*бсчемаонли* \[ используемых\]</span><span class="sxs-lookup"><span data-stu-id="214cf-141">*bSchemaOnly* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="214cf-142">Логическое значение, указывающее, применяется ли запрос к схеме, а не к данным.</span><span class="sxs-lookup"><span data-stu-id="214cf-142">Boolean value that indicates whether the query applies to the schema rather than the data.</span></span> <span data-ttu-id="214cf-143">Значение по умолчанию для этого параметра — **false**.</span><span class="sxs-lookup"><span data-stu-id="214cf-143">The default value for this parameter is **FALSE**.</span></span> <span data-ttu-id="214cf-144">Можно задать только **значение true** , если параметр *стробжектпас* указывает путь к объекту класса.</span><span class="sxs-lookup"><span data-stu-id="214cf-144">It can only be set to **TRUE** if the *strObjectPath* parameter specifies the object path of a class.</span></span> <span data-ttu-id="214cf-145">Если задано **значение true**, набор возвращаемых конечных точек представляет классы, которые связаны с исходным классом в схеме.</span><span class="sxs-lookup"><span data-stu-id="214cf-145">When set to **TRUE**, the set of returned endpoints represent classes that are suitably associated with the source class in schema.</span></span>

</dd> <dt>

<span data-ttu-id="214cf-146">*стррекуиредассоккуалифиер* \[ используемых\]</span><span class="sxs-lookup"><span data-stu-id="214cf-146">*strRequiredAssocQualifier* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="214cf-147">Строка, содержащая имя квалификатора.</span><span class="sxs-lookup"><span data-stu-id="214cf-147">String that contains a qualifier name.</span></span> <span data-ttu-id="214cf-148">Если этот параметр указан, он указывает, что возвращенные конечные точки должны быть связаны с исходным объектом через класс ассоциации, включающий указанный квалификатор.</span><span class="sxs-lookup"><span data-stu-id="214cf-148">If specified, this parameter indicates that the returned endpoints must be associated with the source object through an association class that includes the specified qualifier.</span></span>

</dd> <dt>

<span data-ttu-id="214cf-149">*стррекуиредкуалифиер* \[ используемых\]</span><span class="sxs-lookup"><span data-stu-id="214cf-149">*strRequiredQualifier* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="214cf-150">Строка, содержащая имя квалификатора.</span><span class="sxs-lookup"><span data-stu-id="214cf-150">String that contains a qualifier name.</span></span> <span data-ttu-id="214cf-151">Если этот параметр указан, он указывает, что возвращаемые конечные точки должны включать указанный квалификатор.</span><span class="sxs-lookup"><span data-stu-id="214cf-151">If specified, this parameter indicates that the returned endpoints must include the specified qualifier.</span></span>

</dd> <dt>

<span data-ttu-id="214cf-152">*ифлагс* \[ используемых\]</span><span class="sxs-lookup"><span data-stu-id="214cf-152">*iFlags* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="214cf-153">Целое число, указывающее дополнительные флаги для операции.</span><span class="sxs-lookup"><span data-stu-id="214cf-153">Integer that specifies the additional flags to the operation.</span></span> <span data-ttu-id="214cf-154">Значение по умолчанию для этого параметра — **вбемфлагдонтсендстатус**.</span><span class="sxs-lookup"><span data-stu-id="214cf-154">The default for this parameter is **wbemFlagDontSendStatus**.</span></span> <span data-ttu-id="214cf-155">Этот параметр может принимать следующие значения.</span><span class="sxs-lookup"><span data-stu-id="214cf-155">This parameter can accept the following values.</span></span>

<dt>

<span id="wbemFlagSendStatus"></span><span id="wbemflagsendstatus"></span><span id="WBEMFLAGSENDSTATUS"></span>

<span data-ttu-id="214cf-156"><span id="wbemFlagSendStatus"></span><span id="wbemflagsendstatus"></span><span id="WBEMFLAGSENDSTATUS"></span>Вбемфлагсендстатус \* \* \* \* (128 (0x80))</span><span class="sxs-lookup"><span data-stu-id="214cf-156"><span id="wbemFlagSendStatus"></span><span id="wbemflagsendstatus"></span><span id="WBEMFLAGSENDSTATUS"></span>\*\*\*\*wbemFlagSendStatus\*\*\*\* (128 (0x80))</span></span>


</dt> <dd>

<span data-ttu-id="214cf-157">Вызывает асинхронные вызовы для отправки обновлений состояния обработчику событий [**OnProgress**](swbemsink-onprogress.md) для приемника объекта.</span><span class="sxs-lookup"><span data-stu-id="214cf-157">Causes asynchronous calls to send status updates to the [**OnProgress**](swbemsink-onprogress.md) event handler for the object sink.</span></span>

</dd> <dt>

<span id="wbemFlagDontSendStatus"></span><span id="wbemflagdontsendstatus"></span><span id="WBEMFLAGDONTSENDSTATUS"></span>

<span data-ttu-id="214cf-158"><span id="wbemFlagDontSendStatus"></span><span id="wbemflagdontsendstatus"></span><span id="WBEMFLAGDONTSENDSTATUS"></span>Вбемфлагдонтсендстатус \* \* \* \* (0 (0x0))</span><span class="sxs-lookup"><span data-stu-id="214cf-158"><span id="wbemFlagDontSendStatus"></span><span id="wbemflagdontsendstatus"></span><span id="WBEMFLAGDONTSENDSTATUS"></span>\*\*\*\*wbemFlagDontSendStatus\*\*\*\* (0 (0x0))</span></span>


</dt> <dd>

<span data-ttu-id="214cf-159">Не позволяет асинхронным вызовам отправлять обновления состояния в обработчик событий [**OnProgress**](swbemsink-onprogress.md) для приемника объекта.</span><span class="sxs-lookup"><span data-stu-id="214cf-159">Prevents asynchronous calls from sending status updates to the [**OnProgress**](swbemsink-onprogress.md) event handler for the object sink.</span></span>

</dd> <dt>

<span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>

<span data-ttu-id="214cf-160"><span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>Вбемфлагусеамендедкуалифиерс \* \* \* \* (131072 (0x20000))</span><span class="sxs-lookup"><span data-stu-id="214cf-160"><span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>\*\*\*\*wbemFlagUseAmendedQualifiers\*\*\*\* (131072 (0x20000))</span></span>


</dt> <dd>

<span data-ttu-id="214cf-161">Заставляет Инструментарий WMI возвращать данные о поправности классов вместе с определением базового класса.</span><span class="sxs-lookup"><span data-stu-id="214cf-161">Causes WMI to return class amendment data along with the base class definition.</span></span> <span data-ttu-id="214cf-162">Дополнительные сведения об измененных квалификаторах см. в разделе [Локализация сведений о классе WMI](localizing-wmi-class-information.md).</span><span class="sxs-lookup"><span data-stu-id="214cf-162">For more information about amended qualifiers, see [Localizing WMI Class Information](localizing-wmi-class-information.md).</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="214cf-163">*обжвбемнамедвалуесет* \[ используемых\]</span><span class="sxs-lookup"><span data-stu-id="214cf-163">*objWbemNamedValueSet* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="214cf-164">Как правило, это не определено.</span><span class="sxs-lookup"><span data-stu-id="214cf-164">Typically, this is undefined.</span></span> <span data-ttu-id="214cf-165">В противном случае это объект [**свбемнамедвалуесет**](swbemnamedvalueset.md) , элементы которого представляют сведения о контексте, которые могут использоваться поставщиком, обслуживающим запрос.</span><span class="sxs-lookup"><span data-stu-id="214cf-165">Otherwise, this is an [**SWbemNamedValueSet**](swbemnamedvalueset.md) object whose elements represent the context information that can be used by the provider that is servicing the request.</span></span> <span data-ttu-id="214cf-166">Поставщик, который поддерживает или требует такую информацию, должен документировать распознанные имена значений, тип данных значения, допустимые значения и семантику.</span><span class="sxs-lookup"><span data-stu-id="214cf-166">A provider that supports or requires such information must document the recognized value names, data type of the value, allowed values, and semantics.</span></span>

</dd> <dt>

<span data-ttu-id="214cf-167">*обжвбемасинкконтекст* \[ используемых\]</span><span class="sxs-lookup"><span data-stu-id="214cf-167">*objWbemAsyncContext* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="214cf-168">Объект [**свбемнамедвалуесет**](swbemnamedvalueset.md) , возвращающий приемник объекта для обнаружения источника исходного асинхронного вызова.</span><span class="sxs-lookup"><span data-stu-id="214cf-168">An [**SWbemNamedValueSet**](swbemnamedvalueset.md) object that returns to the object sink to identify the source of the original asynchronous call.</span></span> <span data-ttu-id="214cf-169">Используйте этот параметр, если вы выполняете несколько асинхронных вызовов, использующих один и тот же приемник объекта.</span><span class="sxs-lookup"><span data-stu-id="214cf-169">Use this parameter if you are making multiple asynchronous calls using the same object sink.</span></span> <span data-ttu-id="214cf-170">Чтобы использовать этот параметр, создайте объект **свбемнамедвалуесет** и используйте метод [**свбемнамедвалуесет. Add**](swbemnamedvalueset-add.md) , чтобы добавить значение, идентифицирующее выполняемый асинхронный вызов.</span><span class="sxs-lookup"><span data-stu-id="214cf-170">To use this parameter, create an **SWbemNamedValueSet** object and use the [**SWbemNamedValueSet.Add**](swbemnamedvalueset-add.md) method to add a value that identifies the asynchronous call you are making.</span></span> <span data-ttu-id="214cf-171">Этот объект **свбемнамедвалуесет** возвращается в приемник объекта, и источник вызова можно извлечь с помощью метода [**свбемнамедвалуесет. Item**](swbemnamedvalueset-item.md) .</span><span class="sxs-lookup"><span data-stu-id="214cf-171">This **SWbemNamedValueSet** object is returned to the object sink and the source of the call can be extracted using the [**SWbemNamedValueSet.Item**](swbemnamedvalueset-item.md) method.</span></span> <span data-ttu-id="214cf-172">Дополнительные сведения см. [в разделе вызов метода](calling-a-method.md).</span><span class="sxs-lookup"><span data-stu-id="214cf-172">For more information, see [Calling a Method](calling-a-method.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="214cf-173">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="214cf-173">Return value</span></span>

<span data-ttu-id="214cf-174">Этот метод не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="214cf-174">This method does not return a value.</span></span> <span data-ttu-id="214cf-175">В случае успешного выполнения приемник получает событие [**онобжектреади**](swbemsink-onobjectready.md) для каждого экземпляра.</span><span class="sxs-lookup"><span data-stu-id="214cf-175">If successful, the sink receives an [**OnObjectReady**](swbemsink-onobjectready.md) event per instance.</span></span> <span data-ttu-id="214cf-176">После последнего экземпляра приемник объекта получает событие [**Oncompleteed**](swbemsink-oncompleted.md) .</span><span class="sxs-lookup"><span data-stu-id="214cf-176">After the last instance, the object sink receives an [**OnCompleted**](swbemsink-oncompleted.md) event.</span></span>

## <a name="error-codes"></a><span data-ttu-id="214cf-177">Коды ошибок</span><span class="sxs-lookup"><span data-stu-id="214cf-177">Error codes</span></span>

<span data-ttu-id="214cf-178">После завершения метода **ассоЦиаторсофасинк** объект [Err](/previous-versions//sbf5ze0e(v=vs.85)) может содержать один из кодов ошибок из следующего списка.</span><span class="sxs-lookup"><span data-stu-id="214cf-178">After the completion of the **AssociatorsOfAsync** method, the [Err](/previous-versions//sbf5ze0e(v=vs.85)) object may contain one of the error codes in the following list.</span></span>

<dl> <dt>

<span data-ttu-id="214cf-179">**вбемерракцессдениед** -2147749891 (0x80041003)</span><span class="sxs-lookup"><span data-stu-id="214cf-179">**wbemErrAccessDenied** - 2147749891 (0x80041003)</span></span>
</dt> <dd>

<span data-ttu-id="214cf-180">У текущего пользователя нет разрешения на просмотр одного или нескольких классов, возвращенных вызовом.</span><span class="sxs-lookup"><span data-stu-id="214cf-180">Current user does not have the permission to view one or more of the classes returned by the call.</span></span>

</dd> <dt>

<span data-ttu-id="214cf-181">**вбемеррфаилед** -2147749889 (0x80041001)</span><span class="sxs-lookup"><span data-stu-id="214cf-181">**wbemErrFailed** - 2147749889 (0x80041001)</span></span>
</dt> <dd>

<span data-ttu-id="214cf-182">Незаданная ошибка.</span><span class="sxs-lookup"><span data-stu-id="214cf-182">Unspecified error.</span></span>

</dd> <dt>

<span data-ttu-id="214cf-183">**вбемерринвалидпараметер** -2147749896 (0x80041008)</span><span class="sxs-lookup"><span data-stu-id="214cf-183">**wbemErrInvalidParameter** - 2147749896 (0x80041008)</span></span>
</dt> <dd>

<span data-ttu-id="214cf-184">Указан недопустимый параметр.</span><span class="sxs-lookup"><span data-stu-id="214cf-184">Invalid parameter was specified.</span></span>

</dd> <dt>

<span data-ttu-id="214cf-185">**вбемерраутофмемори** -2147749894 (0x80041006)</span><span class="sxs-lookup"><span data-stu-id="214cf-185">**wbemErrOutOfMemory** - 2147749894 (0x80041006)</span></span>
</dt> <dd>

<span data-ttu-id="214cf-186">Недостаточно памяти для завершения операции.</span><span class="sxs-lookup"><span data-stu-id="214cf-186">Not enough memory to complete the operation.</span></span>

</dd> <dt>

<span data-ttu-id="214cf-187">**вбемеррнотфаунд** -2147749890 (0x80041002)</span><span class="sxs-lookup"><span data-stu-id="214cf-187">**wbemErrNotFound** - 2147749890 (0x80041002)</span></span>
</dt> <dd>

<span data-ttu-id="214cf-188">Запрошенный элемент не найден.</span><span class="sxs-lookup"><span data-stu-id="214cf-188">Requested item was not found.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="214cf-189">Remarks</span><span class="sxs-lookup"><span data-stu-id="214cf-189">Remarks</span></span>

<span data-ttu-id="214cf-190">Этот вызов возвращает немедленно.</span><span class="sxs-lookup"><span data-stu-id="214cf-190">This call returns immediately.</span></span> <span data-ttu-id="214cf-191">Запрошенные объекты и состояние возвращаются вызывающему объекту через обратные вызовы, доставляемые в приемник, указанный в *обжвбемсинк*.</span><span class="sxs-lookup"><span data-stu-id="214cf-191">The requested objects and status are returned to the caller through callbacks delivered to the sink that is specified in *objWbemSink*.</span></span> <span data-ttu-id="214cf-192">Чтобы обработать каждый объект при его возврате, создайте *обжвбемсинк*. Подпрограммы события [**онобжектреади**](swbemsink-onobjectready.md) .</span><span class="sxs-lookup"><span data-stu-id="214cf-192">To process each object when it returns, create an *objWbemSink*.[**OnObjectReady**](swbemsink-onobjectready.md) event subroutine.</span></span> <span data-ttu-id="214cf-193">После возврата всех объектов можно выполнить окончательную обработку в реализации *обжвбемсинк*. Событие [**Oncompleteed**](swbemsink-oncompleted.md) .</span><span class="sxs-lookup"><span data-stu-id="214cf-193">After all the objects are returned, you can perform final processing in your implementation of the *objWbemSink*.[**OnCompleted**](swbemsink-oncompleted.md) event.</span></span>

<span data-ttu-id="214cf-194">Асинхронный обратный вызов позволяет пользователю без проверки подлинности предоставлять данные в приемник.</span><span class="sxs-lookup"><span data-stu-id="214cf-194">An asynchronous callback allows a non-authenticated user to provide data to the sink.</span></span> <span data-ttu-id="214cf-195">Это создает угрозы безопасности для сценариев и приложений.</span><span class="sxs-lookup"><span data-stu-id="214cf-195">This poses security risks to your scripts and applications.</span></span> <span data-ttu-id="214cf-196">Сведения об устранении рисков см. в разделе [Настройка безопасности при асинхронном вызове](setting-security-on-an-asynchronous-call.md).</span><span class="sxs-lookup"><span data-stu-id="214cf-196">To eliminate the risks, see [Setting Security on an Asynchronous Call](setting-security-on-an-asynchronous-call.md).</span></span>

<span data-ttu-id="214cf-197">Используйте параметр *обжвбемасинкконтекст* в скриптах для проверки источника вызова.</span><span class="sxs-lookup"><span data-stu-id="214cf-197">Use the *objWbemAsyncContext* parameter in scripts to verify the source of a call.</span></span>

## <a name="requirements"></a><span data-ttu-id="214cf-198">Требования</span><span class="sxs-lookup"><span data-stu-id="214cf-198">Requirements</span></span>



| <span data-ttu-id="214cf-199">Требование</span><span class="sxs-lookup"><span data-stu-id="214cf-199">Requirement</span></span> | <span data-ttu-id="214cf-200">Значение</span><span class="sxs-lookup"><span data-stu-id="214cf-200">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="214cf-201">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="214cf-201">Minimum supported client</span></span><br/> | <span data-ttu-id="214cf-202">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="214cf-202">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="214cf-203">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="214cf-203">Minimum supported server</span></span><br/> | <span data-ttu-id="214cf-204">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="214cf-204">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="214cf-205">Header</span><span class="sxs-lookup"><span data-stu-id="214cf-205">Header</span></span><br/>                   | <dl> <span data-ttu-id="214cf-206"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="214cf-206"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="214cf-207">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="214cf-207">Type library</span></span><br/>             | <dl> <span data-ttu-id="214cf-208"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="214cf-208"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="214cf-209">DLL</span><span class="sxs-lookup"><span data-stu-id="214cf-209">DLL</span></span><br/>                      | <dl> <span data-ttu-id="214cf-210"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="214cf-210"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="214cf-211">CLSID</span><span class="sxs-lookup"><span data-stu-id="214cf-211">CLSID</span></span><br/>                    | <span data-ttu-id="214cf-212">\_SWBEMSERVICES CLSID</span><span class="sxs-lookup"><span data-stu-id="214cf-212">CLSID\_SWbemServices</span></span><br/>                                                         |
| <span data-ttu-id="214cf-213">IID</span><span class="sxs-lookup"><span data-stu-id="214cf-213">IID</span></span><br/>                      | <span data-ttu-id="214cf-214">IID \_ исвбемсервицес</span><span class="sxs-lookup"><span data-stu-id="214cf-214">IID\_ISWbemServices</span></span><br/>                                                          |



## <a name="see-also"></a><span data-ttu-id="214cf-215">См. также</span><span class="sxs-lookup"><span data-stu-id="214cf-215">See also</span></span>

<dl> <dt>

[<span data-ttu-id="214cf-216">**SWbemServices**</span><span class="sxs-lookup"><span data-stu-id="214cf-216">**SWbemServices**</span></span>](swbemservices.md)
</dt> <dt>

[<span data-ttu-id="214cf-217">**SWbemObject. соединители\_**</span><span class="sxs-lookup"><span data-stu-id="214cf-217">**SWbemObject.Associators\_**</span></span>](swbemobject-associators-.md)
</dt> <dt>

[<span data-ttu-id="214cf-218">**SWbemObject. АссоЦиаторсасинк\_**</span><span class="sxs-lookup"><span data-stu-id="214cf-218">**SWbemObject.AssociatorsAsync\_**</span></span>](swbemobject-associatorsasync-.md)
</dt> <dt>

[<span data-ttu-id="214cf-219">**SWbemObject. References\_**</span><span class="sxs-lookup"><span data-stu-id="214cf-219">**SWbemObject.References\_**</span></span>](swbemobject-references-.md)
</dt> <dt>

[<span data-ttu-id="214cf-220">**SWbemObject. Референцесасинк\_**</span><span class="sxs-lookup"><span data-stu-id="214cf-220">**SWbemObject.ReferencesAsync\_**</span></span>](swbemobject-referencesasync-.md)
</dt> <dt>

[<span data-ttu-id="214cf-221">**SWbemServices. Референцесто**</span><span class="sxs-lookup"><span data-stu-id="214cf-221">**SWbemServices.ReferencesTo**</span></span>](swbemservices-referencesto.md)
</dt> <dt>

[<span data-ttu-id="214cf-222">**SWbemServices. Референцестоасинк**</span><span class="sxs-lookup"><span data-stu-id="214cf-222">**SWbemServices.ReferencesToAsync**</span></span>](swbemservices-referencestoasync.md)
</dt> </dl>

 

