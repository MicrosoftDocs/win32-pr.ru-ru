---
title: Тип элемента управления "заголовок"
description: В этом разделе содержатся сведения о поддержке автоматизации пользовательского интерфейса Майкрософт для типа элемента управления "заголовок". Элемент управления "заголовок окна" представляет заголовок или строку заголовка в окне.
ms.assetid: dc707198-ceb6-4fbf-ace4-8fec88c92b98
keywords:
- Модель автоматизации пользовательского интерфейса, поддержка типа элемента управления "заголовок"
- Модель автоматизации пользовательского интерфейса, тип элемента управления "заголовок"
- Модель автоматизации пользовательского интерфейса, древовидная структура для типа элемента управления "заголовок"
- Модель автоматизации пользовательского интерфейса, свойства для типа элемента управления "заголовок"
- Модель автоматизации пользовательского интерфейса, шаблоны элементов управления для типа элемента управления "заголовок"
- Модель автоматизации пользовательского интерфейса, события для типа элемента управления "заголовок"
- Древовидные структуры, тип элемента управления "заголовок"
- свойства, тип элемента управления "заголовок"
- шаблоны элементов управления, тип элемента управления "заголовок"
- события, тип элемента управления "заголовок"
- Поддержка типа элемента управления "заголовок"
- Тип элемента управления "заголовок"
- типы элементов управления, древовидная структура для типа элемента управления "заголовок"
- типы элементов управления, шаблоны элементов управления для типа элемента управления "заголовок"
- типы элементов управления, поддержка заголовка
- типы элементов управления, строка заголовка
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8f9471d08479345bf8c1df118f720bf273d4d89d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103986804"
---
# <a name="titlebar-control-type"></a><span data-ttu-id="32995-120">Тип элемента управления "заголовок"</span><span class="sxs-lookup"><span data-stu-id="32995-120">TitleBar Control Type</span></span>

<span data-ttu-id="32995-121">В этом разделе содержатся сведения о поддержке автоматизации пользовательского интерфейса Майкрософт для типа элемента управления " **заголовок** ".</span><span class="sxs-lookup"><span data-stu-id="32995-121">This topic provides information about Microsoft UI Automation support for the **TitleBar** control type.</span></span> <span data-ttu-id="32995-122">Элемент управления "заголовок окна" представляет заголовок или строку заголовка в окне.</span><span class="sxs-lookup"><span data-stu-id="32995-122">A title bar control represents a title or caption bar in a window.</span></span>

<span data-ttu-id="32995-123">В следующих разделах определяется необходимая древовидная структура модели автоматизации пользовательского интерфейса, свойства, шаблоны элементов управления и события для типа элемента управления " **заголовок** ".</span><span class="sxs-lookup"><span data-stu-id="32995-123">The following sections define the required UI Automation tree structure, properties, control patterns, and events for the **TitleBar** control type.</span></span> <span data-ttu-id="32995-124">Требования к автоматизации пользовательского интерфейса применяются ко всем элементам управления "заголовок окна", где платформа или платформа пользовательского интерфейса интегрирует поддержку автоматизации пользовательского интерфейса для типов элементов управления и шаблонов элементов управления.</span><span class="sxs-lookup"><span data-stu-id="32995-124">The UI Automation requirements apply to all title bar controls where the UI framework/platform integrates UI Automation support for control types and control patterns.</span></span>

