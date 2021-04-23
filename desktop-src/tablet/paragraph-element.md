---
description: Содержит абзац.
ms.assetid: 60322907-3902-49a9-91a9-e00b0a714c00
title: Элемент абзаца (Windows.ui.xaml.docументс. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Paragraph
api_type:
- HeaderDef
api_location:
- windows.ui.xaml.documents.h
ms.openlocfilehash: bfe3752541bb54571e9802f557e83dcc7632f845
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105656879"
---
# <a name="paragraph-element"></a><span data-ttu-id="69559-103">Элемент абзаца</span><span class="sxs-lookup"><span data-stu-id="69559-103">Paragraph Element</span></span>

<span data-ttu-id="69559-104">Содержит абзац.</span><span class="sxs-lookup"><span data-stu-id="69559-104">Contains a paragraph.</span></span>

## <a name="definition"></a><span data-ttu-id="69559-105">Определение</span><span class="sxs-lookup"><span data-stu-id="69559-105">Definition</span></span>

``` syntax
<xs:element name="Paragraph" type="ParagraphType" minOccurs="0" maxOccurs="unbounded" />
```

## <a name="parent-elements"></a><span data-ttu-id="69559-106">Родительские элементы</span><span class="sxs-lookup"><span data-stu-id="69559-106">Parent Elements</span></span>

[<span data-ttu-id="69559-107">**Содержани**</span><span class="sxs-lookup"><span data-stu-id="69559-107">**Content**</span></span>](content-element--journal-reader.md)

[<span data-ttu-id="69559-108">**граупноде**</span><span class="sxs-lookup"><span data-stu-id="69559-108">**GroupNode**</span></span>](groupnode-element.md)

## <a name="child-elements"></a><span data-ttu-id="69559-109">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="69559-109">Child Elements</span></span>

[<span data-ttu-id="69559-110">**Штрих**</span><span class="sxs-lookup"><span data-stu-id="69559-110">**Line**</span></span>](line-element.md)

[<span data-ttu-id="69559-111">**параграфлинеметрикс**</span><span class="sxs-lookup"><span data-stu-id="69559-111">**ParagraphLineMetrics**</span></span>](paragraphlinemetrics-element.md)

## <a name="attributes"></a><span data-ttu-id="69559-112">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="69559-112">Attributes</span></span>



| <span data-ttu-id="69559-113">attribute</span><span class="sxs-lookup"><span data-stu-id="69559-113">Attribute</span></span>       | <span data-ttu-id="69559-114">Тип</span><span class="sxs-lookup"><span data-stu-id="69559-114">Type</span></span>                      | <span data-ttu-id="69559-115">Обязательно</span><span class="sxs-lookup"><span data-stu-id="69559-115">Required</span></span> | <span data-ttu-id="69559-116">Описание</span><span class="sxs-lookup"><span data-stu-id="69559-116">Description</span></span>                                                                             | <span data-ttu-id="69559-117">Возможные значения</span><span class="sxs-lookup"><span data-stu-id="69559-117">Possible Values</span></span>           |
|-----------------|---------------------------|----------|-----------------------------------------------------------------------------------------|---------------------------|
| <span data-ttu-id="69559-118">**Слева**</span><span class="sxs-lookup"><span data-stu-id="69559-118">**Left**</span></span>        | <span data-ttu-id="69559-119">**xs:integer**</span><span class="sxs-lookup"><span data-stu-id="69559-119">**xs:integer**</span></span>            | <span data-ttu-id="69559-120">Обязательно</span><span class="sxs-lookup"><span data-stu-id="69559-120">Required</span></span> | <span data-ttu-id="69559-121">Расстояние от начала до крайней левой точки в ограничивающем прямоугольнике для элемента.</span><span class="sxs-lookup"><span data-stu-id="69559-121">The distance from the origin to the leftmost point in the bounding box for the element.</span></span> | <span data-ttu-id="69559-122">Любое целое число.</span><span class="sxs-lookup"><span data-stu-id="69559-122">Any integer.</span></span>              |
| <span data-ttu-id="69559-123">**Top**</span><span class="sxs-lookup"><span data-stu-id="69559-123">**Top**</span></span>         | <span data-ttu-id="69559-124">**xs:integer**</span><span class="sxs-lookup"><span data-stu-id="69559-124">**xs:integer**</span></span>            | <span data-ttu-id="69559-125">Обязательно</span><span class="sxs-lookup"><span data-stu-id="69559-125">Required</span></span> | <span data-ttu-id="69559-126">Расстояние от начала до самой верхней точки ограничивающего прямоугольника для элемента.</span><span class="sxs-lookup"><span data-stu-id="69559-126">The distance from the origin to the topmost point in the bounding box for the element.</span></span>  | <span data-ttu-id="69559-127">Любое целое число.</span><span class="sxs-lookup"><span data-stu-id="69559-127">Any integer.</span></span>              |
| <span data-ttu-id="69559-128">**Width**</span><span class="sxs-lookup"><span data-stu-id="69559-128">**Width**</span></span>       | <span data-ttu-id="69559-129">**xs:nonNegativeInteger**</span><span class="sxs-lookup"><span data-stu-id="69559-129">**xs:nonNegativeInteger**</span></span> | <span data-ttu-id="69559-130">Обязательно</span><span class="sxs-lookup"><span data-stu-id="69559-130">Required</span></span> | <span data-ttu-id="69559-131">Ширина ограничивающего прямоугольника для элемента.</span><span class="sxs-lookup"><span data-stu-id="69559-131">The width of the bounding box for the element.</span></span>                                          | <span data-ttu-id="69559-132">Любое неотрицательное целое число.</span><span class="sxs-lookup"><span data-stu-id="69559-132">Any non-negative integer.</span></span> |
| <span data-ttu-id="69559-133">**Height**</span><span class="sxs-lookup"><span data-stu-id="69559-133">**Height**</span></span>      | <span data-ttu-id="69559-134">**xs:nonNegativeInteger**</span><span class="sxs-lookup"><span data-stu-id="69559-134">**xs:nonNegativeInteger**</span></span> | <span data-ttu-id="69559-135">Обязательно</span><span class="sxs-lookup"><span data-stu-id="69559-135">Required</span></span> | <span data-ttu-id="69559-136">Высота ограничивающего прямоугольника для элемента.</span><span class="sxs-lookup"><span data-stu-id="69559-136">The height of the bounding box for the element.</span></span>                                         | <span data-ttu-id="69559-137">Любое неотрицательное целое число.</span><span class="sxs-lookup"><span data-stu-id="69559-137">Any non-negative integer.</span></span> |
| <span data-ttu-id="69559-138">**блоккнумбер**</span><span class="sxs-lookup"><span data-stu-id="69559-138">**BlockNumber**</span></span> | <span data-ttu-id="69559-139">**xs:nonNegativeInteger**</span><span class="sxs-lookup"><span data-stu-id="69559-139">**xs:nonNegativeInteger**</span></span> | <span data-ttu-id="69559-140">Обязательно</span><span class="sxs-lookup"><span data-stu-id="69559-140">Required</span></span> | <span data-ttu-id="69559-141">Номер блока.</span><span class="sxs-lookup"><span data-stu-id="69559-141">Block number.</span></span>                                                                           | <span data-ttu-id="69559-142">Любое неотрицательное целое число.</span><span class="sxs-lookup"><span data-stu-id="69559-142">Any non-negative integer.</span></span> |
| <span data-ttu-id="69559-143">**LineNumber**</span><span class="sxs-lookup"><span data-stu-id="69559-143">**LineNumber**</span></span>  | <span data-ttu-id="69559-144">**xs:nonNegativeInteger**</span><span class="sxs-lookup"><span data-stu-id="69559-144">**xs:nonNegativeInteger**</span></span> | <span data-ttu-id="69559-145">Обязательно</span><span class="sxs-lookup"><span data-stu-id="69559-145">Required</span></span> | <span data-ttu-id="69559-146">Строка, с которой начинается абзац.</span><span class="sxs-lookup"><span data-stu-id="69559-146">The line on which the paragraph begins.</span></span>                                                 | <span data-ttu-id="69559-147">Любое неотрицательное целое число.</span><span class="sxs-lookup"><span data-stu-id="69559-147">Any non-negative integer.</span></span> |



 

## <a name="element-information"></a><span data-ttu-id="69559-148">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="69559-148">Element Information</span></span>



|              |                                                                 |
|--------------|-----------------------------------------------------------------|
| <span data-ttu-id="69559-149">Тип элемента</span><span class="sxs-lookup"><span data-stu-id="69559-149">Element type</span></span> | <span data-ttu-id="69559-150">[**Параграфтипе**](paragraphtype-complex-type.md) complexType</span><span class="sxs-lookup"><span data-stu-id="69559-150">[**ParagraphType**](paragraphtype-complex-type.md) complexType</span></span> |
| <span data-ttu-id="69559-151">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="69559-151">Namespace</span></span>    | <span data-ttu-id="69559-152">urn: schemas-microsoft-com: TabletPC: ричинк</span><span class="sxs-lookup"><span data-stu-id="69559-152">urn:schemas-microsoft-com:tabletpc:richink</span></span>                      |
| <span data-ttu-id="69559-153">Имя схемы</span><span class="sxs-lookup"><span data-stu-id="69559-153">Schema name</span></span>  | <span data-ttu-id="69559-154">Средство чтения журнала</span><span class="sxs-lookup"><span data-stu-id="69559-154">Journal Reader</span></span>                                                  |



 

## <a name="requirements"></a><span data-ttu-id="69559-155">Требования</span><span class="sxs-lookup"><span data-stu-id="69559-155">Requirements</span></span>



| <span data-ttu-id="69559-156">Требование</span><span class="sxs-lookup"><span data-stu-id="69559-156">Requirement</span></span> | <span data-ttu-id="69559-157">Значение</span><span class="sxs-lookup"><span data-stu-id="69559-157">Value</span></span> |
|-------------------|--------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="69559-158">Header</span><span class="sxs-lookup"><span data-stu-id="69559-158">Header</span></span><br/> | <dl> <span data-ttu-id="69559-159"><dt>Windows.ui.xaml.docументс. h</dt></span><span class="sxs-lookup"><span data-stu-id="69559-159"><dt>Windows.ui.xaml.documents.h</dt></span></span> </dl> |



 

 




