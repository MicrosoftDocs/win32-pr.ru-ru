---
description: Определяет группу атрибутов, используемую различными элементами в XML-файле журнала. Он содержит атрибуты, используемые для определения границ элемента в документе (слева, сверху, высотой и ширины).
ms.assetid: 7841aa65-fb35-4909-a34e-3c883555f764
title: Группа атрибутов Баундстипе
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 411a9d3ec30363e5c405cf27654330a0886f8946
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103807979"
---
# <a name="boundstype-attribute-group"></a><span data-ttu-id="4e278-104">Группа атрибутов Баундстипе</span><span class="sxs-lookup"><span data-stu-id="4e278-104">BoundsType Attribute Group</span></span>

<span data-ttu-id="4e278-105">Определяет группу атрибутов, используемую различными элементами в XML-файле журнала.</span><span class="sxs-lookup"><span data-stu-id="4e278-105">Defines an attribute group that is used by a variety of elements in a Journal XML file.</span></span> <span data-ttu-id="4e278-106">Он содержит атрибуты, используемые для определения границ элемента в документе (слева, сверху, высотой и ширины).</span><span class="sxs-lookup"><span data-stu-id="4e278-106">It contains attributes used to define the bounds (left, top, height, and width) of an element in the document.</span></span>

## <a name="definition"></a><span data-ttu-id="4e278-107">Определение</span><span class="sxs-lookup"><span data-stu-id="4e278-107">Definition</span></span>

``` syntax
<xs:attributeGroup name="BoundsType">
  <xs:attribute name="Left" use="required" type="xs:integer" />
  <xs:attribute name="Top" use="required" type="xs:integer" />
  <xs:attribute name="Width" use="required" type="xs:nonNegativeInteger" />
  <xs:attribute name="Height" use="required" type="xs: nonNegativeInteger" />
</xs:attributeGroup>
```

## <a name="child-elements"></a><span data-ttu-id="4e278-108">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="4e278-108">Child Elements</span></span>

<span data-ttu-id="4e278-109">Отсутствует.</span><span class="sxs-lookup"><span data-stu-id="4e278-109">None.</span></span>

## <a name="attributes"></a><span data-ttu-id="4e278-110">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="4e278-110">Attributes</span></span>



