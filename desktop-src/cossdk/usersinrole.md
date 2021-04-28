---
description: Коллекция Усерсинроле — содержит объект для каждого пользователя в роли, к которой относится коллекция.
ms.assetid: e7d9e5e8-1927-42b2-bdd5-0c49a562c31f
title: Коллекция Усерсинроле
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- UsersInRole
api_type:
- COM
api_location: ''
ms.openlocfilehash: 1b73c495a1af1dec9114e5a59274e457c1d09694
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108105542"
---
# <a name="usersinrole-collection"></a><span data-ttu-id="786c0-103">Коллекция Усерсинроле</span><span class="sxs-lookup"><span data-stu-id="786c0-103">UsersInRole collection</span></span>

<span data-ttu-id="786c0-104">Содержит объект для каждого пользователя в роли, к которой относится коллекция.</span><span class="sxs-lookup"><span data-stu-id="786c0-104">Contains an object for each user in the role to which the collection is related.</span></span>

<span data-ttu-id="786c0-105">Эта коллекция поддерживает методы [**Add**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add) и [**Remove**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove) объекта [**комадминкаталогколлектион**](comadmincatalogcollection.md) .</span><span class="sxs-lookup"><span data-stu-id="786c0-105">This collection supports the [**Add**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add) and [**Remove**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove) methods of the [**COMAdminCatalogCollection**](comadmincatalogcollection.md) object.</span></span>

## <a name="members"></a><span data-ttu-id="786c0-106">Элементы</span><span class="sxs-lookup"><span data-stu-id="786c0-106">Members</span></span>

<span data-ttu-id="786c0-107">Коллекция **усерсинроле** наследует от интерфейса [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) , но не содержит дополнительных элементов.</span><span class="sxs-lookup"><span data-stu-id="786c0-107">The **UsersInRole** collection inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface but does not have additional members.</span></span>

## <a name="related-collections"></a><span data-ttu-id="786c0-108">Связанные коллекции</span><span class="sxs-lookup"><span data-stu-id="786c0-108">Related Collections</span></span>

<span data-ttu-id="786c0-109">Можно переходить от этой коллекции к любой из следующих коллекций:</span><span class="sxs-lookup"><span data-stu-id="786c0-109">You can navigate from this collection to any of the following collections:</span></span>

-   [<span data-ttu-id="786c0-110">**ErrorInfo**</span><span class="sxs-lookup"><span data-stu-id="786c0-110">**ErrorInfo**</span></span>](errorinfo.md)
-   [<span data-ttu-id="786c0-111">**PropertyInfo**</span><span class="sxs-lookup"><span data-stu-id="786c0-111">**PropertyInfo**</span></span>](propertyinfo.md)
-   [<span data-ttu-id="786c0-112">**релатедколлектионинфо**</span><span class="sxs-lookup"><span data-stu-id="786c0-112">**RelatedCollectionInfo**</span></span>](relatedcollectioninfo.md)

<span data-ttu-id="786c0-113">Вы можете переходить к этой коллекции из следующих коллекций:</span><span class="sxs-lookup"><span data-stu-id="786c0-113">You can navigate to this collection from the following collections:</span></span>

-   [<span data-ttu-id="786c0-114">**Роли**</span><span class="sxs-lookup"><span data-stu-id="786c0-114">**Roles**</span></span>](roles.md)

## <a name="properties"></a><span data-ttu-id="786c0-115">Свойства</span><span class="sxs-lookup"><span data-stu-id="786c0-115">Properties</span></span>

<span data-ttu-id="786c0-116">Объект [**комадминкаталогобжект**](comadmincatalogobject.md) в коллекции поддерживает следующие свойства:</span><span class="sxs-lookup"><span data-stu-id="786c0-116">The following properties are supported by the [**COMAdminCatalogObject**](comadmincatalogobject.md) object within the collection:</span></span>

-   [<span data-ttu-id="786c0-117">Пользователь</span><span class="sxs-lookup"><span data-stu-id="786c0-117">User</span></span>](#usersinrole-collection)

### <a name="user"></a><span data-ttu-id="786c0-118">Пользователь</span><span class="sxs-lookup"><span data-stu-id="786c0-118">User</span></span>



| <span data-ttu-id="786c0-119">Ввод</span><span class="sxs-lookup"><span data-stu-id="786c0-119">Entry</span></span> | <span data-ttu-id="786c0-120">Значение</span><span class="sxs-lookup"><span data-stu-id="786c0-120">Value</span></span> |
|----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="786c0-121">Описание</span><span class="sxs-lookup"><span data-stu-id="786c0-121">Description</span></span>    | <span data-ttu-id="786c0-122">Имя пользователя.</span><span class="sxs-lookup"><span data-stu-id="786c0-122">The user name.</span></span> <span data-ttu-id="786c0-123">Это свойство возвращается при вызове метода свойства [**Key**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) или [**Name**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_name) для объекта этой коллекции.</span><span class="sxs-lookup"><span data-stu-id="786c0-123">This property is returned when the [**Key**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) or [**Name**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_name) property method is called on an object of this collection.</span></span> |
| <span data-ttu-id="786c0-124">Access</span><span class="sxs-lookup"><span data-stu-id="786c0-124">Access</span></span>         | <span data-ttu-id="786c0-125">Флагом writeonce</span><span class="sxs-lookup"><span data-stu-id="786c0-125">WriteOnce</span></span>                                                                                                                                                                             |
| <span data-ttu-id="786c0-126">Тип</span><span class="sxs-lookup"><span data-stu-id="786c0-126">Type</span></span>           | <span data-ttu-id="786c0-127">Строка</span><span class="sxs-lookup"><span data-stu-id="786c0-127">String</span></span>                                                                                                                                                                                |
| <span data-ttu-id="786c0-128">По умолчанию</span><span class="sxs-lookup"><span data-stu-id="786c0-128">Default</span></span>        | <span data-ttu-id="786c0-129">"Новый пользователь"</span><span class="sxs-lookup"><span data-stu-id="786c0-129">"New User"</span></span>                                                                                                                                                                            |
| <span data-ttu-id="786c0-130">Минимальная система</span><span class="sxs-lookup"><span data-stu-id="786c0-130">Minimum system</span></span> | <span data-ttu-id="786c0-131">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="786c0-131">Windows 2000</span></span>                                                                                                                                                                          |



 

## <a name="see-also"></a><span data-ttu-id="786c0-132">См. также</span><span class="sxs-lookup"><span data-stu-id="786c0-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="786c0-133">Коллекции администрирования COM+</span><span class="sxs-lookup"><span data-stu-id="786c0-133">COM+ Administration Collections</span></span>](com--administration-collections.md)
</dt> </dl>

 

 
