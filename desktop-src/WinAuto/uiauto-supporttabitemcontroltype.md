---
title: Тип элемента управления TabItem
description: В этом разделе содержатся сведения о поддержке автоматизации пользовательского интерфейса Майкрософт для типа элемента управления TabItem.
ms.assetid: 97b8c043-1ac5-4e14-be80-8687300a10a2
keywords:
- Модель автоматизации пользовательского интерфейса, поддержка типа элемента управления TabItem
- Модель автоматизации пользовательского интерфейса, тип элемента управления TabItem
- Модель автоматизации пользовательского интерфейса, древовидная структура для типа элемента управления TabItem
- Модель автоматизации пользовательского интерфейса, свойства для типа элемента управления TabItem
- Модель автоматизации пользовательского интерфейса, шаблоны элементов управления для типа элемента управления TabItem
- Модель автоматизации пользовательского интерфейса, события для типа элемента управления TabItem
- Древовидные структуры, тип элемента управления TabItem
- свойства, тип элемента управления TabItem
- шаблоны элементов управления, тип элемента управления TabItem
- события, тип элемента управления TabItem
- Поддержка типа элемента управления TabItem
- Тип элемента управления TabItem
- типы элементов управления, древовидная структура для типа элемента управления TabItem
- типы элементов управления, шаблоны элементов управления для типа элемента управления TabItem
- типы элементов управления, поддержка TabItem
- типы элементов управления, TabItem
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a1e8f9f900240318de8629048f242cd755994c78
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104258848"
---
# <a name="tabitem-control-type"></a><span data-ttu-id="13268-119">Тип элемента управления TabItem</span><span class="sxs-lookup"><span data-stu-id="13268-119">TabItem Control Type</span></span>

<span data-ttu-id="13268-120">В этом разделе содержатся сведения о поддержке автоматизации пользовательского интерфейса Майкрософт для типа элемента управления **TabItem** .</span><span class="sxs-lookup"><span data-stu-id="13268-120">This topic provides information about Microsoft UI Automation support for the **TabItem** control type.</span></span>

<span data-ttu-id="13268-121">Элемент управления «Элемент вкладки» используется в элементе управления «Вкладка» для выбора определенной страницы, которая должна отображаться в окне.</span><span class="sxs-lookup"><span data-stu-id="13268-121">A tab item control is used as the control within a tab control that selects a specific page to be shown in a window.</span></span>

<span data-ttu-id="13268-122">В следующих разделах определяется необходимая древовидная структура модели автоматизации пользовательского интерфейса, свойства, шаблоны элементов управления и события для типа элемента управления **TabItem** .</span><span class="sxs-lookup"><span data-stu-id="13268-122">The following sections define the required UI Automation tree structure, properties, control patterns, and events for the **TabItem** control type.</span></span> <span data-ttu-id="13268-123">Требования к автоматизации пользовательского интерфейса применяются ко всем элементам управления "элемент вкладки", где платформа или платформа пользовательского интерфейса интегрирует поддержку автоматизации пользовательского интерфейса для типов элементов управления и шаблонов элементов управления.</span><span class="sxs-lookup"><span data-stu-id="13268-123">The UI Automation requirements apply to all tab item controls where the UI framework/platform integrates UI Automation support for control types and control patterns.</span></span>

