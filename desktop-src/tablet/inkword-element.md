---
description: Содержит сведения о заданном рукописном слове в заметке журнала, включая размещение, чередование и фактические рукописные данные.
ms.assetid: 1e197716-bf6c-4a28-ae66-38aa59d7371d
title: Инкворд, элемент
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 179fb5e2bcce2e01f684f0b39d662e8538c7d27e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105702414"
---
# <a name="inkword-element"></a><span data-ttu-id="02013-103">Инкворд, элемент</span><span class="sxs-lookup"><span data-stu-id="02013-103">InkWord Element</span></span>

<span data-ttu-id="02013-104">Содержит сведения о заданном рукописном слове в заметке журнала, включая размещение, чередование и фактические рукописные данные.</span><span class="sxs-lookup"><span data-stu-id="02013-104">Contains information about a given ink word in the Journal note, including position, alternates, and the actual ink data.</span></span>

## <a name="definition"></a><span data-ttu-id="02013-105">Определение</span><span class="sxs-lookup"><span data-stu-id="02013-105">Definition</span></span>

``` syntax
<xs:element name="InkWord" type="InkWordType" />
```

## <a name="parent-elements"></a><span data-ttu-id="02013-106">Родительские элементы</span><span class="sxs-lookup"><span data-stu-id="02013-106">Parent Elements</span></span>

[<span data-ttu-id="02013-107">**граупноде**</span><span class="sxs-lookup"><span data-stu-id="02013-107">**GroupNode**</span></span>](groupnode-element.md)

[<span data-ttu-id="02013-108">**Штрих**</span><span class="sxs-lookup"><span data-stu-id="02013-108">**Line**</span></span>](line-element.md)

## <a name="child-elements"></a><span data-ttu-id="02013-109">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="02013-109">Child Elements</span></span>

[<span data-ttu-id="02013-110">**скалартрансформ**</span><span class="sxs-lookup"><span data-stu-id="02013-110">**ScalarTransform**</span></span>](scalartransform-element.md)

[<span data-ttu-id="02013-111">**алтернателист**</span><span class="sxs-lookup"><span data-stu-id="02013-111">**AlternateList**</span></span>](alternatelist-element.md)

[<span data-ttu-id="02013-112">**канреклассифи**</span><span class="sxs-lookup"><span data-stu-id="02013-112">**CanReClassify**</span></span>](canreclassify-element.md)

[<span data-ttu-id="02013-113">**Достоверность**</span><span class="sxs-lookup"><span data-stu-id="02013-113">**Confidence**</span></span>](confidence-element.md)

[<span data-ttu-id="02013-114">**инкобжект**</span><span class="sxs-lookup"><span data-stu-id="02013-114">**InkObject**</span></span>](inkobject-element.md)

## <a name="attributes"></a><span data-ttu-id="02013-115">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="02013-115">Attributes</span></span>



