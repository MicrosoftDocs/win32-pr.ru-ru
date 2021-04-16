---
description: Содержит закодированные двоичные данные для изображения в документе журнала, если оно есть.
ms.assetid: fbb86bef-68f7-4aad-8a98-1c68e79ea2de
title: Элемент Image
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8437495a4c248a8e5bc68a0f7b75a2cf7d761387
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105693284"
---
# <a name="image-element"></a><span data-ttu-id="a382b-103">Элемент Image</span><span class="sxs-lookup"><span data-stu-id="a382b-103">Image Element</span></span>

<span data-ttu-id="a382b-104">Содержит закодированные двоичные данные для изображения в документе журнала, если оно есть.</span><span class="sxs-lookup"><span data-stu-id="a382b-104">Contains encoded binary data for an image in the Journal document, if present.</span></span>

## <a name="definition"></a><span data-ttu-id="a382b-105">Определение</span><span class="sxs-lookup"><span data-stu-id="a382b-105">Definition</span></span>

``` syntax
 Copy Code<xs:element name="Image" type="ImageType" />
```

## <a name="parent-elements"></a><span data-ttu-id="a382b-106">Родительские элементы</span><span class="sxs-lookup"><span data-stu-id="a382b-106">Parent Elements</span></span>

[<span data-ttu-id="a382b-107">**Содержани**</span><span class="sxs-lookup"><span data-stu-id="a382b-107">**Content**</span></span>](content-element--journal-reader.md)

[<span data-ttu-id="a382b-108">**граупноде**</span><span class="sxs-lookup"><span data-stu-id="a382b-108">**GroupNode**</span></span>](groupnode-element.md)

## <a name="child-elements"></a><span data-ttu-id="a382b-109">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="a382b-109">Child Elements</span></span>

<span data-ttu-id="a382b-110">Отсутствует.</span><span class="sxs-lookup"><span data-stu-id="a382b-110">None.</span></span>

## <a name="attributes"></a><span data-ttu-id="a382b-111">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="a382b-111">Attributes</span></span>



