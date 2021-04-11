---
description: Коллекция Roles всегда связана с объектом в коллекции приложений. Он содержит объект для каждой роли, назначенной приложению, к которому он относится.
ms.assetid: 87f39c2a-ad66-4390-9220-06751dcebd95
title: Коллекция ролей
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Roles
api_type:
- COM
api_location: ''
ms.openlocfilehash: f676a53f5fe54e42ca2a489ad834b9c91e4e0ef5
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104262741"
---
# <a name="roles-collection"></a><span data-ttu-id="74c27-104">Коллекция ролей</span><span class="sxs-lookup"><span data-stu-id="74c27-104">Roles collection</span></span>

<span data-ttu-id="74c27-105">Коллекция **roles** всегда связана с объектом в коллекции [**приложений**](applications.md) .</span><span class="sxs-lookup"><span data-stu-id="74c27-105">The **Roles** collection is always related to an object in the [**Applications**](applications.md) collection.</span></span> <span data-ttu-id="74c27-106">Он содержит объект для каждой роли, назначенной приложению, к которому он относится.</span><span class="sxs-lookup"><span data-stu-id="74c27-106">It holds an object for each role assigned to the application to which it is related.</span></span>

<span data-ttu-id="74c27-107">Эта коллекция поддерживает методы [**Add**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add) и [**Remove**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove) объекта [**комадминкаталогколлектион**](comadmincatalogcollection.md) .</span><span class="sxs-lookup"><span data-stu-id="74c27-107">This collection supports the [**Add**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add) and [**Remove**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove) methods of the [**COMAdminCatalogCollection**](comadmincatalogcollection.md) object.</span></span>

## <a name="members"></a><span data-ttu-id="74c27-108">Элементы</span><span class="sxs-lookup"><span data-stu-id="74c27-108">Members</span></span>

<span data-ttu-id="74c27-109">Коллекция **ролей** наследует от интерфейса [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) , но не содержит дополнительных элементов.</span><span class="sxs-lookup"><span data-stu-id="74c27-109">The **Roles** collection inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface but does not have additional members.</span></span>

## <a name="related-collections"></a><span data-ttu-id="74c27-110">Связанные коллекции</span><span class="sxs-lookup"><span data-stu-id="74c27-110">Related Collections</span></span>

<span data-ttu-id="74c27-111">Можно переходить от этой коллекции к любой из следующих коллекций:</span><span class="sxs-lookup"><span data-stu-id="74c27-111">You can navigate from this collection to any of the following collections:</span></span>

-   [<span data-ttu-id="74c27-112">**ErrorInfo**</span><span class="sxs-lookup"><span data-stu-id="74c27-112">**ErrorInfo**</span></span>](errorinfo.md)
-   [<span data-ttu-id="74c27-113">**PropertyInfo**</span><span class="sxs-lookup"><span data-stu-id="74c27-113">**PropertyInfo**</span></span>](propertyinfo.md)
-   [<span data-ttu-id="74c27-114">**релатедколлектионинфо**</span><span class="sxs-lookup"><span data-stu-id="74c27-114">**RelatedCollectionInfo**</span></span>](relatedcollectioninfo.md)
-   [<span data-ttu-id="74c27-115">**усерсинроле**</span><span class="sxs-lookup"><span data-stu-id="74c27-115">**UsersInRole**</span></span>](usersinrole.md)

<span data-ttu-id="74c27-116">Вы можете переходить к этой коллекции из следующих коллекций:</span><span class="sxs-lookup"><span data-stu-id="74c27-116">You can navigate to this collection from the following collections:</span></span>

-   [<span data-ttu-id="74c27-117">**Приложения**</span><span class="sxs-lookup"><span data-stu-id="74c27-117">**Applications**</span></span>](applications.md)

## <a name="properties"></a><span data-ttu-id="74c27-118">Свойства</span><span class="sxs-lookup"><span data-stu-id="74c27-118">Properties</span></span>

<span data-ttu-id="74c27-119">Объект [**комадминкаталогобжект**](comadmincatalogobject.md) в коллекции поддерживает следующие свойства:</span><span class="sxs-lookup"><span data-stu-id="74c27-119">The following properties are supported by the [**COMAdminCatalogObject**](comadmincatalogobject.md) object within the collection:</span></span>

