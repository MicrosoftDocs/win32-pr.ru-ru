---
description: Содержит набор элементов&\# 8212; Абзац, Инкворд, Drawing, Text, Image или Flag&\# 8212;, которые группируются вместе в заметке журнала.
ms.assetid: 59ee3037-7178-41c8-84d5-d5c68fa2cf9b
title: Граупноде, элемент
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6ee141691ef58d14e6c08a49544e9cf3ecf7540b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105647186"
---
# <a name="groupnode-element"></a><span data-ttu-id="28afb-103">Граупноде, элемент</span><span class="sxs-lookup"><span data-stu-id="28afb-103">GroupNode Element</span></span>

<span data-ttu-id="28afb-104">Содержит набор элементов ([**абзац**](paragraph-element.md), [**инкворд**](inkword-element.md), [**Рисование**](drawing-element.md), [**текст**](text-element.md), [**изображение**](image-element.md)или [**флаг**](flag-element.md)), которые группируются в заметке журнала.</span><span class="sxs-lookup"><span data-stu-id="28afb-104">Contains a set of elements—[**Paragraph**](paragraph-element.md), [**InkWord**](inkword-element.md), [**Drawing**](drawing-element.md), [**Text**](text-element.md), [**Image**](image-element.md), or [**Flag**](flag-element.md)—that are grouped together in the Journal note.</span></span>

## <a name="definition"></a><span data-ttu-id="28afb-105">Определение</span><span class="sxs-lookup"><span data-stu-id="28afb-105">Definition</span></span>

``` syntax
<xs:element name="GroupNode" type="GroupNodeType" />
```

## <a name="parent-elements"></a><span data-ttu-id="28afb-106">Родительские элементы</span><span class="sxs-lookup"><span data-stu-id="28afb-106">Parent Elements</span></span>

[<span data-ttu-id="28afb-107">**Содержани**</span><span class="sxs-lookup"><span data-stu-id="28afb-107">**Content**</span></span>](content-element--journal-reader.md)

## <a name="child-elements"></a><span data-ttu-id="28afb-108">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="28afb-108">Child Elements</span></span>

[<span data-ttu-id="28afb-109">**Paragraph**</span><span class="sxs-lookup"><span data-stu-id="28afb-109">**Paragraph**</span></span>](paragraph-element.md)

[<span data-ttu-id="28afb-110">**инкворд**</span><span class="sxs-lookup"><span data-stu-id="28afb-110">**InkWord**</span></span>](inkword-element.md)

[<span data-ttu-id="28afb-111">**Рисование**</span><span class="sxs-lookup"><span data-stu-id="28afb-111">**Drawing**</span></span>](drawing-element.md)

[<span data-ttu-id="28afb-112">**Полнотекстовым**</span><span class="sxs-lookup"><span data-stu-id="28afb-112">**Text**</span></span>](text-element.md)

[<span data-ttu-id="28afb-113">**Образ**</span><span class="sxs-lookup"><span data-stu-id="28afb-113">**Image**</span></span>](docimage-element.md)

[<span data-ttu-id="28afb-114">**Flag**</span><span class="sxs-lookup"><span data-stu-id="28afb-114">**Flag**</span></span>](flag-element.md)

## <a name="attributes"></a><span data-ttu-id="28afb-115">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="28afb-115">Attributes</span></span>



