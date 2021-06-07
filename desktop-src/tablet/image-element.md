---
description: Содержит закодированные двоичные данные для изображения в документе журнала, если оно есть.
ms.assetid: fbb86bef-68f7-4aad-8a98-1c68e79ea2de
title: Элемент Image
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e9dd3b37a39ce45ee0294f46922fbab376523b64
ms.sourcegitcommit: c3f669dc1d52278432bf75ad9fddba3257d26aa2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/04/2021
ms.locfileid: "111432586"
---
# <a name="image-element"></a><span data-ttu-id="be6c1-103">Элемент Image</span><span class="sxs-lookup"><span data-stu-id="be6c1-103">Image Element</span></span>

<span data-ttu-id="be6c1-104">Содержит закодированные двоичные данные для изображения в документе журнала, если оно есть.</span><span class="sxs-lookup"><span data-stu-id="be6c1-104">Contains encoded binary data for an image in the Journal document, if present.</span></span>

## <a name="definition"></a><span data-ttu-id="be6c1-105">Определение</span><span class="sxs-lookup"><span data-stu-id="be6c1-105">Definition</span></span>

``` syntax
 Copy Code<xs:element name="Image" type="ImageType" />
```

## <a name="parent-elements"></a><span data-ttu-id="be6c1-106">Родительские элементы</span><span class="sxs-lookup"><span data-stu-id="be6c1-106">Parent Elements</span></span>

[<span data-ttu-id="be6c1-107">**Содержани**</span><span class="sxs-lookup"><span data-stu-id="be6c1-107">**Content**</span></span>](content-element--journal-reader.md)

[<span data-ttu-id="be6c1-108">**граупноде**</span><span class="sxs-lookup"><span data-stu-id="be6c1-108">**GroupNode**</span></span>](groupnode-element.md)

## <a name="child-elements"></a><span data-ttu-id="be6c1-109">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="be6c1-109">Child Elements</span></span>

<span data-ttu-id="be6c1-110">Отсутствует.</span><span class="sxs-lookup"><span data-stu-id="be6c1-110">None.</span></span>

## <a name="attributes"></a><span data-ttu-id="be6c1-111">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="be6c1-111">Attributes</span></span>



