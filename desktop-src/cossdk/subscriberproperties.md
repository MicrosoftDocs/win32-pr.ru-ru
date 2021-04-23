---
description: Содержит объект для каждого свойства подписчика для родительской коллекции Субскриптионсфоркомпонент.
ms.assetid: 58c9edbd-1128-4b8c-bb5a-528c212aa6a7
title: Коллекция Субскриберпропертиес
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SubscriberProperties
api_type:
- COM
api_location: ''
ms.openlocfilehash: 7c7a563e3fd3e917812426e34debd87bfd534b46
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103895738"
---
# <a name="subscriberproperties-collection"></a><span data-ttu-id="01002-103">Коллекция Субскриберпропертиес</span><span class="sxs-lookup"><span data-stu-id="01002-103">SubscriberProperties collection</span></span>

<span data-ttu-id="01002-104">Содержит объект для каждого свойства подписчика для родительской коллекции [**субскриптионсфоркомпонент**](subscriptionsforcomponent.md) .</span><span class="sxs-lookup"><span data-stu-id="01002-104">Contains an object for each subscriber property for the parent [**SubscriptionsForComponent**](subscriptionsforcomponent.md) collection.</span></span>

<span data-ttu-id="01002-105">Эта коллекция поддерживает методы [**Add**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add) и [**Remove**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove) объекта [**комадминкаталогколлектион**](comadmincatalogcollection.md) .</span><span class="sxs-lookup"><span data-stu-id="01002-105">This collection supports the [**Add**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add) and [**Remove**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove) methods of the [**COMAdminCatalogCollection**](comadmincatalogcollection.md) object.</span></span>

## <a name="members"></a><span data-ttu-id="01002-106">Элементы</span><span class="sxs-lookup"><span data-stu-id="01002-106">Members</span></span>

<span data-ttu-id="01002-107">Коллекция **субскриберпропертиес** наследует от интерфейса [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) , но не содержит дополнительных элементов.</span><span class="sxs-lookup"><span data-stu-id="01002-107">The **SubscriberProperties** collection inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface but does not have additional members.</span></span>

## <a name="related-collections"></a><span data-ttu-id="01002-108">Связанные коллекции</span><span class="sxs-lookup"><span data-stu-id="01002-108">Related Collections</span></span>

<span data-ttu-id="01002-109">Можно переходить от этой коллекции к любой из следующих коллекций:</span><span class="sxs-lookup"><span data-stu-id="01002-109">You can navigate from this collection to any of the following collections:</span></span>

-   [<span data-ttu-id="01002-110">**ErrorInfo**</span><span class="sxs-lookup"><span data-stu-id="01002-110">**ErrorInfo**</span></span>](errorinfo.md)
-   [<span data-ttu-id="01002-111">**PropertyInfo**</span><span class="sxs-lookup"><span data-stu-id="01002-111">**PropertyInfo**</span></span>](propertyinfo.md)
-   [<span data-ttu-id="01002-112">**релатедколлектионинфо**</span><span class="sxs-lookup"><span data-stu-id="01002-112">**RelatedCollectionInfo**</span></span>](relatedcollectioninfo.md)

<span data-ttu-id="01002-113">Вы можете переходить к этой коллекции из следующих коллекций:</span><span class="sxs-lookup"><span data-stu-id="01002-113">You can navigate to this collection from the following collections:</span></span>

-   [<span data-ttu-id="01002-114">**субскриптионсфоркомпонент**</span><span class="sxs-lookup"><span data-stu-id="01002-114">**SubscriptionsForComponent**</span></span>](subscriptionsforcomponent.md)

## <a name="properties"></a><span data-ttu-id="01002-115">Свойства</span><span class="sxs-lookup"><span data-stu-id="01002-115">Properties</span></span>

<span data-ttu-id="01002-116">Объект [**комадминкаталогобжект**](comadmincatalogobject.md) в коллекции поддерживает следующие свойства:</span><span class="sxs-lookup"><span data-stu-id="01002-116">The following properties are supported by the [**COMAdminCatalogObject**](comadmincatalogobject.md) object within the collection:</span></span>

