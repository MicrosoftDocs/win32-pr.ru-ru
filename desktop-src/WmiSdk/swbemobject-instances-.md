---
description: Метод Instances \_ объекта SWbemObject создает перечислитель, который возвращает экземпляры текущего объекта класса. Этот метод реализует простой запрос. Более сложные запросы могут потребовать использования SWbemServices.ExeКкуери.
ms.assetid: 30402d7d-f7cb-43b5-96b5-a8a76144e32d
ms.tgt_platform: multiple
title: Метод SWbemObject.Instances_ (Wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemObject.Instances_
- ISWbemObject.Instances_
- ISWbemObject.Instances_
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: c573c1e94cd473d22483c7b6a2c801c3e6bcb9dd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105712896"
---
# <a name="swbemobjectinstances_-method"></a><span data-ttu-id="6eaa8-105">SWbemObject. Instances, \_ метод</span><span class="sxs-lookup"><span data-stu-id="6eaa8-105">SWbemObject.Instances\_ method</span></span>

<span data-ttu-id="6eaa8-106">Метод **Instances \_** объекта [**SWbemObject**](swbemobject.md) создает перечислитель, который возвращает экземпляры текущего объекта класса.</span><span class="sxs-lookup"><span data-stu-id="6eaa8-106">The **Instances\_** method of the [**SWbemObject**](swbemobject.md) object creates an enumerator that returns the instances of the current class object.</span></span> <span data-ttu-id="6eaa8-107">Этот метод реализует простой запрос.</span><span class="sxs-lookup"><span data-stu-id="6eaa8-107">This method implements a simple query.</span></span> <span data-ttu-id="6eaa8-108">Более сложные запросы могут потребовать использования [**SWbemServices.Exeккуери**](swbemservices-execquery.md).</span><span class="sxs-lookup"><span data-stu-id="6eaa8-108">More complex queries may require the use of [**SWbemServices.ExecQuery**](swbemservices-execquery.md).</span></span>

<span data-ttu-id="6eaa8-109">Описание этого синтаксиса см. в разделе [соглашения о документе для API скриптов](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="6eaa8-109">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="6eaa8-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="6eaa8-110">Syntax</span></span>


```VB
objWbemObjectSet = .Instances_( _
  [ ByVal iFlags ], _
  [ ByVal objwbemNamedValueSet ] _
)
```



## <a name="parameters"></a><span data-ttu-id="6eaa8-111">Параметры</span><span class="sxs-lookup"><span data-stu-id="6eaa8-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6eaa8-112">*ифлагс* \[ в необязательное\]</span><span class="sxs-lookup"><span data-stu-id="6eaa8-112">*iFlags* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="6eaa8-113">Целое число, определяющее поведение вызова.</span><span class="sxs-lookup"><span data-stu-id="6eaa8-113">Integer that determines the behavior of the call.</span></span> <span data-ttu-id="6eaa8-114">Этот параметр может принимать следующие значения.</span><span class="sxs-lookup"><span data-stu-id="6eaa8-114">This parameter can accept the following values.</span></span>

<dt>

<span id="wbemFlagForwardOnly"></span><span id="wbemflagforwardonly"></span><span id="WBEMFLAGFORWARDONLY"></span>

<span data-ttu-id="6eaa8-115"><span id="wbemFlagForwardOnly"></span><span id="wbemflagforwardonly"></span><span id="WBEMFLAGFORWARDONLY"></span>Вбемфлагфорвардонли \* \* \* \* (32 (0x20))</span><span class="sxs-lookup"><span data-stu-id="6eaa8-115"><span id="wbemFlagForwardOnly"></span><span id="wbemflagforwardonly"></span><span id="WBEMFLAGFORWARDONLY"></span>\*\*\*\*wbemFlagForwardOnly\*\*\*\* (32 (0x20))</span></span>


</dt> <dd>

<span data-ttu-id="6eaa8-116">Вызывает возврат перечислителя "только вперед".</span><span class="sxs-lookup"><span data-stu-id="6eaa8-116">Causes a forward-only enumerator to be returned.</span></span> <span data-ttu-id="6eaa8-117">Перечислители "только вперед" обычно выполняются гораздо быстрее и используют меньше памяти, чем обычные перечислители, но они не допускают вызовов [**SWbemObject. Clone \_**](swbemobject-clone-.md).</span><span class="sxs-lookup"><span data-stu-id="6eaa8-117">Forward-only enumerators are generally much faster and use less memory than conventional enumerators, but they do not allow calls to [**SWbemObject.Clone\_**](swbemobject-clone-.md).</span></span>

</dd> <dt>

<span id="wbemFlagBidirectional"></span><span id="wbemflagbidirectional"></span><span id="WBEMFLAGBIDIRECTIONAL"></span>

<span data-ttu-id="6eaa8-118"><span id="wbemFlagBidirectional"></span><span id="wbemflagbidirectional"></span><span id="WBEMFLAGBIDIRECTIONAL"></span>Вбемфлагбидиректионал \* \* \* \* (0 (0x0))</span><span class="sxs-lookup"><span data-stu-id="6eaa8-118"><span id="wbemFlagBidirectional"></span><span id="wbemflagbidirectional"></span><span id="WBEMFLAGBIDIRECTIONAL"></span>\*\*\*\*wbemFlagBidirectional\*\*\*\* (0 (0x0))</span></span>


</dt> <dd>

<span data-ttu-id="6eaa8-119">Заставляет Инструментарий WMI хранить указатели на объекты перечисления до тех пор, пока клиент не освободит перечислитель.</span><span class="sxs-lookup"><span data-stu-id="6eaa8-119">Causes WMI to retain pointers to objects of the enumeration until the client releases the enumerator.</span></span>

</dd> <dt>

<span id="wbemFlagReturnImmediately"></span><span id="wbemflagreturnimmediately"></span><span id="WBEMFLAGRETURNIMMEDIATELY"></span>

<span data-ttu-id="6eaa8-120"><span id="wbemFlagReturnImmediately"></span><span id="wbemflagreturnimmediately"></span><span id="WBEMFLAGRETURNIMMEDIATELY"></span>Вбемфлагретурниммедиатели \* \* \* \* (16 (0x10))</span><span class="sxs-lookup"><span data-stu-id="6eaa8-120"><span id="wbemFlagReturnImmediately"></span><span id="wbemflagreturnimmediately"></span><span id="WBEMFLAGRETURNIMMEDIATELY"></span>\*\*\*\*wbemFlagReturnImmediately\*\*\*\* (16 (0x10))</span></span>


</dt> <dd>

<span data-ttu-id="6eaa8-121">Значение по умолчанию для этого параметра.</span><span class="sxs-lookup"><span data-stu-id="6eaa8-121">Default value for this parameter.</span></span> <span data-ttu-id="6eaa8-122">Этот флаг приводит к немедленному возврату вызова.</span><span class="sxs-lookup"><span data-stu-id="6eaa8-122">This flag causes the call to return immediately.</span></span>

</dd> <dt>

<span id="wbemFlagReturnWhenComplete"></span><span id="wbemflagreturnwhencomplete"></span><span id="WBEMFLAGRETURNWHENCOMPLETE"></span>

<span data-ttu-id="6eaa8-123"><span id="wbemFlagReturnWhenComplete"></span><span id="wbemflagreturnwhencomplete"></span><span id="WBEMFLAGRETURNWHENCOMPLETE"></span>Вбемфлагретурнвхенкомплете \* \* \* \* (0 (0x0))</span><span class="sxs-lookup"><span data-stu-id="6eaa8-123"><span id="wbemFlagReturnWhenComplete"></span><span id="wbemflagreturnwhencomplete"></span><span id="WBEMFLAGRETURNWHENCOMPLETE"></span>\*\*\*\*wbemFlagReturnWhenComplete\*\*\*\* ( 0 (0x0))</span></span>


</dt> <dd>

<span data-ttu-id="6eaa8-124">Вызывает блокирование этого вызова до тех пор, пока запрос не будет завершен.</span><span class="sxs-lookup"><span data-stu-id="6eaa8-124">Causes this call to block until the query has completed.</span></span>

</dd> <dt>

<span id="wbemQueryFlagShallow"></span><span id="wbemqueryflagshallow"></span><span id="WBEMQUERYFLAGSHALLOW"></span>

<span data-ttu-id="6eaa8-125"><span id="wbemQueryFlagShallow"></span><span id="wbemqueryflagshallow"></span><span id="WBEMQUERYFLAGSHALLOW"></span>Вбемкуерифлагшаллов \* \* \* \* (1 (0x1))</span><span class="sxs-lookup"><span data-stu-id="6eaa8-125"><span id="wbemQueryFlagShallow"></span><span id="wbemqueryflagshallow"></span><span id="WBEMQUERYFLAGSHALLOW"></span>\*\*\*\*wbemQueryFlagShallow\*\*\*\* (1 (0x1))</span></span>


</dt> <dd>

<span data-ttu-id="6eaa8-126">Заставляет перечисление включать только непосредственные подклассы указанного родительского класса.</span><span class="sxs-lookup"><span data-stu-id="6eaa8-126">Forces the enumeration to include only immediate subclasses of the specified parent class.</span></span>

</dd> <dt>

<span id="wbemQueryFlagDeep"></span><span id="wbemqueryflagdeep"></span><span id="WBEMQUERYFLAGDEEP"></span>

<span data-ttu-id="6eaa8-127"><span id="wbemQueryFlagDeep"></span><span id="wbemqueryflagdeep"></span><span id="WBEMQUERYFLAGDEEP"></span>Вбемкуерифлагдип \* \* \* \* (0 (0x0))</span><span class="sxs-lookup"><span data-stu-id="6eaa8-127"><span id="wbemQueryFlagDeep"></span><span id="wbemqueryflagdeep"></span><span id="WBEMQUERYFLAGDEEP"></span>\*\*\*\*wbemQueryFlagDeep\*\*\*\* (0 (0x0))</span></span>


</dt> <dd>

<span data-ttu-id="6eaa8-128">Значение по умолчанию для этого параметра.</span><span class="sxs-lookup"><span data-stu-id="6eaa8-128">Default for this parameter.</span></span> <span data-ttu-id="6eaa8-129">Это значение приводит к включению в перечисление всех классов в иерархии.</span><span class="sxs-lookup"><span data-stu-id="6eaa8-129">This value forces the enumeration to include all classes in the hierarchy.</span></span>

</dd> <dt>

<span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>

<span data-ttu-id="6eaa8-130"><span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>Вбемфлагусеамендедкуалифиерс \* \* \* \* (131072 (0x20000))</span><span class="sxs-lookup"><span data-stu-id="6eaa8-130"><span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>\*\*\*\*wbemFlagUseAmendedQualifiers\*\*\*\* (131072 (0x20000))</span></span>


</dt> <dd>

<span data-ttu-id="6eaa8-131">Заставляет WMI возвращать данные о поправности класса с определением базового класса.</span><span class="sxs-lookup"><span data-stu-id="6eaa8-131">Causes WMI to return class amendment data with the base class definition.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="6eaa8-132">*обжвбемнамедвалуесет* \[ в необязательное\]</span><span class="sxs-lookup"><span data-stu-id="6eaa8-132">*objwbemNamedValueSet* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="6eaa8-133">Как правило, это не определено.</span><span class="sxs-lookup"><span data-stu-id="6eaa8-133">Typically, this is undefined.</span></span> <span data-ttu-id="6eaa8-134">В противном случае это объект [**свбемнамедвалуесет**](swbemnamedvalueset.md) , элементы которого представляют сведения о контексте, которые могут использоваться поставщиком, обслуживающим запрос.</span><span class="sxs-lookup"><span data-stu-id="6eaa8-134">Otherwise, this is an [**SWbemNamedValueSet**](swbemnamedvalueset.md) object whose elements represent the context information that can be used by the provider that is servicing the request.</span></span> <span data-ttu-id="6eaa8-135">Поставщик, который поддерживает или требует такую информацию, должен документировать распознанные имена значений, тип данных значения, допустимые значения и семантику.</span><span class="sxs-lookup"><span data-stu-id="6eaa8-135">A provider that supports or requires such information must document the recognized value names, data type of the value, allowed values, and semantics.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6eaa8-136">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="6eaa8-136">Return value</span></span>

<span data-ttu-id="6eaa8-137">Если метод выполнен успешно, объект [**SWbemObjectSet**](swbemobjectset.md) возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="6eaa8-137">If the method is successful, an [**SWbemObjectSet**](swbemobjectset.md) object returns.</span></span>

## <a name="error-codes"></a><span data-ttu-id="6eaa8-138">Коды ошибок</span><span class="sxs-lookup"><span data-stu-id="6eaa8-138">Error codes</span></span>

<span data-ttu-id="6eaa8-139">После завершения метода **Instances \_** объект **Err** может содержать один из кодов ошибок из следующего списка.</span><span class="sxs-lookup"><span data-stu-id="6eaa8-139">After the completion of the **Instances\_** method, the **Err** object may contain one of the error codes in the following list.</span></span>

<dl> <dt>

<span data-ttu-id="6eaa8-140">**вбемерракцессдениед** -2147749891 (0x80041003)</span><span class="sxs-lookup"><span data-stu-id="6eaa8-140">**wbemErrAccessDenied** - 2147749891 (0x80041003)</span></span>
</dt> <dd>

<span data-ttu-id="6eaa8-141">У текущего пользователя нет разрешения на просмотр экземпляров указанного класса.</span><span class="sxs-lookup"><span data-stu-id="6eaa8-141">Current user does not have permission to view instances of the specified class.</span></span>

</dd> <dt>

<span data-ttu-id="6eaa8-142">**вбемеррфаилед** -2147749889 (0x80041001)</span><span class="sxs-lookup"><span data-stu-id="6eaa8-142">**wbemErrFailed** - 2147749889 (0x80041001)</span></span>
</dt> <dd>

<span data-ttu-id="6eaa8-143">Произошла неопределенная ошибка.</span><span class="sxs-lookup"><span data-stu-id="6eaa8-143">Unspecified error occurred.</span></span>

</dd> <dt>

<span data-ttu-id="6eaa8-144">**вбемерринвалидкласс** -2147749904 (0x80041010)</span><span class="sxs-lookup"><span data-stu-id="6eaa8-144">**wbemErrInvalidClass** - 2147749904 (0x80041010)</span></span>
</dt> <dd>

<span data-ttu-id="6eaa8-145">Указан недопустимый класс.</span><span class="sxs-lookup"><span data-stu-id="6eaa8-145">Specified class is not valid.</span></span>

</dd> <dt>

<span data-ttu-id="6eaa8-146">**вбемерринвалидпараметер** -2147749896 (0x80041008)</span><span class="sxs-lookup"><span data-stu-id="6eaa8-146">**wbemErrInvalidParameter** - 2147749896 (0x80041008)</span></span>
</dt> <dd>

<span data-ttu-id="6eaa8-147">Указан недопустимый параметр.</span><span class="sxs-lookup"><span data-stu-id="6eaa8-147">A specified parameter is not valid.</span></span>

</dd> <dt>

<span data-ttu-id="6eaa8-148">**вбемерраутофмемори** -2147749894 (0x80041006)</span><span class="sxs-lookup"><span data-stu-id="6eaa8-148">**wbemErrOutOfMemory** - 2147749894 (0x80041006)</span></span>
</dt> <dd>

<span data-ttu-id="6eaa8-149">Недостаточно памяти для завершения операции.</span><span class="sxs-lookup"><span data-stu-id="6eaa8-149">Not enough memory to complete the operation.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="6eaa8-150">Комментарии</span><span class="sxs-lookup"><span data-stu-id="6eaa8-150">Remarks</span></span>

<span data-ttu-id="6eaa8-151">Метод **Instances \_** работает только для объектов класса.</span><span class="sxs-lookup"><span data-stu-id="6eaa8-151">The **Instances\_** method only works for class objects.</span></span> <span data-ttu-id="6eaa8-152">Возвращаемая коллекция не содержит нулевых элементов.</span><span class="sxs-lookup"><span data-stu-id="6eaa8-152">It is not an error for the returned collection to have zero elements.</span></span> <span data-ttu-id="6eaa8-153">Поведение по умолчанию для этого метода — [*семисинчронаус*](gloss-s.md) из-за значения *ифлагс* по умолчанию **вбемфлагретурниммедиатели**.</span><span class="sxs-lookup"><span data-stu-id="6eaa8-153">The default behavior for this method is [*semisynchronous*](gloss-s.md) because of the default *IFlags* value **wbemFlagReturnImmediately**.</span></span>

## <a name="requirements"></a><span data-ttu-id="6eaa8-154">Требования</span><span class="sxs-lookup"><span data-stu-id="6eaa8-154">Requirements</span></span>



| <span data-ttu-id="6eaa8-155">Требование</span><span class="sxs-lookup"><span data-stu-id="6eaa8-155">Requirement</span></span> | <span data-ttu-id="6eaa8-156">Значение</span><span class="sxs-lookup"><span data-stu-id="6eaa8-156">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="6eaa8-157">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="6eaa8-157">Minimum supported client</span></span><br/> | <span data-ttu-id="6eaa8-158">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="6eaa8-158">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="6eaa8-159">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="6eaa8-159">Minimum supported server</span></span><br/> | <span data-ttu-id="6eaa8-160">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="6eaa8-160">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="6eaa8-161">Header</span><span class="sxs-lookup"><span data-stu-id="6eaa8-161">Header</span></span><br/>                   | <dl> <span data-ttu-id="6eaa8-162"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="6eaa8-162"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="6eaa8-163">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="6eaa8-163">Type library</span></span><br/>             | <dl> <span data-ttu-id="6eaa8-164"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="6eaa8-164"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="6eaa8-165">DLL</span><span class="sxs-lookup"><span data-stu-id="6eaa8-165">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6eaa8-166"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6eaa8-166"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="6eaa8-167">CLSID</span><span class="sxs-lookup"><span data-stu-id="6eaa8-167">CLSID</span></span><br/>                    | <span data-ttu-id="6eaa8-168">\_SWBEMOBJECT CLSID</span><span class="sxs-lookup"><span data-stu-id="6eaa8-168">CLSID\_SWbemObject</span></span><br/>                                                           |
| <span data-ttu-id="6eaa8-169">IID</span><span class="sxs-lookup"><span data-stu-id="6eaa8-169">IID</span></span><br/>                      | <span data-ttu-id="6eaa8-170">IID \_ исвбемобжект</span><span class="sxs-lookup"><span data-stu-id="6eaa8-170">IID\_ISWbemObject</span></span><br/>                                                            |



## <a name="see-also"></a><span data-ttu-id="6eaa8-171">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="6eaa8-171">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6eaa8-172">**SWbemObject**</span><span class="sxs-lookup"><span data-stu-id="6eaa8-172">**SWbemObject**</span></span>](swbemobject.md)
</dt> <dt>

[<span data-ttu-id="6eaa8-173">**SWbemObjectSet**</span><span class="sxs-lookup"><span data-stu-id="6eaa8-173">**SWbemObjectSet**</span></span>](swbemobjectset.md)
</dt> </dl>

 

 




