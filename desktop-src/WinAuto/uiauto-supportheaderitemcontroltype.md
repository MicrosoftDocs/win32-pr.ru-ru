---
title: Тип элемента управления HeaderItem
description: В этом разделе содержатся сведения о поддержке автоматизации пользовательского интерфейса Майкрософт для типа элемента управления HeaderItem.
ms.assetid: c70420d6-d9f3-47c8-a09f-35ed170f815f
keywords:
- Модель автоматизации пользовательского интерфейса, поддержка типа элемента управления HeaderItem
- Модель автоматизации пользовательского интерфейса, тип элемента управления HeaderItem
- Модель автоматизации пользовательского интерфейса, древовидная структура для типа элемента управления HeaderItem
- Модель автоматизации пользовательского интерфейса, свойства для типа элемента управления HeaderItem
- Модель автоматизации пользовательского интерфейса, шаблоны элементов управления для типа элемента управления HeaderItem
- Модель автоматизации пользовательского интерфейса, события для типа элемента управления HeaderItem
- Древовидные структуры, тип элемента управления HeaderItem
- свойства, тип элемента управления HeaderItem
- шаблоны элементов управления, тип элемента управления HeaderItem
- события, тип элемента управления HeaderItem
- Поддержка типа элемента управления HeaderItem
- Тип элемента управления HeaderItem
- типы элементов управления, древовидная структура для типа элемента управления HeaderItem
- типы элементов управления, шаблоны элементов управления для типа элемента управления HeaderItem
- типы элементов управления, поддержка HeaderItem
- типы элементов управления, HeaderItem
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1bab61f92a6ab4db221810f9f083279ade4bf353
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "105700545"
---
# <a name="headeritem-control-type"></a><span data-ttu-id="fd45d-119">Тип элемента управления HeaderItem</span><span class="sxs-lookup"><span data-stu-id="fd45d-119">HeaderItem Control Type</span></span>

<span data-ttu-id="fd45d-120">В этом разделе содержатся сведения о поддержке автоматизации пользовательского интерфейса Майкрософт для типа элемента управления **HeaderItem** .</span><span class="sxs-lookup"><span data-stu-id="fd45d-120">This topic provides information about Microsoft UI Automation support for the **HeaderItem** control type.</span></span>

<span data-ttu-id="fd45d-121">Тип элемента управления **HeaderItem** предоставляет визуальную метку для строки или столбца данных.</span><span class="sxs-lookup"><span data-stu-id="fd45d-121">The **HeaderItem** control type provides a visual label for a row or column of information.</span></span>

<span data-ttu-id="fd45d-122">В следующих разделах определяется необходимая древовидная структура модели автоматизации пользовательского интерфейса, свойства, шаблоны элементов управления и события для типа элемента управления **HeaderItem** .</span><span class="sxs-lookup"><span data-stu-id="fd45d-122">The following sections define the required UI Automation tree structure, properties, control patterns, and events for the **HeaderItem** control type.</span></span> <span data-ttu-id="fd45d-123">Требования к автоматизации пользовательского интерфейса применяются ко всем элементам управления "элемент заголовка", в которых платформа или платформа пользовательского интерфейса интегрирует поддержку автоматизации пользовательского интерфейса для типов элементов управления и шаблонов элементов управления.</span><span class="sxs-lookup"><span data-stu-id="fd45d-123">The UI Automation requirements apply to all header item controls where the UI framework/platform integrates UI Automation support for control types and control patterns.</span></span>

