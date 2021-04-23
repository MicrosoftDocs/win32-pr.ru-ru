---
title: Шаблон элемента управления RangeValue
description: Описывает правила и соглашения для реализации IRangeValueProvider, включая сведения о свойствах и методах. Шаблон элемента управления RangeValue используется для поддержки элементов управления, для которых можно задать значение в диапазоне.
ms.assetid: e5c1104c-4b20-4fdd-bd12-dfc27cb73ac5
keywords:
- Модель автоматизации пользовательского интерфейса, реализация шаблона элемента управления RangeValue
- Модель автоматизации пользовательского интерфейса, шаблон элемента управления RangeValue
- Модель автоматизации пользовательского интерфейса, IRangeValueProvider
- IRangeValueProvider
- реализация шаблонов элементов управления RangeValue модели автоматизации пользовательского интерфейса
- Шаблоны элементов управления RangeValue
- шаблоны элементов управления, IRangeValueProvider
- шаблоны элементов управления, реализация модели автоматизации пользовательского интерфейса RangeValue
- шаблоны элементов управления, RangeValue
- интерфейсы, IRangeValueProvider
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bf426069ad88ad272fd78c521a220ba7ccf72275
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "105700605"
---
# <a name="rangevalue-control-pattern"></a><span data-ttu-id="6812b-114">Шаблон элемента управления RangeValue</span><span class="sxs-lookup"><span data-stu-id="6812b-114">RangeValue Control Pattern</span></span>

<span data-ttu-id="6812b-115">Описывает правила и соглашения для реализации [**IRangeValueProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irangevalueprovider), включая сведения о свойствах и методах.</span><span class="sxs-lookup"><span data-stu-id="6812b-115">Describes guidelines and conventions for implementing [**IRangeValueProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irangevalueprovider), including information about properties and methods.</span></span> <span data-ttu-id="6812b-116">Шаблон элемента управления **RangeValue** используется для поддержки элементов управления, для которых можно задать значение в диапазоне.</span><span class="sxs-lookup"><span data-stu-id="6812b-116">The **RangeValue** control pattern is used to support controls that can be set to a value within a range.</span></span>

<span data-ttu-id="6812b-117">Примеры элементов управления, реализующих этот шаблон элемента управления, см. в разделе [типы элементов управления и поддерживаемые шаблоны элементов управления](uiauto-controlpatternmapping.md).</span><span class="sxs-lookup"><span data-stu-id="6812b-117">For examples of controls that implement this control pattern, see [Control Types and Their Supported Control Patterns](uiauto-controlpatternmapping.md).</span></span>

