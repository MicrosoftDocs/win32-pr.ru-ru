---
description: Содержит битовую карту в кодировке Base64 для флага, связанного с разделом заметки журнала.
ms.assetid: 612f8814-ab3c-4a3e-9791-525788d4cc72
title: Flag, элемент
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3b6eda9aeb29c07c0de05eadffb8ba8d60f81954
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105701609"
---
# <a name="flag-element"></a><span data-ttu-id="a26c7-103">Flag, элемент</span><span class="sxs-lookup"><span data-stu-id="a26c7-103">Flag Element</span></span>

<span data-ttu-id="a26c7-104">Содержит битовую карту в кодировке Base64 для флага, связанного с разделом заметки журнала.</span><span class="sxs-lookup"><span data-stu-id="a26c7-104">Contains a base64 encoded bitmap of a flag associated with section of a Journal note.</span></span>

## <a name="definition"></a><span data-ttu-id="a26c7-105">Определение</span><span class="sxs-lookup"><span data-stu-id="a26c7-105">Definition</span></span>

``` syntax
<xs:element name="Flag" type="FlagType" minOccurs="0" maxOccurs="unbounded" />
```

## <a name="parent-elements"></a><span data-ttu-id="a26c7-106">Родительские элементы</span><span class="sxs-lookup"><span data-stu-id="a26c7-106">Parent Elements</span></span>

[<span data-ttu-id="a26c7-107">**Содержани**</span><span class="sxs-lookup"><span data-stu-id="a26c7-107">**Content**</span></span>](content-element--journal-reader.md)

[<span data-ttu-id="a26c7-108">**граупноде**</span><span class="sxs-lookup"><span data-stu-id="a26c7-108">**GroupNode**</span></span>](groupnode-element.md)

## <a name="child-elements"></a><span data-ttu-id="a26c7-109">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="a26c7-109">Child Elements</span></span>

<span data-ttu-id="a26c7-110">Отсутствует.</span><span class="sxs-lookup"><span data-stu-id="a26c7-110">None.</span></span>

## <a name="attributes"></a><span data-ttu-id="a26c7-111">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="a26c7-111">Attributes</span></span>



