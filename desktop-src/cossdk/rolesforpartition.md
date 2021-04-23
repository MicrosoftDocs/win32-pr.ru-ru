---
description: Коллекция Ролесфорпартитион всегда связана с объектом в коллекции секций. Он содержит объект для каждой роли, назначенной секции, к которой она относится.
ms.assetid: 56985f55-d6e8-4066-b6d5-21c62d4278ce
title: Коллекция Ролесфорпартитион
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- RolesForPartition
api_type:
- COM
api_location: ''
ms.openlocfilehash: c97d524e3fc516086db3a815396d6d59f9369b31
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104141207"
---
# <a name="rolesforpartition-collection"></a><span data-ttu-id="1b98c-104">Коллекция Ролесфорпартитион</span><span class="sxs-lookup"><span data-stu-id="1b98c-104">RolesForPartition collection</span></span>

<span data-ttu-id="1b98c-105">Коллекция **ролесфорпартитион** всегда связана с объектом в коллекции [**секций**](partitions.md) .</span><span class="sxs-lookup"><span data-stu-id="1b98c-105">The **RolesForPartition** collection is always related to an object in the [**Partitions**](partitions.md) collection.</span></span> <span data-ttu-id="1b98c-106">Он содержит объект для каждой роли, назначенной секции, к которой она относится.</span><span class="sxs-lookup"><span data-stu-id="1b98c-106">It holds an object for each role assigned to the partition to which it is related.</span></span>

<span data-ttu-id="1b98c-107">Эта коллекция не поддерживает методы [**Add**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add) и [**Remove**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove) объекта [**комадминкаталогколлектион**](comadmincatalogcollection.md) .</span><span class="sxs-lookup"><span data-stu-id="1b98c-107">This collection does not support the [**Add**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add) and [**Remove**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove) methods of the [**COMAdminCatalogCollection**](comadmincatalogcollection.md) object.</span></span>

## <a name="members"></a><span data-ttu-id="1b98c-108">Элементы</span><span class="sxs-lookup"><span data-stu-id="1b98c-108">Members</span></span>

<span data-ttu-id="1b98c-109">Коллекция **ролесфорпартитион** наследует от интерфейса [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) , но не содержит дополнительных элементов.</span><span class="sxs-lookup"><span data-stu-id="1b98c-109">The **RolesForPartition** collection inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface but does not have additional members.</span></span>

## <a name="related-collections"></a><span data-ttu-id="1b98c-110">Связанные коллекции</span><span class="sxs-lookup"><span data-stu-id="1b98c-110">Related Collections</span></span>

<span data-ttu-id="1b98c-111">Можно переходить от этой коллекции к любой из следующих коллекций:</span><span class="sxs-lookup"><span data-stu-id="1b98c-111">You can navigate from this collection to any of the following collections:</span></span>

-   [<span data-ttu-id="1b98c-112">**ErrorInfo**</span><span class="sxs-lookup"><span data-stu-id="1b98c-112">**ErrorInfo**</span></span>](errorinfo.md)
-   [<span data-ttu-id="1b98c-113">**PropertyInfo**</span><span class="sxs-lookup"><span data-stu-id="1b98c-113">**PropertyInfo**</span></span>](propertyinfo.md)
-   [<span data-ttu-id="1b98c-114">**релатедколлектионинфо**</span><span class="sxs-lookup"><span data-stu-id="1b98c-114">**RelatedCollectionInfo**</span></span>](relatedcollectioninfo.md)
-   [<span data-ttu-id="1b98c-115">**усерсинпартитионроле**</span><span class="sxs-lookup"><span data-stu-id="1b98c-115">**UsersInPartitionRole**</span></span>](usersinpartitionrole.md)

<span data-ttu-id="1b98c-116">Вы можете переходить к этой коллекции из следующих коллекций:</span><span class="sxs-lookup"><span data-stu-id="1b98c-116">You can navigate to this collection from the following collections:</span></span>

-   [<span data-ttu-id="1b98c-117">**Секции**</span><span class="sxs-lookup"><span data-stu-id="1b98c-117">**Partitions**</span></span>](partitions.md)

## <a name="properties"></a><span data-ttu-id="1b98c-118">Свойства</span><span class="sxs-lookup"><span data-stu-id="1b98c-118">Properties</span></span>

<span data-ttu-id="1b98c-119">Объект [**комадминкаталогобжект**](comadmincatalogobject.md) в коллекции поддерживает следующие свойства:</span><span class="sxs-lookup"><span data-stu-id="1b98c-119">The following properties are supported by the [**COMAdminCatalogObject**](comadmincatalogobject.md) object within the collection:</span></span>