<span data-ttu-id="6812b-118">В этом разделе содержатся следующие подразделы.</span><span class="sxs-lookup"><span data-stu-id="6812b-118">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="6812b-119">Правила и соглашения реализации</span><span class="sxs-lookup"><span data-stu-id="6812b-119">Implementation Guidelines and Conventions</span></span>](#implementation-guidelines-and-conventions)
-   [<span data-ttu-id="6812b-120">Обязательные члены для **IRangeValueProvider**</span><span class="sxs-lookup"><span data-stu-id="6812b-120">Required Members for **IRangeValueProvider**</span></span>](#required-members-for-irangevalueprovider)
-   [<span data-ttu-id="6812b-121">См. также</span><span class="sxs-lookup"><span data-stu-id="6812b-121">Related topics</span></span>](#related-topics)

## <a name="implementation-guidelines-and-conventions"></a><span data-ttu-id="6812b-122">Правила и соглашения реализации</span><span class="sxs-lookup"><span data-stu-id="6812b-122">Implementation Guidelines and Conventions</span></span>

<span data-ttu-id="6812b-123">При реализации шаблона элемента управления **RangeValue** Обратите внимание на следующие правила и соглашения.</span><span class="sxs-lookup"><span data-stu-id="6812b-123">When implementing the **RangeValue** control pattern, note the following guidelines and conventions:</span></span>

-   <span data-ttu-id="6812b-124">Элементы управления позволяют повторную калибровку своих поддерживаемых свойств на основе языкового стандарта или предпочтений пользователя.</span><span class="sxs-lookup"><span data-stu-id="6812b-124">Controls allow recalibration of their supported properties based upon locale or user preference.</span></span> <span data-ttu-id="6812b-125">Примером этого является элемент управления "Термометр", который можно задать для отображения температуры в шкале Цельсия или Фаренгейта.</span><span class="sxs-lookup"><span data-stu-id="6812b-125">An example of this is a thermometer control that can be set to display the temperature in Fahrenheit or Celsius.</span></span>
-   <span data-ttu-id="6812b-126">Элементы управления, имеющие неоднозначные значения диапазона, такие как индикаторы выполнения или ползунки, должны нормализовать эти значения.</span><span class="sxs-lookup"><span data-stu-id="6812b-126">Controls that have ambiguous range values, such as progress bars or sliders, should have those values normalized.</span></span>

## <a name="required-members-for-irangevalueprovider"></a><span data-ttu-id="6812b-127">Обязательные члены для **IRangeValueProvider**</span><span class="sxs-lookup"><span data-stu-id="6812b-127">Required Members for **IRangeValueProvider**</span></span>

<span data-ttu-id="6812b-128">Для реализации интерфейса [**IRangeValueProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irangevalueprovider) требуются следующие свойства и методы.</span><span class="sxs-lookup"><span data-stu-id="6812b-128">The following properties and methods are required for implementing the [**IRangeValueProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irangevalueprovider) interface.</span></span>



| <span data-ttu-id="6812b-129">Обязательные члены</span><span class="sxs-lookup"><span data-stu-id="6812b-129">Required members</span></span>                                              | <span data-ttu-id="6812b-130">Тип члена</span><span class="sxs-lookup"><span data-stu-id="6812b-130">Member type</span></span> | <span data-ttu-id="6812b-131">Примечания</span><span class="sxs-lookup"><span data-stu-id="6812b-131">Notes</span></span> |
|---------------------------------------------------------------|-------------|-------|
| [<span data-ttu-id="6812b-132">**IsReadOnly**</span><span class="sxs-lookup"><span data-stu-id="6812b-132">**IsReadOnly**</span></span>](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irangevalueprovider-get_isreadonly)   | <span data-ttu-id="6812b-133">Свойство</span><span class="sxs-lookup"><span data-stu-id="6812b-133">Property</span></span>    | <span data-ttu-id="6812b-134">Нет</span><span class="sxs-lookup"><span data-stu-id="6812b-134">None</span></span>  |
| [<span data-ttu-id="6812b-135">**Значение**</span><span class="sxs-lookup"><span data-stu-id="6812b-135">**Value**</span></span>](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irangevalueprovider-get_value)             | <span data-ttu-id="6812b-136">Свойство</span><span class="sxs-lookup"><span data-stu-id="6812b-136">Property</span></span>    | <span data-ttu-id="6812b-137">Нет</span><span class="sxs-lookup"><span data-stu-id="6812b-137">None</span></span>  |
| [<span data-ttu-id="6812b-138">**LargeChange**</span><span class="sxs-lookup"><span data-stu-id="6812b-138">**LargeChange**</span></span>](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irangevalueprovider-get_largechange) | <span data-ttu-id="6812b-139">Свойство</span><span class="sxs-lookup"><span data-stu-id="6812b-139">Property</span></span>    | <span data-ttu-id="6812b-140">Нет</span><span class="sxs-lookup"><span data-stu-id="6812b-140">None</span></span>  |
| [<span data-ttu-id="6812b-141">**SmallChange**</span><span class="sxs-lookup"><span data-stu-id="6812b-141">**SmallChange**</span></span>](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irangevalueprovider-get_smallchange) | <span data-ttu-id="6812b-142">Свойство</span><span class="sxs-lookup"><span data-stu-id="6812b-142">Property</span></span>    | <span data-ttu-id="6812b-143">Нет</span><span class="sxs-lookup"><span data-stu-id="6812b-143">None</span></span>  |
| [<span data-ttu-id="6812b-144">**Максимум**</span><span class="sxs-lookup"><span data-stu-id="6812b-144">**Maximum**</span></span>](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irangevalueprovider-get_maximum)         | <span data-ttu-id="6812b-145">Свойство</span><span class="sxs-lookup"><span data-stu-id="6812b-145">Property</span></span>    | <span data-ttu-id="6812b-146">Нет</span><span class="sxs-lookup"><span data-stu-id="6812b-146">None</span></span>  |
| [<span data-ttu-id="6812b-147">**Минимальные**</span><span class="sxs-lookup"><span data-stu-id="6812b-147">**Minimum**</span></span>](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irangevalueprovider-get_minimum)         | <span data-ttu-id="6812b-148">Свойство</span><span class="sxs-lookup"><span data-stu-id="6812b-148">Property</span></span>    | <span data-ttu-id="6812b-149">Нет</span><span class="sxs-lookup"><span data-stu-id="6812b-149">None</span></span>  |
| [<span data-ttu-id="6812b-150">**SetValue**</span><span class="sxs-lookup"><span data-stu-id="6812b-150">**SetValue**</span></span>](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irangevalueprovider-setvalue)       | <span data-ttu-id="6812b-151">Метод</span><span class="sxs-lookup"><span data-stu-id="6812b-151">Method</span></span>      | <span data-ttu-id="6812b-152">Нет</span><span class="sxs-lookup"><span data-stu-id="6812b-152">None</span></span>  |



 

<span data-ttu-id="6812b-153">Этот шаблон элемента управления не имеет связанных событий.</span><span class="sxs-lookup"><span data-stu-id="6812b-153">This control pattern has no associated events.</span></span>

## <a name="related-topics"></a><span data-ttu-id="6812b-154">См. также</span><span class="sxs-lookup"><span data-stu-id="6812b-154">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6812b-155">Типы элементов управления и поддерживаемые ими шаблоны элементов управления</span><span class="sxs-lookup"><span data-stu-id="6812b-155">Control Types and Their Supported Control Patterns</span></span>](uiauto-controlpatternmapping.md)
</dt> <dt>

[<span data-ttu-id="6812b-156">Общие сведения о шаблонах элементов управления модели автоматизации пользовательского интерфейса</span><span class="sxs-lookup"><span data-stu-id="6812b-156">UI Automation Control Patterns Overview</span></span>](uiauto-controlpatternsoverview.md)
</dt> <dt>

[<span data-ttu-id="6812b-157">Общие сведения о дереве модели автоматизации пользовательского интерфейса</span><span class="sxs-lookup"><span data-stu-id="6812b-157">UI Automation Tree Overview</span></span>](uiauto-treeoverview.md)
</dt> </dl>

 

 




