---
description: SWbemServices. АссоЦиаторсоф, метод возвращает коллекцию объектов (классов или экземпляров), называемых конечными точками, которые связаны с указанным объектом.
ms.assetid: a78e6701-6779-4a02-b811-23b2da4f4167
ms.tgt_platform: multiple
title: SWbemServices. АссоЦиаторсоф, метод (Wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemServices.AssociatorsOf
- ISWbemServices.AssociatorsOf
- ISWbemServices.AssociatorsOf
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 95dc8e16939c345b6f885980dd2f1194f180ac5e
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108103692"
---
# <a name="swbemservicesassociatorsof-method"></a><span data-ttu-id="fe16c-103">SWbemServices. АссоЦиаторсоф, метод</span><span class="sxs-lookup"><span data-stu-id="fe16c-103">SWbemServices.AssociatorsOf method</span></span>

<span data-ttu-id="fe16c-104">Метод **ассоЦиаторсоф** объекта [**SwbemServices**](swbemservices.md) Возвращает коллекцию объектов (классов или экземпляров), называемых конечными точками, которые связаны с указанным объектом.</span><span class="sxs-lookup"><span data-stu-id="fe16c-104">The **AssociatorsOf** method of the [**SWbemServices**](swbemservices.md) object returns a collection of objects (classes or instances) called endpoints that are associated with a specified object.</span></span> <span data-ttu-id="fe16c-105">Этот метод выполняет ту же функцию, что и СОЕДИНИТЕЛи WQL-запроса.</span><span class="sxs-lookup"><span data-stu-id="fe16c-105">This method performs the same function that the ASSOCIATORS OF WQL query performs.</span></span>

<span data-ttu-id="fe16c-106">Этот метод по умолчанию вызывается в режиме семисинчронаус.</span><span class="sxs-lookup"><span data-stu-id="fe16c-106">This method is called in the semisynchronous mode by default.</span></span> <span data-ttu-id="fe16c-107">Дополнительные сведения см. [в разделе вызов метода](calling-a-method.md).</span><span class="sxs-lookup"><span data-stu-id="fe16c-107">For more information, see [Calling a Method](calling-a-method.md).</span></span>

<span data-ttu-id="fe16c-108">Описание этого синтаксиса см. в разделе [соглашения о документе для API скриптов](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="fe16c-108">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="fe16c-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="fe16c-109">Syntax</span></span>


```VB
objWbemObjectSet = .AssociatorsOf( _
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
  [ ByVal objwbemNamedValueSet ] _
)
```



## <a name="parameters"></a><span data-ttu-id="fe16c-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="fe16c-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fe16c-111">*стробжектпас*</span><span class="sxs-lookup"><span data-stu-id="fe16c-111">*strObjectPath*</span></span> 
</dt> <dd>

<span data-ttu-id="fe16c-112">Обязательный элемент.</span><span class="sxs-lookup"><span data-stu-id="fe16c-112">Required.</span></span> <span data-ttu-id="fe16c-113">Строка, содержащая путь к объекту исходного класса или экземпляра.</span><span class="sxs-lookup"><span data-stu-id="fe16c-113">String that contains the object path of the source class or instance.</span></span> <span data-ttu-id="fe16c-114">Дополнительные сведения см. [в разделе Описание расположения объекта WMI](describing-the-location-of-a-wmi-object.md).</span><span class="sxs-lookup"><span data-stu-id="fe16c-114">For more information, see [Describing the Location of a WMI Object](describing-the-location-of-a-wmi-object.md).</span></span>

</dd> <dt>

<span data-ttu-id="fe16c-115">*страссоккласс* \[ используемых\]</span><span class="sxs-lookup"><span data-stu-id="fe16c-115">*strAssocClass* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="fe16c-116">Строка, содержащая класс ассоциации.</span><span class="sxs-lookup"><span data-stu-id="fe16c-116">String that contains an association class.</span></span> <span data-ttu-id="fe16c-117">Если этот параметр указан, он указывает, что возвращенные конечные точки должны быть связаны с источником через указанный класс ассоциации или класс, производный от этого класса ассоциации.</span><span class="sxs-lookup"><span data-stu-id="fe16c-117">If specified, this parameter indicates that the returned endpoints must be associated with the source through the specified association class or a class that is derived from this association class.</span></span>

</dd> <dt>

<span data-ttu-id="fe16c-118">*стрресулткласс* \[ используемых\]</span><span class="sxs-lookup"><span data-stu-id="fe16c-118">*strResultClass* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="fe16c-119">Строка, содержащая имя класса.</span><span class="sxs-lookup"><span data-stu-id="fe16c-119">String that contains a class name.</span></span> <span data-ttu-id="fe16c-120">Если этот необязательный параметр указан, то возвращаемые конечные точки должны принадлежать классу, указанному в этом параметре, или быть производным от него.</span><span class="sxs-lookup"><span data-stu-id="fe16c-120">If specified, this optional parameter indicates that the returned endpoints must belong to or be derived from the class specified in this parameter.</span></span>

</dd> <dt>

<span data-ttu-id="fe16c-121">*стрресултроле* \[ используемых\]</span><span class="sxs-lookup"><span data-stu-id="fe16c-121">*strResultRole* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="fe16c-122">Строка, содержащая имя свойства.</span><span class="sxs-lookup"><span data-stu-id="fe16c-122">String that contains a property name.</span></span> <span data-ttu-id="fe16c-123">Если этот параметр указан, он указывает, что возвращаемые конечные точки должны играть определенную роль в связи с исходным объектом.</span><span class="sxs-lookup"><span data-stu-id="fe16c-123">If specified, this parameter indicates that the returned endpoints must play a particular role in their association with the source object.</span></span> <span data-ttu-id="fe16c-124">Роль определяется именем указанного свойства (которое должно быть ссылочным свойством) ассоциации.</span><span class="sxs-lookup"><span data-stu-id="fe16c-124">The role is defined by the name of a specified property (which must be a reference property) of an association.</span></span>

</dd> <dt>

<span data-ttu-id="fe16c-125">*strRole* \[ используемых\]</span><span class="sxs-lookup"><span data-stu-id="fe16c-125">*strRole* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="fe16c-126">Строка, содержащая имя свойства.</span><span class="sxs-lookup"><span data-stu-id="fe16c-126">String that contains a property name.</span></span> <span data-ttu-id="fe16c-127">Если этот параметр задан, он указывает, что возвращенные конечные точки должны участвовать в связи с исходным объектом, в котором исходный объект играет определенную роль.</span><span class="sxs-lookup"><span data-stu-id="fe16c-127">If specified, this parameter indicates that the returned endpoints must participate in an association with the source object in which the source object plays a particular role.</span></span> <span data-ttu-id="fe16c-128">Роль определяется именем указанного свойства (которое должно быть ссылочным свойством) ассоциации.</span><span class="sxs-lookup"><span data-stu-id="fe16c-128">The role is defined by the name of a specified property (which must be a reference property) of an association.</span></span>

</dd> <dt>

<span data-ttu-id="fe16c-129">*бклассесонли* \[ используемых\]</span><span class="sxs-lookup"><span data-stu-id="fe16c-129">*bClassesOnly* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="fe16c-130">Логическое значение, указывающее, следует ли возвращать список имен классов, а не фактические экземпляры классов.</span><span class="sxs-lookup"><span data-stu-id="fe16c-130">Boolean value that indicates whether a list of class names should be returned rather than actual instances of the classes.</span></span> <span data-ttu-id="fe16c-131">Это классы, к которым относятся экземпляры конечных точек.</span><span class="sxs-lookup"><span data-stu-id="fe16c-131">These are the classes to which the endpoint instances belong.</span></span> <span data-ttu-id="fe16c-132">Значение по умолчанию для этого параметра — **false**.</span><span class="sxs-lookup"><span data-stu-id="fe16c-132">The default value for this parameter is **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="fe16c-133">*бсчемаонли* \[ используемых\]</span><span class="sxs-lookup"><span data-stu-id="fe16c-133">*bSchemaOnly* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="fe16c-134">Логическое значение, указывающее, применяется ли запрос к схеме, а не к данным.</span><span class="sxs-lookup"><span data-stu-id="fe16c-134">Boolean value that indicates whether the query applies to the schema rather than the data.</span></span> <span data-ttu-id="fe16c-135">Значение по умолчанию для этого параметра — **false**.</span><span class="sxs-lookup"><span data-stu-id="fe16c-135">The default value for this parameter is **FALSE**.</span></span> <span data-ttu-id="fe16c-136">Можно задать только **значение true** , если параметр *стробжектпас* указывает путь к объекту класса.</span><span class="sxs-lookup"><span data-stu-id="fe16c-136">It can only be set to **TRUE** if the *strObjectPath* parameter specifies the object path of a class.</span></span> <span data-ttu-id="fe16c-137">Если задано **значение true**, набор возвращаемых конечных точек представляет классы, которые связаны с исходным классом в схеме.</span><span class="sxs-lookup"><span data-stu-id="fe16c-137">When set to **TRUE**, the set of returned endpoints represent classes that are suitably associated with the source class in schema.</span></span>

</dd> <dt>

<span data-ttu-id="fe16c-138">*стррекуиредассоккуалифиер* \[ используемых\]</span><span class="sxs-lookup"><span data-stu-id="fe16c-138">*strRequiredAssocQualifier* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="fe16c-139">Строка, содержащая имя квалификатора.</span><span class="sxs-lookup"><span data-stu-id="fe16c-139">String that contains a qualifier name.</span></span> <span data-ttu-id="fe16c-140">Если этот параметр указан, он указывает, что возвращенные конечные точки должны быть связаны с исходным объектом через класс ассоциации, включающий указанный квалификатор.</span><span class="sxs-lookup"><span data-stu-id="fe16c-140">If specified, this parameter indicates that the returned endpoints must be associated with the source object through an association class that includes the specified qualifier.</span></span>

</dd> <dt>

<span data-ttu-id="fe16c-141">*стррекуиредкуалифиер* \[ используемых\]</span><span class="sxs-lookup"><span data-stu-id="fe16c-141">*strRequiredQualifier* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="fe16c-142">Строка, содержащая имя квалификатора.</span><span class="sxs-lookup"><span data-stu-id="fe16c-142">String that contains a qualifier name.</span></span> <span data-ttu-id="fe16c-143">Если этот параметр указан, он указывает, что возвращаемые конечные точки должны включать указанный квалификатор.</span><span class="sxs-lookup"><span data-stu-id="fe16c-143">If specified, this parameter indicates that the returned endpoints must include the specified qualifier.</span></span>

</dd> <dt>

<span data-ttu-id="fe16c-144">*ифлагс* \[ используемых\]</span><span class="sxs-lookup"><span data-stu-id="fe16c-144">*iFlags* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="fe16c-145">Целое число, задающее дополнительные флаги для операции.</span><span class="sxs-lookup"><span data-stu-id="fe16c-145">Integer that specifies additional flags to the operation.</span></span> <span data-ttu-id="fe16c-146">Значение по умолчанию для этого параметра — **вбемфлагретурниммедиатели**, которое вызывает метод в режиме семисинчронаус.</span><span class="sxs-lookup"><span data-stu-id="fe16c-146">The default value for this parameter is **wbemFlagReturnImmediately**, which calls the method in the semisynchronous mode.</span></span> <span data-ttu-id="fe16c-147">Этот параметр может принимать следующие значения.</span><span class="sxs-lookup"><span data-stu-id="fe16c-147">This parameter can accept the following values.</span></span>

<dt>

<span id="wbemFlagForwardOnly"></span><span id="wbemflagforwardonly"></span><span id="WBEMFLAGFORWARDONLY"></span>

<span data-ttu-id="fe16c-148"><span id="wbemFlagForwardOnly"></span><span id="wbemflagforwardonly"></span><span id="WBEMFLAGFORWARDONLY"></span>Вбемфлагфорвардонли \* \* \* \* (32 (0x20))</span><span class="sxs-lookup"><span data-stu-id="fe16c-148"><span id="wbemFlagForwardOnly"></span><span id="wbemflagforwardonly"></span><span id="WBEMFLAGFORWARDONLY"></span>\*\*\*\*wbemFlagForwardOnly\*\*\*\* (32 (0x20))</span></span>


</dt> <dd>

<span data-ttu-id="fe16c-149">Вызывает возврат перечислителя "только вперед".</span><span class="sxs-lookup"><span data-stu-id="fe16c-149">Causes a forward-only enumerator to be returned.</span></span> <span data-ttu-id="fe16c-150">Перечислители "только вперед" обычно выполняются гораздо быстрее и используют меньше памяти, чем обычные перечислители, но они не допускают вызовов [**SWbemObject. Clone \_**](swbemobject-clone-.md).</span><span class="sxs-lookup"><span data-stu-id="fe16c-150">Forward-only enumerators are generally much faster and use less memory than conventional enumerators, but they do not allow calls to [**SWbemObject.Clone\_**](swbemobject-clone-.md).</span></span>

</dd> <dt>

<span id="wbemFlagBidirectional"></span><span id="wbemflagbidirectional"></span><span id="WBEMFLAGBIDIRECTIONAL"></span>

<span data-ttu-id="fe16c-151"><span id="wbemFlagBidirectional"></span><span id="wbemflagbidirectional"></span><span id="WBEMFLAGBIDIRECTIONAL"></span>Вбемфлагбидиректионал \* \* \* \* (0 (0x0))</span><span class="sxs-lookup"><span data-stu-id="fe16c-151"><span id="wbemFlagBidirectional"></span><span id="wbemflagbidirectional"></span><span id="WBEMFLAGBIDIRECTIONAL"></span>\*\*\*\*wbemFlagBidirectional\*\*\*\* (0 (0x0))</span></span>


</dt> <dd>

<span data-ttu-id="fe16c-152">Заставляет Инструментарий WMI хранить указатели на объекты перечисления до тех пор, пока клиент не освободит перечислитель.</span><span class="sxs-lookup"><span data-stu-id="fe16c-152">Causes WMI to retain pointers to objects of the enumeration until the client releases the enumerator.</span></span>

</dd> <dt>

<span id="wbemFlagReturnImmediately"></span><span id="wbemflagreturnimmediately"></span><span id="WBEMFLAGRETURNIMMEDIATELY"></span>

<span data-ttu-id="fe16c-153"><span id="wbemFlagReturnImmediately"></span><span id="wbemflagreturnimmediately"></span><span id="WBEMFLAGRETURNIMMEDIATELY"></span>Вбемфлагретурниммедиатели \* \* \* \* (16 (0x10))</span><span class="sxs-lookup"><span data-stu-id="fe16c-153"><span id="wbemFlagReturnImmediately"></span><span id="wbemflagreturnimmediately"></span><span id="WBEMFLAGRETURNIMMEDIATELY"></span>\*\*\*\*wbemFlagReturnImmediately\*\*\*\* (16 (0x10))</span></span>


</dt> <dd>

<span data-ttu-id="fe16c-154">Приводит к немедленному возврату вызова.</span><span class="sxs-lookup"><span data-stu-id="fe16c-154">Causes the call to return immediately.</span></span>

</dd> <dt>

<span id="wbemFlagReturnWhenComplete"></span><span id="wbemflagreturnwhencomplete"></span><span id="WBEMFLAGRETURNWHENCOMPLETE"></span>

<span data-ttu-id="fe16c-155"><span id="wbemFlagReturnWhenComplete"></span><span id="wbemflagreturnwhencomplete"></span><span id="WBEMFLAGRETURNWHENCOMPLETE"></span>Вбемфлагретурнвхенкомплете \* \* \* \* (0 (0x0))</span><span class="sxs-lookup"><span data-stu-id="fe16c-155"><span id="wbemFlagReturnWhenComplete"></span><span id="wbemflagreturnwhencomplete"></span><span id="WBEMFLAGRETURNWHENCOMPLETE"></span>\*\*\*\*wbemFlagReturnWhenComplete\*\*\*\* (0 (0x0))</span></span>


</dt> <dd>

<span data-ttu-id="fe16c-156">Вызывает блокирование этого вызова до тех пор, пока запрос не будет завершен.</span><span class="sxs-lookup"><span data-stu-id="fe16c-156">Causes this call to block until the query has completed.</span></span> <span data-ttu-id="fe16c-157">Этот флаг вызывает метод в синхронном режиме.</span><span class="sxs-lookup"><span data-stu-id="fe16c-157">This flag calls the method in synchronous mode.</span></span>

</dd> <dt>

<span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>

<span data-ttu-id="fe16c-158"><span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>Вбемфлагусеамендедкуалифиерс \* \* \* \* (131072 (0x20000))</span><span class="sxs-lookup"><span data-stu-id="fe16c-158"><span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>\*\*\*\*wbemFlagUseAmendedQualifiers\*\*\*\* (131072 (0x20000))</span></span>


</dt> <dd>

<span data-ttu-id="fe16c-159">Заставляет Инструментарий WMI возвращать данные о поправности классов вместе с определением базового класса.</span><span class="sxs-lookup"><span data-stu-id="fe16c-159">Causes WMI to return class amendment data along with the base class definition.</span></span> <span data-ttu-id="fe16c-160">Дополнительные сведения см. в разделе [Локализация сведений о классе WMI](localizing-wmi-class-information.md).</span><span class="sxs-lookup"><span data-stu-id="fe16c-160">For more information, see [Localizing WMI Class Information](localizing-wmi-class-information.md).</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="fe16c-161">*обжвбемнамедвалуесет* \[ используемых\]</span><span class="sxs-lookup"><span data-stu-id="fe16c-161">*objwbemNamedValueSet* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="fe16c-162">Как правило, это не определено.</span><span class="sxs-lookup"><span data-stu-id="fe16c-162">Typically, this is undefined.</span></span> <span data-ttu-id="fe16c-163">В противном случае это объект [**свбемнамедвалуесет**](swbemnamedvalueset.md) , элементы которого представляют сведения о контексте, которые могут использоваться поставщиком, обслуживающим запрос.</span><span class="sxs-lookup"><span data-stu-id="fe16c-163">Otherwise, this is an [**SWbemNamedValueSet**](swbemnamedvalueset.md) object whose elements represent the context information that can be used by the provider that is servicing the request.</span></span> <span data-ttu-id="fe16c-164">Поставщик, который поддерживает или требует такую информацию, должен документировать распознанные имена значений, тип данных значения, допустимые значения и семантику.</span><span class="sxs-lookup"><span data-stu-id="fe16c-164">A provider that supports or requires such information must document the recognized value names, data type of the value, allowed values, and semantics.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fe16c-165">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="fe16c-165">Return value</span></span>

<span data-ttu-id="fe16c-166">Если вызов выполнен успешно, возвращается объект [**SWbemObjectSet**](swbemobjectset.md) .</span><span class="sxs-lookup"><span data-stu-id="fe16c-166">If the call is successful, an [**SWbemObjectSet**](swbemobjectset.md) object is returned.</span></span>

## <a name="error-codes"></a><span data-ttu-id="fe16c-167">Коды ошибок</span><span class="sxs-lookup"><span data-stu-id="fe16c-167">Error codes</span></span>

<span data-ttu-id="fe16c-168">После завершения метода **ассоЦиаторсоф** объект **Err** может содержать один из кодов ошибок из следующего списка.</span><span class="sxs-lookup"><span data-stu-id="fe16c-168">After the completion of the **AssociatorsOf** method, the **Err** object may contain one of the error codes in the following list.</span></span>

> [!Note]  
> <span data-ttu-id="fe16c-169">Возвращенная коллекция с нулевым числом элементов не является ошибкой.</span><span class="sxs-lookup"><span data-stu-id="fe16c-169">A returned collection with zero elements is not an error.</span></span>

 

<dl> <dt>

<span data-ttu-id="fe16c-170">**вбемерракцессдениед** -2147749891 (0x80041003)</span><span class="sxs-lookup"><span data-stu-id="fe16c-170">**wbemErrAccessDenied** - 2147749891 (0x80041003)</span></span>
</dt> <dd>

<span data-ttu-id="fe16c-171">У текущего пользователя нет разрешения на просмотр одного или нескольких классов, возвращенных вызовом.</span><span class="sxs-lookup"><span data-stu-id="fe16c-171">Current user does not have the permission to view one or more of the classes returned by the call.</span></span>

</dd> <dt>

<span data-ttu-id="fe16c-172">**вбемеррфаилед** -2147749889 (0x80041001)</span><span class="sxs-lookup"><span data-stu-id="fe16c-172">**wbemErrFailed** - 2147749889 (0x80041001)</span></span>
</dt> <dd>

<span data-ttu-id="fe16c-173">Незаданная ошибка.</span><span class="sxs-lookup"><span data-stu-id="fe16c-173">Unspecified error.</span></span>

</dd> <dt>

<span data-ttu-id="fe16c-174">**вбемерринвалидпараметер** -2147749896 (0x80041008)</span><span class="sxs-lookup"><span data-stu-id="fe16c-174">**wbemErrInvalidParameter** - 2147749896 (0x80041008)</span></span>
</dt> <dd>

<span data-ttu-id="fe16c-175">Указан недопустимый параметр.</span><span class="sxs-lookup"><span data-stu-id="fe16c-175">Invalid parameter was specified.</span></span>

</dd> <dt>

<span data-ttu-id="fe16c-176">**вбемерраутофмемори** -2147749894 (0x80041006)</span><span class="sxs-lookup"><span data-stu-id="fe16c-176">**wbemErrOutOfMemory** - 2147749894 (0x80041006)</span></span>
</dt> <dd>

<span data-ttu-id="fe16c-177">Недостаточно памяти для завершения операции.</span><span class="sxs-lookup"><span data-stu-id="fe16c-177">Not enough memory to complete the operation.</span></span>

</dd> <dt>

<span data-ttu-id="fe16c-178">**вбемеррнотфаунд** -2147749890 (0x80041002)</span><span class="sxs-lookup"><span data-stu-id="fe16c-178">**wbemErrNotFound** - 2147749890 (0x80041002)</span></span>
</dt> <dd>

<span data-ttu-id="fe16c-179">Запрошенный элемент не найден.</span><span class="sxs-lookup"><span data-stu-id="fe16c-179">Requested item was not found.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="fe16c-180">Remarks</span><span class="sxs-lookup"><span data-stu-id="fe16c-180">Remarks</span></span>

<span data-ttu-id="fe16c-181">Метод извлекает экземпляры управляемых ресурсов, связанные с указанным ресурсом, через один или несколько классов взаимосвязей.</span><span class="sxs-lookup"><span data-stu-id="fe16c-181">The method retrieves the instances of managed resources that are associated with a specified resource through one or more association classes.</span></span> <span data-ttu-id="fe16c-182">Вы предоставляете путь к объекту для исходной конечной точки, а АссоЦиаторсоф возвращает управляемые ресурсы в противоположной конечной точке.</span><span class="sxs-lookup"><span data-stu-id="fe16c-182">You provide the object path for the originating endpoint, and AssociatorsOf returns the managed resources at the opposite endpoint.</span></span> <span data-ttu-id="fe16c-183">Метод АссоЦиаторсоф выполняет ту же функцию, что и СОЕДИНИТЕЛи WQL-запросов.</span><span class="sxs-lookup"><span data-stu-id="fe16c-183">The AssociatorsOf method performs the same function that the ASSOCIATORS OF WQL query performs.</span></span>

<span data-ttu-id="fe16c-184">Дополнительные сведения о СОЕДИНИТЕЛях WQL-запросов, исходных экземпляров и конечных точек см. в разделе [соединители оператора](associators-of-statement.md).</span><span class="sxs-lookup"><span data-stu-id="fe16c-184">For more information about the ASSOCIATORS OF WQL query, source instances, and endpoints, see [ASSOCIATORS OF Statement](associators-of-statement.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="fe16c-185">Требования</span><span class="sxs-lookup"><span data-stu-id="fe16c-185">Requirements</span></span>



| <span data-ttu-id="fe16c-186">Требование</span><span class="sxs-lookup"><span data-stu-id="fe16c-186">Requirement</span></span> | <span data-ttu-id="fe16c-187">Значение</span><span class="sxs-lookup"><span data-stu-id="fe16c-187">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="fe16c-188">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="fe16c-188">Minimum supported client</span></span><br/> | <span data-ttu-id="fe16c-189">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="fe16c-189">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="fe16c-190">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="fe16c-190">Minimum supported server</span></span><br/> | <span data-ttu-id="fe16c-191">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="fe16c-191">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="fe16c-192">Header</span><span class="sxs-lookup"><span data-stu-id="fe16c-192">Header</span></span><br/>                   | <dl> <span data-ttu-id="fe16c-193"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="fe16c-193"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="fe16c-194">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="fe16c-194">Type library</span></span><br/>             | <dl> <span data-ttu-id="fe16c-195"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="fe16c-195"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="fe16c-196">DLL</span><span class="sxs-lookup"><span data-stu-id="fe16c-196">DLL</span></span><br/>                      | <dl> <span data-ttu-id="fe16c-197"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fe16c-197"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="fe16c-198">CLSID</span><span class="sxs-lookup"><span data-stu-id="fe16c-198">CLSID</span></span><br/>                    | <span data-ttu-id="fe16c-199">\_SWBEMSERVICES CLSID</span><span class="sxs-lookup"><span data-stu-id="fe16c-199">CLSID\_SWbemServices</span></span><br/>                                                         |
| <span data-ttu-id="fe16c-200">IID</span><span class="sxs-lookup"><span data-stu-id="fe16c-200">IID</span></span><br/>                      | <span data-ttu-id="fe16c-201">IID \_ исвбемсервицес</span><span class="sxs-lookup"><span data-stu-id="fe16c-201">IID\_ISWbemServices</span></span><br/>                                                          |



## <a name="see-also"></a><span data-ttu-id="fe16c-202">См. также</span><span class="sxs-lookup"><span data-stu-id="fe16c-202">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fe16c-203">**SWbemServices**</span><span class="sxs-lookup"><span data-stu-id="fe16c-203">**SWbemServices**</span></span>](swbemservices.md)
</dt> <dt>

[<span data-ttu-id="fe16c-204">**SWbemObject. соединители\_**</span><span class="sxs-lookup"><span data-stu-id="fe16c-204">**SWbemObject.Associators\_**</span></span>](swbemobject-associators-.md)
</dt> <dt>

[<span data-ttu-id="fe16c-205">**SWbemObject. АссоЦиаторсасинк\_**</span><span class="sxs-lookup"><span data-stu-id="fe16c-205">**SWbemObject.AssociatorsAsync\_**</span></span>](swbemobject-associatorsasync-.md)
</dt> <dt>

[<span data-ttu-id="fe16c-206">**SWbemServices. АссоЦиаторсофасинк**</span><span class="sxs-lookup"><span data-stu-id="fe16c-206">**SWbemServices.AssociatorsOfAsync**</span></span>](swbemservices-associatorsofasync.md)
</dt> <dt>

[<span data-ttu-id="fe16c-207">**SWbemObject. References\_**</span><span class="sxs-lookup"><span data-stu-id="fe16c-207">**SWbemObject.References\_**</span></span>](swbemobject-references-.md)
</dt> <dt>

[<span data-ttu-id="fe16c-208">**SWbemServices. Референцесто**</span><span class="sxs-lookup"><span data-stu-id="fe16c-208">**SWbemServices.ReferencesTo**</span></span>](swbemservices-referencesto.md)
</dt> </dl>

 

 




