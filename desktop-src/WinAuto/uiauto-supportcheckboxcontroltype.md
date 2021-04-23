---
title: Тип элемента управления CheckBox
description: В этом разделе содержатся сведения о поддержке автоматизации пользовательского интерфейса Майкрософт для типа элемента управления CheckBox.
ms.assetid: 5a9061bc-2eac-4839-8f2c-32b9d58fe712
keywords:
- Модель автоматизации пользовательского интерфейса, поддержка типа элемента управления CheckBox
- Модель автоматизации пользовательского интерфейса, тип элемента управления CheckBox
- Модель автоматизации пользовательского интерфейса, древовидная структура для типа элемента управления CheckBox
- Модель автоматизации пользовательского интерфейса, свойства для типа элемента управления CheckBox
- Модель автоматизации пользовательского интерфейса, шаблоны элементов управления для типа элемента управления CheckBox
- Модель автоматизации пользовательского интерфейса, события для типа элемента управления CheckBox
- Древовидные структуры, тип элемента управления CheckBox
- свойства, тип элемента управления CheckBox
- шаблоны элементов управления, тип элемента управления CheckBox
- события, тип элемента управления CheckBox
- Поддержка типа элемента управления CheckBox
- CheckBox - тип элемента управления
- типы элементов управления, древовидная структура для типа элемента управления CheckBox
- типы элементов управления, шаблоны элементов управления для типа элемента управления CheckBox
- типы элементов управления, поддержка CheckBox
- типы элементов управления, флажок
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d8e5bac106c8ba3bbf58c7f5b06c087ceb7b3418
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103888320"
---
# <a name="checkbox-control-type"></a><span data-ttu-id="9e414-119">Тип элемента управления CheckBox</span><span class="sxs-lookup"><span data-stu-id="9e414-119">CheckBox Control Type</span></span>

<span data-ttu-id="9e414-120">В этом разделе содержатся сведения о поддержке автоматизации пользовательского интерфейса Майкрософт для типа элемента управления **CheckBox** .</span><span class="sxs-lookup"><span data-stu-id="9e414-120">This topic provides information about Microsoft UI Automation support for the **CheckBox** control type.</span></span>

<span data-ttu-id="9e414-121">Флажок — это объект, используемый для указания состояния, с которым пользователи могут взаимодействовать для циклического перебора этого состояния.</span><span class="sxs-lookup"><span data-stu-id="9e414-121">A check box is an object used to indicate a state that users can interact with to cycle through that state.</span></span> <span data-ttu-id="9e414-122">Флажки представляют пользователю выбор из двух (да/нет, вкл./выкл.) или трех (вкл., выкл., не определено) вариантов.</span><span class="sxs-lookup"><span data-stu-id="9e414-122">Check boxes either present a binary (Yes/No), (On/Off), or tertiary (On, Off, Indeterminate) option to the user.</span></span>

<span data-ttu-id="9e414-123">В следующих разделах определяется необходимая древовидная структура модели автоматизации пользовательского интерфейса, свойства, шаблоны элементов управления и события для типа элемента управления **CheckBox** .</span><span class="sxs-lookup"><span data-stu-id="9e414-123">The following sections define the required UI Automation tree structure, properties, control patterns, and events for the **CheckBox** control type.</span></span> <span data-ttu-id="9e414-124">Требования к автоматизации пользовательского интерфейса применяются ко всем элементам управления "флажок", в которых платформа или платформа пользовательского интерфейса интегрирует поддержку автоматизации пользовательского интерфейса для типов элементов управления и шаблонов элементов управления.</span><span class="sxs-lookup"><span data-stu-id="9e414-124">The UI Automation requirements apply to all check box controls where the UI framework/platform integrates UI Automation support for control types and control patterns.</span></span>

