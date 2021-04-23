---
description: Определяет группу, содержащую набор сгруппированных содержимого в заметке журнала.
ms.assetid: e2561be1-03ce-41f7-9ad4-197d75411c48
title: Группа Контентграуп
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5fbbc13a3dee796646b6d61ac9ba0bde50880f12
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104081150"
---
# <a name="contentgroup-group"></a><span data-ttu-id="2650a-103">Группа Контентграуп</span><span class="sxs-lookup"><span data-stu-id="2650a-103">ContentGroup Group</span></span>

<span data-ttu-id="2650a-104">Определяет группу, содержащую набор сгруппированных содержимого в заметке журнала.</span><span class="sxs-lookup"><span data-stu-id="2650a-104">Defines a group that contains a set of grouped content in a Journal note.</span></span>

## <a name="definition"></a><span data-ttu-id="2650a-105">Определение</span><span class="sxs-lookup"><span data-stu-id="2650a-105">Definition</span></span>

``` syntax
<xs:group name="ContentGroup" >
  <xs:choice>
    <xs:element name="GroupNode" type="GroupNodeType" />
    <xs:element name="Paragraph" type="ParagraphType" />
    <xs:element name="InkWord" type="InkWordType" />
    <xs:element name="Drawing" type="DrawingType" />
    <xs:element name="Text" type="TextType" />
    <xs:element name="Image" type="ImageType" />
    <xs:element name="Flag" type="FlagType" />
    <xs:element name="Reflow" type="ReflowType" />
  </xs:choice>
</xs:group>
```

## <a name="child-elements"></a><span data-ttu-id="2650a-106">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="2650a-106">Child Elements</span></span>

[<span data-ttu-id="2650a-107">**граупноде**</span><span class="sxs-lookup"><span data-stu-id="2650a-107">**GroupNode**</span></span>](groupnode-element.md)

[<span data-ttu-id="2650a-108">**Paragraph**</span><span class="sxs-lookup"><span data-stu-id="2650a-108">**Paragraph**</span></span>](paragraph-element.md)

[<span data-ttu-id="2650a-109">**инкворд**</span><span class="sxs-lookup"><span data-stu-id="2650a-109">**InkWord**</span></span>](inkword-element.md)

[<span data-ttu-id="2650a-110">**Рисование**</span><span class="sxs-lookup"><span data-stu-id="2650a-110">**Drawing**</span></span>](drawing-element.md)

[<span data-ttu-id="2650a-111">**Полнотекстовым**</span><span class="sxs-lookup"><span data-stu-id="2650a-111">**Text**</span></span>](text-element.md)

[<span data-ttu-id="2650a-112">**Образ**</span><span class="sxs-lookup"><span data-stu-id="2650a-112">**Image**</span></span>](docimage-element.md)

[<span data-ttu-id="2650a-113">**Flag**</span><span class="sxs-lookup"><span data-stu-id="2650a-113">**Flag**</span></span>](flag-element.md)

## <a name="attributes"></a><span data-ttu-id="2650a-114">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="2650a-114">Attributes</span></span>



