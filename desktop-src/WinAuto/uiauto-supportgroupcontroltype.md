---
title: Тип элемента управления Group
description: В этом разделе содержатся сведения о поддержке автоматизации пользовательского интерфейса Майкрософт для типа элемента управления Group.
ms.assetid: f8363c2f-dbff-43a3-831f-d30151829ef9
keywords:
- Модель автоматизации пользовательского интерфейса, поддержка типа управления группой
- Модель автоматизации пользовательского интерфейса, тип элемента управления Group
- Модель автоматизации пользовательского интерфейса, древовидная структура для типа элемента управления Group
- Модель автоматизации пользовательского интерфейса, свойства для типа элемента управления Group
- Модель автоматизации пользовательского интерфейса, шаблоны элементов управления для типа элемента управления Group
- Модель автоматизации пользовательского интерфейса, события для типа управления группой
- Древовидные структуры, тип элемента управления Group
- свойства, тип элемента управления Group
- шаблоны элементов управления, тип элемента управления Group
- события, тип элемента управления Group
- Поддержка типа управления группой
- Тип контрольного элемента "Группа"
- типы элементов управления, древовидная структура для типа элемента управления Group
- типы элементов управления, шаблоны элементов управления для типа элемента управления Group
- типы элементов управления, поддержка групп
- типы элементов управления, Группа
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 44b630d0ef736d937e4f024c8131adc4c843b6e4
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104410887"
---
# <a name="group-control-type"></a><span data-ttu-id="6a273-119">Тип элемента управления Group</span><span class="sxs-lookup"><span data-stu-id="6a273-119">Group Control Type</span></span>

<span data-ttu-id="6a273-120">В этом разделе содержатся сведения о поддержке автоматизации пользовательского интерфейса Майкрософт для типа элемента управления **Group** .</span><span class="sxs-lookup"><span data-stu-id="6a273-120">This topic provides information about Microsoft UI Automation support for the **Group** control type.</span></span>

<span data-ttu-id="6a273-121">Элемент управления "Группа" представляет узел в иерархии.</span><span class="sxs-lookup"><span data-stu-id="6a273-121">A group control represents a node within a hierarchy.</span></span> <span data-ttu-id="6a273-122">Тип элемента управления **Group** создает разделение в дереве модели автоматизации пользовательского интерфейса, чтобы элементы, сгруппированные вместе, имели логическое деление в дереве модели автоматизации пользовательского интерфейса.</span><span class="sxs-lookup"><span data-stu-id="6a273-122">The **Group** control type creates a separation in the UI Automation tree so items that are grouped together have a logical division within the UI Automation tree.</span></span>

<span data-ttu-id="6a273-123">В следующих разделах определяется необходимая древовидная структура модели автоматизации пользовательского интерфейса, свойства, шаблоны элементов управления и события для типа элемента управления **Group** .</span><span class="sxs-lookup"><span data-stu-id="6a273-123">The following sections define the required UI Automation tree structure, properties, control patterns, and events for the **Group** control type.</span></span> <span data-ttu-id="6a273-124">Требования к автоматизации пользовательского интерфейса применяются ко всем элементам управления "Группа", в которых платформа или платформа пользовательского интерфейса интегрирует поддержку модели автоматизации пользовательского интерфейса для типов элементов управления и шаблонов элементов управления.</span><span class="sxs-lookup"><span data-stu-id="6a273-124">The UI Automation requirements apply to all group controls where the UI framework/platform integrates UI Automation support for control types and control patterns.</span></span>

