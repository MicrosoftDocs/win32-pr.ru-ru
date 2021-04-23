---
description: Содержит объект для каждой роли, назначенной компоненту, к которому относится коллекция. Роли уже должны быть назначены на уровне приложения.
ms.assetid: c253c72f-908e-4990-ac1a-27e32c99283c
title: Коллекция Ролесфоркомпонент
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- RolesForComponent
api_type:
- COM
api_location: ''
ms.openlocfilehash: 701921f8f88656753857707c045da0c8e231e1a0
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105710736"
---
# <a name="rolesforcomponent-collection"></a><span data-ttu-id="6059d-104">Коллекция Ролесфоркомпонент</span><span class="sxs-lookup"><span data-stu-id="6059d-104">RolesForComponent collection</span></span>

<span data-ttu-id="6059d-105">Содержит объект для каждой роли, назначенной компоненту, к которому относится коллекция.</span><span class="sxs-lookup"><span data-stu-id="6059d-105">Contains an object for each role assigned to the component to which the collection is related.</span></span> <span data-ttu-id="6059d-106">Роли уже должны быть назначены на уровне приложения.</span><span class="sxs-lookup"><span data-stu-id="6059d-106">The roles must already be assigned at the application level.</span></span>

<span data-ttu-id="6059d-107">Эта коллекция поддерживает методы [**Add**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add) и [**Remove**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove) объекта [**комадминкаталогколлектион**](comadmincatalogcollection.md) .</span><span class="sxs-lookup"><span data-stu-id="6059d-107">This collection supports the [**Add**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add) and [**Remove**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove) methods of the [**COMAdminCatalogCollection**](comadmincatalogcollection.md) object.</span></span>

## <a name="members"></a><span data-ttu-id="6059d-108">Элементы</span><span class="sxs-lookup"><span data-stu-id="6059d-108">Members</span></span>

<span data-ttu-id="6059d-109">Коллекция **ролесфоркомпонент** наследует от интерфейса [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) , но не содержит дополнительных элементов.</span><span class="sxs-lookup"><span data-stu-id="6059d-109">The **RolesForComponent** collection inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface but does not have additional members.</span></span>

## <a name="related-collections"></a><span data-ttu-id="6059d-110">Связанные коллекции</span><span class="sxs-lookup"><span data-stu-id="6059d-110">Related Collections</span></span>

<span data-ttu-id="6059d-111">Можно переходить от этой коллекции к любой из следующих коллекций:</span><span class="sxs-lookup"><span data-stu-id="6059d-111">You can navigate from this collection to any of the following collections:</span></span>

-   [<span data-ttu-id="6059d-112">**ErrorInfo**</span><span class="sxs-lookup"><span data-stu-id="6059d-112">**ErrorInfo**</span></span>](errorinfo.md)
-   [<span data-ttu-id="6059d-113">**PropertyInfo**</span><span class="sxs-lookup"><span data-stu-id="6059d-113">**PropertyInfo**</span></span>](propertyinfo.md)
-   [<span data-ttu-id="6059d-114">**релатедколлектионинфо**</span><span class="sxs-lookup"><span data-stu-id="6059d-114">**RelatedCollectionInfo**</span></span>](relatedcollectioninfo.md)

<span data-ttu-id="6059d-115">Вы можете переходить к этой коллекции из следующих коллекций:</span><span class="sxs-lookup"><span data-stu-id="6059d-115">You can navigate to this collection from the following collections:</span></span>

-   [<span data-ttu-id="6059d-116">**Компоненты**</span><span class="sxs-lookup"><span data-stu-id="6059d-116">**Components**</span></span>](components.md)

## <a name="properties"></a><span data-ttu-id="6059d-117">Свойства</span><span class="sxs-lookup"><span data-stu-id="6059d-117">Properties</span></span>

<span data-ttu-id="6059d-118">Объект [**комадминкаталогобжект**](comadmincatalogobject.md) в коллекции поддерживает следующие свойства:</span><span class="sxs-lookup"><span data-stu-id="6059d-118">The following properties are supported by the [**COMAdminCatalogObject**](comadmincatalogobject.md) object within the collection:</span></span>

-   [<span data-ttu-id="6059d-119">Name</span><span class="sxs-lookup"><span data-stu-id="6059d-119">Name</span></span>](#name)

### <a name="name"></a><span data-ttu-id="6059d-120">Имя</span><span class="sxs-lookup"><span data-stu-id="6059d-120">Name</span></span>



| <span data-ttu-id="6059d-121">Ввод</span><span class="sxs-lookup"><span data-stu-id="6059d-121">Entry</span></span> | <span data-ttu-id="6059d-122">Значение</span><span class="sxs-lookup"><span data-stu-id="6059d-122">Value</span></span> |
|----------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6059d-123">Описание</span><span class="sxs-lookup"><span data-stu-id="6059d-123">Description</span></span>    | <span data-ttu-id="6059d-124">Имя роли.</span><span class="sxs-lookup"><span data-stu-id="6059d-124">The role name.</span></span> <span data-ttu-id="6059d-125">Уже должна быть назначена приложению роли (отображается в коллекции ролей).</span><span class="sxs-lookup"><span data-stu-id="6059d-125">Must already be a role assigned to the application (appearing in the Roles collection).</span></span> <span data-ttu-id="6059d-126">Лишние пробелы в начале и конце строки удаляются. Это свойство возвращается при вызове метода свойства [**Key**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) или [**Name**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_name) для объекта этой коллекции.</span><span class="sxs-lookup"><span data-stu-id="6059d-126">Extra spaces at the beginning and end of the string are stripped out. This property is returned when the [**Key**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) or [**Name**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_name) property method is called on an object of this collection.</span></span> |
| <span data-ttu-id="6059d-127">Access</span><span class="sxs-lookup"><span data-stu-id="6059d-127">Access</span></span>         | <span data-ttu-id="6059d-128">Флагом writeonce</span><span class="sxs-lookup"><span data-stu-id="6059d-128">WriteOnce</span></span>                                                                                                                                                                                                                                                                                                                                           |
| <span data-ttu-id="6059d-129">Тип</span><span class="sxs-lookup"><span data-stu-id="6059d-129">Type</span></span>           | <span data-ttu-id="6059d-130">Строка</span><span class="sxs-lookup"><span data-stu-id="6059d-130">String</span></span>                                                                                                                                                                                                                                                                                                                                              |
| <span data-ttu-id="6059d-131">По умолчанию</span><span class="sxs-lookup"><span data-stu-id="6059d-131">Default</span></span>        | <span data-ttu-id="6059d-132">"Создать роль"</span><span class="sxs-lookup"><span data-stu-id="6059d-132">"New Role"</span></span>                                                                                                                                                                                                                                                                                                                                          |
| <span data-ttu-id="6059d-133">Минимальная система</span><span class="sxs-lookup"><span data-stu-id="6059d-133">Minimum system</span></span> | <span data-ttu-id="6059d-134">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="6059d-134">Windows 2000</span></span>                                                                                                                                                                                                                                                                                                                                        |



 

## <a name="see-also"></a><span data-ttu-id="6059d-135">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="6059d-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6059d-136">Коллекции администрирования COM+</span><span class="sxs-lookup"><span data-stu-id="6059d-136">COM+ Administration Collections</span></span>](com--administration-collections.md)
</dt> </dl>

 

 
