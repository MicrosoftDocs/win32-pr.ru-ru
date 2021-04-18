---
description: Метод подклассов \_ объекта SWbemObject возвращает объект SWbemObjectSet.
ms.assetid: c17e5d4a-016f-42ae-bc11-e21a44772ce5
ms.tgt_platform: multiple
title: Метод SWbemObject.Subclasses_ (Wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemObject.Subclasses_
- ISWbemObject.Subclasses_
- ISWbemObject.Subclasses_
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: efae27b26235cbf1c298c7b45de69e1cf49c8570
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105692696"
---
# <a name="swbemobjectsubclasses_-method"></a><span data-ttu-id="9cf1f-103">Метод SWbemObject. подклассов \_</span><span class="sxs-lookup"><span data-stu-id="9cf1f-103">SWbemObject.Subclasses\_ method</span></span>

<span data-ttu-id="9cf1f-104">Метод **подклассов \_** объекта [**SWbemObject**](swbemobject.md) возвращает объект [**SWbemObjectSet**](swbemobjectset.md) .</span><span class="sxs-lookup"><span data-stu-id="9cf1f-104">The **Subclasses\_** method of the [**SWbemObject**](swbemobject.md) object returns an [**SWbemObjectSet**](swbemobjectset.md) object.</span></span> <span data-ttu-id="9cf1f-105">Этот объект представляет собой коллекцию подклассов текущего объекта, который должен быть классом.</span><span class="sxs-lookup"><span data-stu-id="9cf1f-105">This object is a collection of subclasses of the current object, which must be a class.</span></span> <span data-ttu-id="9cf1f-106">Элементы в возвращаемой коллекции можно получить с помощью стандартных методов сбора.</span><span class="sxs-lookup"><span data-stu-id="9cf1f-106">Items in the returned collection can be obtained using standard collection methods.</span></span> <span data-ttu-id="9cf1f-107">Дополнительные сведения см. [в разделе доступ к коллекции](accessing-a-collection.md).</span><span class="sxs-lookup"><span data-stu-id="9cf1f-107">For more information, see [Accessing a Collection](accessing-a-collection.md).</span></span>

<span data-ttu-id="9cf1f-108">Описание этого синтаксиса см. в разделе [соглашения о документе для API скриптов](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="9cf1f-108">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="9cf1f-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="9cf1f-109">Syntax</span></span>


```VB
objWbemObjectSet = .Subclasses_( _
  [ ByVal iFlags ], _
  [ ByVal objwbemNamedValueSet ] _
)
```



## <a name="parameters"></a><span data-ttu-id="9cf1f-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="9cf1f-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9cf1f-111">*ифлагс* \[ в необязательное\]</span><span class="sxs-lookup"><span data-stu-id="9cf1f-111">*iFlags* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="9cf1f-112">Целое число, определяющее, как детально перечисляются вызовы.</span><span class="sxs-lookup"><span data-stu-id="9cf1f-112">Integer that determines how detailed the call enumerates.</span></span> <span data-ttu-id="9cf1f-113">Этот параметр может принимать следующие значения.</span><span class="sxs-lookup"><span data-stu-id="9cf1f-113">This parameter can accept the following values.</span></span>

<dt>

<span id="wbemQueryFlagDeep"></span><span id="wbemqueryflagdeep"></span><span id="WBEMQUERYFLAGDEEP"></span>

<span data-ttu-id="9cf1f-114"><span id="wbemQueryFlagDeep"></span><span id="wbemqueryflagdeep"></span><span id="WBEMQUERYFLAGDEEP"></span>Вбемкуерифлагдип \* \* \* \* (0 (0x0))</span><span class="sxs-lookup"><span data-stu-id="9cf1f-114"><span id="wbemQueryFlagDeep"></span><span id="wbemqueryflagdeep"></span><span id="WBEMQUERYFLAGDEEP"></span>\*\*\*\*wbemQueryFlagDeep\*\*\*\* (0 (0x0))</span></span>


</dt> <dd>

<span data-ttu-id="9cf1f-115">Активирует рекурсивное перечисление во всех подклассах, производных от указанного родительского класса.</span><span class="sxs-lookup"><span data-stu-id="9cf1f-115">Forces recursive enumeration into all subclasses derived from the specified parent class.</span></span> <span data-ttu-id="9cf1f-116">Сам родительский класс не возвращается в перечислении.</span><span class="sxs-lookup"><span data-stu-id="9cf1f-116">The parent class itself is not returned in the enumeration.</span></span>

</dd> <dt>

<span id="wbemQueryFlagShallow"></span><span id="wbemqueryflagshallow"></span><span id="WBEMQUERYFLAGSHALLOW"></span>

<span data-ttu-id="9cf1f-117"><span id="wbemQueryFlagShallow"></span><span id="wbemqueryflagshallow"></span><span id="WBEMQUERYFLAGSHALLOW"></span>Вбемкуерифлагшаллов \* \* \* \* (1 (0x1))</span><span class="sxs-lookup"><span data-stu-id="9cf1f-117"><span id="wbemQueryFlagShallow"></span><span id="wbemqueryflagshallow"></span><span id="WBEMQUERYFLAGSHALLOW"></span>\*\*\*\*wbemQueryFlagShallow\*\*\*\* (1 (0x1))</span></span>


</dt> <dd>

<span data-ttu-id="9cf1f-118">Значение по умолчанию для этого параметра.</span><span class="sxs-lookup"><span data-stu-id="9cf1f-118">Default value for this parameter.</span></span> <span data-ttu-id="9cf1f-119">Он заставляет перечисление включать только непосредственные подклассы указанного родительского класса.</span><span class="sxs-lookup"><span data-stu-id="9cf1f-119">It forces the enumeration to include only immediate subclasses of the specified parent class.</span></span>

</dd> <dt>

<span id="WbemFlagReturnImmediately"></span><span id="wbemflagreturnimmediately"></span><span id="WBEMFLAGRETURNIMMEDIATELY"></span>

<span data-ttu-id="9cf1f-120"><span id="WbemFlagReturnImmediately"></span><span id="wbemflagreturnimmediately"></span><span id="WBEMFLAGRETURNIMMEDIATELY"></span>Вбемфлагретурниммедиатели \* \* \* \* (16 (0x10))</span><span class="sxs-lookup"><span data-stu-id="9cf1f-120"><span id="WbemFlagReturnImmediately"></span><span id="wbemflagreturnimmediately"></span><span id="WBEMFLAGRETURNIMMEDIATELY"></span>\*\*\*\*WbemFlagReturnImmediately\*\*\*\* (16 (0x10))</span></span>


</dt> <dd>

<span data-ttu-id="9cf1f-121">Приводит к немедленному возврату вызова</span><span class="sxs-lookup"><span data-stu-id="9cf1f-121">Causes the call to return immediately</span></span>

</dd> <dt>

<span id="wbemFlagReturnWhenComplete"></span><span id="wbemflagreturnwhencomplete"></span><span id="WBEMFLAGRETURNWHENCOMPLETE"></span>

<span data-ttu-id="9cf1f-122"><span id="wbemFlagReturnWhenComplete"></span><span id="wbemflagreturnwhencomplete"></span><span id="WBEMFLAGRETURNWHENCOMPLETE"></span>Вбемфлагретурнвхенкомплете \* \* \* \* (0 (0x0))</span><span class="sxs-lookup"><span data-stu-id="9cf1f-122"><span id="wbemFlagReturnWhenComplete"></span><span id="wbemflagreturnwhencomplete"></span><span id="WBEMFLAGRETURNWHENCOMPLETE"></span>\*\*\*\*wbemFlagReturnWhenComplete\*\*\*\* (0 (0x0))</span></span>


</dt> <dd>

<span data-ttu-id="9cf1f-123">Вызывает блокирование этого вызова до завершения вызова.</span><span class="sxs-lookup"><span data-stu-id="9cf1f-123">Causes this call to block until the call has completed.</span></span>

</dd> <dt>

<span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>

<span data-ttu-id="9cf1f-124"><span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>Вбемфлагусеамендедкуалифиерс \* \* \* \* (131072 (0x20000))</span><span class="sxs-lookup"><span data-stu-id="9cf1f-124"><span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>\*\*\*\*wbemFlagUseAmendedQualifiers\*\*\*\* (131072 (0x20000))</span></span>


</dt> <dd>

<span data-ttu-id="9cf1f-125">Заставляет Инструментарий WMI возвращать данные о поправности классов вместе с определением базового класса.</span><span class="sxs-lookup"><span data-stu-id="9cf1f-125">Causes WMI to return class amendment data along with the base class definition.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="9cf1f-126">*обжвбемнамедвалуесет* \[ в необязательное\]</span><span class="sxs-lookup"><span data-stu-id="9cf1f-126">*objwbemNamedValueSet* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="9cf1f-127">Как правило, это не определено.</span><span class="sxs-lookup"><span data-stu-id="9cf1f-127">Typically, this is undefined.</span></span> <span data-ttu-id="9cf1f-128">В противном случае это объект [**свбемнамедвалуесет**](swbemnamedvalueset.md) , элементы которого представляют сведения о контексте, которые могут использоваться поставщиком, обслуживающим запрос.</span><span class="sxs-lookup"><span data-stu-id="9cf1f-128">Otherwise, this is an [**SWbemNamedValueSet**](swbemnamedvalueset.md) object whose elements represent the context information that can be used by the provider that is servicing the request.</span></span> <span data-ttu-id="9cf1f-129">Поставщик, который поддерживает или требует такую информацию, должен документировать распознанные имена значений, тип данных значения, допустимые значения и семантику.</span><span class="sxs-lookup"><span data-stu-id="9cf1f-129">A provider that supports or requires such information must document the recognized value names, data type of the value, allowed values, and semantics.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9cf1f-130">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="9cf1f-130">Return value</span></span>

<span data-ttu-id="9cf1f-131">Если вызов выполнен успешно, возвращается объект [**SWbemObjectSet**](swbemobjectset.md) .</span><span class="sxs-lookup"><span data-stu-id="9cf1f-131">If the call is successful, an [**SWbemObjectSet**](swbemobjectset.md) object is returned.</span></span>

## <a name="error-codes"></a><span data-ttu-id="9cf1f-132">Коды ошибок</span><span class="sxs-lookup"><span data-stu-id="9cf1f-132">Error codes</span></span>

<span data-ttu-id="9cf1f-133">После завершения метода **подклассов \_** объект **Err** может содержать один из кодов ошибок из следующего списка.</span><span class="sxs-lookup"><span data-stu-id="9cf1f-133">After the completion of the **Subclasses\_** method, the **Err** object may contain one of the error codes in the following list.</span></span>

<dl> <dt>

<span data-ttu-id="9cf1f-134">**вбемерракцессдениед** -2147749891 (0x80041003)</span><span class="sxs-lookup"><span data-stu-id="9cf1f-134">**wbemErrAccessDenied** - 2147749891 (0x80041003)</span></span>
</dt> <dd>

<span data-ttu-id="9cf1f-135">У текущего пользователя нет разрешения на просмотр одного или нескольких классов, возвращенных вызовом.</span><span class="sxs-lookup"><span data-stu-id="9cf1f-135">Current user does not have permission to view one or more of the classes returned by the call.</span></span>

</dd> <dt>

<span data-ttu-id="9cf1f-136">**вбемеррфаилед** -2147749889 (0x80041001)</span><span class="sxs-lookup"><span data-stu-id="9cf1f-136">**wbemErrFailed** - 2147749889 (0x80041001)</span></span>
</dt> <dd>

<span data-ttu-id="9cf1f-137">Незаданная ошибка.</span><span class="sxs-lookup"><span data-stu-id="9cf1f-137">Unspecified error.</span></span>

</dd> <dt>

<span data-ttu-id="9cf1f-138">**вбемерринвалидкласс** -2147749904 (0x80041010)</span><span class="sxs-lookup"><span data-stu-id="9cf1f-138">**wbemErrInvalidClass** - 2147749904 (0x80041010)</span></span>
</dt> <dd>

<span data-ttu-id="9cf1f-139">Указанный класс не существует.</span><span class="sxs-lookup"><span data-stu-id="9cf1f-139">Specified class did not exist.</span></span>

</dd> <dt>

<span data-ttu-id="9cf1f-140">**вбемерринвалидпараметер** -2147749896 (0x80041008)</span><span class="sxs-lookup"><span data-stu-id="9cf1f-140">**wbemErrInvalidParameter** - 2147749896 (0x80041008)</span></span>
</dt> <dd>

<span data-ttu-id="9cf1f-141">Указан недопустимый параметр.</span><span class="sxs-lookup"><span data-stu-id="9cf1f-141">Invalid parameter was specified.</span></span>

</dd> <dt>

<span data-ttu-id="9cf1f-142">**вбемерраутофмемори** -2147749894 (0x80041006)</span><span class="sxs-lookup"><span data-stu-id="9cf1f-142">**wbemErrOutOfMemory** - 2147749894 (0x80041006)</span></span>
</dt> <dd>

<span data-ttu-id="9cf1f-143">Недостаточно памяти для завершения операции.</span><span class="sxs-lookup"><span data-stu-id="9cf1f-143">Not enough memory to complete the operation.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="9cf1f-144">Комментарии</span><span class="sxs-lookup"><span data-stu-id="9cf1f-144">Remarks</span></span>

<span data-ttu-id="9cf1f-145">Если в возвращаемой коллекции нет подклассов текущего объекта, то не будет возвращать нулевые элементы.</span><span class="sxs-lookup"><span data-stu-id="9cf1f-145">It is not an error for the returned collection to have zero elements if there are no subclasses of the current object.</span></span> <span data-ttu-id="9cf1f-146">Метод **подклассов \_** работает только для объектов класса.</span><span class="sxs-lookup"><span data-stu-id="9cf1f-146">The **Subclasses\_** method only works for class objects.</span></span>

## <a name="requirements"></a><span data-ttu-id="9cf1f-147">Требования</span><span class="sxs-lookup"><span data-stu-id="9cf1f-147">Requirements</span></span>



| <span data-ttu-id="9cf1f-148">Требование</span><span class="sxs-lookup"><span data-stu-id="9cf1f-148">Requirement</span></span> | <span data-ttu-id="9cf1f-149">Значение</span><span class="sxs-lookup"><span data-stu-id="9cf1f-149">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="9cf1f-150">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="9cf1f-150">Minimum supported client</span></span><br/> | <span data-ttu-id="9cf1f-151">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="9cf1f-151">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="9cf1f-152">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="9cf1f-152">Minimum supported server</span></span><br/> | <span data-ttu-id="9cf1f-153">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="9cf1f-153">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="9cf1f-154">Header</span><span class="sxs-lookup"><span data-stu-id="9cf1f-154">Header</span></span><br/>                   | <dl> <span data-ttu-id="9cf1f-155"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="9cf1f-155"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="9cf1f-156">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="9cf1f-156">Type library</span></span><br/>             | <dl> <span data-ttu-id="9cf1f-157"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="9cf1f-157"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="9cf1f-158">DLL</span><span class="sxs-lookup"><span data-stu-id="9cf1f-158">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9cf1f-159"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9cf1f-159"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="9cf1f-160">CLSID</span><span class="sxs-lookup"><span data-stu-id="9cf1f-160">CLSID</span></span><br/>                    | <span data-ttu-id="9cf1f-161">\_SWBEMOBJECT CLSID</span><span class="sxs-lookup"><span data-stu-id="9cf1f-161">CLSID\_SWbemObject</span></span><br/>                                                           |
| <span data-ttu-id="9cf1f-162">IID</span><span class="sxs-lookup"><span data-stu-id="9cf1f-162">IID</span></span><br/>                      | <span data-ttu-id="9cf1f-163">IID \_ исвбемобжект</span><span class="sxs-lookup"><span data-stu-id="9cf1f-163">IID\_ISWbemObject</span></span><br/>                                                            |



## <a name="see-also"></a><span data-ttu-id="9cf1f-164">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="9cf1f-164">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9cf1f-165">**SWbemObject**</span><span class="sxs-lookup"><span data-stu-id="9cf1f-165">**SWbemObject**</span></span>](swbemobject.md)
</dt> <dt>

[<span data-ttu-id="9cf1f-166">**SWbemObjectSet**</span><span class="sxs-lookup"><span data-stu-id="9cf1f-166">**SWbemObjectSet**</span></span>](swbemobjectset.md)
</dt> </dl>

 

 




