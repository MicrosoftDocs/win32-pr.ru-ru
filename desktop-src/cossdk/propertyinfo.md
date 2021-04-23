---
description: Извлекает сведения о свойствах, поддерживаемых указанной коллекцией.
ms.assetid: 5e3963c0-6769-4b5b-8636-2d8c98a8776b
title: Коллекция PropertyInfo
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PropertyInfo
api_type:
- COM
api_location: ''
ms.openlocfilehash: bd9fdd2262d4499efd6a86fbc5b99bae786016f3
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104141806"
---
# <a name="propertyinfo-collection"></a><span data-ttu-id="be4fc-103">Коллекция PropertyInfo</span><span class="sxs-lookup"><span data-stu-id="be4fc-103">PropertyInfo collection</span></span>

<span data-ttu-id="be4fc-104">Извлекает сведения о свойствах, поддерживаемых указанной коллекцией.</span><span class="sxs-lookup"><span data-stu-id="be4fc-104">Retrieves information about the properties that a specified collection supports.</span></span> <span data-ttu-id="be4fc-105">Коллекция **PropertyInfo** доступна из любого объекта [**комадминкаталогколлектион**](comadmincatalogcollection.md) с помощью метода [**IsCollection**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-getcollection) .</span><span class="sxs-lookup"><span data-stu-id="be4fc-105">The **PropertyInfo** collection is accessible from any [**COMAdminCatalogCollection**](comadmincatalogcollection.md) object by using the [**GetCollection**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-getcollection) method.</span></span> <span data-ttu-id="be4fc-106">Коллекция **PropertyInfo** содержит по одному объекту для каждого свойства, которое поддерживается исходной коллекцией.</span><span class="sxs-lookup"><span data-stu-id="be4fc-106">The **PropertyInfo** collection contains one object for each property that is supported by the original collection.</span></span>

## <a name="members"></a><span data-ttu-id="be4fc-107">Элементы</span><span class="sxs-lookup"><span data-stu-id="be4fc-107">Members</span></span>

<span data-ttu-id="be4fc-108">Коллекция **PropertyInfo** наследует от интерфейса [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) , но не содержит дополнительных элементов.</span><span class="sxs-lookup"><span data-stu-id="be4fc-108">The **PropertyInfo** collection inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface but does not have additional members.</span></span>

## <a name="related-collections"></a><span data-ttu-id="be4fc-109">Связанные коллекции</span><span class="sxs-lookup"><span data-stu-id="be4fc-109">Related Collections</span></span>

<span data-ttu-id="be4fc-110">Можно переходить от этой коллекции к любой из следующих коллекций:</span><span class="sxs-lookup"><span data-stu-id="be4fc-110">You can navigate from this collection to any of the following collections:</span></span>

-   <span data-ttu-id="be4fc-111">**PropertyInfo**</span><span class="sxs-lookup"><span data-stu-id="be4fc-111">**PropertyInfo**</span></span>
-   [<span data-ttu-id="be4fc-112">**релатедколлектионинфо**</span><span class="sxs-lookup"><span data-stu-id="be4fc-112">**RelatedCollectionInfo**</span></span>](relatedcollectioninfo.md)

<span data-ttu-id="be4fc-113">Можно переходить к этой коллекции из каждой коллекции.</span><span class="sxs-lookup"><span data-stu-id="be4fc-113">You can navigate to this collection from every collection.</span></span>

## <a name="properties"></a><span data-ttu-id="be4fc-114">Свойства</span><span class="sxs-lookup"><span data-stu-id="be4fc-114">Properties</span></span>

<span data-ttu-id="be4fc-115">Объект [**комадминкаталогобжект**](comadmincatalogobject.md) в коллекции поддерживает следующие свойства:</span><span class="sxs-lookup"><span data-stu-id="be4fc-115">The following properties are supported by the [**COMAdminCatalogObject**](comadmincatalogobject.md) object within the collection:</span></span>

-   [<span data-ttu-id="be4fc-116">Name</span><span class="sxs-lookup"><span data-stu-id="be4fc-116">Name</span></span>](#name)

### <a name="name"></a><span data-ttu-id="be4fc-117">Имя</span><span class="sxs-lookup"><span data-stu-id="be4fc-117">Name</span></span>



| <span data-ttu-id="be4fc-118">Ввод</span><span class="sxs-lookup"><span data-stu-id="be4fc-118">Entry</span></span> | <span data-ttu-id="be4fc-119">Значение</span><span class="sxs-lookup"><span data-stu-id="be4fc-119">Value</span></span> |
|----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="be4fc-120">Описание</span><span class="sxs-lookup"><span data-stu-id="be4fc-120">Description</span></span>    | <span data-ttu-id="be4fc-121">Имя свойства.</span><span class="sxs-lookup"><span data-stu-id="be4fc-121">The name of the property.</span></span> <span data-ttu-id="be4fc-122">Это свойство возвращается при вызове метода свойства [**Key**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) или [**Name**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_name) для объекта этой коллекции.</span><span class="sxs-lookup"><span data-stu-id="be4fc-122">This property is returned when the [**Key**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) or [**Name**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_name) property method is called on an object of this collection.</span></span> |
| <span data-ttu-id="be4fc-123">Access</span><span class="sxs-lookup"><span data-stu-id="be4fc-123">Access</span></span>         | <span data-ttu-id="be4fc-124">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="be4fc-124">ReadOnly</span></span>                                                                                                                                                                                         |
| <span data-ttu-id="be4fc-125">Тип</span><span class="sxs-lookup"><span data-stu-id="be4fc-125">Type</span></span>           | <span data-ttu-id="be4fc-126">Строка</span><span class="sxs-lookup"><span data-stu-id="be4fc-126">String</span></span>                                                                                                                                                                                           |
| <span data-ttu-id="be4fc-127">По умолчанию</span><span class="sxs-lookup"><span data-stu-id="be4fc-127">Default</span></span>        | <span data-ttu-id="be4fc-128">None</span><span class="sxs-lookup"><span data-stu-id="be4fc-128">None</span></span>                                                                                                                                                                                             |
| <span data-ttu-id="be4fc-129">Минимальная система</span><span class="sxs-lookup"><span data-stu-id="be4fc-129">Minimum system</span></span> | <span data-ttu-id="be4fc-130">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="be4fc-130">Windows 2000</span></span>                                                                                                                                                                                     |



 

## <a name="see-also"></a><span data-ttu-id="be4fc-131">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="be4fc-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="be4fc-132">Коллекции администрирования COM+</span><span class="sxs-lookup"><span data-stu-id="be4fc-132">COM+ Administration Collections</span></span>](com--administration-collections.md)
</dt> </dl>

 

 
