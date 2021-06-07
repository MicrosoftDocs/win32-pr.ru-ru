---
description: Содержит текстовую информацию из заметки журнала.
ms.assetid: 09ec2e8a-bd50-4f82-8ce3-a1c61f48ddb7
title: Элемент Text
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 570f613a06f9fe814bfb1acbdbdba040dbc1119f
ms.sourcegitcommit: c3f669dc1d52278432bf75ad9fddba3257d26aa2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/04/2021
ms.locfileid: "111432329"
---
# <a name="text-element"></a><span data-ttu-id="dfc0c-103">Элемент Text</span><span class="sxs-lookup"><span data-stu-id="dfc0c-103">Text Element</span></span>

<span data-ttu-id="dfc0c-104">Содержит текстовую информацию из заметки журнала.</span><span class="sxs-lookup"><span data-stu-id="dfc0c-104">Contains text information from the Journal note.</span></span>

## <a name="definition"></a><span data-ttu-id="dfc0c-105">Определение</span><span class="sxs-lookup"><span data-stu-id="dfc0c-105">Definition</span></span>

<span data-ttu-id="dfc0c-106">При использовании с [**содержимым**](content-element--journal-reader.md):</span><span class="sxs-lookup"><span data-stu-id="dfc0c-106">When used with [**Content**](content-element--journal-reader.md):</span></span>

``` syntax
<xs:element name="Text" type="TextType" />
```

<span data-ttu-id="dfc0c-107">Или при использовании с [**титлеинфо**](titleinfo-element.md) и [**граупноде**](groupnode-element.md):</span><span class="sxs-lookup"><span data-stu-id="dfc0c-107">Or, when used with [**TitleInfo**](titleinfo-element.md) and [**GroupNode**](groupnode-element.md):</span></span>

``` syntax
<xs:element name="Text" type="xs:string" />
```

## <a name="parent-elements"></a><span data-ttu-id="dfc0c-108">Родительские элементы</span><span class="sxs-lookup"><span data-stu-id="dfc0c-108">Parent Elements</span></span>

[<span data-ttu-id="dfc0c-109">**Содержани**</span><span class="sxs-lookup"><span data-stu-id="dfc0c-109">**Content**</span></span>](content-element--journal-reader.md)

[<span data-ttu-id="dfc0c-110">**граупноде**</span><span class="sxs-lookup"><span data-stu-id="dfc0c-110">**GroupNode**</span></span>](groupnode-element.md)

[<span data-ttu-id="dfc0c-111">**титлеинфо**</span><span class="sxs-lookup"><span data-stu-id="dfc0c-111">**TitleInfo**</span></span>](titleinfo-element.md)

## <a name="child-elements"></a><span data-ttu-id="dfc0c-112">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="dfc0c-112">Child Elements</span></span>

<span data-ttu-id="dfc0c-113">Отсутствует.</span><span class="sxs-lookup"><span data-stu-id="dfc0c-113">None.</span></span>

## <a name="attributes"></a><span data-ttu-id="dfc0c-114">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="dfc0c-114">Attributes</span></span>

<span data-ttu-id="dfc0c-115">При использовании с [**титлеинфо**](titleinfo-element.md) и [**граупноде**](groupnode-element.md)атрибуты не используются.</span><span class="sxs-lookup"><span data-stu-id="dfc0c-115">There are no attributes when used with [**TitleInfo**](titleinfo-element.md) and [**GroupNode**](groupnode-element.md).</span></span> <span data-ttu-id="dfc0c-116">При использовании с [**содержимым**](content-element--journal-reader.md)атрибуты выглядят следующим образом.</span><span class="sxs-lookup"><span data-stu-id="dfc0c-116">When used with [**Content**](content-element--journal-reader.md), the attributes are as follows.</span></span>



