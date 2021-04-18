---
description: Интерфейс Ипортабледевицекэйколлектион содержит коллекцию значений PROPERTYKEY. Этот интерфейс можно получить из метода или, если требуется новый объект, вызовите Create с помощью CLSID \_ портабледевицекэйколлектион.
ms.assetid: 2460f5bc-6b1c-4e3b-bdb9-faaa6d6c87fd
title: Интерфейс Ипортабледевицекэйколлектион (Портабледевицетипес. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDeviceKeyCollection
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: c246fabe7ced72a5aad6d30101df8035a159a923
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105708348"
---
# <a name="iportabledevicekeycollection-interface"></a><span data-ttu-id="9fff0-104">Интерфейс Ипортабледевицекэйколлектион</span><span class="sxs-lookup"><span data-stu-id="9fff0-104">IPortableDeviceKeyCollection interface</span></span>

<span data-ttu-id="9fff0-105">Интерфейс **ипортабледевицекэйколлектион** содержит коллекцию значений **PROPERTYKEY** .</span><span class="sxs-lookup"><span data-stu-id="9fff0-105">The **IPortableDeviceKeyCollection** interface holds a collection of **PROPERTYKEY** values.</span></span> <span data-ttu-id="9fff0-106">Этот интерфейс можно получить из метода или, если требуется новый объект, вызовите **CREATE** с помощью **CLSID \_ портабледевицекэйколлектион**.</span><span class="sxs-lookup"><span data-stu-id="9fff0-106">This interface can be retrieved from a method or, if a new object is required, call **CoCreate** with **CLSID\_PortableDeviceKeyCollection**.</span></span>

## <a name="members"></a><span data-ttu-id="9fff0-107">Элементы</span><span class="sxs-lookup"><span data-stu-id="9fff0-107">Members</span></span>

<span data-ttu-id="9fff0-108">Интерфейс **ипортабледевицекэйколлектион** наследует от интерфейса [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="9fff0-108">The **IPortableDeviceKeyCollection** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="9fff0-109">**Ипортабледевицекэйколлектион** также имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="9fff0-109">**IPortableDeviceKeyCollection** also has these types of members:</span></span>

-   [<span data-ttu-id="9fff0-110">Методы</span><span class="sxs-lookup"><span data-stu-id="9fff0-110">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="9fff0-111">Методы</span><span class="sxs-lookup"><span data-stu-id="9fff0-111">Methods</span></span>

<span data-ttu-id="9fff0-112">Интерфейс **ипортабледевицекэйколлектион** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="9fff0-112">The **IPortableDeviceKeyCollection** interface has these methods.</span></span>



| <span data-ttu-id="9fff0-113">Метод</span><span class="sxs-lookup"><span data-stu-id="9fff0-113">Method</span></span>                                                    | <span data-ttu-id="9fff0-114">Описание</span><span class="sxs-lookup"><span data-stu-id="9fff0-114">Description</span></span>                                                                         |
|:----------------------------------------------------------|:------------------------------------------------------------------------------------|
| [<span data-ttu-id="9fff0-115">**Включить**</span><span class="sxs-lookup"><span data-stu-id="9fff0-115">**Add**</span></span>](iportabledevicekeycollection-add.md)           | <span data-ttu-id="9fff0-116">Добавляет ключ свойства в коллекцию.</span><span class="sxs-lookup"><span data-stu-id="9fff0-116">Adds a property key to the collection.</span></span><br/>                                   |
| [<span data-ttu-id="9fff0-117">**Открытым**</span><span class="sxs-lookup"><span data-stu-id="9fff0-117">**Clear**</span></span>](iportabledevicekeycollection-clear.md)       | <span data-ttu-id="9fff0-118">Удаляет все элементы из коллекции.</span><span class="sxs-lookup"><span data-stu-id="9fff0-118">Deletes all items from the collection.</span></span><br/>                                   |
| [<span data-ttu-id="9fff0-119">**GetAt**</span><span class="sxs-lookup"><span data-stu-id="9fff0-119">**GetAt**</span></span>](iportabledevicekeycollection-getat.md)       | <span data-ttu-id="9fff0-120">Извлекает **PROPERTYKEY** из коллекции по индексу.</span><span class="sxs-lookup"><span data-stu-id="9fff0-120">Retrieves a **PROPERTYKEY** from the collection by index.</span></span><br/>                |
| [<span data-ttu-id="9fff0-121">**GetCount**</span><span class="sxs-lookup"><span data-stu-id="9fff0-121">**GetCount**</span></span>](iportabledevicekeycollection-getcount.md) | <span data-ttu-id="9fff0-122">Возвращает число ключей в этой коллекции.</span><span class="sxs-lookup"><span data-stu-id="9fff0-122">Retrieves the number of keys in this collection.</span></span><br/>                         |
| [<span data-ttu-id="9fff0-123">**RemoveAt**</span><span class="sxs-lookup"><span data-stu-id="9fff0-123">**RemoveAt**</span></span>](iportabledevicekeycollection-removeat.md) | <span data-ttu-id="9fff0-124">Удаляет элемент, хранящийся в расположении, указанном заданным индексом.</span><span class="sxs-lookup"><span data-stu-id="9fff0-124">Removes the element stored at the location specified by the given index.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="9fff0-125">Требования</span><span class="sxs-lookup"><span data-stu-id="9fff0-125">Requirements</span></span>



| <span data-ttu-id="9fff0-126">Требование</span><span class="sxs-lookup"><span data-stu-id="9fff0-126">Requirement</span></span> | <span data-ttu-id="9fff0-127">Значение</span><span class="sxs-lookup"><span data-stu-id="9fff0-127">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9fff0-128">Header</span><span class="sxs-lookup"><span data-stu-id="9fff0-128">Header</span></span><br/>  | <dl> <span data-ttu-id="9fff0-129"><dt>Портабледевицетипес. h</dt></span><span class="sxs-lookup"><span data-stu-id="9fff0-129"><dt>PortableDeviceTypes.h</dt></span></span> </dl>   |
| <span data-ttu-id="9fff0-130">Библиотека</span><span class="sxs-lookup"><span data-stu-id="9fff0-130">Library</span></span><br/> | <dl> <span data-ttu-id="9fff0-131"><dt>Портабледевицегуидс. lib</dt></span><span class="sxs-lookup"><span data-stu-id="9fff0-131"><dt>PortableDeviceGUIDs.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9fff0-132">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="9fff0-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9fff0-133">**Интерфейсы коллекции**</span><span class="sxs-lookup"><span data-stu-id="9fff0-133">**Collection Interfaces**</span></span>](collection-interfaces.md)
</dt> </dl>

 

