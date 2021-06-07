---
description: Содержит сведения о местоположении и границах для заголовка примечания, если оно есть.
ms.assetid: b193f6c2-5f26-41f9-acc8-d734c426b069
title: Титлеареа, элемент
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 88d563e8d7f6fc0107bc3302d3f8d94d29dfbfb8
ms.sourcegitcommit: c3f669dc1d52278432bf75ad9fddba3257d26aa2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/04/2021
ms.locfileid: "111432196"
---
# <a name="titlearea-element"></a><span data-ttu-id="37914-103">Титлеареа, элемент</span><span class="sxs-lookup"><span data-stu-id="37914-103">TitleArea Element</span></span>

<span data-ttu-id="37914-104">Содержит сведения о местоположении и границах для заголовка примечания, если оно есть.</span><span class="sxs-lookup"><span data-stu-id="37914-104">Contains location and bounding information for the note Title, if present.</span></span>

## <a name="definition"></a><span data-ttu-id="37914-105">Определение</span><span class="sxs-lookup"><span data-stu-id="37914-105">Definition</span></span>

``` syntax
<xs:element name="TitleArea" type="TitleAreaType" minOccurs="0" />
```

## <a name="parent-elements"></a><span data-ttu-id="37914-106">Родительские элементы</span><span class="sxs-lookup"><span data-stu-id="37914-106">Parent Elements</span></span>

[<span data-ttu-id="37914-107">**Заголовок**</span><span class="sxs-lookup"><span data-stu-id="37914-107">**Title**</span></span>](title-element.md)

## <a name="child-elements"></a><span data-ttu-id="37914-108">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="37914-108">Child Elements</span></span>

<span data-ttu-id="37914-109">Отсутствует.</span><span class="sxs-lookup"><span data-stu-id="37914-109">None.</span></span>

## <a name="attributes"></a><span data-ttu-id="37914-110">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="37914-110">Attributes</span></span>



