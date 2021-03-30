---
description: Объект Свбеммесодсет — это коллекция объектов Свбеммесод. Элементы извлекаются с помощью метода Item. Дополнительные сведения см. в разделе доступ к коллекции. Не удается создать этот объект с помощью вызова функции VBScript.
ms.assetid: 0ca2601f-ed40-472e-b4f2-eee750c8c8d1
ms.tgt_platform: multiple
title: Объект Свбеммесодсет (Wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemMethodSet
- ISWbemMethodSet
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: d47c4dc8335077d6f8568be4b56200558942ac39
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103910280"
---
# <a name="swbemmethodset-object"></a><span data-ttu-id="89266-106">Объект Свбеммесодсет</span><span class="sxs-lookup"><span data-stu-id="89266-106">SWbemMethodSet object</span></span>

<span data-ttu-id="89266-107">Объект **свбеммесодсет** — это коллекция объектов [**свбеммесод**](swbemmethod.md) .</span><span class="sxs-lookup"><span data-stu-id="89266-107">An **SWbemMethodSet** object is a collection of [**SWbemMethod**](swbemmethod.md) objects.</span></span> <span data-ttu-id="89266-108">Элементы извлекаются с помощью метода [**Item**](swbemmethodset-item.md) .</span><span class="sxs-lookup"><span data-stu-id="89266-108">Items are retrieved using the [**Item**](swbemmethodset-item.md) method.</span></span> <span data-ttu-id="89266-109">Дополнительные сведения см. [в разделе доступ к коллекции](accessing-a-collection.md).</span><span class="sxs-lookup"><span data-stu-id="89266-109">For more information, see [Accessing a Collection](accessing-a-collection.md).</span></span> <span data-ttu-id="89266-110">Не удается создать этот объект с **помощью вызова функции** VBScript.</span><span class="sxs-lookup"><span data-stu-id="89266-110">This object cannot be created by the VBScript **CreateObject** call.</span></span>

> [!Note]  
> <span data-ttu-id="89266-111">В этой версии API доступ на запись к сведениям о методе не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="89266-111">In this version of the API, write access to method information is not supported.</span></span> <span data-ttu-id="89266-112">Если необходимо определить методы или изменить существующие определения методов, можно определить изменения метода в MOF-файле и отправить изменения с помощью компилятора MOF.</span><span class="sxs-lookup"><span data-stu-id="89266-112">If you want to define methods or modify existing method definitions, you can define the method changes in a MOF file and submit the changes using the MOF Compiler.</span></span> <span data-ttu-id="89266-113">Кроме того, можно использовать API WMI COM.</span><span class="sxs-lookup"><span data-stu-id="89266-113">Alternatively, use the WMI COM API.</span></span>

 

## <a name="members"></a><span data-ttu-id="89266-114">Элементы</span><span class="sxs-lookup"><span data-stu-id="89266-114">Members</span></span>

<span data-ttu-id="89266-115">Объект **свбеммесодсет** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="89266-115">The **SWbemMethodSet** object has these types of members:</span></span>

-   [<span data-ttu-id="89266-116">Методы</span><span class="sxs-lookup"><span data-stu-id="89266-116">Methods</span></span>](#swbemmethodset-object)
-   [<span data-ttu-id="89266-117">Свойства</span><span class="sxs-lookup"><span data-stu-id="89266-117">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="89266-118">Методы</span><span class="sxs-lookup"><span data-stu-id="89266-118">Methods</span></span>

<span data-ttu-id="89266-119">Объект **свбеммесодсет** содержит эти методы.</span><span class="sxs-lookup"><span data-stu-id="89266-119">The **SWbemMethodSet** object has these methods.</span></span>



| <span data-ttu-id="89266-120">Метод</span><span class="sxs-lookup"><span data-stu-id="89266-120">Method</span></span>                              | <span data-ttu-id="89266-121">Описание</span><span class="sxs-lookup"><span data-stu-id="89266-121">Description</span></span>                                                                                                                                  |
|:------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="89266-122">**Item**</span><span class="sxs-lookup"><span data-stu-id="89266-122">**Item**</span></span>](swbemmethodset-item.md) | <span data-ttu-id="89266-123">Извлекает объект [**свбеммесод**](swbemmethod.md) из коллекции.</span><span class="sxs-lookup"><span data-stu-id="89266-123">Retrieves an [**SWbemMethod**](swbemmethod.md) object from the collection.</span></span> <span data-ttu-id="89266-124">Это метод автоматизации по умолчанию для этого объекта.</span><span class="sxs-lookup"><span data-stu-id="89266-124">This is the default automation method of this object.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="89266-125">Свойства</span><span class="sxs-lookup"><span data-stu-id="89266-125">Properties</span></span>

<span data-ttu-id="89266-126">Объект **свбеммесодсет** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="89266-126">The **SWbemMethodSet** object has these properties.</span></span>



| <span data-ttu-id="89266-127">Свойство</span><span class="sxs-lookup"><span data-stu-id="89266-127">Property</span></span>                                         | <span data-ttu-id="89266-128">Тип доступа</span><span class="sxs-lookup"><span data-stu-id="89266-128">Access type</span></span>          | <span data-ttu-id="89266-129">Описание</span><span class="sxs-lookup"><span data-stu-id="89266-129">Description</span></span>                                       |
|:-------------------------------------------------|:---------------------|:--------------------------------------------------|
| [<span data-ttu-id="89266-130">**Расчета**</span><span class="sxs-lookup"><span data-stu-id="89266-130">**Count**</span></span>](swbemmethodset-count.md)<br/> | <span data-ttu-id="89266-131">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="89266-131">Read-only</span></span><br/> | <span data-ttu-id="89266-132">Количество элементов в коллекции.</span><span class="sxs-lookup"><span data-stu-id="89266-132">The number of items in the collection.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="89266-133">Требования</span><span class="sxs-lookup"><span data-stu-id="89266-133">Requirements</span></span>



| <span data-ttu-id="89266-134">Требование</span><span class="sxs-lookup"><span data-stu-id="89266-134">Requirement</span></span> | <span data-ttu-id="89266-135">Значение</span><span class="sxs-lookup"><span data-stu-id="89266-135">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="89266-136">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="89266-136">Minimum supported client</span></span><br/> | <span data-ttu-id="89266-137">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="89266-137">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="89266-138">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="89266-138">Minimum supported server</span></span><br/> | <span data-ttu-id="89266-139">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="89266-139">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="89266-140">Header</span><span class="sxs-lookup"><span data-stu-id="89266-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="89266-141"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="89266-141"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="89266-142">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="89266-142">Type library</span></span><br/>             | <dl> <span data-ttu-id="89266-143"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="89266-143"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="89266-144">DLL</span><span class="sxs-lookup"><span data-stu-id="89266-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="89266-145"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="89266-145"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="89266-146">CLSID</span><span class="sxs-lookup"><span data-stu-id="89266-146">CLSID</span></span><br/>                    | <span data-ttu-id="89266-147">\_СВБЕММЕСОДСЕТ CLSID</span><span class="sxs-lookup"><span data-stu-id="89266-147">CLSID\_SWbemMethodSet</span></span><br/>                                                        |
| <span data-ttu-id="89266-148">IID</span><span class="sxs-lookup"><span data-stu-id="89266-148">IID</span></span><br/>                      | <span data-ttu-id="89266-149">IID \_ исвбеммесодсет</span><span class="sxs-lookup"><span data-stu-id="89266-149">IID\_ISWbemMethodSet</span></span><br/>                                                         |



## <a name="see-also"></a><span data-ttu-id="89266-150">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="89266-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="89266-151">Создание скриптов для объектов API</span><span class="sxs-lookup"><span data-stu-id="89266-151">Scripting API Objects</span></span>](scripting-api-objects.md)
</dt> </dl>

 

 




