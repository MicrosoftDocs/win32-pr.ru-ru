---
description: Содержит содержимое, классифицированное анализатором или пользователем в виде рисунка.
ms.assetid: 566542f3-b824-442d-9d8b-0064ebcf9b68
title: Элемент Drawing
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1d87c0a3d8879fb5f3146c46c9c88d83a6e658d8
ms.sourcegitcommit: c3f669dc1d52278432bf75ad9fddba3257d26aa2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/04/2021
ms.locfileid: "111432516"
---
# <a name="drawing-element"></a><span data-ttu-id="c91c1-103">Элемент Drawing</span><span class="sxs-lookup"><span data-stu-id="c91c1-103">Drawing Element</span></span>

<span data-ttu-id="c91c1-104">Содержит содержимое, классифицированное анализатором или пользователем в виде рисунка.</span><span class="sxs-lookup"><span data-stu-id="c91c1-104">Contains content that has been classified by the analyzer or the user as a drawing.</span></span>

## <a name="definition"></a><span data-ttu-id="c91c1-105">Определение</span><span class="sxs-lookup"><span data-stu-id="c91c1-105">Definition</span></span>

``` syntax
<xs:element name="Drawing" type="DrawingType" minOccurs="0" maxOccurs="unbounded" />
```

## <a name="parent-elements"></a><span data-ttu-id="c91c1-106">Родительские элементы</span><span class="sxs-lookup"><span data-stu-id="c91c1-106">Parent Elements</span></span>

[<span data-ttu-id="c91c1-107">**Содержани**</span><span class="sxs-lookup"><span data-stu-id="c91c1-107">**Content**</span></span>](content-element--journal-reader.md)

[<span data-ttu-id="c91c1-108">**граупноде**</span><span class="sxs-lookup"><span data-stu-id="c91c1-108">**GroupNode**</span></span>](groupnode-element.md)

## <a name="child-elements"></a><span data-ttu-id="c91c1-109">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="c91c1-109">Child Elements</span></span>

[<span data-ttu-id="c91c1-110">**скалартрансформ**</span><span class="sxs-lookup"><span data-stu-id="c91c1-110">**ScalarTransform**</span></span>](scalartransform-element.md)

[<span data-ttu-id="c91c1-111">**канреклассифи**</span><span class="sxs-lookup"><span data-stu-id="c91c1-111">**CanReClassify**</span></span>](canreclassify-element.md)

[<span data-ttu-id="c91c1-112">**инккласс**</span><span class="sxs-lookup"><span data-stu-id="c91c1-112">**InkClass**</span></span>](inkclass-element.md)

[<span data-ttu-id="c91c1-113">**инкобжект**</span><span class="sxs-lookup"><span data-stu-id="c91c1-113">**InkObject**</span></span>](inkobject-element.md)

## <a name="attributes"></a><span data-ttu-id="c91c1-114">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="c91c1-114">Attributes</span></span>



