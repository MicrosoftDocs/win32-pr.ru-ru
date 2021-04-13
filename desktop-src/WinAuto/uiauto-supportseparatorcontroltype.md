---
title: Тип элемента управления Separator
description: В этом разделе содержатся сведения о поддержке автоматизации пользовательского интерфейса Майкрософт для типа элемента управления Separator.
ms.assetid: 4987b05a-101e-48b1-aed2-bd7206146f70
keywords:
- Модель автоматизации пользовательского интерфейса, поддержка типа элемента управления Separator
- Модель автоматизации пользовательского интерфейса, тип элемента управления Separator
- Модель автоматизации пользовательского интерфейса, древовидная структура для типа элемента управления Separator
- Модель автоматизации пользовательского интерфейса, свойства для типа элемента управления Separator
- Модель автоматизации пользовательского интерфейса, шаблоны элементов управления для типа элемента управления Separator
- Модель автоматизации пользовательского интерфейса, события для типа элемента управления Separator
- Древовидные структуры, тип элемента управления Separator
- свойства, тип элемента управления Separator
- шаблоны элементов управления, тип элемента управления Separator
- события, тип элемента управления Separator
- Поддержка типа элемента управления Separator
- Separator - тип элемента управления
- типы элементов управления, древовидная структура для типа элемента управления Separator
- типы элементов управления, шаблоны элементов управления для типа элемента управления Separator
- типы элементов управления, поддержка разделителя
- типы элементов управления, разделитель
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 92cdf6c15dbe461e78877c6b93f0ff4b52f67fc8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104532315"
---
# <a name="separator-control-type"></a><span data-ttu-id="e8e66-119">Тип элемента управления Separator</span><span class="sxs-lookup"><span data-stu-id="e8e66-119">Separator Control Type</span></span>

<span data-ttu-id="e8e66-120">В этом разделе содержатся сведения о поддержке автоматизации пользовательского интерфейса Майкрософт для типа элемента управления **separator** .</span><span class="sxs-lookup"><span data-stu-id="e8e66-120">This topic provides information about Microsoft UI Automation support for the **Separator** control type.</span></span>

<span data-ttu-id="e8e66-121">Элементы управления "Разделитель" используются для визуального разделения пространства на две области.</span><span class="sxs-lookup"><span data-stu-id="e8e66-121">Separator controls are used to visually divide a space into two regions.</span></span> <span data-ttu-id="e8e66-122">Например, элемент управления "Разделитель" может быть полосой, задающей две панели в окне.</span><span class="sxs-lookup"><span data-stu-id="e8e66-122">For example, a separator control can be a bar that defines two panes in a window.</span></span> <span data-ttu-id="e8e66-123">Если разделитель можно перемещать, элемент управления должен поддерживать тип элемента управления Thumb.</span><span class="sxs-lookup"><span data-stu-id="e8e66-123">If the separator can be moved, the control should be exposed as Thumb in control type.</span></span>

<span data-ttu-id="e8e66-124">В следующих разделах определяется необходимая древовидная структура модели автоматизации пользовательского интерфейса, свойства, шаблоны элементов управления и события для типа элемента управления **separator** .</span><span class="sxs-lookup"><span data-stu-id="e8e66-124">The following sections define the required UI Automation tree structure, properties, control patterns, and events for the **Separator** control type.</span></span> <span data-ttu-id="e8e66-125">Требования к автоматизации пользовательского интерфейса применяются ко всем элементам управления "разделитель", в которых платформа или платформа пользовательского интерфейса интегрирует поддержку модели автоматизации пользовательского интерфейса для типов элементов управления и шаблонов элементов управления.</span><span class="sxs-lookup"><span data-stu-id="e8e66-125">The UI Automation requirements apply to all separator controls where the UI framework/platform integrates UI Automation support for control types and control patterns.</span></span>

