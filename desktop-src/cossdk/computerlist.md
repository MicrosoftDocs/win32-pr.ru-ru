---
description: Содержит список компьютеров в папке Computers средства администрирования служб компонентов. Он содержит объект для каждого компьютера.
ms.assetid: 56e32b47-a9f5-4888-b727-71ad0499da00
title: Коллекция Компутерлист
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ComputerList
api_type:
- COM
api_location: ''
ms.openlocfilehash: 379e5e07a86d06961de3f8f3936a260451bf43ae
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104496170"
---
# <a name="computerlist-collection"></a><span data-ttu-id="6d942-104">Коллекция Компутерлист</span><span class="sxs-lookup"><span data-stu-id="6d942-104">ComputerList collection</span></span>

<span data-ttu-id="6d942-105">Содержит список компьютеров в папке **Computers** средства администрирования служб компонентов.</span><span class="sxs-lookup"><span data-stu-id="6d942-105">Contains a list of the computers in the **Computers** folder of the Component Services administration tool.</span></span> <span data-ttu-id="6d942-106">Он содержит объект для каждого компьютера.</span><span class="sxs-lookup"><span data-stu-id="6d942-106">It contains an object for each computer.</span></span>

<span data-ttu-id="6d942-107">Эта коллекция поддерживает методы [**Add**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add) и [**Remove**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove) объекта [**комадминкаталогколлектион**](comadmincatalogcollection.md) .</span><span class="sxs-lookup"><span data-stu-id="6d942-107">This collection supports the [**Add**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add) and [**Remove**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove) methods of the [**COMAdminCatalogCollection**](comadmincatalogcollection.md) object.</span></span>

## <a name="members"></a><span data-ttu-id="6d942-108">Элементы</span><span class="sxs-lookup"><span data-stu-id="6d942-108">Members</span></span>

<span data-ttu-id="6d942-109">Коллекция **компутерлист** наследует от интерфейса [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) , но не содержит дополнительных элементов.</span><span class="sxs-lookup"><span data-stu-id="6d942-109">The **ComputerList** collection inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface but does not have additional members.</span></span>

## <a name="related-collections"></a><span data-ttu-id="6d942-110">Связанные коллекции</span><span class="sxs-lookup"><span data-stu-id="6d942-110">Related Collections</span></span>

<span data-ttu-id="6d942-111">Можно переходить от этой коллекции к любой из следующих коллекций:</span><span class="sxs-lookup"><span data-stu-id="6d942-111">You can navigate from this collection to any of the following collections:</span></span>

-   [<span data-ttu-id="6d942-112">**ErrorInfo**</span><span class="sxs-lookup"><span data-stu-id="6d942-112">**ErrorInfo**</span></span>](errorinfo.md)
-   [<span data-ttu-id="6d942-113">**PropertyInfo**</span><span class="sxs-lookup"><span data-stu-id="6d942-113">**PropertyInfo**</span></span>](propertyinfo.md)
-   [<span data-ttu-id="6d942-114">**релатедколлектионинфо**</span><span class="sxs-lookup"><span data-stu-id="6d942-114">**RelatedCollectionInfo**</span></span>](relatedcollectioninfo.md)

<span data-ttu-id="6d942-115">Вы можете переходить к этой коллекции из следующих коллекций:</span><span class="sxs-lookup"><span data-stu-id="6d942-115">You can navigate to this collection from the following collections:</span></span>

-   [<span data-ttu-id="6d942-116">**Корневой**</span><span class="sxs-lookup"><span data-stu-id="6d942-116">**Root**</span></span>](root.md)

## <a name="properties"></a><span data-ttu-id="6d942-117">Свойства</span><span class="sxs-lookup"><span data-stu-id="6d942-117">Properties</span></span>

<span data-ttu-id="6d942-118">Объект [**комадминкаталогобжект**](comadmincatalogobject.md) в коллекции поддерживает следующие свойства:</span><span class="sxs-lookup"><span data-stu-id="6d942-118">The following properties are supported by the [**COMAdminCatalogObject**](comadmincatalogobject.md) object within the collection:</span></span>

-   [<span data-ttu-id="6d942-119">Name</span><span class="sxs-lookup"><span data-stu-id="6d942-119">Name</span></span>](#name)

### <a name="name"></a><span data-ttu-id="6d942-120">Имя</span><span class="sxs-lookup"><span data-stu-id="6d942-120">Name</span></span>



| <span data-ttu-id="6d942-121">Ввод</span><span class="sxs-lookup"><span data-stu-id="6d942-121">Entry</span></span> | <span data-ttu-id="6d942-122">Значение</span><span class="sxs-lookup"><span data-stu-id="6d942-122">Value</span></span> |
|----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6d942-123">Описание</span><span class="sxs-lookup"><span data-stu-id="6d942-123">Description</span></span>    | <span data-ttu-id="6d942-124">Имя компьютера.</span><span class="sxs-lookup"><span data-stu-id="6d942-124">The name of the computer.</span></span> <span data-ttu-id="6d942-125">Лишние пробелы в начале и конце строки удаляются. Это свойство возвращается при вызове метода свойства [**Key**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) или [**Name**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_name) для объекта этой коллекции.</span><span class="sxs-lookup"><span data-stu-id="6d942-125">Extra spaces at the beginning and end of the string are stripped out. This property is returned when the [**Key**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) or [**Name**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_name) property method is called on an object of this collection.</span></span> |
| <span data-ttu-id="6d942-126">Access</span><span class="sxs-lookup"><span data-stu-id="6d942-126">Access</span></span>         | <span data-ttu-id="6d942-127">Флагом writeonce</span><span class="sxs-lookup"><span data-stu-id="6d942-127">WriteOnce</span></span>                                                                                                                                                                                                                                                              |
| <span data-ttu-id="6d942-128">Тип</span><span class="sxs-lookup"><span data-stu-id="6d942-128">Type</span></span>           | <span data-ttu-id="6d942-129">Строка</span><span class="sxs-lookup"><span data-stu-id="6d942-129">String</span></span>                                                                                                                                                                                                                                                                 |
| <span data-ttu-id="6d942-130">По умолчанию</span><span class="sxs-lookup"><span data-stu-id="6d942-130">Default</span></span>        | <span data-ttu-id="6d942-131">"Новый компьютер"</span><span class="sxs-lookup"><span data-stu-id="6d942-131">"New Computer"</span></span>                                                                                                                                                                                                                                                         |
| <span data-ttu-id="6d942-132">Минимальная система</span><span class="sxs-lookup"><span data-stu-id="6d942-132">Minimum system</span></span> | <span data-ttu-id="6d942-133">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="6d942-133">Windows 2000</span></span>                                                                                                                                                                                                                                                           |



 

## <a name="see-also"></a><span data-ttu-id="6d942-134">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="6d942-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6d942-135">Коллекции администрирования COM+</span><span class="sxs-lookup"><span data-stu-id="6d942-135">COM+ Administration Collections</span></span>](com--administration-collections.md)
</dt> </dl>

 

 
