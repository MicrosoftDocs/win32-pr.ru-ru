---
title: Тип элемента управления Slider
description: В этом разделе содержатся сведения о поддержке автоматизации пользовательского интерфейса Майкрософт для типа элемента управления Slider.
ms.assetid: dc7bef7a-b68c-4184-a9e7-745bb41b592e
keywords:
- Модель автоматизации пользовательского интерфейса, поддержка типа элемента управления Slider
- Модель автоматизации пользовательского интерфейса, тип элемента управления Slider
- Модель автоматизации пользовательского интерфейса, древовидная структура для типа элемента управления Slider
- Модель автоматизации пользовательского интерфейса, свойства для типа элемента управления Slider
- Модель автоматизации пользовательского интерфейса, шаблоны элементов управления для типа элемента управления Slider
- Модель автоматизации пользовательского интерфейса, события для типа элемента управления Slider
- Древовидные структуры, тип элемента управления Slider
- свойства, тип элемента управления Slider
- шаблоны элементов управления, тип элемента управления Slider
- события, тип элемента управления Slider
- Поддержка типа элемента управления Slider
- Тип элемента управления "Ползунок"
- типы элементов управления, древовидная структура для типа элемента управления Slider
- типы элементов управления, шаблоны элементов управления для типа элемента управления Slider
- типы элементов управления, поддержка Slider
- типы элементов управления, ползунок
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5be8e82dfc8f011363086745368ed1693c45a6aa
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103986605"
---
# <a name="slider-control-type"></a><span data-ttu-id="a1405-119">Тип элемента управления Slider</span><span class="sxs-lookup"><span data-stu-id="a1405-119">Slider Control Type</span></span>

<span data-ttu-id="a1405-120">В этом разделе содержатся сведения о поддержке автоматизации пользовательского интерфейса Майкрософт для типа элемента управления **Slider** .</span><span class="sxs-lookup"><span data-stu-id="a1405-120">This topic provides information about Microsoft UI Automation support for the **Slider** control type.</span></span>

<span data-ttu-id="a1405-121">Элемент управления "ползунок" — это составной элемент управления с кнопками, которые позволяют пользователю задать числовой диапазон или выбрать из набора элементов.</span><span class="sxs-lookup"><span data-stu-id="a1405-121">A slider control is a composite control with buttons that enable a user to set a numerical range or select from a set of items.</span></span>

<span data-ttu-id="a1405-122">В следующих разделах определяется необходимая древовидная структура модели автоматизации пользовательского интерфейса, свойства, шаблоны элементов управления и события для типа элемента управления **Slider** .</span><span class="sxs-lookup"><span data-stu-id="a1405-122">The following sections define the required UI Automation tree structure, properties, control patterns, and events for the **Slider** control type.</span></span> <span data-ttu-id="a1405-123">Требования к автоматизации пользовательского интерфейса применяются ко всем элементам управления "ползунок", в которых платформа или платформа пользовательского интерфейса интегрирует поддержку автоматизации пользовательского интерфейса для типов элементов управления и шаблонов элементов управления.</span><span class="sxs-lookup"><span data-stu-id="a1405-123">The UI Automation requirements apply to all slider controls where the UI framework/platform integrates UI Automation support for control types and control patterns.</span></span>

