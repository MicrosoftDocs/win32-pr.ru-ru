---
description: Интерфейс Ипортабледевицевалуесколлектион содержит коллекцию индексируемых от нуля интерфейсов Ипортабледевицевалуес.
ms.assetid: 8bce9d27-f240-41ec-acf4-fefccdd95e9f
title: Интерфейс Ипортабледевицевалуесколлектион (Портабледевицетипес. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDeviceValuesCollection
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: cebe15dc9a4f4347eb58563e9b43240464565a4c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105717778"
---
# <a name="iportabledevicevaluescollection-interface"></a><span data-ttu-id="2aa3f-103">Интерфейс Ипортабледевицевалуесколлектион</span><span class="sxs-lookup"><span data-stu-id="2aa3f-103">IPortableDeviceValuesCollection interface</span></span>

<span data-ttu-id="2aa3f-104">Интерфейс **ипортабледевицевалуесколлектион** содержит коллекцию индексируемых от нуля интерфейсов **ипортабледевицевалуес** .</span><span class="sxs-lookup"><span data-stu-id="2aa3f-104">The **IPortableDeviceValuesCollection** interface holds a collection of zero-based indexed **IPortableDeviceValues** interfaces.</span></span> <span data-ttu-id="2aa3f-105">Этот интерфейс можно извлечь из метода или, если требуется новый объект, вызвать **CREATE** с помощью **CLSID \_ портабледевицевалуесколлектион**.</span><span class="sxs-lookup"><span data-stu-id="2aa3f-105">This interface can be retrieved from a method, or if a new object is required, call **CoCreate** with **CLSID\_PortableDeviceValuesCollection**.</span></span>

## <a name="members"></a><span data-ttu-id="2aa3f-106">Элементы</span><span class="sxs-lookup"><span data-stu-id="2aa3f-106">Members</span></span>

<span data-ttu-id="2aa3f-107">Интерфейс **ипортабледевицевалуесколлектион** наследует от интерфейса [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="2aa3f-107">The **IPortableDeviceValuesCollection** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="2aa3f-108">**Ипортабледевицевалуесколлектион** также имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="2aa3f-108">**IPortableDeviceValuesCollection** also has these types of members:</span></span>

-   [<span data-ttu-id="2aa3f-109">Методы</span><span class="sxs-lookup"><span data-stu-id="2aa3f-109">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="2aa3f-110">Методы</span><span class="sxs-lookup"><span data-stu-id="2aa3f-110">Methods</span></span>

<span data-ttu-id="2aa3f-111">Интерфейс **ипортабледевицевалуесколлектион** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="2aa3f-111">The **IPortableDeviceValuesCollection** interface has these methods.</span></span>



| <span data-ttu-id="2aa3f-112">Метод</span><span class="sxs-lookup"><span data-stu-id="2aa3f-112">Method</span></span>                                                       | <span data-ttu-id="2aa3f-113">Описание</span><span class="sxs-lookup"><span data-stu-id="2aa3f-113">Description</span></span>                                                                         |
|:-------------------------------------------------------------|:------------------------------------------------------------------------------------|
| [<span data-ttu-id="2aa3f-114">**Включить**</span><span class="sxs-lookup"><span data-stu-id="2aa3f-114">**Add**</span></span>](iportabledevicevaluescollection-add.md)           | <span data-ttu-id="2aa3f-115">Добавляет элемент в коллекцию.</span><span class="sxs-lookup"><span data-stu-id="2aa3f-115">Adds an item to the collection</span></span><br/>                                           |
| [<span data-ttu-id="2aa3f-116">**Открытым**</span><span class="sxs-lookup"><span data-stu-id="2aa3f-116">**Clear**</span></span>](iportabledevicevaluescollection-clear.md)       | <span data-ttu-id="2aa3f-117">Освобождает все элементы из коллекции.</span><span class="sxs-lookup"><span data-stu-id="2aa3f-117">Releases all items from the collection.</span></span><br/>                                  |
| [<span data-ttu-id="2aa3f-118">**GetAt**</span><span class="sxs-lookup"><span data-stu-id="2aa3f-118">**GetAt**</span></span>](iportabledevicevaluescollection-getat.md)       | <span data-ttu-id="2aa3f-119">Извлекает элемент из коллекции по индексу, начинающимся с нуля.</span><span class="sxs-lookup"><span data-stu-id="2aa3f-119">Retrieves an item from the collection by a zero-based index.</span></span><br/>             |
| [<span data-ttu-id="2aa3f-120">**GetCount**</span><span class="sxs-lookup"><span data-stu-id="2aa3f-120">**GetCount**</span></span>](iportabledevicevaluescollection-getcount.md) | <span data-ttu-id="2aa3f-121">Возвращает количество элементов в коллекции.</span><span class="sxs-lookup"><span data-stu-id="2aa3f-121">Retrieves the number of items in the collection.</span></span><br/>                         |
| [<span data-ttu-id="2aa3f-122">**RemoveAt**</span><span class="sxs-lookup"><span data-stu-id="2aa3f-122">**RemoveAt**</span></span>](iportabledevicevaluescollection-removeat.md) | <span data-ttu-id="2aa3f-123">Удаляет элемент, хранящийся в расположении, указанном заданным индексом.</span><span class="sxs-lookup"><span data-stu-id="2aa3f-123">Removes the element stored at the location specified by the given index.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="2aa3f-124">Требования</span><span class="sxs-lookup"><span data-stu-id="2aa3f-124">Requirements</span></span>



| <span data-ttu-id="2aa3f-125">Требование</span><span class="sxs-lookup"><span data-stu-id="2aa3f-125">Requirement</span></span> | <span data-ttu-id="2aa3f-126">Значение</span><span class="sxs-lookup"><span data-stu-id="2aa3f-126">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2aa3f-127">Header</span><span class="sxs-lookup"><span data-stu-id="2aa3f-127">Header</span></span><br/>  | <dl> <span data-ttu-id="2aa3f-128"><dt>Портабледевицетипес. h</dt></span><span class="sxs-lookup"><span data-stu-id="2aa3f-128"><dt>PortableDeviceTypes.h</dt></span></span> </dl>   |
| <span data-ttu-id="2aa3f-129">Библиотека</span><span class="sxs-lookup"><span data-stu-id="2aa3f-129">Library</span></span><br/> | <dl> <span data-ttu-id="2aa3f-130"><dt>Портабледевицегуидс. lib</dt></span><span class="sxs-lookup"><span data-stu-id="2aa3f-130"><dt>PortableDeviceGUIDs.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2aa3f-131">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="2aa3f-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2aa3f-132">**Интерфейсы коллекции**</span><span class="sxs-lookup"><span data-stu-id="2aa3f-132">**Collection Interfaces**</span></span>](collection-interfaces.md)
</dt> </dl>

 

