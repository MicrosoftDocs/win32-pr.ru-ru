---
description: Извлекает сведения о других коллекциях, связанных с коллекцией, из которой она вызывается.
ms.assetid: daea5b23-6a13-46f4-89c8-0d93b614311e
title: Коллекция Релатедколлектионинфо
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- RelatedCollectionInfo
api_type:
- COM
api_location: ''
ms.openlocfilehash: 21a9a1905d75c81d605f30a3f6cffced8837034d
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104262620"
---
# <a name="relatedcollectioninfo-collection"></a><span data-ttu-id="ab200-103">Коллекция Релатедколлектионинфо</span><span class="sxs-lookup"><span data-stu-id="ab200-103">RelatedCollectionInfo collection</span></span>

<span data-ttu-id="ab200-104">Извлекает сведения о других коллекциях, связанных с коллекцией, из которой она вызывается.</span><span class="sxs-lookup"><span data-stu-id="ab200-104">Retrieves information about other collections related to the collection from which it is called.</span></span> <span data-ttu-id="ab200-105">Коллекция **релатедколлектионинфо** доступна из любого объекта [**комадминкаталогколлектион**](comadmincatalogcollection.md) с помощью метода [**IsCollection**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-getcollection) .</span><span class="sxs-lookup"><span data-stu-id="ab200-105">The **RelatedCollectionInfo** collection is accessible from any [**COMAdminCatalogCollection**](comadmincatalogcollection.md) object by using the [**GetCollection**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-getcollection) method.</span></span> <span data-ttu-id="ab200-106">Коллекция **релатедколлектионинфо** содержит по одному объекту для каждой коллекции, доступной из исходной коллекции.</span><span class="sxs-lookup"><span data-stu-id="ab200-106">The **RelatedCollectionInfo** collection contains one object for each collection that is accessible from the original collection.</span></span> <span data-ttu-id="ab200-107">Связанные коллекции соответствуют иерархии коллекции средств администрирования служб компонентов.</span><span class="sxs-lookup"><span data-stu-id="ab200-107">Related collections follow the Component Services administration tool collection hierarchy.</span></span>

<span data-ttu-id="ab200-108">Эта коллекция не поддерживает методы [**Add**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add) и [**Remove**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove) объекта [**комадминкаталогколлектион**](comadmincatalogcollection.md) .</span><span class="sxs-lookup"><span data-stu-id="ab200-108">This collection does not support the [**Add**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add) and [**Remove**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove) methods of the [**COMAdminCatalogCollection**](comadmincatalogcollection.md) object.</span></span>

## <a name="members"></a><span data-ttu-id="ab200-109">Элементы</span><span class="sxs-lookup"><span data-stu-id="ab200-109">Members</span></span>

<span data-ttu-id="ab200-110">Коллекция **релатедколлектионинфо** наследует от интерфейса [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) , но не содержит дополнительных элементов.</span><span class="sxs-lookup"><span data-stu-id="ab200-110">The **RelatedCollectionInfo** collection inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface but does not have additional members.</span></span>

## <a name="related-collections"></a><span data-ttu-id="ab200-111">Связанные коллекции</span><span class="sxs-lookup"><span data-stu-id="ab200-111">Related Collections</span></span>

<span data-ttu-id="ab200-112">Можно переходить от этой коллекции к любой из следующих коллекций:</span><span class="sxs-lookup"><span data-stu-id="ab200-112">You can navigate from this collection to any of the following collections:</span></span>

-   [<span data-ttu-id="ab200-113">**PropertyInfo**</span><span class="sxs-lookup"><span data-stu-id="ab200-113">**PropertyInfo**</span></span>](propertyinfo.md)
-   <span data-ttu-id="ab200-114">**релатедколлектионинфо**</span><span class="sxs-lookup"><span data-stu-id="ab200-114">**RelatedCollectionInfo**</span></span>

<span data-ttu-id="ab200-115">Можно переходить к этой коллекции из каждой коллекции.</span><span class="sxs-lookup"><span data-stu-id="ab200-115">You can navigate to this collection from every collection.</span></span>

## <a name="properties"></a><span data-ttu-id="ab200-116">Свойства</span><span class="sxs-lookup"><span data-stu-id="ab200-116">Properties</span></span>

<span data-ttu-id="ab200-117">Объект [**комадминкаталогобжект**](comadmincatalogobject.md) в коллекции поддерживает следующие свойства:</span><span class="sxs-lookup"><span data-stu-id="ab200-117">The following properties are supported by the [**COMAdminCatalogObject**](comadmincatalogobject.md) object within the collection:</span></span>

-   [<span data-ttu-id="ab200-118">Name</span><span class="sxs-lookup"><span data-stu-id="ab200-118">Name</span></span>](#name)

### <a name="name"></a><span data-ttu-id="ab200-119">Имя</span><span class="sxs-lookup"><span data-stu-id="ab200-119">Name</span></span>



| <span data-ttu-id="ab200-120">Ввод</span><span class="sxs-lookup"><span data-stu-id="ab200-120">Entry</span></span> | <span data-ttu-id="ab200-121">Значение</span><span class="sxs-lookup"><span data-stu-id="ab200-121">Value</span></span> |
|----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ab200-122">Описание</span><span class="sxs-lookup"><span data-stu-id="ab200-122">Description</span></span>    | <span data-ttu-id="ab200-123">Имя связанной коллекции.</span><span class="sxs-lookup"><span data-stu-id="ab200-123">The name of the related collection.</span></span> <span data-ttu-id="ab200-124">Это свойство возвращается при вызове метода свойства [**Key**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) или [**Name**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_name) для объекта этой коллекции.</span><span class="sxs-lookup"><span data-stu-id="ab200-124">This property is returned when the [**Key**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) or [**Name**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_name) property method is called on an object of this collection.</span></span> |
| <span data-ttu-id="ab200-125">Access</span><span class="sxs-lookup"><span data-stu-id="ab200-125">Access</span></span>         | <span data-ttu-id="ab200-126">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="ab200-126">ReadOnly</span></span>                                                                                                                                                                                                   |
| <span data-ttu-id="ab200-127">Тип</span><span class="sxs-lookup"><span data-stu-id="ab200-127">Type</span></span>           | <span data-ttu-id="ab200-128">Строка</span><span class="sxs-lookup"><span data-stu-id="ab200-128">String</span></span>                                                                                                                                                                                                     |
| <span data-ttu-id="ab200-129">По умолчанию</span><span class="sxs-lookup"><span data-stu-id="ab200-129">Default</span></span>        | <span data-ttu-id="ab200-130">None</span><span class="sxs-lookup"><span data-stu-id="ab200-130">None</span></span>                                                                                                                                                                                                       |
| <span data-ttu-id="ab200-131">Минимальная система</span><span class="sxs-lookup"><span data-stu-id="ab200-131">Minimum system</span></span> | <span data-ttu-id="ab200-132">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="ab200-132">Windows 2000</span></span>                                                                                                                                                                                               |



 

## <a name="see-also"></a><span data-ttu-id="ab200-133">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="ab200-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ab200-134">Коллекции администрирования COM+</span><span class="sxs-lookup"><span data-stu-id="ab200-134">COM+ Administration Collections</span></span>](com--administration-collections.md)
</dt> </dl>

 

 
