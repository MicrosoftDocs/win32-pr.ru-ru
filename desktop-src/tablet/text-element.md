---
description: Содержит текстовую информацию из заметки журнала.
ms.assetid: 09ec2e8a-bd50-4f82-8ce3-a1c61f48ddb7
title: Элемент Text
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ed9c72fe584d0e796d4a6f897297aa60bbeddc5d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103999424"
---
# <a name="text-element"></a><span data-ttu-id="0fa63-103">Элемент Text</span><span class="sxs-lookup"><span data-stu-id="0fa63-103">Text Element</span></span>

<span data-ttu-id="0fa63-104">Содержит текстовую информацию из заметки журнала.</span><span class="sxs-lookup"><span data-stu-id="0fa63-104">Contains text information from the Journal note.</span></span>

## <a name="definition"></a><span data-ttu-id="0fa63-105">Определение</span><span class="sxs-lookup"><span data-stu-id="0fa63-105">Definition</span></span>

<span data-ttu-id="0fa63-106">При использовании с [**содержимым**](content-element--journal-reader.md):</span><span class="sxs-lookup"><span data-stu-id="0fa63-106">When used with [**Content**](content-element--journal-reader.md):</span></span>

``` syntax
<xs:element name="Text" type="TextType" />
```

<span data-ttu-id="0fa63-107">Или при использовании с [**титлеинфо**](titleinfo-element.md) и [**граупноде**](groupnode-element.md):</span><span class="sxs-lookup"><span data-stu-id="0fa63-107">Or, when used with [**TitleInfo**](titleinfo-element.md) and [**GroupNode**](groupnode-element.md):</span></span>

``` syntax
<xs:element name="Text" type="xs:string" />
```

## <a name="parent-elements"></a><span data-ttu-id="0fa63-108">Родительские элементы</span><span class="sxs-lookup"><span data-stu-id="0fa63-108">Parent Elements</span></span>

[<span data-ttu-id="0fa63-109">**Содержани**</span><span class="sxs-lookup"><span data-stu-id="0fa63-109">**Content**</span></span>](content-element--journal-reader.md)

[<span data-ttu-id="0fa63-110">**граупноде**</span><span class="sxs-lookup"><span data-stu-id="0fa63-110">**GroupNode**</span></span>](groupnode-element.md)

[<span data-ttu-id="0fa63-111">**титлеинфо**</span><span class="sxs-lookup"><span data-stu-id="0fa63-111">**TitleInfo**</span></span>](titleinfo-element.md)

## <a name="child-elements"></a><span data-ttu-id="0fa63-112">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="0fa63-112">Child Elements</span></span>

<span data-ttu-id="0fa63-113">Отсутствует.</span><span class="sxs-lookup"><span data-stu-id="0fa63-113">None.</span></span>

## <a name="attributes"></a><span data-ttu-id="0fa63-114">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="0fa63-114">Attributes</span></span>

<span data-ttu-id="0fa63-115">При использовании с [**титлеинфо**](titleinfo-element.md) и [**граупноде**](groupnode-element.md)атрибуты не используются.</span><span class="sxs-lookup"><span data-stu-id="0fa63-115">There are no attributes when used with [**TitleInfo**](titleinfo-element.md) and [**GroupNode**](groupnode-element.md).</span></span> <span data-ttu-id="0fa63-116">При использовании с [**содержимым**](content-element--journal-reader.md)атрибуты выглядят следующим образом.</span><span class="sxs-lookup"><span data-stu-id="0fa63-116">When used with [**Content**](content-element--journal-reader.md), the attributes are as follows.</span></span>



