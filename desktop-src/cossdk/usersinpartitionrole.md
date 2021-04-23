---
description: Содержит объект для каждого пользователя в роли, к которой относится коллекция.
ms.assetid: c6aebf7a-04d1-4c7c-a015-bc6fb4841c4a
title: Коллекция Усерсинпартитионроле
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- UsersInPartitionRole
api_type:
- COM
api_location: ''
ms.openlocfilehash: fce1577636a7b2e678bdade9c32f706c7ccbf158
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104141788"
---
# <a name="usersinpartitionrole-collection"></a><span data-ttu-id="65c89-103">Коллекция Усерсинпартитионроле</span><span class="sxs-lookup"><span data-stu-id="65c89-103">UsersInPartitionRole collection</span></span>

<span data-ttu-id="65c89-104">Содержит объект для каждого пользователя в роли, к которой относится коллекция.</span><span class="sxs-lookup"><span data-stu-id="65c89-104">Contains an object for each user in the role to which the collection is related.</span></span>

<span data-ttu-id="65c89-105">Эта коллекция поддерживает методы [**Add**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add) и [**Remove**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove) объекта [**комадминкаталогколлектион**](comadmincatalogcollection.md) .</span><span class="sxs-lookup"><span data-stu-id="65c89-105">This collection supports the [**Add**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add) and [**Remove**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove) methods of the [**COMAdminCatalogCollection**](comadmincatalogcollection.md) object.</span></span>

## <a name="members"></a><span data-ttu-id="65c89-106">Элементы</span><span class="sxs-lookup"><span data-stu-id="65c89-106">Members</span></span>

<span data-ttu-id="65c89-107">Коллекция **усерсинпартитионроле** наследует от интерфейса [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) , но не содержит дополнительных элементов.</span><span class="sxs-lookup"><span data-stu-id="65c89-107">The **UsersInPartitionRole** collection inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface but does not have additional members.</span></span>

## <a name="related-collections"></a><span data-ttu-id="65c89-108">Связанные коллекции</span><span class="sxs-lookup"><span data-stu-id="65c89-108">Related Collections</span></span>

<span data-ttu-id="65c89-109">Можно переходить от этой коллекции к любой из следующих коллекций:</span><span class="sxs-lookup"><span data-stu-id="65c89-109">You can navigate from this collection to any of the following collections:</span></span>

-   [<span data-ttu-id="65c89-110">**ErrorInfo**</span><span class="sxs-lookup"><span data-stu-id="65c89-110">**ErrorInfo**</span></span>](errorinfo.md)
-   [<span data-ttu-id="65c89-111">**PropertyInfo**</span><span class="sxs-lookup"><span data-stu-id="65c89-111">**PropertyInfo**</span></span>](propertyinfo.md)
-   [<span data-ttu-id="65c89-112">**релатедколлектионинфо**</span><span class="sxs-lookup"><span data-stu-id="65c89-112">**RelatedCollectionInfo**</span></span>](relatedcollectioninfo.md)

<span data-ttu-id="65c89-113">Вы можете переходить к этой коллекции из следующих коллекций:</span><span class="sxs-lookup"><span data-stu-id="65c89-113">You can navigate to this collection from the following collections:</span></span>

-   [<span data-ttu-id="65c89-114">**ролесфорпартитион**</span><span class="sxs-lookup"><span data-stu-id="65c89-114">**RolesForPartition**</span></span>](rolesforpartition.md)

## <a name="properties"></a><span data-ttu-id="65c89-115">Свойства</span><span class="sxs-lookup"><span data-stu-id="65c89-115">Properties</span></span>

<span data-ttu-id="65c89-116">Объект [**комадминкаталогобжект**](comadmincatalogobject.md) в коллекции поддерживает следующие свойства:</span><span class="sxs-lookup"><span data-stu-id="65c89-116">The following properties are supported by the [**COMAdminCatalogObject**](comadmincatalogobject.md) object within the collection:</span></span>

-   [<span data-ttu-id="65c89-117">Пользователь</span><span class="sxs-lookup"><span data-stu-id="65c89-117">User</span></span>](#usersinpartitionrole-collection)

### <a name="user"></a><span data-ttu-id="65c89-118">Пользователь</span><span class="sxs-lookup"><span data-stu-id="65c89-118">User</span></span>



| <span data-ttu-id="65c89-119">Ввод</span><span class="sxs-lookup"><span data-stu-id="65c89-119">Entry</span></span> | <span data-ttu-id="65c89-120">Значение</span><span class="sxs-lookup"><span data-stu-id="65c89-120">Value</span></span> |
|----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="65c89-121">Описание</span><span class="sxs-lookup"><span data-stu-id="65c89-121">Description</span></span>    | <span data-ttu-id="65c89-122">Имя пользователя.</span><span class="sxs-lookup"><span data-stu-id="65c89-122">The user name.</span></span> <span data-ttu-id="65c89-123">Это свойство возвращается при вызове метода свойства [**Key**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) или [**Name**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_name) для объекта этой коллекции.</span><span class="sxs-lookup"><span data-stu-id="65c89-123">This property is returned when the [**Key**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) or [**Name**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_name) property method is called on an object of this collection.</span></span> |
| <span data-ttu-id="65c89-124">Access</span><span class="sxs-lookup"><span data-stu-id="65c89-124">Access</span></span>         | <span data-ttu-id="65c89-125">Флагом writeonce</span><span class="sxs-lookup"><span data-stu-id="65c89-125">WriteOnce</span></span>                                                                                                                                                                             |
| <span data-ttu-id="65c89-126">Тип</span><span class="sxs-lookup"><span data-stu-id="65c89-126">Type</span></span>           | <span data-ttu-id="65c89-127">Строка</span><span class="sxs-lookup"><span data-stu-id="65c89-127">String</span></span>                                                                                                                                                                                |
| <span data-ttu-id="65c89-128">По умолчанию</span><span class="sxs-lookup"><span data-stu-id="65c89-128">Default</span></span>        | <span data-ttu-id="65c89-129">"Новый пользователь"</span><span class="sxs-lookup"><span data-stu-id="65c89-129">"New User"</span></span>                                                                                                                                                                            |
| <span data-ttu-id="65c89-130">Минимальная система</span><span class="sxs-lookup"><span data-stu-id="65c89-130">Minimum system</span></span> | <span data-ttu-id="65c89-131">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="65c89-131">Windows Server 2003</span></span>                                                                                                                                                                   |



 

## <a name="see-also"></a><span data-ttu-id="65c89-132">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="65c89-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="65c89-133">Коллекции администрирования COM+</span><span class="sxs-lookup"><span data-stu-id="65c89-133">COM+ Administration Collections</span></span>](com--administration-collections.md)
</dt> </dl>

 

 
