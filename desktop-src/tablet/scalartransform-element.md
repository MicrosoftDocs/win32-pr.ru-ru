---
description: Скалярное преобразование, используемое Drawing или Инкворд.
ms.assetid: 88fc3b90-9ec6-41c0-9267-ed5b585ea07b
title: Скалартрансформ, элемент
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2f5853c0fab76cd5a4857ae0235127a2fe103872
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105712621"
---
# <a name="scalartransform-element"></a><span data-ttu-id="568b8-103">Скалартрансформ, элемент</span><span class="sxs-lookup"><span data-stu-id="568b8-103">ScalarTransform Element</span></span>

<span data-ttu-id="568b8-104">Скалярное преобразование, используемое [**Drawing**](drawing-element.md) или [**инкворд**](inkword-element.md).</span><span class="sxs-lookup"><span data-stu-id="568b8-104">Scalar transform used by the [**Drawing**](drawing-element.md) or [**InkWord**](inkword-element.md).</span></span>

## <a name="definition"></a><span data-ttu-id="568b8-105">Определение</span><span class="sxs-lookup"><span data-stu-id="568b8-105">Definition</span></span>

``` syntax
<xs:element name="ScalarTransform" minOccurs="0" type="ScalarTransformType" />
```

## <a name="parent-elements"></a><span data-ttu-id="568b8-106">Родительские элементы</span><span class="sxs-lookup"><span data-stu-id="568b8-106">Parent Elements</span></span>

[<span data-ttu-id="568b8-107">**Рисование**</span><span class="sxs-lookup"><span data-stu-id="568b8-107">**Drawing**</span></span>](drawing-element.md)

[<span data-ttu-id="568b8-108">**инкворд**</span><span class="sxs-lookup"><span data-stu-id="568b8-108">**InkWord**</span></span>](inkword-element.md)

## <a name="child-elements"></a><span data-ttu-id="568b8-109">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="568b8-109">Child Elements</span></span>

<span data-ttu-id="568b8-110">Отсутствует.</span><span class="sxs-lookup"><span data-stu-id="568b8-110">None.</span></span>

## <a name="attributes"></a><span data-ttu-id="568b8-111">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="568b8-111">Attributes</span></span>



