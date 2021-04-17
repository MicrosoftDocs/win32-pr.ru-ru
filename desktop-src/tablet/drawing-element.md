---
description: Содержит содержимое, классифицированное анализатором или пользователем в виде рисунка.
ms.assetid: 566542f3-b824-442d-9d8b-0064ebcf9b68
title: Элемент Drawing
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fe516a4ba33e6e597b17ce8365d792f19468c3b5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105693764"
---
# <a name="drawing-element"></a><span data-ttu-id="81e31-103">Элемент Drawing</span><span class="sxs-lookup"><span data-stu-id="81e31-103">Drawing Element</span></span>

<span data-ttu-id="81e31-104">Содержит содержимое, классифицированное анализатором или пользователем в виде рисунка.</span><span class="sxs-lookup"><span data-stu-id="81e31-104">Contains content that has been classified by the analyzer or the user as a drawing.</span></span>

## <a name="definition"></a><span data-ttu-id="81e31-105">Определение</span><span class="sxs-lookup"><span data-stu-id="81e31-105">Definition</span></span>

``` syntax
<xs:element name="Drawing" type="DrawingType" minOccurs="0" maxOccurs="unbounded" />
```

## <a name="parent-elements"></a><span data-ttu-id="81e31-106">Родительские элементы</span><span class="sxs-lookup"><span data-stu-id="81e31-106">Parent Elements</span></span>

[<span data-ttu-id="81e31-107">**Содержани**</span><span class="sxs-lookup"><span data-stu-id="81e31-107">**Content**</span></span>](content-element--journal-reader.md)

[<span data-ttu-id="81e31-108">**граупноде**</span><span class="sxs-lookup"><span data-stu-id="81e31-108">**GroupNode**</span></span>](groupnode-element.md)

## <a name="child-elements"></a><span data-ttu-id="81e31-109">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="81e31-109">Child Elements</span></span>

[<span data-ttu-id="81e31-110">**скалартрансформ**</span><span class="sxs-lookup"><span data-stu-id="81e31-110">**ScalarTransform**</span></span>](scalartransform-element.md)

[<span data-ttu-id="81e31-111">**канреклассифи**</span><span class="sxs-lookup"><span data-stu-id="81e31-111">**CanReClassify**</span></span>](canreclassify-element.md)

[<span data-ttu-id="81e31-112">**инккласс**</span><span class="sxs-lookup"><span data-stu-id="81e31-112">**InkClass**</span></span>](inkclass-element.md)

[<span data-ttu-id="81e31-113">**инкобжект**</span><span class="sxs-lookup"><span data-stu-id="81e31-113">**InkObject**</span></span>](inkobject-element.md)

## <a name="attributes"></a><span data-ttu-id="81e31-114">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="81e31-114">Attributes</span></span>