<span data-ttu-id="a1405-124">В этом разделе содержатся следующие подразделы.</span><span class="sxs-lookup"><span data-stu-id="a1405-124">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="a1405-125">Типичная древовидная структура</span><span class="sxs-lookup"><span data-stu-id="a1405-125">Typical Tree Structure</span></span>](#typical-tree-structure)
-   [<span data-ttu-id="a1405-126">Соответствующие свойства</span><span class="sxs-lookup"><span data-stu-id="a1405-126">Relevant Properties</span></span>](#relevant-properties)
-   [<span data-ttu-id="a1405-127">Обязательные шаблоны элементов управления</span><span class="sxs-lookup"><span data-stu-id="a1405-127">Required Control Patterns</span></span>](#required-control-patterns)
-   [<span data-ttu-id="a1405-128">Обязательные события</span><span class="sxs-lookup"><span data-stu-id="a1405-128">Required Events</span></span>](#required-events)
-   [<span data-ttu-id="a1405-129">См. также</span><span class="sxs-lookup"><span data-stu-id="a1405-129">Related topics</span></span>](#related-topics)

## <a name="typical-tree-structure"></a><span data-ttu-id="a1405-130">Типичная древовидная структура</span><span class="sxs-lookup"><span data-stu-id="a1405-130">Typical Tree Structure</span></span>

<span data-ttu-id="a1405-131">В следующей таблице описывается типичный элемент управления и представление содержимого дерева модели автоматизации пользовательского интерфейса, относящиеся к элементам управления "ползунок", и показывается, что может содержаться в каждом представлении.</span><span class="sxs-lookup"><span data-stu-id="a1405-131">The following table depicts a typical control and content view of the UI Automation tree that pertains to slider controls and describes what can be contained in each view.</span></span> <span data-ttu-id="a1405-132">Дополнительные сведения о дереве автоматизации пользовательского интерфейса см. в разделе [Общие сведения о дереве модели автоматизации пользовательского интерфейса](uiauto-treeoverview.md).</span><span class="sxs-lookup"><span data-stu-id="a1405-132">For more information about the UI Automation tree, see [UI Automation Tree Overview](uiauto-treeoverview.md).</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="a1405-133">Представление элемента управления</span><span class="sxs-lookup"><span data-stu-id="a1405-133">Control View</span></span></th>
<th><span data-ttu-id="a1405-134">Представление содержимого</span><span class="sxs-lookup"><span data-stu-id="a1405-134">Content View</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><ul>
<li><span data-ttu-id="a1405-135">Ползунок</span><span class="sxs-lookup"><span data-stu-id="a1405-135">Slider</span></span>
<ul>
<li><span data-ttu-id="a1405-136">Button (2 или 4)</span><span class="sxs-lookup"><span data-stu-id="a1405-136">Button (2 or 4)</span></span></li>
<li><span data-ttu-id="a1405-137">Бегунок (1)</span><span class="sxs-lookup"><span data-stu-id="a1405-137">Thumb (1)</span></span></li>
<li><span data-ttu-id="a1405-138">ListItem (0 или более)</span><span class="sxs-lookup"><span data-stu-id="a1405-138">List Item (0 or more)</span></span></li>
</ul></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="a1405-139">Ползунок</span><span class="sxs-lookup"><span data-stu-id="a1405-139">Slider</span></span>
<ul>
<li><span data-ttu-id="a1405-140">ListItem (0 или более)</span><span class="sxs-lookup"><span data-stu-id="a1405-140">List Item (0 or more)</span></span></li>
</ul></li>
</ul></td>
</tr>
</tbody>
</table>



 

## <a name="relevant-properties"></a><span data-ttu-id="a1405-141">Соответствующие свойства</span><span class="sxs-lookup"><span data-stu-id="a1405-141">Relevant Properties</span></span>

<span data-ttu-id="a1405-142">В следующей таблице перечислены свойства модели автоматизации пользовательского интерфейса, значения или определения которых особенно важны для элементов управления "ползунок".</span><span class="sxs-lookup"><span data-stu-id="a1405-142">The following table lists the UI Automation properties whose value or definition is especially relevant to slider controls.</span></span> <span data-ttu-id="a1405-143">Дополнительные сведения о свойствах модели автоматизации пользовательского интерфейса см. в разделе [Получение свойств элементов модели автоматизации пользовательского интерфейса](uiauto-propertiesforclients.md).</span><span class="sxs-lookup"><span data-stu-id="a1405-143">For more information about UI Automation properties, see [Retrieving Properties from UI Automation Elements](uiauto-propertiesforclients.md).</span></span>



| <span data-ttu-id="a1405-144">Свойство модели автоматизации пользовательского интерфейса</span><span class="sxs-lookup"><span data-stu-id="a1405-144">UI Automation Property</span></span>                                                                                              | <span data-ttu-id="a1405-145">Значение</span><span class="sxs-lookup"><span data-stu-id="a1405-145">Value</span></span>      | <span data-ttu-id="a1405-146">Примечания</span><span class="sxs-lookup"><span data-stu-id="a1405-146">Notes</span></span>                                                                                                                                                                                                                          |
|---------------------------------------------------------------------------------------------------------------------|------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="a1405-147">**UIA \_ аутоматионидпропертид**</span><span class="sxs-lookup"><span data-stu-id="a1405-147">**UIA\_AutomationIdPropertyId**</span></span>](uiauto-automation-element-propids.md)                 | <span data-ttu-id="a1405-148">См. примечания.</span><span class="sxs-lookup"><span data-stu-id="a1405-148">See notes.</span></span> | <span data-ttu-id="a1405-149">Значение этого свойства должно быть уникальным среди всех одноранговых элементов в необработанном представлении дерева модели автоматизации пользовательского интерфейса.</span><span class="sxs-lookup"><span data-stu-id="a1405-149">The value of this property must be unique among all peer elements in the raw view of the UI Automation tree.</span></span>                                                                                                                   |
| [<span data-ttu-id="a1405-150">**UIA \_ баундингректанглепропертид**</span><span class="sxs-lookup"><span data-stu-id="a1405-150">**UIA\_BoundingRectanglePropertyId**</span></span>](uiauto-automation-element-propids.md)       | <span data-ttu-id="a1405-151">См. примечания.</span><span class="sxs-lookup"><span data-stu-id="a1405-151">See notes.</span></span> | <span data-ttu-id="a1405-152">Внешний прямоугольник, содержащий весь элемент управления.</span><span class="sxs-lookup"><span data-stu-id="a1405-152">The outermost rectangle that contains the whole control.</span></span>                                                                                                                                                                       |
| [<span data-ttu-id="a1405-153">**UIA \_ кликкаблепоинтпропертид**</span><span class="sxs-lookup"><span data-stu-id="a1405-153">**UIA\_ClickablePointPropertyId**</span></span>](uiauto-automation-element-propids.md)             | <span data-ttu-id="a1405-154">См. примечания.</span><span class="sxs-lookup"><span data-stu-id="a1405-154">See notes.</span></span> | <span data-ttu-id="a1405-155">Большинство элементов управления "ползунок" должны возвращать ошибку [**UIA \_ E \_ нокликкаблепоинт**](uiauto-error-codes.md) , поскольку весь ограничивающий прямоугольник элемента управления "ползунок" занят дочерними элементами управления.</span><span class="sxs-lookup"><span data-stu-id="a1405-155">The majority of slider controls must return the [**UIA\_E\_NOCLICKABLEPOINT**](uiauto-error-codes.md) error because the entire bounding rectangle of the slider control is occupied by child controls.</span></span> |
| [<span data-ttu-id="a1405-156">**UIA \_ контролтипепропертид**</span><span class="sxs-lookup"><span data-stu-id="a1405-156">**UIA\_ControlTypePropertyId**</span></span>](uiauto-automation-element-propids.md)                   | <span data-ttu-id="a1405-157">**Ползунок**</span><span class="sxs-lookup"><span data-stu-id="a1405-157">**Slider**</span></span> | <span data-ttu-id="a1405-158">Это значение одинаково для всех инфраструктур.</span><span class="sxs-lookup"><span data-stu-id="a1405-158">This value is the same for all frameworks.</span></span>                                                                                                                                                                                     |
| [<span data-ttu-id="a1405-159">**UIA \_ исконтентелементпропертид**</span><span class="sxs-lookup"><span data-stu-id="a1405-159">**UIA\_IsContentElementPropertyId**</span></span>](uiauto-automation-element-propids.md)         | <span data-ttu-id="a1405-160">true</span><span class="sxs-lookup"><span data-stu-id="a1405-160">TRUE</span></span>       | <span data-ttu-id="a1405-161">Элемент управления "ползунок" всегда включается в представление содержимого дерева модели автоматизации пользовательского интерфейса.</span><span class="sxs-lookup"><span data-stu-id="a1405-161">The slider control is always included in the content view of the UI Automation tree.</span></span>                                                                                                                                           |
| [<span data-ttu-id="a1405-162">**UIA \_ исконтролелементпропертид**</span><span class="sxs-lookup"><span data-stu-id="a1405-162">**UIA\_IsControlElementPropertyId**</span></span>](uiauto-automation-element-propids.md)         | <span data-ttu-id="a1405-163">true</span><span class="sxs-lookup"><span data-stu-id="a1405-163">TRUE</span></span>       | <span data-ttu-id="a1405-164">Элемент управления "ползунок" всегда включается в представление элемента управления дерева модели автоматизации пользовательского интерфейса.</span><span class="sxs-lookup"><span data-stu-id="a1405-164">The slider control is always included in the control view of the UI Automation tree.</span></span>                                                                                                                                           |
| [<span data-ttu-id="a1405-165">**UIA \_ искэйбоардфокусаблепропертид**</span><span class="sxs-lookup"><span data-stu-id="a1405-165">**UIA\_IsKeyboardFocusablePropertyId**</span></span>](uiauto-automation-element-propids.md)   | <span data-ttu-id="a1405-166">См. примечания.</span><span class="sxs-lookup"><span data-stu-id="a1405-166">See notes.</span></span> | <span data-ttu-id="a1405-167">Если элемент управления может получать фокус клавиатуры, он должен поддерживать это свойство.</span><span class="sxs-lookup"><span data-stu-id="a1405-167">If the control can receive keyboard focus, it must support this property.</span></span> <span data-ttu-id="a1405-168">Дочерние элементы (кнопки и бегунки) элемента управления "ползунок" никогда не должны брать фокус.</span><span class="sxs-lookup"><span data-stu-id="a1405-168">The children (buttons and thumb) of a slider control should never take the focus.</span></span> <span data-ttu-id="a1405-169">Фокус должен всегда оставаться на самом элементе управления Slider.</span><span class="sxs-lookup"><span data-stu-id="a1405-169">The focus should always remain on the slider control itself.</span></span>       |
| [<span data-ttu-id="a1405-170">**UIA \_ лабеледбипропертид**</span><span class="sxs-lookup"><span data-stu-id="a1405-170">**UIA\_LabeledByPropertyId**</span></span>](uiauto-automation-element-propids.md)                       | <span data-ttu-id="a1405-171">См. примечания.</span><span class="sxs-lookup"><span data-stu-id="a1405-171">See notes.</span></span> | <span data-ttu-id="a1405-172">Если с элементом управления связана статическая текстовая метка, это свойство должно предоставлять ссылку на этот элемент управления.</span><span class="sxs-lookup"><span data-stu-id="a1405-172">If there is a static text label associated with the control, this property must expose a reference to that control.</span></span> <span data-ttu-id="a1405-173">Если элемент управления "текст" является подкомпонентом другого элемента управления, для него не будет задано свойство **лабеледби** .</span><span class="sxs-lookup"><span data-stu-id="a1405-173">If the text control is a subcomponent of another control, it will not have a **LabeledBy** property set.</span></span>   |
| [<span data-ttu-id="a1405-174">**UIA \_ локализедконтролтипепропертид**</span><span class="sxs-lookup"><span data-stu-id="a1405-174">**UIA\_LocalizedControlTypePropertyId**</span></span>](uiauto-automation-element-propids.md) | <span data-ttu-id="a1405-175">См. примечания.</span><span class="sxs-lookup"><span data-stu-id="a1405-175">See notes.</span></span> | <span data-ttu-id="a1405-176">Локализованная строка, соответствующая типу элемента управления **Slider** .</span><span class="sxs-lookup"><span data-stu-id="a1405-176">Localized string corresponding to the **Slider** control type.</span></span> <span data-ttu-id="a1405-177">Значение по умолчанию — "Slider" для en-US или English (США).</span><span class="sxs-lookup"><span data-stu-id="a1405-177">The default value is "slider" for en-US or English (United States).</span></span>                                                                                             |
| [<span data-ttu-id="a1405-178">**UIA \_ намепропертид**</span><span class="sxs-lookup"><span data-stu-id="a1405-178">**UIA\_NamePropertyId**</span></span>](uiauto-automation-element-propids.md)                                 | <span data-ttu-id="a1405-179">См. примечания.</span><span class="sxs-lookup"><span data-stu-id="a1405-179">See notes.</span></span> | <span data-ttu-id="a1405-180">Имя элемента управления Slider обычно создается на основе статической текстовой метки.</span><span class="sxs-lookup"><span data-stu-id="a1405-180">The name of the slider control is typically generated from a static text label.</span></span> <span data-ttu-id="a1405-181">Если статическая текстовая метка отсутствует, разработчик приложения должен назначить значение свойства **Name** .</span><span class="sxs-lookup"><span data-stu-id="a1405-181">If there is not a static text label, a property value for **Name** must be assigned by the application developer.</span></span>                              |



 

## <a name="required-control-patterns"></a><span data-ttu-id="a1405-182">Обязательные шаблоны элементов управления</span><span class="sxs-lookup"><span data-stu-id="a1405-182">Required Control Patterns</span></span>

<span data-ttu-id="a1405-183">В следующей таблице перечислены шаблоны элементов управления модели автоматизации пользовательского интерфейса, которые должны поддерживаться всеми элементами управления "ползунок".</span><span class="sxs-lookup"><span data-stu-id="a1405-183">The following table lists the UI Automation control patterns required to be supported by all slider controls.</span></span> <span data-ttu-id="a1405-184">Дополнительные сведения о шаблонах элементов управления см. в разделе [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md).</span><span class="sxs-lookup"><span data-stu-id="a1405-184">For more information on control patterns, see [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md).</span></span>



| <span data-ttu-id="a1405-185">Шаблон элемента управления/свойство шаблона</span><span class="sxs-lookup"><span data-stu-id="a1405-185">Control Pattern/Pattern Property</span></span>                          | <span data-ttu-id="a1405-186">Поддержка/значение</span><span class="sxs-lookup"><span data-stu-id="a1405-186">Support/Value</span></span> | <span data-ttu-id="a1405-187">Примечания</span><span class="sxs-lookup"><span data-stu-id="a1405-187">Notes</span></span>                                                                                                                                                                                                                                                                                                      |
|-----------------------------------------------------------|---------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="a1405-188">**IRangeValueProvider**</span><span class="sxs-lookup"><span data-stu-id="a1405-188">**IRangeValueProvider**</span></span>](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irangevalueprovider) | <span data-ttu-id="a1405-189">Зависит</span><span class="sxs-lookup"><span data-stu-id="a1405-189">Depends</span></span>       | <span data-ttu-id="a1405-190">Если содержимому может быть присвоено значение в числовом диапазоне, ползунок должен поддерживать шаблон элемента управления [RangeValue](uiauto-implementingrangevalue.md) .</span><span class="sxs-lookup"><span data-stu-id="a1405-190">A slider should support the [RangeValue](uiauto-implementingrangevalue.md) control pattern if the content can be set to a value within a numerical range.</span></span>                                                                                                                                                 |
| [<span data-ttu-id="a1405-191">**ISelectionProvider**</span><span class="sxs-lookup"><span data-stu-id="a1405-191">**ISelectionProvider**</span></span>](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iselectionprovider)   | <span data-ttu-id="a1405-192">Зависит</span><span class="sxs-lookup"><span data-stu-id="a1405-192">Depends</span></span>       | <span data-ttu-id="a1405-193">Если содержимое представляет одно значение из дискретного набора параметров, ползунок должен поддерживать шаблон элемента управления [Selection](uiauto-implementingselection.md) .</span><span class="sxs-lookup"><span data-stu-id="a1405-193">A slider should support the [Selection](uiauto-implementingselection.md) control pattern if the content represents one value among a discrete set of options.</span></span> <span data-ttu-id="a1405-194">Если шаблон элемента управления Selection поддерживается, соответствующий выбор должен представляться как один или несколько дочерних элементов списка ползунка.</span><span class="sxs-lookup"><span data-stu-id="a1405-194">When the Selection control pattern is supported, the corresponding selection must be exposed as one or more child list items of the slider.</span></span> |
| [<span data-ttu-id="a1405-195">**IValueProvider**</span><span class="sxs-lookup"><span data-stu-id="a1405-195">**IValueProvider**</span></span>](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-ivalueprovider)           | <span data-ttu-id="a1405-196">Зависит</span><span class="sxs-lookup"><span data-stu-id="a1405-196">Depends</span></span>       | <span data-ttu-id="a1405-197">Если содержимое представляет одно значение из дискретного набора параметров, ползунок должен поддерживать шаблон элемента управления [value](uiauto-implementingvalue.md) .</span><span class="sxs-lookup"><span data-stu-id="a1405-197">A slider should support the [Value](uiauto-implementingvalue.md) control pattern if the content represents one value among a discrete set of options.</span></span>                                                                                                                                                     |



 

## <a name="required-events"></a><span data-ttu-id="a1405-198">Обязательные события</span><span class="sxs-lookup"><span data-stu-id="a1405-198">Required Events</span></span>

<span data-ttu-id="a1405-199">В следующей таблице перечислены события модели автоматизации пользовательского интерфейса, которые требуются для поддержки элементов управления Slider.</span><span class="sxs-lookup"><span data-stu-id="a1405-199">The following table lists the UI Automation events that slider controls are required to support.</span></span> <span data-ttu-id="a1405-200">Дополнительные сведения о событиях см. в разделе [UI Automation Events Overview](uiauto-eventsoverview.md).</span><span class="sxs-lookup"><span data-stu-id="a1405-200">For more information on events, see [UI Automation Events Overview](uiauto-eventsoverview.md).</span></span>



| <span data-ttu-id="a1405-201">Событие автоматизации пользовательского интерфейса</span><span class="sxs-lookup"><span data-stu-id="a1405-201">UI Automation Event</span></span>                                                                                                                   | <span data-ttu-id="a1405-202">Примечания</span><span class="sxs-lookup"><span data-stu-id="a1405-202">Notes</span></span>                                                                                                                      |
|---------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="a1405-203">**UIA \_ аутоматионфокусчанжедевентид**</span><span class="sxs-lookup"><span data-stu-id="a1405-203">**UIA\_AutomationFocusChangedEventId**</span></span>](uiauto-event-ids.md)                                      |                                                                                                                            |
| <span data-ttu-id="a1405-204">[**UIA \_**](uiauto-automation-element-propids.md) Событие изменения свойства баундингректанглепропертид.</span><span class="sxs-lookup"><span data-stu-id="a1405-204">[**UIA\_BoundingRectanglePropertyId**](uiauto-automation-element-propids.md) property-changed event.</span></span> |                                                                                                                            |
| <span data-ttu-id="a1405-205">[**UIA \_**](uiauto-automation-element-propids.md) Событие изменения свойства исенабледпропертид.</span><span class="sxs-lookup"><span data-stu-id="a1405-205">[**UIA\_IsEnabledPropertyId**](uiauto-automation-element-propids.md) property-changed event.</span></span>                 | <span data-ttu-id="a1405-206">Если элемент управления поддерживает свойство « [**включено**](uiauto-automation-element-propids.md) », оно должно поддерживать это событие.</span><span class="sxs-lookup"><span data-stu-id="a1405-206">If the control supports the [**IsEnabled**](uiauto-automation-element-propids.md) property, it must support this event.</span></span>   |
| <span data-ttu-id="a1405-207">[**UIA \_**](uiauto-automation-element-propids.md) Событие изменения свойства исоффскринпропертид.</span><span class="sxs-lookup"><span data-stu-id="a1405-207">[**UIA\_IsOffscreenPropertyId**](uiauto-automation-element-propids.md) property-changed event.</span></span>             | <span data-ttu-id="a1405-208">Если элемент управления поддерживает свойство [**исоффскрин**](uiauto-automation-element-propids.md) , он должен поддерживать это событие.</span><span class="sxs-lookup"><span data-stu-id="a1405-208">If the control supports the [**IsOffscreen**](uiauto-automation-element-propids.md) property, it must support this event.</span></span> |
| <span data-ttu-id="a1405-209">[**UIA \_**](uiauto-control-pattern-propids.md) Событие изменения свойства ранжевалуевалуепропертид.</span><span class="sxs-lookup"><span data-stu-id="a1405-209">[**UIA\_RangeValueValuePropertyId**](uiauto-control-pattern-propids.md) property-changed event.</span></span>        | <span data-ttu-id="a1405-210">Если элемент управления поддерживает шаблон элемента управления [RangeValue](uiauto-implementingrangevalue.md) , он должен поддерживать это событие.</span><span class="sxs-lookup"><span data-stu-id="a1405-210">If the control supports the [RangeValue](uiauto-implementingrangevalue.md) control pattern, it must support this event.</span></span>   |
| [<span data-ttu-id="a1405-211">**\_Выбор UIA \_ инвалидатедевентид**</span><span class="sxs-lookup"><span data-stu-id="a1405-211">**UIA\_Selection\_InvalidatedEventId**</span></span>](uiauto-event-ids.md)                                       | <span data-ttu-id="a1405-212">Если элемент управления поддерживает шаблон элемента управления [Selection](uiauto-implementingselection.md) , он должен поддерживать это событие.</span><span class="sxs-lookup"><span data-stu-id="a1405-212">If the control supports the [Selection](uiauto-implementingselection.md) control pattern, it must support this event.</span></span>     |
| [<span data-ttu-id="a1405-213">**UIA \_ структуречанжедевентид**</span><span class="sxs-lookup"><span data-stu-id="a1405-213">**UIA\_StructureChangedEventId**</span></span>](uiauto-event-ids.md)                                                  |                                                                                                                            |
| <span data-ttu-id="a1405-214">[**UIA \_**](uiauto-control-pattern-propids.md) Событие изменения свойства валуевалуепропертид.</span><span class="sxs-lookup"><span data-stu-id="a1405-214">[**UIA\_ValueValuePropertyId**](uiauto-control-pattern-propids.md) property-changed event.</span></span>                  | <span data-ttu-id="a1405-215">Если элемент управления поддерживает шаблон элемента управления [value](uiauto-implementingvalue.md) , он должен поддерживать это событие.</span><span class="sxs-lookup"><span data-stu-id="a1405-215">If the control supports the [Value](uiauto-implementingvalue.md) control pattern, it must support this event.</span></span>             |



 

## <a name="related-topics"></a><span data-ttu-id="a1405-216">См. также</span><span class="sxs-lookup"><span data-stu-id="a1405-216">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="a1405-217">**Зрения**</span><span class="sxs-lookup"><span data-stu-id="a1405-217">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="a1405-218">Общие сведения о типах элементов управления автоматизации пользовательского интерфейса</span><span class="sxs-lookup"><span data-stu-id="a1405-218">UI Automation Control Types Overview</span></span>](uiauto-controltypesoverview.md)
</dt> <dt>

[<span data-ttu-id="a1405-219">Общие сведения о модели автоматизации пользовательского интерфейса</span><span class="sxs-lookup"><span data-stu-id="a1405-219">UI Automation Overview</span></span>](uiauto-uiautomationoverview.md)
</dt> </dl>

 

 