-   [<span data-ttu-id="1b98c-120">Описание</span><span class="sxs-lookup"><span data-stu-id="1b98c-120">Description</span></span>](#description)
-   [<span data-ttu-id="1b98c-121">Имя</span><span class="sxs-lookup"><span data-stu-id="1b98c-121">Name</span></span>](#name)

### <a name="description"></a><span data-ttu-id="1b98c-122">Описание</span><span class="sxs-lookup"><span data-stu-id="1b98c-122">Description</span></span>



| <span data-ttu-id="1b98c-123">Ввод</span><span class="sxs-lookup"><span data-stu-id="1b98c-123">Entry</span></span> | <span data-ttu-id="1b98c-124">Значение</span><span class="sxs-lookup"><span data-stu-id="1b98c-124">Value</span></span> |
|----------------|----------------------------|
| <span data-ttu-id="1b98c-125">Описание</span><span class="sxs-lookup"><span data-stu-id="1b98c-125">Description</span></span>    | <span data-ttu-id="1b98c-126">Описание роли.</span><span class="sxs-lookup"><span data-stu-id="1b98c-126">A description of the role.</span></span> |
| <span data-ttu-id="1b98c-127">Access</span><span class="sxs-lookup"><span data-stu-id="1b98c-127">Access</span></span>         | <span data-ttu-id="1b98c-128">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="1b98c-128">ReadOnly</span></span>                   |
| <span data-ttu-id="1b98c-129">Тип</span><span class="sxs-lookup"><span data-stu-id="1b98c-129">Type</span></span>           | <span data-ttu-id="1b98c-130">Строка</span><span class="sxs-lookup"><span data-stu-id="1b98c-130">String</span></span>                     |
| <span data-ttu-id="1b98c-131">По умолчанию</span><span class="sxs-lookup"><span data-stu-id="1b98c-131">Default</span></span>        | <span data-ttu-id="1b98c-132">""</span><span class="sxs-lookup"><span data-stu-id="1b98c-132">""</span></span>                         |
| <span data-ttu-id="1b98c-133">Минимальная система</span><span class="sxs-lookup"><span data-stu-id="1b98c-133">Minimum system</span></span> | <span data-ttu-id="1b98c-134">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="1b98c-134">Windows Server 2003</span></span>        |



 

### <a name="name"></a><span data-ttu-id="1b98c-135">Имя</span><span class="sxs-lookup"><span data-stu-id="1b98c-135">Name</span></span>



| <span data-ttu-id="1b98c-136">Ввод</span><span class="sxs-lookup"><span data-stu-id="1b98c-136">Entry</span></span> | <span data-ttu-id="1b98c-137">Значение</span><span class="sxs-lookup"><span data-stu-id="1b98c-137">Value</span></span> |
|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1b98c-138">Описание</span><span class="sxs-lookup"><span data-stu-id="1b98c-138">Description</span></span>    | <span data-ttu-id="1b98c-139">Имя роли.</span><span class="sxs-lookup"><span data-stu-id="1b98c-139">The role name.</span></span> <span data-ttu-id="1b98c-140">Лишние пробелы в начале и конце строки удаляются. Это свойство возвращается при вызове метода свойства [**Key**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) или [**Name**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_name) для объекта этой коллекции.</span><span class="sxs-lookup"><span data-stu-id="1b98c-140">Extra spaces at the beginning and end of the string are stripped out. This property is returned when the [**Key**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) or [**Name**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_name) property method is called on an object of this collection.</span></span> |
| <span data-ttu-id="1b98c-141">Access</span><span class="sxs-lookup"><span data-stu-id="1b98c-141">Access</span></span>         | <span data-ttu-id="1b98c-142">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="1b98c-142">ReadOnly</span></span>                                                                                                                                                                                                                                                    |
| <span data-ttu-id="1b98c-143">Тип</span><span class="sxs-lookup"><span data-stu-id="1b98c-143">Type</span></span>           | <span data-ttu-id="1b98c-144">Строка</span><span class="sxs-lookup"><span data-stu-id="1b98c-144">String</span></span>                                                                                                                                                                                                                                                      |
| <span data-ttu-id="1b98c-145">По умолчанию</span><span class="sxs-lookup"><span data-stu-id="1b98c-145">Default</span></span>        | <span data-ttu-id="1b98c-146">""</span><span class="sxs-lookup"><span data-stu-id="1b98c-146">""</span></span>                                                                                                                                                                                                                                                          |
| <span data-ttu-id="1b98c-147">Минимальная система</span><span class="sxs-lookup"><span data-stu-id="1b98c-147">Minimum system</span></span> | <span data-ttu-id="1b98c-148">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="1b98c-148">Windows Server 2003</span></span>                                                                                                                                                                                                                                         |



 

## <a name="see-also"></a><span data-ttu-id="1b98c-149">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="1b98c-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1b98c-150">Коллекции администрирования COM+</span><span class="sxs-lookup"><span data-stu-id="1b98c-150">COM+ Administration Collections</span></span>](com--administration-collections.md)
</dt> </dl>

 

 
