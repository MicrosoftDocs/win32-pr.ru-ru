---
title: Интерфейс Исеарчресулт (Вдсшаредидл. h)
description: Предоставляет сведения и свойства, относящиеся к результирующему набору.
ms.assetid: 2f50b9d7-f6fd-481c-a5db-d622a7b02017
keywords:
- Устаревшие функции среды Windows интерфейса Исеарчресулт
- Интерфейс Исеарчресулт устаревшие функции среды Windows, описание
topic_type:
- apiref
api_name:
- ISearchResult
api_location:
- WdsSharedIDL.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 89387ebe02c87ca6a5c5ac663a67ea060bd78948
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103802884"
---
# <a name="isearchresult-interface"></a><span data-ttu-id="ca1fb-105">Интерфейс Исеарчресулт</span><span class="sxs-lookup"><span data-stu-id="ca1fb-105">ISearchResult interface</span></span>

> [!NOTE]
> <span data-ttu-id="ca1fb-106">Windows Desktop Search 2. x — это устаревшая технология, которая изначально была доступна в качестве надстройки для Windows XP и Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="ca1fb-106">Windows Desktop Search 2.x is an obsolete technology that was originally available as an add-in for Windows XP and Windows Server 2003.</span></span> <span data-ttu-id="ca1fb-107">В более поздних выпусках используйте [API поиска Windows](../search/-search-reference-entry-page.md) .</span><span class="sxs-lookup"><span data-stu-id="ca1fb-107">On later releases, use the [Windows Search API](../search/-search-reference-entry-page.md) instead.</span></span> 

<span data-ttu-id="ca1fb-108">Предоставляет сведения и свойства, относящиеся к результирующему набору.</span><span class="sxs-lookup"><span data-stu-id="ca1fb-108">Exposes information and properties regarding the result set.</span></span>

## <a name="members"></a><span data-ttu-id="ca1fb-109">Элементы</span><span class="sxs-lookup"><span data-stu-id="ca1fb-109">Members</span></span>