<span data-ttu-id="13268-124">В этом разделе содержатся следующие подразделы.</span><span class="sxs-lookup"><span data-stu-id="13268-124">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="13268-125">Типичная древовидная структура</span><span class="sxs-lookup"><span data-stu-id="13268-125">Typical Tree Structure</span></span>](#typical-tree-structure)
-   [<span data-ttu-id="13268-126">Соответствующие свойства</span><span class="sxs-lookup"><span data-stu-id="13268-126">Relevant Properties</span></span>](#relevant-properties)
-   [<span data-ttu-id="13268-127">Обязательные шаблоны элементов управления</span><span class="sxs-lookup"><span data-stu-id="13268-127">Required Control Patterns</span></span>](#required-control-patterns)
-   [<span data-ttu-id="13268-128">Обязательные события</span><span class="sxs-lookup"><span data-stu-id="13268-128">Required Events</span></span>](#required-events)
-   [<span data-ttu-id="13268-129">См. также</span><span class="sxs-lookup"><span data-stu-id="13268-129">Related topics</span></span>](#related-topics)

## <a name="typical-tree-structure"></a><span data-ttu-id="13268-130">Типичная древовидная структура</span><span class="sxs-lookup"><span data-stu-id="13268-130">Typical Tree Structure</span></span>

<span data-ttu-id="13268-131">В следующей таблице описывается типичный элемент управления и представление содержимого дерева модели автоматизации пользовательского интерфейса, которое относится к элементам управления "элемент вкладки" и описывает, что может содержаться в каждом представлении.</span><span class="sxs-lookup"><span data-stu-id="13268-131">The following table depicts a typical control and content view of the UI Automation tree that pertains to tab item controls and describes what can be contained in each view.</span></span> <span data-ttu-id="13268-132">Дополнительные сведения о дереве автоматизации пользовательского интерфейса см. в разделе [Общие сведения о дереве модели автоматизации пользовательского интерфейса](uiauto-treeoverview.md).</span><span class="sxs-lookup"><span data-stu-id="13268-132">For more information about the UI Automation tree, see [UI Automation Tree Overview](uiauto-treeoverview.md).</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="13268-133">Представление элемента управления</span><span class="sxs-lookup"><span data-stu-id="13268-133">Control View</span></span></th>
<th><span data-ttu-id="13268-134">Представление содержимого</span><span class="sxs-lookup"><span data-stu-id="13268-134">Content View</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><ul>
<li><span data-ttu-id="13268-135">TabItem</span><span class="sxs-lookup"><span data-stu-id="13268-135">TabItem</span></span>
<ul>
<li><span data-ttu-id="13268-136">Image (0 или 1)</span><span class="sxs-lookup"><span data-stu-id="13268-136">Image (0 or 1)</span></span></li>
<li><span data-ttu-id="13268-137">Текст</span><span class="sxs-lookup"><span data-stu-id="13268-137">Text</span></span></li>
<li><span data-ttu-id="13268-138">Панель</span><span class="sxs-lookup"><span data-stu-id="13268-138">Pane</span></span>
<ul>
<li><span data-ttu-id="13268-139">Различные элементы управления (0 или более)</span><span class="sxs-lookup"><span data-stu-id="13268-139">Various controls (0 or more)</span></span></li>
</ul></li>
</ul></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="13268-140">TabItem</span><span class="sxs-lookup"><span data-stu-id="13268-140">TabItem</span></span>
<ul>
<li><span data-ttu-id="13268-141">Панель</span><span class="sxs-lookup"><span data-stu-id="13268-141">Pane</span></span>
<ul>
<li><span data-ttu-id="13268-142">Различные элементы управления (0 или более)</span><span class="sxs-lookup"><span data-stu-id="13268-142">Various controls (0 or more)</span></span></li>
</ul></li>
</ul></li>
</ul></td>
</tr>
</tbody>
</table>



 

## <a name="relevant-properties"></a><span data-ttu-id="13268-143">Соответствующие свойства</span><span class="sxs-lookup"><span data-stu-id="13268-143">Relevant Properties</span></span>

<span data-ttu-id="13268-144">В следующей таблице перечислены свойства модели автоматизации пользовательского интерфейса, значения или определения которых особенно важны для типа элемента управления **TabItem** .</span><span class="sxs-lookup"><span data-stu-id="13268-144">The following table lists the UI Automation properties whose value or definition is especially relevant to the **TabItem** control type.</span></span> <span data-ttu-id="13268-145">Дополнительные сведения о свойствах модели автоматизации пользовательского интерфейса см. в разделе [Получение свойств элементов модели автоматизации пользовательского интерфейса](uiauto-propertiesforclients.md).</span><span class="sxs-lookup"><span data-stu-id="13268-145">For more information about UI Automation properties, see [Retrieving Properties from UI Automation Elements](uiauto-propertiesforclients.md).</span></span>



| <span data-ttu-id="13268-146">Свойство модели автоматизации пользовательского интерфейса</span><span class="sxs-lookup"><span data-stu-id="13268-146">UI Automation Property</span></span>                                                                                              | <span data-ttu-id="13268-147">Значение</span><span class="sxs-lookup"><span data-stu-id="13268-147">Value</span></span>       | <span data-ttu-id="13268-148">Примечания</span><span class="sxs-lookup"><span data-stu-id="13268-148">Notes</span></span>                                                                                                                                       |
|---------------------------------------------------------------------------------------------------------------------|-------------|---------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="13268-149">**UIA \_ аутоматионидпропертид**</span><span class="sxs-lookup"><span data-stu-id="13268-149">**UIA\_AutomationIdPropertyId**</span></span>](uiauto-automation-element-propids.md)                 | <span data-ttu-id="13268-150">См. примечания.</span><span class="sxs-lookup"><span data-stu-id="13268-150">See notes.</span></span>  | <span data-ttu-id="13268-151">Значение этого свойства должно быть уникальным среди всех одноранговых элементов в необработанном представлении дерева модели автоматизации пользовательского интерфейса.</span><span class="sxs-lookup"><span data-stu-id="13268-151">The value of this property must be unique among all peer elements in the raw view of the UI Automation tree.</span></span>                                |
| [<span data-ttu-id="13268-152">**UIA \_ баундингректанглепропертид**</span><span class="sxs-lookup"><span data-stu-id="13268-152">**UIA\_BoundingRectanglePropertyId**</span></span>](uiauto-automation-element-propids.md)       | <span data-ttu-id="13268-153">См. примечания.</span><span class="sxs-lookup"><span data-stu-id="13268-153">See notes.</span></span>  | <span data-ttu-id="13268-154">Внешний прямоугольник, содержащий весь элемент управления.</span><span class="sxs-lookup"><span data-stu-id="13268-154">The outermost rectangle that contains the whole control.</span></span>                                                                                    |
| [<span data-ttu-id="13268-155">**UIA \_ кликкаблепоинтпропертид**</span><span class="sxs-lookup"><span data-stu-id="13268-155">**UIA\_ClickablePointPropertyId**</span></span>](uiauto-automation-element-propids.md)             | <span data-ttu-id="13268-156">См. примечания.</span><span class="sxs-lookup"><span data-stu-id="13268-156">See notes.</span></span>  | <span data-ttu-id="13268-157">Элемент управления «Элемент вкладки» должен иметь активную точку, которая приводит к выбору этого элемента.</span><span class="sxs-lookup"><span data-stu-id="13268-157">The tab item control must have a clickable point that causes the item to become selected.</span></span>                                                   |
| [<span data-ttu-id="13268-158">**UIA \_ контроллерфорпропертид**</span><span class="sxs-lookup"><span data-stu-id="13268-158">**UIA\_ControllerForPropertyId**</span></span>](uiauto-automation-element-propids.md)               | <span data-ttu-id="13268-159">См. примечания.</span><span class="sxs-lookup"><span data-stu-id="13268-159">See notes.</span></span>  | <span data-ttu-id="13268-160">Это свойство может использоваться как указатель на связанную панель вкладки.</span><span class="sxs-lookup"><span data-stu-id="13268-160">This property can be used as pointer to the associated tab pane.</span></span> <span data-ttu-id="13268-161">Это полезно, если невозможно разместить панель как дочерний объект элемента вкладки.</span><span class="sxs-lookup"><span data-stu-id="13268-161">This is useful when it cannot host a pane as child of the tab item object.</span></span> |
| [<span data-ttu-id="13268-162">**UIA \_ контролтипепропертид**</span><span class="sxs-lookup"><span data-stu-id="13268-162">**UIA\_ControlTypePropertyId**</span></span>](uiauto-automation-element-propids.md)                   | <span data-ttu-id="13268-163">**TabItem**</span><span class="sxs-lookup"><span data-stu-id="13268-163">**TabItem**</span></span> | <span data-ttu-id="13268-164">Это значение одинаково для всех инфраструктур пользовательского интерфейса.</span><span class="sxs-lookup"><span data-stu-id="13268-164">This value is the same for all UI frameworks.</span></span>                                                                                               |
| [<span data-ttu-id="13268-165">**UIA \_ исконтентелементпропертид**</span><span class="sxs-lookup"><span data-stu-id="13268-165">**UIA\_IsContentElementPropertyId**</span></span>](uiauto-automation-element-propids.md)         | <span data-ttu-id="13268-166">true</span><span class="sxs-lookup"><span data-stu-id="13268-166">TRUE</span></span>        | <span data-ttu-id="13268-167">Элемент управления "пункт вкладки" всегда включается в представление содержимого дерева модели автоматизации пользовательского интерфейса.</span><span class="sxs-lookup"><span data-stu-id="13268-167">The tab item control is always included in the content view of the UI Automation tree.</span></span>                                                      |
| [<span data-ttu-id="13268-168">**UIA \_ исконтролелементпропертид**</span><span class="sxs-lookup"><span data-stu-id="13268-168">**UIA\_IsControlElementPropertyId**</span></span>](uiauto-automation-element-propids.md)         | <span data-ttu-id="13268-169">true</span><span class="sxs-lookup"><span data-stu-id="13268-169">TRUE</span></span>        | <span data-ttu-id="13268-170">Элемент управления "пункт вкладки" всегда включается в представление элемента управления дерева модели автоматизации пользовательского интерфейса.</span><span class="sxs-lookup"><span data-stu-id="13268-170">The tab item control is always included in the control view of the UI Automation tree.</span></span>                                                      |
| [<span data-ttu-id="13268-171">**UIA \_ искэйбоардфокусаблепропертид**</span><span class="sxs-lookup"><span data-stu-id="13268-171">**UIA\_IsKeyboardFocusablePropertyId**</span></span>](uiauto-automation-element-propids.md)   | <span data-ttu-id="13268-172">См. примечания.</span><span class="sxs-lookup"><span data-stu-id="13268-172">See notes.</span></span>  | <span data-ttu-id="13268-173">Если элемент управления может получать фокус клавиатуры, он должен поддерживать это свойство.</span><span class="sxs-lookup"><span data-stu-id="13268-173">If the control can receive keyboard focus, it must support this property.</span></span>                                                                   |
| [<span data-ttu-id="13268-174">**UIA \_ лабеледбипропертид**</span><span class="sxs-lookup"><span data-stu-id="13268-174">**UIA\_LabeledByPropertyId**</span></span>](uiauto-automation-element-propids.md)                       | <span data-ttu-id="13268-175">NULL</span><span class="sxs-lookup"><span data-stu-id="13268-175">Null</span></span>        | <span data-ttu-id="13268-176">Элементы управления «Элемент вкладки» не имеют меток со статическим текстом.</span><span class="sxs-lookup"><span data-stu-id="13268-176">The tab item control does not have a static text label.</span></span>                                                                                     |
| [<span data-ttu-id="13268-177">**UIA \_ локализедконтролтипепропертид**</span><span class="sxs-lookup"><span data-stu-id="13268-177">**UIA\_LocalizedControlTypePropertyId**</span></span>](uiauto-automation-element-propids.md) | <span data-ttu-id="13268-178">См. примечания.</span><span class="sxs-lookup"><span data-stu-id="13268-178">See notes.</span></span>  | <span data-ttu-id="13268-179">Локализованная строка, соответствующая типу элемента управления **TabItem** .</span><span class="sxs-lookup"><span data-stu-id="13268-179">Localized string corresponding to the **TabItem** control type.</span></span> <span data-ttu-id="13268-180">Значение по умолчанию — "элемент вкладки" для en-US или English (США).</span><span class="sxs-lookup"><span data-stu-id="13268-180">The default value is "tab item" for en-US or English (United States).</span></span>       |
| [<span data-ttu-id="13268-181">**UIA \_ намепропертид**</span><span class="sxs-lookup"><span data-stu-id="13268-181">**UIA\_NamePropertyId**</span></span>](uiauto-automation-element-propids.md)                                 | <span data-ttu-id="13268-182">См. примечания.</span><span class="sxs-lookup"><span data-stu-id="13268-182">See notes.</span></span>  | <span data-ttu-id="13268-183">Элемент управления элемента вкладки с подписью.</span><span class="sxs-lookup"><span data-stu-id="13268-183">The tab item control self-labeled.</span></span>                                                                                                          |



 

## <a name="required-control-patterns"></a><span data-ttu-id="13268-184">Обязательные шаблоны элементов управления</span><span class="sxs-lookup"><span data-stu-id="13268-184">Required Control Patterns</span></span>

<span data-ttu-id="13268-185">В следующей таблице перечислены шаблоны элементов управления модели автоматизации пользовательского интерфейса, которые должны поддерживаться всеми элементами управления "элемент вкладки".</span><span class="sxs-lookup"><span data-stu-id="13268-185">The following table lists the UI Automation control patterns required to be supported by all tab item controls.</span></span> <span data-ttu-id="13268-186">Дополнительные сведения о шаблонах элементов управления см. в разделе [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md).</span><span class="sxs-lookup"><span data-stu-id="13268-186">For more information on control patterns, see [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md).</span></span>



| <span data-ttu-id="13268-187">Шаблон элемента управления</span><span class="sxs-lookup"><span data-stu-id="13268-187">Control Pattern</span></span>                                                 | <span data-ttu-id="13268-188">Поддержка</span><span class="sxs-lookup"><span data-stu-id="13268-188">Support</span></span>  | <span data-ttu-id="13268-189">Примечания</span><span class="sxs-lookup"><span data-stu-id="13268-189">Notes</span></span>                                                                                                                    |
|-----------------------------------------------------------------|----------|--------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="13268-190">**ISelectionItemProvider**</span><span class="sxs-lookup"><span data-stu-id="13268-190">**ISelectionItemProvider**</span></span>](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iselectionitemprovider) | <span data-ttu-id="13268-191">Обязательно</span><span class="sxs-lookup"><span data-stu-id="13268-191">Required</span></span> | <span data-ttu-id="13268-192">Элемент управления "элемент вкладки" должен поддерживать [**иуиаутоматионселектионитемпаттерн**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationselectionitempattern).</span><span class="sxs-lookup"><span data-stu-id="13268-192">The tab item control must support [**IUIAutomationSelectionItemPattern**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationselectionitempattern).</span></span> |
| [<span data-ttu-id="13268-193">**IInvokeProvider**</span><span class="sxs-lookup"><span data-stu-id="13268-193">**IInvokeProvider**</span></span>](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iinvokeprovider)               | <span data-ttu-id="13268-194">Никогда</span><span class="sxs-lookup"><span data-stu-id="13268-194">Never</span></span>    | <span data-ttu-id="13268-195">Элемент управления "элемент вкладки" никогда не поддерживает [**иуиаутоматионинвокепаттерн**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationinvokepattern).</span><span class="sxs-lookup"><span data-stu-id="13268-195">The tab item control never supports [**IUIAutomationInvokePattern**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationinvokepattern).</span></span>             |



 

## <a name="required-events"></a><span data-ttu-id="13268-196">Обязательные события</span><span class="sxs-lookup"><span data-stu-id="13268-196">Required Events</span></span>

<span data-ttu-id="13268-197">В следующей таблице перечислены события автоматизации пользовательского интерфейса, которые необходимы для поддержки элементов управления "элемент вкладки".</span><span class="sxs-lookup"><span data-stu-id="13268-197">The following table lists the UI Automation events that tab item controls are required to support.</span></span> <span data-ttu-id="13268-198">Дополнительные сведения о событиях см. в разделе [UI Automation Events Overview](uiauto-eventsoverview.md).</span><span class="sxs-lookup"><span data-stu-id="13268-198">For more information on events, see [UI Automation Events Overview](uiauto-eventsoverview.md).</span></span>



| <span data-ttu-id="13268-199">Событие автоматизации пользовательского интерфейса</span><span class="sxs-lookup"><span data-stu-id="13268-199">UI Automation Event</span></span>                                                                                                                     | <span data-ttu-id="13268-200">Примечания</span><span class="sxs-lookup"><span data-stu-id="13268-200">Notes</span></span>                                                                                                                      |
|-----------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="13268-201">**UIA \_ аутоматионфокусчанжедевентид**</span><span class="sxs-lookup"><span data-stu-id="13268-201">**UIA\_AutomationFocusChangedEventId**</span></span>](uiauto-event-ids.md)                                        |                                                                                                                            |
| <span data-ttu-id="13268-202">[**UIA \_**](uiauto-automation-element-propids.md) Событие изменения свойства баундингректанглепропертид.</span><span class="sxs-lookup"><span data-stu-id="13268-202">[**UIA\_BoundingRectanglePropertyId**](uiauto-automation-element-propids.md) property-changed event.</span></span>   |                                                                                                                            |
| <span data-ttu-id="13268-203">[**UIA \_**](uiauto-automation-element-propids.md) Событие изменения свойства исенабледпропертид.</span><span class="sxs-lookup"><span data-stu-id="13268-203">[**UIA\_IsEnabledPropertyId**](uiauto-automation-element-propids.md) property-changed event.</span></span>                   | <span data-ttu-id="13268-204">Если элемент управления поддерживает свойство « [**включено**](uiauto-automation-element-propids.md) », оно должно поддерживать это событие.</span><span class="sxs-lookup"><span data-stu-id="13268-204">If the control supports the [**IsEnabled**](uiauto-automation-element-propids.md) property, it must support this event.</span></span>   |
| <span data-ttu-id="13268-205">[**UIA \_**](uiauto-automation-element-propids.md) Событие изменения свойства исоффскринпропертид.</span><span class="sxs-lookup"><span data-stu-id="13268-205">[**UIA\_IsOffscreenPropertyId**](uiauto-automation-element-propids.md) property-changed event.</span></span>               | <span data-ttu-id="13268-206">Если элемент управления поддерживает свойство [**исоффскрин**](uiauto-automation-element-propids.md) , он должен поддерживать это событие.</span><span class="sxs-lookup"><span data-stu-id="13268-206">If the control supports the [**IsOffscreen**](uiauto-automation-element-propids.md) property, it must support this event.</span></span> |
| [<span data-ttu-id="13268-207">**UIA \_ SelectionItem \_ елементремоведфромселектионевентид**</span><span class="sxs-lookup"><span data-stu-id="13268-207">**UIA\_SelectionItem\_ElementRemovedFromSelectionEventId**</span></span>](uiauto-event-ids.md) |                                                                                                                            |
| [<span data-ttu-id="13268-208">**UIA \_ SelectionItem \_ елементселектедевентид**</span><span class="sxs-lookup"><span data-stu-id="13268-208">**UIA\_SelectionItem\_ElementSelectedEventId**</span></span>](uiauto-event-ids.md)                         |                                                                                                                            |
| [<span data-ttu-id="13268-209">**UIA \_ структуречанжедевентид**</span><span class="sxs-lookup"><span data-stu-id="13268-209">**UIA\_StructureChangedEventId**</span></span>](uiauto-event-ids.md)                                                    |                                                                                                                            |



 

## <a name="related-topics"></a><span data-ttu-id="13268-210">См. также</span><span class="sxs-lookup"><span data-stu-id="13268-210">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="13268-211">**Зрения**</span><span class="sxs-lookup"><span data-stu-id="13268-211">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="13268-212">Общие сведения о типах элементов управления автоматизации пользовательского интерфейса</span><span class="sxs-lookup"><span data-stu-id="13268-212">UI Automation Control Types Overview</span></span>](uiauto-controltypesoverview.md)
</dt> <dt>

[<span data-ttu-id="13268-213">Общие сведения о модели автоматизации пользовательского интерфейса</span><span class="sxs-lookup"><span data-stu-id="13268-213">UI Automation Overview</span></span>](uiauto-uiautomationoverview.md)
</dt> </dl>

 

 