| <span data-ttu-id="0fa63-117">attribute</span><span class="sxs-lookup"><span data-stu-id="0fa63-117">Attribute</span></span>  | <span data-ttu-id="0fa63-118">Тип</span><span class="sxs-lookup"><span data-stu-id="0fa63-118">Type</span></span>                      | <span data-ttu-id="0fa63-119">Обязательно</span><span class="sxs-lookup"><span data-stu-id="0fa63-119">Required</span></span> | <span data-ttu-id="0fa63-120">Описание</span><span class="sxs-lookup"><span data-stu-id="0fa63-120">Description</span></span>                                                                             | <span data-ttu-id="0fa63-121">Возможные значения</span><span class="sxs-lookup"><span data-stu-id="0fa63-121">Possible Values</span></span>           |
|------------|---------------------------|----------|-----------------------------------------------------------------------------------------|---------------------------|
| <span data-ttu-id="0fa63-122">**Слева**</span><span class="sxs-lookup"><span data-stu-id="0fa63-122">**Left**</span></span>   | <span data-ttu-id="0fa63-123">**xs:integer**</span><span class="sxs-lookup"><span data-stu-id="0fa63-123">**xs:integer**</span></span>            | <span data-ttu-id="0fa63-124">Обязательно</span><span class="sxs-lookup"><span data-stu-id="0fa63-124">Required</span></span> | <span data-ttu-id="0fa63-125">Расстояние от начала до крайней левой точки в ограничивающем прямоугольнике для элемента.</span><span class="sxs-lookup"><span data-stu-id="0fa63-125">The distance from the origin to the leftmost point in the bounding box for the element.</span></span> | <span data-ttu-id="0fa63-126">Любое целое число.</span><span class="sxs-lookup"><span data-stu-id="0fa63-126">Any integer.</span></span>              |
| <span data-ttu-id="0fa63-127">**Top**</span><span class="sxs-lookup"><span data-stu-id="0fa63-127">**Top**</span></span>    | <span data-ttu-id="0fa63-128">**xs:integer**</span><span class="sxs-lookup"><span data-stu-id="0fa63-128">**xs:integer**</span></span>            | <span data-ttu-id="0fa63-129">Обязательно</span><span class="sxs-lookup"><span data-stu-id="0fa63-129">Required</span></span> | <span data-ttu-id="0fa63-130">Расстояние от начала до самой верхней точки ограничивающего прямоугольника для элемента.</span><span class="sxs-lookup"><span data-stu-id="0fa63-130">The distance from the origin to the topmost point in the bounding box for the element.</span></span>  | <span data-ttu-id="0fa63-131">Любое целое число.</span><span class="sxs-lookup"><span data-stu-id="0fa63-131">Any integer.</span></span>              |
| <span data-ttu-id="0fa63-132">**Width**</span><span class="sxs-lookup"><span data-stu-id="0fa63-132">**Width**</span></span>  | <span data-ttu-id="0fa63-133">**xs:nonNegativeInteger**</span><span class="sxs-lookup"><span data-stu-id="0fa63-133">**xs:nonNegativeInteger**</span></span> | <span data-ttu-id="0fa63-134">Обязательно</span><span class="sxs-lookup"><span data-stu-id="0fa63-134">Required</span></span> | <span data-ttu-id="0fa63-135">Ширина ограничивающего прямоугольника для элемента.</span><span class="sxs-lookup"><span data-stu-id="0fa63-135">The width of the bounding box for the element.</span></span>                                          | <span data-ttu-id="0fa63-136">Любое неотрицательное целое число.</span><span class="sxs-lookup"><span data-stu-id="0fa63-136">Any non-negative integer.</span></span> |
| <span data-ttu-id="0fa63-137">**Height**</span><span class="sxs-lookup"><span data-stu-id="0fa63-137">**Height**</span></span> | <span data-ttu-id="0fa63-138">**xs:nonNegativeInteger**</span><span class="sxs-lookup"><span data-stu-id="0fa63-138">**xs:nonNegativeInteger**</span></span> | <span data-ttu-id="0fa63-139">Обязательно</span><span class="sxs-lookup"><span data-stu-id="0fa63-139">Required</span></span> | <span data-ttu-id="0fa63-140">Высота ограничивающего прямоугольника для элемента.</span><span class="sxs-lookup"><span data-stu-id="0fa63-140">The height of the bounding box for the element.</span></span>                                         | <span data-ttu-id="0fa63-141">Любое неотрицательное целое число.</span><span class="sxs-lookup"><span data-stu-id="0fa63-141">Any non-negative integer.</span></span> |



 

## <a name="element-information"></a><span data-ttu-id="0fa63-142">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="0fa63-142">Element Information</span></span>



|              |                                                                                                                                                                                                     |
|--------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0fa63-143">Тип элемента</span><span class="sxs-lookup"><span data-stu-id="0fa63-143">Element type</span></span> | <span data-ttu-id="0fa63-144">[**Тексттипе**](texttype-complex-type.md) complexType (с элементом Content) или **xs: String** (с элементами [**граупноде**](groupnode-element.md) и [**титлеинфо**](titleinfo-element.md) )</span><span class="sxs-lookup"><span data-stu-id="0fa63-144">[**TextType**](texttype-complex-type.md) complexType (with the Content element) or **xs:string** (with [**GroupNode**](groupnode-element.md) and [**TitleInfo**](titleinfo-element.md) elements)</span></span> |
| <span data-ttu-id="0fa63-145">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="0fa63-145">Namespace</span></span>    | <span data-ttu-id="0fa63-146">urn: schemas-microsoft-com: TabletPC: ричинк</span><span class="sxs-lookup"><span data-stu-id="0fa63-146">urn:schemas-microsoft-com:tabletpc:richink</span></span><br/>                                                                                                                                               |
| <span data-ttu-id="0fa63-147">Имя схемы</span><span class="sxs-lookup"><span data-stu-id="0fa63-147">Schema name</span></span>  | <span data-ttu-id="0fa63-148">Средство чтения журнала</span><span class="sxs-lookup"><span data-stu-id="0fa63-148">Journal Reader</span></span><br/>                                                                                                                                                                           |



 

 

 