| <span data-ttu-id="a382b-112">attribute</span><span class="sxs-lookup"><span data-stu-id="a382b-112">Attribute</span></span>  | <span data-ttu-id="a382b-113">Тип</span><span class="sxs-lookup"><span data-stu-id="a382b-113">Type</span></span>                      | <span data-ttu-id="a382b-114">Обязательно</span><span class="sxs-lookup"><span data-stu-id="a382b-114">Required</span></span> | <span data-ttu-id="a382b-115">Описание</span><span class="sxs-lookup"><span data-stu-id="a382b-115">Description</span></span>                                                                             | <span data-ttu-id="a382b-116">Возможные значения</span><span class="sxs-lookup"><span data-stu-id="a382b-116">Possible Values</span></span>           |
|------------|---------------------------|----------|-----------------------------------------------------------------------------------------|---------------------------|
| <span data-ttu-id="a382b-117">**Слева**</span><span class="sxs-lookup"><span data-stu-id="a382b-117">**Left**</span></span>   | <span data-ttu-id="a382b-118">**xs:integer**</span><span class="sxs-lookup"><span data-stu-id="a382b-118">**xs:integer**</span></span>            | <span data-ttu-id="a382b-119">Обязательно</span><span class="sxs-lookup"><span data-stu-id="a382b-119">Required</span></span> | <span data-ttu-id="a382b-120">Расстояние от начала до крайней левой точки в ограничивающем прямоугольнике для элемента.</span><span class="sxs-lookup"><span data-stu-id="a382b-120">The distance from the origin to the leftmost point in the bounding box for the element.</span></span> | <span data-ttu-id="a382b-121">Любое целое число.</span><span class="sxs-lookup"><span data-stu-id="a382b-121">Any integer.</span></span>              |
| <span data-ttu-id="a382b-122">**Top**</span><span class="sxs-lookup"><span data-stu-id="a382b-122">**Top**</span></span>    | <span data-ttu-id="a382b-123">**xs:integer**</span><span class="sxs-lookup"><span data-stu-id="a382b-123">**xs:integer**</span></span>            | <span data-ttu-id="a382b-124">Обязательно</span><span class="sxs-lookup"><span data-stu-id="a382b-124">Required</span></span> | <span data-ttu-id="a382b-125">Расстояние от начала до самой верхней точки ограничивающего прямоугольника для элемента.</span><span class="sxs-lookup"><span data-stu-id="a382b-125">The distance from the origin to the topmost point in the bounding box for the element.</span></span>  | <span data-ttu-id="a382b-126">Любое целое число.</span><span class="sxs-lookup"><span data-stu-id="a382b-126">Any integer.</span></span>              |
| <span data-ttu-id="a382b-127">**Width**</span><span class="sxs-lookup"><span data-stu-id="a382b-127">**Width**</span></span>  | <span data-ttu-id="a382b-128">**xs:nonNegativeInteger**</span><span class="sxs-lookup"><span data-stu-id="a382b-128">**xs:nonNegativeInteger**</span></span> | <span data-ttu-id="a382b-129">Обязательно</span><span class="sxs-lookup"><span data-stu-id="a382b-129">Required</span></span> | <span data-ttu-id="a382b-130">Ширина ограничивающего прямоугольника для элемента.</span><span class="sxs-lookup"><span data-stu-id="a382b-130">The width of the bounding box for the element.</span></span>                                          | <span data-ttu-id="a382b-131">Любое неотрицательное целое число.</span><span class="sxs-lookup"><span data-stu-id="a382b-131">Any non-negative integer.</span></span> |
| <span data-ttu-id="a382b-132">**Height**</span><span class="sxs-lookup"><span data-stu-id="a382b-132">**Height**</span></span> | <span data-ttu-id="a382b-133">**xs:nonNegativeInteger**</span><span class="sxs-lookup"><span data-stu-id="a382b-133">**xs:nonNegativeInteger**</span></span> | <span data-ttu-id="a382b-134">Обязательно</span><span class="sxs-lookup"><span data-stu-id="a382b-134">Required</span></span> | <span data-ttu-id="a382b-135">Высота ограничивающего прямоугольника для элемента.</span><span class="sxs-lookup"><span data-stu-id="a382b-135">The height of the bounding box for the element.</span></span>                                         | <span data-ttu-id="a382b-136">Любое неотрицательное целое число.</span><span class="sxs-lookup"><span data-stu-id="a382b-136">Any non-negative integer.</span></span> |



 

## <a name="element-information"></a><span data-ttu-id="a382b-137">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="a382b-137">Element Information</span></span>



|              |                                                         |
|--------------|---------------------------------------------------------|
| <span data-ttu-id="a382b-138">Тип элемента</span><span class="sxs-lookup"><span data-stu-id="a382b-138">Element type</span></span> | <span data-ttu-id="a382b-139">[**ImageType**](imagetype-complex-type.md) complexType</span><span class="sxs-lookup"><span data-stu-id="a382b-139">[**ImageType**](imagetype-complex-type.md) complexType</span></span> |
| <span data-ttu-id="a382b-140">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="a382b-140">Namespace</span></span>    | <span data-ttu-id="a382b-141">urn: schemas-microsoft-com: TabletPC: ричинк</span><span class="sxs-lookup"><span data-stu-id="a382b-141">urn:schemas-microsoft-com:tabletpc:richink</span></span>              |
| <span data-ttu-id="a382b-142">Имя схемы</span><span class="sxs-lookup"><span data-stu-id="a382b-142">Schema name</span></span>  | <span data-ttu-id="a382b-143">Средство чтения журнала</span><span class="sxs-lookup"><span data-stu-id="a382b-143">Journal Reader</span></span>                                          |



 

## <a name="see-also"></a><span data-ttu-id="a382b-144">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="a382b-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a382b-145">**Историческая справка**</span><span class="sxs-lookup"><span data-stu-id="a382b-145">**Background**</span></span>](background-element.md)
</dt> </dl>

 

 