| <span data-ttu-id="02013-116">attribute</span><span class="sxs-lookup"><span data-stu-id="02013-116">Attribute</span></span>  | <span data-ttu-id="02013-117">Тип</span><span class="sxs-lookup"><span data-stu-id="02013-117">Type</span></span>                      | <span data-ttu-id="02013-118">Обязательно</span><span class="sxs-lookup"><span data-stu-id="02013-118">Required</span></span> | <span data-ttu-id="02013-119">Описание</span><span class="sxs-lookup"><span data-stu-id="02013-119">Description</span></span>                                                                             | <span data-ttu-id="02013-120">Возможные значения</span><span class="sxs-lookup"><span data-stu-id="02013-120">Possible Values</span></span>           |
|------------|---------------------------|----------|-----------------------------------------------------------------------------------------|---------------------------|
| <span data-ttu-id="02013-121">**Слева**</span><span class="sxs-lookup"><span data-stu-id="02013-121">**Left**</span></span>   | <span data-ttu-id="02013-122">**xs:integer**</span><span class="sxs-lookup"><span data-stu-id="02013-122">**xs:integer**</span></span>            | <span data-ttu-id="02013-123">Обязательно</span><span class="sxs-lookup"><span data-stu-id="02013-123">Required</span></span> | <span data-ttu-id="02013-124">Расстояние от начала до крайней левой точки в ограничивающем прямоугольнике для элемента.</span><span class="sxs-lookup"><span data-stu-id="02013-124">The distance from the origin to the leftmost point in the bounding box for the element.</span></span> | <span data-ttu-id="02013-125">Любое целое число.</span><span class="sxs-lookup"><span data-stu-id="02013-125">Any integer.</span></span>              |
| <span data-ttu-id="02013-126">**Top**</span><span class="sxs-lookup"><span data-stu-id="02013-126">**Top**</span></span>    | <span data-ttu-id="02013-127">**xs:integer**</span><span class="sxs-lookup"><span data-stu-id="02013-127">**xs:integer**</span></span>            | <span data-ttu-id="02013-128">Обязательно</span><span class="sxs-lookup"><span data-stu-id="02013-128">Required</span></span> | <span data-ttu-id="02013-129">Расстояние от начала до самой верхней точки ограничивающего прямоугольника для элемента.</span><span class="sxs-lookup"><span data-stu-id="02013-129">The distance from the origin to the topmost point in the bounding box for the element.</span></span>  | <span data-ttu-id="02013-130">Любое целое число.</span><span class="sxs-lookup"><span data-stu-id="02013-130">Any integer.</span></span>              |
| <span data-ttu-id="02013-131">**Width**</span><span class="sxs-lookup"><span data-stu-id="02013-131">**Width**</span></span>  | <span data-ttu-id="02013-132">**xs:nonNegativeInteger**</span><span class="sxs-lookup"><span data-stu-id="02013-132">**xs:nonNegativeInteger**</span></span> | <span data-ttu-id="02013-133">Обязательно</span><span class="sxs-lookup"><span data-stu-id="02013-133">Required</span></span> | <span data-ttu-id="02013-134">Ширина ограничивающего прямоугольника для элемента.</span><span class="sxs-lookup"><span data-stu-id="02013-134">The width of the bounding box for the element.</span></span>                                          | <span data-ttu-id="02013-135">Любое неотрицательное целое число.</span><span class="sxs-lookup"><span data-stu-id="02013-135">Any non-negative integer.</span></span> |
| <span data-ttu-id="02013-136">**Height**</span><span class="sxs-lookup"><span data-stu-id="02013-136">**Height**</span></span> | <span data-ttu-id="02013-137">**xs:nonNegativeInteger**</span><span class="sxs-lookup"><span data-stu-id="02013-137">**xs:nonNegativeInteger**</span></span> | <span data-ttu-id="02013-138">Обязательно</span><span class="sxs-lookup"><span data-stu-id="02013-138">Required</span></span> | <span data-ttu-id="02013-139">Высота ограничивающего прямоугольника для элемента.</span><span class="sxs-lookup"><span data-stu-id="02013-139">The height of the bounding box for the element.</span></span>                                         | <span data-ttu-id="02013-140">Любое неотрицательное целое число.</span><span class="sxs-lookup"><span data-stu-id="02013-140">Any non-negative integer.</span></span> |



 

> [!WARNING]
> <span data-ttu-id="02013-141">Внутреннее координатное сопоставленное слово — это английские единицы метрики, а в приложении необходимо использовать множитель 2,54, чтобы преобразовать значения ширины и высоты в единицы HIMETRIC, используемые интерфейсами API платформы Tablet PC.</span><span class="sxs-lookup"><span data-stu-id="02013-141">The ink word's internal coordinate mapping is English Metric Units and a multiplier of 2.54 will need to be used by your application to convert the Width and Height values to the HIMETRIC units used by the Tablet PC platform APIs.</span></span>

 

## <a name="element-information"></a><span data-ttu-id="02013-142">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="02013-142">Element Information</span></span>



|              |                                                             |
|--------------|-------------------------------------------------------------|
| <span data-ttu-id="02013-143">Тип элемента</span><span class="sxs-lookup"><span data-stu-id="02013-143">Element type</span></span> | <span data-ttu-id="02013-144">[**Инквордтипе**](inkwordtype-complex-type.md) complexType</span><span class="sxs-lookup"><span data-stu-id="02013-144">[**InkWordType**](inkwordtype-complex-type.md) complexType</span></span> |
| <span data-ttu-id="02013-145">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="02013-145">Namespace</span></span>    | <span data-ttu-id="02013-146">urn: schemas-microsoft-com: TabletPC: ричинк</span><span class="sxs-lookup"><span data-stu-id="02013-146">urn:schemas-microsoft-com:tabletpc:richink</span></span>                  |
| <span data-ttu-id="02013-147">Имя схемы</span><span class="sxs-lookup"><span data-stu-id="02013-147">Schema name</span></span>  | <span data-ttu-id="02013-148">Средство чтения журнала</span><span class="sxs-lookup"><span data-stu-id="02013-148">Journal Reader</span></span>                                              |



 

 

 



