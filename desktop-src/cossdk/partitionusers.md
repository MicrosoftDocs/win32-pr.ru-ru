---
description: Содержит объект для каждого пользователя секции.
ms.assetid: baec56ae-be8a-42a7-90bc-1db7c5cd7fe2
title: Коллекция Партитионусерс
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PartitionUsers
api_type:
- COM
api_location: ''
ms.openlocfilehash: 1521642879037938451decd873a9aa14211ce296
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105701267"
---
# <a name="partitionusers-collection"></a><span data-ttu-id="8cd31-103">Коллекция Партитионусерс</span><span class="sxs-lookup"><span data-stu-id="8cd31-103">PartitionUsers collection</span></span>

<span data-ttu-id="8cd31-104">Содержит объект для каждого пользователя секции.</span><span class="sxs-lookup"><span data-stu-id="8cd31-104">Contains an object for each partition user.</span></span>

<span data-ttu-id="8cd31-105">Эта коллекция поддерживает методы [**Add**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add) и [**Remove**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove) объекта [**комадминкаталогколлектион**](comadmincatalogcollection.md) .</span><span class="sxs-lookup"><span data-stu-id="8cd31-105">This collection supports the [**Add**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add) and [**Remove**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove) methods of the [**COMAdminCatalogCollection**](comadmincatalogcollection.md) object.</span></span>

## <a name="members"></a><span data-ttu-id="8cd31-106">Элементы</span><span class="sxs-lookup"><span data-stu-id="8cd31-106">Members</span></span>

<span data-ttu-id="8cd31-107">Коллекция **партитионусерс** наследует от интерфейса [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) , но не содержит дополнительных элементов.</span><span class="sxs-lookup"><span data-stu-id="8cd31-107">The **PartitionUsers** collection inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface but does not have additional members.</span></span>

## <a name="related-collections"></a><span data-ttu-id="8cd31-108">Связанные коллекции</span><span class="sxs-lookup"><span data-stu-id="8cd31-108">Related Collections</span></span>

<span data-ttu-id="8cd31-109">Можно переходить от этой коллекции к любой из следующих коллекций:</span><span class="sxs-lookup"><span data-stu-id="8cd31-109">You can navigate from this collection to any of the following collections:</span></span>

-   [<span data-ttu-id="8cd31-110">**ErrorInfo**</span><span class="sxs-lookup"><span data-stu-id="8cd31-110">**ErrorInfo**</span></span>](errorinfo.md)
-   [<span data-ttu-id="8cd31-111">**PropertyInfo**</span><span class="sxs-lookup"><span data-stu-id="8cd31-111">**PropertyInfo**</span></span>](propertyinfo.md)
-   [<span data-ttu-id="8cd31-112">**релатедколлектионинфо**</span><span class="sxs-lookup"><span data-stu-id="8cd31-112">**RelatedCollectionInfo**</span></span>](relatedcollectioninfo.md)

<span data-ttu-id="8cd31-113">Вы можете переходить к этой коллекции из следующих коллекций:</span><span class="sxs-lookup"><span data-stu-id="8cd31-113">You can navigate to this collection from the following collections:</span></span>

-   [<span data-ttu-id="8cd31-114">**Корневой**</span><span class="sxs-lookup"><span data-stu-id="8cd31-114">**Root**</span></span>](root.md)

## <a name="properties"></a><span data-ttu-id="8cd31-115">Свойства</span><span class="sxs-lookup"><span data-stu-id="8cd31-115">Properties</span></span>

<span data-ttu-id="8cd31-116">Объект [**комадминкаталогобжект**](comadmincatalogobject.md) в коллекции поддерживает следующие свойства:</span><span class="sxs-lookup"><span data-stu-id="8cd31-116">The following properties are supported by the [**COMAdminCatalogObject**](comadmincatalogobject.md) object within the collection:</span></span>