| <span data-ttu-id="81e31-115">attribute</span><span class="sxs-lookup"><span data-stu-id="81e31-115">Attribute</span></span>  | <span data-ttu-id="81e31-116">Тип</span><span class="sxs-lookup"><span data-stu-id="81e31-116">Type</span></span>                      | <span data-ttu-id="81e31-117">Обязательно</span><span class="sxs-lookup"><span data-stu-id="81e31-117">Required</span></span> | <span data-ttu-id="81e31-118">Описание</span><span class="sxs-lookup"><span data-stu-id="81e31-118">Description</span></span>                                                                             | <span data-ttu-id="81e31-119">Возможные значения</span><span class="sxs-lookup"><span data-stu-id="81e31-119">Possible Values</span></span>           |
|------------|---------------------------|----------|-----------------------------------------------------------------------------------------|---------------------------|
| <span data-ttu-id="81e31-120">**Слева**</span><span class="sxs-lookup"><span data-stu-id="81e31-120">**Left**</span></span>   | <span data-ttu-id="81e31-121">**xs:integer**</span><span class="sxs-lookup"><span data-stu-id="81e31-121">**xs:integer**</span></span>            | <span data-ttu-id="81e31-122">Обязательно</span><span class="sxs-lookup"><span data-stu-id="81e31-122">Required</span></span> | <span data-ttu-id="81e31-123">Расстояние от начала до крайней левой точки в ограничивающем прямоугольнике для элемента.</span><span class="sxs-lookup"><span data-stu-id="81e31-123">The distance from the origin to the leftmost point in the bounding box for the element.</span></span> | <span data-ttu-id="81e31-124">Любое целое число.</span><span class="sxs-lookup"><span data-stu-id="81e31-124">Any integer.</span></span>              |
| <span data-ttu-id="81e31-125">**Top**</span><span class="sxs-lookup"><span data-stu-id="81e31-125">**Top**</span></span>    | <span data-ttu-id="81e31-126">**xs:integer**</span><span class="sxs-lookup"><span data-stu-id="81e31-126">**xs:integer**</span></span>            | <span data-ttu-id="81e31-127">Обязательно</span><span class="sxs-lookup"><span data-stu-id="81e31-127">Required</span></span> | <span data-ttu-id="81e31-128">Расстояние от начала до самой верхней точки ограничивающего прямоугольника для элемента.</span><span class="sxs-lookup"><span data-stu-id="81e31-128">The distance from the origin to the topmost point in the bounding box for the element.</span></span>  | <span data-ttu-id="81e31-129">Любое целое число.</span><span class="sxs-lookup"><span data-stu-id="81e31-129">Any integer.</span></span>              |
| <span data-ttu-id="81e31-130">**Width**</span><span class="sxs-lookup"><span data-stu-id="81e31-130">**Width**</span></span>  | <span data-ttu-id="81e31-131">**xs:nonNegativeInteger**</span><span class="sxs-lookup"><span data-stu-id="81e31-131">**xs:nonNegativeInteger**</span></span> | <span data-ttu-id="81e31-132">Обязательно</span><span class="sxs-lookup"><span data-stu-id="81e31-132">Required</span></span> | <span data-ttu-id="81e31-133">Ширина ограничивающего прямоугольника для элемента.</span><span class="sxs-lookup"><span data-stu-id="81e31-133">The width of the bounding box for the element.</span></span>                                          | <span data-ttu-id="81e31-134">Любое неотрицательное целое число.</span><span class="sxs-lookup"><span data-stu-id="81e31-134">Any non-negative integer.</span></span> |
| <span data-ttu-id="81e31-135">**Height**</span><span class="sxs-lookup"><span data-stu-id="81e31-135">**Height**</span></span> | <span data-ttu-id="81e31-136">**xs:nonNegativeInteger**</span><span class="sxs-lookup"><span data-stu-id="81e31-136">**xs:nonNegativeInteger**</span></span> | <span data-ttu-id="81e31-137">Обязательно</span><span class="sxs-lookup"><span data-stu-id="81e31-137">Required</span></span> | <span data-ttu-id="81e31-138">Высота ограничивающего прямоугольника для элемента.</span><span class="sxs-lookup"><span data-stu-id="81e31-138">The height of the bounding box for the element.</span></span>                                         | <span data-ttu-id="81e31-139">Любое неотрицательное целое число.</span><span class="sxs-lookup"><span data-stu-id="81e31-139">Any non-negative integer.</span></span> |



 

## <a name="element-information"></a><span data-ttu-id="81e31-140">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="81e31-140">Element Information</span></span>



|              |                                                             |
|--------------|-------------------------------------------------------------|
| <span data-ttu-id="81e31-141">Тип элемента</span><span class="sxs-lookup"><span data-stu-id="81e31-141">Element type</span></span> | <span data-ttu-id="81e31-142">[**Дравингтипе**](drawingtype-complex-type.md) complexType</span><span class="sxs-lookup"><span data-stu-id="81e31-142">[**DrawingType**](drawingtype-complex-type.md) complexType</span></span> |
| <span data-ttu-id="81e31-143">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="81e31-143">Namespace</span></span>    | <span data-ttu-id="81e31-144">urn: schemas-microsoft-com: TabletPC: ричинк</span><span class="sxs-lookup"><span data-stu-id="81e31-144">urn:schemas-microsoft-com:tabletpc:richink</span></span>                  |
| <span data-ttu-id="81e31-145">Имя схемы</span><span class="sxs-lookup"><span data-stu-id="81e31-145">Schema name</span></span>  | <span data-ttu-id="81e31-146">Средство чтения журнала</span><span class="sxs-lookup"><span data-stu-id="81e31-146">Journal Reader</span></span>                                              |



 

 

 



