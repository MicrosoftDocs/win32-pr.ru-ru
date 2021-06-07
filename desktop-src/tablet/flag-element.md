---
description: Содержит битовую карту в кодировке Base64 для флага, связанного с разделом заметки журнала.
ms.assetid: 612f8814-ab3c-4a3e-9791-525788d4cc72
title: Flag, элемент
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 46508f9821379fbedb3291ba45d16dbdd0fb316f
ms.sourcegitcommit: c3f669dc1d52278432bf75ad9fddba3257d26aa2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/04/2021
ms.locfileid: "111432334"
---
# <a name="flag-element"></a><span data-ttu-id="43d12-103">Flag, элемент</span><span class="sxs-lookup"><span data-stu-id="43d12-103">Flag Element</span></span>

<span data-ttu-id="43d12-104">Содержит битовую карту в кодировке Base64 для флага, связанного с разделом заметки журнала.</span><span class="sxs-lookup"><span data-stu-id="43d12-104">Contains a base64 encoded bitmap of a flag associated with section of a Journal note.</span></span>

## <a name="definition"></a><span data-ttu-id="43d12-105">Определение</span><span class="sxs-lookup"><span data-stu-id="43d12-105">Definition</span></span>

``` syntax
<xs:element name="Flag" type="FlagType" minOccurs="0" maxOccurs="unbounded" />
```

## <a name="parent-elements"></a><span data-ttu-id="43d12-106">Родительские элементы</span><span class="sxs-lookup"><span data-stu-id="43d12-106">Parent Elements</span></span>

[<span data-ttu-id="43d12-107">**Содержани**</span><span class="sxs-lookup"><span data-stu-id="43d12-107">**Content**</span></span>](content-element--journal-reader.md)

[<span data-ttu-id="43d12-108">**граупноде**</span><span class="sxs-lookup"><span data-stu-id="43d12-108">**GroupNode**</span></span>](groupnode-element.md)

## <a name="child-elements"></a><span data-ttu-id="43d12-109">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="43d12-109">Child Elements</span></span>

<span data-ttu-id="43d12-110">Отсутствует.</span><span class="sxs-lookup"><span data-stu-id="43d12-110">None.</span></span>

## <a name="attributes"></a><span data-ttu-id="43d12-111">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="43d12-111">Attributes</span></span>



