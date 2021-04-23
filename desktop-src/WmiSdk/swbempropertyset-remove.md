---
description: Метод Remove объекта SWbemPropertySet Удаляет свойство из коллекции SWbemPropertySet.
ms.assetid: 2a1005db-033c-48f9-8ea0-0bd43b8c989f
ms.tgt_platform: multiple
title: Метод SWbemPropertySet. Remove (Wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemPropertySet.Remove
- ISWbemPropertySet.Remove
- ISWbemPropertySet.Remove
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 5b6903ae05c801d5903754ef8df0bb02cad51204
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104155826"
---
# <a name="swbempropertysetremove-method"></a><span data-ttu-id="846c2-103">SWbemPropertySet. Remove, метод</span><span class="sxs-lookup"><span data-stu-id="846c2-103">SWbemPropertySet.Remove method</span></span>

<span data-ttu-id="846c2-104">Метод **Remove** объекта [**SWbemPropertySet**](swbempropertyset.md) Удаляет свойство из коллекции **SWbemPropertySet** .</span><span class="sxs-lookup"><span data-stu-id="846c2-104">The **Remove** method of the [**SWbemPropertySet**](swbempropertyset.md) object deletes a property from the **SWbemPropertySet** collection.</span></span>

<span data-ttu-id="846c2-105">Описание этого синтаксиса см. в разделе [соглашения о документе для API скриптов](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="846c2-105">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="846c2-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="846c2-106">Syntax</span></span>


```VB
SWbemPropertySet.Remove( _
  ByVal strName, _
  [ ByVal iFlags ] _
)
```



## <a name="parameters"></a><span data-ttu-id="846c2-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="846c2-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="846c2-108">*strName* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="846c2-108">*strName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="846c2-109">Обязательный.</span><span class="sxs-lookup"><span data-stu-id="846c2-109">Required.</span></span> <span data-ttu-id="846c2-110">Имя удаляемого элемента.</span><span class="sxs-lookup"><span data-stu-id="846c2-110">Name of the item to remove.</span></span>

</dd> <dt>

<span data-ttu-id="846c2-111">*ифлагс* \[ в необязательное\]</span><span class="sxs-lookup"><span data-stu-id="846c2-111">*iFlags* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="846c2-112">Зарезервировано.</span><span class="sxs-lookup"><span data-stu-id="846c2-112">Reserved.</span></span> <span data-ttu-id="846c2-113">Если указано, это значение должно быть равно 0 (нулю).</span><span class="sxs-lookup"><span data-stu-id="846c2-113">This value must be 0 (zero) if specified.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="846c2-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="846c2-114">Return value</span></span>

<span data-ttu-id="846c2-115">Этот метод не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="846c2-115">This method does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="846c2-116">Коды ошибок</span><span class="sxs-lookup"><span data-stu-id="846c2-116">Error codes</span></span>

<span data-ttu-id="846c2-117">После завершения метода **Remove** объект **Err** может содержать один из кодов ошибок из следующего списка.</span><span class="sxs-lookup"><span data-stu-id="846c2-117">After completion of the **Remove** method, the **Err** object may contain one of the error codes in the following list.</span></span>

<dl> <dt>

<span data-ttu-id="846c2-118">**вбемеррфаилед** -2147749889 (0x80041001)</span><span class="sxs-lookup"><span data-stu-id="846c2-118">**wbemErrFailed** - 2147749889 (0x80041001)</span></span>
</dt> <dd>

<span data-ttu-id="846c2-119">Неопределенный сбой.</span><span class="sxs-lookup"><span data-stu-id="846c2-119">Unspecified failure.</span></span>

</dd> <dt>

<span data-ttu-id="846c2-120">**вбемерринвалидоператион** -2147749910 (0x80041016)</span><span class="sxs-lookup"><span data-stu-id="846c2-120">**wbemErrInvalidOperation** - 2147749910 (0x80041016)</span></span>
</dt> <dd>

<span data-ttu-id="846c2-121">Пользователь попытался удалить свойство, которое не может быть удалено.</span><span class="sxs-lookup"><span data-stu-id="846c2-121">User attempted to delete a property that cannot be deleted.</span></span>

</dd> <dt>

<span data-ttu-id="846c2-122">**вбемерринвалидпараметер** -2147749896 (0x80041008)</span><span class="sxs-lookup"><span data-stu-id="846c2-122">**wbemErrInvalidParameter** - 2147749896 (0x80041008)</span></span>
</dt> <dd>

<span data-ttu-id="846c2-123">Указан недопустимый параметр.</span><span class="sxs-lookup"><span data-stu-id="846c2-123">Invalid parameter was specified.</span></span>

</dd> <dt>

<span data-ttu-id="846c2-124">**вбемеррнотфаунд** -2147749890 (0x80041002)</span><span class="sxs-lookup"><span data-stu-id="846c2-124">**wbemErrNotFound** - 2147749890 (0x80041002)</span></span>
</dt> <dd>

<span data-ttu-id="846c2-125">Указанное свойство не существует.</span><span class="sxs-lookup"><span data-stu-id="846c2-125">Specified property does not exist.</span></span>

</dd> <dt>

<span data-ttu-id="846c2-126">**вбемерраутофмемори** -2147749894 (0x80041006)</span><span class="sxs-lookup"><span data-stu-id="846c2-126">**wbemErrOutOfMemory** - 2147749894 (0x80041006)</span></span>
</dt> <dd>

<span data-ttu-id="846c2-127">Недостаточно памяти для выполнения этого метода.</span><span class="sxs-lookup"><span data-stu-id="846c2-127">Not enough memory for this method to execute.</span></span>

</dd> <dt>

<span data-ttu-id="846c2-128">**вбемеррпропагатедпроперти** -142927303552 (0x2147219380)</span><span class="sxs-lookup"><span data-stu-id="846c2-128">**wbemErrPropagatedProperty** - 142927303552 (0x2147219380)</span></span>
</dt> <dd>

<span data-ttu-id="846c2-129">Пользователь попытался удалить свойство, владельцем которого он не является.</span><span class="sxs-lookup"><span data-stu-id="846c2-129">User attempted to delete a property that was not owned.</span></span> <span data-ttu-id="846c2-130">Свойство было унаследовано от класса-родителя.</span><span class="sxs-lookup"><span data-stu-id="846c2-130">The property was inherited from a parent class.</span></span>

</dd> <dt>

<span data-ttu-id="846c2-131">**вбемеррресеттодефаулт** -2147758082 (0x80043002)</span><span class="sxs-lookup"><span data-stu-id="846c2-131">**wbemErrResetToDefault** - 2147758082 (0x80043002)</span></span>
</dt> <dd>

<span data-ttu-id="846c2-132">Пользователь удалил значение переопределения по умолчанию для текущего класса.</span><span class="sxs-lookup"><span data-stu-id="846c2-132">User deleted an override default value for the current class.</span></span> <span data-ttu-id="846c2-133">Значение по умолчанию для этого свойства в родительском классе было повторно активировано.</span><span class="sxs-lookup"><span data-stu-id="846c2-133">The default value for this property in the parent class has been reactivated.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="846c2-134">Комментарии</span><span class="sxs-lookup"><span data-stu-id="846c2-134">Remarks</span></span>

<span data-ttu-id="846c2-135">Невозможно удалить свойства из экземпляров класса или производных классов с унаследованными свойствами.</span><span class="sxs-lookup"><span data-stu-id="846c2-135">Properties cannot be removed from class instances or derived classes with inherited properties.</span></span> <span data-ttu-id="846c2-136">Такие попытки удаления вызывают ошибку, и свойство не удаляется. свойство сбрасывается до значения по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="846c2-136">Such deletion attempts raise an error and the property is not removed; the property is reset to its default value.</span></span>

<span data-ttu-id="846c2-137">Невозможно выполнить итерацию коллекции при удалении элементов, так как при удалении элемента из коллекции указатель коллекции перемещается к следующему элементу.</span><span class="sxs-lookup"><span data-stu-id="846c2-137">You cannot iterate a collection while removing items because when you remove an element from a collection, the collection pointer is moved to the next element.</span></span> <span data-ttu-id="846c2-138">Дополнительные сведения см. [в разделе доступ к коллекции](accessing-a-collection.md).</span><span class="sxs-lookup"><span data-stu-id="846c2-138">For more information, see [Accessing a Collection](accessing-a-collection.md).</span></span>

## <a name="examples"></a><span data-ttu-id="846c2-139">Примеры</span><span class="sxs-lookup"><span data-stu-id="846c2-139">Examples</span></span>

<span data-ttu-id="846c2-140">Пример кода, в котором используется этот метод, см. в разделе [**SWbemPropertySet**](swbempropertyset.md) .</span><span class="sxs-lookup"><span data-stu-id="846c2-140">For a code example that uses this method, see the [**SWbemPropertySet**](swbempropertyset.md) topic.</span></span>

## <a name="requirements"></a><span data-ttu-id="846c2-141">Требования</span><span class="sxs-lookup"><span data-stu-id="846c2-141">Requirements</span></span>



| <span data-ttu-id="846c2-142">Требование</span><span class="sxs-lookup"><span data-stu-id="846c2-142">Requirement</span></span> | <span data-ttu-id="846c2-143">Значение</span><span class="sxs-lookup"><span data-stu-id="846c2-143">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="846c2-144">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="846c2-144">Minimum supported client</span></span><br/> | <span data-ttu-id="846c2-145">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="846c2-145">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="846c2-146">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="846c2-146">Minimum supported server</span></span><br/> | <span data-ttu-id="846c2-147">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="846c2-147">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="846c2-148">Header</span><span class="sxs-lookup"><span data-stu-id="846c2-148">Header</span></span><br/>                   | <dl> <span data-ttu-id="846c2-149"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="846c2-149"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="846c2-150">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="846c2-150">Type library</span></span><br/>             | <dl> <span data-ttu-id="846c2-151"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="846c2-151"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="846c2-152">DLL</span><span class="sxs-lookup"><span data-stu-id="846c2-152">DLL</span></span><br/>                      | <dl> <span data-ttu-id="846c2-153"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="846c2-153"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="846c2-154">CLSID</span><span class="sxs-lookup"><span data-stu-id="846c2-154">CLSID</span></span><br/>                    | <span data-ttu-id="846c2-155">\_SWBEMPROPERTYSET CLSID</span><span class="sxs-lookup"><span data-stu-id="846c2-155">CLSID\_SWbemPropertySet</span></span><br/>                                                      |
| <span data-ttu-id="846c2-156">IID</span><span class="sxs-lookup"><span data-stu-id="846c2-156">IID</span></span><br/>                      | <span data-ttu-id="846c2-157">IID \_ исвбемпропертисет</span><span class="sxs-lookup"><span data-stu-id="846c2-157">IID\_ISWbemPropertySet</span></span><br/>                                                       |



## <a name="see-also"></a><span data-ttu-id="846c2-158">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="846c2-158">See also</span></span>

<dl> <dt>

[<span data-ttu-id="846c2-159">**SWbemPropertySet**</span><span class="sxs-lookup"><span data-stu-id="846c2-159">**SWbemPropertySet**</span></span>](swbempropertyset.md)
</dt> <dt>

[<span data-ttu-id="846c2-160">**SWbemPropertySet. Add**</span><span class="sxs-lookup"><span data-stu-id="846c2-160">**SWbemPropertySet.Add**</span></span>](swbempropertyset-add.md)
</dt> </dl>

 

 




