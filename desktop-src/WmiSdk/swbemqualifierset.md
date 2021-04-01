---
description: Объект Свбемкуалифиерсет — это коллекция объектов Свбемкуалифиер.
ms.assetid: 7ac5469c-357b-499d-a558-30bf760c5311
ms.tgt_platform: multiple
title: Объект Свбемкуалифиерсет (Wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemQualifierSet
- ISWbemQualifierSet
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: e74b495313e8061cc6e08e255d1d055bb2f72a92
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104081518"
---
# <a name="swbemqualifierset-object"></a><span data-ttu-id="81706-103">Объект Свбемкуалифиерсет</span><span class="sxs-lookup"><span data-stu-id="81706-103">SWbemQualifierSet object</span></span>

<span data-ttu-id="81706-104">Объект **свбемкуалифиерсет** — это коллекция объектов [**свбемкуалифиер**](swbemqualifier.md) .</span><span class="sxs-lookup"><span data-stu-id="81706-104">An **SWbemQualifierSet** object is a collection of [**SWbemQualifier**](swbemqualifier.md) objects.</span></span> <span data-ttu-id="81706-105">Элементы добавляются в коллекцию с помощью метода [**Add**](swbemqualifierset-add.md) , полученного из коллекции с помощью метода [**Item**](swbemqualifierset-item.md) , и удаляются из коллекции с помощью метода [**Remove**](swbemqualifierset-remove.md) .</span><span class="sxs-lookup"><span data-stu-id="81706-105">Items are added to the collection using the [**Add**](swbemqualifierset-add.md) method, retrieved from the collection using the [**Item**](swbemqualifierset-item.md) method, and removed from the collection using the [**Remove**](swbemqualifierset-remove.md) method.</span></span> <span data-ttu-id="81706-106">Не удается создать этот объект с [помощью вызова функции](creating-an-object-using-vbscript.md) VBScript.</span><span class="sxs-lookup"><span data-stu-id="81706-106">This object cannot be created by the VBScript [CreateObject](creating-an-object-using-vbscript.md) call.</span></span>

<span data-ttu-id="81706-107">Дополнительные сведения см. [в разделе доступ к коллекции](accessing-a-collection.md).</span><span class="sxs-lookup"><span data-stu-id="81706-107">For more information, see [Accessing a Collection](accessing-a-collection.md).</span></span>

<span data-ttu-id="81706-108">Объекты [**свбемкуалифиер**](swbemqualifier.md) , составляющие коллекцию **свбемкуалифиерсет** , описывают квалификаторы, присоединенные к классу WMI, экземпляру, методу или параметру метода.</span><span class="sxs-lookup"><span data-stu-id="81706-108">The [**SWbemQualifier**](swbemqualifier.md) objects that make up an **SWbemQualifierSet** collection describe the qualifiers attached to a WMI class, instance, method, or method parameter.</span></span>

## <a name="members"></a><span data-ttu-id="81706-109">Элементы</span><span class="sxs-lookup"><span data-stu-id="81706-109">Members</span></span>

<span data-ttu-id="81706-110">Объект **свбемкуалифиерсет** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="81706-110">The **SWbemQualifierSet** object has these types of members:</span></span>

-   [<span data-ttu-id="81706-111">Методы</span><span class="sxs-lookup"><span data-stu-id="81706-111">Methods</span></span>](#methods)
-   [<span data-ttu-id="81706-112">Свойства</span><span class="sxs-lookup"><span data-stu-id="81706-112">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="81706-113">Методы</span><span class="sxs-lookup"><span data-stu-id="81706-113">Methods</span></span>

<span data-ttu-id="81706-114">Объект **свбемкуалифиерсет** содержит эти методы.</span><span class="sxs-lookup"><span data-stu-id="81706-114">The **SWbemQualifierSet** object has these methods.</span></span>



| <span data-ttu-id="81706-115">Метод</span><span class="sxs-lookup"><span data-stu-id="81706-115">Method</span></span>                                     | <span data-ttu-id="81706-116">Описание</span><span class="sxs-lookup"><span data-stu-id="81706-116">Description</span></span>                                                                                                 |
|:-------------------------------------------|:------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="81706-117">**Включить**</span><span class="sxs-lookup"><span data-stu-id="81706-117">**Add**</span></span>](swbemqualifierset-add.md)       | <span data-ttu-id="81706-118">Добавляет объект [**свбемкуалифиер**](swbemqualifier.md) в коллекцию **свбемкуалифиерсет** .</span><span class="sxs-lookup"><span data-stu-id="81706-118">Adds an [**SWbemQualifier**](swbemqualifier.md) object to the **SWbemQualifierSet** collection.</span></span><br/> |
| [<span data-ttu-id="81706-119">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="81706-119">**Item**</span></span>](swbemqualifierset-item.md)     | <span data-ttu-id="81706-120">Возвращает именованный объект [**свбемкуалифиер**](swbemqualifier.md) из коллекции.</span><span class="sxs-lookup"><span data-stu-id="81706-120">Returns a named [**SWbemQualifier**](swbemqualifier.md) object from the collection.</span></span><br/>             |
| [<span data-ttu-id="81706-121">**Отменит**</span><span class="sxs-lookup"><span data-stu-id="81706-121">**Remove**</span></span>](swbemqualifierset-remove.md) | <span data-ttu-id="81706-122">Удаляет именованный квалификатор из коллекции.</span><span class="sxs-lookup"><span data-stu-id="81706-122">Deletes a named qualifier from the collection.</span></span><br/>                                                   |



 

### <a name="properties"></a><span data-ttu-id="81706-123">Свойства</span><span class="sxs-lookup"><span data-stu-id="81706-123">Properties</span></span>

<span data-ttu-id="81706-124">Объект **свбемкуалифиерсет** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="81706-124">The **SWbemQualifierSet** object has these properties.</span></span>



| <span data-ttu-id="81706-125">Свойство</span><span class="sxs-lookup"><span data-stu-id="81706-125">Property</span></span>                                            | <span data-ttu-id="81706-126">Тип доступа</span><span class="sxs-lookup"><span data-stu-id="81706-126">Access type</span></span>          | <span data-ttu-id="81706-127">Описание</span><span class="sxs-lookup"><span data-stu-id="81706-127">Description</span></span>                                                                     |
|:----------------------------------------------------|:---------------------|:--------------------------------------------------------------------------------|
| [<span data-ttu-id="81706-128">**Расчета**</span><span class="sxs-lookup"><span data-stu-id="81706-128">**Count**</span></span>](swbemqualifierset-count.md)<br/> | <span data-ttu-id="81706-129">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="81706-129">Read-only</span></span><br/> | <span data-ttu-id="81706-130">Содержит количество элементов в коллекции **свбемкуалифиерсет** .</span><span class="sxs-lookup"><span data-stu-id="81706-130">Contains the number of items in an **SWbemQualifierSet** collection.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="81706-131">Требования</span><span class="sxs-lookup"><span data-stu-id="81706-131">Requirements</span></span>



| <span data-ttu-id="81706-132">Требование</span><span class="sxs-lookup"><span data-stu-id="81706-132">Requirement</span></span> | <span data-ttu-id="81706-133">Значение</span><span class="sxs-lookup"><span data-stu-id="81706-133">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="81706-134">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="81706-134">Minimum supported client</span></span><br/> | <span data-ttu-id="81706-135">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="81706-135">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="81706-136">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="81706-136">Minimum supported server</span></span><br/> | <span data-ttu-id="81706-137">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="81706-137">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="81706-138">Header</span><span class="sxs-lookup"><span data-stu-id="81706-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="81706-139"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="81706-139"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="81706-140">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="81706-140">Type library</span></span><br/>             | <dl> <span data-ttu-id="81706-141"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="81706-141"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="81706-142">DLL</span><span class="sxs-lookup"><span data-stu-id="81706-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="81706-143"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="81706-143"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="81706-144">CLSID</span><span class="sxs-lookup"><span data-stu-id="81706-144">CLSID</span></span><br/>                    | <span data-ttu-id="81706-145">\_СВБЕМКУАЛИФИЕРСЕТ CLSID</span><span class="sxs-lookup"><span data-stu-id="81706-145">CLSID\_SWbemQualifierSet</span></span><br/>                                                     |
| <span data-ttu-id="81706-146">IID</span><span class="sxs-lookup"><span data-stu-id="81706-146">IID</span></span><br/>                      | <span data-ttu-id="81706-147">IID \_ исвбемкуалифиерсет</span><span class="sxs-lookup"><span data-stu-id="81706-147">IID\_ISWbemQualifierSet</span></span><br/>                                                      |



## <a name="see-also"></a><span data-ttu-id="81706-148">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="81706-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="81706-149">Создание скриптов для объектов API</span><span class="sxs-lookup"><span data-stu-id="81706-149">Scripting API Objects</span></span>](scripting-api-objects.md)
</dt> </dl>

 

 