| <span data-ttu-id="568b8-112">attribute</span><span class="sxs-lookup"><span data-stu-id="568b8-112">Attribute</span></span> | <span data-ttu-id="568b8-113">Тип</span><span class="sxs-lookup"><span data-stu-id="568b8-113">Type</span></span>           | <span data-ttu-id="568b8-114">Обязательно</span><span class="sxs-lookup"><span data-stu-id="568b8-114">Required</span></span> | <span data-ttu-id="568b8-115">Описание</span><span class="sxs-lookup"><span data-stu-id="568b8-115">Description</span></span> | <span data-ttu-id="568b8-116">Возможные значения</span><span class="sxs-lookup"><span data-stu-id="568b8-116">Possible Values</span></span>     |
|-----------|----------------|----------|-------------|---------------------|
| <span data-ttu-id="568b8-117">**Mat1**</span><span class="sxs-lookup"><span data-stu-id="568b8-117">**Mat1**</span></span>  | <span data-ttu-id="568b8-118">**xs:decimal**</span><span class="sxs-lookup"><span data-stu-id="568b8-118">**xs:decimal**</span></span> | <span data-ttu-id="568b8-119">Обязательно</span><span class="sxs-lookup"><span data-stu-id="568b8-119">Required</span></span> |             | <span data-ttu-id="568b8-120">Любое десятичное число.</span><span class="sxs-lookup"><span data-stu-id="568b8-120">Any decimal number.</span></span> |
| <span data-ttu-id="568b8-121">**Mat2**</span><span class="sxs-lookup"><span data-stu-id="568b8-121">**Mat2**</span></span>  | <span data-ttu-id="568b8-122">**xs:decimal**</span><span class="sxs-lookup"><span data-stu-id="568b8-122">**xs:decimal**</span></span> | <span data-ttu-id="568b8-123">Обязательно</span><span class="sxs-lookup"><span data-stu-id="568b8-123">Required</span></span> |             | <span data-ttu-id="568b8-124">Любое десятичное число.</span><span class="sxs-lookup"><span data-stu-id="568b8-124">Any decimal number.</span></span> |
| <span data-ttu-id="568b8-125">**Mat3**</span><span class="sxs-lookup"><span data-stu-id="568b8-125">**Mat3**</span></span>  | <span data-ttu-id="568b8-126">**xs:decimal**</span><span class="sxs-lookup"><span data-stu-id="568b8-126">**xs:decimal**</span></span> | <span data-ttu-id="568b8-127">Обязательно</span><span class="sxs-lookup"><span data-stu-id="568b8-127">Required</span></span> |             | <span data-ttu-id="568b8-128">Любое десятичное число.</span><span class="sxs-lookup"><span data-stu-id="568b8-128">Any decimal number.</span></span> |
| <span data-ttu-id="568b8-129">**Mat4**</span><span class="sxs-lookup"><span data-stu-id="568b8-129">**Mat4**</span></span>  | <span data-ttu-id="568b8-130">**xs:decimal**</span><span class="sxs-lookup"><span data-stu-id="568b8-130">**xs:decimal**</span></span> | <span data-ttu-id="568b8-131">Обязательно</span><span class="sxs-lookup"><span data-stu-id="568b8-131">Required</span></span> |             | <span data-ttu-id="568b8-132">Любое десятичное число.</span><span class="sxs-lookup"><span data-stu-id="568b8-132">Any decimal number.</span></span> |
| <span data-ttu-id="568b8-133">**Mat5**</span><span class="sxs-lookup"><span data-stu-id="568b8-133">**Mat5**</span></span>  | <span data-ttu-id="568b8-134">**xs:decimal**</span><span class="sxs-lookup"><span data-stu-id="568b8-134">**xs:decimal**</span></span> | <span data-ttu-id="568b8-135">Обязательно</span><span class="sxs-lookup"><span data-stu-id="568b8-135">Required</span></span> |             | <span data-ttu-id="568b8-136">Любое десятичное число.</span><span class="sxs-lookup"><span data-stu-id="568b8-136">Any decimal number.</span></span> |
| <span data-ttu-id="568b8-137">**Mat6**</span><span class="sxs-lookup"><span data-stu-id="568b8-137">**Mat6**</span></span>  | <span data-ttu-id="568b8-138">**xs:decimal**</span><span class="sxs-lookup"><span data-stu-id="568b8-138">**xs:decimal**</span></span> | <span data-ttu-id="568b8-139">Обязательно</span><span class="sxs-lookup"><span data-stu-id="568b8-139">Required</span></span> |             | <span data-ttu-id="568b8-140">Любое десятичное число.</span><span class="sxs-lookup"><span data-stu-id="568b8-140">Any decimal number.</span></span> |
| <span data-ttu-id="568b8-141">**Mat7**</span><span class="sxs-lookup"><span data-stu-id="568b8-141">**Mat7**</span></span>  | <span data-ttu-id="568b8-142">**xs:decimal**</span><span class="sxs-lookup"><span data-stu-id="568b8-142">**xs:decimal**</span></span> | <span data-ttu-id="568b8-143">Обязательно</span><span class="sxs-lookup"><span data-stu-id="568b8-143">Required</span></span> |             | <span data-ttu-id="568b8-144">Любое десятичное число.</span><span class="sxs-lookup"><span data-stu-id="568b8-144">Any decimal number.</span></span> |
| <span data-ttu-id="568b8-145">**Mat8**</span><span class="sxs-lookup"><span data-stu-id="568b8-145">**Mat8**</span></span>  | <span data-ttu-id="568b8-146">**xs:decimal**</span><span class="sxs-lookup"><span data-stu-id="568b8-146">**xs:decimal**</span></span> | <span data-ttu-id="568b8-147">Обязательно</span><span class="sxs-lookup"><span data-stu-id="568b8-147">Required</span></span> |             | <span data-ttu-id="568b8-148">Любое десятичное число.</span><span class="sxs-lookup"><span data-stu-id="568b8-148">Any decimal number.</span></span> |
| <span data-ttu-id="568b8-149">**Mat9**</span><span class="sxs-lookup"><span data-stu-id="568b8-149">**Mat9**</span></span>  | <span data-ttu-id="568b8-150">**xs:decimal**</span><span class="sxs-lookup"><span data-stu-id="568b8-150">**xs:decimal**</span></span> | <span data-ttu-id="568b8-151">Обязательно</span><span class="sxs-lookup"><span data-stu-id="568b8-151">Required</span></span> |             | <span data-ttu-id="568b8-152">Любое десятичное число.</span><span class="sxs-lookup"><span data-stu-id="568b8-152">Any decimal number.</span></span> |



 

## <a name="element-information"></a><span data-ttu-id="568b8-153">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="568b8-153">Element Information</span></span>



|              |                                                                             |
|--------------|-----------------------------------------------------------------------------|
| <span data-ttu-id="568b8-154">Тип элемента</span><span class="sxs-lookup"><span data-stu-id="568b8-154">Element type</span></span> | <span data-ttu-id="568b8-155">[**Скалартрансформтипе**](scalartransformtype-complex-type.md) complexType</span><span class="sxs-lookup"><span data-stu-id="568b8-155">[**ScalarTransformType**](scalartransformtype-complex-type.md) complexType</span></span> |
| <span data-ttu-id="568b8-156">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="568b8-156">Namespace</span></span>    | <span data-ttu-id="568b8-157">urn: schemas-microsoft-com: TabletPC: ричинк</span><span class="sxs-lookup"><span data-stu-id="568b8-157">urn:schemas-microsoft-com:tabletpc:richink</span></span>                                  |
| <span data-ttu-id="568b8-158">Имя схемы</span><span class="sxs-lookup"><span data-stu-id="568b8-158">Schema name</span></span>  | <span data-ttu-id="568b8-159">Средство чтения журнала</span><span class="sxs-lookup"><span data-stu-id="568b8-159">Journal Reader</span></span>                                                              |



 

 

 



