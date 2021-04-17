---
description: Содержит объект для каждой роли, назначенной методу, к которому относится коллекция. Роли уже должны быть назначены на уровне приложения.
ms.assetid: 3a086163-e367-4dd1-996b-821b3e1111b2
title: Коллекция Ролесформесод
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- RolesForMethod
api_type:
- COM
api_location: ''
ms.openlocfilehash: c73ba5f7a14a5efc6711a65f211cd036e1c2a14d
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105710744"
---
# <a name="rolesformethod-collection"></a><span data-ttu-id="dc247-104">Коллекция Ролесформесод</span><span class="sxs-lookup"><span data-stu-id="dc247-104">RolesForMethod collection</span></span>

<span data-ttu-id="dc247-105">Содержит объект для каждой роли, назначенной методу, к которому относится коллекция.</span><span class="sxs-lookup"><span data-stu-id="dc247-105">Contains an object for each role assigned to the method to which the collection is related.</span></span> <span data-ttu-id="dc247-106">Роли уже должны быть назначены на уровне приложения.</span><span class="sxs-lookup"><span data-stu-id="dc247-106">The roles must already be assigned at the application level.</span></span>

<span data-ttu-id="dc247-107">Эта коллекция поддерживает методы [**Add**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add) и [**Remove**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove) объекта [**комадминкаталогколлектион**](comadmincatalogcollection.md) .</span><span class="sxs-lookup"><span data-stu-id="dc247-107">This collection supports the [**Add**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add) and [**Remove**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove) methods of the [**COMAdminCatalogCollection**](comadmincatalogcollection.md) object.</span></span>

## <a name="members"></a><span data-ttu-id="dc247-108">Элементы</span><span class="sxs-lookup"><span data-stu-id="dc247-108">Members</span></span>

<span data-ttu-id="dc247-109">Коллекция **ролесформесод** наследует от интерфейса [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) , но не содержит дополнительных элементов.</span><span class="sxs-lookup"><span data-stu-id="dc247-109">The **RolesForMethod** collection inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface but does not have additional members.</span></span>

## <a name="related-collections"></a><span data-ttu-id="dc247-110">Связанные коллекции</span><span class="sxs-lookup"><span data-stu-id="dc247-110">Related Collections</span></span>

<span data-ttu-id="dc247-111">Можно переходить от этой коллекции к любой из следующих коллекций:</span><span class="sxs-lookup"><span data-stu-id="dc247-111">You can navigate from this collection to any of the following collections:</span></span>

-   [<span data-ttu-id="dc247-112">**ErrorInfo**</span><span class="sxs-lookup"><span data-stu-id="dc247-112">**ErrorInfo**</span></span>](errorinfo.md)
-   [<span data-ttu-id="dc247-113">**PropertyInfo**</span><span class="sxs-lookup"><span data-stu-id="dc247-113">**PropertyInfo**</span></span>](propertyinfo.md)
-   [<span data-ttu-id="dc247-114">**релатедколлектионинфо**</span><span class="sxs-lookup"><span data-stu-id="dc247-114">**RelatedCollectionInfo**</span></span>](relatedcollectioninfo.md)

<span data-ttu-id="dc247-115">Вы можете переходить к этой коллекции из следующих коллекций:</span><span class="sxs-lookup"><span data-stu-id="dc247-115">You can navigate to this collection from the following collections:</span></span>

-   [<span data-ttu-id="dc247-116">**месодсфоринтерфаце**</span><span class="sxs-lookup"><span data-stu-id="dc247-116">**MethodsForInterface**</span></span>](methodsforinterface.md)

## <a name="properties"></a><span data-ttu-id="dc247-117">Свойства</span><span class="sxs-lookup"><span data-stu-id="dc247-117">Properties</span></span>

<span data-ttu-id="dc247-118">Объект [**комадминкаталогобжект**](comadmincatalogobject.md) в коллекции поддерживает следующие свойства:</span><span class="sxs-lookup"><span data-stu-id="dc247-118">The following properties are supported by the [**COMAdminCatalogObject**](comadmincatalogobject.md) object within the collection:</span></span>

-   [<span data-ttu-id="dc247-119">Name</span><span class="sxs-lookup"><span data-stu-id="dc247-119">Name</span></span>](#name)

### <a name="name"></a><span data-ttu-id="dc247-120">Имя</span><span class="sxs-lookup"><span data-stu-id="dc247-120">Name</span></span>



| <span data-ttu-id="dc247-121">Ввод</span><span class="sxs-lookup"><span data-stu-id="dc247-121">Entry</span></span> | <span data-ttu-id="dc247-122">Значение</span><span class="sxs-lookup"><span data-stu-id="dc247-122">Value</span></span> |
|----------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="dc247-123">Описание</span><span class="sxs-lookup"><span data-stu-id="dc247-123">Description</span></span>    | <span data-ttu-id="dc247-124">Имя роли.</span><span class="sxs-lookup"><span data-stu-id="dc247-124">The role name.</span></span> <span data-ttu-id="dc247-125">Уже должна быть назначена приложению роли (отображается в коллекции ролей).</span><span class="sxs-lookup"><span data-stu-id="dc247-125">Must already be a role assigned to the application (appearing in the Roles collection).</span></span> <span data-ttu-id="dc247-126">Лишние пробелы в начале и конце строки удаляются. Это свойство возвращается при вызове метода свойства [**Key**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) или [**Name**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_name) для объекта этой коллекции.</span><span class="sxs-lookup"><span data-stu-id="dc247-126">Extra spaces at the beginning and end of the string are stripped out. This property is returned when the [**Key**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) or [**Name**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_name) property method is called on an object of this collection.</span></span> |
| <span data-ttu-id="dc247-127">Access</span><span class="sxs-lookup"><span data-stu-id="dc247-127">Access</span></span>         | <span data-ttu-id="dc247-128">Флагом writeonce</span><span class="sxs-lookup"><span data-stu-id="dc247-128">WriteOnce</span></span>                                                                                                                                                                                                                                                                                                                                           |
| <span data-ttu-id="dc247-129">Тип</span><span class="sxs-lookup"><span data-stu-id="dc247-129">Type</span></span>           | <span data-ttu-id="dc247-130">Строка</span><span class="sxs-lookup"><span data-stu-id="dc247-130">String</span></span>                                                                                                                                                                                                                                                                                                                                              |
| <span data-ttu-id="dc247-131">По умолчанию</span><span class="sxs-lookup"><span data-stu-id="dc247-131">Default</span></span>        | <span data-ttu-id="dc247-132">"Создать роль"</span><span class="sxs-lookup"><span data-stu-id="dc247-132">"New Role"</span></span>                                                                                                                                                                                                                                                                                                                                          |
| <span data-ttu-id="dc247-133">Минимальная система</span><span class="sxs-lookup"><span data-stu-id="dc247-133">Minimum system</span></span> | <span data-ttu-id="dc247-134">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="dc247-134">Windows 2000</span></span>                                                                                                                                                                                                                                                                                                                                        |



 

## <a name="see-also"></a><span data-ttu-id="dc247-135">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="dc247-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dc247-136">Коллекции администрирования COM+</span><span class="sxs-lookup"><span data-stu-id="dc247-136">COM+ Administration Collections</span></span>](com--administration-collections.md)
</dt> </dl>

 

 
