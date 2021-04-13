---
title: Интерфейс Ипропертифилтерколлектион (Вдсшаредидл. h)
description: Обеспечивает доступ к свойствам возвращенной коллекции на основе отправленного запроса.
ms.assetid: 9ed4217f-54b0-4d69-bf44-2547320a9681
keywords:
- Устаревшие функции среды Windows интерфейса Ипропертифилтерколлектион
- Интерфейс Ипропертифилтерколлектион устаревшие функции среды Windows, описание
topic_type:
- apiref
api_name:
- IPropertyFilterCollection
api_location:
- WdsSharedIDL.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9be9fe01bacf24c852b49538beae16b4ecbc97b1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104340855"
---
# <a name="ipropertyfiltercollection-interface"></a><span data-ttu-id="dedb1-105">Интерфейс Ипропертифилтерколлектион</span><span class="sxs-lookup"><span data-stu-id="dedb1-105">IPropertyFilterCollection interface</span></span>

> [!NOTE]
> <span data-ttu-id="dedb1-106">Windows Desktop Search 2. x — это устаревшая технология, которая изначально была доступна в качестве надстройки для Windows XP и Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="dedb1-106">Windows Desktop Search 2.x is an obsolete technology that was originally available as an add-in for Windows XP and Windows Server 2003.</span></span> <span data-ttu-id="dedb1-107">В более поздних выпусках используйте [API поиска Windows](../search/-search-reference-entry-page.md) .</span><span class="sxs-lookup"><span data-stu-id="dedb1-107">On later releases, use the [Windows Search API](../search/-search-reference-entry-page.md) instead.</span></span> 

<span data-ttu-id="dedb1-108">Обеспечивает доступ к свойствам возвращенной коллекции на основе отправленного запроса.</span><span class="sxs-lookup"><span data-stu-id="dedb1-108">Exposes properties of the returned collection based on the query submitted.</span></span>

## <a name="members"></a><span data-ttu-id="dedb1-109">Элементы</span><span class="sxs-lookup"><span data-stu-id="dedb1-109">Members</span></span>

