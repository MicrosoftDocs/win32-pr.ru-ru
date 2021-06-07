---
description: Скалярное преобразование, используемое Drawing или Инкворд.
ms.assetid: 88fc3b90-9ec6-41c0-9267-ed5b585ea07b
title: Скалартрансформ, элемент
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 91ed5f7d3b44456522b45c7243b15390b7c52433
ms.sourcegitcommit: c3f669dc1d52278432bf75ad9fddba3257d26aa2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/04/2021
ms.locfileid: "111432436"
---
# <a name="scalartransform-element"></a><span data-ttu-id="d6b40-103">Скалартрансформ, элемент</span><span class="sxs-lookup"><span data-stu-id="d6b40-103">ScalarTransform Element</span></span>

<span data-ttu-id="d6b40-104">Скалярное преобразование, используемое [**Drawing**](drawing-element.md) или [**инкворд**](inkword-element.md).</span><span class="sxs-lookup"><span data-stu-id="d6b40-104">Scalar transform used by the [**Drawing**](drawing-element.md) or [**InkWord**](inkword-element.md).</span></span>

## <a name="definition"></a><span data-ttu-id="d6b40-105">Определение</span><span class="sxs-lookup"><span data-stu-id="d6b40-105">Definition</span></span>

``` syntax
<xs:element name="ScalarTransform" minOccurs="0" type="ScalarTransformType" />
```

## <a name="parent-elements"></a><span data-ttu-id="d6b40-106">Родительские элементы</span><span class="sxs-lookup"><span data-stu-id="d6b40-106">Parent Elements</span></span>

[<span data-ttu-id="d6b40-107">**Рисование**</span><span class="sxs-lookup"><span data-stu-id="d6b40-107">**Drawing**</span></span>](drawing-element.md)

[<span data-ttu-id="d6b40-108">**инкворд**</span><span class="sxs-lookup"><span data-stu-id="d6b40-108">**InkWord**</span></span>](inkword-element.md)

## <a name="child-elements"></a><span data-ttu-id="d6b40-109">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="d6b40-109">Child Elements</span></span>

<span data-ttu-id="d6b40-110">Отсутствует.</span><span class="sxs-lookup"><span data-stu-id="d6b40-110">None.</span></span>

## <a name="attributes"></a><span data-ttu-id="d6b40-111">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="d6b40-111">Attributes</span></span>



