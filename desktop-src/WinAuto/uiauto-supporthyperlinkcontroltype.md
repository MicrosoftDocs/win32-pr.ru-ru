---
title: Тип элемента управления HyperLink
description: В этом разделе содержатся сведения о поддержке автоматизации пользовательского интерфейса Майкрософт для типа элемента управления HyperLink.
ms.assetid: 6dd16ae6-eff0-4913-8916-5092aec34f1f
keywords:
- Модель автоматизации пользовательского интерфейса, поддержка типа элемента управления HyperLink
- Модель автоматизации пользовательского интерфейса, тип элемента управления HyperLink
- Модель автоматизации пользовательского интерфейса, древовидная структура для типа элемента управления HyperLink
- Модель автоматизации пользовательского интерфейса, свойства для типа элемента управления HyperLink
- Модель автоматизации пользовательского интерфейса, шаблоны элементов управления для типа элемента управления HyperLink
- Модель автоматизации пользовательского интерфейса, события для типа элемента управления HyperLink
- Древовидные структуры, тип элемента управления HyperLink
- свойства, тип элемента управления HyperLink
- шаблоны элементов управления, тип элемента управления HyperLink
- события, тип элемента управления HyperLink
- Поддержка типа элемента управления HyperLink
- Hyperlink - тип элемента управления
- типы элементов управления, древовидная структура для типа элемента управления HyperLink
- типы элементов управления, шаблоны элементов управления для типа элемента управления HyperLink
- типы элементов управления, поддержка гиперссылок
- типы элементов управления, гиперссылка
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 71547f37380aeb029e4f73f8d9b2286b285187ff
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103775848"
---
# <a name="hyperlink-control-type"></a><span data-ttu-id="14d0b-119">Тип элемента управления HyperLink</span><span class="sxs-lookup"><span data-stu-id="14d0b-119">Hyperlink Control Type</span></span>

<span data-ttu-id="14d0b-120">В этом разделе содержатся сведения о поддержке автоматизации пользовательского интерфейса Майкрософт для типа элемента управления **Hyperlink** .</span><span class="sxs-lookup"><span data-stu-id="14d0b-120">This topic provides information about Microsoft UI Automation support for the **Hyperlink** control type.</span></span>

<span data-ttu-id="14d0b-121">Элементы управления HyperLink создают ссылки, позволяющие пользователям переходить с одной страницы на другую.</span><span class="sxs-lookup"><span data-stu-id="14d0b-121">Hyperlink controls create links that enable users to navigate within the same page, or from one page to another.</span></span>

<span data-ttu-id="14d0b-122">В следующих разделах определяется необходимая древовидная структура модели автоматизации пользовательского интерфейса, свойства, шаблоны элементов управления и события для типа элемента управления **Hyperlink** .</span><span class="sxs-lookup"><span data-stu-id="14d0b-122">The following sections define the required UI Automation tree structure, properties, control patterns, and events for the **Hyperlink** control type.</span></span> <span data-ttu-id="14d0b-123">Требования к автоматизации пользовательского интерфейса применяются ко всем элементам управления HyperLink, в которых платформа или платформа пользовательского интерфейса интегрирует поддержку модели автоматизации пользовательского интерфейса для типов элементов управления и шаблонов элементов управления.</span><span class="sxs-lookup"><span data-stu-id="14d0b-123">The UI Automation requirements apply to all hyperlink controls where the UI framework/platform integrates UI Automation support for control types and control patterns.</span></span>

