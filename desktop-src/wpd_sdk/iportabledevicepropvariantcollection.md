---
description: Интерфейс Ипортабледевицепропвариантколлектион содержит коллекцию индексированных значений ПРОПВАРИАНТ для одного и того же объекта VARTYPE.
ms.assetid: 41224958-a5a0-4e09-8733-d0ae036f68b9
title: Интерфейс Ипортабледевицепропвариантколлектион (Портабледевицетипес. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDevicePropVariantCollection
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: 14ba07894c74567487704bb1f63e7242542af313
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105717873"
---
# <a name="iportabledevicepropvariantcollection-interface"></a><span data-ttu-id="db8a9-103">Интерфейс Ипортабледевицепропвариантколлектион</span><span class="sxs-lookup"><span data-stu-id="db8a9-103">IPortableDevicePropVariantCollection interface</span></span>

<span data-ttu-id="db8a9-104">Интерфейс **ипортабледевицепропвариантколлектион** содержит коллекцию индексированных значений **пропвариант** для одного и того же объекта VarType.</span><span class="sxs-lookup"><span data-stu-id="db8a9-104">The **IPortableDevicePropVariantCollection** interface holds a collection of indexed **PROPVARIANT** values of the same VARTYPE.</span></span> <span data-ttu-id="db8a9-105">VARTYPE первого элемента, добавляемого в коллекцию, определяет VARTYPE коллекции.</span><span class="sxs-lookup"><span data-stu-id="db8a9-105">The VARTYPE of the first item that is added to the collection determines the VARTYPE of the collection.</span></span> <span data-ttu-id="db8a9-106">Попытка добавить элемент другого объекта VARTYPE может завершиться ошибкой, если значение **пропвариант** не может быть изменено на текущую VarType коллекции.</span><span class="sxs-lookup"><span data-stu-id="db8a9-106">An attempt to add an item of a different VARTYPE may fail if the **PROPVARIANT** value cannot be changed to the collection's current VARTYPE.</span></span> <span data-ttu-id="db8a9-107">Чтобы изменить VARTYPE коллекции, вызовите метод **ChangeType**.</span><span class="sxs-lookup"><span data-stu-id="db8a9-107">To change the VARTYPE of the collection, call **ChangeType**.</span></span>

<span data-ttu-id="db8a9-108">Этот интерфейс можно получить из метода или, если требуется новый объект, вызовите **CREATE** с помощью **CLSID \_ портабледевицепропвариантколлектион**.</span><span class="sxs-lookup"><span data-stu-id="db8a9-108">This interface can be retrieved from a method or, if a new object is required, call **CoCreate** with **CLSID\_PortableDevicePropVariantCollection**.</span></span>

## <a name="members"></a><span data-ttu-id="db8a9-109">Элементы</span><span class="sxs-lookup"><span data-stu-id="db8a9-109">Members</span></span>

<span data-ttu-id="db8a9-110">Интерфейс **ипортабледевицепропвариантколлектион** наследует от интерфейса [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="db8a9-110">The **IPortableDevicePropVariantCollection** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="db8a9-111">**Ипортабледевицепропвариантколлектион** также имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="db8a9-111">**IPortableDevicePropVariantCollection** also has these types of members:</span></span>

-   [<span data-ttu-id="db8a9-112">Методы</span><span class="sxs-lookup"><span data-stu-id="db8a9-112">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="db8a9-113">Методы</span><span class="sxs-lookup"><span data-stu-id="db8a9-113">Methods</span></span>

<span data-ttu-id="db8a9-114">Интерфейс **ипортабледевицепропвариантколлектион** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="db8a9-114">The **IPortableDevicePropVariantCollection** interface has these methods.</span></span>



| <span data-ttu-id="db8a9-115">Метод</span><span class="sxs-lookup"><span data-stu-id="db8a9-115">Method</span></span>                                                                | <span data-ttu-id="db8a9-116">Описание</span><span class="sxs-lookup"><span data-stu-id="db8a9-116">Description</span></span>                                                                         |
|:----------------------------------------------------------------------|:------------------------------------------------------------------------------------|
| [<span data-ttu-id="db8a9-117">**Включить**</span><span class="sxs-lookup"><span data-stu-id="db8a9-117">**Add**</span></span>](iportabledevicepropvariantcollection-add.md)               | <span data-ttu-id="db8a9-118">Добавляет элемент в коллекцию.</span><span class="sxs-lookup"><span data-stu-id="db8a9-118">Adds an item to the collection.</span></span><br/>                                          |
| [<span data-ttu-id="db8a9-119">**ChangeType**</span><span class="sxs-lookup"><span data-stu-id="db8a9-119">**ChangeType**</span></span>](iportabledevicepropvariantcollection-changetype.md) | <span data-ttu-id="db8a9-120">Преобразует все элементы в коллекции в указанный объект VARTYPE.</span><span class="sxs-lookup"><span data-stu-id="db8a9-120">Converts all items in the collection to the specified VARTYPE.</span></span><br/>           |
| [<span data-ttu-id="db8a9-121">**Открытым**</span><span class="sxs-lookup"><span data-stu-id="db8a9-121">**Clear**</span></span>](iportabledevicepropvariantcollection-clear.md)           | <span data-ttu-id="db8a9-122">Освобождает, а затем удаляет все элементы из коллекции.</span><span class="sxs-lookup"><span data-stu-id="db8a9-122">Frees, and then removes, all items from the collection.</span></span><br/>                  |
| [<span data-ttu-id="db8a9-123">**GetAt**</span><span class="sxs-lookup"><span data-stu-id="db8a9-123">**GetAt**</span></span>](iportabledevicepropvariantcollection-getat.md)           | <span data-ttu-id="db8a9-124">Извлекает элемент из коллекции по индексу, начинающимся с нуля.</span><span class="sxs-lookup"><span data-stu-id="db8a9-124">Retrieves an item from the collection by a zero-based index.</span></span><br/>             |
| [<span data-ttu-id="db8a9-125">**GetCount**</span><span class="sxs-lookup"><span data-stu-id="db8a9-125">**GetCount**</span></span>](iportabledevicepropvariantcollection-getcount.md)     | <span data-ttu-id="db8a9-126">Возвращает число элементов в этой коллекции.</span><span class="sxs-lookup"><span data-stu-id="db8a9-126">Retrieves the number of items in this collection.</span></span><br/>                        |
| [<span data-ttu-id="db8a9-127">**GetType**</span><span class="sxs-lookup"><span data-stu-id="db8a9-127">**GetType**</span></span>](iportabledevicepropvariantcollection-gettype.md)       | <span data-ttu-id="db8a9-128">Возвращает тип данных элементов коллекции.</span><span class="sxs-lookup"><span data-stu-id="db8a9-128">Retrieves the data type of the items in the collection.</span></span><br/>                  |
| [<span data-ttu-id="db8a9-129">**RemoveAt**</span><span class="sxs-lookup"><span data-stu-id="db8a9-129">**RemoveAt**</span></span>](iportabledevicepropvariantcollection-removeat.md)     | <span data-ttu-id="db8a9-130">Удаляет элемент, хранящийся в расположении, указанном заданным индексом.</span><span class="sxs-lookup"><span data-stu-id="db8a9-130">Removes the element stored at the location specified by the given index.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="db8a9-131">Требования</span><span class="sxs-lookup"><span data-stu-id="db8a9-131">Requirements</span></span>



| <span data-ttu-id="db8a9-132">Требование</span><span class="sxs-lookup"><span data-stu-id="db8a9-132">Requirement</span></span> | <span data-ttu-id="db8a9-133">Значение</span><span class="sxs-lookup"><span data-stu-id="db8a9-133">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="db8a9-134">Header</span><span class="sxs-lookup"><span data-stu-id="db8a9-134">Header</span></span><br/>  | <dl> <span data-ttu-id="db8a9-135"><dt>Портабледевицетипес. h</dt></span><span class="sxs-lookup"><span data-stu-id="db8a9-135"><dt>PortableDeviceTypes.h</dt></span></span> </dl>   |
| <span data-ttu-id="db8a9-136">Библиотека</span><span class="sxs-lookup"><span data-stu-id="db8a9-136">Library</span></span><br/> | <dl> <span data-ttu-id="db8a9-137"><dt>Портабледевицегуидс. lib</dt></span><span class="sxs-lookup"><span data-stu-id="db8a9-137"><dt>PortableDeviceGUIDs.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="db8a9-138">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="db8a9-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="db8a9-139">**Интерфейсы коллекции**</span><span class="sxs-lookup"><span data-stu-id="db8a9-139">**Collection Interfaces**</span></span>](collection-interfaces.md)
</dt> </dl>

 

