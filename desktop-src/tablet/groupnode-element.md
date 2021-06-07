---
description: Содержит набор элементов&\# 8212; Абзац, Инкворд, Drawing, Text, Image или Flag&\# 8212;, которые группируются вместе в заметке журнала.
ms.assetid: 59ee3037-7178-41c8-84d5-d5c68fa2cf9b
title: Граупноде, элемент
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cbc4d39a592b5b6328bd31ff37761cfd3f0138c0
ms.sourcegitcommit: c3f669dc1d52278432bf75ad9fddba3257d26aa2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/04/2021
ms.locfileid: "111432575"
---
# <a name="groupnode-element"></a><span data-ttu-id="46a43-103">Граупноде, элемент</span><span class="sxs-lookup"><span data-stu-id="46a43-103">GroupNode Element</span></span>

<span data-ttu-id="46a43-104">Содержит набор элементов ([**абзац**](paragraph-element.md), [**инкворд**](inkword-element.md), [**Рисование**](drawing-element.md), [**текст**](text-element.md), [**изображение**](image-element.md)или [**флаг**](flag-element.md)), которые группируются в заметке журнала.</span><span class="sxs-lookup"><span data-stu-id="46a43-104">Contains a set of elements—[**Paragraph**](paragraph-element.md), [**InkWord**](inkword-element.md), [**Drawing**](drawing-element.md), [**Text**](text-element.md), [**Image**](image-element.md), or [**Flag**](flag-element.md)—that are grouped together in the Journal note.</span></span>

## <a name="definition"></a><span data-ttu-id="46a43-105">Определение</span><span class="sxs-lookup"><span data-stu-id="46a43-105">Definition</span></span>

``` syntax
<xs:element name="GroupNode" type="GroupNodeType" />
```

## <a name="parent-elements"></a><span data-ttu-id="46a43-106">Родительские элементы</span><span class="sxs-lookup"><span data-stu-id="46a43-106">Parent Elements</span></span>

[<span data-ttu-id="46a43-107">**Содержани**</span><span class="sxs-lookup"><span data-stu-id="46a43-107">**Content**</span></span>](content-element--journal-reader.md)

## <a name="child-elements"></a><span data-ttu-id="46a43-108">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="46a43-108">Child Elements</span></span>

[<span data-ttu-id="46a43-109">**Paragraph**</span><span class="sxs-lookup"><span data-stu-id="46a43-109">**Paragraph**</span></span>](paragraph-element.md)

[<span data-ttu-id="46a43-110">**инкворд**</span><span class="sxs-lookup"><span data-stu-id="46a43-110">**InkWord**</span></span>](inkword-element.md)

[<span data-ttu-id="46a43-111">**Рисование**</span><span class="sxs-lookup"><span data-stu-id="46a43-111">**Drawing**</span></span>](drawing-element.md)

[<span data-ttu-id="46a43-112">**Полнотекстовым**</span><span class="sxs-lookup"><span data-stu-id="46a43-112">**Text**</span></span>](text-element.md)

[<span data-ttu-id="46a43-113">**Изображение**</span><span class="sxs-lookup"><span data-stu-id="46a43-113">**Image**</span></span>](docimage-element.md)

[<span data-ttu-id="46a43-114">**Flag**</span><span class="sxs-lookup"><span data-stu-id="46a43-114">**Flag**</span></span>](flag-element.md)

## <a name="attributes"></a><span data-ttu-id="46a43-115">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="46a43-115">Attributes</span></span>



