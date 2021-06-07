---
description: Содержит сведения о заданном рукописном слове в заметке журнала, включая размещение, чередование и фактические рукописные данные.
ms.assetid: 1e197716-bf6c-4a28-ae66-38aa59d7371d
title: Инкворд, элемент
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e8dc9baea7cda0346e82c11331c45f453e61f192
ms.sourcegitcommit: c3f669dc1d52278432bf75ad9fddba3257d26aa2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/04/2021
ms.locfileid: "111432396"
---
# <a name="inkword-element"></a><span data-ttu-id="183c9-103">Инкворд, элемент</span><span class="sxs-lookup"><span data-stu-id="183c9-103">InkWord Element</span></span>

<span data-ttu-id="183c9-104">Содержит сведения о заданном рукописном слове в заметке журнала, включая размещение, чередование и фактические рукописные данные.</span><span class="sxs-lookup"><span data-stu-id="183c9-104">Contains information about a given ink word in the Journal note, including position, alternates, and the actual ink data.</span></span>

## <a name="definition"></a><span data-ttu-id="183c9-105">Определение</span><span class="sxs-lookup"><span data-stu-id="183c9-105">Definition</span></span>

``` syntax
<xs:element name="InkWord" type="InkWordType" />
```

## <a name="parent-elements"></a><span data-ttu-id="183c9-106">Родительские элементы</span><span class="sxs-lookup"><span data-stu-id="183c9-106">Parent Elements</span></span>

[<span data-ttu-id="183c9-107">**граупноде**</span><span class="sxs-lookup"><span data-stu-id="183c9-107">**GroupNode**</span></span>](groupnode-element.md)

[<span data-ttu-id="183c9-108">**Штрих**</span><span class="sxs-lookup"><span data-stu-id="183c9-108">**Line**</span></span>](line-element.md)

## <a name="child-elements"></a><span data-ttu-id="183c9-109">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="183c9-109">Child Elements</span></span>

[<span data-ttu-id="183c9-110">**скалартрансформ**</span><span class="sxs-lookup"><span data-stu-id="183c9-110">**ScalarTransform**</span></span>](scalartransform-element.md)

[<span data-ttu-id="183c9-111">**алтернателист**</span><span class="sxs-lookup"><span data-stu-id="183c9-111">**AlternateList**</span></span>](alternatelist-element.md)

[<span data-ttu-id="183c9-112">**канреклассифи**</span><span class="sxs-lookup"><span data-stu-id="183c9-112">**CanReClassify**</span></span>](canreclassify-element.md)

[<span data-ttu-id="183c9-113">**Уровень**</span><span class="sxs-lookup"><span data-stu-id="183c9-113">**Confidence**</span></span>](confidence-element.md)

[<span data-ttu-id="183c9-114">**инкобжект**</span><span class="sxs-lookup"><span data-stu-id="183c9-114">**InkObject**</span></span>](inkobject-element.md)

## <a name="attributes"></a><span data-ttu-id="183c9-115">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="183c9-115">Attributes</span></span>