| <span data-ttu-id="d6b40-112">attribute</span><span class="sxs-lookup"><span data-stu-id="d6b40-112">Attribute</span></span> | <span data-ttu-id="d6b40-113">Тип</span><span class="sxs-lookup"><span data-stu-id="d6b40-113">Type</span></span>           | <span data-ttu-id="d6b40-114">Обязательно</span><span class="sxs-lookup"><span data-stu-id="d6b40-114">Required</span></span> | <span data-ttu-id="d6b40-115">Описание</span><span class="sxs-lookup"><span data-stu-id="d6b40-115">Description</span></span> | <span data-ttu-id="d6b40-116">Возможные значения</span><span class="sxs-lookup"><span data-stu-id="d6b40-116">Possible Values</span></span>     |
|-----------|----------------|----------|-------------|---------------------|
| <span data-ttu-id="d6b40-117">**Mat1**</span><span class="sxs-lookup"><span data-stu-id="d6b40-117">**Mat1**</span></span>  | <span data-ttu-id="d6b40-118">**xs:decimal**</span><span class="sxs-lookup"><span data-stu-id="d6b40-118">**xs:decimal**</span></span> | <span data-ttu-id="d6b40-119">Обязательно</span><span class="sxs-lookup"><span data-stu-id="d6b40-119">Required</span></span> |             | <span data-ttu-id="d6b40-120">Любое десятичное число.</span><span class="sxs-lookup"><span data-stu-id="d6b40-120">Any decimal number.</span></span> |
| <span data-ttu-id="d6b40-121">**Mat2**</span><span class="sxs-lookup"><span data-stu-id="d6b40-121">**Mat2**</span></span>  | <span data-ttu-id="d6b40-122">**xs:decimal**</span><span class="sxs-lookup"><span data-stu-id="d6b40-122">**xs:decimal**</span></span> | <span data-ttu-id="d6b40-123">Обязательно</span><span class="sxs-lookup"><span data-stu-id="d6b40-123">Required</span></span> |             | <span data-ttu-id="d6b40-124">Любое десятичное число.</span><span class="sxs-lookup"><span data-stu-id="d6b40-124">Any decimal number.</span></span> |
| <span data-ttu-id="d6b40-125">**Mat3**</span><span class="sxs-lookup"><span data-stu-id="d6b40-125">**Mat3**</span></span>  | <span data-ttu-id="d6b40-126">**xs:decimal**</span><span class="sxs-lookup"><span data-stu-id="d6b40-126">**xs:decimal**</span></span> | <span data-ttu-id="d6b40-127">Обязательно</span><span class="sxs-lookup"><span data-stu-id="d6b40-127">Required</span></span> |             | <span data-ttu-id="d6b40-128">Любое десятичное число.</span><span class="sxs-lookup"><span data-stu-id="d6b40-128">Any decimal number.</span></span> |
| <span data-ttu-id="d6b40-129">**Mat4**</span><span class="sxs-lookup"><span data-stu-id="d6b40-129">**Mat4**</span></span>  | <span data-ttu-id="d6b40-130">**xs:decimal**</span><span class="sxs-lookup"><span data-stu-id="d6b40-130">**xs:decimal**</span></span> | <span data-ttu-id="d6b40-131">Обязательно</span><span class="sxs-lookup"><span data-stu-id="d6b40-131">Required</span></span> |             | <span data-ttu-id="d6b40-132">Любое десятичное число.</span><span class="sxs-lookup"><span data-stu-id="d6b40-132">Any decimal number.</span></span> |
| <span data-ttu-id="d6b40-133">**Mat5**</span><span class="sxs-lookup"><span data-stu-id="d6b40-133">**Mat5**</span></span>  | <span data-ttu-id="d6b40-134">**xs:decimal**</span><span class="sxs-lookup"><span data-stu-id="d6b40-134">**xs:decimal**</span></span> | <span data-ttu-id="d6b40-135">Обязательно</span><span class="sxs-lookup"><span data-stu-id="d6b40-135">Required</span></span> |             | <span data-ttu-id="d6b40-136">Любое десятичное число.</span><span class="sxs-lookup"><span data-stu-id="d6b40-136">Any decimal number.</span></span> |
| <span data-ttu-id="d6b40-137">**Mat6**</span><span class="sxs-lookup"><span data-stu-id="d6b40-137">**Mat6**</span></span>  | <span data-ttu-id="d6b40-138">**xs:decimal**</span><span class="sxs-lookup"><span data-stu-id="d6b40-138">**xs:decimal**</span></span> | <span data-ttu-id="d6b40-139">Обязательно</span><span class="sxs-lookup"><span data-stu-id="d6b40-139">Required</span></span> |             | <span data-ttu-id="d6b40-140">Любое десятичное число.</span><span class="sxs-lookup"><span data-stu-id="d6b40-140">Any decimal number.</span></span> |
| <span data-ttu-id="d6b40-141">**Mat7**</span><span class="sxs-lookup"><span data-stu-id="d6b40-141">**Mat7**</span></span>  | <span data-ttu-id="d6b40-142">**xs:decimal**</span><span class="sxs-lookup"><span data-stu-id="d6b40-142">**xs:decimal**</span></span> | <span data-ttu-id="d6b40-143">Обязательно</span><span class="sxs-lookup"><span data-stu-id="d6b40-143">Required</span></span> |             | <span data-ttu-id="d6b40-144">Любое десятичное число.</span><span class="sxs-lookup"><span data-stu-id="d6b40-144">Any decimal number.</span></span> |
| <span data-ttu-id="d6b40-145">**Mat8**</span><span class="sxs-lookup"><span data-stu-id="d6b40-145">**Mat8**</span></span>  | <span data-ttu-id="d6b40-146">**xs:decimal**</span><span class="sxs-lookup"><span data-stu-id="d6b40-146">**xs:decimal**</span></span> | <span data-ttu-id="d6b40-147">Обязательно</span><span class="sxs-lookup"><span data-stu-id="d6b40-147">Required</span></span> |             | <span data-ttu-id="d6b40-148">Любое десятичное число.</span><span class="sxs-lookup"><span data-stu-id="d6b40-148">Any decimal number.</span></span> |
| <span data-ttu-id="d6b40-149">**Mat9**</span><span class="sxs-lookup"><span data-stu-id="d6b40-149">**Mat9**</span></span>  | <span data-ttu-id="d6b40-150">**xs:decimal**</span><span class="sxs-lookup"><span data-stu-id="d6b40-150">**xs:decimal**</span></span> | <span data-ttu-id="d6b40-151">Обязательно</span><span class="sxs-lookup"><span data-stu-id="d6b40-151">Required</span></span> |             | <span data-ttu-id="d6b40-152">Любое десятичное число.</span><span class="sxs-lookup"><span data-stu-id="d6b40-152">Any decimal number.</span></span> |



 

## <a name="element-information"></a><span data-ttu-id="d6b40-153">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="d6b40-153">Element Information</span></span>



| <span data-ttu-id="d6b40-154">Элемент</span><span class="sxs-lookup"><span data-stu-id="d6b40-154">Element</span></span>      | <span data-ttu-id="d6b40-155">Значение</span><span class="sxs-lookup"><span data-stu-id="d6b40-155">Value</span></span>                                                                       |
|--------------|-----------------------------------------------------------------------------|
| <span data-ttu-id="d6b40-156">Тип элемента</span><span class="sxs-lookup"><span data-stu-id="d6b40-156">Element type</span></span> | <span data-ttu-id="d6b40-157">[**Скалартрансформтипе**](scalartransformtype-complex-type.md) complexType</span><span class="sxs-lookup"><span data-stu-id="d6b40-157">[**ScalarTransformType**](scalartransformtype-complex-type.md) complexType</span></span> |
| <span data-ttu-id="d6b40-158">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="d6b40-158">Namespace</span></span>    | <span data-ttu-id="d6b40-159">urn: schemas-microsoft-com: TabletPC: ричинк</span><span class="sxs-lookup"><span data-stu-id="d6b40-159">urn:schemas-microsoft-com:tabletpc:richink</span></span>                                  |
| <span data-ttu-id="d6b40-160">Имя схемы</span><span class="sxs-lookup"><span data-stu-id="d6b40-160">Schema name</span></span>  | <span data-ttu-id="d6b40-161">Средство чтения журнала</span><span class="sxs-lookup"><span data-stu-id="d6b40-161">Journal Reader</span></span>                                                              |



 

 

 