| <span data-ttu-id="be6c1-112">attribute</span><span class="sxs-lookup"><span data-stu-id="be6c1-112">Attribute</span></span>  | <span data-ttu-id="be6c1-113">Тип</span><span class="sxs-lookup"><span data-stu-id="be6c1-113">Type</span></span>                      | <span data-ttu-id="be6c1-114">Обязательно</span><span class="sxs-lookup"><span data-stu-id="be6c1-114">Required</span></span> | <span data-ttu-id="be6c1-115">Описание</span><span class="sxs-lookup"><span data-stu-id="be6c1-115">Description</span></span>                                                                             | <span data-ttu-id="be6c1-116">Возможные значения</span><span class="sxs-lookup"><span data-stu-id="be6c1-116">Possible Values</span></span>           |
|------------|---------------------------|----------|-----------------------------------------------------------------------------------------|---------------------------|
| <span data-ttu-id="be6c1-117">**Слева**</span><span class="sxs-lookup"><span data-stu-id="be6c1-117">**Left**</span></span>   | <span data-ttu-id="be6c1-118">**xs:integer**</span><span class="sxs-lookup"><span data-stu-id="be6c1-118">**xs:integer**</span></span>            | <span data-ttu-id="be6c1-119">Обязательно</span><span class="sxs-lookup"><span data-stu-id="be6c1-119">Required</span></span> | <span data-ttu-id="be6c1-120">Расстояние от начала до крайней левой точки в ограничивающем прямоугольнике для элемента.</span><span class="sxs-lookup"><span data-stu-id="be6c1-120">The distance from the origin to the leftmost point in the bounding box for the element.</span></span> | <span data-ttu-id="be6c1-121">Любое целое число.</span><span class="sxs-lookup"><span data-stu-id="be6c1-121">Any integer.</span></span>              |
| <span data-ttu-id="be6c1-122">**Top**</span><span class="sxs-lookup"><span data-stu-id="be6c1-122">**Top**</span></span>    | <span data-ttu-id="be6c1-123">**xs:integer**</span><span class="sxs-lookup"><span data-stu-id="be6c1-123">**xs:integer**</span></span>            | <span data-ttu-id="be6c1-124">Обязательно</span><span class="sxs-lookup"><span data-stu-id="be6c1-124">Required</span></span> | <span data-ttu-id="be6c1-125">Расстояние от начала до самой верхней точки ограничивающего прямоугольника для элемента.</span><span class="sxs-lookup"><span data-stu-id="be6c1-125">The distance from the origin to the topmost point in the bounding box for the element.</span></span>  | <span data-ttu-id="be6c1-126">Любое целое число.</span><span class="sxs-lookup"><span data-stu-id="be6c1-126">Any integer.</span></span>              |
| <span data-ttu-id="be6c1-127">**Width**</span><span class="sxs-lookup"><span data-stu-id="be6c1-127">**Width**</span></span>  | <span data-ttu-id="be6c1-128">**xs:nonNegativeInteger**</span><span class="sxs-lookup"><span data-stu-id="be6c1-128">**xs:nonNegativeInteger**</span></span> | <span data-ttu-id="be6c1-129">Обязательно</span><span class="sxs-lookup"><span data-stu-id="be6c1-129">Required</span></span> | <span data-ttu-id="be6c1-130">Ширина ограничивающего прямоугольника для элемента.</span><span class="sxs-lookup"><span data-stu-id="be6c1-130">The width of the bounding box for the element.</span></span>                                          | <span data-ttu-id="be6c1-131">Любое неотрицательное целое число.</span><span class="sxs-lookup"><span data-stu-id="be6c1-131">Any non-negative integer.</span></span> |
| <span data-ttu-id="be6c1-132">**Height**</span><span class="sxs-lookup"><span data-stu-id="be6c1-132">**Height**</span></span> | <span data-ttu-id="be6c1-133">**xs:nonNegativeInteger**</span><span class="sxs-lookup"><span data-stu-id="be6c1-133">**xs:nonNegativeInteger**</span></span> | <span data-ttu-id="be6c1-134">Обязательно</span><span class="sxs-lookup"><span data-stu-id="be6c1-134">Required</span></span> | <span data-ttu-id="be6c1-135">Высота ограничивающего прямоугольника для элемента.</span><span class="sxs-lookup"><span data-stu-id="be6c1-135">The height of the bounding box for the element.</span></span>                                         | <span data-ttu-id="be6c1-136">Любое неотрицательное целое число.</span><span class="sxs-lookup"><span data-stu-id="be6c1-136">Any non-negative integer.</span></span> |



 

## <a name="element-information"></a><span data-ttu-id="be6c1-137">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="be6c1-137">Element Information</span></span>



|  <span data-ttu-id="be6c1-138">Элемент</span><span class="sxs-lookup"><span data-stu-id="be6c1-138">Element</span></span>     | <span data-ttu-id="be6c1-139">Значение</span><span class="sxs-lookup"><span data-stu-id="be6c1-139">Value</span></span>                                                     |
|--------------|---------------------------------------------------------|
| <span data-ttu-id="be6c1-140">Тип элемента</span><span class="sxs-lookup"><span data-stu-id="be6c1-140">Element type</span></span> | <span data-ttu-id="be6c1-141">[**ImageType**](imagetype-complex-type.md) complexType</span><span class="sxs-lookup"><span data-stu-id="be6c1-141">[**ImageType**](imagetype-complex-type.md) complexType</span></span> |
| <span data-ttu-id="be6c1-142">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="be6c1-142">Namespace</span></span>    | <span data-ttu-id="be6c1-143">urn: schemas-microsoft-com: TabletPC: ричинк</span><span class="sxs-lookup"><span data-stu-id="be6c1-143">urn:schemas-microsoft-com:tabletpc:richink</span></span>              |
| <span data-ttu-id="be6c1-144">Имя схемы</span><span class="sxs-lookup"><span data-stu-id="be6c1-144">Schema name</span></span>  | <span data-ttu-id="be6c1-145">Средство чтения журнала</span><span class="sxs-lookup"><span data-stu-id="be6c1-145">Journal Reader</span></span>                                          |



 

## <a name="see-also"></a><span data-ttu-id="be6c1-146">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="be6c1-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="be6c1-147">**Фон**</span><span class="sxs-lookup"><span data-stu-id="be6c1-147">**Background**</span></span>](background-element.md)
</dt> </dl>

 

 