-   [<span data-ttu-id="01002-117">Name</span><span class="sxs-lookup"><span data-stu-id="01002-117">Name</span></span>](#name)
-   [<span data-ttu-id="01002-118">Значение</span><span class="sxs-lookup"><span data-stu-id="01002-118">Value</span></span>](#value)

### <a name="name"></a><span data-ttu-id="01002-119">Имя</span><span class="sxs-lookup"><span data-stu-id="01002-119">Name</span></span>



| <span data-ttu-id="01002-120">Ввод</span><span class="sxs-lookup"><span data-stu-id="01002-120">Entry</span></span> | <span data-ttu-id="01002-121">Значение</span><span class="sxs-lookup"><span data-stu-id="01002-121">Value</span></span> |
|----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="01002-122">Описание</span><span class="sxs-lookup"><span data-stu-id="01002-122">Description</span></span>    | <span data-ttu-id="01002-123">Имя свойства.</span><span class="sxs-lookup"><span data-stu-id="01002-123">The name of the property.</span></span> <span data-ttu-id="01002-124">Лишние пробелы в начале и конце строки удаляются. Это свойство возвращается при вызове метода свойства [**Key**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) или [**Name**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_name) для объекта этой коллекции.</span><span class="sxs-lookup"><span data-stu-id="01002-124">Extra spaces at the beginning and end of the string are stripped out. This property is returned when the [**Key**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) or [**Name**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_name) property method is called on an object of this collection.</span></span> |
| <span data-ttu-id="01002-125">Access</span><span class="sxs-lookup"><span data-stu-id="01002-125">Access</span></span>         | <span data-ttu-id="01002-126">Флагом writeonce</span><span class="sxs-lookup"><span data-stu-id="01002-126">WriteOnce</span></span>                                                                                                                                                                                                                                                              |
| <span data-ttu-id="01002-127">Тип</span><span class="sxs-lookup"><span data-stu-id="01002-127">Type</span></span>           | <span data-ttu-id="01002-128">Строка</span><span class="sxs-lookup"><span data-stu-id="01002-128">String</span></span>                                                                                                                                                                                                                                                                 |
| <span data-ttu-id="01002-129">По умолчанию</span><span class="sxs-lookup"><span data-stu-id="01002-129">Default</span></span>        | <span data-ttu-id="01002-130">"Создать свойство"</span><span class="sxs-lookup"><span data-stu-id="01002-130">"New Property"</span></span>                                                                                                                                                                                                                                                         |
| <span data-ttu-id="01002-131">Минимальная система</span><span class="sxs-lookup"><span data-stu-id="01002-131">Minimum system</span></span> | <span data-ttu-id="01002-132">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="01002-132">Windows 2000</span></span>                                                                                                                                                                                                                                                           |



 

### <a name="value"></a><span data-ttu-id="01002-133">Значение</span><span class="sxs-lookup"><span data-stu-id="01002-133">Value</span></span>



| <span data-ttu-id="01002-134">Ввод</span><span class="sxs-lookup"><span data-stu-id="01002-134">Entry</span></span> | <span data-ttu-id="01002-135">Значение</span><span class="sxs-lookup"><span data-stu-id="01002-135">Value</span></span> |
|----------------|---------------------------|
| <span data-ttu-id="01002-136">Описание</span><span class="sxs-lookup"><span data-stu-id="01002-136">Description</span></span>    | <span data-ttu-id="01002-137">Значение для свойства.</span><span class="sxs-lookup"><span data-stu-id="01002-137">A value for the property.</span></span> |
| <span data-ttu-id="01002-138">Access</span><span class="sxs-lookup"><span data-stu-id="01002-138">Access</span></span>         | <span data-ttu-id="01002-139">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="01002-139">ReadWrite</span></span>                 |
| <span data-ttu-id="01002-140">Тип</span><span class="sxs-lookup"><span data-stu-id="01002-140">Type</span></span>           | <span data-ttu-id="01002-141">Variant</span><span class="sxs-lookup"><span data-stu-id="01002-141">Variant</span></span>                   |
| <span data-ttu-id="01002-142">Значение по умолчанию</span><span class="sxs-lookup"><span data-stu-id="01002-142">Default</span></span>        | <span data-ttu-id="01002-143">Н/Д</span><span class="sxs-lookup"><span data-stu-id="01002-143">N/A</span></span>                       |
| <span data-ttu-id="01002-144">Минимальная система</span><span class="sxs-lookup"><span data-stu-id="01002-144">Minimum system</span></span> | <span data-ttu-id="01002-145">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="01002-145">Windows 2000</span></span>              |



 

## <a name="see-also"></a><span data-ttu-id="01002-146">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="01002-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="01002-147">Коллекции администрирования COM+</span><span class="sxs-lookup"><span data-stu-id="01002-147">COM+ Administration Collections</span></span>](com--administration-collections.md)
</dt> </dl>

 

 
