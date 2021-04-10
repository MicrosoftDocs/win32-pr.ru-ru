---
description: '\_Метод-соединители объекта SWbemObject Возвращает коллекцию объектов (классов или экземпляров), связанных с текущим объектом.'
ms.assetid: 79f01853-c649-4cbe-b2fa-cff38fb4b733
ms.tgt_platform: multiple
title: Метод SWbemObject.Associators_ (Wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemObject.Associators_
- ISWbemObject.Associators_
- ISWbemObject.Associators_
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 1f9ff4536936661ece54b5bff29e500ce6e98d3f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103999195"
---
# <a name="swbemobjectassociators_-method"></a><span data-ttu-id="863b2-103">SWbemObject. методы сопоставления \_</span><span class="sxs-lookup"><span data-stu-id="863b2-103">SWbemObject.Associators\_ method</span></span>

<span data-ttu-id="863b2-104">Метод- **соединители \_** объекта [**SWbemObject**](swbemobject.md) Возвращает коллекцию объектов (классов или экземпляров), связанных с текущим объектом.</span><span class="sxs-lookup"><span data-stu-id="863b2-104">The **Associators\_** method of the [**SWbemObject**](swbemobject.md) object returns a collection of objects (classes or instances) that are associated with the current object.</span></span> <span data-ttu-id="863b2-105">Эти возвращенные объекты называются конечными точками.</span><span class="sxs-lookup"><span data-stu-id="863b2-105">These returned objects are called endpoints.</span></span> <span data-ttu-id="863b2-106">Этот метод выполняет ту же функцию, что и СОЕДИНИТЕЛи WQL-запроса.</span><span class="sxs-lookup"><span data-stu-id="863b2-106">This method performs the same function that the ASSOCIATORS OF WQL query performs.</span></span>

<span data-ttu-id="863b2-107">Описание этого синтаксиса см. в разделе [соглашения о документе для API скриптов](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="863b2-107">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="863b2-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="863b2-108">Syntax</span></span>


```VB
objWbemObjectSet = .Associators_( _
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



## <a name="parameters"></a><span data-ttu-id="863b2-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="863b2-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="863b2-110">*страссоккласс* \[ в необязательное\]</span><span class="sxs-lookup"><span data-stu-id="863b2-110">*strAssocClass* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="863b2-111">Строка, содержащая класс ассоциации.</span><span class="sxs-lookup"><span data-stu-id="863b2-111">String that contains an association class.</span></span> <span data-ttu-id="863b2-112">Если этот параметр указан, он указывает, что возвращенные конечные точки должны быть связаны с источником через указанный класс ассоциации или класс, производный от этого класса ассоциации.</span><span class="sxs-lookup"><span data-stu-id="863b2-112">If specified, this parameter indicates that the returned endpoints must be associated with the source through the specified association class or a class derived from this association class.</span></span>

</dd> <dt>

<span data-ttu-id="863b2-113">*стрресулткласс* \[ в необязательное\]</span><span class="sxs-lookup"><span data-stu-id="863b2-113">*strResultClass* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="863b2-114">Строка, содержащая имя класса.</span><span class="sxs-lookup"><span data-stu-id="863b2-114">String that contains a class name.</span></span> <span data-ttu-id="863b2-115">Если этот параметр указан, он указывает, что возвращаемые конечные точки должны принадлежать или быть производными от класса, указанного в этом параметре.</span><span class="sxs-lookup"><span data-stu-id="863b2-115">If specified, this parameter indicates that the returned endpoints must belong to or be derived from the class specified in this parameter.</span></span>

</dd> <dt>

<span data-ttu-id="863b2-116">*стрресултроле* \[ в необязательное\]</span><span class="sxs-lookup"><span data-stu-id="863b2-116">*strResultRole* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="863b2-117">Строка, содержащая имя свойства.</span><span class="sxs-lookup"><span data-stu-id="863b2-117">String that contains a property name.</span></span> <span data-ttu-id="863b2-118">Если этот параметр указан, он указывает, что возвращаемые конечные точки должны играть определенную роль в связи с исходным объектом.</span><span class="sxs-lookup"><span data-stu-id="863b2-118">If specified, this parameter indicates that the returned endpoints must play a particular role in their association with the source object.</span></span> <span data-ttu-id="863b2-119">Роль определяется именем указанного свойства (которое должно быть ссылочным свойством) ассоциации.</span><span class="sxs-lookup"><span data-stu-id="863b2-119">The role is defined by the name of a specified property (which must be a reference property) of an association.</span></span>

</dd> <dt>

<span data-ttu-id="863b2-120">*strRole* \[ в необязательное\]</span><span class="sxs-lookup"><span data-stu-id="863b2-120">*strRole* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="863b2-121">Строка, содержащая имя свойства.</span><span class="sxs-lookup"><span data-stu-id="863b2-121">String that contains a property name.</span></span> <span data-ttu-id="863b2-122">Если этот параметр задан, он указывает, что возвращенные конечные точки должны участвовать в связи с исходным объектом, в котором исходный объект играет определенную роль.</span><span class="sxs-lookup"><span data-stu-id="863b2-122">If specified, this parameter indicates that the returned endpoints must participate in an association with the source object in which the source object plays a particular role.</span></span> <span data-ttu-id="863b2-123">Роль определяется именем указанного свойства (которое должно быть ссылочным свойством) ассоциации.</span><span class="sxs-lookup"><span data-stu-id="863b2-123">The role is defined by the name of a specified property (which must be a reference property) of an association.</span></span>

</dd> <dt>

<span data-ttu-id="863b2-124">*бклассесонли* \[ в необязательное\]</span><span class="sxs-lookup"><span data-stu-id="863b2-124">*bClassesOnly* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="863b2-125">Логическое значение, указывающее, следует ли возвращать список имен классов, а не фактические экземпляры классов.</span><span class="sxs-lookup"><span data-stu-id="863b2-125">Boolean value that indicates whether a list of class names should be returned rather than actual instances of the classes.</span></span> <span data-ttu-id="863b2-126">Это классы, к которым относятся экземпляры конечных точек.</span><span class="sxs-lookup"><span data-stu-id="863b2-126">These are the classes to which the endpoint instances belong.</span></span> <span data-ttu-id="863b2-127">Значение по умолчанию для этого параметра — **false**.</span><span class="sxs-lookup"><span data-stu-id="863b2-127">The default value for this parameter is **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="863b2-128">*бсчемаонли* \[ в необязательное\]</span><span class="sxs-lookup"><span data-stu-id="863b2-128">*bSchemaOnly* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="863b2-129">Это логическое значение, указывающее, применяется ли запрос к схеме, а не к данным.</span><span class="sxs-lookup"><span data-stu-id="863b2-129">This is a Boolean value that indicates whether the query applies to the schema rather than the data.</span></span> <span data-ttu-id="863b2-130">Значение по умолчанию для этого параметра — **false**.</span><span class="sxs-lookup"><span data-stu-id="863b2-130">The default value for this parameter is **FALSE**.</span></span> <span data-ttu-id="863b2-131">Можно задать только **значение true** , если объект, для которого вызывается этот метод, является классом.</span><span class="sxs-lookup"><span data-stu-id="863b2-131">It can only be set to **TRUE** if the object on which this method is invoked is a class.</span></span> <span data-ttu-id="863b2-132">Если задано **значение true**, набор возвращаемых конечных точек представляет классы, которые связаны с исходным классом в схеме.</span><span class="sxs-lookup"><span data-stu-id="863b2-132">When set to **TRUE**, the set of returned endpoints represent classes that are suitably associated with the source class in the schema.</span></span>

</dd> <dt>

<span data-ttu-id="863b2-133">*стррекуиредассоккуалифиер* \[ в необязательное\]</span><span class="sxs-lookup"><span data-stu-id="863b2-133">*strRequiredAssocQualifier* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="863b2-134">Строка, содержащая имя квалификатора.</span><span class="sxs-lookup"><span data-stu-id="863b2-134">String that contains a qualifier name.</span></span> <span data-ttu-id="863b2-135">Этот параметр, если он указан, указывает, что возвращенные конечные точки должны быть связаны с исходным объектом через класс ассоциации, включающий указанный квалификатор.</span><span class="sxs-lookup"><span data-stu-id="863b2-135">This parameter, if specified, indicates that the returned endpoints must be associated with the source object through an association class that includes the specified qualifier.</span></span>

</dd> <dt>

<span data-ttu-id="863b2-136">*стррекуиредкуалифиер* \[ в необязательное\]</span><span class="sxs-lookup"><span data-stu-id="863b2-136">*strRequiredQualifier* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="863b2-137">Строка, содержащая имя квалификатора.</span><span class="sxs-lookup"><span data-stu-id="863b2-137">String that contains a qualifier name.</span></span> <span data-ttu-id="863b2-138">Этот параметр, если он указан, указывает, что возвращаемые конечные точки должны включать указанный квалификатор.</span><span class="sxs-lookup"><span data-stu-id="863b2-138">This parameter, if specified, indicates that the returned endpoints must include the specified qualifier.</span></span>

</dd> <dt>

<span data-ttu-id="863b2-139">*ифлагс* \[ в необязательное\]</span><span class="sxs-lookup"><span data-stu-id="863b2-139">*iFlags* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="863b2-140">Целое число, указывающее дополнительные флаги для операции.</span><span class="sxs-lookup"><span data-stu-id="863b2-140">Integer specifying additional flags to the operation.</span></span> <span data-ttu-id="863b2-141">По умолчанию для этого параметра задано значение **вбемфлагретурниммедиатели**, которое направляет вызов для возврата немедленно, а не ожидания завершения запроса.</span><span class="sxs-lookup"><span data-stu-id="863b2-141">The default for this parameter is **wbemFlagReturnImmediately**, which directs the call to return immediately rather than wait until the query has completed.</span></span> <span data-ttu-id="863b2-142">Этот параметр может принимать следующие значения.</span><span class="sxs-lookup"><span data-stu-id="863b2-142">This parameter can accept the following values.</span></span>

<dt>

<span id="wbemFlagForwardOnly"></span><span id="wbemflagforwardonly"></span><span id="WBEMFLAGFORWARDONLY"></span>

<span data-ttu-id="863b2-143"><span id="wbemFlagForwardOnly"></span><span id="wbemflagforwardonly"></span><span id="WBEMFLAGFORWARDONLY"></span>Вбемфлагфорвардонли \* \* \* \* (32 (0x20))</span><span class="sxs-lookup"><span data-stu-id="863b2-143"><span id="wbemFlagForwardOnly"></span><span id="wbemflagforwardonly"></span><span id="WBEMFLAGFORWARDONLY"></span>\*\*\*\*wbemFlagForwardOnly\*\*\*\* (32 (0x20))</span></span>


</dt> <dd>

<span data-ttu-id="863b2-144">Вызывает возврат перечислителя "только вперед".</span><span class="sxs-lookup"><span data-stu-id="863b2-144">Causes a forward-only enumerator to be returned.</span></span> <span data-ttu-id="863b2-145">Перечислители "только вперед" обычно выполняются гораздо быстрее и используют меньше памяти, чем обычные перечислители, но они не допускают вызовов [**SWbemObject. Clone \_**](swbemobject-clone-.md).</span><span class="sxs-lookup"><span data-stu-id="863b2-145">Forward-only enumerators are generally much faster and use less memory than conventional enumerators, but they do not allow calls to [**SWbemObject.Clone\_**](swbemobject-clone-.md).</span></span>

</dd> <dt>

<span id="wbemFlagBidirectional"></span><span id="wbemflagbidirectional"></span><span id="WBEMFLAGBIDIRECTIONAL"></span>

<span data-ttu-id="863b2-146"><span id="wbemFlagBidirectional"></span><span id="wbemflagbidirectional"></span><span id="WBEMFLAGBIDIRECTIONAL"></span>Вбемфлагбидиректионал \* \* \* \* (0 (0x0))</span><span class="sxs-lookup"><span data-stu-id="863b2-146"><span id="wbemFlagBidirectional"></span><span id="wbemflagbidirectional"></span><span id="WBEMFLAGBIDIRECTIONAL"></span>\*\*\*\*wbemFlagBidirectional\*\*\*\* (0 (0x0))</span></span>


</dt> <dd>

<span data-ttu-id="863b2-147">Заставляет Инструментарий WMI хранить указатели на объекты перечисления до тех пор, пока клиент не освободит перечислитель.</span><span class="sxs-lookup"><span data-stu-id="863b2-147">Causes WMI to retain pointers to objects of the enumeration until the client releases the enumerator.</span></span>

</dd> <dt>

<span id="wbemFlagReturnImmediately"></span><span id="wbemflagreturnimmediately"></span><span id="WBEMFLAGRETURNIMMEDIATELY"></span>

<span data-ttu-id="863b2-148"><span id="wbemFlagReturnImmediately"></span><span id="wbemflagreturnimmediately"></span><span id="WBEMFLAGRETURNIMMEDIATELY"></span>Вбемфлагретурниммедиатели \* \* \* \* (16 (0x10))</span><span class="sxs-lookup"><span data-stu-id="863b2-148"><span id="wbemFlagReturnImmediately"></span><span id="wbemflagreturnimmediately"></span><span id="WBEMFLAGRETURNIMMEDIATELY"></span>\*\*\*\*wbemFlagReturnImmediately\*\*\*\* (16 (0x10))</span></span>


</dt> <dd>

<span data-ttu-id="863b2-149">Приводит к немедленному возврату вызова.</span><span class="sxs-lookup"><span data-stu-id="863b2-149">Causes the call to return immediately.</span></span>

</dd> <dt>

<span id="wbemFlagReturnWhenComplete"></span><span id="wbemflagreturnwhencomplete"></span><span id="WBEMFLAGRETURNWHENCOMPLETE"></span>

<span data-ttu-id="863b2-150"><span id="wbemFlagReturnWhenComplete"></span><span id="wbemflagreturnwhencomplete"></span><span id="WBEMFLAGRETURNWHENCOMPLETE"></span>Вбемфлагретурнвхенкомплете \* \* \* \* (0 (0x0))</span><span class="sxs-lookup"><span data-stu-id="863b2-150"><span id="wbemFlagReturnWhenComplete"></span><span id="wbemflagreturnwhencomplete"></span><span id="WBEMFLAGRETURNWHENCOMPLETE"></span>\*\*\*\*wbemFlagReturnWhenComplete\*\*\*\* (0 (0x0))</span></span>


</dt> <dd>

<span data-ttu-id="863b2-151">Вызывает блокирование этого вызова до тех пор, пока запрос не будет завершен.</span><span class="sxs-lookup"><span data-stu-id="863b2-151">Causes this call to block until the query has completed.</span></span>

</dd> <dt>

<span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>

<span data-ttu-id="863b2-152"><span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>Вбемфлагусеамендедкуалифиерс \* \* \* \* (131072 (0x20000))</span><span class="sxs-lookup"><span data-stu-id="863b2-152"><span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>\*\*\*\*wbemFlagUseAmendedQualifiers\*\*\*\* (131072 (0x20000))</span></span>


</dt> <dd>

<span data-ttu-id="863b2-153">Заставляет WMI возвращать данные о поправности класса с определением базового класса.</span><span class="sxs-lookup"><span data-stu-id="863b2-153">Causes WMI to return class amendment data with the base class definition.</span></span> <span data-ttu-id="863b2-154">Включение этого флага делает текст квалификатора локализованного описания доступным для классов, свойств и методов.</span><span class="sxs-lookup"><span data-stu-id="863b2-154">Including this flag makes the localized description qualifier text available for classes, properties and methods.</span></span> <span data-ttu-id="863b2-155">Дополнительные сведения об измененных квалификаторах см. в разделе [Локализация сведений о классе WMI](localizing-wmi-class-information.md).</span><span class="sxs-lookup"><span data-stu-id="863b2-155">For more information about amended qualifiers, see [Localizing WMI Class Information](localizing-wmi-class-information.md).</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="863b2-156">*обжвбемнамедвалуесет* \[ в необязательное\]</span><span class="sxs-lookup"><span data-stu-id="863b2-156">*objwbemNamedValueSet* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="863b2-157">Как правило, это не определено.</span><span class="sxs-lookup"><span data-stu-id="863b2-157">Typically, this is undefined.</span></span> <span data-ttu-id="863b2-158">В противном случае это объект [**свбемнамедвалуесет**](swbemnamedvalueset.md) , элементы которого представляют сведения о контексте, которые могут использоваться поставщиком, обслуживающим запрос.</span><span class="sxs-lookup"><span data-stu-id="863b2-158">Otherwise, this is an [**SWbemNamedValueSet**](swbemnamedvalueset.md) object whose elements represent the context information that can be used by the provider that is servicing the request.</span></span> <span data-ttu-id="863b2-159">Поставщик, который поддерживает или требует такую информацию, должен документировать распознанные имена значений, тип данных значения, допустимые значения и семантику.</span><span class="sxs-lookup"><span data-stu-id="863b2-159">A provider that supports or requires such information must document the recognized value names, data type of the value, allowed values, and semantics.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="863b2-160">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="863b2-160">Return value</span></span>

<span data-ttu-id="863b2-161">Если вызов выполнен успешно, возвращается объект [**SWbemObjectSet**](swbemobjectset.md) .</span><span class="sxs-lookup"><span data-stu-id="863b2-161">If the call is successful, an [**SWbemObjectSet**](swbemobjectset.md) object is returned.</span></span>

## <a name="error-codes"></a><span data-ttu-id="863b2-162">Коды ошибок</span><span class="sxs-lookup"><span data-stu-id="863b2-162">Error codes</span></span>

<span data-ttu-id="863b2-163">После завершения метода **сопоставления \_** объект **Err** может содержать один из кодов ошибок из следующего списка.</span><span class="sxs-lookup"><span data-stu-id="863b2-163">After completion of the **Associators\_** method, the **Err** object may contain one of the error codes in the following list.</span></span>

<dl> <dt>

<span data-ttu-id="863b2-164">**вбемерракцессдениед** -2147749891 (0x80041003)</span><span class="sxs-lookup"><span data-stu-id="863b2-164">**wbemErrAccessDenied** - 2147749891 (0x80041003)</span></span>
</dt> <dd>

<span data-ttu-id="863b2-165">Текущий пользователь не имеет разрешения на просмотр одного или нескольких классов, возвращенных вызовом.</span><span class="sxs-lookup"><span data-stu-id="863b2-165">The current user does not have permission to view one or more of the classes returned by the call.</span></span>

</dd> <dt>

<span data-ttu-id="863b2-166">**вбемеррфаилед** -2147749889 (0x80041001)</span><span class="sxs-lookup"><span data-stu-id="863b2-166">**wbemErrFailed** - 2147749889 (0x80041001)</span></span>
</dt> <dd>

<span data-ttu-id="863b2-167">Незаданная ошибка.</span><span class="sxs-lookup"><span data-stu-id="863b2-167">Unspecified error.</span></span>

</dd> <dt>

<span data-ttu-id="863b2-168">**вбемерринвалидпараметер** -2147749896 (0x80041008)</span><span class="sxs-lookup"><span data-stu-id="863b2-168">**wbemErrInvalidParameter** - 2147749896 (0x80041008)</span></span>
</dt> <dd>

<span data-ttu-id="863b2-169">Указан недопустимый параметр.</span><span class="sxs-lookup"><span data-stu-id="863b2-169">A specified parameter is not valid.</span></span>

</dd> <dt>

<span data-ttu-id="863b2-170">**вбемерраутофмемори** -2147749894</span><span class="sxs-lookup"><span data-stu-id="863b2-170">**wbemErrOutOfMemory** - 2147749894</span></span>
</dt> <dd>

<span data-ttu-id="863b2-171">Недостаточно памяти для завершения операции.</span><span class="sxs-lookup"><span data-stu-id="863b2-171">Not enough memory to complete the operation.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="863b2-172">Комментарии</span><span class="sxs-lookup"><span data-stu-id="863b2-172">Remarks</span></span>

<span data-ttu-id="863b2-173">Дополнительные сведения о СОЕДИНИТЕЛях связанного WQL-запроса, исходных экземпляров и конечных точек см. в разделе [соединители оператора](associators-of-statement.md).</span><span class="sxs-lookup"><span data-stu-id="863b2-173">For more information about the ASSOCIATORS OF associated WQL query, source instances, and endpoints, see [ASSOCIATORS OF Statement](associators-of-statement.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="863b2-174">Требования</span><span class="sxs-lookup"><span data-stu-id="863b2-174">Requirements</span></span>



| <span data-ttu-id="863b2-175">Требование</span><span class="sxs-lookup"><span data-stu-id="863b2-175">Requirement</span></span> | <span data-ttu-id="863b2-176">Значение</span><span class="sxs-lookup"><span data-stu-id="863b2-176">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="863b2-177">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="863b2-177">Minimum supported client</span></span><br/> | <span data-ttu-id="863b2-178">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="863b2-178">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="863b2-179">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="863b2-179">Minimum supported server</span></span><br/> | <span data-ttu-id="863b2-180">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="863b2-180">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="863b2-181">Header</span><span class="sxs-lookup"><span data-stu-id="863b2-181">Header</span></span><br/>                   | <dl> <span data-ttu-id="863b2-182"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="863b2-182"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="863b2-183">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="863b2-183">Type library</span></span><br/>             | <dl> <span data-ttu-id="863b2-184"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="863b2-184"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="863b2-185">DLL</span><span class="sxs-lookup"><span data-stu-id="863b2-185">DLL</span></span><br/>                      | <dl> <span data-ttu-id="863b2-186"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="863b2-186"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="863b2-187">CLSID</span><span class="sxs-lookup"><span data-stu-id="863b2-187">CLSID</span></span><br/>                    | <span data-ttu-id="863b2-188">\_SWBEMOBJECT CLSID</span><span class="sxs-lookup"><span data-stu-id="863b2-188">CLSID\_SWbemObject</span></span><br/>                                                           |
| <span data-ttu-id="863b2-189">IID</span><span class="sxs-lookup"><span data-stu-id="863b2-189">IID</span></span><br/>                      | <span data-ttu-id="863b2-190">IID \_ исвбемобжект</span><span class="sxs-lookup"><span data-stu-id="863b2-190">IID\_ISWbemObject</span></span><br/>                                                            |



## <a name="see-also"></a><span data-ttu-id="863b2-191">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="863b2-191">See also</span></span>

<dl> <dt>

[<span data-ttu-id="863b2-192">**SWbemObject**</span><span class="sxs-lookup"><span data-stu-id="863b2-192">**SWbemObject**</span></span>](swbemobject.md)
</dt> <dt>

[<span data-ttu-id="863b2-193">**SWbemObject. References\_**</span><span class="sxs-lookup"><span data-stu-id="863b2-193">**SWbemObject.References\_**</span></span>](swbemobject-references-.md)
</dt> <dt>

[<span data-ttu-id="863b2-194">**SWbemServices. АссоЦиаторсоф**</span><span class="sxs-lookup"><span data-stu-id="863b2-194">**SWbemServices.AssociatorsOf**</span></span>](swbemservices-associatorsof.md)
</dt> <dt>

[<span data-ttu-id="863b2-195">**SWbemServices. Референцесто**</span><span class="sxs-lookup"><span data-stu-id="863b2-195">**SWbemServices.ReferencesTo**</span></span>](swbemservices-referencesto.md)
</dt> </dl>

 

 