| <span data-ttu-id="43d12-112">attribute</span><span class="sxs-lookup"><span data-stu-id="43d12-112">Attribute</span></span>  | <span data-ttu-id="43d12-113">Тип</span><span class="sxs-lookup"><span data-stu-id="43d12-113">Type</span></span>                      | <span data-ttu-id="43d12-114">Обязательно</span><span class="sxs-lookup"><span data-stu-id="43d12-114">Required</span></span> | <span data-ttu-id="43d12-115">Описание</span><span class="sxs-lookup"><span data-stu-id="43d12-115">Description</span></span>                                                                             | <span data-ttu-id="43d12-116">Возможные значения</span><span class="sxs-lookup"><span data-stu-id="43d12-116">Possible Values</span></span>           |
|------------|---------------------------|----------|-----------------------------------------------------------------------------------------|---------------------------|
| <span data-ttu-id="43d12-117">**Слева**</span><span class="sxs-lookup"><span data-stu-id="43d12-117">**Left**</span></span>   | <span data-ttu-id="43d12-118">**xs:integer**</span><span class="sxs-lookup"><span data-stu-id="43d12-118">**xs:integer**</span></span>            | <span data-ttu-id="43d12-119">Обязательно</span><span class="sxs-lookup"><span data-stu-id="43d12-119">Required</span></span> | <span data-ttu-id="43d12-120">Расстояние от начала до крайней левой точки в ограничивающем прямоугольнике для элемента.</span><span class="sxs-lookup"><span data-stu-id="43d12-120">The distance from the origin to the leftmost point in the bounding box for the element.</span></span> | <span data-ttu-id="43d12-121">Любое целое число.</span><span class="sxs-lookup"><span data-stu-id="43d12-121">Any integer.</span></span>              |
| <span data-ttu-id="43d12-122">**Top**</span><span class="sxs-lookup"><span data-stu-id="43d12-122">**Top**</span></span>    | <span data-ttu-id="43d12-123">**xs:integer**</span><span class="sxs-lookup"><span data-stu-id="43d12-123">**xs:integer**</span></span>            | <span data-ttu-id="43d12-124">Обязательно</span><span class="sxs-lookup"><span data-stu-id="43d12-124">Required</span></span> | <span data-ttu-id="43d12-125">Расстояние от начала до самой верхней точки ограничивающего прямоугольника для элемента.</span><span class="sxs-lookup"><span data-stu-id="43d12-125">The distance from the origin to the topmost point in the bounding box for the element.</span></span>  | <span data-ttu-id="43d12-126">Любое целое число.</span><span class="sxs-lookup"><span data-stu-id="43d12-126">Any integer.</span></span>              |
| <span data-ttu-id="43d12-127">**Width**</span><span class="sxs-lookup"><span data-stu-id="43d12-127">**Width**</span></span>  | <span data-ttu-id="43d12-128">**xs:nonNegativeInteger**</span><span class="sxs-lookup"><span data-stu-id="43d12-128">**xs:nonNegativeInteger**</span></span> | <span data-ttu-id="43d12-129">Обязательно</span><span class="sxs-lookup"><span data-stu-id="43d12-129">Required</span></span> | <span data-ttu-id="43d12-130">Ширина ограничивающего прямоугольника для элемента.</span><span class="sxs-lookup"><span data-stu-id="43d12-130">The width of the bounding box for the element.</span></span>                                          | <span data-ttu-id="43d12-131">Любое неотрицательное целое число.</span><span class="sxs-lookup"><span data-stu-id="43d12-131">Any non-negative integer.</span></span> |
| <span data-ttu-id="43d12-132">**Height**</span><span class="sxs-lookup"><span data-stu-id="43d12-132">**Height**</span></span> | <span data-ttu-id="43d12-133">**xs:nonNegativeInteger**</span><span class="sxs-lookup"><span data-stu-id="43d12-133">**xs:nonNegativeInteger**</span></span> | <span data-ttu-id="43d12-134">Обязательно</span><span class="sxs-lookup"><span data-stu-id="43d12-134">Required</span></span> | <span data-ttu-id="43d12-135">Высота ограничивающего прямоугольника для элемента.</span><span class="sxs-lookup"><span data-stu-id="43d12-135">The height of the bounding box for the element.</span></span>                                         | <span data-ttu-id="43d12-136">Любое неотрицательное целое число.</span><span class="sxs-lookup"><span data-stu-id="43d12-136">Any non-negative integer.</span></span> |



 

## <a name="element-information"></a><span data-ttu-id="43d12-137">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="43d12-137">Element Information</span></span>



|  <span data-ttu-id="43d12-138">Элемент</span><span class="sxs-lookup"><span data-stu-id="43d12-138">Element</span></span>     | <span data-ttu-id="43d12-139">Значение</span><span class="sxs-lookup"><span data-stu-id="43d12-139">Value</span></span>                                                     |
|--------------|-------------------------------------------------------|
| <span data-ttu-id="43d12-140">Тип элемента</span><span class="sxs-lookup"><span data-stu-id="43d12-140">Element type</span></span> | <span data-ttu-id="43d12-141">[**Флагтипе**](flagtype-complex-type.md) complexType</span><span class="sxs-lookup"><span data-stu-id="43d12-141">[**FlagType**](flagtype-complex-type.md) complexType</span></span> |
| <span data-ttu-id="43d12-142">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="43d12-142">Namespace</span></span>    | <span data-ttu-id="43d12-143">urn: schemas-microsoft-com: TabletPC: ричинк</span><span class="sxs-lookup"><span data-stu-id="43d12-143">urn:schemas-microsoft-com:tabletpc:richink</span></span>            |
| <span data-ttu-id="43d12-144">Имя схемы</span><span class="sxs-lookup"><span data-stu-id="43d12-144">Schema name</span></span>  | <span data-ttu-id="43d12-145">Средство чтения журнала</span><span class="sxs-lookup"><span data-stu-id="43d12-145">Journal Reader</span></span>                                        |



 

 

 



