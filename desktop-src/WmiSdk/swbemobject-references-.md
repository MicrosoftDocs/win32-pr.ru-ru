---
description: Метод References \_ объекта SWbemObject Возвращает коллекцию всех классов ассоциации или экземпляров, ссылающихся на текущий объект.
ms.assetid: ba02da47-0bb2-40e1-af50-1c42b4be2abd
ms.tgt_platform: multiple
title: Метод SWbemObject.References_ (Wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemObject.References_
- ISWbemObject.References_
- ISWbemObject.References_
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 3349ff104a5f0730ee99735a230d265fffd1333f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103913204"
---
# <a name="swbemobjectreferences_-method"></a><span data-ttu-id="b2ba7-103">SWbemObject. References, \_ метод</span><span class="sxs-lookup"><span data-stu-id="b2ba7-103">SWbemObject.References\_ method</span></span>

<span data-ttu-id="b2ba7-104">Метод **References \_** объекта [**SWbemObject**](swbemobject.md) Возвращает коллекцию всех классов ассоциации или экземпляров, ссылающихся на текущий объект.</span><span class="sxs-lookup"><span data-stu-id="b2ba7-104">The **References\_** method of the [**SWbemObject**](swbemobject.md) object returns a collection of all association classes or instances that refer to the current object.</span></span>

<span data-ttu-id="b2ba7-105">Этот метод выполняет ту же функцию, что и [ссылки на](references-of-statement.md) WQL-запрос.</span><span class="sxs-lookup"><span data-stu-id="b2ba7-105">This method performs the same function as the [REFERENCES OF](references-of-statement.md) WQL query.</span></span>

<span data-ttu-id="b2ba7-106">Описание этого синтаксиса см. в разделе [соглашения о документе для API скриптов](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="b2ba7-106">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="b2ba7-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="b2ba7-107">Syntax</span></span>


```VB
objWbemObjectSet = .References_( _
  [ ByVal strResultClass ], _
  [ ByVal strRole ], _
  [ ByVal bClassesOnly ], _
  [ ByVal bSchemaOnly ], _
  [ ByVal strRequiredQualifier ], _
  [ ByVal iFlags ], _
  [ ByVal objwbemNamedValueSet ] _
)
```



## <a name="parameters"></a><span data-ttu-id="b2ba7-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="b2ba7-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b2ba7-109">*стрресулткласс* \[ в необязательное\]</span><span class="sxs-lookup"><span data-stu-id="b2ba7-109">*strResultClass* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="b2ba7-110">Строка, содержащая имя класса.</span><span class="sxs-lookup"><span data-stu-id="b2ba7-110">String that contains a class name.</span></span> <span data-ttu-id="b2ba7-111">Если этот параметр указан, он указывает, что возвращаемые объекты ассоциации должны принадлежать или быть производными от класса, указанного в этом параметре.</span><span class="sxs-lookup"><span data-stu-id="b2ba7-111">If specified, this parameter indicates that the returned association objects must belong to or be derived from the class specified in this parameter.</span></span>

</dd> <dt>

<span data-ttu-id="b2ba7-112">*strRole* \[ в необязательное\]</span><span class="sxs-lookup"><span data-stu-id="b2ba7-112">*strRole* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="b2ba7-113">Строка, содержащая имя свойства.</span><span class="sxs-lookup"><span data-stu-id="b2ba7-113">String that contains a property name.</span></span> <span data-ttu-id="b2ba7-114">Если этот параметр задан, он указывает, что возвращаемые объекты связи должны быть ограничены теми, в которых исходный объект играет определенную роль.</span><span class="sxs-lookup"><span data-stu-id="b2ba7-114">If specified, this parameter indicates that the returned association objects must be limited to those in which the source object plays a specific role.</span></span> <span data-ttu-id="b2ba7-115">Роль определяется именем указанного свойства (которое должно быть ссылочным свойством) ассоциации.</span><span class="sxs-lookup"><span data-stu-id="b2ba7-115">The role is defined by the name of a specified property (which must be a reference property) of an association.</span></span>

</dd> <dt>

<span data-ttu-id="b2ba7-116">*бклассесонли* \[ в необязательное\]</span><span class="sxs-lookup"><span data-stu-id="b2ba7-116">*bClassesOnly* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="b2ba7-117">Логическое значение, указывающее, следует ли возвращать список имен классов, а не фактические экземпляры классов.</span><span class="sxs-lookup"><span data-stu-id="b2ba7-117">Boolean value that indicates whether or not a list of class names should be returned rather than actual instances of the classes.</span></span> <span data-ttu-id="b2ba7-118">Это классы, к которым принадлежат объекты взаимосвязей.</span><span class="sxs-lookup"><span data-stu-id="b2ba7-118">These are the classes to which the association objects belong.</span></span> <span data-ttu-id="b2ba7-119">Значение по умолчанию для этого параметра — **false**.</span><span class="sxs-lookup"><span data-stu-id="b2ba7-119">The default value for this parameter is **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="b2ba7-120">*бсчемаонли* \[ в необязательное\]</span><span class="sxs-lookup"><span data-stu-id="b2ba7-120">*bSchemaOnly* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="b2ba7-121">Логическое значение, указывающее, применяется ли запрос к схеме, а не к данным.</span><span class="sxs-lookup"><span data-stu-id="b2ba7-121">Boolean value that indicates whether or not the query applies to the schema rather than the data.</span></span> <span data-ttu-id="b2ba7-122">Значение по умолчанию для этого параметра — **false**.</span><span class="sxs-lookup"><span data-stu-id="b2ba7-122">The default value for this parameter is **FALSE**.</span></span> <span data-ttu-id="b2ba7-123">Можно задать только **значение true** , если объект, для которого вызывается этот метод, является классом.</span><span class="sxs-lookup"><span data-stu-id="b2ba7-123">It can only be set to **TRUE** if the object on which this method is invoked is a class.</span></span> <span data-ttu-id="b2ba7-124">Если задано **значение true**, набор возвращаемых конечных точек представляет классы, которые связаны с исходным классом в схеме.</span><span class="sxs-lookup"><span data-stu-id="b2ba7-124">When set to **TRUE**, the set of returned endpoints represents classes that are suitably associated with the source class in the schema.</span></span>

</dd> <dt>

<span data-ttu-id="b2ba7-125">*стррекуиредкуалифиер* \[ в необязательное\]</span><span class="sxs-lookup"><span data-stu-id="b2ba7-125">*strRequiredQualifier* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="b2ba7-126">Строка, содержащая имя квалификатора.</span><span class="sxs-lookup"><span data-stu-id="b2ba7-126">String that contains a qualifier name.</span></span> <span data-ttu-id="b2ba7-127">Если этот параметр указан, он указывает, что возвращаемые объекты связи должны включать указанный квалификатор.</span><span class="sxs-lookup"><span data-stu-id="b2ba7-127">If specified, this parameter indicates that the returned association objects must include the specified qualifier.</span></span>

</dd> <dt>

<span data-ttu-id="b2ba7-128">*ифлагс* \[ в необязательное\]</span><span class="sxs-lookup"><span data-stu-id="b2ba7-128">*iFlags* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="b2ba7-129">Целое число, указывающее дополнительные флаги для операции.</span><span class="sxs-lookup"><span data-stu-id="b2ba7-129">Integer specifying additional flags to the operation.</span></span> <span data-ttu-id="b2ba7-130">По умолчанию для этого параметра задано значение **вбемфлагретурниммедиатели**, которое направляет вызов для возврата немедленно, а не ожидания завершения запроса.</span><span class="sxs-lookup"><span data-stu-id="b2ba7-130">The default for this parameter is **wbemFlagReturnImmediately**, which directs the call to return immediately rather than wait until the query has completed.</span></span> <span data-ttu-id="b2ba7-131">Этот параметр может принимать следующие значения.</span><span class="sxs-lookup"><span data-stu-id="b2ba7-131">This parameter can accept the following values.</span></span>

<dt>

<span id="wbemFlagForwardOnly"></span><span id="wbemflagforwardonly"></span><span id="WBEMFLAGFORWARDONLY"></span>

<span data-ttu-id="b2ba7-132"><span id="wbemFlagForwardOnly"></span><span id="wbemflagforwardonly"></span><span id="WBEMFLAGFORWARDONLY"></span>Вбемфлагфорвардонли \* \* \* \* (32 (0x20))</span><span class="sxs-lookup"><span data-stu-id="b2ba7-132"><span id="wbemFlagForwardOnly"></span><span id="wbemflagforwardonly"></span><span id="WBEMFLAGFORWARDONLY"></span>\*\*\*\*wbemFlagForwardOnly\*\*\*\* (32 (0x20))</span></span>


</dt> <dd>

<span data-ttu-id="b2ba7-133">Вызывает возврат перечислителя "только вперед".</span><span class="sxs-lookup"><span data-stu-id="b2ba7-133">Causes a forward-only enumerator to be returned.</span></span> <span data-ttu-id="b2ba7-134">Перечислители "только вперед" обычно выполняются гораздо быстрее и используют меньше памяти, чем обычные перечислители, но они не допускают вызовов [**SWbemObject. Clone \_**](swbemobject-clone-.md).</span><span class="sxs-lookup"><span data-stu-id="b2ba7-134">Forward-only enumerators are generally much faster and use less memory than conventional enumerators, but they do not allow calls to [**SWbemObject.Clone\_**](swbemobject-clone-.md).</span></span>

</dd> <dt>

<span id="wbemFlagBidirectional"></span><span id="wbemflagbidirectional"></span><span id="WBEMFLAGBIDIRECTIONAL"></span>

<span data-ttu-id="b2ba7-135"><span id="wbemFlagBidirectional"></span><span id="wbemflagbidirectional"></span><span id="WBEMFLAGBIDIRECTIONAL"></span>Вбемфлагбидиректионал \* \* \* \* (0 (0x0))</span><span class="sxs-lookup"><span data-stu-id="b2ba7-135"><span id="wbemFlagBidirectional"></span><span id="wbemflagbidirectional"></span><span id="WBEMFLAGBIDIRECTIONAL"></span>\*\*\*\*wbemFlagBidirectional\*\*\*\* (0 (0x0))</span></span>


</dt> <dd>

<span data-ttu-id="b2ba7-136">Заставляет инструментарий управления Windows (WMI) (WMI) хранить указатели на объекты перечисления до тех пор, пока клиент не освободит перечислитель.</span><span class="sxs-lookup"><span data-stu-id="b2ba7-136">Causes Windows Management Instrumentation (WMI) to retain pointers to objects of the enumeration until the client releases the enumerator.</span></span>

</dd> <dt>

<span id="wbemFlagReturnImmediately"></span><span id="wbemflagreturnimmediately"></span><span id="WBEMFLAGRETURNIMMEDIATELY"></span>

<span data-ttu-id="b2ba7-137"><span id="wbemFlagReturnImmediately"></span><span id="wbemflagreturnimmediately"></span><span id="WBEMFLAGRETURNIMMEDIATELY"></span>Вбемфлагретурниммедиатели \* \* \* \* (16 (0x10))</span><span class="sxs-lookup"><span data-stu-id="b2ba7-137"><span id="wbemFlagReturnImmediately"></span><span id="wbemflagreturnimmediately"></span><span id="WBEMFLAGRETURNIMMEDIATELY"></span>\*\*\*\*wbemFlagReturnImmediately\*\*\*\* (16 (0x10))</span></span>


</dt> <dd>

<span data-ttu-id="b2ba7-138">Приводит к немедленному возврату вызова.</span><span class="sxs-lookup"><span data-stu-id="b2ba7-138">Causes the call to return immediately.</span></span>

</dd> <dt>

<span id="wbemFlagReturnWhenComplete"></span><span id="wbemflagreturnwhencomplete"></span><span id="WBEMFLAGRETURNWHENCOMPLETE"></span>

<span data-ttu-id="b2ba7-139"><span id="wbemFlagReturnWhenComplete"></span><span id="wbemflagreturnwhencomplete"></span><span id="WBEMFLAGRETURNWHENCOMPLETE"></span>Вбемфлагретурнвхенкомплете \* \* \* \* (0 (0x0))</span><span class="sxs-lookup"><span data-stu-id="b2ba7-139"><span id="wbemFlagReturnWhenComplete"></span><span id="wbemflagreturnwhencomplete"></span><span id="WBEMFLAGRETURNWHENCOMPLETE"></span>\*\*\*\*wbemFlagReturnWhenComplete\*\*\*\* (0 (0x0))</span></span>


</dt> <dd>

<span data-ttu-id="b2ba7-140">Вызывает блокирование этого вызова до тех пор, пока запрос не будет завершен.</span><span class="sxs-lookup"><span data-stu-id="b2ba7-140">Causes this call to block until the query has completed.</span></span>

</dd> <dt>

<span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>

<span data-ttu-id="b2ba7-141"><span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>Вбемфлагусеамендедкуалифиерс \* \* \* \* (131072 (0x20000))</span><span class="sxs-lookup"><span data-stu-id="b2ba7-141"><span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>\*\*\*\*wbemFlagUseAmendedQualifiers\*\*\*\* (131072 (0x20000))</span></span>


</dt> <dd>

<span data-ttu-id="b2ba7-142">Заставляет WMI возвращать данные о поправности класса с определением базового класса.</span><span class="sxs-lookup"><span data-stu-id="b2ba7-142">Causes WMI to return class amendment data with the base class definition.</span></span> <span data-ttu-id="b2ba7-143">Дополнительные сведения об измененных квалификаторах см. в разделе [Локализация сведений о классе WMI](localizing-wmi-class-information.md).</span><span class="sxs-lookup"><span data-stu-id="b2ba7-143">For more information about amended qualifiers, see [Localizing WMI Class Information](localizing-wmi-class-information.md).</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="b2ba7-144">*обжвбемнамедвалуесет* \[ в необязательное\]</span><span class="sxs-lookup"><span data-stu-id="b2ba7-144">*objwbemNamedValueSet* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="b2ba7-145">Как правило, это не определено.</span><span class="sxs-lookup"><span data-stu-id="b2ba7-145">Typically, this is undefined.</span></span> <span data-ttu-id="b2ba7-146">В противном случае это объект [**свбемнамедвалуесет**](swbemnamedvalueset.md) , элементы которого представляют сведения о контексте, которые могут использоваться поставщиком, обслуживающим запрос.</span><span class="sxs-lookup"><span data-stu-id="b2ba7-146">Otherwise, this is an [**SWbemNamedValueSet**](swbemnamedvalueset.md) object whose elements represent the context information that can be used by the provider that is servicing the request.</span></span> <span data-ttu-id="b2ba7-147">Поставщик, который поддерживает или требует такую информацию, должен документировать распознанные имена значений, тип данных значения, допустимые значения и семантику.</span><span class="sxs-lookup"><span data-stu-id="b2ba7-147">A provider that supports or requires such information must document the recognized value names, data type of the value, allowed values, and semantics.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b2ba7-148">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="b2ba7-148">Return value</span></span>

<span data-ttu-id="b2ba7-149">Если вызов выполнен успешно, возвращается объект [**SWbemObjectSet**](swbemobjectset.md) .</span><span class="sxs-lookup"><span data-stu-id="b2ba7-149">If the call is successful, an [**SWbemObjectSet**](swbemobjectset.md) object is returned.</span></span>

## <a name="error-codes"></a><span data-ttu-id="b2ba7-150">Коды ошибок</span><span class="sxs-lookup"><span data-stu-id="b2ba7-150">Error codes</span></span>

<span data-ttu-id="b2ba7-151">После завершения метода **References \_** объект **Err** может содержать один из кодов ошибок из следующего списка.</span><span class="sxs-lookup"><span data-stu-id="b2ba7-151">After the completion of the **References\_** method, the **Err** object may contain one of the error codes in the following list.</span></span>

<dl> <dt>

<span data-ttu-id="b2ba7-152">**вбемерракцессдениед** -2147749891 (0x80041003)</span><span class="sxs-lookup"><span data-stu-id="b2ba7-152">**wbemErrAccessDenied** - 2147749891 (0x80041003)</span></span>
</dt> <dd>

<span data-ttu-id="b2ba7-153">У текущего пользователя нет разрешения на просмотр одного или нескольких классов, возвращенных вызовом.</span><span class="sxs-lookup"><span data-stu-id="b2ba7-153">Current user does not have permission to view one or more of the classes returned by the call.</span></span>

</dd> <dt>

<span data-ttu-id="b2ba7-154">**вбемеррфаилед** -2147749889 (0x80041001)</span><span class="sxs-lookup"><span data-stu-id="b2ba7-154">**wbemErrFailed** - 2147749889 (0x80041001)</span></span>
</dt> <dd>

<span data-ttu-id="b2ba7-155">Незаданная ошибка.</span><span class="sxs-lookup"><span data-stu-id="b2ba7-155">Unspecified error.</span></span>

</dd> <dt>

<span data-ttu-id="b2ba7-156">**вбемерринвалидпараметер** -2147749896 (0x80041008)</span><span class="sxs-lookup"><span data-stu-id="b2ba7-156">**wbemErrInvalidParameter** - 2147749896 (0x80041008)</span></span>
</dt> <dd>

<span data-ttu-id="b2ba7-157">Указан недопустимый параметр.</span><span class="sxs-lookup"><span data-stu-id="b2ba7-157">Invalid parameter was specified.</span></span>

</dd> <dt>

<span data-ttu-id="b2ba7-158">**вбемерраутофмемори** -2147749894 (0x80041006)</span><span class="sxs-lookup"><span data-stu-id="b2ba7-158">**wbemErrOutOfMemory** - 2147749894 (0x80041006)</span></span>
</dt> <dd>

<span data-ttu-id="b2ba7-159">Недостаточно памяти для завершения операции.</span><span class="sxs-lookup"><span data-stu-id="b2ba7-159">Not enough memory to complete the operation.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="b2ba7-160">Комментарии</span><span class="sxs-lookup"><span data-stu-id="b2ba7-160">Remarks</span></span>

<span data-ttu-id="b2ba7-161">Дополнительные сведения о ССЫЛКАх на связанный WQL-запрос, исходные экземпляры и объекты связи см. в разделе [соединители оператора](associators-of-statement.md).</span><span class="sxs-lookup"><span data-stu-id="b2ba7-161">For more information about the REFERENCES OF associated WQL query, source instances, and association objects, see [ASSOCIATORS OF Statement](associators-of-statement.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="b2ba7-162">Требования</span><span class="sxs-lookup"><span data-stu-id="b2ba7-162">Requirements</span></span>



| <span data-ttu-id="b2ba7-163">Требование</span><span class="sxs-lookup"><span data-stu-id="b2ba7-163">Requirement</span></span> | <span data-ttu-id="b2ba7-164">Значение</span><span class="sxs-lookup"><span data-stu-id="b2ba7-164">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="b2ba7-165">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="b2ba7-165">Minimum supported client</span></span><br/> | <span data-ttu-id="b2ba7-166">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="b2ba7-166">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="b2ba7-167">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="b2ba7-167">Minimum supported server</span></span><br/> | <span data-ttu-id="b2ba7-168">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="b2ba7-168">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="b2ba7-169">Header</span><span class="sxs-lookup"><span data-stu-id="b2ba7-169">Header</span></span><br/>                   | <dl> <span data-ttu-id="b2ba7-170"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="b2ba7-170"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="b2ba7-171">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="b2ba7-171">Type library</span></span><br/>             | <dl> <span data-ttu-id="b2ba7-172"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="b2ba7-172"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="b2ba7-173">DLL</span><span class="sxs-lookup"><span data-stu-id="b2ba7-173">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b2ba7-174"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b2ba7-174"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="b2ba7-175">CLSID</span><span class="sxs-lookup"><span data-stu-id="b2ba7-175">CLSID</span></span><br/>                    | <span data-ttu-id="b2ba7-176">\_SWBEMOBJECT CLSID</span><span class="sxs-lookup"><span data-stu-id="b2ba7-176">CLSID\_SWbemObject</span></span><br/>                                                           |
| <span data-ttu-id="b2ba7-177">IID</span><span class="sxs-lookup"><span data-stu-id="b2ba7-177">IID</span></span><br/>                      | <span data-ttu-id="b2ba7-178">IID \_ исвбемобжект</span><span class="sxs-lookup"><span data-stu-id="b2ba7-178">IID\_ISWbemObject</span></span><br/>                                                            |



## <a name="see-also"></a><span data-ttu-id="b2ba7-179">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="b2ba7-179">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b2ba7-180">**SWbemObject**</span><span class="sxs-lookup"><span data-stu-id="b2ba7-180">**SWbemObject**</span></span>](swbemobject.md)
</dt> <dt>

[<span data-ttu-id="b2ba7-181">**SWbemObject. соединители\_**</span><span class="sxs-lookup"><span data-stu-id="b2ba7-181">**SWbemObject.Associators\_**</span></span>](swbemobject-associators-.md)
</dt> <dt>

[<span data-ttu-id="b2ba7-182">**SWbemServices. АссоЦиаторсоф**</span><span class="sxs-lookup"><span data-stu-id="b2ba7-182">**SWbemServices.AssociatorsOf**</span></span>](swbemservices-associatorsof.md)
</dt> <dt>

[<span data-ttu-id="b2ba7-183">**SWbemServices. Референцесто**</span><span class="sxs-lookup"><span data-stu-id="b2ba7-183">**SWbemServices.ReferencesTo**</span></span>](swbemservices-referencesto.md)
</dt> </dl>

 

 