<span data-ttu-id="dedb1-110">Интерфейс **ипропертифилтерколлектион** наследует от интерфейса [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="dedb1-110">The **IPropertyFilterCollection** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="dedb1-111">**Ипропертифилтерколлектион** также имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="dedb1-111">**IPropertyFilterCollection** also has these types of members:</span></span>

-   [<span data-ttu-id="dedb1-112">Свойства</span><span class="sxs-lookup"><span data-stu-id="dedb1-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="dedb1-113">Свойства</span><span class="sxs-lookup"><span data-stu-id="dedb1-113">Properties</span></span>

<span data-ttu-id="dedb1-114">Интерфейс **ипропертифилтерколлектион** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="dedb1-114">The **IPropertyFilterCollection** interface has these properties.</span></span>



| <span data-ttu-id="dedb1-115">Свойство</span><span class="sxs-lookup"><span data-stu-id="dedb1-115">Property</span></span>                                                                         | <span data-ttu-id="dedb1-116">Тип доступа</span><span class="sxs-lookup"><span data-stu-id="dedb1-116">Access type</span></span>           | <span data-ttu-id="dedb1-117">Описание</span><span class="sxs-lookup"><span data-stu-id="dedb1-117">Description</span></span>                                                  |
|:---------------------------------------------------------------------------------|:----------------------|:-------------------------------------------------------------|
| [<span data-ttu-id="dedb1-118">**AddItem**</span><span class="sxs-lookup"><span data-stu-id="dedb1-118">**AddItem**</span></span>](-search-2x-ipropertyfiltercollection-additem.md)<br/>       | <span data-ttu-id="dedb1-119">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="dedb1-119">Read-only</span></span><br/>  | <span data-ttu-id="dedb1-120">Добавляет новый фильтр в коллекцию.</span><span class="sxs-lookup"><span data-stu-id="dedb1-120">Adds a new filter to the collection.</span></span> <br/>             |
| [<span data-ttu-id="dedb1-121">**открытым**</span><span class="sxs-lookup"><span data-stu-id="dedb1-121">**clear**</span></span>](-search-2x-ipropertyfiltercollection-clear.md)<br/>           | <span data-ttu-id="dedb1-122">Только на запись</span><span class="sxs-lookup"><span data-stu-id="dedb1-122">Write-only</span></span><br/> | <span data-ttu-id="dedb1-123">Очищает коллекцию.</span><span class="sxs-lookup"><span data-stu-id="dedb1-123">Clears the collection.</span></span> <br/>                           |
| [<span data-ttu-id="dedb1-124">**Расчета**</span><span class="sxs-lookup"><span data-stu-id="dedb1-124">**Count**</span></span>](-search-2x-ipropertyfiltercollection-count.md)<br/>           | <span data-ttu-id="dedb1-125">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="dedb1-125">Read-only</span></span><br/>  | <span data-ttu-id="dedb1-126">Число фильтров в коллекции.</span><span class="sxs-lookup"><span data-stu-id="dedb1-126">Number of filters in the collection.</span></span> <br/>             |
| [<span data-ttu-id="dedb1-127">**GetITem**</span><span class="sxs-lookup"><span data-stu-id="dedb1-127">**GetITem**</span></span>](-search-2x-ipropertyfiltercollection-getitem.md)<br/>       | <span data-ttu-id="dedb1-128">Чтение/запись</span><span class="sxs-lookup"><span data-stu-id="dedb1-128">Read/write</span></span><br/> | <span data-ttu-id="dedb1-129">Возвращает конкретный фильтр в коллекции.</span><span class="sxs-lookup"><span data-stu-id="dedb1-129">Returns a specific filter within the collection.</span></span> <br/> |
| [<span data-ttu-id="dedb1-130">**RemoveItem**</span><span class="sxs-lookup"><span data-stu-id="dedb1-130">**RemoveItem**</span></span>](-search-2x-ipropertyfiltercollection-removeitem.md)<br/> | <span data-ttu-id="dedb1-131">Только на запись</span><span class="sxs-lookup"><span data-stu-id="dedb1-131">Write-only</span></span><br/> | <span data-ttu-id="dedb1-132">Удаляет конкретный фильтр в коллекции.</span><span class="sxs-lookup"><span data-stu-id="dedb1-132">Removes a specific filter to the collection.</span></span> <br/>     |



 

## <a name="remarks"></a><span data-ttu-id="dedb1-133">Комментарии</span><span class="sxs-lookup"><span data-stu-id="dedb1-133">Remarks</span></span>

<span data-ttu-id="dedb1-134">Эти свойства используются для фильтрации коллекции, возвращаемой запросом.</span><span class="sxs-lookup"><span data-stu-id="dedb1-134">These properties are used to filter collection returned by the query.</span></span>

## <a name="requirements"></a><span data-ttu-id="dedb1-135">Требования</span><span class="sxs-lookup"><span data-stu-id="dedb1-135">Requirements</span></span>



| <span data-ttu-id="dedb1-136">Требование</span><span class="sxs-lookup"><span data-stu-id="dedb1-136">Requirement</span></span> | <span data-ttu-id="dedb1-137">Значение</span><span class="sxs-lookup"><span data-stu-id="dedb1-137">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="dedb1-138">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="dedb1-138">Minimum supported client</span></span><br/> | <span data-ttu-id="dedb1-139">Только для настольных приложений Windows XP с пакетом обновления 2 \[\]</span><span class="sxs-lookup"><span data-stu-id="dedb1-139">Windows XP with SP2 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="dedb1-140">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="dedb1-140">Minimum supported server</span></span><br/> | <span data-ttu-id="dedb1-141">Только для настольных приложений Windows Server 2003 с пакетом обновления 1 \[\]</span><span class="sxs-lookup"><span data-stu-id="dedb1-141">Windows Server 2003 with SP1 \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="dedb1-142">Распространяемые компоненты</span><span class="sxs-lookup"><span data-stu-id="dedb1-142">Redistributable</span></span><br/>          | <span data-ttu-id="dedb1-143">Поиск на рабочем столе Windows (WDS) 3,0</span><span class="sxs-lookup"><span data-stu-id="dedb1-143">Windows Desktop Search (WDS) 3.0</span></span><br/>                                               |
| <span data-ttu-id="dedb1-144">Header</span><span class="sxs-lookup"><span data-stu-id="dedb1-144">Header</span></span><br/>                   | <dl> <span data-ttu-id="dedb1-145"><dt>Вдсшаредидл. h</dt></span><span class="sxs-lookup"><span data-stu-id="dedb1-145"><dt>WdsSharedIDL.h</dt></span></span> </dl> |



 