| <span data-ttu-id="c91c1-115">attribute</span><span class="sxs-lookup"><span data-stu-id="c91c1-115">Attribute</span></span>  | <span data-ttu-id="c91c1-116">Тип</span><span class="sxs-lookup"><span data-stu-id="c91c1-116">Type</span></span>                      | <span data-ttu-id="c91c1-117">Обязательно</span><span class="sxs-lookup"><span data-stu-id="c91c1-117">Required</span></span> | <span data-ttu-id="c91c1-118">Описание</span><span class="sxs-lookup"><span data-stu-id="c91c1-118">Description</span></span>                                                                             | <span data-ttu-id="c91c1-119">Возможные значения</span><span class="sxs-lookup"><span data-stu-id="c91c1-119">Possible Values</span></span>           |
|------------|---------------------------|----------|-----------------------------------------------------------------------------------------|---------------------------|
| <span data-ttu-id="c91c1-120">**Слева**</span><span class="sxs-lookup"><span data-stu-id="c91c1-120">**Left**</span></span>   | <span data-ttu-id="c91c1-121">**xs:integer**</span><span class="sxs-lookup"><span data-stu-id="c91c1-121">**xs:integer**</span></span>            | <span data-ttu-id="c91c1-122">Обязательно</span><span class="sxs-lookup"><span data-stu-id="c91c1-122">Required</span></span> | <span data-ttu-id="c91c1-123">Расстояние от начала до крайней левой точки в ограничивающем прямоугольнике для элемента.</span><span class="sxs-lookup"><span data-stu-id="c91c1-123">The distance from the origin to the leftmost point in the bounding box for the element.</span></span> | <span data-ttu-id="c91c1-124">Любое целое число.</span><span class="sxs-lookup"><span data-stu-id="c91c1-124">Any integer.</span></span>              |
| <span data-ttu-id="c91c1-125">**Top**</span><span class="sxs-lookup"><span data-stu-id="c91c1-125">**Top**</span></span>    | <span data-ttu-id="c91c1-126">**xs:integer**</span><span class="sxs-lookup"><span data-stu-id="c91c1-126">**xs:integer**</span></span>            | <span data-ttu-id="c91c1-127">Обязательно</span><span class="sxs-lookup"><span data-stu-id="c91c1-127">Required</span></span> | <span data-ttu-id="c91c1-128">Расстояние от начала до самой верхней точки ограничивающего прямоугольника для элемента.</span><span class="sxs-lookup"><span data-stu-id="c91c1-128">The distance from the origin to the topmost point in the bounding box for the element.</span></span>  | <span data-ttu-id="c91c1-129">Любое целое число.</span><span class="sxs-lookup"><span data-stu-id="c91c1-129">Any integer.</span></span>              |
| <span data-ttu-id="c91c1-130">**Width**</span><span class="sxs-lookup"><span data-stu-id="c91c1-130">**Width**</span></span>  | <span data-ttu-id="c91c1-131">**xs:nonNegativeInteger**</span><span class="sxs-lookup"><span data-stu-id="c91c1-131">**xs:nonNegativeInteger**</span></span> | <span data-ttu-id="c91c1-132">Обязательно</span><span class="sxs-lookup"><span data-stu-id="c91c1-132">Required</span></span> | <span data-ttu-id="c91c1-133">Ширина ограничивающего прямоугольника для элемента.</span><span class="sxs-lookup"><span data-stu-id="c91c1-133">The width of the bounding box for the element.</span></span>                                          | <span data-ttu-id="c91c1-134">Любое неотрицательное целое число.</span><span class="sxs-lookup"><span data-stu-id="c91c1-134">Any non-negative integer.</span></span> |
| <span data-ttu-id="c91c1-135">**Height**</span><span class="sxs-lookup"><span data-stu-id="c91c1-135">**Height**</span></span> | <span data-ttu-id="c91c1-136">**xs:nonNegativeInteger**</span><span class="sxs-lookup"><span data-stu-id="c91c1-136">**xs:nonNegativeInteger**</span></span> | <span data-ttu-id="c91c1-137">Обязательно</span><span class="sxs-lookup"><span data-stu-id="c91c1-137">Required</span></span> | <span data-ttu-id="c91c1-138">Высота ограничивающего прямоугольника для элемента.</span><span class="sxs-lookup"><span data-stu-id="c91c1-138">The height of the bounding box for the element.</span></span>                                         | <span data-ttu-id="c91c1-139">Любое неотрицательное целое число.</span><span class="sxs-lookup"><span data-stu-id="c91c1-139">Any non-negative integer.</span></span> |



 

## <a name="element-information"></a><span data-ttu-id="c91c1-140">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="c91c1-140">Element Information</span></span>



|  <span data-ttu-id="c91c1-141">Элемент</span><span class="sxs-lookup"><span data-stu-id="c91c1-141">Element</span></span>     | <span data-ttu-id="c91c1-142">Значение</span><span class="sxs-lookup"><span data-stu-id="c91c1-142">Value</span></span>                                                     |
|--------------|-------------------------------------------------------------|
| <span data-ttu-id="c91c1-143">Тип элемента</span><span class="sxs-lookup"><span data-stu-id="c91c1-143">Element type</span></span> | <span data-ttu-id="c91c1-144">[**Дравингтипе**](drawingtype-complex-type.md) complexType</span><span class="sxs-lookup"><span data-stu-id="c91c1-144">[**DrawingType**](drawingtype-complex-type.md) complexType</span></span> |
| <span data-ttu-id="c91c1-145">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="c91c1-145">Namespace</span></span>    | <span data-ttu-id="c91c1-146">urn: schemas-microsoft-com: TabletPC: ричинк</span><span class="sxs-lookup"><span data-stu-id="c91c1-146">urn:schemas-microsoft-com:tabletpc:richink</span></span>                  |
| <span data-ttu-id="c91c1-147">Имя схемы</span><span class="sxs-lookup"><span data-stu-id="c91c1-147">Schema name</span></span>  | <span data-ttu-id="c91c1-148">Средство чтения журнала</span><span class="sxs-lookup"><span data-stu-id="c91c1-148">Journal Reader</span></span>                                              |



 

 

 



