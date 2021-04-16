---
description: Метод Add объекта SWbemPropertySet добавляет объект SWbemProperty в коллекцию SWbemPropertySet. Если свойство с таким именем уже существует в коллекции, его содержимое заменяется новым определением.
ms.assetid: 52a5f964-3d53-441b-9a58-650afdc5b1b9
ms.tgt_platform: multiple
title: Метод SWbemPropertySet. Add (Wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemPropertySet.Add
- ISWbemPropertySet.Add
- ISWbemPropertySet.Add
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 1ad5b40d31d162b287bdb1a387cd0602e0be1ce6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105712895"
---
# <a name="swbempropertysetadd-method"></a><span data-ttu-id="d8352-104">SWbemPropertySet. Add, метод</span><span class="sxs-lookup"><span data-stu-id="d8352-104">SWbemPropertySet.Add method</span></span>

<span data-ttu-id="d8352-105">Метод **Add** объекта [**SWbemPropertySet**](swbempropertyset.md) добавляет объект [**SWbemProperty**](swbemproperty.md) в коллекцию **SWbemPropertySet** .</span><span class="sxs-lookup"><span data-stu-id="d8352-105">The **Add** method of the [**SWbemPropertySet**](swbempropertyset.md) object adds an [**SWbemProperty**](swbemproperty.md) object to the **SWbemPropertySet** collection.</span></span> <span data-ttu-id="d8352-106">Если свойство с таким именем уже существует в коллекции, его содержимое заменяется новым определением.</span><span class="sxs-lookup"><span data-stu-id="d8352-106">If a property with the same name already exists in the collection, its contents are replaced with the new definition.</span></span>

> [!Note]  
> <span data-ttu-id="d8352-107">После этой операции значение добавленного свойства равно **null** (не назначено).</span><span class="sxs-lookup"><span data-stu-id="d8352-107">The value of the added property is **NULL** (unassigned) after this operation.</span></span> <span data-ttu-id="d8352-108">Чтобы задать или изменить значение свойства WMI, необходимо задать свойство [**value**](swbemdatetime-value.md) возвращаемого объекта [**SWbemProperty**](swbemproperty.md) .</span><span class="sxs-lookup"><span data-stu-id="d8352-108">To set or change the value of a WMI property, you must set the [**Value**](swbemdatetime-value.md) property of the returned [**SWbemProperty**](swbemproperty.md) object.</span></span>

 

<span data-ttu-id="d8352-109">Описание этого синтаксиса см. в разделе [соглашения о документе для API скриптов](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="d8352-109">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="d8352-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="d8352-110">Syntax</span></span>


```VB
objProperty = .Add( _
  ByVal strName, _
  ByVal iCIMType, _
  [ ByVal bIsArray ], _
  [ ByVal iFlags ] _
)
```



## <a name="parameters"></a><span data-ttu-id="d8352-111">Параметры</span><span class="sxs-lookup"><span data-stu-id="d8352-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d8352-112">*strName* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="d8352-112">*strName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d8352-113">Обязательный.</span><span class="sxs-lookup"><span data-stu-id="d8352-113">Required.</span></span> <span data-ttu-id="d8352-114">Имя нового свойства.</span><span class="sxs-lookup"><span data-stu-id="d8352-114">Name of the new property.</span></span>

</dd> <dt>

<span data-ttu-id="d8352-115">*иЦимтипе* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="d8352-115">*iCIMType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d8352-116">Обязательный.</span><span class="sxs-lookup"><span data-stu-id="d8352-116">Required.</span></span> <span data-ttu-id="d8352-117">Целое число, представляющее квалификатор **Цимтипе** нового свойства.</span><span class="sxs-lookup"><span data-stu-id="d8352-117">An integer that represents the **CIMType** qualifier of the new property.</span></span> <span data-ttu-id="d8352-118">См. [**вбемЦимтипинум**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemcimtypeenum) для списка с квалификаторами **Цимтипе** и их значениями.</span><span class="sxs-lookup"><span data-stu-id="d8352-118">See [**WbemCimTypeEnum**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemcimtypeenum) for the list with the **CIMType** qualifiers and their values.</span></span>

</dd> <dt>

<span data-ttu-id="d8352-119">*бисаррай* \[ в необязательное\]</span><span class="sxs-lookup"><span data-stu-id="d8352-119">*bIsArray* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="d8352-120">Указывает, является ли свойство типом массива.</span><span class="sxs-lookup"><span data-stu-id="d8352-120">Specifies whether the property is an array type.</span></span> <span data-ttu-id="d8352-121">Значение по умолчанию для этого параметра — **false**.</span><span class="sxs-lookup"><span data-stu-id="d8352-121">The default value for this parameter is **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="d8352-122">*ифлагс* \[ в необязательное\]</span><span class="sxs-lookup"><span data-stu-id="d8352-122">*iFlags* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="d8352-123">Зарезервировано и должно быть равно нулю, если указано.</span><span class="sxs-lookup"><span data-stu-id="d8352-123">Reserved and must be zero if specified.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d8352-124">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="d8352-124">Return value</span></span>

<span data-ttu-id="d8352-125">В случае успеха этот метод возвращает объект [**SWbemProperty**](swbemproperty.md) , представляющий новое свойство.</span><span class="sxs-lookup"><span data-stu-id="d8352-125">If successful, this method returns an [**SWbemProperty**](swbemproperty.md) object that represents the new property.</span></span> <span data-ttu-id="d8352-126">В противном случае возвращается **пустой** объект.</span><span class="sxs-lookup"><span data-stu-id="d8352-126">Otherwise, a **null** object is returned.</span></span>

## <a name="error-codes"></a><span data-ttu-id="d8352-127">Коды ошибок</span><span class="sxs-lookup"><span data-stu-id="d8352-127">Error codes</span></span>

<span data-ttu-id="d8352-128">После завершения метода **Add** объект **Err** может содержать один из кодов ошибок, приведенных ниже.</span><span class="sxs-lookup"><span data-stu-id="d8352-128">After completion of the **Add** method, the **Err** object may contain one of the error codes below.</span></span>

<dl> <dt>

<span data-ttu-id="d8352-129">**вбемеррфаилед** -2147749889 (0x80041001)</span><span class="sxs-lookup"><span data-stu-id="d8352-129">**wbemErrFailed** - 2147749889 (0x80041001)</span></span>
</dt> <dd>

<span data-ttu-id="d8352-130">Неопределенный сбой.</span><span class="sxs-lookup"><span data-stu-id="d8352-130">Unspecified failure.</span></span>

</dd> <dt>

<span data-ttu-id="d8352-131">**вбемерринвалидпараметер** -2147749896 (0x80041008)</span><span class="sxs-lookup"><span data-stu-id="d8352-131">**wbemErrInvalidParameter** - 2147749896 (0x80041008)</span></span>
</dt> <dd>

<span data-ttu-id="d8352-132">Указан недопустимый параметр.</span><span class="sxs-lookup"><span data-stu-id="d8352-132">Invalid parameter was specified.</span></span>

</dd> <dt>

<span data-ttu-id="d8352-133">**вбемерраутофмемори** -2147749894 (0x80041006)</span><span class="sxs-lookup"><span data-stu-id="d8352-133">**wbemErrOutOfMemory** - 2147749894 (0x80041006)</span></span>
</dt> <dd>

<span data-ttu-id="d8352-134">Недостаточно памяти для выполнения этого метода.</span><span class="sxs-lookup"><span data-stu-id="d8352-134">Not enough memory for this method to execute.</span></span>

</dd> <dt>

<span data-ttu-id="d8352-135">**вбемерринвалидпропертитипе** -2147749930</span><span class="sxs-lookup"><span data-stu-id="d8352-135">**wbemErrInvalidPropertyType** - 2147749930</span></span>
</dt> <dd>

<span data-ttu-id="d8352-136">Квалификатор **Цимтипе** не распознан.</span><span class="sxs-lookup"><span data-stu-id="d8352-136">The **CIMType** qualifier is not recognized.</span></span>

</dd> </dl>

## <a name="examples"></a><span data-ttu-id="d8352-137">Примеры</span><span class="sxs-lookup"><span data-stu-id="d8352-137">Examples</span></span>

<span data-ttu-id="d8352-138">Пример кода, в котором используется этот метод, см. в разделе [**SWbemPropertySet**](swbempropertyset.md) .</span><span class="sxs-lookup"><span data-stu-id="d8352-138">For a code example that uses this method, see the [**SWbemPropertySet**](swbempropertyset.md) topic.</span></span>

## <a name="requirements"></a><span data-ttu-id="d8352-139">Требования</span><span class="sxs-lookup"><span data-stu-id="d8352-139">Requirements</span></span>



| <span data-ttu-id="d8352-140">Требование</span><span class="sxs-lookup"><span data-stu-id="d8352-140">Requirement</span></span> | <span data-ttu-id="d8352-141">Значение</span><span class="sxs-lookup"><span data-stu-id="d8352-141">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="d8352-142">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="d8352-142">Minimum supported client</span></span><br/> | <span data-ttu-id="d8352-143">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="d8352-143">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="d8352-144">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="d8352-144">Minimum supported server</span></span><br/> | <span data-ttu-id="d8352-145">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="d8352-145">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="d8352-146">Header</span><span class="sxs-lookup"><span data-stu-id="d8352-146">Header</span></span><br/>                   | <dl> <span data-ttu-id="d8352-147"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="d8352-147"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="d8352-148">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="d8352-148">Type library</span></span><br/>             | <dl> <span data-ttu-id="d8352-149"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="d8352-149"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="d8352-150">DLL</span><span class="sxs-lookup"><span data-stu-id="d8352-150">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d8352-151"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d8352-151"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="d8352-152">CLSID</span><span class="sxs-lookup"><span data-stu-id="d8352-152">CLSID</span></span><br/>                    | <span data-ttu-id="d8352-153">\_SWBEMPROPERTYSET CLSID</span><span class="sxs-lookup"><span data-stu-id="d8352-153">CLSID\_SWbemPropertySet</span></span><br/>                                                      |
| <span data-ttu-id="d8352-154">IID</span><span class="sxs-lookup"><span data-stu-id="d8352-154">IID</span></span><br/>                      | <span data-ttu-id="d8352-155">IID \_ исвбемпропертисет</span><span class="sxs-lookup"><span data-stu-id="d8352-155">IID\_ISWbemPropertySet</span></span><br/>                                                       |



## <a name="see-also"></a><span data-ttu-id="d8352-156">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="d8352-156">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d8352-157">**SWbemPropertySet**</span><span class="sxs-lookup"><span data-stu-id="d8352-157">**SWbemPropertySet**</span></span>](swbempropertyset.md)
</dt> <dt>

[<span data-ttu-id="d8352-158">**SWbemPropertySet. Remove**</span><span class="sxs-lookup"><span data-stu-id="d8352-158">**SWbemPropertySet.Remove**</span></span>](swbempropertyset-remove.md)
</dt> <dt>

[<span data-ttu-id="d8352-159">**SWbemProperty. Value**</span><span class="sxs-lookup"><span data-stu-id="d8352-159">**SWbemProperty.Value**</span></span>](swbemproperty-value.md)
</dt> </dl>

 

 




