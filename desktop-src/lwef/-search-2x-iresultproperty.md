---
title: Интерфейс Иресултпроперти (Вдсшаредидл. h)
description: Предоставляет свойства результата.
ms.assetid: 58d8c516-47c6-4cae-b46c-5127baf3054d
keywords:
- Устаревшие функции среды Windows интерфейса Иресултпроперти
- Интерфейс Иресултпроперти устаревшие функции среды Windows, описание
topic_type:
- apiref
api_name:
- IResultProperty
api_location:
- WdsSharedIDL.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 716c0b3998171731dea5f976afc266fe81b2c613
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105691878"
---
# <a name="iresultproperty-interface"></a><span data-ttu-id="648ea-105">Интерфейс Иресултпроперти</span><span class="sxs-lookup"><span data-stu-id="648ea-105">IResultProperty interface</span></span>

> [!NOTE]
> <span data-ttu-id="648ea-106">Windows Desktop Search 2. x — это устаревшая технология, которая изначально была доступна в качестве надстройки для Windows XP и Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="648ea-106">Windows Desktop Search 2.x is an obsolete technology that was originally available as an add-in for Windows XP and Windows Server 2003.</span></span> <span data-ttu-id="648ea-107">В более поздних выпусках используйте [API поиска Windows](../search/-search-reference-entry-page.md) .</span><span class="sxs-lookup"><span data-stu-id="648ea-107">On later releases, use the [Windows Search API](../search/-search-reference-entry-page.md) instead.</span></span> 

<span data-ttu-id="648ea-108">Предоставляет свойства результата.</span><span class="sxs-lookup"><span data-stu-id="648ea-108">Exposes result properties.</span></span>

## <a name="members"></a><span data-ttu-id="648ea-109">Элементы</span><span class="sxs-lookup"><span data-stu-id="648ea-109">Members</span></span>