| <span data-ttu-id="4e278-111">attribute</span><span class="sxs-lookup"><span data-stu-id="4e278-111">Attribute</span></span>  | <span data-ttu-id="4e278-112">Тип</span><span class="sxs-lookup"><span data-stu-id="4e278-112">Type</span></span>                      | <span data-ttu-id="4e278-113">Обязательно</span><span class="sxs-lookup"><span data-stu-id="4e278-113">Required</span></span> | <span data-ttu-id="4e278-114">Описание</span><span class="sxs-lookup"><span data-stu-id="4e278-114">Description</span></span>                                                                                        | <span data-ttu-id="4e278-115">поссиблевалуес</span><span class="sxs-lookup"><span data-stu-id="4e278-115">PossibleValues</span></span>                       |
|------------|---------------------------|----------|----------------------------------------------------------------------------------------------------|--------------------------------------|
| <span data-ttu-id="4e278-116">**Слева**</span><span class="sxs-lookup"><span data-stu-id="4e278-116">**Left**</span></span>   | <span data-ttu-id="4e278-117">**xs:integer**</span><span class="sxs-lookup"><span data-stu-id="4e278-117">**xs:integer**</span></span>            | <span data-ttu-id="4e278-118">Обязательно</span><span class="sxs-lookup"><span data-stu-id="4e278-118">Required</span></span> | <span data-ttu-id="4e278-119">Расстояние от начала до крайней левой точки в ограничивающем прямоугольнике для элемента.</span><span class="sxs-lookup"><span data-stu-id="4e278-119">The distance from the origin to the leftmost point in the bounding box for the element.</span></span><br/> | <span data-ttu-id="4e278-120">Любое целое число.</span><span class="sxs-lookup"><span data-stu-id="4e278-120">Any integer.</span></span><br/>              |
| <span data-ttu-id="4e278-121">**Top**</span><span class="sxs-lookup"><span data-stu-id="4e278-121">**Top**</span></span>    | <span data-ttu-id="4e278-122">**xs:integer**</span><span class="sxs-lookup"><span data-stu-id="4e278-122">**xs:integer**</span></span>            | <span data-ttu-id="4e278-123">Обязательно</span><span class="sxs-lookup"><span data-stu-id="4e278-123">Required</span></span> | <span data-ttu-id="4e278-124">Расстояние от начала до самой верхней точки ограничивающего прямоугольника для элемента.</span><span class="sxs-lookup"><span data-stu-id="4e278-124">The distance from the origin to the topmost point in the bounding box for the element.</span></span><br/>  | <span data-ttu-id="4e278-125">Любое целое число.</span><span class="sxs-lookup"><span data-stu-id="4e278-125">Any integer.</span></span><br/>              |
| <span data-ttu-id="4e278-126">**Width**</span><span class="sxs-lookup"><span data-stu-id="4e278-126">**Width**</span></span>  | <span data-ttu-id="4e278-127">**xs:nonNegativeInteger**</span><span class="sxs-lookup"><span data-stu-id="4e278-127">**xs:nonNegativeInteger**</span></span> | <span data-ttu-id="4e278-128">Обязательно</span><span class="sxs-lookup"><span data-stu-id="4e278-128">Required</span></span> | <span data-ttu-id="4e278-129">Ширина ограничивающего прямоугольника для элемента.</span><span class="sxs-lookup"><span data-stu-id="4e278-129">The width of the bounding box for the element.</span></span><br/>                                          | <span data-ttu-id="4e278-130">Любое неотрицательное целое число.</span><span class="sxs-lookup"><span data-stu-id="4e278-130">Any non-negative integer.</span></span><br/> |
| <span data-ttu-id="4e278-131">**Height**</span><span class="sxs-lookup"><span data-stu-id="4e278-131">**Height**</span></span> | <span data-ttu-id="4e278-132">**xs:nonNegativeInteger**</span><span class="sxs-lookup"><span data-stu-id="4e278-132">**xs:nonNegativeInteger**</span></span> | <span data-ttu-id="4e278-133">Обязательно</span><span class="sxs-lookup"><span data-stu-id="4e278-133">Required</span></span> | <span data-ttu-id="4e278-134">Высота ограничивающего прямоугольника для элемента.</span><span class="sxs-lookup"><span data-stu-id="4e278-134">The height of the bounding box for the element.</span></span><br/>                                         | <span data-ttu-id="4e278-135">Любое неотрицательное целое число.</span><span class="sxs-lookup"><span data-stu-id="4e278-135">Any non-negative integer.</span></span><br/> |



 

## <a name="type-information"></a><span data-ttu-id="4e278-136">Сведения о типе</span><span class="sxs-lookup"><span data-stu-id="4e278-136">Type Information</span></span>



|             |                                            |
|-------------|--------------------------------------------|
| <span data-ttu-id="4e278-137">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="4e278-137">Namespace</span></span>   | <span data-ttu-id="4e278-138">urn: schemas-microsoft-com: TabletPC: ричинк</span><span class="sxs-lookup"><span data-stu-id="4e278-138">urn:schemas-microsoft-com:tabletpc:richink</span></span> |
| <span data-ttu-id="4e278-139">Имя схемы</span><span class="sxs-lookup"><span data-stu-id="4e278-139">Schema name</span></span> | <span data-ttu-id="4e278-140">Средство чтения журнала</span><span class="sxs-lookup"><span data-stu-id="4e278-140">Journal Reader</span></span>                             |



 

## <a name="remarks"></a><span data-ttu-id="4e278-141">Комментарии</span><span class="sxs-lookup"><span data-stu-id="4e278-141">Remarks</span></span>

<span data-ttu-id="4e278-142">**Left** и **Top** могут быть отрицательными, так как источник определяется полями, а не страницей.</span><span class="sxs-lookup"><span data-stu-id="4e278-142">**Left** and **Top** can be negative because the origin is defined by the margins, not the page.</span></span>

 

 