<span data-ttu-id="ca1fb-110">Интерфейс **исеарчресулт** наследует от интерфейса [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="ca1fb-110">The **ISearchResult** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="ca1fb-111">**Исеарчресулт** также имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="ca1fb-111">**ISearchResult** also has these types of members:</span></span>

-   [<span data-ttu-id="ca1fb-112">Методы</span><span class="sxs-lookup"><span data-stu-id="ca1fb-112">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="ca1fb-113">Методы</span><span class="sxs-lookup"><span data-stu-id="ca1fb-113">Methods</span></span>

<span data-ttu-id="ca1fb-114">Интерфейс **исеарчресулт** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="ca1fb-114">The **ISearchResult** interface has these methods.</span></span>



| <span data-ttu-id="ca1fb-115">Метод</span><span class="sxs-lookup"><span data-stu-id="ca1fb-115">Method</span></span>                                                            | <span data-ttu-id="ca1fb-116">Описание</span><span class="sxs-lookup"><span data-stu-id="ca1fb-116">Description</span></span>                 |
|:------------------------------------------------------------------|:----------------------------|
| [<span data-ttu-id="ca1fb-117">**Доступность**</span><span class="sxs-lookup"><span data-stu-id="ca1fb-117">**Availability**</span></span>](-search-2x-isearchresult-availability.md)     | <span data-ttu-id="ca1fb-118">Не реализован.</span><span class="sxs-lookup"><span data-stu-id="ca1fb-118">Not implemented.</span></span><br/> |
| [<span data-ttu-id="ca1fb-119">**доверб**</span><span class="sxs-lookup"><span data-stu-id="ca1fb-119">**DoVerb**</span></span>](-search-2x-isearchresult-doverb.md)                 | <span data-ttu-id="ca1fb-120">Не реализован.</span><span class="sxs-lookup"><span data-stu-id="ca1fb-120">Not implemented.</span></span><br/> |
| [<span data-ttu-id="ca1fb-121">**Значок**</span><span class="sxs-lookup"><span data-stu-id="ca1fb-121">**GetIcon**</span></span>](-search-2x-isearchresult-geticon.md)               | <span data-ttu-id="ca1fb-122">Не реализован.</span><span class="sxs-lookup"><span data-stu-id="ca1fb-122">Not implemented.</span></span><br/> |
| [<span data-ttu-id="ca1fb-123">**GetThumbnail**</span><span class="sxs-lookup"><span data-stu-id="ca1fb-123">**GetThumbnail**</span></span>](-search-2x-isearchresult-getthumbnail.md)     | <span data-ttu-id="ca1fb-124">Не реализован.</span><span class="sxs-lookup"><span data-stu-id="ca1fb-124">Not implemented.</span></span><br/> |
| [<span data-ttu-id="ca1fb-125">**GetValue**</span><span class="sxs-lookup"><span data-stu-id="ca1fb-125">**GetValue**</span></span>](-search-2x-isearchresult-getvalue.md)             | <span data-ttu-id="ca1fb-126">Не реализован.</span><span class="sxs-lookup"><span data-stu-id="ca1fb-126">Not implemented.</span></span><br/> |
| [<span data-ttu-id="ca1fb-127">**Команда verb**</span><span class="sxs-lookup"><span data-stu-id="ca1fb-127">**GetVerb**</span></span>](-search-2x-isearchresult-getverb.md)               | <span data-ttu-id="ca1fb-128">Не реализован.</span><span class="sxs-lookup"><span data-stu-id="ca1fb-128">Not implemented.</span></span><br/> |
| [<span data-ttu-id="ca1fb-129">**иконкаунт**</span><span class="sxs-lookup"><span data-stu-id="ca1fb-129">**IconCount**</span></span>](-search-2x-isearchresult-iconcount.md)           | <span data-ttu-id="ca1fb-130">Не реализован.</span><span class="sxs-lookup"><span data-stu-id="ca1fb-130">Not implemented.</span></span><br/> |
| [<span data-ttu-id="ca1fb-131">**Номер**</span><span class="sxs-lookup"><span data-stu-id="ca1fb-131">**Index**</span></span>](-search-2x-isearchresult-index.md)                   | <span data-ttu-id="ca1fb-132">Не реализован.</span><span class="sxs-lookup"><span data-stu-id="ca1fb-132">Not implemented.</span></span><br/> |
| [<span data-ttu-id="ca1fb-133">**LoadState**</span><span class="sxs-lookup"><span data-stu-id="ca1fb-133">**LoadState**</span></span>](-search-2x-isearchresult-loadstate.md)           | <span data-ttu-id="ca1fb-134">Не реализован.</span><span class="sxs-lookup"><span data-stu-id="ca1fb-134">Not implemented.</span></span><br/> |
| [<span data-ttu-id="ca1fb-135">**Средство предварительного просмотра**</span><span class="sxs-lookup"><span data-stu-id="ca1fb-135">**Previewer**</span></span>](-search-2x-isearchresult-previewer.md)           | <span data-ttu-id="ca1fb-136">Не реализован.</span><span class="sxs-lookup"><span data-stu-id="ca1fb-136">Not implemented.</span></span><br/> |
| [<span data-ttu-id="ca1fb-137">**путвалуе**</span><span class="sxs-lookup"><span data-stu-id="ca1fb-137">**PutValue**</span></span>](-search-2x-isearchresult-putvalue.md)             | <span data-ttu-id="ca1fb-138">Не реализован.</span><span class="sxs-lookup"><span data-stu-id="ca1fb-138">Not implemented.</span></span><br/> |
| [<span data-ttu-id="ca1fb-139">**сумбнаилстате**</span><span class="sxs-lookup"><span data-stu-id="ca1fb-139">**ThumbnailState**</span></span>](-search-2x-isearchresult-thumbnailstate.md) | <span data-ttu-id="ca1fb-140">Не реализован.</span><span class="sxs-lookup"><span data-stu-id="ca1fb-140">Not implemented.</span></span><br/> |
| [<span data-ttu-id="ca1fb-141">**Тип**</span><span class="sxs-lookup"><span data-stu-id="ca1fb-141">**Type**</span></span>](-search-2x-isearchresult-type.md)                     | <span data-ttu-id="ca1fb-142">Не реализован.</span><span class="sxs-lookup"><span data-stu-id="ca1fb-142">Not implemented.</span></span><br/> |
| [<span data-ttu-id="ca1fb-143">**вербкаунт**</span><span class="sxs-lookup"><span data-stu-id="ca1fb-143">**VerbCount**</span></span>](-search-2x-isearchresult-verbcount.md)           | <span data-ttu-id="ca1fb-144">Не реализован.</span><span class="sxs-lookup"><span data-stu-id="ca1fb-144">Not implemented.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="ca1fb-145">Комментарии</span><span class="sxs-lookup"><span data-stu-id="ca1fb-145">Remarks</span></span>

<span data-ttu-id="ca1fb-146">Эти методы предоставляют свойства и действия, применимые к результирующему набору.</span><span class="sxs-lookup"><span data-stu-id="ca1fb-146">These methods expose properties and actions applicable to the result set.</span></span>

## <a name="requirements"></a><span data-ttu-id="ca1fb-147">Требования</span><span class="sxs-lookup"><span data-stu-id="ca1fb-147">Requirements</span></span>



| <span data-ttu-id="ca1fb-148">Требование</span><span class="sxs-lookup"><span data-stu-id="ca1fb-148">Requirement</span></span> | <span data-ttu-id="ca1fb-149">Значение</span><span class="sxs-lookup"><span data-stu-id="ca1fb-149">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="ca1fb-150">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="ca1fb-150">Minimum supported client</span></span><br/> | <span data-ttu-id="ca1fb-151">Только для настольных приложений Windows XP с пакетом обновления 2 \[\]</span><span class="sxs-lookup"><span data-stu-id="ca1fb-151">Windows XP with SP2 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="ca1fb-152">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="ca1fb-152">Minimum supported server</span></span><br/> | <span data-ttu-id="ca1fb-153">Только для настольных приложений Windows Server 2003 с пакетом обновления 1 \[\]</span><span class="sxs-lookup"><span data-stu-id="ca1fb-153">Windows Server 2003 with SP1 \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="ca1fb-154">Распространяемые компоненты</span><span class="sxs-lookup"><span data-stu-id="ca1fb-154">Redistributable</span></span><br/>          | <span data-ttu-id="ca1fb-155">Поиск на рабочем столе Windows (WDS) 3,0</span><span class="sxs-lookup"><span data-stu-id="ca1fb-155">Windows Desktop Search (WDS) 3.0</span></span><br/>                                               |
| <span data-ttu-id="ca1fb-156">Header</span><span class="sxs-lookup"><span data-stu-id="ca1fb-156">Header</span></span><br/>                   | <dl> <span data-ttu-id="ca1fb-157"><dt>Вдсшаредидл. h</dt></span><span class="sxs-lookup"><span data-stu-id="ca1fb-157"><dt>WdsSharedIDL.h</dt></span></span> </dl> |



 

