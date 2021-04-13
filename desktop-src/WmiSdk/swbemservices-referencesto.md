---
description: Возвращает коллекцию всех классов или экземпляров взаимосвязей, которые ссылаются на конкретный исходный класс или экземпляр.
ms.assetid: 33425b1c-13f5-4c3d-8f8a-2922f3e95264
ms.tgt_platform: multiple
title: SWbemServices. Референцесто, метод (Wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemServices.ReferencesTo
- ISWbemServices.ReferencesTo
- ISWbemServices.ReferencesTo
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 73addea189815d1594d0963fbdd6e20c562b3be3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104156759"
---
# <a name="swbemservicesreferencesto-method"></a><span data-ttu-id="145dc-103">SWbemServices. Референцесто, метод</span><span class="sxs-lookup"><span data-stu-id="145dc-103">SWbemServices.ReferencesTo method</span></span>

<span data-ttu-id="145dc-104">Метод **референцесто** объекта [**SwbemServices**](swbemservices.md) Возвращает коллекцию всех классов ассоциации или экземпляров, ссылающихся на конкретный исходный класс или экземпляр.</span><span class="sxs-lookup"><span data-stu-id="145dc-104">The **ReferencesTo** method of the [**SWbemServices**](swbemservices.md) object returns a collection of all association classes or instances that refer to a specific source class or instance.</span></span> <span data-ttu-id="145dc-105">Этот метод выполняет ту же функцию, что и [ссылки на](references-of-statement.md) WQL-запросы.</span><span class="sxs-lookup"><span data-stu-id="145dc-105">This method performs the same function that the [REFERENCES OF](references-of-statement.md) WQL query performs.</span></span>

<span data-ttu-id="145dc-106">Этот метод вызывается в режиме семисинчронаус.</span><span class="sxs-lookup"><span data-stu-id="145dc-106">This method is called in the semisynchronous mode.</span></span> <span data-ttu-id="145dc-107">Дополнительные сведения см. [в разделе вызов метода](calling-a-method.md).</span><span class="sxs-lookup"><span data-stu-id="145dc-107">For more information, see [Calling a Method](calling-a-method.md).</span></span>

<span data-ttu-id="145dc-108">Описание этого синтаксиса см. в разделе [соглашения о документе для API скриптов](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="145dc-108">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="145dc-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="145dc-109">Syntax</span></span>


```VB
objWbemObjectSet = .ReferencesTo( _
  ByVal strObjectPath, _
  [ ByVal strResultClass ], _
  [ ByVal strRole ], _
  [ ByVal bClassesOnly ], _
  [ ByVal bSchemaOnly ], _
  [ ByVal strRequiredQualifier ], _
  [ ByVal iFlags ], _
  [ ByVal objWbemNamedValueSet ] _
)
```



## <a name="parameters"></a><span data-ttu-id="145dc-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="145dc-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="145dc-111">*стробжектпас*</span><span class="sxs-lookup"><span data-stu-id="145dc-111">*strObjectPath*</span></span> 
</dt> <dd>

<span data-ttu-id="145dc-112">Обязательный.</span><span class="sxs-lookup"><span data-stu-id="145dc-112">Required.</span></span> <span data-ttu-id="145dc-113">Строка, содержащая путь к объекту источника для этого метода.</span><span class="sxs-lookup"><span data-stu-id="145dc-113">String that contains the object path of the source for this method.</span></span> <span data-ttu-id="145dc-114">Дополнительные сведения см. [в разделе Описание расположения объекта WMI](describing-the-location-of-a-wmi-object.md).</span><span class="sxs-lookup"><span data-stu-id="145dc-114">For more information, see [Describing the Location of a WMI Object](describing-the-location-of-a-wmi-object.md).</span></span>

</dd> <dt>

<span data-ttu-id="145dc-115">*стрресулткласс* \[ используемых\]</span><span class="sxs-lookup"><span data-stu-id="145dc-115">*strResultClass* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="145dc-116">Строка, содержащая имя класса.</span><span class="sxs-lookup"><span data-stu-id="145dc-116">String that contains a class name.</span></span> <span data-ttu-id="145dc-117">Если этот параметр указан, то возвращаемые объекты ассоциации должны принадлежать классу, указанному в этом параметре, или быть производным от него.</span><span class="sxs-lookup"><span data-stu-id="145dc-117">If specified, this parameter indicates that the returned association objects must belong to or be derived from the class that is specified in this parameter.</span></span>

</dd> <dt>

<span data-ttu-id="145dc-118">*strRole* \[ используемых\]</span><span class="sxs-lookup"><span data-stu-id="145dc-118">*strRole* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="145dc-119">Строка, содержащая имя свойства.</span><span class="sxs-lookup"><span data-stu-id="145dc-119">String that contains a property name.</span></span> <span data-ttu-id="145dc-120">Если этот параметр задан, он указывает, что возвращаемые объекты связи должны быть ограничены теми, в которых исходный объект играет определенную роль.</span><span class="sxs-lookup"><span data-stu-id="145dc-120">If specified, this parameter indicates that the returned association objects must be limited to those in which the source object plays a specific role.</span></span> <span data-ttu-id="145dc-121">Роль определяется именем указанного свойства (которое должно быть ссылочным свойством) ассоциации.</span><span class="sxs-lookup"><span data-stu-id="145dc-121">The role is defined by the name of a specified property (which must be a reference property) of an association.</span></span>

</dd> <dt>

<span data-ttu-id="145dc-122">*бклассесонли* \[ используемых\]</span><span class="sxs-lookup"><span data-stu-id="145dc-122">*bClassesOnly* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="145dc-123">Логическое значение, указывающее, следует ли возвращать список имен классов, а не фактические экземпляры классов.</span><span class="sxs-lookup"><span data-stu-id="145dc-123">Boolean value that indicates whether or not a list of class names should be returned rather than actual instances of the classes.</span></span> <span data-ttu-id="145dc-124">Это классы, к которым принадлежат объекты взаимосвязей.</span><span class="sxs-lookup"><span data-stu-id="145dc-124">These are the classes to which the association objects belong.</span></span> <span data-ttu-id="145dc-125">Значение по умолчанию для этого параметра — **false**.</span><span class="sxs-lookup"><span data-stu-id="145dc-125">The default value for this parameter is **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="145dc-126">*бсчемаонли* \[ используемых\]</span><span class="sxs-lookup"><span data-stu-id="145dc-126">*bSchemaOnly* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="145dc-127">Логическое значение, указывающее, применяется ли запрос к схеме, а не к данным.</span><span class="sxs-lookup"><span data-stu-id="145dc-127">Boolean value that indicates whether or not the query applies to the schema rather than the data.</span></span> <span data-ttu-id="145dc-128">Значение по умолчанию для этого параметра — **false**.</span><span class="sxs-lookup"><span data-stu-id="145dc-128">The default value for this parameter is **FALSE**.</span></span> <span data-ttu-id="145dc-129">Можно задать только **значение true** , если параметр *стробжектпас* указывает путь к объекту класса.</span><span class="sxs-lookup"><span data-stu-id="145dc-129">It can only be set to **TRUE** if the *strObjectPath* parameter specifies the object path of a class.</span></span> <span data-ttu-id="145dc-130">Если задано **значение true**, набор возвращаемых конечных точек представляет классы, которые связаны с исходным классом в схеме.</span><span class="sxs-lookup"><span data-stu-id="145dc-130">When set to **TRUE**, the set of returned endpoints represents classes that are suitably associated with the source class in the schema.</span></span>

</dd> <dt>

<span data-ttu-id="145dc-131">*стррекуиредкуалифиер* \[ используемых\]</span><span class="sxs-lookup"><span data-stu-id="145dc-131">*strRequiredQualifier* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="145dc-132">Строка, содержащая имя квалификатора.</span><span class="sxs-lookup"><span data-stu-id="145dc-132">String that contains a qualifier name.</span></span> <span data-ttu-id="145dc-133">Если этот параметр указан, он указывает, что возвращаемые объекты связи должны включать указанный квалификатор.</span><span class="sxs-lookup"><span data-stu-id="145dc-133">If specified, this parameter indicates that the returned association objects must include the specified qualifier.</span></span>

</dd> <dt>

<span data-ttu-id="145dc-134">*ифлагс* \[ используемых\]</span><span class="sxs-lookup"><span data-stu-id="145dc-134">*iFlags* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="145dc-135">Целое число, задающее дополнительные флаги для операции.</span><span class="sxs-lookup"><span data-stu-id="145dc-135">Integer that specifies additional flags to the operation.</span></span> <span data-ttu-id="145dc-136">По умолчанию для этого параметра задано значение **вбемфлагретурниммедиатели**, которое направляет вызов для возврата немедленно, а не ожидания завершения запроса.</span><span class="sxs-lookup"><span data-stu-id="145dc-136">The default for this parameter is **wbemFlagReturnImmediately**, which directs the call to return immediately rather than wait until the query has completed.</span></span> <span data-ttu-id="145dc-137">Этот параметр может принимать следующие значения.</span><span class="sxs-lookup"><span data-stu-id="145dc-137">This parameter can accept the following values.</span></span>

<dt>

<span id="wbemFlagForwardOnly"></span><span id="wbemflagforwardonly"></span><span id="WBEMFLAGFORWARDONLY"></span>

<span data-ttu-id="145dc-138"><span id="wbemFlagForwardOnly"></span><span id="wbemflagforwardonly"></span><span id="WBEMFLAGFORWARDONLY"></span>Вбемфлагфорвардонли \* \* \* \* (32 (0x20))</span><span class="sxs-lookup"><span data-stu-id="145dc-138"><span id="wbemFlagForwardOnly"></span><span id="wbemflagforwardonly"></span><span id="WBEMFLAGFORWARDONLY"></span>\*\*\*\*wbemFlagForwardOnly\*\*\*\* (32 (0x20))</span></span>


</dt> <dd>

<span data-ttu-id="145dc-139">Вызывает возврат перечислителя "только вперед".</span><span class="sxs-lookup"><span data-stu-id="145dc-139">Causes a forward-only enumerator to be returned.</span></span> <span data-ttu-id="145dc-140">Перечислители "только вперед" обычно выполняются гораздо быстрее и используют меньше памяти, чем обычные перечислители, но они не допускают вызовов [**SWbemObject. Clone \_**](swbemobject-clone-.md).</span><span class="sxs-lookup"><span data-stu-id="145dc-140">Forward-only enumerators are generally much faster and use less memory than conventional enumerators, but they do not allow calls to [**SWbemObject.Clone\_**](swbemobject-clone-.md).</span></span>

</dd> <dt>

<span id="wbemFlagBidirectional"></span><span id="wbemflagbidirectional"></span><span id="WBEMFLAGBIDIRECTIONAL"></span>

<span data-ttu-id="145dc-141"><span id="wbemFlagBidirectional"></span><span id="wbemflagbidirectional"></span><span id="WBEMFLAGBIDIRECTIONAL"></span>Вбемфлагбидиректионал \* \* \* \* (0 (0x0))</span><span class="sxs-lookup"><span data-stu-id="145dc-141"><span id="wbemFlagBidirectional"></span><span id="wbemflagbidirectional"></span><span id="WBEMFLAGBIDIRECTIONAL"></span>\*\*\*\*wbemFlagBidirectional\*\*\*\* (0 (0x0))</span></span>


</dt> <dd>

<span data-ttu-id="145dc-142">Заставляет инструментарий управления Windows (WMI) (WMI) хранить указатели на объекты перечисления до тех пор, пока клиент не освободит перечислитель.</span><span class="sxs-lookup"><span data-stu-id="145dc-142">Causes Windows Management Instrumentation (WMI) to retain pointers to objects of the enumeration until the client releases the enumerator.</span></span>

</dd> <dt>

<span id="wbemFlagReturnImmediately"></span><span id="wbemflagreturnimmediately"></span><span id="WBEMFLAGRETURNIMMEDIATELY"></span>

<span data-ttu-id="145dc-143"><span id="wbemFlagReturnImmediately"></span><span id="wbemflagreturnimmediately"></span><span id="WBEMFLAGRETURNIMMEDIATELY"></span>Вбемфлагретурниммедиатели \* \* \* \* (16 (0x10))</span><span class="sxs-lookup"><span data-stu-id="145dc-143"><span id="wbemFlagReturnImmediately"></span><span id="wbemflagreturnimmediately"></span><span id="WBEMFLAGRETURNIMMEDIATELY"></span>\*\*\*\*wbemFlagReturnImmediately\*\*\*\* (16 (0x10))</span></span>


</dt> <dd>

<span data-ttu-id="145dc-144">Приводит к немедленному возврату вызова.</span><span class="sxs-lookup"><span data-stu-id="145dc-144">Causes the call to return immediately.</span></span>

</dd> <dt>

<span id="wbemFlagReturnWhenComplete"></span><span id="wbemflagreturnwhencomplete"></span><span id="WBEMFLAGRETURNWHENCOMPLETE"></span>

<span data-ttu-id="145dc-145"><span id="wbemFlagReturnWhenComplete"></span><span id="wbemflagreturnwhencomplete"></span><span id="WBEMFLAGRETURNWHENCOMPLETE"></span>Вбемфлагретурнвхенкомплете \* \* \* \* (0 (0x0))</span><span class="sxs-lookup"><span data-stu-id="145dc-145"><span id="wbemFlagReturnWhenComplete"></span><span id="wbemflagreturnwhencomplete"></span><span id="WBEMFLAGRETURNWHENCOMPLETE"></span>\*\*\*\*wbemFlagReturnWhenComplete\*\*\*\* (0 (0x0))</span></span>


</dt> <dd>

<span data-ttu-id="145dc-146">Вызывает блокирование этого вызова до тех пор, пока запрос не будет завершен.</span><span class="sxs-lookup"><span data-stu-id="145dc-146">Causes this call to block until the query has completed.</span></span> <span data-ttu-id="145dc-147">Этот флаг вызывает метод в синхронном режиме.</span><span class="sxs-lookup"><span data-stu-id="145dc-147">This flag calls the method in the synchronous mode.</span></span>

</dd> <dt>

<span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>

<span data-ttu-id="145dc-148"><span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>Вбемфлагусеамендедкуалифиерс \* \* \* \* (131072 (0x20000))</span><span class="sxs-lookup"><span data-stu-id="145dc-148"><span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>\*\*\*\*wbemFlagUseAmendedQualifiers\*\*\*\* (131072 (0x20000))</span></span>


</dt> <dd>

<span data-ttu-id="145dc-149">Заставляет Инструментарий WMI возвращать данные о поправности классов вместе с определением базового класса.</span><span class="sxs-lookup"><span data-stu-id="145dc-149">Causes WMI to return class amendment data along with the base class definition.</span></span> <span data-ttu-id="145dc-150">Дополнительные сведения см. в разделе [Локализация сведений о классе WMI](localizing-wmi-class-information.md).</span><span class="sxs-lookup"><span data-stu-id="145dc-150">For more information, see [Localizing WMI Class Information](localizing-wmi-class-information.md).</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="145dc-151">*обжвбемнамедвалуесет* \[ используемых\]</span><span class="sxs-lookup"><span data-stu-id="145dc-151">*objWbemNamedValueSet* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="145dc-152">Как правило, это не определено.</span><span class="sxs-lookup"><span data-stu-id="145dc-152">Typically, this is undefined.</span></span> <span data-ttu-id="145dc-153">В противном случае это объект [**свбемнамедвалуесет**](swbemnamedvalueset.md) , элементы которого представляют сведения о контексте, которые могут использоваться поставщиком, обслуживающим запрос.</span><span class="sxs-lookup"><span data-stu-id="145dc-153">Otherwise, this is an [**SWbemNamedValueSet**](swbemnamedvalueset.md) object whose elements represent the context information that can be used by the provider that is servicing the request.</span></span> <span data-ttu-id="145dc-154">Поставщик, который поддерживает или требует такую информацию, должен документировать распознанные имена значений, тип данных значения, допустимые значения и семантику.</span><span class="sxs-lookup"><span data-stu-id="145dc-154">A provider that supports or requires such information must document the recognized value names, data type of the value, allowed values, and semantics.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="145dc-155">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="145dc-155">Return value</span></span>

<span data-ttu-id="145dc-156">Если метод выполнен успешно, метод возвращает объект [**SWbemObjectSet**](swbemobjectset.md) .</span><span class="sxs-lookup"><span data-stu-id="145dc-156">If the method is successful, the method returns an [**SWbemObjectSet**](swbemobjectset.md) object.</span></span>

## <a name="error-codes"></a><span data-ttu-id="145dc-157">Коды ошибок</span><span class="sxs-lookup"><span data-stu-id="145dc-157">Error codes</span></span>

<span data-ttu-id="145dc-158">После завершения метода **референцесто** объект **Err** может содержать один из кодов ошибок из следующего списка.</span><span class="sxs-lookup"><span data-stu-id="145dc-158">After the completion of the **ReferencesTo** method, the **Err** object may contain one of the error codes in the following list.</span></span>

> [!Note]  
> <span data-ttu-id="145dc-159">Возвращенная коллекция с нулевым числом элементов не является ошибкой.</span><span class="sxs-lookup"><span data-stu-id="145dc-159">A returned collection with zero elements is not an error.</span></span>

 

<dl> <dt>

<span data-ttu-id="145dc-160">**вбемерракцессдениед** -2147749891 (0x80041003)</span><span class="sxs-lookup"><span data-stu-id="145dc-160">**wbemErrAccessDenied** - 2147749891 (0x80041003)</span></span>
</dt> <dd>

<span data-ttu-id="145dc-161">У текущего пользователя нет разрешения на просмотр одного или нескольких классов, возвращенных вызовом.</span><span class="sxs-lookup"><span data-stu-id="145dc-161">Current user does not have the permission to view one or more of the classes returned by the call.</span></span>

</dd> <dt>

<span data-ttu-id="145dc-162">**вбемеррфаилед** -2147749889 (0x80041001)</span><span class="sxs-lookup"><span data-stu-id="145dc-162">**wbemErrFailed** - 2147749889 (0x80041001)</span></span>
</dt> <dd>

<span data-ttu-id="145dc-163">Незаданная ошибка.</span><span class="sxs-lookup"><span data-stu-id="145dc-163">Unspecified error.</span></span>

</dd> <dt>

<span data-ttu-id="145dc-164">**вбемерринвалидпараметер** -2147749896 (0x80041008)</span><span class="sxs-lookup"><span data-stu-id="145dc-164">**wbemErrInvalidParameter** - 2147749896 (0x80041008)</span></span>
</dt> <dd>

<span data-ttu-id="145dc-165">Указан недопустимый параметр.</span><span class="sxs-lookup"><span data-stu-id="145dc-165">Invalid parameter was specified.</span></span>

</dd> <dt>

<span data-ttu-id="145dc-166">**вбемерраутофмемори** -2147749894 (0x80041006)</span><span class="sxs-lookup"><span data-stu-id="145dc-166">**wbemErrOutOfMemory** - 2147749894 (0x80041006)</span></span>
</dt> <dd>

<span data-ttu-id="145dc-167">Недостаточно памяти для завершения операции.</span><span class="sxs-lookup"><span data-stu-id="145dc-167">Not enough memory to complete the operation.</span></span>

</dd> <dt>

<span data-ttu-id="145dc-168">**вбемфлагусеамендедкуалифиерс** -131072 (0x20000)</span><span class="sxs-lookup"><span data-stu-id="145dc-168">**wbemFlagUseAmendedQualifiers** - 131072 (0x20000)</span></span>
</dt> <dd>

<span data-ttu-id="145dc-169">Заставляет WMI возвращать данные о поправности класса с определением базового класса.</span><span class="sxs-lookup"><span data-stu-id="145dc-169">Causes WMI to return class amendment data with the base class definition.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="145dc-170">Комментарии</span><span class="sxs-lookup"><span data-stu-id="145dc-170">Remarks</span></span>

<span data-ttu-id="145dc-171">Дополнительные сведения о ССЫЛКАх на связанный WQL-запрос, исходные экземпляры и объекты связи см. в разделе [соединители оператора](associators-of-statement.md).</span><span class="sxs-lookup"><span data-stu-id="145dc-171">For more information about the REFERENCES OF associated WQL query, source instances, and association objects, see [ASSOCIATORS OF Statement](associators-of-statement.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="145dc-172">Требования</span><span class="sxs-lookup"><span data-stu-id="145dc-172">Requirements</span></span>



| <span data-ttu-id="145dc-173">Требование</span><span class="sxs-lookup"><span data-stu-id="145dc-173">Requirement</span></span> | <span data-ttu-id="145dc-174">Значение</span><span class="sxs-lookup"><span data-stu-id="145dc-174">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="145dc-175">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="145dc-175">Minimum supported client</span></span><br/> | <span data-ttu-id="145dc-176">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="145dc-176">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="145dc-177">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="145dc-177">Minimum supported server</span></span><br/> | <span data-ttu-id="145dc-178">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="145dc-178">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="145dc-179">Header</span><span class="sxs-lookup"><span data-stu-id="145dc-179">Header</span></span><br/>                   | <dl> <span data-ttu-id="145dc-180"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="145dc-180"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="145dc-181">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="145dc-181">Type library</span></span><br/>             | <dl> <span data-ttu-id="145dc-182"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="145dc-182"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="145dc-183">DLL</span><span class="sxs-lookup"><span data-stu-id="145dc-183">DLL</span></span><br/>                      | <dl> <span data-ttu-id="145dc-184"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="145dc-184"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="145dc-185">CLSID</span><span class="sxs-lookup"><span data-stu-id="145dc-185">CLSID</span></span><br/>                    | <span data-ttu-id="145dc-186">\_SWBEMSERVICES CLSID</span><span class="sxs-lookup"><span data-stu-id="145dc-186">CLSID\_SWbemServices</span></span><br/>                                                         |
| <span data-ttu-id="145dc-187">IID</span><span class="sxs-lookup"><span data-stu-id="145dc-187">IID</span></span><br/>                      | <span data-ttu-id="145dc-188">IID \_ исвбемсервицес</span><span class="sxs-lookup"><span data-stu-id="145dc-188">IID\_ISWbemServices</span></span><br/>                                                          |



## <a name="see-also"></a><span data-ttu-id="145dc-189">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="145dc-189">See also</span></span>

<dl> <dt>

[<span data-ttu-id="145dc-190">**SWbemServices**</span><span class="sxs-lookup"><span data-stu-id="145dc-190">**SWbemServices**</span></span>](swbemservices.md)
</dt> <dt>

[<span data-ttu-id="145dc-191">**SWbemObject. соединители\_**</span><span class="sxs-lookup"><span data-stu-id="145dc-191">**SWbemObject.Associators\_**</span></span>](swbemobject-associators-.md)
</dt> <dt>

[<span data-ttu-id="145dc-192">**SWbemObject. References\_**</span><span class="sxs-lookup"><span data-stu-id="145dc-192">**SWbemObject.References\_**</span></span>](swbemobject-references-.md)
</dt> <dt>

[<span data-ttu-id="145dc-193">**SWbemServices. АссоЦиаторсоф**</span><span class="sxs-lookup"><span data-stu-id="145dc-193">**SWbemServices.AssociatorsOf**</span></span>](swbemservices-associatorsof.md)
</dt> </dl>

 

 