| <span data-ttu-id="46a43-116">attribute</span><span class="sxs-lookup"><span data-stu-id="46a43-116">Attribute</span></span>  | <span data-ttu-id="46a43-117">Тип</span><span class="sxs-lookup"><span data-stu-id="46a43-117">Type</span></span>                      | <span data-ttu-id="46a43-118">Обязательно</span><span class="sxs-lookup"><span data-stu-id="46a43-118">Required</span></span> | <span data-ttu-id="46a43-119">Описание</span><span class="sxs-lookup"><span data-stu-id="46a43-119">Description</span></span>                                                                             | <span data-ttu-id="46a43-120">Возможные значения</span><span class="sxs-lookup"><span data-stu-id="46a43-120">Possible Values</span></span>           |
|------------|---------------------------|----------|-----------------------------------------------------------------------------------------|---------------------------|
| <span data-ttu-id="46a43-121">**Слева**</span><span class="sxs-lookup"><span data-stu-id="46a43-121">**Left**</span></span>   | <span data-ttu-id="46a43-122">**xs:integer**</span><span class="sxs-lookup"><span data-stu-id="46a43-122">**xs:integer**</span></span>            | <span data-ttu-id="46a43-123">Обязательно</span><span class="sxs-lookup"><span data-stu-id="46a43-123">Required</span></span> | <span data-ttu-id="46a43-124">Расстояние от начала до крайней левой точки в ограничивающем прямоугольнике для элемента.</span><span class="sxs-lookup"><span data-stu-id="46a43-124">The distance from the origin to the leftmost point in the bounding box for the element.</span></span> | <span data-ttu-id="46a43-125">Любое целое число.</span><span class="sxs-lookup"><span data-stu-id="46a43-125">Any integer.</span></span>              |
| <span data-ttu-id="46a43-126">**Top**</span><span class="sxs-lookup"><span data-stu-id="46a43-126">**Top**</span></span>    | <span data-ttu-id="46a43-127">**xs:integer**</span><span class="sxs-lookup"><span data-stu-id="46a43-127">**xs:integer**</span></span>            | <span data-ttu-id="46a43-128">Обязательно</span><span class="sxs-lookup"><span data-stu-id="46a43-128">Required</span></span> | <span data-ttu-id="46a43-129">Расстояние от начала до самой верхней точки ограничивающего прямоугольника для элемента.</span><span class="sxs-lookup"><span data-stu-id="46a43-129">The distance from the origin to the topmost point in the bounding box for the element.</span></span>  | <span data-ttu-id="46a43-130">Любое целое число.</span><span class="sxs-lookup"><span data-stu-id="46a43-130">Any integer.</span></span>              |
| <span data-ttu-id="46a43-131">**Width**</span><span class="sxs-lookup"><span data-stu-id="46a43-131">**Width**</span></span>  | <span data-ttu-id="46a43-132">**xs:nonNegativeInteger**</span><span class="sxs-lookup"><span data-stu-id="46a43-132">**xs:nonNegativeInteger**</span></span> | <span data-ttu-id="46a43-133">Обязательно</span><span class="sxs-lookup"><span data-stu-id="46a43-133">Required</span></span> | <span data-ttu-id="46a43-134">Ширина ограничивающего прямоугольника для элемента.</span><span class="sxs-lookup"><span data-stu-id="46a43-134">The width of the bounding box for the element.</span></span>                                          | <span data-ttu-id="46a43-135">Любое неотрицательное целое число.</span><span class="sxs-lookup"><span data-stu-id="46a43-135">Any non-negative integer.</span></span> |
| <span data-ttu-id="46a43-136">**Height**</span><span class="sxs-lookup"><span data-stu-id="46a43-136">**Height**</span></span> | <span data-ttu-id="46a43-137">**xs:nonNegativeInteger**</span><span class="sxs-lookup"><span data-stu-id="46a43-137">**xs:nonNegativeInteger**</span></span> | <span data-ttu-id="46a43-138">Обязательно</span><span class="sxs-lookup"><span data-stu-id="46a43-138">Required</span></span> | <span data-ttu-id="46a43-139">Высота ограничивающего прямоугольника для элемента.</span><span class="sxs-lookup"><span data-stu-id="46a43-139">The height of the bounding box for the element.</span></span>                                         | <span data-ttu-id="46a43-140">Любое неотрицательное целое число.</span><span class="sxs-lookup"><span data-stu-id="46a43-140">Any non-negative integer.</span></span> |



 

## <a name="element-information"></a><span data-ttu-id="46a43-141">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="46a43-141">Element Information</span></span>



|  <span data-ttu-id="46a43-142">Элемент</span><span class="sxs-lookup"><span data-stu-id="46a43-142">Element</span></span>     | <span data-ttu-id="46a43-143">Значение</span><span class="sxs-lookup"><span data-stu-id="46a43-143">Value</span></span>                                                     |
|--------------|-----------------------------------------------------------------|
| <span data-ttu-id="46a43-144">Тип элемента</span><span class="sxs-lookup"><span data-stu-id="46a43-144">Element type</span></span> | <span data-ttu-id="46a43-145">[**Граупнодетипе**](groupnodetype-complex-type.md) complexType</span><span class="sxs-lookup"><span data-stu-id="46a43-145">[**GroupNodeType**](groupnodetype-complex-type.md) complexType</span></span> |
| <span data-ttu-id="46a43-146">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="46a43-146">Namespace</span></span>    | <span data-ttu-id="46a43-147">urn: schemas-microsoft-com: TabletPC: ричинк</span><span class="sxs-lookup"><span data-stu-id="46a43-147">urn:schemas-microsoft-com:tabletpc:richink</span></span>                      |
| <span data-ttu-id="46a43-148">Имя схемы</span><span class="sxs-lookup"><span data-stu-id="46a43-148">Schema name</span></span>  | <span data-ttu-id="46a43-149">Средство чтения журнала</span><span class="sxs-lookup"><span data-stu-id="46a43-149">Journal Reader</span></span>                                                  |



 

 

 