<span data-ttu-id="14d0b-124">В этом разделе содержатся следующие подразделы.</span><span class="sxs-lookup"><span data-stu-id="14d0b-124">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="14d0b-125">Типичная древовидная структура</span><span class="sxs-lookup"><span data-stu-id="14d0b-125">Typical Tree Structure</span></span>](#typical-tree-structure)
-   [<span data-ttu-id="14d0b-126">Соответствующие свойства</span><span class="sxs-lookup"><span data-stu-id="14d0b-126">Relevant Properties</span></span>](#relevant-properties)
-   [<span data-ttu-id="14d0b-127">Обязательные шаблоны элементов управления</span><span class="sxs-lookup"><span data-stu-id="14d0b-127">Required Control Patterns</span></span>](#required-control-patterns)
-   [<span data-ttu-id="14d0b-128">Обязательные события</span><span class="sxs-lookup"><span data-stu-id="14d0b-128">Required Events</span></span>](#required-events)
-   [<span data-ttu-id="14d0b-129">Замечания</span><span class="sxs-lookup"><span data-stu-id="14d0b-129">Remarks</span></span>](#remarks)
-   [<span data-ttu-id="14d0b-130">См. также</span><span class="sxs-lookup"><span data-stu-id="14d0b-130">Related topics</span></span>](#related-topics)

## <a name="typical-tree-structure"></a><span data-ttu-id="14d0b-131">Типичная древовидная структура</span><span class="sxs-lookup"><span data-stu-id="14d0b-131">Typical Tree Structure</span></span>

<span data-ttu-id="14d0b-132">В следующей таблице описывается типичный элемент управления и представление содержимого дерева модели автоматизации пользовательского интерфейса, которое относится к элементам управления HyperLink и описывает, что может содержаться в каждом представлении.</span><span class="sxs-lookup"><span data-stu-id="14d0b-132">The following table depicts a typical control and content view of the UI Automation tree that pertains to hyperlink controls and describes what can be contained in each view.</span></span> <span data-ttu-id="14d0b-133">Дополнительные сведения о дереве автоматизации пользовательского интерфейса см. в разделе [Общие сведения о дереве модели автоматизации пользовательского интерфейса](uiauto-treeoverview.md).</span><span class="sxs-lookup"><span data-stu-id="14d0b-133">For more information about the UI Automation tree, see [UI Automation Tree Overview](uiauto-treeoverview.md).</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="14d0b-134">Представление элемента управления</span><span class="sxs-lookup"><span data-stu-id="14d0b-134">Control View</span></span></th>
<th><span data-ttu-id="14d0b-135">Представление содержимого</span><span class="sxs-lookup"><span data-stu-id="14d0b-135">Content View</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><ul>
<li><span data-ttu-id="14d0b-136">Гиперссылка</span><span class="sxs-lookup"><span data-stu-id="14d0b-136">Hyperlink</span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="14d0b-137">Гиперссылка</span><span class="sxs-lookup"><span data-stu-id="14d0b-137">Hyperlink</span></span></li>
</ul></td>
</tr>
</tbody>
</table>



 

## <a name="relevant-properties"></a><span data-ttu-id="14d0b-138">Соответствующие свойства</span><span class="sxs-lookup"><span data-stu-id="14d0b-138">Relevant Properties</span></span>

<span data-ttu-id="14d0b-139">В следующей таблице перечислены свойства модели автоматизации пользовательского интерфейса, значения или определения которых особенно важны для элементов управления HyperLink.</span><span class="sxs-lookup"><span data-stu-id="14d0b-139">The following table lists the UI Automation properties whose value or definition is especially relevant to the hyperlink controls.</span></span> <span data-ttu-id="14d0b-140">Дополнительные сведения о свойствах модели автоматизации пользовательского интерфейса см. в разделе [Получение свойств элементов модели автоматизации пользовательского интерфейса](uiauto-propertiesforclients.md).</span><span class="sxs-lookup"><span data-stu-id="14d0b-140">For more information about UI Automation properties, see [Retrieving Properties from UI Automation Elements](uiauto-propertiesforclients.md).</span></span>



| <span data-ttu-id="14d0b-141">Свойство модели автоматизации пользовательского интерфейса</span><span class="sxs-lookup"><span data-stu-id="14d0b-141">UI Automation Property</span></span>                                                                                              | <span data-ttu-id="14d0b-142">Значение</span><span class="sxs-lookup"><span data-stu-id="14d0b-142">Value</span></span>         | <span data-ttu-id="14d0b-143">Примечания</span><span class="sxs-lookup"><span data-stu-id="14d0b-143">Notes</span></span>                                                                                                                                    |
|---------------------------------------------------------------------------------------------------------------------|---------------|------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="14d0b-144">**UIA \_ аутоматионидпропертид**</span><span class="sxs-lookup"><span data-stu-id="14d0b-144">**UIA\_AutomationIdPropertyId**</span></span>](uiauto-automation-element-propids.md)                 | <span data-ttu-id="14d0b-145">См. примечания.</span><span class="sxs-lookup"><span data-stu-id="14d0b-145">See notes.</span></span>    | <span data-ttu-id="14d0b-146">Значение этого свойства должно быть уникальным для всех элементов управления в приложении.</span><span class="sxs-lookup"><span data-stu-id="14d0b-146">The value of this property must be unique across all controls in an application.</span></span>                                                         |
| [<span data-ttu-id="14d0b-147">**UIA \_ баундингректанглепропертид**</span><span class="sxs-lookup"><span data-stu-id="14d0b-147">**UIA\_BoundingRectanglePropertyId**</span></span>](uiauto-automation-element-propids.md)       | <span data-ttu-id="14d0b-148">См. примечания.</span><span class="sxs-lookup"><span data-stu-id="14d0b-148">See notes.</span></span>    | <span data-ttu-id="14d0b-149">Внешний прямоугольник, содержащий весь элемент управления.</span><span class="sxs-lookup"><span data-stu-id="14d0b-149">The outermost rectangle that contains the whole control.</span></span>                                                                                 |
| [<span data-ttu-id="14d0b-150">**UIA \_ кликкаблепоинтпропертид**</span><span class="sxs-lookup"><span data-stu-id="14d0b-150">**UIA\_ClickablePointPropertyId**</span></span>](uiauto-automation-element-propids.md)             | <span data-ttu-id="14d0b-151">См. примечания.</span><span class="sxs-lookup"><span data-stu-id="14d0b-151">See notes.</span></span>    | <span data-ttu-id="14d0b-152">Точка щелчка элемента управления HyperLink должна быть точкой, запускающей гиперссылку, если она была нажата с помощью указателя мыши.</span><span class="sxs-lookup"><span data-stu-id="14d0b-152">The hyperlink control's clickable point must be a point that launches the hyperlink if clicked with a mouse pointer.</span></span>                     |
| [<span data-ttu-id="14d0b-153">**UIA \_ контролтипепропертид**</span><span class="sxs-lookup"><span data-stu-id="14d0b-153">**UIA\_ControlTypePropertyId**</span></span>](uiauto-automation-element-propids.md)                   | <span data-ttu-id="14d0b-154">**Гиперссылка**</span><span class="sxs-lookup"><span data-stu-id="14d0b-154">**Hyperlink**</span></span> |                                                                                                                                          |
| [<span data-ttu-id="14d0b-155">**UIA \_ исконтентелементпропертид**</span><span class="sxs-lookup"><span data-stu-id="14d0b-155">**UIA\_IsContentElementPropertyId**</span></span>](uiauto-automation-element-propids.md)         | <span data-ttu-id="14d0b-156">true</span><span class="sxs-lookup"><span data-stu-id="14d0b-156">TRUE</span></span>          | <span data-ttu-id="14d0b-157">Элемент управления Hyperlink всегда включается в представление содержимого дерева модели автоматизации пользовательского интерфейса.</span><span class="sxs-lookup"><span data-stu-id="14d0b-157">The hyperlink control is always included in the content view of the UI Automation tree.</span></span>                                                  |
| [<span data-ttu-id="14d0b-158">**UIA \_ исконтролелементпропертид**</span><span class="sxs-lookup"><span data-stu-id="14d0b-158">**UIA\_IsControlElementPropertyId**</span></span>](uiauto-automation-element-propids.md)         | <span data-ttu-id="14d0b-159">true</span><span class="sxs-lookup"><span data-stu-id="14d0b-159">TRUE</span></span>          | <span data-ttu-id="14d0b-160">Элемент управления Hyperlink всегда включается в представление элемента управления дерева модели автоматизации пользовательского интерфейса.</span><span class="sxs-lookup"><span data-stu-id="14d0b-160">The hyperlink control is always included in the control view of the UI Automation tree.</span></span>                                                  |
| [<span data-ttu-id="14d0b-161">**UIA \_ искэйбоардфокусаблепропертид**</span><span class="sxs-lookup"><span data-stu-id="14d0b-161">**UIA\_IsKeyboardFocusablePropertyId**</span></span>](uiauto-automation-element-propids.md)   | <span data-ttu-id="14d0b-162">См. примечания.</span><span class="sxs-lookup"><span data-stu-id="14d0b-162">See notes.</span></span>    | <span data-ttu-id="14d0b-163">Если элемент управления может получать фокус клавиатуры, он должен поддерживать это свойство.</span><span class="sxs-lookup"><span data-stu-id="14d0b-163">If the control can receive keyboard focus, it must support this property.</span></span>                                                                |
| [<span data-ttu-id="14d0b-164">**UIA \_ лабеледбипропертид**</span><span class="sxs-lookup"><span data-stu-id="14d0b-164">**UIA\_LabeledByPropertyId**</span></span>](uiauto-automation-element-propids.md)                       | <span data-ttu-id="14d0b-165">См. примечания.</span><span class="sxs-lookup"><span data-stu-id="14d0b-165">See notes.</span></span>    | <span data-ttu-id="14d0b-166">Если имеется статическая текстовая метка, это свойство должно предоставлять ссылку на этот элемент управления.</span><span class="sxs-lookup"><span data-stu-id="14d0b-166">If there is a static text label, this property must expose a reference to that control.</span></span>                                                  |
| [<span data-ttu-id="14d0b-167">**UIA \_ локализедконтролтипепропертид**</span><span class="sxs-lookup"><span data-stu-id="14d0b-167">**UIA\_LocalizedControlTypePropertyId**</span></span>](uiauto-automation-element-propids.md) | <span data-ttu-id="14d0b-168">См. примечания.</span><span class="sxs-lookup"><span data-stu-id="14d0b-168">See notes.</span></span>    | <span data-ttu-id="14d0b-169">Локализованная строка, соответствующая типу элемента управления **Hyperlink** .</span><span class="sxs-lookup"><span data-stu-id="14d0b-169">Localized string corresponding to the **Hyperlink** control type.</span></span> <span data-ttu-id="14d0b-170">Значение по умолчанию — "Hyperlink" для en-US или English (США).</span><span class="sxs-lookup"><span data-stu-id="14d0b-170">The default value is "hyperlink" for en-US or English (United States).</span></span> |
| [<span data-ttu-id="14d0b-171">**UIA \_ намепропертид**</span><span class="sxs-lookup"><span data-stu-id="14d0b-171">**UIA\_NamePropertyId**</span></span>](uiauto-automation-element-propids.md)                                 | <span data-ttu-id="14d0b-172">См. примечания.</span><span class="sxs-lookup"><span data-stu-id="14d0b-172">See notes.</span></span>    | <span data-ttu-id="14d0b-173">Имя элемента управления HyperLink — это текст, отображаемый на экране как подчеркнутый.</span><span class="sxs-lookup"><span data-stu-id="14d0b-173">The hyperlink control's name is the text that is displayed on the screen as underlined.</span></span>                                                  |



 

## <a name="required-control-patterns"></a><span data-ttu-id="14d0b-174">Обязательные шаблоны элементов управления</span><span class="sxs-lookup"><span data-stu-id="14d0b-174">Required Control Patterns</span></span>

<span data-ttu-id="14d0b-175">В следующей таблице перечислены шаблоны элементов управления модели автоматизации пользовательского интерфейса, которые требуются для поддержки элементов управления HyperLink.</span><span class="sxs-lookup"><span data-stu-id="14d0b-175">The following table lists the UI Automation control patterns that hyperlink controls are required to support.</span></span> <span data-ttu-id="14d0b-176">Дополнительные сведения о шаблонах элементов управления см. в разделе [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md).</span><span class="sxs-lookup"><span data-stu-id="14d0b-176">For more information on control patterns, see [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md).</span></span>



| <span data-ttu-id="14d0b-177">Шаблон элемента управления/свойство шаблона</span><span class="sxs-lookup"><span data-stu-id="14d0b-177">Control Pattern/Pattern Property</span></span>                  | <span data-ttu-id="14d0b-178">Поддержка/значение</span><span class="sxs-lookup"><span data-stu-id="14d0b-178">Support/Value</span></span>                | <span data-ttu-id="14d0b-179">Примечания</span><span class="sxs-lookup"><span data-stu-id="14d0b-179">Notes</span></span>                                                                                                                                                                                                                                                  |
|---------------------------------------------------|------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="14d0b-180">**IInvokeProvider**</span><span class="sxs-lookup"><span data-stu-id="14d0b-180">**IInvokeProvider**</span></span>](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iinvokeprovider) | <span data-ttu-id="14d0b-181">Обязательно</span><span class="sxs-lookup"><span data-stu-id="14d0b-181">Required</span></span>                     | <span data-ttu-id="14d0b-182">Все элементы управления Hyperlink должны поддерживать шаблон элемента управления [Invoke](uiauto-implementinginvoke.md) .</span><span class="sxs-lookup"><span data-stu-id="14d0b-182">All hyperlink controls must support the [Invoke](uiauto-implementinginvoke.md) control pattern.</span></span>                                                                                                                                                       |
| [<span data-ttu-id="14d0b-183">**IValueProvider**</span><span class="sxs-lookup"><span data-stu-id="14d0b-183">**IValueProvider**</span></span>](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-ivalueprovider)   | <span data-ttu-id="14d0b-184">Зависит</span><span class="sxs-lookup"><span data-stu-id="14d0b-184">Depends</span></span>                      | <span data-ttu-id="14d0b-185">Элементы управления Hyperlink должны поддерживать шаблон элемента управления [value](uiauto-implementingvalue.md) , если ссылка содержит сведения, которые могут быть использованы и понятны пользователю.</span><span class="sxs-lookup"><span data-stu-id="14d0b-185">Hyperlink controls should support the [Value](uiauto-implementingvalue.md) control pattern when the link contains information that is usable and meaningful to the user.</span></span>                                                                              |
| [<span data-ttu-id="14d0b-186">**Значение**</span><span class="sxs-lookup"><span data-stu-id="14d0b-186">**Value**</span></span>](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-ivalueprovider-get_value)      | <span data-ttu-id="14d0b-187">Например, https://www...</span><span class="sxs-lookup"><span data-stu-id="14d0b-187">For example, "https://www..."</span></span> | <span data-ttu-id="14d0b-188">URL-адрес для адреса в Интернете или интрасети является примером гиперссылки, содержащей сведения, имеющие смысл для пользователя.</span><span class="sxs-lookup"><span data-stu-id="14d0b-188">A URL for an Internet or intranet address is an example of a hyperlink that contains information that is meaningful to the user.</span></span> <span data-ttu-id="14d0b-189">Однако программная ссылка имеет смысл только для приложения и не рекомендуется для свойства **value** .</span><span class="sxs-lookup"><span data-stu-id="14d0b-189">A programmatic link, however, is meaningful only to an application and is not recommended for the **Value** property.</span></span> |



 

## <a name="required-events"></a><span data-ttu-id="14d0b-190">Обязательные события</span><span class="sxs-lookup"><span data-stu-id="14d0b-190">Required Events</span></span>

<span data-ttu-id="14d0b-191">В следующей таблице перечислены события автоматизации пользовательского интерфейса, которые должны поддерживать элементы управления HyperLink.</span><span class="sxs-lookup"><span data-stu-id="14d0b-191">The following table lists the UI Automation events that hyperlink controls are required to support.</span></span> <span data-ttu-id="14d0b-192">Дополнительные сведения о событиях см. в разделе [UI Automation Events Overview](uiauto-eventsoverview.md).</span><span class="sxs-lookup"><span data-stu-id="14d0b-192">For more information on events, see [UI Automation Events Overview](uiauto-eventsoverview.md).</span></span>



| <span data-ttu-id="14d0b-193">Событие автоматизации пользовательского интерфейса</span><span class="sxs-lookup"><span data-stu-id="14d0b-193">UI Automation Event</span></span>                                                                                                                   | <span data-ttu-id="14d0b-194">Примечания</span><span class="sxs-lookup"><span data-stu-id="14d0b-194">Notes</span></span>                                                                                                                      |
|---------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="14d0b-195">**UIA \_ аутоматионфокусчанжедевентид**</span><span class="sxs-lookup"><span data-stu-id="14d0b-195">**UIA\_AutomationFocusChangedEventId**</span></span>](uiauto-event-ids.md)                                      |                                                                                                                            |
| <span data-ttu-id="14d0b-196">[**UIA \_**](uiauto-automation-element-propids.md) Событие изменения свойства баундингректанглепропертид.</span><span class="sxs-lookup"><span data-stu-id="14d0b-196">[**UIA\_BoundingRectanglePropertyId**](uiauto-automation-element-propids.md) property-changed event.</span></span> |                                                                                                                            |
| [<span data-ttu-id="14d0b-197">**UIA \_ Invoke \_ инвокедевентид**</span><span class="sxs-lookup"><span data-stu-id="14d0b-197">**UIA\_Invoke\_InvokedEventId**</span></span>](uiauto-event-ids.md)                                                     |                                                                                                                            |
| <span data-ttu-id="14d0b-198">[**UIA \_**](uiauto-automation-element-propids.md) Событие изменения свойства исенабледпропертид.</span><span class="sxs-lookup"><span data-stu-id="14d0b-198">[**UIA\_IsEnabledPropertyId**](uiauto-automation-element-propids.md) property-changed event.</span></span>                 | <span data-ttu-id="14d0b-199">Если элемент управления поддерживает свойство « [**включено**](uiauto-automation-element-propids.md) », оно должно поддерживать это событие.</span><span class="sxs-lookup"><span data-stu-id="14d0b-199">If the control supports the [**IsEnabled**](uiauto-automation-element-propids.md) property, it must support this event.</span></span>   |
| <span data-ttu-id="14d0b-200">[**UIA \_**](uiauto-automation-element-propids.md) Событие изменения свойства исоффскринпропертид.</span><span class="sxs-lookup"><span data-stu-id="14d0b-200">[**UIA\_IsOffscreenPropertyId**](uiauto-automation-element-propids.md) property-changed event.</span></span>             | <span data-ttu-id="14d0b-201">Если элемент управления поддерживает свойство [**исоффскрин**](uiauto-automation-element-propids.md) , он должен поддерживать это событие.</span><span class="sxs-lookup"><span data-stu-id="14d0b-201">If the control supports the [**IsOffscreen**](uiauto-automation-element-propids.md) property, it must support this event.</span></span> |
| [<span data-ttu-id="14d0b-202">**UIA \_ структуречанжедевентид**</span><span class="sxs-lookup"><span data-stu-id="14d0b-202">**UIA\_StructureChangedEventId**</span></span>](uiauto-event-ids.md)                                                  |                                                                                                                            |



 

## <a name="remarks"></a><span data-ttu-id="14d0b-203">Комментарии</span><span class="sxs-lookup"><span data-stu-id="14d0b-203">Remarks</span></span>

<span data-ttu-id="14d0b-204">Тип элемента управления HyperLink должен применяться только к объекту, при щелчке которого происходит переход. его не следует применять к контейнеру гиперссылки.</span><span class="sxs-lookup"><span data-stu-id="14d0b-204">The Hyperlink control type should be applied only to an object that, when clicked, causes navigation to occur; it should not be applied to the container of the hyperlink.</span></span> <span data-ttu-id="14d0b-205">Например, только активные зоны, которые могут быть активными, внутри гиперкарты должны иметь тип элемента управления **Hyperlink** .</span><span class="sxs-lookup"><span data-stu-id="14d0b-205">For example, only the clickable "hot spots" inside an image map should have the **Hyperlink** control type.</span></span> <span data-ttu-id="14d0b-206">То же самое касается гиперссылок в текстовом поле или контейнере документа.</span><span class="sxs-lookup"><span data-stu-id="14d0b-206">The same is true of hyperlinks in a text field or document container.</span></span> <span data-ttu-id="14d0b-207">В этом случае только текст или изображение гиперссылки должны иметь тип элемента управления **Hyperlink** , а не контейнер.</span><span class="sxs-lookup"><span data-stu-id="14d0b-207">In this case, only the hyperlink text or image should have the **Hyperlink** control type, not the container.</span></span>

<span data-ttu-id="14d0b-208">Шаблон элемента управления [Text](uiauto-implementingtextandtextrange.md) идеально подходит для поддержки внедренных гиперссылок в тексте или элементах документа.</span><span class="sxs-lookup"><span data-stu-id="14d0b-208">The [Text](uiauto-implementingtextandtextrange.md) control pattern is ideal for supporting embedded hyperlinks in text or document elements.</span></span>

## <a name="related-topics"></a><span data-ttu-id="14d0b-209">См. также</span><span class="sxs-lookup"><span data-stu-id="14d0b-209">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="14d0b-210">**Зрения**</span><span class="sxs-lookup"><span data-stu-id="14d0b-210">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="14d0b-211">Общие сведения о типах элементов управления автоматизации пользовательского интерфейса</span><span class="sxs-lookup"><span data-stu-id="14d0b-211">UI Automation Control Types Overview</span></span>](uiauto-controltypesoverview.md)
</dt> <dt>

[<span data-ttu-id="14d0b-212">Общие сведения о модели автоматизации пользовательского интерфейса</span><span class="sxs-lookup"><span data-stu-id="14d0b-212">UI Automation Overview</span></span>](uiauto-uiautomationoverview.md)
</dt> </dl>

 

 