| <span data-ttu-id="28afb-116">attribute</span><span class="sxs-lookup"><span data-stu-id="28afb-116">Attribute</span></span>  | <span data-ttu-id="28afb-117">Тип</span><span class="sxs-lookup"><span data-stu-id="28afb-117">Type</span></span>                      | <span data-ttu-id="28afb-118">Обязательно</span><span class="sxs-lookup"><span data-stu-id="28afb-118">Required</span></span> | <span data-ttu-id="28afb-119">Описание</span><span class="sxs-lookup"><span data-stu-id="28afb-119">Description</span></span>                                                                             | <span data-ttu-id="28afb-120">Возможные значения</span><span class="sxs-lookup"><span data-stu-id="28afb-120">Possible Values</span></span>           |
|------------|---------------------------|----------|-----------------------------------------------------------------------------------------|---------------------------|
| <span data-ttu-id="28afb-121">**Слева**</span><span class="sxs-lookup"><span data-stu-id="28afb-121">**Left**</span></span>   | <span data-ttu-id="28afb-122">**xs:integer**</span><span class="sxs-lookup"><span data-stu-id="28afb-122">**xs:integer**</span></span>            | <span data-ttu-id="28afb-123">Обязательно</span><span class="sxs-lookup"><span data-stu-id="28afb-123">Required</span></span> | <span data-ttu-id="28afb-124">Расстояние от начала до крайней левой точки в ограничивающем прямоугольнике для элемента.</span><span class="sxs-lookup"><span data-stu-id="28afb-124">The distance from the origin to the leftmost point in the bounding box for the element.</span></span> | <span data-ttu-id="28afb-125">Любое целое число.</span><span class="sxs-lookup"><span data-stu-id="28afb-125">Any integer.</span></span>              |
| <span data-ttu-id="28afb-126">**Top**</span><span class="sxs-lookup"><span data-stu-id="28afb-126">**Top**</span></span>    | <span data-ttu-id="28afb-127">**xs:integer**</span><span class="sxs-lookup"><span data-stu-id="28afb-127">**xs:integer**</span></span>            | <span data-ttu-id="28afb-128">Обязательно</span><span class="sxs-lookup"><span data-stu-id="28afb-128">Required</span></span> | <span data-ttu-id="28afb-129">Расстояние от начала до самой верхней точки ограничивающего прямоугольника для элемента.</span><span class="sxs-lookup"><span data-stu-id="28afb-129">The distance from the origin to the topmost point in the bounding box for the element.</span></span>  | <span data-ttu-id="28afb-130">Любое целое число.</span><span class="sxs-lookup"><span data-stu-id="28afb-130">Any integer.</span></span>              |
| <span data-ttu-id="28afb-131">**Width**</span><span class="sxs-lookup"><span data-stu-id="28afb-131">**Width**</span></span>  | <span data-ttu-id="28afb-132">**xs:nonNegativeInteger**</span><span class="sxs-lookup"><span data-stu-id="28afb-132">**xs:nonNegativeInteger**</span></span> | <span data-ttu-id="28afb-133">Обязательно</span><span class="sxs-lookup"><span data-stu-id="28afb-133">Required</span></span> | <span data-ttu-id="28afb-134">Ширина ограничивающего прямоугольника для элемента.</span><span class="sxs-lookup"><span data-stu-id="28afb-134">The width of the bounding box for the element.</span></span>                                          | <span data-ttu-id="28afb-135">Любое неотрицательное целое число.</span><span class="sxs-lookup"><span data-stu-id="28afb-135">Any non-negative integer.</span></span> |
| <span data-ttu-id="28afb-136">**Height**</span><span class="sxs-lookup"><span data-stu-id="28afb-136">**Height**</span></span> | <span data-ttu-id="28afb-137">**xs:nonNegativeInteger**</span><span class="sxs-lookup"><span data-stu-id="28afb-137">**xs:nonNegativeInteger**</span></span> | <span data-ttu-id="28afb-138">Обязательно</span><span class="sxs-lookup"><span data-stu-id="28afb-138">Required</span></span> | <span data-ttu-id="28afb-139">Высота ограничивающего прямоугольника для элемента.</span><span class="sxs-lookup"><span data-stu-id="28afb-139">The height of the bounding box for the element.</span></span>                                         | <span data-ttu-id="28afb-140">Любое неотрицательное целое число.</span><span class="sxs-lookup"><span data-stu-id="28afb-140">Any non-negative integer.</span></span> |



 

## <a name="element-information"></a><span data-ttu-id="28afb-141">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="28afb-141">Element Information</span></span>



|              |                                                                 |
|--------------|-----------------------------------------------------------------|
| <span data-ttu-id="28afb-142">Тип элемента</span><span class="sxs-lookup"><span data-stu-id="28afb-142">Element type</span></span> | <span data-ttu-id="28afb-143">[**Граупнодетипе**](groupnodetype-complex-type.md) complexType</span><span class="sxs-lookup"><span data-stu-id="28afb-143">[**GroupNodeType**](groupnodetype-complex-type.md) complexType</span></span> |
| <span data-ttu-id="28afb-144">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="28afb-144">Namespace</span></span>    | <span data-ttu-id="28afb-145">urn: schemas-microsoft-com: TabletPC: ричинк</span><span class="sxs-lookup"><span data-stu-id="28afb-145">urn:schemas-microsoft-com:tabletpc:richink</span></span>                      |
| <span data-ttu-id="28afb-146">Имя схемы</span><span class="sxs-lookup"><span data-stu-id="28afb-146">Schema name</span></span>  | <span data-ttu-id="28afb-147">Средство чтения журнала</span><span class="sxs-lookup"><span data-stu-id="28afb-147">Journal Reader</span></span>                                                  |



 

 

 