<span data-ttu-id="32995-125">В этом разделе содержатся следующие подразделы.</span><span class="sxs-lookup"><span data-stu-id="32995-125">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="32995-126">Типичная древовидная структура</span><span class="sxs-lookup"><span data-stu-id="32995-126">Typical Tree Structure</span></span>](#typical-tree-structure)
-   [<span data-ttu-id="32995-127">Соответствующие свойства</span><span class="sxs-lookup"><span data-stu-id="32995-127">Relevant Properties</span></span>](#relevant-properties)
-   [<span data-ttu-id="32995-128">Обязательные шаблоны элементов управления</span><span class="sxs-lookup"><span data-stu-id="32995-128">Required Control Patterns</span></span>](#required-control-patterns)
-   [<span data-ttu-id="32995-129">Обязательные события</span><span class="sxs-lookup"><span data-stu-id="32995-129">Required Events</span></span>](#required-events)
-   [<span data-ttu-id="32995-130">См. также</span><span class="sxs-lookup"><span data-stu-id="32995-130">Related topics</span></span>](#related-topics)

## <a name="typical-tree-structure"></a><span data-ttu-id="32995-131">Типичная древовидная структура</span><span class="sxs-lookup"><span data-stu-id="32995-131">Typical Tree Structure</span></span>

<span data-ttu-id="32995-132">В следующей таблице описывается типичный элемент управления и представление содержимого дерева модели автоматизации пользовательского интерфейса, которое относится к элементам управления "заголовок окна" и описывает, что может содержаться в каждом представлении.</span><span class="sxs-lookup"><span data-stu-id="32995-132">The following table depicts a typical control and content view of the UI Automation tree that pertains to title bar controls and describes what can be contained in each view.</span></span> <span data-ttu-id="32995-133">Дополнительные сведения о дереве автоматизации пользовательского интерфейса см. в разделе [Общие сведения о дереве модели автоматизации пользовательского интерфейса](uiauto-treeoverview.md).</span><span class="sxs-lookup"><span data-stu-id="32995-133">For more information about the UI Automation tree, see [UI Automation Tree Overview](uiauto-treeoverview.md).</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="32995-134">Представление элемента управления</span><span class="sxs-lookup"><span data-stu-id="32995-134">Control View</span></span></th>
<th><span data-ttu-id="32995-135">Представление содержимого</span><span class="sxs-lookup"><span data-stu-id="32995-135">Content View</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><ul>
<li><span data-ttu-id="32995-136">TitleBar</span><span class="sxs-lookup"><span data-stu-id="32995-136">TitleBar</span></span>
<ul>
<li><span data-ttu-id="32995-137">Menu (0 или 1)</span><span class="sxs-lookup"><span data-stu-id="32995-137">Menu (0 or 1)</span></span></li>
<li><span data-ttu-id="32995-138">Button (0 или более)</span><span class="sxs-lookup"><span data-stu-id="32995-138">Button (0 or more)</span></span></li>
</ul></li>
</ul></td>
<td><span data-ttu-id="32995-139">(Неприменимо; элемент управления "заголовок окна" не имеет содержимого)</span><span class="sxs-lookup"><span data-stu-id="32995-139">(Not applicable; the title bar control has no content)</span></span></td>
</tr>
</tbody>
</table>



 

## <a name="relevant-properties"></a><span data-ttu-id="32995-140">Соответствующие свойства</span><span class="sxs-lookup"><span data-stu-id="32995-140">Relevant Properties</span></span>

<span data-ttu-id="32995-141">В следующей таблице перечислены свойства модели автоматизации пользовательского интерфейса, значения или определения которых особенно важны для типа элемента управления " **заголовок** ".</span><span class="sxs-lookup"><span data-stu-id="32995-141">The following table lists the UI Automation properties whose value or definition is especially relevant to the **TitleBar** control type.</span></span> <span data-ttu-id="32995-142">Дополнительные сведения о свойствах модели автоматизации пользовательского интерфейса см. в разделе [Получение свойств элементов модели автоматизации пользовательского интерфейса](uiauto-propertiesforclients.md).</span><span class="sxs-lookup"><span data-stu-id="32995-142">For more information about UI Automation properties, see [Retrieving Properties from UI Automation Elements](uiauto-propertiesforclients.md).</span></span>



| <span data-ttu-id="32995-143">Свойство модели автоматизации пользовательского интерфейса</span><span class="sxs-lookup"><span data-stu-id="32995-143">UI Automation Property</span></span>                                                                                              | <span data-ttu-id="32995-144">Значение</span><span class="sxs-lookup"><span data-stu-id="32995-144">Value</span></span>        | <span data-ttu-id="32995-145">Примечания</span><span class="sxs-lookup"><span data-stu-id="32995-145">Notes</span></span>                                                                                                                                                                                                |
|---------------------------------------------------------------------------------------------------------------------|--------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="32995-146">**UIA \_ аутоматионидпропертид**</span><span class="sxs-lookup"><span data-stu-id="32995-146">**UIA\_AutomationIdPropertyId**</span></span>](uiauto-automation-element-propids.md)                 | <span data-ttu-id="32995-147">См. примечания.</span><span class="sxs-lookup"><span data-stu-id="32995-147">See notes.</span></span>   | <span data-ttu-id="32995-148">Значение этого свойства должно быть уникальным среди всех одноранговых элементов в необработанном представлении дерева модели автоматизации пользовательского интерфейса.</span><span class="sxs-lookup"><span data-stu-id="32995-148">The value of this property must be unique among all peer elements in the raw view of the UI Automation tree.</span></span>                                                                                         |
| [<span data-ttu-id="32995-149">**UIA \_ баундингректанглепропертид**</span><span class="sxs-lookup"><span data-stu-id="32995-149">**UIA\_BoundingRectanglePropertyId**</span></span>](uiauto-automation-element-propids.md)       | <span data-ttu-id="32995-150">См. примечания.</span><span class="sxs-lookup"><span data-stu-id="32995-150">See notes.</span></span>   | <span data-ttu-id="32995-151">Значение, представляемое этим свойством, должно включать все содержащиеся в нем элементы управления.</span><span class="sxs-lookup"><span data-stu-id="32995-151">The value exposed by this property must include all of the controls contained within it.</span></span>                                                                                                             |
| [<span data-ttu-id="32995-152">**UIA \_ кликкаблепоинтпропертид**</span><span class="sxs-lookup"><span data-stu-id="32995-152">**UIA\_ClickablePointPropertyId**</span></span>](uiauto-automation-element-propids.md)             | <span data-ttu-id="32995-153">См. примечания.</span><span class="sxs-lookup"><span data-stu-id="32995-153">See notes.</span></span>   | <span data-ttu-id="32995-154">Поддерживается при наличии ограничивающего прямоугольника.</span><span class="sxs-lookup"><span data-stu-id="32995-154">Supported if there is a bounding rectangle.</span></span> <span data-ttu-id="32995-155">Если не все точки внутри ограничивающего прямоугольника являются щелчками, а элемент выполняет специализированное тестирование нажатия, переопределите и предоставьте точку для щелчка.</span><span class="sxs-lookup"><span data-stu-id="32995-155">If not every point within the bounding rectangle is clickable, and the element performs specialized hit testing, override and provide a clickable point.</span></span> |
| [<span data-ttu-id="32995-156">**UIA \_ контролтипепропертид**</span><span class="sxs-lookup"><span data-stu-id="32995-156">**UIA\_ControlTypePropertyId**</span></span>](uiauto-automation-element-propids.md)                   | <span data-ttu-id="32995-157">**TitleBar**</span><span class="sxs-lookup"><span data-stu-id="32995-157">**TitleBar**</span></span> | <span data-ttu-id="32995-158">Это значение одинаково для всех инфраструктур пользовательского интерфейса.</span><span class="sxs-lookup"><span data-stu-id="32995-158">This value is the same for all UI frameworks.</span></span>                                                                                                                                                        |
| [<span data-ttu-id="32995-159">**UIA \_ исконтентелементпропертид**</span><span class="sxs-lookup"><span data-stu-id="32995-159">**UIA\_IsContentElementPropertyId**</span></span>](uiauto-automation-element-propids.md)         | <span data-ttu-id="32995-160">FALSE</span><span class="sxs-lookup"><span data-stu-id="32995-160">FALSE</span></span>        | <span data-ttu-id="32995-161">Элемент управления "заголовок окна" никогда не включается в представление содержимого дерева модели автоматизации пользовательского интерфейса.</span><span class="sxs-lookup"><span data-stu-id="32995-161">The title bar control is never included in the content view of the UI Automation tree.</span></span>                                                                                                               |
| [<span data-ttu-id="32995-162">**UIA \_ исконтролелементпропертид**</span><span class="sxs-lookup"><span data-stu-id="32995-162">**UIA\_IsControlElementPropertyId**</span></span>](uiauto-automation-element-propids.md)         | <span data-ttu-id="32995-163">true</span><span class="sxs-lookup"><span data-stu-id="32995-163">TRUE</span></span>         | <span data-ttu-id="32995-164">Элемент управления "заголовок окна" всегда включается в представление элемента управления дерева модели автоматизации пользовательского интерфейса.</span><span class="sxs-lookup"><span data-stu-id="32995-164">The title bar control is always included in the control view of the UI Automation tree.</span></span>                                                                                                              |
| [<span data-ttu-id="32995-165">**UIA \_ искэйбоардфокусаблепропертид**</span><span class="sxs-lookup"><span data-stu-id="32995-165">**UIA\_IsKeyboardFocusablePropertyId**</span></span>](uiauto-automation-element-propids.md)   | <span data-ttu-id="32995-166">FALSE</span><span class="sxs-lookup"><span data-stu-id="32995-166">FALSE</span></span>        | <span data-ttu-id="32995-167">Элемент управления "заголовок окна" никогда не имеет фокуса клавиатуры.</span><span class="sxs-lookup"><span data-stu-id="32995-167">A title bar control never has keyboard focus.</span></span>                                                                                                                                                        |
| [<span data-ttu-id="32995-168">**UIA \_ исоффскринпропертид**</span><span class="sxs-lookup"><span data-stu-id="32995-168">**UIA\_IsOffscreenPropertyId**</span></span>](uiauto-automation-element-propids.md)                   | <span data-ttu-id="32995-169">Зависит</span><span class="sxs-lookup"><span data-stu-id="32995-169">Depends</span></span>      | <span data-ttu-id="32995-170">Элемент управления "заголовок окна" возвращает значение в зависимости от того, отображается ли он на экране.</span><span class="sxs-lookup"><span data-stu-id="32995-170">A title bar control returns a value depending on whether it is visible on the screen.</span></span>                                                                                                                |
| [<span data-ttu-id="32995-171">**UIA \_ лабеледбипропертид**</span><span class="sxs-lookup"><span data-stu-id="32995-171">**UIA\_LabeledByPropertyId**</span></span>](uiauto-automation-element-propids.md)                       | <span data-ttu-id="32995-172">См. примечания.</span><span class="sxs-lookup"><span data-stu-id="32995-172">See notes.</span></span>   | <span data-ttu-id="32995-173">Элемент управления "заголовок окна" обычно не имеет метки.</span><span class="sxs-lookup"><span data-stu-id="32995-173">A title bar control typically does not have a label.</span></span>                                                                                                                                                 |
| [<span data-ttu-id="32995-174">**UIA \_ локализедконтролтипепропертид**</span><span class="sxs-lookup"><span data-stu-id="32995-174">**UIA\_LocalizedControlTypePropertyId**</span></span>](uiauto-automation-element-propids.md) | <span data-ttu-id="32995-175">См. примечания.</span><span class="sxs-lookup"><span data-stu-id="32995-175">See notes.</span></span>   | <span data-ttu-id="32995-176">Локализованная строка, соответствующая типу элемента управления TitleBar.</span><span class="sxs-lookup"><span data-stu-id="32995-176">Localized string corresponding to the TitleBar control type.</span></span> <span data-ttu-id="32995-177">Значение по умолчанию — "заголовок окна" для en-US или English (США).</span><span class="sxs-lookup"><span data-stu-id="32995-177">The default value is "title bar" for en-US or English (United States).</span></span>                                                                  |
| [<span data-ttu-id="32995-178">**UIA \_ намепропертид**</span><span class="sxs-lookup"><span data-stu-id="32995-178">**UIA\_NamePropertyId**</span></span>](uiauto-automation-element-propids.md)                                 | <span data-ttu-id="32995-179">""</span><span class="sxs-lookup"><span data-stu-id="32995-179">""</span></span>           | <span data-ttu-id="32995-180">Заголовок не является содержимым; его текстовая информация предоставляется именем родительского окна.</span><span class="sxs-lookup"><span data-stu-id="32995-180">A title bar is not content; its textual information is exposed by the name of the parent window.</span></span>                                                                                                     |



 

## <a name="required-control-patterns"></a><span data-ttu-id="32995-181">Обязательные шаблоны элементов управления</span><span class="sxs-lookup"><span data-stu-id="32995-181">Required Control Patterns</span></span>

<span data-ttu-id="32995-182">Тип элемента управления " **заголовок** окна" не требуется для поддержки шаблонов элементов управления.</span><span class="sxs-lookup"><span data-stu-id="32995-182">The **TitleBar** control type is not required to support any control patterns.</span></span> <span data-ttu-id="32995-183">Его функциональность предоставляется с помощью шаблона элемента управления [Window](uiauto-implementingwindow.md) в типе элемента управления [Window](uiauto-supportwindowcontroltype.md) .</span><span class="sxs-lookup"><span data-stu-id="32995-183">Its functionality is exposed through the [Window](uiauto-implementingwindow.md) control pattern on the [Window](uiauto-supportwindowcontroltype.md) control type.</span></span>

## <a name="required-events"></a><span data-ttu-id="32995-184">Обязательные события</span><span class="sxs-lookup"><span data-stu-id="32995-184">Required Events</span></span>

<span data-ttu-id="32995-185">В следующей таблице перечислены события автоматизации пользовательского интерфейса, которые должны поддерживаться элементами управления "заголовок окна".</span><span class="sxs-lookup"><span data-stu-id="32995-185">The following table lists the UI Automation events that title bar controls are required to support.</span></span> <span data-ttu-id="32995-186">Дополнительные сведения о событиях см. в разделе [UI Automation Events Overview](uiauto-eventsoverview.md).</span><span class="sxs-lookup"><span data-stu-id="32995-186">For more information on events, see [UI Automation Events Overview](uiauto-eventsoverview.md).</span></span>



| <span data-ttu-id="32995-187">Событие автоматизации пользовательского интерфейса</span><span class="sxs-lookup"><span data-stu-id="32995-187">UI Automation Event</span></span>                                                                                                                   | <span data-ttu-id="32995-188">Примечания</span><span class="sxs-lookup"><span data-stu-id="32995-188">Notes</span></span>                                                                                                                      |
|---------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="32995-189">**UIA \_ аутоматионфокусчанжедевентид**</span><span class="sxs-lookup"><span data-stu-id="32995-189">**UIA\_AutomationFocusChangedEventId**</span></span>](uiauto-event-ids.md)                                      |                                                                                                                            |
| <span data-ttu-id="32995-190">[**UIA \_**](uiauto-automation-element-propids.md) Событие изменения свойства баундингректанглепропертид.</span><span class="sxs-lookup"><span data-stu-id="32995-190">[**UIA\_BoundingRectanglePropertyId**](uiauto-automation-element-propids.md) property-changed event.</span></span> |                                                                                                                            |
| <span data-ttu-id="32995-191">[**UIA \_**](uiauto-automation-element-propids.md) Событие изменения свойства исенабледпропертид.</span><span class="sxs-lookup"><span data-stu-id="32995-191">[**UIA\_IsEnabledPropertyId**](uiauto-automation-element-propids.md) property-changed event.</span></span>                 | <span data-ttu-id="32995-192">Если элемент управления поддерживает свойство « [**включено**](uiauto-automation-element-propids.md) », оно должно поддерживать это событие.</span><span class="sxs-lookup"><span data-stu-id="32995-192">If the control supports the [**IsEnabled**](uiauto-automation-element-propids.md) property, it must support this event.</span></span>   |
| <span data-ttu-id="32995-193">[**UIA \_**](uiauto-automation-element-propids.md) Событие изменения свойства исоффскринпропертид.</span><span class="sxs-lookup"><span data-stu-id="32995-193">[**UIA\_IsOffscreenPropertyId**](uiauto-automation-element-propids.md) property-changed event.</span></span>             | <span data-ttu-id="32995-194">Если элемент управления поддерживает свойство [**исоффскрин**](uiauto-automation-element-propids.md) , он должен поддерживать это событие.</span><span class="sxs-lookup"><span data-stu-id="32995-194">If the control supports the [**IsOffscreen**](uiauto-automation-element-propids.md) property, it must support this event.</span></span> |
| [<span data-ttu-id="32995-195">**UIA \_ структуречанжедевентид**</span><span class="sxs-lookup"><span data-stu-id="32995-195">**UIA\_StructureChangedEventId**</span></span>](uiauto-event-ids.md)                                                  |                                                                                                                            |



 

## <a name="related-topics"></a><span data-ttu-id="32995-196">См. также</span><span class="sxs-lookup"><span data-stu-id="32995-196">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="32995-197">**Зрения**</span><span class="sxs-lookup"><span data-stu-id="32995-197">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="32995-198">Общие сведения о типах элементов управления автоматизации пользовательского интерфейса</span><span class="sxs-lookup"><span data-stu-id="32995-198">UI Automation Control Types Overview</span></span>](uiauto-controltypesoverview.md)
</dt> <dt>

[<span data-ttu-id="32995-199">Общие сведения о модели автоматизации пользовательского интерфейса</span><span class="sxs-lookup"><span data-stu-id="32995-199">UI Automation Overview</span></span>](uiauto-uiautomationoverview.md)
</dt> </dl>

 

 