| <span data-ttu-id="a26c7-112">attribute</span><span class="sxs-lookup"><span data-stu-id="a26c7-112">Attribute</span></span>  | <span data-ttu-id="a26c7-113">Тип</span><span class="sxs-lookup"><span data-stu-id="a26c7-113">Type</span></span>                      | <span data-ttu-id="a26c7-114">Обязательно</span><span class="sxs-lookup"><span data-stu-id="a26c7-114">Required</span></span> | <span data-ttu-id="a26c7-115">Описание</span><span class="sxs-lookup"><span data-stu-id="a26c7-115">Description</span></span>                                                                             | <span data-ttu-id="a26c7-116">Возможные значения</span><span class="sxs-lookup"><span data-stu-id="a26c7-116">Possible Values</span></span>           |
|------------|---------------------------|----------|-----------------------------------------------------------------------------------------|---------------------------|
| <span data-ttu-id="a26c7-117">**Слева**</span><span class="sxs-lookup"><span data-stu-id="a26c7-117">**Left**</span></span>   | <span data-ttu-id="a26c7-118">**xs:integer**</span><span class="sxs-lookup"><span data-stu-id="a26c7-118">**xs:integer**</span></span>            | <span data-ttu-id="a26c7-119">Обязательно</span><span class="sxs-lookup"><span data-stu-id="a26c7-119">Required</span></span> | <span data-ttu-id="a26c7-120">Расстояние от начала до крайней левой точки в ограничивающем прямоугольнике для элемента.</span><span class="sxs-lookup"><span data-stu-id="a26c7-120">The distance from the origin to the leftmost point in the bounding box for the element.</span></span> | <span data-ttu-id="a26c7-121">Любое целое число.</span><span class="sxs-lookup"><span data-stu-id="a26c7-121">Any integer.</span></span>              |
| <span data-ttu-id="a26c7-122">**Top**</span><span class="sxs-lookup"><span data-stu-id="a26c7-122">**Top**</span></span>    | <span data-ttu-id="a26c7-123">**xs:integer**</span><span class="sxs-lookup"><span data-stu-id="a26c7-123">**xs:integer**</span></span>            | <span data-ttu-id="a26c7-124">Обязательно</span><span class="sxs-lookup"><span data-stu-id="a26c7-124">Required</span></span> | <span data-ttu-id="a26c7-125">Расстояние от начала до самой верхней точки ограничивающего прямоугольника для элемента.</span><span class="sxs-lookup"><span data-stu-id="a26c7-125">The distance from the origin to the topmost point in the bounding box for the element.</span></span>  | <span data-ttu-id="a26c7-126">Любое целое число.</span><span class="sxs-lookup"><span data-stu-id="a26c7-126">Any integer.</span></span>              |
| <span data-ttu-id="a26c7-127">**Width**</span><span class="sxs-lookup"><span data-stu-id="a26c7-127">**Width**</span></span>  | <span data-ttu-id="a26c7-128">**xs:nonNegativeInteger**</span><span class="sxs-lookup"><span data-stu-id="a26c7-128">**xs:nonNegativeInteger**</span></span> | <span data-ttu-id="a26c7-129">Обязательно</span><span class="sxs-lookup"><span data-stu-id="a26c7-129">Required</span></span> | <span data-ttu-id="a26c7-130">Ширина ограничивающего прямоугольника для элемента.</span><span class="sxs-lookup"><span data-stu-id="a26c7-130">The width of the bounding box for the element.</span></span>                                          | <span data-ttu-id="a26c7-131">Любое неотрицательное целое число.</span><span class="sxs-lookup"><span data-stu-id="a26c7-131">Any non-negative integer.</span></span> |
| <span data-ttu-id="a26c7-132">**Height**</span><span class="sxs-lookup"><span data-stu-id="a26c7-132">**Height**</span></span> | <span data-ttu-id="a26c7-133">**xs:nonNegativeInteger**</span><span class="sxs-lookup"><span data-stu-id="a26c7-133">**xs:nonNegativeInteger**</span></span> | <span data-ttu-id="a26c7-134">Обязательно</span><span class="sxs-lookup"><span data-stu-id="a26c7-134">Required</span></span> | <span data-ttu-id="a26c7-135">Высота ограничивающего прямоугольника для элемента.</span><span class="sxs-lookup"><span data-stu-id="a26c7-135">The height of the bounding box for the element.</span></span>                                         | <span data-ttu-id="a26c7-136">Любое неотрицательное целое число.</span><span class="sxs-lookup"><span data-stu-id="a26c7-136">Any non-negative integer.</span></span> |



 

## <a name="element-information"></a><span data-ttu-id="a26c7-137">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="a26c7-137">Element Information</span></span>



|              |                                                       |
|--------------|-------------------------------------------------------|
| <span data-ttu-id="a26c7-138">Тип элемента</span><span class="sxs-lookup"><span data-stu-id="a26c7-138">Element type</span></span> | <span data-ttu-id="a26c7-139">[**Флагтипе**](flagtype-complex-type.md) complexType</span><span class="sxs-lookup"><span data-stu-id="a26c7-139">[**FlagType**](flagtype-complex-type.md) complexType</span></span> |
| <span data-ttu-id="a26c7-140">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="a26c7-140">Namespace</span></span>    | <span data-ttu-id="a26c7-141">urn: schemas-microsoft-com: TabletPC: ричинк</span><span class="sxs-lookup"><span data-stu-id="a26c7-141">urn:schemas-microsoft-com:tabletpc:richink</span></span>            |
| <span data-ttu-id="a26c7-142">Имя схемы</span><span class="sxs-lookup"><span data-stu-id="a26c7-142">Schema name</span></span>  | <span data-ttu-id="a26c7-143">Средство чтения журнала</span><span class="sxs-lookup"><span data-stu-id="a26c7-143">Journal Reader</span></span>                                        |



 

 

 