| <span data-ttu-id="2650a-115">attribute</span><span class="sxs-lookup"><span data-stu-id="2650a-115">Attribute</span></span>  | <span data-ttu-id="2650a-116">Тип</span><span class="sxs-lookup"><span data-stu-id="2650a-116">Type</span></span>                      | <span data-ttu-id="2650a-117">Обязательно</span><span class="sxs-lookup"><span data-stu-id="2650a-117">Required</span></span> | <span data-ttu-id="2650a-118">Описание</span><span class="sxs-lookup"><span data-stu-id="2650a-118">Description</span></span>                                                                                        | <span data-ttu-id="2650a-119">поссиблевалуес</span><span class="sxs-lookup"><span data-stu-id="2650a-119">PossibleValues</span></span>                       |
|------------|---------------------------|----------|----------------------------------------------------------------------------------------------------|--------------------------------------|
| <span data-ttu-id="2650a-120">**Слева**</span><span class="sxs-lookup"><span data-stu-id="2650a-120">**Left**</span></span>   | <span data-ttu-id="2650a-121">**xs:integer**</span><span class="sxs-lookup"><span data-stu-id="2650a-121">**xs:integer**</span></span>            | <span data-ttu-id="2650a-122">Обязательно</span><span class="sxs-lookup"><span data-stu-id="2650a-122">Required</span></span> | <span data-ttu-id="2650a-123">Расстояние от начала до крайней левой точки в ограничивающем прямоугольнике для элемента.</span><span class="sxs-lookup"><span data-stu-id="2650a-123">The distance from the origin to the leftmost point in the bounding box for the element.</span></span><br/> | <span data-ttu-id="2650a-124">Любое целое число.</span><span class="sxs-lookup"><span data-stu-id="2650a-124">Any integer.</span></span><br/>              |
| <span data-ttu-id="2650a-125">**Top**</span><span class="sxs-lookup"><span data-stu-id="2650a-125">**Top**</span></span>    | <span data-ttu-id="2650a-126">**xs:integer**</span><span class="sxs-lookup"><span data-stu-id="2650a-126">**xs:integer**</span></span>            | <span data-ttu-id="2650a-127">Обязательно</span><span class="sxs-lookup"><span data-stu-id="2650a-127">Required</span></span> | <span data-ttu-id="2650a-128">Расстояние от начала до самой верхней точки ограничивающего прямоугольника для элемента.</span><span class="sxs-lookup"><span data-stu-id="2650a-128">The distance from the origin to the topmost point in the bounding box for the element.</span></span><br/>  | <span data-ttu-id="2650a-129">Любое целое число.</span><span class="sxs-lookup"><span data-stu-id="2650a-129">Any integer.</span></span><br/>              |
| <span data-ttu-id="2650a-130">**Width**</span><span class="sxs-lookup"><span data-stu-id="2650a-130">**Width**</span></span>  | <span data-ttu-id="2650a-131">**xs:nonNegativeInteger**</span><span class="sxs-lookup"><span data-stu-id="2650a-131">**xs:nonNegativeInteger**</span></span> | <span data-ttu-id="2650a-132">Обязательно</span><span class="sxs-lookup"><span data-stu-id="2650a-132">Required</span></span> | <span data-ttu-id="2650a-133">Ширина ограничивающего прямоугольника для элемента.</span><span class="sxs-lookup"><span data-stu-id="2650a-133">The width of the bounding box for the element.</span></span><br/>                                          | <span data-ttu-id="2650a-134">Любое неотрицательное целое число.</span><span class="sxs-lookup"><span data-stu-id="2650a-134">Any non-negative integer.</span></span><br/> |
| <span data-ttu-id="2650a-135">**Height**</span><span class="sxs-lookup"><span data-stu-id="2650a-135">**Height**</span></span> | <span data-ttu-id="2650a-136">**xs:nonNegativeInteger**</span><span class="sxs-lookup"><span data-stu-id="2650a-136">**xs:nonNegativeInteger**</span></span> | <span data-ttu-id="2650a-137">Обязательно</span><span class="sxs-lookup"><span data-stu-id="2650a-137">Required</span></span> | <span data-ttu-id="2650a-138">Высота ограничивающего прямоугольника для элемента.</span><span class="sxs-lookup"><span data-stu-id="2650a-138">The height of the bounding box for the element.</span></span><br/>                                         | <span data-ttu-id="2650a-139">Любое неотрицательное целое число.</span><span class="sxs-lookup"><span data-stu-id="2650a-139">Any non-negative integer.</span></span><br/> |



 

## <a name="type-information"></a><span data-ttu-id="2650a-140">Сведения о типе</span><span class="sxs-lookup"><span data-stu-id="2650a-140">Type Information</span></span>



|             |                                            |
|-------------|--------------------------------------------|
| <span data-ttu-id="2650a-141">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="2650a-141">Namespace</span></span>   | <span data-ttu-id="2650a-142">urn: schemas-microsoft-com: TabletPC: ричинк</span><span class="sxs-lookup"><span data-stu-id="2650a-142">urn:schemas-microsoft-com:tabletpc:richink</span></span> |
| <span data-ttu-id="2650a-143">Имя схемы</span><span class="sxs-lookup"><span data-stu-id="2650a-143">Schema name</span></span> | <span data-ttu-id="2650a-144">Средство чтения журнала</span><span class="sxs-lookup"><span data-stu-id="2650a-144">Journal Reader</span></span>                             |



 

 

 