<span data-ttu-id="648ea-110">Интерфейс **иресултпроперти** наследует от интерфейса [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="648ea-110">The **IResultProperty** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="648ea-111">**Иресултпроперти** также имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="648ea-111">**IResultProperty** also has these types of members:</span></span>

-   [<span data-ttu-id="648ea-112">Методы</span><span class="sxs-lookup"><span data-stu-id="648ea-112">Methods</span></span>](#methods)
-   [<span data-ttu-id="648ea-113">Свойства</span><span class="sxs-lookup"><span data-stu-id="648ea-113">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="648ea-114">Методы</span><span class="sxs-lookup"><span data-stu-id="648ea-114">Methods</span></span>

<span data-ttu-id="648ea-115">Интерфейс **иресултпроперти** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="648ea-115">The **IResultProperty** interface has these methods.</span></span>



| <span data-ttu-id="648ea-116">Метод</span><span class="sxs-lookup"><span data-stu-id="648ea-116">Method</span></span>                                                    | <span data-ttu-id="648ea-117">Описание</span><span class="sxs-lookup"><span data-stu-id="648ea-117">Description</span></span>                 |
|:----------------------------------------------------------|:----------------------------|
| [<span data-ttu-id="648ea-118">**GoBack**</span><span class="sxs-lookup"><span data-stu-id="648ea-118">**GoBack**</span></span>](-search-2x-iresultproperty-goback.md)       | <span data-ttu-id="648ea-119">Не реализован.</span><span class="sxs-lookup"><span data-stu-id="648ea-119">Not implemented.</span></span><br/> |
| [<span data-ttu-id="648ea-120">**GoForward**</span><span class="sxs-lookup"><span data-stu-id="648ea-120">**GoForward**</span></span>](-search-2x-iresultproperty-goforward.md) | <span data-ttu-id="648ea-121">Не реализован.</span><span class="sxs-lookup"><span data-stu-id="648ea-121">Not implemented.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="648ea-122">Свойства</span><span class="sxs-lookup"><span data-stu-id="648ea-122">Properties</span></span>

<span data-ttu-id="648ea-123">Интерфейс **иресултпроперти** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="648ea-123">The **IResultProperty** interface has these properties.</span></span>



| <span data-ttu-id="648ea-124">Свойство</span><span class="sxs-lookup"><span data-stu-id="648ea-124">Property</span></span>                                                                   | <span data-ttu-id="648ea-125">Тип доступа</span><span class="sxs-lookup"><span data-stu-id="648ea-125">Access type</span></span>          | <span data-ttu-id="648ea-126">Описание</span><span class="sxs-lookup"><span data-stu-id="648ea-126">Description</span></span>                                           |
|:---------------------------------------------------------------------------|:---------------------|:------------------------------------------------------|
| [<span data-ttu-id="648ea-127">**Заданий**</span><span class="sxs-lookup"><span data-stu-id="648ea-127">**DataType**</span></span>](-search-2x-iresultproperty-datatype.md)<br/>         | <span data-ttu-id="648ea-128">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="648ea-128">Read-only</span></span><br/> | <span data-ttu-id="648ea-129">Тип данных Properties.</span><span class="sxs-lookup"><span data-stu-id="648ea-129">A properties data type.</span></span> <br/>                   |
| [<span data-ttu-id="648ea-130">**DisplayName**</span><span class="sxs-lookup"><span data-stu-id="648ea-130">**DisplayName**</span></span>](-search-2x-iresultproperty-displayname.md)<br/>   | <span data-ttu-id="648ea-131">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="648ea-131">Read-only</span></span><br/> | <span data-ttu-id="648ea-132">Локализованное отображаемое имя свойства.</span><span class="sxs-lookup"><span data-stu-id="648ea-132">Localized display name of the property.</span></span> <br/>   |
| [<span data-ttu-id="648ea-133">**DisplayState**</span><span class="sxs-lookup"><span data-stu-id="648ea-133">**DisplayState**</span></span>](-search-2x-iresultproperty-displaystate.md)<br/> | <span data-ttu-id="648ea-134">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="648ea-134">Read-only</span></span><br/> | <span data-ttu-id="648ea-135">Висабилити свойства.</span><span class="sxs-lookup"><span data-stu-id="648ea-135">Visability of the property.</span></span> <br/>               |
| [<span data-ttu-id="648ea-136">**Хинтинга**</span><span class="sxs-lookup"><span data-stu-id="648ea-136">**Hint**</span></span>](-search-2x-iresultproperty-hint.md)<br/>                 | <span data-ttu-id="648ea-137">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="648ea-137">Read-only</span></span><br/> | <span data-ttu-id="648ea-138">Специальное значение, используемое для облегчения извлечения данных.</span><span class="sxs-lookup"><span data-stu-id="648ea-138">Special value used to aid data retrieval.</span></span> <br/> |
| [<span data-ttu-id="648ea-139">**индексколумн**</span><span class="sxs-lookup"><span data-stu-id="648ea-139">**IndexColumn**</span></span>](-search-2x-iresultproperty-indexcolumn.md)<br/>   | <span data-ttu-id="648ea-140">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="648ea-140">Read-only</span></span><br/> | <span data-ttu-id="648ea-141">Имя столбца свойств в индексе.</span><span class="sxs-lookup"><span data-stu-id="648ea-141">Properties column name in the index.</span></span> <br/>      |
| [<span data-ttu-id="648ea-142">**ИД пользователя**</span><span class="sxs-lookup"><span data-stu-id="648ea-142">**UID**</span></span>](-search-2x-iresultproperty-uid.md)<br/>                   | <span data-ttu-id="648ea-143">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="648ea-143">Read-only</span></span><br/> | <span data-ttu-id="648ea-144">Уникальный идентификатор свойства.</span><span class="sxs-lookup"><span data-stu-id="648ea-144">Unique identifier for the property.</span></span> <br/>       |



 

## <a name="remarks"></a><span data-ttu-id="648ea-145">Комментарии</span><span class="sxs-lookup"><span data-stu-id="648ea-145">Remarks</span></span>

<span data-ttu-id="648ea-146">Это элементы, возвращающие свойства.</span><span class="sxs-lookup"><span data-stu-id="648ea-146">These are the items return properties.</span></span>

## <a name="requirements"></a><span data-ttu-id="648ea-147">Требования</span><span class="sxs-lookup"><span data-stu-id="648ea-147">Requirements</span></span>



| <span data-ttu-id="648ea-148">Требование</span><span class="sxs-lookup"><span data-stu-id="648ea-148">Requirement</span></span> | <span data-ttu-id="648ea-149">Значение</span><span class="sxs-lookup"><span data-stu-id="648ea-149">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="648ea-150">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="648ea-150">Minimum supported client</span></span><br/> | <span data-ttu-id="648ea-151">Только для настольных приложений Windows XP с пакетом обновления 2 \[\]</span><span class="sxs-lookup"><span data-stu-id="648ea-151">Windows XP with SP2 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="648ea-152">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="648ea-152">Minimum supported server</span></span><br/> | <span data-ttu-id="648ea-153">Только для настольных приложений Windows Server 2003 с пакетом обновления 1 \[\]</span><span class="sxs-lookup"><span data-stu-id="648ea-153">Windows Server 2003 with SP1 \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="648ea-154">Распространяемые компоненты</span><span class="sxs-lookup"><span data-stu-id="648ea-154">Redistributable</span></span><br/>          | <span data-ttu-id="648ea-155">Поиск на рабочем столе Windows (WDS) 3,0</span><span class="sxs-lookup"><span data-stu-id="648ea-155">Windows Desktop Search (WDS) 3.0</span></span><br/>                                               |
| <span data-ttu-id="648ea-156">Header</span><span class="sxs-lookup"><span data-stu-id="648ea-156">Header</span></span><br/>                   | <dl> <span data-ttu-id="648ea-157"><dt>Вдсшаредидл. h</dt></span><span class="sxs-lookup"><span data-stu-id="648ea-157"><dt>WdsSharedIDL.h</dt></span></span> </dl> |



 

