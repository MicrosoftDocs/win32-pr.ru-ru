---
title: Интерфейс Иресултсвиевер (Вдсшаредидл. h)
description: Предоставляет методы и свойства для представления результатов.
ms.assetid: 4d476511-d65c-4417-8073-337cfbae621d
keywords:
- Устаревшие функции среды Windows интерфейса Иресултсвиевер
- Интерфейс Иресултсвиевер устаревшие функции среды Windows, описание
topic_type:
- apiref
api_name:
- IResultsViewer
api_location:
- WdsSharedIDL.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 18702812394f6e7fedd626062aa8c0116cab8427
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104534511"
---
# <a name="iresultsviewer-interface"></a><span data-ttu-id="2e2a5-105">Интерфейс Иресултсвиевер</span><span class="sxs-lookup"><span data-stu-id="2e2a5-105">IResultsViewer interface</span></span>

> [!NOTE]
> <span data-ttu-id="2e2a5-106">Windows Desktop Search 2. x — это устаревшая технология, которая изначально была доступна в качестве надстройки для Windows XP и Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="2e2a5-106">Windows Desktop Search 2.x is an obsolete technology that was originally available as an add-in for Windows XP and Windows Server 2003.</span></span> <span data-ttu-id="2e2a5-107">В более поздних выпусках используйте [API поиска Windows](../search/-search-reference-entry-page.md) .</span><span class="sxs-lookup"><span data-stu-id="2e2a5-107">On later releases, use the [Windows Search API](../search/-search-reference-entry-page.md) instead.</span></span> 

<span data-ttu-id="2e2a5-108">Предоставляет методы и свойства для представления результатов.</span><span class="sxs-lookup"><span data-stu-id="2e2a5-108">Exposes methods and properties for the results view.</span></span>

## <a name="members"></a><span data-ttu-id="2e2a5-109">Элементы</span><span class="sxs-lookup"><span data-stu-id="2e2a5-109">Members</span></span>

