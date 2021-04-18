---
description: Объект SWbemPropertySet — это коллекция объектов SWbemProperty.
ms.assetid: 0edad17b-facc-4885-9ce4-561ca6f57a66
ms.tgt_platform: multiple
title: Объект SWbemPropertySet (Wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemPropertySet
- ISWbemPropertySet
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 05ae5d5e0bfbc5ab0733e00e4649baa2849d3446
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105712929"
---
# <a name="swbempropertyset-object"></a><span data-ttu-id="d2e97-103">Объект SWbemPropertySet</span><span class="sxs-lookup"><span data-stu-id="d2e97-103">SWbemPropertySet object</span></span>

<span data-ttu-id="d2e97-104">Объект **SWbemPropertySet** — это коллекция объектов [**SWbemProperty**](swbemproperty.md) .</span><span class="sxs-lookup"><span data-stu-id="d2e97-104">An **SWbemPropertySet** object is a collection of [**SWbemProperty**](swbemproperty.md) objects.</span></span> <span data-ttu-id="d2e97-105">Вы можете добавлять элементы в коллекцию с помощью метода [**Add**](swbempropertyset-add.md) , получать элементы из коллекции с помощью метода [**Item**](swbempropertyset-item.md) и удалять элементы из коллекции с помощью метода [**Remove**](swbempropertyset-remove.md) .</span><span class="sxs-lookup"><span data-stu-id="d2e97-105">You can add items to the collection using the [**Add**](swbempropertyset-add.md) method, retrieve items from the collection using the [**Item**](swbempropertyset-item.md) method, and remove items from the collection using the [**Remove**](swbempropertyset-remove.md) method.</span></span> <span data-ttu-id="d2e97-106">Дополнительные сведения см. [в разделе доступ к коллекции](accessing-a-collection.md).</span><span class="sxs-lookup"><span data-stu-id="d2e97-106">For more information, see [Accessing a Collection](accessing-a-collection.md).</span></span> <span data-ttu-id="d2e97-107">Не удается создать этот объект с [помощью вызова функции](creating-an-object-using-vbscript.md) VBScript.</span><span class="sxs-lookup"><span data-stu-id="d2e97-107">This object cannot be created by the VBScript [CreateObject](creating-an-object-using-vbscript.md) call.</span></span>

<span data-ttu-id="d2e97-108">Объекты [**SWbemProperty**](swbemproperty.md) , составляющие коллекцию **SWbemPropertySet** , используются для описания свойств одного класса или экземпляра WMI.</span><span class="sxs-lookup"><span data-stu-id="d2e97-108">The [**SWbemProperty**](swbemproperty.md) objects that make up an **SWbemPropertySet** collection are used to describe the properties of a single WMI class or instance.</span></span>

## <a name="members"></a><span data-ttu-id="d2e97-109">Элементы</span><span class="sxs-lookup"><span data-stu-id="d2e97-109">Members</span></span>

<span data-ttu-id="d2e97-110">Объект **SWbemPropertySet** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="d2e97-110">The **SWbemPropertySet** object has these types of members:</span></span>

-   [<span data-ttu-id="d2e97-111">Методы</span><span class="sxs-lookup"><span data-stu-id="d2e97-111">Methods</span></span>](#methods)
-   [<span data-ttu-id="d2e97-112">Свойства</span><span class="sxs-lookup"><span data-stu-id="d2e97-112">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="d2e97-113">Методы</span><span class="sxs-lookup"><span data-stu-id="d2e97-113">Methods</span></span>

<span data-ttu-id="d2e97-114">Объект **SWbemPropertySet** содержит эти методы.</span><span class="sxs-lookup"><span data-stu-id="d2e97-114">The **SWbemPropertySet** object has these methods.</span></span>



| <span data-ttu-id="d2e97-115">Метод</span><span class="sxs-lookup"><span data-stu-id="d2e97-115">Method</span></span>                                    | <span data-ttu-id="d2e97-116">Описание</span><span class="sxs-lookup"><span data-stu-id="d2e97-116">Description</span></span>                                                                                                                     |
|:------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="d2e97-117">**Включить**</span><span class="sxs-lookup"><span data-stu-id="d2e97-117">**Add**</span></span>](swbempropertyset-add.md)       | <span data-ttu-id="d2e97-118">Добавляет объект [**SWbemProperty**](swbemproperty.md) в коллекцию **SWbemPropertySet** .</span><span class="sxs-lookup"><span data-stu-id="d2e97-118">Adds an [**SWbemProperty**](swbemproperty.md) object to the **SWbemPropertySet** collection.</span></span><br/>                        |
| [<span data-ttu-id="d2e97-119">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="d2e97-119">**Item**</span></span>](swbempropertyset-item.md)     | <span data-ttu-id="d2e97-120">Возвращает именованный [**SWbemProperty**](swbemproperty.md) из коллекции.</span><span class="sxs-lookup"><span data-stu-id="d2e97-120">Gets a named [**SWbemProperty**](swbemproperty.md) from the collection.</span></span> <span data-ttu-id="d2e97-121">Это метод по умолчанию для этого объекта.</span><span class="sxs-lookup"><span data-stu-id="d2e97-121">This is the default method for this object.</span></span><br/> |
| [<span data-ttu-id="d2e97-122">**Отменит**</span><span class="sxs-lookup"><span data-stu-id="d2e97-122">**Remove**</span></span>](swbempropertyset-remove.md) | <span data-ttu-id="d2e97-123">Удаляет объект [**SWbemProperty**](swbemproperty.md) из коллекции.</span><span class="sxs-lookup"><span data-stu-id="d2e97-123">Deletes an [**SWbemProperty**](swbemproperty.md) object from the collection.</span></span><br/>                                        |



 

### <a name="properties"></a><span data-ttu-id="d2e97-124">Свойства</span><span class="sxs-lookup"><span data-stu-id="d2e97-124">Properties</span></span>

<span data-ttu-id="d2e97-125">Объект **SWbemPropertySet** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="d2e97-125">The **SWbemPropertySet** object has these properties.</span></span>



| <span data-ttu-id="d2e97-126">Свойство</span><span class="sxs-lookup"><span data-stu-id="d2e97-126">Property</span></span>                                           | <span data-ttu-id="d2e97-127">Тип доступа</span><span class="sxs-lookup"><span data-stu-id="d2e97-127">Access type</span></span>          | <span data-ttu-id="d2e97-128">Описание</span><span class="sxs-lookup"><span data-stu-id="d2e97-128">Description</span></span>                                                            |
|:---------------------------------------------------|:---------------------|:-----------------------------------------------------------------------|
| [<span data-ttu-id="d2e97-129">**Расчета**</span><span class="sxs-lookup"><span data-stu-id="d2e97-129">**Count**</span></span>](swbempropertyset-count.md)<br/> | <span data-ttu-id="d2e97-130">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="d2e97-130">Read-only</span></span><br/> | <span data-ttu-id="d2e97-131">Число элементов в коллекции **SWbemPropertySet** .</span><span class="sxs-lookup"><span data-stu-id="d2e97-131">The number of items in the **SWbemPropertySet** collection.</span></span><br/> |



 

## <a name="examples"></a><span data-ttu-id="d2e97-132">Примеры</span><span class="sxs-lookup"><span data-stu-id="d2e97-132">Examples</span></span>

<span data-ttu-id="d2e97-133">В следующем примере VBScript показано, как [**SWbemPropertySet. Remove**](swbempropertyset-remove.md) может возвращать **вбемеррресеттодефаулт** , если свойство переопределено.</span><span class="sxs-lookup"><span data-stu-id="d2e97-133">The following VBScript sample demonstrates how [**SWbemPropertySet.Remove**](swbempropertyset-remove.md) can return **wbemErrResetToDefault** if the property is overridden.</span></span>


```VB
on error resume next 

'Create a keyed class with a defaulted property
set service = GetObject("Winmgmts:")
set emptyclass = service.Get
emptyclass.path_.class = "REMOVETEST00"
set prop = emptyclass.properties_.add ("p", 19)

prop.qualifiers_.add "key", true
emptyclass.properties_.add ("q", 19).Value = 12

emptyclass.put_

'create an instance and override the property
set instance = service.get ("RemoveTest00").spawninstance_

instance.properties_("q").Value = 24
instance.properties_("p").Value = 1
instance.put_

'retrieve the instance and remove the property
set instance = service.get ("removetest00=1")
set property = instance.properties_ ("q")

WScript.echo "Overridden value of property is [24]:", property.value
WScript.echo ""

instance.properties_.remove "q"
set property = instance.properties_ ("q")
WScript.echo "Value of property after removal is [12]:", property.value
WScript.echo ""

if err <> 0 then
 WScript.Echo "0x" & Hex(Err.Number), Err.Description, Err.Source
end if
```



## <a name="requirements"></a><span data-ttu-id="d2e97-134">Требования</span><span class="sxs-lookup"><span data-stu-id="d2e97-134">Requirements</span></span>



| <span data-ttu-id="d2e97-135">Требование</span><span class="sxs-lookup"><span data-stu-id="d2e97-135">Requirement</span></span> | <span data-ttu-id="d2e97-136">Значение</span><span class="sxs-lookup"><span data-stu-id="d2e97-136">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="d2e97-137">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="d2e97-137">Minimum supported client</span></span><br/> | <span data-ttu-id="d2e97-138">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="d2e97-138">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="d2e97-139">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="d2e97-139">Minimum supported server</span></span><br/> | <span data-ttu-id="d2e97-140">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="d2e97-140">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="d2e97-141">Header</span><span class="sxs-lookup"><span data-stu-id="d2e97-141">Header</span></span><br/>                   | <dl> <span data-ttu-id="d2e97-142"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="d2e97-142"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="d2e97-143">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="d2e97-143">Type library</span></span><br/>             | <dl> <span data-ttu-id="d2e97-144"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="d2e97-144"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="d2e97-145">DLL</span><span class="sxs-lookup"><span data-stu-id="d2e97-145">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d2e97-146"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d2e97-146"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="d2e97-147">CLSID</span><span class="sxs-lookup"><span data-stu-id="d2e97-147">CLSID</span></span><br/>                    | <span data-ttu-id="d2e97-148">\_SWBEMPROPERTYSET CLSID</span><span class="sxs-lookup"><span data-stu-id="d2e97-148">CLSID\_SWbemPropertySet</span></span><br/>                                                      |
| <span data-ttu-id="d2e97-149">IID</span><span class="sxs-lookup"><span data-stu-id="d2e97-149">IID</span></span><br/>                      | <span data-ttu-id="d2e97-150">IID \_ исвбемпропертисет</span><span class="sxs-lookup"><span data-stu-id="d2e97-150">IID\_ISWbemPropertySet</span></span><br/>                                                       |



## <a name="see-also"></a><span data-ttu-id="d2e97-151">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="d2e97-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d2e97-152">Создание скриптов для объектов API</span><span class="sxs-lookup"><span data-stu-id="d2e97-152">Scripting API Objects</span></span>](scripting-api-objects.md)
</dt> </dl>

 

 