<span data-ttu-id="e8e66-126">В этом разделе содержатся следующие подразделы.</span><span class="sxs-lookup"><span data-stu-id="e8e66-126">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="e8e66-127">Типичная древовидная структура</span><span class="sxs-lookup"><span data-stu-id="e8e66-127">Typical Tree Structure</span></span>](#typical-tree-structure)
-   [<span data-ttu-id="e8e66-128">Соответствующие свойства</span><span class="sxs-lookup"><span data-stu-id="e8e66-128">Relevant Properties</span></span>](#relevant-properties)
-   [<span data-ttu-id="e8e66-129">Обязательные шаблоны элементов управления</span><span class="sxs-lookup"><span data-stu-id="e8e66-129">Required Control Patterns</span></span>](#required-control-patterns)
-   [<span data-ttu-id="e8e66-130">Обязательные события</span><span class="sxs-lookup"><span data-stu-id="e8e66-130">Required Events</span></span>](#required-events)
-   [<span data-ttu-id="e8e66-131">См. также</span><span class="sxs-lookup"><span data-stu-id="e8e66-131">Related topics</span></span>](#related-topics)

## <a name="typical-tree-structure"></a><span data-ttu-id="e8e66-132">Типичная древовидная структура</span><span class="sxs-lookup"><span data-stu-id="e8e66-132">Typical Tree Structure</span></span>

<span data-ttu-id="e8e66-133">В следующей таблице описывается типичный элемент управления и представление содержимого дерева модели автоматизации пользовательского интерфейса, относящиеся к элементам управления "разделитель", и показывается, что может содержаться в каждом представлении.</span><span class="sxs-lookup"><span data-stu-id="e8e66-133">The following table depicts a typical control and content view of the UI Automation tree that pertains to separator controls and describes what can be contained in each view.</span></span> <span data-ttu-id="e8e66-134">Дополнительные сведения о дереве автоматизации пользовательского интерфейса см. в разделе [Общие сведения о дереве модели автоматизации пользовательского интерфейса](uiauto-treeoverview.md).</span><span class="sxs-lookup"><span data-stu-id="e8e66-134">For more information about the UI Automation tree, see [UI Automation Tree Overview](uiauto-treeoverview.md).</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="e8e66-135">Представление элемента управления</span><span class="sxs-lookup"><span data-stu-id="e8e66-135">Control View</span></span></th>
<th><span data-ttu-id="e8e66-136">Представление содержимого</span><span class="sxs-lookup"><span data-stu-id="e8e66-136">Content View</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><ul>
<li><span data-ttu-id="e8e66-137">Separator</span><span class="sxs-lookup"><span data-stu-id="e8e66-137">Separator</span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="e8e66-138">Тип элемента управления <strong>separator</strong> никогда не имеет содержимого.</span><span class="sxs-lookup"><span data-stu-id="e8e66-138">The <strong>Separator</strong> control type never has content.</span></span></li>
</ul></td>
</tr>
</tbody>
</table>



 

## <a name="relevant-properties"></a><span data-ttu-id="e8e66-139">Соответствующие свойства</span><span class="sxs-lookup"><span data-stu-id="e8e66-139">Relevant Properties</span></span>

<span data-ttu-id="e8e66-140">В следующей таблице перечислены свойства модели автоматизации пользовательского интерфейса, значения или определения которых особенно важны для элементов управления "разделитель".</span><span class="sxs-lookup"><span data-stu-id="e8e66-140">The following table lists the UI Automation properties whose value or definition is especially relevant to separator controls.</span></span> <span data-ttu-id="e8e66-141">Дополнительные сведения о свойствах модели автоматизации пользовательского интерфейса см. в разделе [Получение свойств элементов модели автоматизации пользовательского интерфейса](uiauto-propertiesforclients.md).</span><span class="sxs-lookup"><span data-stu-id="e8e66-141">For more information about UI Automation properties, see [Retrieving Properties from UI Automation Elements](uiauto-propertiesforclients.md).</span></span>



| <span data-ttu-id="e8e66-142">Свойство модели автоматизации пользовательского интерфейса</span><span class="sxs-lookup"><span data-stu-id="e8e66-142">UI Automation Property</span></span>                                                                                              | <span data-ttu-id="e8e66-143">Значение</span><span class="sxs-lookup"><span data-stu-id="e8e66-143">Value</span></span>         | <span data-ttu-id="e8e66-144">Примечания</span><span class="sxs-lookup"><span data-stu-id="e8e66-144">Notes</span></span>                                                                                                                                                                                                |
|---------------------------------------------------------------------------------------------------------------------|---------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="e8e66-145">**UIA \_ аутоматионидпропертид**</span><span class="sxs-lookup"><span data-stu-id="e8e66-145">**UIA\_AutomationIdPropertyId**</span></span>](uiauto-automation-element-propids.md)                 | <span data-ttu-id="e8e66-146">См. примечания.</span><span class="sxs-lookup"><span data-stu-id="e8e66-146">See notes.</span></span>    | <span data-ttu-id="e8e66-147">Значение этого свойства должно быть уникальным среди всех одноранговых элементов в необработанном представлении дерева модели автоматизации пользовательского интерфейса.</span><span class="sxs-lookup"><span data-stu-id="e8e66-147">The value of this property must be unique among all peer elements in the raw view of the UI Automation tree.</span></span>                                                                                         |
| [<span data-ttu-id="e8e66-148">**UIA \_ баундингректанглепропертид**</span><span class="sxs-lookup"><span data-stu-id="e8e66-148">**UIA\_BoundingRectanglePropertyId**</span></span>](uiauto-automation-element-propids.md)       | <span data-ttu-id="e8e66-149">См. примечания.</span><span class="sxs-lookup"><span data-stu-id="e8e66-149">See notes.</span></span>    | <span data-ttu-id="e8e66-150">Внешний прямоугольник, содержащий весь элемент управления.</span><span class="sxs-lookup"><span data-stu-id="e8e66-150">The outermost rectangle that contains the whole control.</span></span>                                                                                                                                             |
| [<span data-ttu-id="e8e66-151">**UIA \_ кликкаблепоинтпропертид**</span><span class="sxs-lookup"><span data-stu-id="e8e66-151">**UIA\_ClickablePointPropertyId**</span></span>](uiauto-automation-element-propids.md)             | <span data-ttu-id="e8e66-152">См. примечания.</span><span class="sxs-lookup"><span data-stu-id="e8e66-152">See notes.</span></span>    | <span data-ttu-id="e8e66-153">Поддерживается при наличии ограничивающего прямоугольника.</span><span class="sxs-lookup"><span data-stu-id="e8e66-153">Supported if there is a bounding rectangle.</span></span> <span data-ttu-id="e8e66-154">Если не все точки внутри ограничивающего прямоугольника являются щелчками, а элемент выполняет специализированное тестирование нажатия, переопределите и предоставьте точку для щелчка.</span><span class="sxs-lookup"><span data-stu-id="e8e66-154">If not every point within the bounding rectangle is clickable, and the element performs specialized hit testing, override and provide a clickable point.</span></span> |
| [<span data-ttu-id="e8e66-155">**UIA \_ контролтипепропертид**</span><span class="sxs-lookup"><span data-stu-id="e8e66-155">**UIA\_ControlTypePropertyId**</span></span>](uiauto-automation-element-propids.md)                   | <span data-ttu-id="e8e66-156">**Separator**</span><span class="sxs-lookup"><span data-stu-id="e8e66-156">**Separator**</span></span> |                                                                                                                                                                                                      |
| [<span data-ttu-id="e8e66-157">**UIA \_ исконтентелементпропертид**</span><span class="sxs-lookup"><span data-stu-id="e8e66-157">**UIA\_IsContentElementPropertyId**</span></span>](uiauto-automation-element-propids.md)         | <span data-ttu-id="e8e66-158">FALSE</span><span class="sxs-lookup"><span data-stu-id="e8e66-158">FALSE</span></span>         | <span data-ttu-id="e8e66-159">Элемент управления "Разделитель" никогда не является содержимым.</span><span class="sxs-lookup"><span data-stu-id="e8e66-159">The separator control is never content.</span></span>                                                                                                                                                              |
| [<span data-ttu-id="e8e66-160">**UIA \_ исконтролелементпропертид**</span><span class="sxs-lookup"><span data-stu-id="e8e66-160">**UIA\_IsControlElementPropertyId**</span></span>](uiauto-automation-element-propids.md)         | <span data-ttu-id="e8e66-161">true</span><span class="sxs-lookup"><span data-stu-id="e8e66-161">TRUE</span></span>          | <span data-ttu-id="e8e66-162">Элемент управления "Разделитель" всегда должен быть элементом управления.</span><span class="sxs-lookup"><span data-stu-id="e8e66-162">The separator control must always be a control.</span></span>                                                                                                                                                      |
| [<span data-ttu-id="e8e66-163">**UIA \_ искэйбоардфокусаблепропертид**</span><span class="sxs-lookup"><span data-stu-id="e8e66-163">**UIA\_IsKeyboardFocusablePropertyId**</span></span>](uiauto-automation-element-propids.md)   | <span data-ttu-id="e8e66-164">См. примечания.</span><span class="sxs-lookup"><span data-stu-id="e8e66-164">See notes.</span></span>    | <span data-ttu-id="e8e66-165">Если элемент управления может получать фокус клавиатуры, он должен поддерживать это свойство.</span><span class="sxs-lookup"><span data-stu-id="e8e66-165">If the control can receive keyboard focus, it must support this property.</span></span>                                                                                                                            |
| [<span data-ttu-id="e8e66-166">**UIA \_ лабеледбипропертид**</span><span class="sxs-lookup"><span data-stu-id="e8e66-166">**UIA\_LabeledByPropertyId**</span></span>](uiauto-automation-element-propids.md)                       | <span data-ttu-id="e8e66-167">NULL</span><span class="sxs-lookup"><span data-stu-id="e8e66-167">NULL</span></span>          | <span data-ttu-id="e8e66-168">Элемент управления "Разделитель" не имеет статической метки.</span><span class="sxs-lookup"><span data-stu-id="e8e66-168">The separator control does not have a static label.</span></span>                                                                                                                                                  |
| [<span data-ttu-id="e8e66-169">**UIA \_ локализедконтролтипепропертид**</span><span class="sxs-lookup"><span data-stu-id="e8e66-169">**UIA\_LocalizedControlTypePropertyId**</span></span>](uiauto-automation-element-propids.md) | <span data-ttu-id="e8e66-170">См. примечания.</span><span class="sxs-lookup"><span data-stu-id="e8e66-170">See notes.</span></span>    | <span data-ttu-id="e8e66-171">Локализованная строка, соответствующая типу элемента управления **separator** .</span><span class="sxs-lookup"><span data-stu-id="e8e66-171">Localized string corresponding to the **Separator** control type.</span></span> <span data-ttu-id="e8e66-172">Значение по умолчанию — "разделитель" для en-US или English (США).</span><span class="sxs-lookup"><span data-stu-id="e8e66-172">The default value is "Separator" for en-US or English (United States).</span></span>                                                             |
| [<span data-ttu-id="e8e66-173">**UIA \_ намепропертид**</span><span class="sxs-lookup"><span data-stu-id="e8e66-173">**UIA\_NamePropertyId**</span></span>](uiauto-automation-element-propids.md)                                 | <span data-ttu-id="e8e66-174">""</span><span class="sxs-lookup"><span data-stu-id="e8e66-174">""</span></span>            | <span data-ttu-id="e8e66-175">Для элемента управления Separator не требуется свойство **Name** .</span><span class="sxs-lookup"><span data-stu-id="e8e66-175">The separator control does not require a **Name** property.</span></span>                                                                                                                                          |



 

## <a name="required-control-patterns"></a><span data-ttu-id="e8e66-176">Обязательные шаблоны элементов управления</span><span class="sxs-lookup"><span data-stu-id="e8e66-176">Required Control Patterns</span></span>

<span data-ttu-id="e8e66-177">Не требуется, чтобы элемент управления "Разделитель" поддерживал какой-либо шаблон элемента управления.</span><span class="sxs-lookup"><span data-stu-id="e8e66-177">The separator control is not required to support any control patterns.</span></span> <span data-ttu-id="e8e66-178">Дополнительные сведения о шаблонах элементов управления см. в разделе [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md).</span><span class="sxs-lookup"><span data-stu-id="e8e66-178">For more information on control patterns, see [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md).</span></span>

## <a name="required-events"></a><span data-ttu-id="e8e66-179">Обязательные события</span><span class="sxs-lookup"><span data-stu-id="e8e66-179">Required Events</span></span>

<span data-ttu-id="e8e66-180">В следующей таблице перечислены события автоматизации пользовательского интерфейса, которые должны поддерживаться элементами управления "разделитель".</span><span class="sxs-lookup"><span data-stu-id="e8e66-180">The following table lists the UI Automation events that separator controls are required to support.</span></span> <span data-ttu-id="e8e66-181">Дополнительные сведения о событиях см. в разделе [UI Automation Events Overview](uiauto-eventsoverview.md).</span><span class="sxs-lookup"><span data-stu-id="e8e66-181">For more information on events, see [UI Automation Events Overview](uiauto-eventsoverview.md).</span></span>



| <span data-ttu-id="e8e66-182">Событие автоматизации пользовательского интерфейса</span><span class="sxs-lookup"><span data-stu-id="e8e66-182">UI Automation Event</span></span>                                                                                                                   | <span data-ttu-id="e8e66-183">Примечания</span><span class="sxs-lookup"><span data-stu-id="e8e66-183">Notes</span></span>                                                                                                                      |
|---------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="e8e66-184">**UIA \_ аутоматионфокусчанжедевентид**</span><span class="sxs-lookup"><span data-stu-id="e8e66-184">**UIA\_AutomationFocusChangedEventId**</span></span>](uiauto-event-ids.md)                                      |                                                                                                                            |
| <span data-ttu-id="e8e66-185">[**UIA \_**](uiauto-automation-element-propids.md) Событие изменения свойства баундингректанглепропертид.</span><span class="sxs-lookup"><span data-stu-id="e8e66-185">[**UIA\_BoundingRectanglePropertyId**](uiauto-automation-element-propids.md) property-changed event.</span></span> |                                                                                                                            |
| <span data-ttu-id="e8e66-186">[**UIA \_**](uiauto-automation-element-propids.md) Событие изменения свойства исенабледпропертид.</span><span class="sxs-lookup"><span data-stu-id="e8e66-186">[**UIA\_IsEnabledPropertyId**](uiauto-automation-element-propids.md) property-changed event.</span></span>                 | <span data-ttu-id="e8e66-187">Если элемент управления поддерживает свойство « [**включено**](uiauto-automation-element-propids.md) », оно должно поддерживать это событие.</span><span class="sxs-lookup"><span data-stu-id="e8e66-187">If the control supports the [**IsEnabled**](uiauto-automation-element-propids.md) property, it must support this event.</span></span>   |
| <span data-ttu-id="e8e66-188">[**UIA \_**](uiauto-automation-element-propids.md) Событие изменения свойства исоффскринпропертид.</span><span class="sxs-lookup"><span data-stu-id="e8e66-188">[**UIA\_IsOffscreenPropertyId**](uiauto-automation-element-propids.md) property-changed event.</span></span>             | <span data-ttu-id="e8e66-189">Если элемент управления поддерживает свойство [**исоффскрин**](uiauto-automation-element-propids.md) , он должен поддерживать это событие.</span><span class="sxs-lookup"><span data-stu-id="e8e66-189">If the control supports the [**IsOffscreen**](uiauto-automation-element-propids.md) property, it must support this event.</span></span> |
| [<span data-ttu-id="e8e66-190">**UIA \_ структуречанжедевентид**</span><span class="sxs-lookup"><span data-stu-id="e8e66-190">**UIA\_StructureChangedEventId**</span></span>](uiauto-event-ids.md)                                                  |                                                                                                                            |



 

## <a name="related-topics"></a><span data-ttu-id="e8e66-191">См. также</span><span class="sxs-lookup"><span data-stu-id="e8e66-191">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="e8e66-192">**Зрения**</span><span class="sxs-lookup"><span data-stu-id="e8e66-192">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="e8e66-193">Общие сведения о типах элементов управления автоматизации пользовательского интерфейса</span><span class="sxs-lookup"><span data-stu-id="e8e66-193">UI Automation Control Types Overview</span></span>](uiauto-controltypesoverview.md)
</dt> <dt>

[<span data-ttu-id="e8e66-194">Общие сведения о модели автоматизации пользовательского интерфейса</span><span class="sxs-lookup"><span data-stu-id="e8e66-194">UI Automation Overview</span></span>](uiauto-uiautomationoverview.md)
</dt> </dl>

 

 