<span data-ttu-id="2e2a5-110">Интерфейс **иресултсвиевер** наследует от интерфейса [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="2e2a5-110">The **IResultsViewer** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="2e2a5-111">**Иресултсвиевер** также имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="2e2a5-111">**IResultsViewer** also has these types of members:</span></span>

-   [<span data-ttu-id="2e2a5-112">Методы</span><span class="sxs-lookup"><span data-stu-id="2e2a5-112">Methods</span></span>](#methods)
-   [<span data-ttu-id="2e2a5-113">Свойства</span><span class="sxs-lookup"><span data-stu-id="2e2a5-113">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="2e2a5-114">Методы</span><span class="sxs-lookup"><span data-stu-id="2e2a5-114">Methods</span></span>

<span data-ttu-id="2e2a5-115">Интерфейс **иресултсвиевер** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="2e2a5-115">The **IResultsViewer** interface has these methods.</span></span>



| <span data-ttu-id="2e2a5-116">Метод</span><span class="sxs-lookup"><span data-stu-id="2e2a5-116">Method</span></span>                                                   | <span data-ttu-id="2e2a5-117">Описание</span><span class="sxs-lookup"><span data-stu-id="2e2a5-117">Description</span></span>                                                                            |
|:---------------------------------------------------------|:---------------------------------------------------------------------------------------|
| [<span data-ttu-id="2e2a5-118">**GoBack**</span><span class="sxs-lookup"><span data-stu-id="2e2a5-118">**GoBack**</span></span>](-search-2x-iresultsviewer-goback.md)       | <span data-ttu-id="2e2a5-119">Не реализован.</span><span class="sxs-lookup"><span data-stu-id="2e2a5-119">Not implemented.</span></span><br/>                                                            |
| [<span data-ttu-id="2e2a5-120">**GoForward**</span><span class="sxs-lookup"><span data-stu-id="2e2a5-120">**GoForward**</span></span>](-search-2x-iresultsviewer-goforward.md) | <span data-ttu-id="2e2a5-121">Не реализован.</span><span class="sxs-lookup"><span data-stu-id="2e2a5-121">Not implemented.</span></span><br/>                                                            |
| [<span data-ttu-id="2e2a5-122">**Обновить**</span><span class="sxs-lookup"><span data-stu-id="2e2a5-122">**Refresh**</span></span>](-search-2x-iresultsviewer-refresh.md)     | <span data-ttu-id="2e2a5-123">Не реализован.</span><span class="sxs-lookup"><span data-stu-id="2e2a5-123">Not implemented.</span></span><br/>                                                            |
| [<span data-ttu-id="2e2a5-124">**Stop**</span><span class="sxs-lookup"><span data-stu-id="2e2a5-124">**Stop**</span></span>](-search-2x-iresultsviewer-stop.md)           | <span data-ttu-id="2e2a5-125">Не реализован.</span><span class="sxs-lookup"><span data-stu-id="2e2a5-125">Not implemented.</span></span><br/>                                                            |
| [<span data-ttu-id="2e2a5-126">**Обновляют**</span><span class="sxs-lookup"><span data-stu-id="2e2a5-126">**Update**</span></span>](-search-2x-iresultsviewer-update.md)       | <span data-ttu-id="2e2a5-127">Применяет любые изменения запроса и перемещает представление к новому набору результатов.</span><span class="sxs-lookup"><span data-stu-id="2e2a5-127">Applies any query changes and navigates the view to the new set of results.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="2e2a5-128">Свойства</span><span class="sxs-lookup"><span data-stu-id="2e2a5-128">Properties</span></span>

<span data-ttu-id="2e2a5-129">Интерфейс **иресултсвиевер** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="2e2a5-129">The **IResultsViewer** interface has these properties.</span></span>



| <span data-ttu-id="2e2a5-130">Свойство</span><span class="sxs-lookup"><span data-stu-id="2e2a5-130">Property</span></span>                                                                            | <span data-ttu-id="2e2a5-131">Тип доступа</span><span class="sxs-lookup"><span data-stu-id="2e2a5-131">Access type</span></span>           | <span data-ttu-id="2e2a5-132">Описание</span><span class="sxs-lookup"><span data-stu-id="2e2a5-132">Description</span></span>                                                                                      |
|:------------------------------------------------------------------------------------|:----------------------|:-------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="2e2a5-133">**Содержимое**</span><span class="sxs-lookup"><span data-stu-id="2e2a5-133">**Contents**</span></span>](-search-2x-iresultsviewer-contents.md)<br/>                   | <span data-ttu-id="2e2a5-134">Только на запись</span><span class="sxs-lookup"><span data-stu-id="2e2a5-134">Write-only</span></span><br/> | <span data-ttu-id="2e2a5-135">Это свойство отслеживает тип содержимого, отображаемого в представлении результатов.</span><span class="sxs-lookup"><span data-stu-id="2e2a5-135">This property tracks the type of the content being displayed in the results view.</span></span> <br/>    |
| [<span data-ttu-id="2e2a5-136">**DisplayName**</span><span class="sxs-lookup"><span data-stu-id="2e2a5-136">**DisplayName**</span></span>](-search-2x-iresultsviewer-displayname.md)<br/>             | <span data-ttu-id="2e2a5-137">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="2e2a5-137">Read-only</span></span><br/>  | <span data-ttu-id="2e2a5-138">Локализованное отображаемое имя типа.</span><span class="sxs-lookup"><span data-stu-id="2e2a5-138">Localized display name of the type.</span></span><br/>                                                   |
| [<span data-ttu-id="2e2a5-139">**енумселектедитемс**</span><span class="sxs-lookup"><span data-stu-id="2e2a5-139">**EnumSelectedItems**</span></span>](-search-2x-iresultsviewer-enumselecteditems.md)<br/> | <span data-ttu-id="2e2a5-140">Только на запись</span><span class="sxs-lookup"><span data-stu-id="2e2a5-140">Write-only</span></span><br/> | <span data-ttu-id="2e2a5-141">Не реализован.</span><span class="sxs-lookup"><span data-stu-id="2e2a5-141">Not implemented.</span></span><br/>                                                                      |
| [<span data-ttu-id="2e2a5-142">**FilterType**</span><span class="sxs-lookup"><span data-stu-id="2e2a5-142">**FilterType**</span></span>](-search-2x-iresultsviewer-filtertype.md)<br/>               | <span data-ttu-id="2e2a5-143">Чтение/запись</span><span class="sxs-lookup"><span data-stu-id="2e2a5-143">Read/write</span></span><br/> | <span data-ttu-id="2e2a5-144">Это свойство задает или возвращает имя типа прецеивед, по которому будут фильтроваться результаты.</span><span class="sxs-lookup"><span data-stu-id="2e2a5-144">This property will set or return the name of the preceived type to filter results by.</span></span><br/> |
| [<span data-ttu-id="2e2a5-145">**хеадерстиле**</span><span class="sxs-lookup"><span data-stu-id="2e2a5-145">**HeaderStyle**</span></span>](-search-2x-iresultsviewer-headerstyle.md)<br/>             | <span data-ttu-id="2e2a5-146">Чтение/запись</span><span class="sxs-lookup"><span data-stu-id="2e2a5-146">Read/write</span></span><br/> | <span data-ttu-id="2e2a5-147">Стиль заголовка, отображаемого в представлении.</span><span class="sxs-lookup"><span data-stu-id="2e2a5-147">The style of header displayed in the view.</span></span><br/>                                            |
| [<span data-ttu-id="2e2a5-148">**исупдатенидед**</span><span class="sxs-lookup"><span data-stu-id="2e2a5-148">**IsUpdateNeeded**</span></span>](-search-2x-iresultsviewer-isupdateneeded.md)<br/>       | <span data-ttu-id="2e2a5-149">Только на запись</span><span class="sxs-lookup"><span data-stu-id="2e2a5-149">Write-only</span></span><br/> | <span data-ttu-id="2e2a5-150">Это возвращает значение TRUE, если запрос views был изменен и требует обновления.</span><span class="sxs-lookup"><span data-stu-id="2e2a5-150">This returns TRUE if the views query has been modified and needs updating.</span></span> <br/>           |
| [<span data-ttu-id="2e2a5-151">**ItemStore**</span><span class="sxs-lookup"><span data-stu-id="2e2a5-151">**ItemStore**</span></span>](-search-2x-iresultsviewer-itemstore.md)<br/>                 | <span data-ttu-id="2e2a5-152">Чтение/запись</span><span class="sxs-lookup"><span data-stu-id="2e2a5-152">Read/write</span></span><br/> | <span data-ttu-id="2e2a5-153">Это свойство задает или возвращает имя хранилища, по которому будут фильтроваться результаты.</span><span class="sxs-lookup"><span data-stu-id="2e2a5-153">This property will set or return the name of the store to filter results by.</span></span><br/>          |
| [<span data-ttu-id="2e2a5-154">**превиевстиле**</span><span class="sxs-lookup"><span data-stu-id="2e2a5-154">**PreviewStyle**</span></span>](-search-2x-iresultsviewer-previewstyle.md)<br/>           | <span data-ttu-id="2e2a5-155">Чтение/запись</span><span class="sxs-lookup"><span data-stu-id="2e2a5-155">Read/write</span></span><br/> | <span data-ttu-id="2e2a5-156">Управляет режимом просмотра панели просмотра.</span><span class="sxs-lookup"><span data-stu-id="2e2a5-156">Controls the preview pane's display mode.</span></span><br/>                                             |
| [<span data-ttu-id="2e2a5-157">**пропертифилтерс**</span><span class="sxs-lookup"><span data-stu-id="2e2a5-157">**PropertyFilters**</span></span>](-search-2x-iresultsviewer-propertyfilters.md)<br/>     | <span data-ttu-id="2e2a5-158">Только на запись</span><span class="sxs-lookup"><span data-stu-id="2e2a5-158">Write-only</span></span><br/> | <span data-ttu-id="2e2a5-159">При вызове коллекции фильтров свойств будет возвращено следующее:</span><span class="sxs-lookup"><span data-stu-id="2e2a5-159">When calling the property filter collection it will return the following:</span></span><br/>             |
| [<span data-ttu-id="2e2a5-160">**QueryText**</span><span class="sxs-lookup"><span data-stu-id="2e2a5-160">**QueryText**</span></span>](-search-2x-iresultsviewer-querytext.md)<br/>                 | <span data-ttu-id="2e2a5-161">Чтение/запись</span><span class="sxs-lookup"><span data-stu-id="2e2a5-161">Read/write</span></span><br/> | <span data-ttu-id="2e2a5-162">Возвращает или задает текст текущего запроса.</span><span class="sxs-lookup"><span data-stu-id="2e2a5-162">Gets or sets the current query text.</span></span><br/>                                                  |
| [<span data-ttu-id="2e2a5-163">**ресултсстиле**</span><span class="sxs-lookup"><span data-stu-id="2e2a5-163">**ResultsStyle**</span></span>](-search-2x-iresultsviewer-resultsstyle.md)<br/>           | <span data-ttu-id="2e2a5-164">Только на запись</span><span class="sxs-lookup"><span data-stu-id="2e2a5-164">Write-only</span></span><br/> | <span data-ttu-id="2e2a5-165">Не реализован.</span><span class="sxs-lookup"><span data-stu-id="2e2a5-165">Not implemented.</span></span><br/>                                                                      |
| [<span data-ttu-id="2e2a5-166">**сортордерпроперти**</span><span class="sxs-lookup"><span data-stu-id="2e2a5-166">**SortOrderProperty**</span></span>](-search-2x-iresultsviewer-sortorderproperty.md)<br/> | <span data-ttu-id="2e2a5-167">Чтение/запись</span><span class="sxs-lookup"><span data-stu-id="2e2a5-167">Read/write</span></span><br/> | <span data-ttu-id="2e2a5-168">Это свойство задает или возвращает порядок столбцов для сортировки результатов по.</span><span class="sxs-lookup"><span data-stu-id="2e2a5-168">This property will set or return the order of columns to sort results by.</span></span> <br/>            |
| [<span data-ttu-id="2e2a5-169">**SortProperty**</span><span class="sxs-lookup"><span data-stu-id="2e2a5-169">**SortProperty**</span></span>](-search-2x-iresultsviewer-sortproperty.md)<br/>           | <span data-ttu-id="2e2a5-170">Чтение/запись</span><span class="sxs-lookup"><span data-stu-id="2e2a5-170">Read/write</span></span><br/> | <span data-ttu-id="2e2a5-171">Это свойство задаст или возвратит Индексколумн свойства для сортировки результатов по.</span><span class="sxs-lookup"><span data-stu-id="2e2a5-171">This property will set or return the IndexColumn of the property to sort results by.</span></span> <br/> |



 

## <a name="remarks"></a><span data-ttu-id="2e2a5-172">Комментарии</span><span class="sxs-lookup"><span data-stu-id="2e2a5-172">Remarks</span></span>

<span data-ttu-id="2e2a5-173">Эти методы и свойства используются для работы с просматриваемой информацией.</span><span class="sxs-lookup"><span data-stu-id="2e2a5-173">These methods and properties are used to manipulate the information viewed.</span></span>

## <a name="requirements"></a><span data-ttu-id="2e2a5-174">Требования</span><span class="sxs-lookup"><span data-stu-id="2e2a5-174">Requirements</span></span>



| <span data-ttu-id="2e2a5-175">Требование</span><span class="sxs-lookup"><span data-stu-id="2e2a5-175">Requirement</span></span> | <span data-ttu-id="2e2a5-176">Значение</span><span class="sxs-lookup"><span data-stu-id="2e2a5-176">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="2e2a5-177">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="2e2a5-177">Minimum supported client</span></span><br/> | <span data-ttu-id="2e2a5-178">Только для настольных приложений Windows XP с пакетом обновления 2 \[\]</span><span class="sxs-lookup"><span data-stu-id="2e2a5-178">Windows XP with SP2 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="2e2a5-179">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="2e2a5-179">Minimum supported server</span></span><br/> | <span data-ttu-id="2e2a5-180">Только для настольных приложений Windows Server 2003 с пакетом обновления 1 \[\]</span><span class="sxs-lookup"><span data-stu-id="2e2a5-180">Windows Server 2003 with SP1 \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="2e2a5-181">Распространяемые компоненты</span><span class="sxs-lookup"><span data-stu-id="2e2a5-181">Redistributable</span></span><br/>          | <span data-ttu-id="2e2a5-182">Поиск на рабочем столе Windows (WDS) 3,0</span><span class="sxs-lookup"><span data-stu-id="2e2a5-182">Windows Desktop Search (WDS) 3.0</span></span><br/>                                               |
| <span data-ttu-id="2e2a5-183">Header</span><span class="sxs-lookup"><span data-stu-id="2e2a5-183">Header</span></span><br/>                   | <dl> <span data-ttu-id="2e2a5-184"><dt>Вдсшаредидл. h</dt></span><span class="sxs-lookup"><span data-stu-id="2e2a5-184"><dt>WdsSharedIDL.h</dt></span></span> </dl> |



 