<span data-ttu-id="fd45d-124">В этом разделе содержатся следующие подразделы.</span><span class="sxs-lookup"><span data-stu-id="fd45d-124">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="fd45d-125">Типичная древовидная структура</span><span class="sxs-lookup"><span data-stu-id="fd45d-125">Typical Tree Structure</span></span>](#typical-tree-structure)
-   [<span data-ttu-id="fd45d-126">Соответствующие свойства</span><span class="sxs-lookup"><span data-stu-id="fd45d-126">Relevant Properties</span></span>](#relevant-properties)
-   [<span data-ttu-id="fd45d-127">Обязательные шаблоны элементов управления</span><span class="sxs-lookup"><span data-stu-id="fd45d-127">Required Control Patterns</span></span>](#required-control-patterns)
-   [<span data-ttu-id="fd45d-128">Обязательные события</span><span class="sxs-lookup"><span data-stu-id="fd45d-128">Required Events</span></span>](#required-events)
-   [<span data-ttu-id="fd45d-129">См. также</span><span class="sxs-lookup"><span data-stu-id="fd45d-129">Related topics</span></span>](#related-topics)

## <a name="typical-tree-structure"></a><span data-ttu-id="fd45d-130">Типичная древовидная структура</span><span class="sxs-lookup"><span data-stu-id="fd45d-130">Typical Tree Structure</span></span>

<span data-ttu-id="fd45d-131">В следующей таблице описывается типичный элемент управления и представление содержимого дерева модели автоматизации пользовательского интерфейса, которое относится к элементам управления "элемент заголовка" и описывает, что может содержаться в каждом представлении.</span><span class="sxs-lookup"><span data-stu-id="fd45d-131">The following table depicts a typical control and content view of the UI Automation tree that pertains to header item controls and describes what can be contained in each view.</span></span> <span data-ttu-id="fd45d-132">Дополнительные сведения о дереве автоматизации пользовательского интерфейса см. в разделе [Общие сведения о дереве модели автоматизации пользовательского интерфейса](uiauto-treeoverview.md).</span><span class="sxs-lookup"><span data-stu-id="fd45d-132">For more information about the UI Automation tree, see [UI Automation Tree Overview](uiauto-treeoverview.md).</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="fd45d-133">Представление элемента управления</span><span class="sxs-lookup"><span data-stu-id="fd45d-133">Control View</span></span></th>
<th><span data-ttu-id="fd45d-134">Представление содержимого</span><span class="sxs-lookup"><span data-stu-id="fd45d-134">Content View</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><ul>
<li><span data-ttu-id="fd45d-135">HeaderItem</span><span class="sxs-lookup"><span data-stu-id="fd45d-135">HeaderItem</span></span></li>
</ul></td>
<td><span data-ttu-id="fd45d-136">(Неприменимо)</span><span class="sxs-lookup"><span data-stu-id="fd45d-136">(Not applicable)</span></span></td>
</tr>
</tbody>
</table>



 

## <a name="relevant-properties"></a><span data-ttu-id="fd45d-137">Соответствующие свойства</span><span class="sxs-lookup"><span data-stu-id="fd45d-137">Relevant Properties</span></span>

<span data-ttu-id="fd45d-138">В следующей таблице перечислены свойства модели автоматизации пользовательского интерфейса, значения или определения которых особенно важны для типа элемента управления **HeaderItem** .</span><span class="sxs-lookup"><span data-stu-id="fd45d-138">The following table lists the UI Automation properties whose value or definition is especially relevant to the **HeaderItem** control type.</span></span> <span data-ttu-id="fd45d-139">Дополнительные сведения о свойствах модели автоматизации пользовательского интерфейса см. в разделе [Получение свойств элементов модели автоматизации пользовательского интерфейса](uiauto-propertiesforclients.md).</span><span class="sxs-lookup"><span data-stu-id="fd45d-139">For more information about UI Automation properties, see [Retrieving Properties from UI Automation Elements](uiauto-propertiesforclients.md).</span></span>



| <span data-ttu-id="fd45d-140">Свойство модели автоматизации пользовательского интерфейса</span><span class="sxs-lookup"><span data-stu-id="fd45d-140">UI Automation Property</span></span>                                                                                              | <span data-ttu-id="fd45d-141">Значение</span><span class="sxs-lookup"><span data-stu-id="fd45d-141">Value</span></span>          | <span data-ttu-id="fd45d-142">Примечания</span><span class="sxs-lookup"><span data-stu-id="fd45d-142">Notes</span></span>                                                                                                                                                                                                |
|---------------------------------------------------------------------------------------------------------------------|----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="fd45d-143">**UIA \_ аутоматионидпропертид**</span><span class="sxs-lookup"><span data-stu-id="fd45d-143">**UIA\_AutomationIdPropertyId**</span></span>](uiauto-automation-element-propids.md)                 | <span data-ttu-id="fd45d-144">См. примечания.</span><span class="sxs-lookup"><span data-stu-id="fd45d-144">See notes.</span></span>     | <span data-ttu-id="fd45d-145">Значение этого свойства должно быть уникальным среди всех одноранговых элементов в необработанном представлении дерева модели автоматизации пользовательского интерфейса.</span><span class="sxs-lookup"><span data-stu-id="fd45d-145">The value of this property must be unique among all peer elements in the raw view of the UI Automation tree.</span></span>                                                                                         |
| [<span data-ttu-id="fd45d-146">**UIA \_ баундингректанглепропертид**</span><span class="sxs-lookup"><span data-stu-id="fd45d-146">**UIA\_BoundingRectanglePropertyId**</span></span>](uiauto-automation-element-propids.md)       | <span data-ttu-id="fd45d-147">См. примечания.</span><span class="sxs-lookup"><span data-stu-id="fd45d-147">See notes.</span></span>     | <span data-ttu-id="fd45d-148">Внешний прямоугольник, содержащий весь элемент управления.</span><span class="sxs-lookup"><span data-stu-id="fd45d-148">The outermost rectangle that contains the whole control.</span></span>                                                                                                                                             |
| [<span data-ttu-id="fd45d-149">**UIA \_ кликкаблепоинтпропертид**</span><span class="sxs-lookup"><span data-stu-id="fd45d-149">**UIA\_ClickablePointPropertyId**</span></span>](uiauto-automation-element-propids.md)             | <span data-ttu-id="fd45d-150">См. примечания.</span><span class="sxs-lookup"><span data-stu-id="fd45d-150">See notes.</span></span>     | <span data-ttu-id="fd45d-151">Поддерживается при наличии ограничивающего прямоугольника.</span><span class="sxs-lookup"><span data-stu-id="fd45d-151">Supported if there is a bounding rectangle.</span></span> <span data-ttu-id="fd45d-152">Если не все точки внутри ограничивающего прямоугольника являются щелчками, а элемент выполняет специализированное тестирование нажатия, переопределите и предоставьте точку для щелчка.</span><span class="sxs-lookup"><span data-stu-id="fd45d-152">If not every point within the bounding rectangle is clickable, and the element performs specialized hit testing, override and provide a clickable point.</span></span> |
| [<span data-ttu-id="fd45d-153">**UIA \_ контролтипепропертид**</span><span class="sxs-lookup"><span data-stu-id="fd45d-153">**UIA\_ControlTypePropertyId**</span></span>](uiauto-automation-element-propids.md)                   | <span data-ttu-id="fd45d-154">**HeaderItem**</span><span class="sxs-lookup"><span data-stu-id="fd45d-154">**HeaderItem**</span></span> | <span data-ttu-id="fd45d-155">Это значение одинаково для всех инфраструктур пользовательского интерфейса.</span><span class="sxs-lookup"><span data-stu-id="fd45d-155">This value is the same for all UI frameworks.</span></span>                                                                                                                                                        |
| [<span data-ttu-id="fd45d-156">**UIA \_ исконтентелементпропертид**</span><span class="sxs-lookup"><span data-stu-id="fd45d-156">**UIA\_IsContentElementPropertyId**</span></span>](uiauto-automation-element-propids.md)         | <span data-ttu-id="fd45d-157">FALSE</span><span class="sxs-lookup"><span data-stu-id="fd45d-157">FALSE</span></span>          | <span data-ttu-id="fd45d-158">Элемент управления "элемент заголовка" не включен в представление содержимого дерева модели автоматизации пользовательского интерфейса.</span><span class="sxs-lookup"><span data-stu-id="fd45d-158">The header item control is not included in the content view of the UI Automation tree.</span></span>                                                                                                               |
| [<span data-ttu-id="fd45d-159">**UIA \_ исконтролелементпропертид**</span><span class="sxs-lookup"><span data-stu-id="fd45d-159">**UIA\_IsControlElementPropertyId**</span></span>](uiauto-automation-element-propids.md)         | <span data-ttu-id="fd45d-160">true</span><span class="sxs-lookup"><span data-stu-id="fd45d-160">TRUE</span></span>           | <span data-ttu-id="fd45d-161">Элемент управления "заголовок" всегда включается в представление элемента управления дерева модели автоматизации пользовательского интерфейса.</span><span class="sxs-lookup"><span data-stu-id="fd45d-161">The header item control is always included in the control view of the UI Automation tree.</span></span>                                                                                                            |
| [<span data-ttu-id="fd45d-162">**UIA \_ искэйбоардфокусаблепропертид**</span><span class="sxs-lookup"><span data-stu-id="fd45d-162">**UIA\_IsKeyboardFocusablePropertyId**</span></span>](uiauto-automation-element-propids.md)   | <span data-ttu-id="fd45d-163">См. примечания.</span><span class="sxs-lookup"><span data-stu-id="fd45d-163">See notes.</span></span>     | <span data-ttu-id="fd45d-164">Если элемент управления может получать фокус клавиатуры, он должен поддерживать это свойство.</span><span class="sxs-lookup"><span data-stu-id="fd45d-164">If the control can receive keyboard focus, it must support this property.</span></span>                                                                                                                            |
| [<span data-ttu-id="fd45d-165">**UIA \_ итемстатуспропертид**</span><span class="sxs-lookup"><span data-stu-id="fd45d-165">**UIA\_ItemStatusPropertyId**</span></span>](uiauto-automation-element-propids.md)                     | <span data-ttu-id="fd45d-166">См. примечания</span><span class="sxs-lookup"><span data-stu-id="fd45d-166">See notes</span></span>      | <span data-ttu-id="fd45d-167">Это свойство предоставляет сведения для порядков сортировки по элементу заголовка.</span><span class="sxs-lookup"><span data-stu-id="fd45d-167">This property provides information for sort orders by the header item.</span></span>                                                                                                                               |
| [<span data-ttu-id="fd45d-168">**UIA \_ лабеледбипропертид**</span><span class="sxs-lookup"><span data-stu-id="fd45d-168">**UIA\_LabeledByPropertyId**</span></span>](uiauto-automation-element-propids.md)                       | <span data-ttu-id="fd45d-169">NULL</span><span class="sxs-lookup"><span data-stu-id="fd45d-169">NULL</span></span>           | <span data-ttu-id="fd45d-170">Элементы управления "элемент заголовка" не имеют статической текстовой метки.</span><span class="sxs-lookup"><span data-stu-id="fd45d-170">Header item controls do not have a static text label.</span></span>                                                                                                                                                |
| [<span data-ttu-id="fd45d-171">**UIA \_ локализедконтролтипепропертид**</span><span class="sxs-lookup"><span data-stu-id="fd45d-171">**UIA\_LocalizedControlTypePropertyId**</span></span>](uiauto-automation-element-propids.md) | <span data-ttu-id="fd45d-172">См. примечания.</span><span class="sxs-lookup"><span data-stu-id="fd45d-172">See notes.</span></span>     | <span data-ttu-id="fd45d-173">Локализованная строка, соответствующая типу элемента управления **HeaderItem** .</span><span class="sxs-lookup"><span data-stu-id="fd45d-173">Localized string corresponding to the **HeaderItem** control type.</span></span> <span data-ttu-id="fd45d-174">Значение по умолчанию — "элемент заголовка" для en-US или English (США).</span><span class="sxs-lookup"><span data-stu-id="fd45d-174">The default value is "header item" for en-US or English (United States).</span></span>                                                          |
| [<span data-ttu-id="fd45d-175">**UIA \_ намепропертид**</span><span class="sxs-lookup"><span data-stu-id="fd45d-175">**UIA\_NamePropertyId**</span></span>](uiauto-automation-element-propids.md)                                 | <span data-ttu-id="fd45d-176">См. примечания.</span><span class="sxs-lookup"><span data-stu-id="fd45d-176">See notes.</span></span>     | <span data-ttu-id="fd45d-177">Элемент управления "Элемент заголовка" всегда получает метку автоматически.</span><span class="sxs-lookup"><span data-stu-id="fd45d-177">The header item control is always self-labeling.</span></span>                                                                                                                                                     |



 

## <a name="required-control-patterns"></a><span data-ttu-id="fd45d-178">Обязательные шаблоны элементов управления</span><span class="sxs-lookup"><span data-stu-id="fd45d-178">Required Control Patterns</span></span>

<span data-ttu-id="fd45d-179">В следующей таблице перечислены шаблоны элементов управления модели автоматизации пользовательского интерфейса, которые должны поддерживаться всеми элементами управления "элемент заголовка".</span><span class="sxs-lookup"><span data-stu-id="fd45d-179">The following table lists the UI Automation control patterns required to be supported by all header item controls.</span></span> <span data-ttu-id="fd45d-180">Дополнительные сведения о шаблонах элементов управления см. в разделе [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md).</span><span class="sxs-lookup"><span data-stu-id="fd45d-180">For more information on control patterns, see [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md).</span></span>



| <span data-ttu-id="fd45d-181">Шаблон элемента управления</span><span class="sxs-lookup"><span data-stu-id="fd45d-181">Control Pattern</span></span>                                         | <span data-ttu-id="fd45d-182">Поддержка</span><span class="sxs-lookup"><span data-stu-id="fd45d-182">Support</span></span> | <span data-ttu-id="fd45d-183">Примечания</span><span class="sxs-lookup"><span data-stu-id="fd45d-183">Notes</span></span>                                                                                                                             |
|---------------------------------------------------------|---------|-----------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="fd45d-184">**IInvokeProvider**</span><span class="sxs-lookup"><span data-stu-id="fd45d-184">**IInvokeProvider**</span></span>](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iinvokeprovider)       | <span data-ttu-id="fd45d-185">Зависит</span><span class="sxs-lookup"><span data-stu-id="fd45d-185">Depends</span></span> | <span data-ttu-id="fd45d-186">Реализуйте шаблон элемента управления [Invoke](uiauto-implementinginvoke.md) , если элемент управления "элемент заголовка" можно щелкнуть для сортировки данных.</span><span class="sxs-lookup"><span data-stu-id="fd45d-186">Implement the [Invoke](uiauto-implementinginvoke.md) control pattern if the header item control can be clicked to sort the data.</span></span> |
| [<span data-ttu-id="fd45d-187">**ITransformProvider**</span><span class="sxs-lookup"><span data-stu-id="fd45d-187">**ITransformProvider**</span></span>](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itransformprovider) | <span data-ttu-id="fd45d-188">Зависит</span><span class="sxs-lookup"><span data-stu-id="fd45d-188">Depends</span></span> | <span data-ttu-id="fd45d-189">Реализуйте шаблон элемента управления [Transform](uiauto-implementingtransform.md) , если размер элемента управления заголовка может быть изменен.</span><span class="sxs-lookup"><span data-stu-id="fd45d-189">Implement the [Transform](uiauto-implementingtransform.md) control pattern if the header item control can be resized.</span></span>            |



 

## <a name="required-events"></a><span data-ttu-id="fd45d-190">Обязательные события</span><span class="sxs-lookup"><span data-stu-id="fd45d-190">Required Events</span></span>

<span data-ttu-id="fd45d-191">В следующей таблице перечислены события автоматизации пользовательского интерфейса, которые должны поддерживать элементы управления "элемент заголовка".</span><span class="sxs-lookup"><span data-stu-id="fd45d-191">The following table lists the UI Automation events that header item controls are required to support.</span></span> <span data-ttu-id="fd45d-192">Дополнительные сведения о событиях см. в разделе [UI Automation Events Overview](uiauto-eventsoverview.md).</span><span class="sxs-lookup"><span data-stu-id="fd45d-192">For more information on events, see [UI Automation Events Overview](uiauto-eventsoverview.md).</span></span>



| <span data-ttu-id="fd45d-193">Событие автоматизации пользовательского интерфейса</span><span class="sxs-lookup"><span data-stu-id="fd45d-193">UI Automation Event</span></span>                                                                                                                   | <span data-ttu-id="fd45d-194">Примечания</span><span class="sxs-lookup"><span data-stu-id="fd45d-194">Notes</span></span>                                                                                                                      |
|---------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="fd45d-195">**UIA \_ аутоматионфокусчанжедевентид**</span><span class="sxs-lookup"><span data-stu-id="fd45d-195">**UIA\_AutomationFocusChangedEventId**</span></span>](uiauto-event-ids.md)                                      |                                                                                                                            |
| <span data-ttu-id="fd45d-196">[**UIA \_**](uiauto-automation-element-propids.md) Событие изменения свойства баундингректанглепропертид.</span><span class="sxs-lookup"><span data-stu-id="fd45d-196">[**UIA\_BoundingRectanglePropertyId**](uiauto-automation-element-propids.md) property-changed event.</span></span> |                                                                                                                            |
| [<span data-ttu-id="fd45d-197">**UIA \_ Invoke \_ инвокедевентид**</span><span class="sxs-lookup"><span data-stu-id="fd45d-197">**UIA\_Invoke\_InvokedEventId**</span></span>](uiauto-event-ids.md)                                                     | <span data-ttu-id="fd45d-198">Если элемент управления поддерживает шаблон элемента управления [Invoke](uiauto-implementinginvoke.md) , он должен поддерживать это событие.</span><span class="sxs-lookup"><span data-stu-id="fd45d-198">If the control supports the [Invoke](uiauto-implementinginvoke.md) control pattern, it must support this event.</span></span>           |
| <span data-ttu-id="fd45d-199">[**UIA \_**](uiauto-automation-element-propids.md) Событие изменения свойства исенабледпропертид.</span><span class="sxs-lookup"><span data-stu-id="fd45d-199">[**UIA\_IsEnabledPropertyId**](uiauto-automation-element-propids.md) property-changed event.</span></span>                 | <span data-ttu-id="fd45d-200">Если элемент управления поддерживает свойство « [**включено**](uiauto-automation-element-propids.md) », оно должно поддерживать это событие.</span><span class="sxs-lookup"><span data-stu-id="fd45d-200">If the control supports the [**IsEnabled**](uiauto-automation-element-propids.md) property, it must support this event.</span></span>   |
| <span data-ttu-id="fd45d-201">[**UIA \_**](uiauto-automation-element-propids.md) Событие изменения свойства исоффскринпропертид.</span><span class="sxs-lookup"><span data-stu-id="fd45d-201">[**UIA\_IsOffscreenPropertyId**](uiauto-automation-element-propids.md) property-changed event.</span></span>             | <span data-ttu-id="fd45d-202">Если элемент управления поддерживает свойство [**исоффскрин**](uiauto-automation-element-propids.md) , он должен поддерживать это событие.</span><span class="sxs-lookup"><span data-stu-id="fd45d-202">If the control supports the [**IsOffscreen**](uiauto-automation-element-propids.md) property, it must support this event.</span></span> |
| [<span data-ttu-id="fd45d-203">**UIA \_ структуречанжедевентид**</span><span class="sxs-lookup"><span data-stu-id="fd45d-203">**UIA\_StructureChangedEventId**</span></span>](uiauto-event-ids.md)                                                  |                                                                                                                            |



 

## <a name="related-topics"></a><span data-ttu-id="fd45d-204">См. также</span><span class="sxs-lookup"><span data-stu-id="fd45d-204">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="fd45d-205">**Зрения**</span><span class="sxs-lookup"><span data-stu-id="fd45d-205">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="fd45d-206">Общие сведения о типах элементов управления автоматизации пользовательского интерфейса</span><span class="sxs-lookup"><span data-stu-id="fd45d-206">UI Automation Control Types Overview</span></span>](uiauto-controltypesoverview.md)
</dt> <dt>

[<span data-ttu-id="fd45d-207">Общие сведения о модели автоматизации пользовательского интерфейса</span><span class="sxs-lookup"><span data-stu-id="fd45d-207">UI Automation Overview</span></span>](uiauto-uiautomationoverview.md)
</dt> </dl>

 

 