| <span data-ttu-id="37914-111">attribute</span><span class="sxs-lookup"><span data-stu-id="37914-111">Attribute</span></span>  | <span data-ttu-id="37914-112">Тип</span><span class="sxs-lookup"><span data-stu-id="37914-112">Type</span></span>                      | <span data-ttu-id="37914-113">Обязательно</span><span class="sxs-lookup"><span data-stu-id="37914-113">Required</span></span> | <span data-ttu-id="37914-114">Описание</span><span class="sxs-lookup"><span data-stu-id="37914-114">Description</span></span>                                                                             | <span data-ttu-id="37914-115">Возможные значения</span><span class="sxs-lookup"><span data-stu-id="37914-115">Possible Values</span></span>           |
|------------|---------------------------|----------|-----------------------------------------------------------------------------------------|---------------------------|
| <span data-ttu-id="37914-116">**Слева**</span><span class="sxs-lookup"><span data-stu-id="37914-116">**Left**</span></span>   | <span data-ttu-id="37914-117">**xs:integer**</span><span class="sxs-lookup"><span data-stu-id="37914-117">**xs:integer**</span></span>            | <span data-ttu-id="37914-118">Обязательно</span><span class="sxs-lookup"><span data-stu-id="37914-118">Required</span></span> | <span data-ttu-id="37914-119">Расстояние от начала до крайней левой точки в ограничивающем прямоугольнике для элемента.</span><span class="sxs-lookup"><span data-stu-id="37914-119">The distance from the origin to the leftmost point in the bounding box for the element.</span></span> | <span data-ttu-id="37914-120">Любое целое число.</span><span class="sxs-lookup"><span data-stu-id="37914-120">Any integer.</span></span>              |
| <span data-ttu-id="37914-121">**Top**</span><span class="sxs-lookup"><span data-stu-id="37914-121">**Top**</span></span>    | <span data-ttu-id="37914-122">**xs:integer**</span><span class="sxs-lookup"><span data-stu-id="37914-122">**xs:integer**</span></span>            | <span data-ttu-id="37914-123">Обязательно</span><span class="sxs-lookup"><span data-stu-id="37914-123">Required</span></span> | <span data-ttu-id="37914-124">Расстояние от начала до самой верхней точки ограничивающего прямоугольника для элемента.</span><span class="sxs-lookup"><span data-stu-id="37914-124">The distance from the origin to the topmost point in the bounding box for the element.</span></span>  | <span data-ttu-id="37914-125">Любое целое число.</span><span class="sxs-lookup"><span data-stu-id="37914-125">Any integer.</span></span>              |
| <span data-ttu-id="37914-126">**Width**</span><span class="sxs-lookup"><span data-stu-id="37914-126">**Width**</span></span>  | <span data-ttu-id="37914-127">**xs:nonNegativeInteger**</span><span class="sxs-lookup"><span data-stu-id="37914-127">**xs:nonNegativeInteger**</span></span> | <span data-ttu-id="37914-128">Обязательно</span><span class="sxs-lookup"><span data-stu-id="37914-128">Required</span></span> | <span data-ttu-id="37914-129">Ширина ограничивающего прямоугольника для элемента.</span><span class="sxs-lookup"><span data-stu-id="37914-129">The width of the bounding box for the element.</span></span>                                          | <span data-ttu-id="37914-130">Любое неотрицательное целое число.</span><span class="sxs-lookup"><span data-stu-id="37914-130">Any non-negative integer.</span></span> |
| <span data-ttu-id="37914-131">**Height**</span><span class="sxs-lookup"><span data-stu-id="37914-131">**Height**</span></span> | <span data-ttu-id="37914-132">**xs:nonNegativeInteger**</span><span class="sxs-lookup"><span data-stu-id="37914-132">**xs:nonNegativeInteger**</span></span> | <span data-ttu-id="37914-133">Обязательно</span><span class="sxs-lookup"><span data-stu-id="37914-133">Required</span></span> | <span data-ttu-id="37914-134">Высота ограничивающего прямоугольника для элемента.</span><span class="sxs-lookup"><span data-stu-id="37914-134">The height of the bounding box for the element.</span></span>                                         | <span data-ttu-id="37914-135">Любое неотрицательное целое число.</span><span class="sxs-lookup"><span data-stu-id="37914-135">Any non-negative integer.</span></span> |



 

## <a name="element-information"></a><span data-ttu-id="37914-136">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="37914-136">Element Information</span></span>



|   <span data-ttu-id="37914-137">Элемент</span><span class="sxs-lookup"><span data-stu-id="37914-137">Element</span></span>    | <span data-ttu-id="37914-138">Значение</span><span class="sxs-lookup"><span data-stu-id="37914-138">Value</span></span>                                                           |
|--------------|-----------------------------------------------------------------|
| <span data-ttu-id="37914-139">Тип элемента</span><span class="sxs-lookup"><span data-stu-id="37914-139">Element type</span></span> | <span data-ttu-id="37914-140">[**Титлеареатипе**](titleareatype-complex-type.md) complexType</span><span class="sxs-lookup"><span data-stu-id="37914-140">[**TitleAreaType**](titleareatype-complex-type.md) complexType</span></span> |
| <span data-ttu-id="37914-141">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="37914-141">Namespace</span></span>    | <span data-ttu-id="37914-142">urn: schemas-microsoft-com: TabletPC: ричинк</span><span class="sxs-lookup"><span data-stu-id="37914-142">urn:schemas-microsoft-com:tabletpc:richink</span></span>                      |
| <span data-ttu-id="37914-143">Имя схемы</span><span class="sxs-lookup"><span data-stu-id="37914-143">Schema name</span></span>  | <span data-ttu-id="37914-144">Средство чтения журнала</span><span class="sxs-lookup"><span data-stu-id="37914-144">Journal Reader</span></span>                                                  |



 

 

 