| <span data-ttu-id="183c9-116">attribute</span><span class="sxs-lookup"><span data-stu-id="183c9-116">Attribute</span></span>  | <span data-ttu-id="183c9-117">Тип</span><span class="sxs-lookup"><span data-stu-id="183c9-117">Type</span></span>                      | <span data-ttu-id="183c9-118">Обязательно</span><span class="sxs-lookup"><span data-stu-id="183c9-118">Required</span></span> | <span data-ttu-id="183c9-119">Описание</span><span class="sxs-lookup"><span data-stu-id="183c9-119">Description</span></span>                                                                             | <span data-ttu-id="183c9-120">Возможные значения</span><span class="sxs-lookup"><span data-stu-id="183c9-120">Possible Values</span></span>           |
|------------|---------------------------|----------|-----------------------------------------------------------------------------------------|---------------------------|
| <span data-ttu-id="183c9-121">**Слева**</span><span class="sxs-lookup"><span data-stu-id="183c9-121">**Left**</span></span>   | <span data-ttu-id="183c9-122">**xs:integer**</span><span class="sxs-lookup"><span data-stu-id="183c9-122">**xs:integer**</span></span>            | <span data-ttu-id="183c9-123">Обязательно</span><span class="sxs-lookup"><span data-stu-id="183c9-123">Required</span></span> | <span data-ttu-id="183c9-124">Расстояние от начала до крайней левой точки в ограничивающем прямоугольнике для элемента.</span><span class="sxs-lookup"><span data-stu-id="183c9-124">The distance from the origin to the leftmost point in the bounding box for the element.</span></span> | <span data-ttu-id="183c9-125">Любое целое число.</span><span class="sxs-lookup"><span data-stu-id="183c9-125">Any integer.</span></span>              |
| <span data-ttu-id="183c9-126">**Top**</span><span class="sxs-lookup"><span data-stu-id="183c9-126">**Top**</span></span>    | <span data-ttu-id="183c9-127">**xs:integer**</span><span class="sxs-lookup"><span data-stu-id="183c9-127">**xs:integer**</span></span>            | <span data-ttu-id="183c9-128">Обязательно</span><span class="sxs-lookup"><span data-stu-id="183c9-128">Required</span></span> | <span data-ttu-id="183c9-129">Расстояние от начала до самой верхней точки ограничивающего прямоугольника для элемента.</span><span class="sxs-lookup"><span data-stu-id="183c9-129">The distance from the origin to the topmost point in the bounding box for the element.</span></span>  | <span data-ttu-id="183c9-130">Любое целое число.</span><span class="sxs-lookup"><span data-stu-id="183c9-130">Any integer.</span></span>              |
| <span data-ttu-id="183c9-131">**Width**</span><span class="sxs-lookup"><span data-stu-id="183c9-131">**Width**</span></span>  | <span data-ttu-id="183c9-132">**xs:nonNegativeInteger**</span><span class="sxs-lookup"><span data-stu-id="183c9-132">**xs:nonNegativeInteger**</span></span> | <span data-ttu-id="183c9-133">Обязательно</span><span class="sxs-lookup"><span data-stu-id="183c9-133">Required</span></span> | <span data-ttu-id="183c9-134">Ширина ограничивающего прямоугольника для элемента.</span><span class="sxs-lookup"><span data-stu-id="183c9-134">The width of the bounding box for the element.</span></span>                                          | <span data-ttu-id="183c9-135">Любое неотрицательное целое число.</span><span class="sxs-lookup"><span data-stu-id="183c9-135">Any non-negative integer.</span></span> |
| <span data-ttu-id="183c9-136">**Height**</span><span class="sxs-lookup"><span data-stu-id="183c9-136">**Height**</span></span> | <span data-ttu-id="183c9-137">**xs:nonNegativeInteger**</span><span class="sxs-lookup"><span data-stu-id="183c9-137">**xs:nonNegativeInteger**</span></span> | <span data-ttu-id="183c9-138">Обязательно</span><span class="sxs-lookup"><span data-stu-id="183c9-138">Required</span></span> | <span data-ttu-id="183c9-139">Высота ограничивающего прямоугольника для элемента.</span><span class="sxs-lookup"><span data-stu-id="183c9-139">The height of the bounding box for the element.</span></span>                                         | <span data-ttu-id="183c9-140">Любое неотрицательное целое число.</span><span class="sxs-lookup"><span data-stu-id="183c9-140">Any non-negative integer.</span></span> |



 

> [!WARNING]
> <span data-ttu-id="183c9-141">Внутреннее координатное сопоставленное слово — это английские единицы метрики, а в приложении необходимо использовать множитель 2,54, чтобы преобразовать значения ширины и высоты в единицы HIMETRIC, используемые интерфейсами API платформы Tablet PC.</span><span class="sxs-lookup"><span data-stu-id="183c9-141">The ink word's internal coordinate mapping is English Metric Units and a multiplier of 2.54 will need to be used by your application to convert the Width and Height values to the HIMETRIC units used by the Tablet PC platform APIs.</span></span>

 

## <a name="element-information"></a><span data-ttu-id="183c9-142">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="183c9-142">Element Information</span></span>



|  <span data-ttu-id="183c9-143">Элемент</span><span class="sxs-lookup"><span data-stu-id="183c9-143">Element</span></span>     | <span data-ttu-id="183c9-144">Значение</span><span class="sxs-lookup"><span data-stu-id="183c9-144">Value</span></span>                                                     |
|--------------|-------------------------------------------------------------|
| <span data-ttu-id="183c9-145">Тип элемента</span><span class="sxs-lookup"><span data-stu-id="183c9-145">Element type</span></span> | <span data-ttu-id="183c9-146">[**Инквордтипе**](inkwordtype-complex-type.md) complexType</span><span class="sxs-lookup"><span data-stu-id="183c9-146">[**InkWordType**](inkwordtype-complex-type.md) complexType</span></span> |
| <span data-ttu-id="183c9-147">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="183c9-147">Namespace</span></span>    | <span data-ttu-id="183c9-148">urn: schemas-microsoft-com: TabletPC: ричинк</span><span class="sxs-lookup"><span data-stu-id="183c9-148">urn:schemas-microsoft-com:tabletpc:richink</span></span>                  |
| <span data-ttu-id="183c9-149">Имя схемы</span><span class="sxs-lookup"><span data-stu-id="183c9-149">Schema name</span></span>  | <span data-ttu-id="183c9-150">Средство чтения журнала</span><span class="sxs-lookup"><span data-stu-id="183c9-150">Journal Reader</span></span>                                              |



 

 

 



