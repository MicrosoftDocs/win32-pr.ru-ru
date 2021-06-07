---
description: Определяет группу, содержащую набор сгруппированных содержимого в заметке журнала.
ms.assetid: e2561be1-03ce-41f7-9ad4-197d75411c48
title: Группа Контентграуп
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 02e4291da1912c43674871c06fb803e1936f7178
ms.sourcegitcommit: c3f669dc1d52278432bf75ad9fddba3257d26aa2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/04/2021
ms.locfileid: "111432616"
---
# <a name="contentgroup-group"></a><span data-ttu-id="edf16-103">Группа Контентграуп</span><span class="sxs-lookup"><span data-stu-id="edf16-103">ContentGroup Group</span></span>

<span data-ttu-id="edf16-104">Определяет группу, содержащую набор сгруппированных содержимого в заметке журнала.</span><span class="sxs-lookup"><span data-stu-id="edf16-104">Defines a group that contains a set of grouped content in a Journal note.</span></span>

## <a name="definition"></a><span data-ttu-id="edf16-105">Определение</span><span class="sxs-lookup"><span data-stu-id="edf16-105">Definition</span></span>

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

## <a name="child-elements"></a><span data-ttu-id="edf16-106">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="edf16-106">Child Elements</span></span>

[<span data-ttu-id="edf16-107">**граупноде**</span><span class="sxs-lookup"><span data-stu-id="edf16-107">**GroupNode**</span></span>](groupnode-element.md)

[<span data-ttu-id="edf16-108">**Paragraph**</span><span class="sxs-lookup"><span data-stu-id="edf16-108">**Paragraph**</span></span>](paragraph-element.md)

[<span data-ttu-id="edf16-109">**инкворд**</span><span class="sxs-lookup"><span data-stu-id="edf16-109">**InkWord**</span></span>](inkword-element.md)

[<span data-ttu-id="edf16-110">**Рисование**</span><span class="sxs-lookup"><span data-stu-id="edf16-110">**Drawing**</span></span>](drawing-element.md)

[<span data-ttu-id="edf16-111">**Полнотекстовым**</span><span class="sxs-lookup"><span data-stu-id="edf16-111">**Text**</span></span>](text-element.md)

[<span data-ttu-id="edf16-112">**Изображение**</span><span class="sxs-lookup"><span data-stu-id="edf16-112">**Image**</span></span>](docimage-element.md)

[<span data-ttu-id="edf16-113">**Flag**</span><span class="sxs-lookup"><span data-stu-id="edf16-113">**Flag**</span></span>](flag-element.md)

## <a name="attributes"></a><span data-ttu-id="edf16-114">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="edf16-114">Attributes</span></span>



