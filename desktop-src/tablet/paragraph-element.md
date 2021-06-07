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
ms.openlocfilehash: 2f246294c80814ec809c0a1ca035fcb4741c30c5
ms.sourcegitcommit: c3f669dc1d52278432bf75ad9fddba3257d26aa2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/04/2021
ms.locfileid: "111432236"
---
# <a name="paragraph-element"></a><span data-ttu-id="a2858-103">Элемент абзаца</span><span class="sxs-lookup"><span data-stu-id="a2858-103">Paragraph Element</span></span>

<span data-ttu-id="a2858-104">Содержит абзац.</span><span class="sxs-lookup"><span data-stu-id="a2858-104">Contains a paragraph.</span></span>

## <a name="definition"></a><span data-ttu-id="a2858-105">Определение</span><span class="sxs-lookup"><span data-stu-id="a2858-105">Definition</span></span>

``` syntax
<xs:element name="Paragraph" type="ParagraphType" minOccurs="0" maxOccurs="unbounded" />
```

## <a name="parent-elements"></a><span data-ttu-id="a2858-106">Родительские элементы</span><span class="sxs-lookup"><span data-stu-id="a2858-106">Parent Elements</span></span>

[<span data-ttu-id="a2858-107">**Содержани**</span><span class="sxs-lookup"><span data-stu-id="a2858-107">**Content**</span></span>](content-element--journal-reader.md)

[<span data-ttu-id="a2858-108">**граупноде**</span><span class="sxs-lookup"><span data-stu-id="a2858-108">**GroupNode**</span></span>](groupnode-element.md)

## <a name="child-elements"></a><span data-ttu-id="a2858-109">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="a2858-109">Child Elements</span></span>

[<span data-ttu-id="a2858-110">**Штрих**</span><span class="sxs-lookup"><span data-stu-id="a2858-110">**Line**</span></span>](line-element.md)

[<span data-ttu-id="a2858-111">**параграфлинеметрикс**</span><span class="sxs-lookup"><span data-stu-id="a2858-111">**ParagraphLineMetrics**</span></span>](paragraphlinemetrics-element.md)

## <a name="attributes"></a><span data-ttu-id="a2858-112">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="a2858-112">Attributes</span></span>



| <span data-ttu-id="a2858-113">attribute</span><span class="sxs-lookup"><span data-stu-id="a2858-113">Attribute</span></span>       | <span data-ttu-id="a2858-114">Тип</span><span class="sxs-lookup"><span data-stu-id="a2858-114">Type</span></span>                      | <span data-ttu-id="a2858-115">Обязательно</span><span class="sxs-lookup"><span data-stu-id="a2858-115">Required</span></span> | <span data-ttu-id="a2858-116">Описание</span><span class="sxs-lookup"><span data-stu-id="a2858-116">Description</span></span>                                                                             | <span data-ttu-id="a2858-117">Возможные значения</span><span class="sxs-lookup"><span data-stu-id="a2858-117">Possible Values</span></span>           |
|-----------------|---------------------------|----------|-----------------------------------------------------------------------------------------|---------------------------|
| <span data-ttu-id="a2858-118">**Слева**</span><span class="sxs-lookup"><span data-stu-id="a2858-118">**Left**</span></span>        | <span data-ttu-id="a2858-119">**xs:integer**</span><span class="sxs-lookup"><span data-stu-id="a2858-119">**xs:integer**</span></span>            | <span data-ttu-id="a2858-120">Обязательно</span><span class="sxs-lookup"><span data-stu-id="a2858-120">Required</span></span> | <span data-ttu-id="a2858-121">Расстояние от начала до крайней левой точки в ограничивающем прямоугольнике для элемента.</span><span class="sxs-lookup"><span data-stu-id="a2858-121">The distance from the origin to the leftmost point in the bounding box for the element.</span></span> | <span data-ttu-id="a2858-122">Любое целое число.</span><span class="sxs-lookup"><span data-stu-id="a2858-122">Any integer.</span></span>              |
| <span data-ttu-id="a2858-123">**Top**</span><span class="sxs-lookup"><span data-stu-id="a2858-123">**Top**</span></span>         | <span data-ttu-id="a2858-124">**xs:integer**</span><span class="sxs-lookup"><span data-stu-id="a2858-124">**xs:integer**</span></span>            | <span data-ttu-id="a2858-125">Обязательно</span><span class="sxs-lookup"><span data-stu-id="a2858-125">Required</span></span> | <span data-ttu-id="a2858-126">Расстояние от начала до самой верхней точки ограничивающего прямоугольника для элемента.</span><span class="sxs-lookup"><span data-stu-id="a2858-126">The distance from the origin to the topmost point in the bounding box for the element.</span></span>  | <span data-ttu-id="a2858-127">Любое целое число.</span><span class="sxs-lookup"><span data-stu-id="a2858-127">Any integer.</span></span>              |
| <span data-ttu-id="a2858-128">**Width**</span><span class="sxs-lookup"><span data-stu-id="a2858-128">**Width**</span></span>       | <span data-ttu-id="a2858-129">**xs:nonNegativeInteger**</span><span class="sxs-lookup"><span data-stu-id="a2858-129">**xs:nonNegativeInteger**</span></span> | <span data-ttu-id="a2858-130">Обязательно</span><span class="sxs-lookup"><span data-stu-id="a2858-130">Required</span></span> | <span data-ttu-id="a2858-131">Ширина ограничивающего прямоугольника для элемента.</span><span class="sxs-lookup"><span data-stu-id="a2858-131">The width of the bounding box for the element.</span></span>                                          | <span data-ttu-id="a2858-132">Любое неотрицательное целое число.</span><span class="sxs-lookup"><span data-stu-id="a2858-132">Any non-negative integer.</span></span> |
| <span data-ttu-id="a2858-133">**Height**</span><span class="sxs-lookup"><span data-stu-id="a2858-133">**Height**</span></span>      | <span data-ttu-id="a2858-134">**xs:nonNegativeInteger**</span><span class="sxs-lookup"><span data-stu-id="a2858-134">**xs:nonNegativeInteger**</span></span> | <span data-ttu-id="a2858-135">Обязательно</span><span class="sxs-lookup"><span data-stu-id="a2858-135">Required</span></span> | <span data-ttu-id="a2858-136">Высота ограничивающего прямоугольника для элемента.</span><span class="sxs-lookup"><span data-stu-id="a2858-136">The height of the bounding box for the element.</span></span>                                         | <span data-ttu-id="a2858-137">Любое неотрицательное целое число.</span><span class="sxs-lookup"><span data-stu-id="a2858-137">Any non-negative integer.</span></span> |
| <span data-ttu-id="a2858-138">**BlockNumber**</span><span class="sxs-lookup"><span data-stu-id="a2858-138">**BlockNumber**</span></span> | <span data-ttu-id="a2858-139">**xs:nonNegativeInteger**</span><span class="sxs-lookup"><span data-stu-id="a2858-139">**xs:nonNegativeInteger**</span></span> | <span data-ttu-id="a2858-140">Обязательно</span><span class="sxs-lookup"><span data-stu-id="a2858-140">Required</span></span> | <span data-ttu-id="a2858-141">Номер блока.</span><span class="sxs-lookup"><span data-stu-id="a2858-141">Block number.</span></span>                                                                           | <span data-ttu-id="a2858-142">Любое неотрицательное целое число.</span><span class="sxs-lookup"><span data-stu-id="a2858-142">Any non-negative integer.</span></span> |
| <span data-ttu-id="a2858-143">**LineNumber**</span><span class="sxs-lookup"><span data-stu-id="a2858-143">**LineNumber**</span></span>  | <span data-ttu-id="a2858-144">**xs:nonNegativeInteger**</span><span class="sxs-lookup"><span data-stu-id="a2858-144">**xs:nonNegativeInteger**</span></span> | <span data-ttu-id="a2858-145">Обязательно</span><span class="sxs-lookup"><span data-stu-id="a2858-145">Required</span></span> | <span data-ttu-id="a2858-146">Строка, с которой начинается абзац.</span><span class="sxs-lookup"><span data-stu-id="a2858-146">The line on which the paragraph begins.</span></span>                                                 | <span data-ttu-id="a2858-147">Любое неотрицательное целое число.</span><span class="sxs-lookup"><span data-stu-id="a2858-147">Any non-negative integer.</span></span> |



 