-   [<span data-ttu-id="74c27-120">Описание</span><span class="sxs-lookup"><span data-stu-id="74c27-120">Description</span></span>](#description)
-   [<span data-ttu-id="74c27-121">Имя</span><span class="sxs-lookup"><span data-stu-id="74c27-121">Name</span></span>](#name)

### <a name="description"></a><span data-ttu-id="74c27-122">Описание</span><span class="sxs-lookup"><span data-stu-id="74c27-122">Description</span></span>



| <span data-ttu-id="74c27-123">Ввод</span><span class="sxs-lookup"><span data-stu-id="74c27-123">Entry</span></span> | <span data-ttu-id="74c27-124">Значение</span><span class="sxs-lookup"><span data-stu-id="74c27-124">Value</span></span> |
|----------------|----------------------------|
| <span data-ttu-id="74c27-125">Описание</span><span class="sxs-lookup"><span data-stu-id="74c27-125">Description</span></span>    | <span data-ttu-id="74c27-126">Описание роли.</span><span class="sxs-lookup"><span data-stu-id="74c27-126">A description of the role.</span></span> |
| <span data-ttu-id="74c27-127">Access</span><span class="sxs-lookup"><span data-stu-id="74c27-127">Access</span></span>         | <span data-ttu-id="74c27-128">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="74c27-128">ReadWrite</span></span>                  |
| <span data-ttu-id="74c27-129">Тип</span><span class="sxs-lookup"><span data-stu-id="74c27-129">Type</span></span>           | <span data-ttu-id="74c27-130">Строка</span><span class="sxs-lookup"><span data-stu-id="74c27-130">String</span></span>                     |
| <span data-ttu-id="74c27-131">По умолчанию</span><span class="sxs-lookup"><span data-stu-id="74c27-131">Default</span></span>        | <span data-ttu-id="74c27-132">""</span><span class="sxs-lookup"><span data-stu-id="74c27-132">""</span></span>                         |
| <span data-ttu-id="74c27-133">Минимальная система</span><span class="sxs-lookup"><span data-stu-id="74c27-133">Minimum system</span></span> | <span data-ttu-id="74c27-134">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="74c27-134">Windows 2000</span></span>               |



 

### <a name="name"></a><span data-ttu-id="74c27-135">Имя</span><span class="sxs-lookup"><span data-stu-id="74c27-135">Name</span></span>



| <span data-ttu-id="74c27-136">Ввод</span><span class="sxs-lookup"><span data-stu-id="74c27-136">Entry</span></span> | <span data-ttu-id="74c27-137">Значение</span><span class="sxs-lookup"><span data-stu-id="74c27-137">Value</span></span> |
|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="74c27-138">Описание</span><span class="sxs-lookup"><span data-stu-id="74c27-138">Description</span></span>    | <span data-ttu-id="74c27-139">Имя роли.</span><span class="sxs-lookup"><span data-stu-id="74c27-139">The role name.</span></span> <span data-ttu-id="74c27-140">Лишние пробелы в начале и конце строки удаляются. Это свойство возвращается при вызове метода свойства [**Key**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) или [**Name**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_name) для объекта этой коллекции.</span><span class="sxs-lookup"><span data-stu-id="74c27-140">Extra spaces at the beginning and end of the string are stripped out. This property is returned when the [**Key**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) or [**Name**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_name) property method is called on an object of this collection.</span></span> |
| <span data-ttu-id="74c27-141">Access</span><span class="sxs-lookup"><span data-stu-id="74c27-141">Access</span></span>         | <span data-ttu-id="74c27-142">Флагом writeonce</span><span class="sxs-lookup"><span data-stu-id="74c27-142">WriteOnce</span></span>                                                                                                                                                                                                                                                   |
| <span data-ttu-id="74c27-143">Тип</span><span class="sxs-lookup"><span data-stu-id="74c27-143">Type</span></span>           | <span data-ttu-id="74c27-144">Строка</span><span class="sxs-lookup"><span data-stu-id="74c27-144">String</span></span>                                                                                                                                                                                                                                                      |
| <span data-ttu-id="74c27-145">По умолчанию</span><span class="sxs-lookup"><span data-stu-id="74c27-145">Default</span></span>        | <span data-ttu-id="74c27-146">"Создать роль"</span><span class="sxs-lookup"><span data-stu-id="74c27-146">"New Role"</span></span>                                                                                                                                                                                                                                                  |
| <span data-ttu-id="74c27-147">Минимальная система</span><span class="sxs-lookup"><span data-stu-id="74c27-147">Minimum system</span></span> | <span data-ttu-id="74c27-148">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="74c27-148">Windows 2000</span></span>                                                                                                                                                                                                                                                |



 

## <a name="see-also"></a><span data-ttu-id="74c27-149">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="74c27-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="74c27-150">Коллекции администрирования COM+</span><span class="sxs-lookup"><span data-stu-id="74c27-150">COM+ Administration Collections</span></span>](com--administration-collections.md)
</dt> </dl>

 

 