| <span data-ttu-id="edf16-115">attribute</span><span class="sxs-lookup"><span data-stu-id="edf16-115">Attribute</span></span>  | <span data-ttu-id="edf16-116">Тип</span><span class="sxs-lookup"><span data-stu-id="edf16-116">Type</span></span>                      | <span data-ttu-id="edf16-117">Обязательно</span><span class="sxs-lookup"><span data-stu-id="edf16-117">Required</span></span> | <span data-ttu-id="edf16-118">Описание</span><span class="sxs-lookup"><span data-stu-id="edf16-118">Description</span></span>                                                                                        | <span data-ttu-id="edf16-119">поссиблевалуес</span><span class="sxs-lookup"><span data-stu-id="edf16-119">PossibleValues</span></span>                       |
|------------|---------------------------|----------|----------------------------------------------------------------------------------------------------|--------------------------------------|
| <span data-ttu-id="edf16-120">**Слева**</span><span class="sxs-lookup"><span data-stu-id="edf16-120">**Left**</span></span>   | <span data-ttu-id="edf16-121">**xs:integer**</span><span class="sxs-lookup"><span data-stu-id="edf16-121">**xs:integer**</span></span>            | <span data-ttu-id="edf16-122">Обязательно</span><span class="sxs-lookup"><span data-stu-id="edf16-122">Required</span></span> | <span data-ttu-id="edf16-123">Расстояние от начала до крайней левой точки в ограничивающем прямоугольнике для элемента.</span><span class="sxs-lookup"><span data-stu-id="edf16-123">The distance from the origin to the leftmost point in the bounding box for the element.</span></span><br/> | <span data-ttu-id="edf16-124">Любое целое число.</span><span class="sxs-lookup"><span data-stu-id="edf16-124">Any integer.</span></span><br/>              |
| <span data-ttu-id="edf16-125">**Top**</span><span class="sxs-lookup"><span data-stu-id="edf16-125">**Top**</span></span>    | <span data-ttu-id="edf16-126">**xs:integer**</span><span class="sxs-lookup"><span data-stu-id="edf16-126">**xs:integer**</span></span>            | <span data-ttu-id="edf16-127">Обязательно</span><span class="sxs-lookup"><span data-stu-id="edf16-127">Required</span></span> | <span data-ttu-id="edf16-128">Расстояние от начала до самой верхней точки ограничивающего прямоугольника для элемента.</span><span class="sxs-lookup"><span data-stu-id="edf16-128">The distance from the origin to the topmost point in the bounding box for the element.</span></span><br/>  | <span data-ttu-id="edf16-129">Любое целое число.</span><span class="sxs-lookup"><span data-stu-id="edf16-129">Any integer.</span></span><br/>              |
| <span data-ttu-id="edf16-130">**Width**</span><span class="sxs-lookup"><span data-stu-id="edf16-130">**Width**</span></span>  | <span data-ttu-id="edf16-131">**xs:nonNegativeInteger**</span><span class="sxs-lookup"><span data-stu-id="edf16-131">**xs:nonNegativeInteger**</span></span> | <span data-ttu-id="edf16-132">Обязательно</span><span class="sxs-lookup"><span data-stu-id="edf16-132">Required</span></span> | <span data-ttu-id="edf16-133">Ширина ограничивающего прямоугольника для элемента.</span><span class="sxs-lookup"><span data-stu-id="edf16-133">The width of the bounding box for the element.</span></span><br/>                                          | <span data-ttu-id="edf16-134">Любое неотрицательное целое число.</span><span class="sxs-lookup"><span data-stu-id="edf16-134">Any non-negative integer.</span></span><br/> |
| <span data-ttu-id="edf16-135">**Height**</span><span class="sxs-lookup"><span data-stu-id="edf16-135">**Height**</span></span> | <span data-ttu-id="edf16-136">**xs:nonNegativeInteger**</span><span class="sxs-lookup"><span data-stu-id="edf16-136">**xs:nonNegativeInteger**</span></span> | <span data-ttu-id="edf16-137">Обязательно</span><span class="sxs-lookup"><span data-stu-id="edf16-137">Required</span></span> | <span data-ttu-id="edf16-138">Высота ограничивающего прямоугольника для элемента.</span><span class="sxs-lookup"><span data-stu-id="edf16-138">The height of the bounding box for the element.</span></span><br/>                                         | <span data-ttu-id="edf16-139">Любое неотрицательное целое число.</span><span class="sxs-lookup"><span data-stu-id="edf16-139">Any non-negative integer.</span></span><br/> |



 

## <a name="type-information"></a><span data-ttu-id="edf16-140">Сведения о типе</span><span class="sxs-lookup"><span data-stu-id="edf16-140">Type Information</span></span>



|  <span data-ttu-id="edf16-141">Элемент</span><span class="sxs-lookup"><span data-stu-id="edf16-141">Element</span></span>     | <span data-ttu-id="edf16-142">Значение</span><span class="sxs-lookup"><span data-stu-id="edf16-142">Value</span></span>                                                     |
|-------------|--------------------------------------------|
| <span data-ttu-id="edf16-143">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="edf16-143">Namespace</span></span>   | <span data-ttu-id="edf16-144">urn: schemas-microsoft-com: TabletPC: ричинк</span><span class="sxs-lookup"><span data-stu-id="edf16-144">urn:schemas-microsoft-com:tabletpc:richink</span></span> |
| <span data-ttu-id="edf16-145">Имя схемы</span><span class="sxs-lookup"><span data-stu-id="edf16-145">Schema name</span></span> | <span data-ttu-id="edf16-146">Средство чтения журнала</span><span class="sxs-lookup"><span data-stu-id="edf16-146">Journal Reader</span></span>                             |



 

 

 