-   [<span data-ttu-id="8cd31-117">AccountName</span><span class="sxs-lookup"><span data-stu-id="8cd31-117">AccountName</span></span>](#accountname)
-   [<span data-ttu-id="8cd31-118">дефаултпартитионид</span><span class="sxs-lookup"><span data-stu-id="8cd31-118">DefaultPartitionID</span></span>](#defaultpartitionid)

### <a name="accountname"></a><span data-ttu-id="8cd31-119">AccountName</span><span class="sxs-lookup"><span data-stu-id="8cd31-119">AccountName</span></span>



| <span data-ttu-id="8cd31-120">Ввод</span><span class="sxs-lookup"><span data-stu-id="8cd31-120">Entry</span></span> | <span data-ttu-id="8cd31-121">Значение</span><span class="sxs-lookup"><span data-stu-id="8cd31-121">Value</span></span> |
|----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8cd31-122">Описание</span><span class="sxs-lookup"><span data-stu-id="8cd31-122">Description</span></span>    | <span data-ttu-id="8cd31-123">Имя учетной записи пользователя раздела.</span><span class="sxs-lookup"><span data-stu-id="8cd31-123">Name of the partition user's account.</span></span> <span data-ttu-id="8cd31-124">Это свойство возвращается при вызове метода свойства [**Key**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) или [**Name**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_name) для объекта этой коллекции.</span><span class="sxs-lookup"><span data-stu-id="8cd31-124">This property is returned when the [**Key**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) or [**Name**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_name) property method is called on an object of this collection.</span></span> |
| <span data-ttu-id="8cd31-125">Access</span><span class="sxs-lookup"><span data-stu-id="8cd31-125">Access</span></span>         | <span data-ttu-id="8cd31-126">Флагом writeonce</span><span class="sxs-lookup"><span data-stu-id="8cd31-126">WriteOnce</span></span>                                                                                                                                                                                                    |
| <span data-ttu-id="8cd31-127">Тип</span><span class="sxs-lookup"><span data-stu-id="8cd31-127">Type</span></span>           | <span data-ttu-id="8cd31-128">Строка</span><span class="sxs-lookup"><span data-stu-id="8cd31-128">String</span></span>                                                                                                                                                                                                       |
| <span data-ttu-id="8cd31-129">По умолчанию</span><span class="sxs-lookup"><span data-stu-id="8cd31-129">Default</span></span>        | <span data-ttu-id="8cd31-130">"Новый пользователь"</span><span class="sxs-lookup"><span data-stu-id="8cd31-130">"New User"</span></span>                                                                                                                                                                                                   |
| <span data-ttu-id="8cd31-131">Минимальная система</span><span class="sxs-lookup"><span data-stu-id="8cd31-131">Minimum system</span></span> | <span data-ttu-id="8cd31-132">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="8cd31-132">Windows Server 2003</span></span>                                                                                                                                                                                          |



 

### <a name="defaultpartitionid"></a><span data-ttu-id="8cd31-133">дефаултпартитионид</span><span class="sxs-lookup"><span data-stu-id="8cd31-133">DefaultPartitionID</span></span>



| <span data-ttu-id="8cd31-134">Ввод</span><span class="sxs-lookup"><span data-stu-id="8cd31-134">Entry</span></span> | <span data-ttu-id="8cd31-135">Значение</span><span class="sxs-lookup"><span data-stu-id="8cd31-135">Value</span></span> |
|----------------|--------------------------------------------------------------------|
| <span data-ttu-id="8cd31-136">Описание</span><span class="sxs-lookup"><span data-stu-id="8cd31-136">Description</span></span>    | <span data-ttu-id="8cd31-137">Глобальный уникальный идентификатор базового раздела приложения.</span><span class="sxs-lookup"><span data-stu-id="8cd31-137">The globally unique identifier for the base application partition.</span></span> |
| <span data-ttu-id="8cd31-138">Access</span><span class="sxs-lookup"><span data-stu-id="8cd31-138">Access</span></span>         | <span data-ttu-id="8cd31-139">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="8cd31-139">ReadWrite</span></span>                                                          |
| <span data-ttu-id="8cd31-140">Тип</span><span class="sxs-lookup"><span data-stu-id="8cd31-140">Type</span></span>           | <span data-ttu-id="8cd31-141">Строка</span><span class="sxs-lookup"><span data-stu-id="8cd31-141">String</span></span>                                                             |
| <span data-ttu-id="8cd31-142">По умолчанию</span><span class="sxs-lookup"><span data-stu-id="8cd31-142">Default</span></span>        | <span data-ttu-id="8cd31-143">{41E90F3E-56C1-4633-81C3-6E8BAC8BDD70}</span><span class="sxs-lookup"><span data-stu-id="8cd31-143">{41E90F3E-56C1-4633-81C3-6E8BAC8BDD70}</span></span>                             |
| <span data-ttu-id="8cd31-144">Минимальная система</span><span class="sxs-lookup"><span data-stu-id="8cd31-144">Minimum system</span></span> | <span data-ttu-id="8cd31-145">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="8cd31-145">Windows Server 2003</span></span>                                                |



 

## <a name="see-also"></a><span data-ttu-id="8cd31-146">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="8cd31-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8cd31-147">Коллекции администрирования COM+</span><span class="sxs-lookup"><span data-stu-id="8cd31-147">COM+ Administration Collections</span></span>](com--administration-collections.md)
</dt> </dl>

 

 