<span data-ttu-id="6a273-125">В этом разделе содержатся следующие подразделы.</span><span class="sxs-lookup"><span data-stu-id="6a273-125">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="6a273-126">Типичная древовидная структура</span><span class="sxs-lookup"><span data-stu-id="6a273-126">Typical Tree Structure</span></span>](#typical-tree-structure)
-   [<span data-ttu-id="6a273-127">Соответствующие свойства</span><span class="sxs-lookup"><span data-stu-id="6a273-127">Relevant Properties</span></span>](#relevant-properties)
-   [<span data-ttu-id="6a273-128">Обязательные шаблоны элементов управления</span><span class="sxs-lookup"><span data-stu-id="6a273-128">Required Control Patterns</span></span>](#required-control-patterns)
-   [<span data-ttu-id="6a273-129">Обязательные события</span><span class="sxs-lookup"><span data-stu-id="6a273-129">Required Events</span></span>](#required-events)
-   [<span data-ttu-id="6a273-130">См. также</span><span class="sxs-lookup"><span data-stu-id="6a273-130">Related topics</span></span>](#related-topics)

## <a name="typical-tree-structure"></a><span data-ttu-id="6a273-131">Типичная древовидная структура</span><span class="sxs-lookup"><span data-stu-id="6a273-131">Typical Tree Structure</span></span>

<span data-ttu-id="6a273-132">В следующей таблице описывается типичный элемент управления и представление содержимого дерева модели автоматизации пользовательского интерфейса, которое относится к элементам управления "Группа" и описывает, что может содержаться в каждом представлении.</span><span class="sxs-lookup"><span data-stu-id="6a273-132">The following table depicts a typical control and content view of the UI Automation tree that pertains to group controls and describes what can be contained in each view.</span></span> <span data-ttu-id="6a273-133">Дополнительные сведения о дереве автоматизации пользовательского интерфейса см. в разделе [Общие сведения о дереве модели автоматизации пользовательского интерфейса](uiauto-treeoverview.md).</span><span class="sxs-lookup"><span data-stu-id="6a273-133">For more information about the UI Automation tree, see [UI Automation Tree Overview](uiauto-treeoverview.md).</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="6a273-134">Представление элемента управления</span><span class="sxs-lookup"><span data-stu-id="6a273-134">Control View</span></span></th>
<th><span data-ttu-id="6a273-135">Представление содержимого</span><span class="sxs-lookup"><span data-stu-id="6a273-135">Content View</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><ul>
<li><span data-ttu-id="6a273-136">Группа</span><span class="sxs-lookup"><span data-stu-id="6a273-136">Group</span></span>
<ul>
<li><span data-ttu-id="6a273-137">0 или несколько элементов управления</span><span class="sxs-lookup"><span data-stu-id="6a273-137">0 or many controls</span></span></li>
</ul></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="6a273-138">Группа</span><span class="sxs-lookup"><span data-stu-id="6a273-138">Group</span></span>
<ul>
<li><span data-ttu-id="6a273-139">0 или несколько элементов управления</span><span class="sxs-lookup"><span data-stu-id="6a273-139">0 or many controls</span></span></li>
</ul></li>
</ul></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="6a273-140">Элементы управления "Группа" обычно включают поддержку автоматизации пользовательского интерфейса для типов элементов управления, обнаруженных под ними в поддереве, включая типы [ListItem](uiauto-supportlistitemcontroltype.md), [TreeItem](uiauto-supporttreeitemcontroltype.md)и [DataItem](uiauto-supportdataitemcontroltype.md) .</span><span class="sxs-lookup"><span data-stu-id="6a273-140">Group controls typically include UI Automation support for control types found below them in the subtree, including the [ListItem](uiauto-supportlistitemcontroltype.md), [TreeItem](uiauto-supporttreeitemcontroltype.md), and [DataItem](uiauto-supportdataitemcontroltype.md) control types.</span></span> <span data-ttu-id="6a273-141">Поскольку элемент управления "Группа" является универсальным контейнером, любой тип элемента управления может находиться под элементом управления "Группа" в дереве.</span><span class="sxs-lookup"><span data-stu-id="6a273-141">Because a group control is a generic container, it is possible for any type of control to be under the group control in the tree.</span></span>

## <a name="relevant-properties"></a><span data-ttu-id="6a273-142">Соответствующие свойства</span><span class="sxs-lookup"><span data-stu-id="6a273-142">Relevant Properties</span></span>

<span data-ttu-id="6a273-143">В следующей таблице перечислены свойства модели автоматизации пользовательского интерфейса, значение или определение которых особенно важно для элементов управления группы.</span><span class="sxs-lookup"><span data-stu-id="6a273-143">The following table lists the UI Automation properties whose value or definition is especially relevant to the group controls.</span></span> <span data-ttu-id="6a273-144">Дополнительные сведения о свойствах модели автоматизации пользовательского интерфейса см. в разделе [Получение свойств элементов модели автоматизации пользовательского интерфейса](uiauto-propertiesforclients.md).</span><span class="sxs-lookup"><span data-stu-id="6a273-144">For more information about UI Automation properties, see [Retrieving Properties from UI Automation Elements](uiauto-propertiesforclients.md).</span></span>



| <span data-ttu-id="6a273-145">Свойство модели автоматизации пользовательского интерфейса</span><span class="sxs-lookup"><span data-stu-id="6a273-145">UI Automation Property</span></span>                                                                                              | <span data-ttu-id="6a273-146">Значение</span><span class="sxs-lookup"><span data-stu-id="6a273-146">Value</span></span>      | <span data-ttu-id="6a273-147">Примечания</span><span class="sxs-lookup"><span data-stu-id="6a273-147">Notes</span></span>                                                                                                                                                                                                |
|---------------------------------------------------------------------------------------------------------------------|------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="6a273-148">**UIA \_ аутоматионидпропертид**</span><span class="sxs-lookup"><span data-stu-id="6a273-148">**UIA\_AutomationIdPropertyId**</span></span>](uiauto-automation-element-propids.md)                 | <span data-ttu-id="6a273-149">См. примечания.</span><span class="sxs-lookup"><span data-stu-id="6a273-149">See notes.</span></span> | <span data-ttu-id="6a273-150">Значение этого свойства должно быть уникальным среди всех одноранговых элементов в необработанном представлении дерева модели автоматизации пользовательского интерфейса.</span><span class="sxs-lookup"><span data-stu-id="6a273-150">The value of this property must be unique among all peer elements in the raw view of the UI Automation tree.</span></span>                                                                                         |
| [<span data-ttu-id="6a273-151">**UIA \_ баундингректанглепропертид**</span><span class="sxs-lookup"><span data-stu-id="6a273-151">**UIA\_BoundingRectanglePropertyId**</span></span>](uiauto-automation-element-propids.md)       | <span data-ttu-id="6a273-152">См. примечания.</span><span class="sxs-lookup"><span data-stu-id="6a273-152">See notes.</span></span> | <span data-ttu-id="6a273-153">Внешний прямоугольник, содержащий весь элемент управления.</span><span class="sxs-lookup"><span data-stu-id="6a273-153">The outermost rectangle that contains the whole control.</span></span>                                                                                                                                             |
| [<span data-ttu-id="6a273-154">**UIA \_ кликкаблепоинтпропертид**</span><span class="sxs-lookup"><span data-stu-id="6a273-154">**UIA\_ClickablePointPropertyId**</span></span>](uiauto-automation-element-propids.md)             | <span data-ttu-id="6a273-155">См. примечания.</span><span class="sxs-lookup"><span data-stu-id="6a273-155">See notes.</span></span> | <span data-ttu-id="6a273-156">Поддерживается при наличии ограничивающего прямоугольника.</span><span class="sxs-lookup"><span data-stu-id="6a273-156">Supported if there is a bounding rectangle.</span></span> <span data-ttu-id="6a273-157">Если не все точки внутри ограничивающего прямоугольника являются щелчками, а элемент выполняет специализированное тестирование нажатия, переопределите и предоставьте точку для щелчка.</span><span class="sxs-lookup"><span data-stu-id="6a273-157">If not every point within the bounding rectangle is clickable, and the element performs specialized hit testing, override and provide a clickable point.</span></span> |
| [<span data-ttu-id="6a273-158">**UIA \_ контролтипепропертид**</span><span class="sxs-lookup"><span data-stu-id="6a273-158">**UIA\_ControlTypePropertyId**</span></span>](uiauto-automation-element-propids.md)                   | <span data-ttu-id="6a273-159">**Группа**</span><span class="sxs-lookup"><span data-stu-id="6a273-159">**Group**</span></span>  |                                                                                                                                                                                                      |
| [<span data-ttu-id="6a273-160">**UIA \_ исконтентелементпропертид**</span><span class="sxs-lookup"><span data-stu-id="6a273-160">**UIA\_IsContentElementPropertyId**</span></span>](uiauto-automation-element-propids.md)         | <span data-ttu-id="6a273-161">**TRUE**</span><span class="sxs-lookup"><span data-stu-id="6a273-161">**TRUE**</span></span>   | <span data-ttu-id="6a273-162">Элемент управления "Группа" всегда включается в представление содержимого дерева модели автоматизации пользовательского интерфейса.</span><span class="sxs-lookup"><span data-stu-id="6a273-162">The group control is always included in the content view of the UI Automation tree.</span></span>                                                                                                                  |
| [<span data-ttu-id="6a273-163">**UIA \_ исконтролелементпропертид**</span><span class="sxs-lookup"><span data-stu-id="6a273-163">**UIA\_IsControlElementPropertyId**</span></span>](uiauto-automation-element-propids.md)         | <span data-ttu-id="6a273-164">**TRUE**</span><span class="sxs-lookup"><span data-stu-id="6a273-164">**TRUE**</span></span>   | <span data-ttu-id="6a273-165">Элемент управления "Группа" всегда включается в представление элемента управления дерева модели автоматизации пользовательского интерфейса.</span><span class="sxs-lookup"><span data-stu-id="6a273-165">The group control is always included in the control view of the UI Automation tree.</span></span>                                                                                                                  |
| [<span data-ttu-id="6a273-166">**UIA \_ искэйбоардфокусаблепропертид**</span><span class="sxs-lookup"><span data-stu-id="6a273-166">**UIA\_IsKeyboardFocusablePropertyId**</span></span>](uiauto-automation-element-propids.md)   | <span data-ttu-id="6a273-167">См. примечания.</span><span class="sxs-lookup"><span data-stu-id="6a273-167">See notes.</span></span> | <span data-ttu-id="6a273-168">Если элемент управления может получать фокус клавиатуры, он должен поддерживать это свойство.</span><span class="sxs-lookup"><span data-stu-id="6a273-168">If the control can receive keyboard focus, it must support this property.</span></span>                                                                                                                            |
| [<span data-ttu-id="6a273-169">**UIA \_ лабеледбипропертид**</span><span class="sxs-lookup"><span data-stu-id="6a273-169">**UIA\_LabeledByPropertyId**</span></span>](uiauto-automation-element-propids.md)                       | <span data-ttu-id="6a273-170">См. примечания.</span><span class="sxs-lookup"><span data-stu-id="6a273-170">See notes.</span></span> | <span data-ttu-id="6a273-171">Обычно элементы управления "Группа" получают метки автоматически.</span><span class="sxs-lookup"><span data-stu-id="6a273-171">Group controls are typically self-labeling.</span></span> <span data-ttu-id="6a273-172">В этих случаях возвращается **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="6a273-172">In these cases, return **NULL**.</span></span> <span data-ttu-id="6a273-173">Если у группы есть статическая текстовая метка, то следует вернуть метку в качестве значения свойства **лабеледби** .</span><span class="sxs-lookup"><span data-stu-id="6a273-173">If the group has a static text label, return the label as the value of the **LabeledBy** property.</span></span>                      |
| [<span data-ttu-id="6a273-174">**UIA \_ локализедконтролтипепропертид**</span><span class="sxs-lookup"><span data-stu-id="6a273-174">**UIA\_LocalizedControlTypePropertyId**</span></span>](uiauto-automation-element-propids.md) | <span data-ttu-id="6a273-175">См. примечания.</span><span class="sxs-lookup"><span data-stu-id="6a273-175">See notes.</span></span> | <span data-ttu-id="6a273-176">Локализованная строка, соответствующая типу элемента управления **Group** .</span><span class="sxs-lookup"><span data-stu-id="6a273-176">Localized string corresponding to the **Group** control type.</span></span> <span data-ttu-id="6a273-177">Значение по умолчанию — "Group" для en-US или English (США).</span><span class="sxs-lookup"><span data-stu-id="6a273-177">The default value is "group" for en-US or English (United States).</span></span>                                                                     |
| [<span data-ttu-id="6a273-178">**UIA \_ намепропертид**</span><span class="sxs-lookup"><span data-stu-id="6a273-178">**UIA\_NamePropertyId**</span></span>](uiauto-automation-element-propids.md)                                 | <span data-ttu-id="6a273-179">См. примечания.</span><span class="sxs-lookup"><span data-stu-id="6a273-179">See notes.</span></span> | <span data-ttu-id="6a273-180">Элемент управления "Группа" обычно получает свое имя из текста метки элемента управления.</span><span class="sxs-lookup"><span data-stu-id="6a273-180">The group control typically gets its name from the text that labels the control.</span></span>                                                                                                                     |



 

## <a name="required-control-patterns"></a><span data-ttu-id="6a273-181">Обязательные шаблоны элементов управления</span><span class="sxs-lookup"><span data-stu-id="6a273-181">Required Control Patterns</span></span>

<span data-ttu-id="6a273-182">В следующей таблице перечислены шаблоны элементов управления модели автоматизации пользовательского интерфейса, которые должны поддерживаться для типа элемента управления **Group** .</span><span class="sxs-lookup"><span data-stu-id="6a273-182">The following table lists the UI Automation control patterns required to be supported for the **Group** control type.</span></span> <span data-ttu-id="6a273-183">Дополнительные сведения о шаблонах элементов управления см. в разделе [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md).</span><span class="sxs-lookup"><span data-stu-id="6a273-183">For more information on control patterns, see [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md).</span></span>



| <span data-ttu-id="6a273-184">Шаблон элемента управления</span><span class="sxs-lookup"><span data-stu-id="6a273-184">Control Pattern</span></span>                                                   | <span data-ttu-id="6a273-185">Поддержка</span><span class="sxs-lookup"><span data-stu-id="6a273-185">Support</span></span> | <span data-ttu-id="6a273-186">Примечания</span><span class="sxs-lookup"><span data-stu-id="6a273-186">Notes</span></span>                                                                                                                                                 |
|-------------------------------------------------------------------|---------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="6a273-187">**IExpandCollapseProvider**</span><span class="sxs-lookup"><span data-stu-id="6a273-187">**IExpandCollapseProvider**</span></span>](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iexpandcollapseprovider) | <span data-ttu-id="6a273-188">Зависит</span><span class="sxs-lookup"><span data-stu-id="6a273-188">Depends</span></span> | <span data-ttu-id="6a273-189">Элементы управления группы, которые могут использоваться для отображения или скрытия информации, должны поддерживать шаблон элемента управления [ExpandCollapse](uiauto-implementingexpandcollapse.md) .</span><span class="sxs-lookup"><span data-stu-id="6a273-189">Group controls that can be used to show or hide information must support the [ExpandCollapse](uiauto-implementingexpandcollapse.md) control pattern.</span></span> |



 

## <a name="required-events"></a><span data-ttu-id="6a273-190">Обязательные события</span><span class="sxs-lookup"><span data-stu-id="6a273-190">Required Events</span></span>

<span data-ttu-id="6a273-191">В следующей таблице перечислены события автоматизации пользовательского интерфейса, которые требуются для поддержки элементов управления группы.</span><span class="sxs-lookup"><span data-stu-id="6a273-191">The following table lists the UI Automation events that group controls are required to support.</span></span> <span data-ttu-id="6a273-192">Дополнительные сведения о событиях см. в разделе [UI Automation Events Overview](uiauto-eventsoverview.md).</span><span class="sxs-lookup"><span data-stu-id="6a273-192">For more information on events, see [UI Automation Events Overview](uiauto-eventsoverview.md).</span></span>



| <span data-ttu-id="6a273-193">Событие автоматизации пользовательского интерфейса</span><span class="sxs-lookup"><span data-stu-id="6a273-193">UI Automation Event</span></span>                                                                                                                                                | <span data-ttu-id="6a273-194">Примечания</span><span class="sxs-lookup"><span data-stu-id="6a273-194">Notes</span></span>                                                                                                                                            |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="6a273-195">**UIA \_ аутоматионфокусчанжедевентид**</span><span class="sxs-lookup"><span data-stu-id="6a273-195">**UIA\_AutomationFocusChangedEventId**</span></span>](uiauto-event-ids.md)                                                                   |                                                                                                                                                  |
| <span data-ttu-id="6a273-196">[**UIA \_**](uiauto-automation-element-propids.md) Событие изменения свойства баундингректанглепропертид.</span><span class="sxs-lookup"><span data-stu-id="6a273-196">[**UIA\_BoundingRectanglePropertyId**](uiauto-automation-element-propids.md) property-changed event.</span></span>                              |                                                                                                                                                  |
| <span data-ttu-id="6a273-197">[**UIA \_**](uiauto-control-pattern-propids.md) Событие изменения свойства експандколлапсикспандколлапсестатепропертид.</span><span class="sxs-lookup"><span data-stu-id="6a273-197">[**UIA\_ExpandCollapseExpandCollapseStatePropertyId**](uiauto-control-pattern-propids.md) property-changed event.</span></span> | <span data-ttu-id="6a273-198">Если элемент управления поддерживает шаблон элемента управления шаблон элемента управления [ExpandCollapse](uiauto-implementingexpandcollapse.md) , он должен поддерживать это событие.</span><span class="sxs-lookup"><span data-stu-id="6a273-198">If the control supports the [ExpandCollapse](uiauto-implementingexpandcollapse.md) control pattern control pattern, it must support this event.</span></span> |
| <span data-ttu-id="6a273-199">[**UIA \_**](uiauto-automation-element-propids.md) Событие изменения свойства исенабледпропертид.</span><span class="sxs-lookup"><span data-stu-id="6a273-199">[**UIA\_IsEnabledPropertyId**](uiauto-automation-element-propids.md) property-changed event.</span></span>                                              | <span data-ttu-id="6a273-200">Если элемент управления поддерживает свойство « [**включено**](uiauto-automation-element-propids.md) », оно должно поддерживать это событие.</span><span class="sxs-lookup"><span data-stu-id="6a273-200">If the control supports the [**IsEnabled**](uiauto-automation-element-propids.md) property, it must support this event.</span></span>                         |
| <span data-ttu-id="6a273-201">[**UIA \_**](uiauto-automation-element-propids.md) Событие изменения свойства исоффскринпропертид.</span><span class="sxs-lookup"><span data-stu-id="6a273-201">[**UIA\_IsOffscreenPropertyId**](uiauto-automation-element-propids.md) property-changed event.</span></span>                                          | <span data-ttu-id="6a273-202">Если элемент управления поддерживает свойство [**исоффскрин**](uiauto-automation-element-propids.md) , он должен поддерживать это событие.</span><span class="sxs-lookup"><span data-stu-id="6a273-202">If the control supports the [**IsOffscreen**](uiauto-automation-element-propids.md) property, it must support this event.</span></span>                       |
| <span data-ttu-id="6a273-203">[**UIA \_**](uiauto-control-pattern-propids.md) Событие изменения свойства тогглетогглестатепропертид.</span><span class="sxs-lookup"><span data-stu-id="6a273-203">[**UIA\_ToggleToggleStatePropertyId**](uiauto-control-pattern-propids.md) property-changed event.</span></span>                                 | <span data-ttu-id="6a273-204">Если элемент управления поддерживает шаблон элемента управления [Toggle](uiauto-implementingtoggle.md) , он должен поддерживать это событие.</span><span class="sxs-lookup"><span data-stu-id="6a273-204">If the control supports the [Toggle](uiauto-implementingtoggle.md) control pattern, it must support this event.</span></span>                                 |
| [<span data-ttu-id="6a273-205">**UIA \_ структуречанжедевентид**</span><span class="sxs-lookup"><span data-stu-id="6a273-205">**UIA\_StructureChangedEventId**</span></span>](uiauto-event-ids.md)                                                                               |                                                                                                                                                  |



 

## <a name="related-topics"></a><span data-ttu-id="6a273-206">См. также</span><span class="sxs-lookup"><span data-stu-id="6a273-206">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="6a273-207">**Зрения**</span><span class="sxs-lookup"><span data-stu-id="6a273-207">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="6a273-208">Общие сведения о типах элементов управления автоматизации пользовательского интерфейса</span><span class="sxs-lookup"><span data-stu-id="6a273-208">UI Automation Control Types Overview</span></span>](uiauto-controltypesoverview.md)
</dt> <dt>

[<span data-ttu-id="6a273-209">Общие сведения о модели автоматизации пользовательского интерфейса</span><span class="sxs-lookup"><span data-stu-id="6a273-209">UI Automation Overview</span></span>](uiauto-uiautomationoverview.md)
</dt> </dl>

 

 