| <span data-ttu-id="dfc0c-117">attribute</span><span class="sxs-lookup"><span data-stu-id="dfc0c-117">Attribute</span></span>  | <span data-ttu-id="dfc0c-118">Тип</span><span class="sxs-lookup"><span data-stu-id="dfc0c-118">Type</span></span>                      | <span data-ttu-id="dfc0c-119">Обязательно</span><span class="sxs-lookup"><span data-stu-id="dfc0c-119">Required</span></span> | <span data-ttu-id="dfc0c-120">Описание</span><span class="sxs-lookup"><span data-stu-id="dfc0c-120">Description</span></span>                                                                             | <span data-ttu-id="dfc0c-121">Возможные значения</span><span class="sxs-lookup"><span data-stu-id="dfc0c-121">Possible Values</span></span>           |
|------------|---------------------------|----------|-----------------------------------------------------------------------------------------|---------------------------|
| <span data-ttu-id="dfc0c-122">**Слева**</span><span class="sxs-lookup"><span data-stu-id="dfc0c-122">**Left**</span></span>   | <span data-ttu-id="dfc0c-123">**xs:integer**</span><span class="sxs-lookup"><span data-stu-id="dfc0c-123">**xs:integer**</span></span>            | <span data-ttu-id="dfc0c-124">Обязательно</span><span class="sxs-lookup"><span data-stu-id="dfc0c-124">Required</span></span> | <span data-ttu-id="dfc0c-125">Расстояние от начала до крайней левой точки в ограничивающем прямоугольнике для элемента.</span><span class="sxs-lookup"><span data-stu-id="dfc0c-125">The distance from the origin to the leftmost point in the bounding box for the element.</span></span> | <span data-ttu-id="dfc0c-126">Любое целое число.</span><span class="sxs-lookup"><span data-stu-id="dfc0c-126">Any integer.</span></span>              |
| <span data-ttu-id="dfc0c-127">**Top**</span><span class="sxs-lookup"><span data-stu-id="dfc0c-127">**Top**</span></span>    | <span data-ttu-id="dfc0c-128">**xs:integer**</span><span class="sxs-lookup"><span data-stu-id="dfc0c-128">**xs:integer**</span></span>            | <span data-ttu-id="dfc0c-129">Обязательно</span><span class="sxs-lookup"><span data-stu-id="dfc0c-129">Required</span></span> | <span data-ttu-id="dfc0c-130">Расстояние от начала до самой верхней точки ограничивающего прямоугольника для элемента.</span><span class="sxs-lookup"><span data-stu-id="dfc0c-130">The distance from the origin to the topmost point in the bounding box for the element.</span></span>  | <span data-ttu-id="dfc0c-131">Любое целое число.</span><span class="sxs-lookup"><span data-stu-id="dfc0c-131">Any integer.</span></span>              |
| <span data-ttu-id="dfc0c-132">**Width**</span><span class="sxs-lookup"><span data-stu-id="dfc0c-132">**Width**</span></span>  | <span data-ttu-id="dfc0c-133">**xs:nonNegativeInteger**</span><span class="sxs-lookup"><span data-stu-id="dfc0c-133">**xs:nonNegativeInteger**</span></span> | <span data-ttu-id="dfc0c-134">Обязательно</span><span class="sxs-lookup"><span data-stu-id="dfc0c-134">Required</span></span> | <span data-ttu-id="dfc0c-135">Ширина ограничивающего прямоугольника для элемента.</span><span class="sxs-lookup"><span data-stu-id="dfc0c-135">The width of the bounding box for the element.</span></span>                                          | <span data-ttu-id="dfc0c-136">Любое неотрицательное целое число.</span><span class="sxs-lookup"><span data-stu-id="dfc0c-136">Any non-negative integer.</span></span> |
| <span data-ttu-id="dfc0c-137">**Height**</span><span class="sxs-lookup"><span data-stu-id="dfc0c-137">**Height**</span></span> | <span data-ttu-id="dfc0c-138">**xs:nonNegativeInteger**</span><span class="sxs-lookup"><span data-stu-id="dfc0c-138">**xs:nonNegativeInteger**</span></span> | <span data-ttu-id="dfc0c-139">Обязательно</span><span class="sxs-lookup"><span data-stu-id="dfc0c-139">Required</span></span> | <span data-ttu-id="dfc0c-140">Высота ограничивающего прямоугольника для элемента.</span><span class="sxs-lookup"><span data-stu-id="dfc0c-140">The height of the bounding box for the element.</span></span>                                         | <span data-ttu-id="dfc0c-141">Любое неотрицательное целое число.</span><span class="sxs-lookup"><span data-stu-id="dfc0c-141">Any non-negative integer.</span></span> |



 

## <a name="element-information"></a><span data-ttu-id="dfc0c-142">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="dfc0c-142">Element Information</span></span>



|   <span data-ttu-id="dfc0c-143">Элемент</span><span class="sxs-lookup"><span data-stu-id="dfc0c-143">Element</span></span>           |   <span data-ttu-id="dfc0c-144">Значение</span><span class="sxs-lookup"><span data-stu-id="dfc0c-144">Value</span></span>                                |
|--------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="dfc0c-145">Тип элемента</span><span class="sxs-lookup"><span data-stu-id="dfc0c-145">Element type</span></span> | <span data-ttu-id="dfc0c-146">[**Тексттипе**](texttype-complex-type.md) complexType (с элементом Content) или **xs: String** (с элементами [**граупноде**](groupnode-element.md) и [**титлеинфо**](titleinfo-element.md) )</span><span class="sxs-lookup"><span data-stu-id="dfc0c-146">[**TextType**](texttype-complex-type.md) complexType (with the Content element) or **xs:string** (with [**GroupNode**](groupnode-element.md) and [**TitleInfo**](titleinfo-element.md) elements)</span></span> |
| <span data-ttu-id="dfc0c-147">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="dfc0c-147">Namespace</span></span>    | <span data-ttu-id="dfc0c-148">urn: schemas-microsoft-com: TabletPC: ричинк</span><span class="sxs-lookup"><span data-stu-id="dfc0c-148">urn:schemas-microsoft-com:tabletpc:richink</span></span><br/>                                                                                                                                               |
| <span data-ttu-id="dfc0c-149">Имя схемы</span><span class="sxs-lookup"><span data-stu-id="dfc0c-149">Schema name</span></span>  | <span data-ttu-id="dfc0c-150">Средство чтения журнала</span><span class="sxs-lookup"><span data-stu-id="dfc0c-150">Journal Reader</span></span><br/>                                                                                                                                                                           |



 

 

 




