---
description: Содержит сведения о местоположении и границах для заголовка примечания, если оно есть.
ms.assetid: b193f6c2-5f26-41f9-acc8-d734c426b069
title: Титлеареа, элемент
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c009d817af9679edda618dd0262c7cbb85a612ed
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103999523"
---
# <a name="titlearea-element"></a><span data-ttu-id="51300-103">Титлеареа, элемент</span><span class="sxs-lookup"><span data-stu-id="51300-103">TitleArea Element</span></span>

<span data-ttu-id="51300-104">Содержит сведения о местоположении и границах для заголовка примечания, если оно есть.</span><span class="sxs-lookup"><span data-stu-id="51300-104">Contains location and bounding information for the note Title, if present.</span></span>

## <a name="definition"></a><span data-ttu-id="51300-105">Определение</span><span class="sxs-lookup"><span data-stu-id="51300-105">Definition</span></span>

``` syntax
<xs:element name="TitleArea" type="TitleAreaType" minOccurs="0" />
```

## <a name="parent-elements"></a><span data-ttu-id="51300-106">Родительские элементы</span><span class="sxs-lookup"><span data-stu-id="51300-106">Parent Elements</span></span>

[<span data-ttu-id="51300-107">**Заголовок**</span><span class="sxs-lookup"><span data-stu-id="51300-107">**Title**</span></span>](title-element.md)

## <a name="child-elements"></a><span data-ttu-id="51300-108">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="51300-108">Child Elements</span></span>

<span data-ttu-id="51300-109">Отсутствует.</span><span class="sxs-lookup"><span data-stu-id="51300-109">None.</span></span>

## <a name="attributes"></a><span data-ttu-id="51300-110">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="51300-110">Attributes</span></span>



| <span data-ttu-id="51300-111">attribute</span><span class="sxs-lookup"><span data-stu-id="51300-111">Attribute</span></span>  | <span data-ttu-id="51300-112">Тип</span><span class="sxs-lookup"><span data-stu-id="51300-112">Type</span></span>                      | <span data-ttu-id="51300-113">Обязательно</span><span class="sxs-lookup"><span data-stu-id="51300-113">Required</span></span> | <span data-ttu-id="51300-114">Описание</span><span class="sxs-lookup"><span data-stu-id="51300-114">Description</span></span>                                                                             | <span data-ttu-id="51300-115">Возможные значения</span><span class="sxs-lookup"><span data-stu-id="51300-115">Possible Values</span></span>           |
|------------|---------------------------|----------|-----------------------------------------------------------------------------------------|---------------------------|
| <span data-ttu-id="51300-116">**Слева**</span><span class="sxs-lookup"><span data-stu-id="51300-116">**Left**</span></span>   | <span data-ttu-id="51300-117">**xs:integer**</span><span class="sxs-lookup"><span data-stu-id="51300-117">**xs:integer**</span></span>            | <span data-ttu-id="51300-118">Обязательно</span><span class="sxs-lookup"><span data-stu-id="51300-118">Required</span></span> | <span data-ttu-id="51300-119">Расстояние от начала до крайней левой точки в ограничивающем прямоугольнике для элемента.</span><span class="sxs-lookup"><span data-stu-id="51300-119">The distance from the origin to the leftmost point in the bounding box for the element.</span></span> | <span data-ttu-id="51300-120">Любое целое число.</span><span class="sxs-lookup"><span data-stu-id="51300-120">Any integer.</span></span>              |
| <span data-ttu-id="51300-121">**Top**</span><span class="sxs-lookup"><span data-stu-id="51300-121">**Top**</span></span>    | <span data-ttu-id="51300-122">**xs:integer**</span><span class="sxs-lookup"><span data-stu-id="51300-122">**xs:integer**</span></span>            | <span data-ttu-id="51300-123">Обязательно</span><span class="sxs-lookup"><span data-stu-id="51300-123">Required</span></span> | <span data-ttu-id="51300-124">Расстояние от начала до самой верхней точки ограничивающего прямоугольника для элемента.</span><span class="sxs-lookup"><span data-stu-id="51300-124">The distance from the origin to the topmost point in the bounding box for the element.</span></span>  | <span data-ttu-id="51300-125">Любое целое число.</span><span class="sxs-lookup"><span data-stu-id="51300-125">Any integer.</span></span>              |
| <span data-ttu-id="51300-126">**Width**</span><span class="sxs-lookup"><span data-stu-id="51300-126">**Width**</span></span>  | <span data-ttu-id="51300-127">**xs:nonNegativeInteger**</span><span class="sxs-lookup"><span data-stu-id="51300-127">**xs:nonNegativeInteger**</span></span> | <span data-ttu-id="51300-128">Обязательно</span><span class="sxs-lookup"><span data-stu-id="51300-128">Required</span></span> | <span data-ttu-id="51300-129">Ширина ограничивающего прямоугольника для элемента.</span><span class="sxs-lookup"><span data-stu-id="51300-129">The width of the bounding box for the element.</span></span>                                          | <span data-ttu-id="51300-130">Любое неотрицательное целое число.</span><span class="sxs-lookup"><span data-stu-id="51300-130">Any non-negative integer.</span></span> |
| <span data-ttu-id="51300-131">**Height**</span><span class="sxs-lookup"><span data-stu-id="51300-131">**Height**</span></span> | <span data-ttu-id="51300-132">**xs:nonNegativeInteger**</span><span class="sxs-lookup"><span data-stu-id="51300-132">**xs:nonNegativeInteger**</span></span> | <span data-ttu-id="51300-133">Обязательно</span><span class="sxs-lookup"><span data-stu-id="51300-133">Required</span></span> | <span data-ttu-id="51300-134">Высота ограничивающего прямоугольника для элемента.</span><span class="sxs-lookup"><span data-stu-id="51300-134">The height of the bounding box for the element.</span></span>                                         | <span data-ttu-id="51300-135">Любое неотрицательное целое число.</span><span class="sxs-lookup"><span data-stu-id="51300-135">Any non-negative integer.</span></span> |



 

## <a name="element-information"></a><span data-ttu-id="51300-136">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="51300-136">Element Information</span></span>



|              |                                                                 |
|--------------|-----------------------------------------------------------------|
| <span data-ttu-id="51300-137">Тип элемента</span><span class="sxs-lookup"><span data-stu-id="51300-137">Element type</span></span> | <span data-ttu-id="51300-138">[**Титлеареатипе**](titleareatype-complex-type.md) complexType</span><span class="sxs-lookup"><span data-stu-id="51300-138">[**TitleAreaType**](titleareatype-complex-type.md) complexType</span></span> |
| <span data-ttu-id="51300-139">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="51300-139">Namespace</span></span>    | <span data-ttu-id="51300-140">urn: schemas-microsoft-com: TabletPC: ричинк</span><span class="sxs-lookup"><span data-stu-id="51300-140">urn:schemas-microsoft-com:tabletpc:richink</span></span>                      |
| <span data-ttu-id="51300-141">Имя схемы</span><span class="sxs-lookup"><span data-stu-id="51300-141">Schema name</span></span>  | <span data-ttu-id="51300-142">Средство чтения журнала</span><span class="sxs-lookup"><span data-stu-id="51300-142">Journal Reader</span></span>                                                  |



 

 

 