<span data-ttu-id="9e414-125">В этом разделе содержатся следующие подразделы.</span><span class="sxs-lookup"><span data-stu-id="9e414-125">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="9e414-126">Типичная древовидная структура</span><span class="sxs-lookup"><span data-stu-id="9e414-126">Typical Tree Structure</span></span>](#typical-tree-structure)
-   [<span data-ttu-id="9e414-127">Соответствующие свойства</span><span class="sxs-lookup"><span data-stu-id="9e414-127">Relevant Properties</span></span>](#relevant-properties)
-   [<span data-ttu-id="9e414-128">Обязательные шаблоны элементов управления</span><span class="sxs-lookup"><span data-stu-id="9e414-128">Required Control Patterns</span></span>](#required-control-patterns)
-   [<span data-ttu-id="9e414-129">Обязательные события</span><span class="sxs-lookup"><span data-stu-id="9e414-129">Required Events</span></span>](#required-events)
-   [<span data-ttu-id="9e414-130">DefaultAction</span><span class="sxs-lookup"><span data-stu-id="9e414-130">DefaultAction</span></span>](#defaultaction)
-   [<span data-ttu-id="9e414-131">См. также</span><span class="sxs-lookup"><span data-stu-id="9e414-131">Related topics</span></span>](#related-topics)

## <a name="typical-tree-structure"></a><span data-ttu-id="9e414-132">Типичная древовидная структура</span><span class="sxs-lookup"><span data-stu-id="9e414-132">Typical Tree Structure</span></span>

<span data-ttu-id="9e414-133">В следующей таблице описывается типичный элемент управления и представление содержимого дерева модели автоматизации пользовательского интерфейса, которое относится к элементам управления "флажок" и описывает, что может содержаться в каждом представлении.</span><span class="sxs-lookup"><span data-stu-id="9e414-133">The following table depicts a typical control and content view of the UI Automation tree that pertains to check box controls and describes what can be contained in each view.</span></span> <span data-ttu-id="9e414-134">Дополнительные сведения о дереве автоматизации пользовательского интерфейса см. в разделе [Общие сведения о дереве модели автоматизации пользовательского интерфейса](uiauto-treeoverview.md).</span><span class="sxs-lookup"><span data-stu-id="9e414-134">For more information about the UI Automation tree, see [UI Automation Tree Overview](uiauto-treeoverview.md).</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="9e414-135">Представление элемента управления</span><span class="sxs-lookup"><span data-stu-id="9e414-135">Control View</span></span></th>
<th><span data-ttu-id="9e414-136">Представление содержимого</span><span class="sxs-lookup"><span data-stu-id="9e414-136">Content View</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><ul>
<li><span data-ttu-id="9e414-137">CheckBox</span><span class="sxs-lookup"><span data-stu-id="9e414-137">CheckBox</span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="9e414-138">CheckBox</span><span class="sxs-lookup"><span data-stu-id="9e414-138">CheckBox</span></span></li>
</ul></td>
</tr>
</tbody>
</table>



 

## <a name="relevant-properties"></a><span data-ttu-id="9e414-139">Соответствующие свойства</span><span class="sxs-lookup"><span data-stu-id="9e414-139">Relevant Properties</span></span>

<span data-ttu-id="9e414-140">В следующей таблице перечислены свойства модели автоматизации пользовательского интерфейса, значения или определения которых особенно важны для типа элемента управления **CheckBox** .</span><span class="sxs-lookup"><span data-stu-id="9e414-140">The following table lists the UI Automation properties whose value or definition is especially relevant to the **CheckBox** control type.</span></span> <span data-ttu-id="9e414-141">Дополнительные сведения о свойствах модели автоматизации пользовательского интерфейса см. в разделе [Получение свойств элементов модели автоматизации пользовательского интерфейса](uiauto-propertiesforclients.md).</span><span class="sxs-lookup"><span data-stu-id="9e414-141">For more information about UI Automation properties, see [Retrieving Properties from UI Automation Elements](uiauto-propertiesforclients.md).</span></span>



| <span data-ttu-id="9e414-142">Свойство модели автоматизации пользовательского интерфейса</span><span class="sxs-lookup"><span data-stu-id="9e414-142">UI Automation Property</span></span>                                                                                              | <span data-ttu-id="9e414-143">Значение</span><span class="sxs-lookup"><span data-stu-id="9e414-143">Value</span></span>        | <span data-ttu-id="9e414-144">Примечания</span><span class="sxs-lookup"><span data-stu-id="9e414-144">Notes</span></span>                                                                                                                                                                                                                                                                              |
|---------------------------------------------------------------------------------------------------------------------|--------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="9e414-145">**UIA \_ аутоматионидпропертид**</span><span class="sxs-lookup"><span data-stu-id="9e414-145">**UIA\_AutomationIdPropertyId**</span></span>](uiauto-automation-element-propids.md)                 | <span data-ttu-id="9e414-146">См. примечания.</span><span class="sxs-lookup"><span data-stu-id="9e414-146">See notes.</span></span>   | <span data-ttu-id="9e414-147">Значение этого свойства должно быть уникальным среди всех одноранговых элементов в необработанном представлении дерева модели автоматизации пользовательского интерфейса.</span><span class="sxs-lookup"><span data-stu-id="9e414-147">The value of this property must be unique among all peer elements in the raw view of the UI Automation tree.</span></span>                                                                                                                                                                       |
| [<span data-ttu-id="9e414-148">**UIA \_ баундингректанглепропертид**</span><span class="sxs-lookup"><span data-stu-id="9e414-148">**UIA\_BoundingRectanglePropertyId**</span></span>](uiauto-automation-element-propids.md)       | <span data-ttu-id="9e414-149">См. примечания.</span><span class="sxs-lookup"><span data-stu-id="9e414-149">See notes.</span></span>   | <span data-ttu-id="9e414-150">Внешний прямоугольник, содержащий весь элемент управления.</span><span class="sxs-lookup"><span data-stu-id="9e414-150">The outermost rectangle that contains the whole control.</span></span>                                                                                                                                                                                                                           |
| [<span data-ttu-id="9e414-151">**UIA \_ кликкаблепоинтпропертид**</span><span class="sxs-lookup"><span data-stu-id="9e414-151">**UIA\_ClickablePointPropertyId**</span></span>](uiauto-automation-element-propids.md)             | <span data-ttu-id="9e414-152">См. примечания.</span><span class="sxs-lookup"><span data-stu-id="9e414-152">See notes.</span></span>   | <span data-ttu-id="9e414-153">Поддерживается при наличии ограничивающего прямоугольника.</span><span class="sxs-lookup"><span data-stu-id="9e414-153">Supported if there is a bounding rectangle.</span></span> <span data-ttu-id="9e414-154">Если не все точки внутри ограничивающего прямоугольника являются щелчками, а элемент выполняет специализированное тестирование нажатия, переопределите и предоставьте точку для щелчка.</span><span class="sxs-lookup"><span data-stu-id="9e414-154">If not every point within the bounding rectangle is clickable, and the element performs specialized hit testing, override and provide a clickable point.</span></span>                                                                               |
| [<span data-ttu-id="9e414-155">**UIA \_ контролтипепропертид**</span><span class="sxs-lookup"><span data-stu-id="9e414-155">**UIA\_ControlTypePropertyId**</span></span>](uiauto-automation-element-propids.md)                   | <span data-ttu-id="9e414-156">**CheckBox**</span><span class="sxs-lookup"><span data-stu-id="9e414-156">**CheckBox**</span></span> |                                                                                                                                                                                                                                                                                    |
| [<span data-ttu-id="9e414-157">**UIA \_ исконтентелементпропертид**</span><span class="sxs-lookup"><span data-stu-id="9e414-157">**UIA\_IsContentElementPropertyId**</span></span>](uiauto-automation-element-propids.md)         | <span data-ttu-id="9e414-158">true</span><span class="sxs-lookup"><span data-stu-id="9e414-158">TRUE</span></span>         | <span data-ttu-id="9e414-159">Значение этого свойства всегда должно быть **true**.</span><span class="sxs-lookup"><span data-stu-id="9e414-159">The value of this property must always be **TRUE**.</span></span> <span data-ttu-id="9e414-160">Это означает, что элемент управления "флажок" всегда должен включаться в представление содержимого дерева модели автоматизации пользовательского интерфейса.</span><span class="sxs-lookup"><span data-stu-id="9e414-160">This means that the check box control must always be included in the content view of the UI Automation tree.</span></span>                                                                                                                   |
| [<span data-ttu-id="9e414-161">**UIA \_ исконтролелементпропертид**</span><span class="sxs-lookup"><span data-stu-id="9e414-161">**UIA\_IsControlElementPropertyId**</span></span>](uiauto-automation-element-propids.md)         | <span data-ttu-id="9e414-162">true</span><span class="sxs-lookup"><span data-stu-id="9e414-162">TRUE</span></span>         | <span data-ttu-id="9e414-163">Значение этого свойства всегда должно быть **true**.</span><span class="sxs-lookup"><span data-stu-id="9e414-163">The value of this property must always be **TRUE**.</span></span> <span data-ttu-id="9e414-164">Это означает, что элемент управления "флажок" всегда должен включаться в представление элемента управления дерева модели автоматизации пользовательского интерфейса.</span><span class="sxs-lookup"><span data-stu-id="9e414-164">This means that the check box control must always be included in the control view of the UI Automation tree.</span></span>                                                                                                                   |
| [<span data-ttu-id="9e414-165">**UIA \_ искэйбоардфокусаблепропертид**</span><span class="sxs-lookup"><span data-stu-id="9e414-165">**UIA\_IsKeyboardFocusablePropertyId**</span></span>](uiauto-automation-element-propids.md)   | <span data-ttu-id="9e414-166">См. примечания.</span><span class="sxs-lookup"><span data-stu-id="9e414-166">See notes.</span></span>   | <span data-ttu-id="9e414-167">Если элемент управления может получать фокус клавиатуры, он должен поддерживать это свойство.</span><span class="sxs-lookup"><span data-stu-id="9e414-167">If the control can receive keyboard focus, it must support this property.</span></span>                                                                                                                                                                                                          |
| [<span data-ttu-id="9e414-168">**UIA \_ лабеледбипропертид**</span><span class="sxs-lookup"><span data-stu-id="9e414-168">**UIA\_LabeledByPropertyId**</span></span>](uiauto-automation-element-propids.md)                       | <span data-ttu-id="9e414-169">NULL</span><span class="sxs-lookup"><span data-stu-id="9e414-169">Null</span></span>         | <span data-ttu-id="9e414-170">Элементы управления "флажок" являются самостоятельными метками.</span><span class="sxs-lookup"><span data-stu-id="9e414-170">Check box controls are self-labeling.</span></span>                                                                                                                                                                                                                                              |
| [<span data-ttu-id="9e414-171">**UIA \_ локализедконтролтипепропертид**</span><span class="sxs-lookup"><span data-stu-id="9e414-171">**UIA\_LocalizedControlTypePropertyId**</span></span>](uiauto-automation-element-propids.md) | <span data-ttu-id="9e414-172">См. примечания.</span><span class="sxs-lookup"><span data-stu-id="9e414-172">See notes.</span></span>   | <span data-ttu-id="9e414-173">Локализованная строка, соответствующая типу элемента управления **CheckBox** .</span><span class="sxs-lookup"><span data-stu-id="9e414-173">Localized string corresponding to the **CheckBox** control type.</span></span> <span data-ttu-id="9e414-174">Значение по умолчанию — "флажок" для en-US или English (США).</span><span class="sxs-lookup"><span data-stu-id="9e414-174">The default value is "check box" for en-US or English (United States).</span></span>                                                                                                                                            |
| [<span data-ttu-id="9e414-175">**UIA \_ намепропертид**</span><span class="sxs-lookup"><span data-stu-id="9e414-175">**UIA\_NamePropertyId**</span></span>](uiauto-automation-element-propids.md)                                 | <span data-ttu-id="9e414-176">См. примечания.</span><span class="sxs-lookup"><span data-stu-id="9e414-176">See notes.</span></span>   | <span data-ttu-id="9e414-177">Значением свойства [**иуиаутоматионелемент:: куррентнаме**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-get_currentname) (или [**качеднаме**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-get_cachedname)) элемента управления "флажок" является текст, отображаемый рядом с полем, поддерживающим состояние переключения.</span><span class="sxs-lookup"><span data-stu-id="9e414-177">The value of the check box control's [**IUIAutomationElement::CurrentName**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-get_currentname) (or [**CachedName**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-get_cachedname)) property is the text that is displayed beside the box that maintains the toggle state.</span></span> |



 

## <a name="required-control-patterns"></a><span data-ttu-id="9e414-178">Обязательные шаблоны элементов управления</span><span class="sxs-lookup"><span data-stu-id="9e414-178">Required Control Patterns</span></span>

<span data-ttu-id="9e414-179">В следующей таблице перечислены шаблоны элементов управления модели автоматизации пользовательского интерфейса, которые должны поддерживаться всеми элементами управления "флажок".</span><span class="sxs-lookup"><span data-stu-id="9e414-179">The following table lists the UI Automation control patterns required to be supported by all check box controls.</span></span> <span data-ttu-id="9e414-180">Дополнительные сведения о шаблонах элементов управления см. в разделе [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md).</span><span class="sxs-lookup"><span data-stu-id="9e414-180">For more information on control patterns, see [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md).</span></span>



| <span data-ttu-id="9e414-181">Шаблон элемента управления/свойство шаблона</span><span class="sxs-lookup"><span data-stu-id="9e414-181">Control Pattern/Pattern Property</span></span>                  | <span data-ttu-id="9e414-182">Поддержка/значение</span><span class="sxs-lookup"><span data-stu-id="9e414-182">Support/Value</span></span> | <span data-ttu-id="9e414-183">Примечания</span><span class="sxs-lookup"><span data-stu-id="9e414-183">Notes</span></span>                                                                                                                                                             |
|---------------------------------------------------|---------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="9e414-184">**IToggleProvider**</span><span class="sxs-lookup"><span data-stu-id="9e414-184">**IToggleProvider**</span></span>](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itoggleprovider) | <span data-ttu-id="9e414-185">Обязательно</span><span class="sxs-lookup"><span data-stu-id="9e414-185">Required</span></span>      | <span data-ttu-id="9e414-186">Флажки поддерживают шаблон элемента управления [Toggle](uiauto-implementingtoggle.md) , чтобы этот флажок был программно циклически переключаться по внутренним состояниям.</span><span class="sxs-lookup"><span data-stu-id="9e414-186">Check boxes support the [Toggle](uiauto-implementingtoggle.md) control pattern to allow the check box to be programmatically cycled through its internal states.</span></span> |



 

## <a name="required-events"></a><span data-ttu-id="9e414-187">Обязательные события</span><span class="sxs-lookup"><span data-stu-id="9e414-187">Required Events</span></span>

<span data-ttu-id="9e414-188">В следующей таблице перечислены события автоматизации пользовательского интерфейса, которые должны поддерживаться элементами управления "флажок".</span><span class="sxs-lookup"><span data-stu-id="9e414-188">The following table lists the UI Automation events that check box controls are required to support.</span></span> <span data-ttu-id="9e414-189">Дополнительные сведения о событиях см. в разделе [UI Automation Events Overview](uiauto-eventsoverview.md).</span><span class="sxs-lookup"><span data-stu-id="9e414-189">For more information on events, see [UI Automation Events Overview](uiauto-eventsoverview.md).</span></span>



| <span data-ttu-id="9e414-190">Событие автоматизации пользовательского интерфейса</span><span class="sxs-lookup"><span data-stu-id="9e414-190">UI Automation Event</span></span>                                                                                                                   | <span data-ttu-id="9e414-191">Примечания</span><span class="sxs-lookup"><span data-stu-id="9e414-191">Notes</span></span>                                                                                                                      |
|---------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="9e414-192">**UIA \_ аутоматионфокусчанжедевентид**</span><span class="sxs-lookup"><span data-stu-id="9e414-192">**UIA\_AutomationFocusChangedEventId**</span></span>](uiauto-event-ids.md)                                      |                                                                                                                            |
| <span data-ttu-id="9e414-193">[**UIA \_**](uiauto-automation-element-propids.md) Событие изменения свойства баундингректанглепропертид.</span><span class="sxs-lookup"><span data-stu-id="9e414-193">[**UIA\_BoundingRectanglePropertyId**](uiauto-automation-element-propids.md) property-changed event.</span></span> |                                                                                                                            |
| <span data-ttu-id="9e414-194">[**UIA \_**](uiauto-automation-element-propids.md) Событие изменения свойства исоффскринпропертид.</span><span class="sxs-lookup"><span data-stu-id="9e414-194">[**UIA\_IsOffscreenPropertyId**](uiauto-automation-element-propids.md) property-changed event.</span></span>             | <span data-ttu-id="9e414-195">Если элемент управления поддерживает свойство [**исоффскрин**](uiauto-automation-element-propids.md) , он должен поддерживать это событие.</span><span class="sxs-lookup"><span data-stu-id="9e414-195">If the control supports the [**IsOffscreen**](uiauto-automation-element-propids.md) property, it must support this event.</span></span> |
| <span data-ttu-id="9e414-196">[**UIA \_**](uiauto-automation-element-propids.md) Событие изменения свойства исенабледпропертид.</span><span class="sxs-lookup"><span data-stu-id="9e414-196">[**UIA\_IsEnabledPropertyId**](uiauto-automation-element-propids.md) property-changed event.</span></span>                 | <span data-ttu-id="9e414-197">Если элемент управления поддерживает свойство « [**включено**](uiauto-automation-element-propids.md) », оно должно поддерживать это событие.</span><span class="sxs-lookup"><span data-stu-id="9e414-197">If the control supports the [**IsEnabled**](uiauto-automation-element-propids.md) property, it must support this event.</span></span>   |
| [<span data-ttu-id="9e414-198">**UIA \_ структуречанжедевентид**</span><span class="sxs-lookup"><span data-stu-id="9e414-198">**UIA\_StructureChangedEventId**</span></span>](uiauto-event-ids.md)                                                  |                                                                                                                            |
| <span data-ttu-id="9e414-199">[**UIA \_**](uiauto-control-pattern-propids.md) Событие изменения свойства тогглетогглестатепропертид.</span><span class="sxs-lookup"><span data-stu-id="9e414-199">[**UIA\_ToggleToggleStatePropertyId**](uiauto-control-pattern-propids.md) property-changed event.</span></span>    |                                                                                                                            |



 

## <a name="defaultaction"></a><span data-ttu-id="9e414-200">DefaultAction</span><span class="sxs-lookup"><span data-stu-id="9e414-200">DefaultAction</span></span>

<span data-ttu-id="9e414-201">Действие по умолчанию флажка — вызов переключателя для получения фокуса и переключение текущего состояния.</span><span class="sxs-lookup"><span data-stu-id="9e414-201">The default action of the check box is to cause a radio button to become focused and toggle its current state.</span></span> <span data-ttu-id="9e414-202">Как упоминалось ранее, флажки предоставляют пользователю решение в двоичном виде (да/нет или вкл.) или в третьем (вкл., отключено, неопределенное).</span><span class="sxs-lookup"><span data-stu-id="9e414-202">As mentioned previously, check boxes either present a binary (Yes/No or On/Off) decision to the user or a tertiary (On, Off, Indeterminate).</span></span> <span data-ttu-id="9e414-203">Если флажок является двоичным, в результате действия по умолчанию состояние «вкл.» становится состоянием «выкл.», или состояние «выкл.» становится «вкл.».</span><span class="sxs-lookup"><span data-stu-id="9e414-203">If the check box is binary the default action causes the "on" state to become "off" or the "off" state to become "on".</span></span> <span data-ttu-id="9e414-204">В третичном флажке действие по умолчанию циклически проходит по состояниям флажка в том же порядке, что и если пользователь отправил щелчок мышью в элементе управления.</span><span class="sxs-lookup"><span data-stu-id="9e414-204">In a tertiary check box the default action cycles through the states of the check box in the same order as if the user had sent successive mouse clicks to the control.</span></span>

## <a name="related-topics"></a><span data-ttu-id="9e414-205">См. также</span><span class="sxs-lookup"><span data-stu-id="9e414-205">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="9e414-206">**Зрения**</span><span class="sxs-lookup"><span data-stu-id="9e414-206">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="9e414-207">Общие сведения о типах элементов управления автоматизации пользовательского интерфейса</span><span class="sxs-lookup"><span data-stu-id="9e414-207">UI Automation Control Types Overview</span></span>](uiauto-controltypesoverview.md)
</dt> <dt>

[<span data-ttu-id="9e414-208">Общие сведения о модели автоматизации пользовательского интерфейса</span><span class="sxs-lookup"><span data-stu-id="9e414-208">UI Automation Overview</span></span>](uiauto-uiautomationoverview.md)
</dt> </dl>

 

 