## <a name="element-information"></a><span data-ttu-id="a2858-148">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="a2858-148">Element Information</span></span>



|  <span data-ttu-id="a2858-149">Элемент</span><span class="sxs-lookup"><span data-stu-id="a2858-149">Element</span></span>     | <span data-ttu-id="a2858-150">Значение</span><span class="sxs-lookup"><span data-stu-id="a2858-150">Value</span></span>                                                     |
|--------------|-----------------------------------------------------------------|
| <span data-ttu-id="a2858-151">Тип элемента</span><span class="sxs-lookup"><span data-stu-id="a2858-151">Element type</span></span> | <span data-ttu-id="a2858-152">[**Параграфтипе**](paragraphtype-complex-type.md) complexType</span><span class="sxs-lookup"><span data-stu-id="a2858-152">[**ParagraphType**](paragraphtype-complex-type.md) complexType</span></span> |
| <span data-ttu-id="a2858-153">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="a2858-153">Namespace</span></span>    | <span data-ttu-id="a2858-154">urn: schemas-microsoft-com: TabletPC: ричинк</span><span class="sxs-lookup"><span data-stu-id="a2858-154">urn:schemas-microsoft-com:tabletpc:richink</span></span>                      |
| <span data-ttu-id="a2858-155">Имя схемы</span><span class="sxs-lookup"><span data-stu-id="a2858-155">Schema name</span></span>  | <span data-ttu-id="a2858-156">Средство чтения журнала</span><span class="sxs-lookup"><span data-stu-id="a2858-156">Journal Reader</span></span>                                                  |



 

## <a name="requirements"></a><span data-ttu-id="a2858-157">Требования</span><span class="sxs-lookup"><span data-stu-id="a2858-157">Requirements</span></span>



| <span data-ttu-id="a2858-158">Требование</span><span class="sxs-lookup"><span data-stu-id="a2858-158">Requirement</span></span> | <span data-ttu-id="a2858-159">Значение</span><span class="sxs-lookup"><span data-stu-id="a2858-159">Value</span></span> |
|-------------------|--------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a2858-160">Заголовок</span><span class="sxs-lookup"><span data-stu-id="a2858-160">Header</span></span><br/> | <dl> <span data-ttu-id="a2858-161"><dt>Windows.ui.xaml.docументс. h</dt></span><span class="sxs-lookup"><span data-stu-id="a2858-161"><dt>Windows.ui.xaml.documents.h</dt></span></span> </dl> |



 

 




