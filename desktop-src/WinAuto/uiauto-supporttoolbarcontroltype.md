---
title: Тип элемента управления ToolBar
description: В этом разделе содержатся сведения о поддержке автоматизации пользовательского интерфейса Майкрософт для типа элемента управления ToolBar. Элементы управления ToolBar позволяют конечным пользователям активировать команды и средства, содержащиеся в приложении.
ms.assetid: e2a72ce3-5263-43f8-be4d-715a78224b68
keywords:
- Модель автоматизации пользовательского интерфейса, поддержка типа элемента управления ToolBar
- Модель автоматизации пользовательского интерфейса, тип элемента управления ToolBar
- Модель автоматизации пользовательского интерфейса, структура дерева для типа элемента управления ToolBar
- Модель автоматизации пользовательского интерфейса, свойства для типа элемента управления ToolBar
- Модель автоматизации пользовательского интерфейса, шаблоны элементов управления для типа элемента управления ToolBar
- Модель автоматизации пользовательского интерфейса, события для типа элемента управления ToolBar
- Древовидные структуры, тип элемента управления ToolBar
- свойства, тип элемента управления ToolBar
- шаблоны элементов управления, тип элемента управления ToolBar
- события, тип элемента управления ToolBar
- Поддержка типа элемента управления ToolBar
- ToolBar - тип элемента управления
- типы элементов управления, древовидная структура для типа элемента управления ToolBar
- типы элементов управления, шаблоны элементов управления для типа элемента ToolBar
- типы элементов управления, поддержка панели инструментов
- типы элементов управления, панель инструментов
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4327c187a86ace6f02b93082675c345eae4d4edf
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104411329"
---
# <a name="toolbar-control-type"></a><span data-ttu-id="26ab1-120">Тип элемента управления ToolBar</span><span class="sxs-lookup"><span data-stu-id="26ab1-120">ToolBar Control Type</span></span>

<span data-ttu-id="26ab1-121">В этом разделе содержатся сведения о поддержке автоматизации пользовательского интерфейса Майкрософт для типа элемента управления **Toolbar** .</span><span class="sxs-lookup"><span data-stu-id="26ab1-121">This topic provides information about Microsoft UI Automation support for the **ToolBar** control type.</span></span> <span data-ttu-id="26ab1-122">Элементы управления ToolBar позволяют конечным пользователям активировать команды и средства, содержащиеся в приложении.</span><span class="sxs-lookup"><span data-stu-id="26ab1-122">Toolbar controls enable end users to activate commands and tools contained within a application.</span></span>

<span data-ttu-id="26ab1-123">В следующих разделах определяется необходимая древовидная структура модели автоматизации пользовательского интерфейса, свойства, шаблоны элементов управления и события для типа элемента управления **Toolbar** .</span><span class="sxs-lookup"><span data-stu-id="26ab1-123">The following sections define the required UI Automation tree structure, properties, control patterns, and events for the **ToolBar** control type.</span></span> <span data-ttu-id="26ab1-124">Требования к автоматизации пользовательского интерфейса применяются ко всем элементам управления ToolBar, в которых платформа или платформа пользовательского интерфейса интегрирует поддержку модели автоматизации пользовательского интерфейса для типов элементов управления и шаблонов элементов управления.</span><span class="sxs-lookup"><span data-stu-id="26ab1-124">The UI Automation requirements apply to all toolbar controls where the UI framework/platform integrates UI Automation support for control types and control patterns.</span></span>

<span data-ttu-id="26ab1-125">В этом разделе содержатся следующие подразделы.</span><span class="sxs-lookup"><span data-stu-id="26ab1-125">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="26ab1-126">Типичная древовидная структура</span><span class="sxs-lookup"><span data-stu-id="26ab1-126">Typical Tree Structure</span></span>](#typical-tree-structure)
-   [<span data-ttu-id="26ab1-127">Соответствующие свойства</span><span class="sxs-lookup"><span data-stu-id="26ab1-127">Relevant Properties</span></span>](#relevant-properties)
-   [<span data-ttu-id="26ab1-128">Обязательные шаблоны элементов управления</span><span class="sxs-lookup"><span data-stu-id="26ab1-128">Required Control Patterns</span></span>](#required-control-patterns)
-   [<span data-ttu-id="26ab1-129">Обязательные события</span><span class="sxs-lookup"><span data-stu-id="26ab1-129">Required Events</span></span>](#required-events)
-   [<span data-ttu-id="26ab1-130">См. также</span><span class="sxs-lookup"><span data-stu-id="26ab1-130">Related topics</span></span>](#related-topics)

## <a name="typical-tree-structure"></a><span data-ttu-id="26ab1-131">Типичная древовидная структура</span><span class="sxs-lookup"><span data-stu-id="26ab1-131">Typical Tree Structure</span></span>

<span data-ttu-id="26ab1-132">В следующей таблице описывается типичный элемент управления и представление содержимого дерева модели автоматизации пользовательского интерфейса, которое относится к элементам управления Toolbar и описывает, что может содержаться в каждом представлении.</span><span class="sxs-lookup"><span data-stu-id="26ab1-132">The following table depicts a typical control and content view of the UI Automation tree that pertains to toolbar controls and describes what can be contained in each view.</span></span> <span data-ttu-id="26ab1-133">Дополнительные сведения о дереве автоматизации пользовательского интерфейса см. в разделе [Общие сведения о дереве модели автоматизации пользовательского интерфейса](uiauto-treeoverview.md).</span><span class="sxs-lookup"><span data-stu-id="26ab1-133">For more information about the UI Automation tree, see [UI Automation Tree Overview](uiauto-treeoverview.md).</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="26ab1-134">Представление элемента управления</span><span class="sxs-lookup"><span data-stu-id="26ab1-134">Control View</span></span></th>
<th><span data-ttu-id="26ab1-135">Представление содержимого</span><span class="sxs-lookup"><span data-stu-id="26ab1-135">Content View</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><ul>
<li><span data-ttu-id="26ab1-136">ToolBar</span><span class="sxs-lookup"><span data-stu-id="26ab1-136">ToolBar</span></span>
<ul>
<li><span data-ttu-id="26ab1-137">Различные элементы управления (0 или более)</span><span class="sxs-lookup"><span data-stu-id="26ab1-137">Various controls (0 or more)</span></span></li>
</ul></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="26ab1-138">ToolBar</span><span class="sxs-lookup"><span data-stu-id="26ab1-138">ToolBar</span></span>
<ul>
<li><span data-ttu-id="26ab1-139">Различные элементы управления (0 или более)</span><span class="sxs-lookup"><span data-stu-id="26ab1-139">Various controls (0 or more)</span></span></li>
</ul></li>
</ul></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="26ab1-140">Элемент управления ToolBar может содержать элементы управления любого типа в поддереве.</span><span class="sxs-lookup"><span data-stu-id="26ab1-140">A toolbar control can contain any type of control within its subtree.</span></span> <span data-ttu-id="26ab1-141">Чаще всего они содержат кнопки, поля со списком и разворачивающиеся кнопки.</span><span class="sxs-lookup"><span data-stu-id="26ab1-141">They most often contain buttons, combo boxes, and split buttons.</span></span>

## <a name="relevant-properties"></a><span data-ttu-id="26ab1-142">Соответствующие свойства</span><span class="sxs-lookup"><span data-stu-id="26ab1-142">Relevant Properties</span></span>

<span data-ttu-id="26ab1-143">В следующей таблице перечислены свойства модели автоматизации пользовательского интерфейса, значения или определения которых особенно важны для типа элемента управления **Toolbar** .</span><span class="sxs-lookup"><span data-stu-id="26ab1-143">The following table lists the UI Automation properties whose value or definition is especially relevant to the **ToolBar** control type.</span></span> <span data-ttu-id="26ab1-144">Дополнительные сведения о свойствах модели автоматизации пользовательского интерфейса см. в разделе [Получение свойств элементов модели автоматизации пользовательского интерфейса](uiauto-propertiesforclients.md).</span><span class="sxs-lookup"><span data-stu-id="26ab1-144">For more information about UI Automation properties, see [Retrieving Properties from UI Automation Elements](uiauto-propertiesforclients.md).</span></span>



| <span data-ttu-id="26ab1-145">Свойство модели автоматизации пользовательского интерфейса</span><span class="sxs-lookup"><span data-stu-id="26ab1-145">UI Automation Property</span></span>                                                                                              | <span data-ttu-id="26ab1-146">Значение</span><span class="sxs-lookup"><span data-stu-id="26ab1-146">Value</span></span>       | <span data-ttu-id="26ab1-147">Примечания</span><span class="sxs-lookup"><span data-stu-id="26ab1-147">Notes</span></span>                                                                                                                                                                                                      |
|---------------------------------------------------------------------------------------------------------------------|-------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="26ab1-148">**UIA \_ аутоматионидпропертид**</span><span class="sxs-lookup"><span data-stu-id="26ab1-148">**UIA\_AutomationIdPropertyId**</span></span>](uiauto-automation-element-propids.md)                 | <span data-ttu-id="26ab1-149">См. примечания.</span><span class="sxs-lookup"><span data-stu-id="26ab1-149">See notes.</span></span>  | <span data-ttu-id="26ab1-150">Значение этого свойства должно быть уникальным среди всех одноранговых элементов в необработанном представлении дерева модели автоматизации пользовательского интерфейса.</span><span class="sxs-lookup"><span data-stu-id="26ab1-150">The value of this property must be unique among all peer elements in the raw view of the UI Automation tree.</span></span>                                                                                               |
| [<span data-ttu-id="26ab1-151">**UIA \_ баундингректанглепропертид**</span><span class="sxs-lookup"><span data-stu-id="26ab1-151">**UIA\_BoundingRectanglePropertyId**</span></span>](uiauto-automation-element-propids.md)       | <span data-ttu-id="26ab1-152">См. примечания.</span><span class="sxs-lookup"><span data-stu-id="26ab1-152">See notes.</span></span>  | <span data-ttu-id="26ab1-153">Внешний прямоугольник, содержащий весь элемент управления.</span><span class="sxs-lookup"><span data-stu-id="26ab1-153">The outermost rectangle that contains the whole control.</span></span>                                                                                                                                                   |
| [<span data-ttu-id="26ab1-154">**UIA \_ кликкаблепоинтпропертид**</span><span class="sxs-lookup"><span data-stu-id="26ab1-154">**UIA\_ClickablePointPropertyId**</span></span>](uiauto-automation-element-propids.md)             | <span data-ttu-id="26ab1-155">См. примечания.</span><span class="sxs-lookup"><span data-stu-id="26ab1-155">See notes.</span></span>  | <span data-ttu-id="26ab1-156">Поддерживается при наличии ограничивающего прямоугольника.</span><span class="sxs-lookup"><span data-stu-id="26ab1-156">Supported if there is a bounding rectangle.</span></span> <span data-ttu-id="26ab1-157">Если не все точки внутри ограничивающего прямоугольника являются щелчками, а элемент выполняет специализированное тестирование нажатия, переопределите и предоставьте точку для щелчка.</span><span class="sxs-lookup"><span data-stu-id="26ab1-157">If not every point within the bounding rectangle is clickable, and the element performs specialized hit testing, override and provide a clickable point.</span></span>       |
| [<span data-ttu-id="26ab1-158">**UIA \_ контролтипепропертид**</span><span class="sxs-lookup"><span data-stu-id="26ab1-158">**UIA\_ControlTypePropertyId**</span></span>](uiauto-automation-element-propids.md)                   | <span data-ttu-id="26ab1-159">**Панелей**</span><span class="sxs-lookup"><span data-stu-id="26ab1-159">**ToolBar**</span></span> | <span data-ttu-id="26ab1-160">Это значение одинаково для всех инфраструктур пользовательского интерфейса.</span><span class="sxs-lookup"><span data-stu-id="26ab1-160">This value is the same for all UI frameworks.</span></span>                                                                                                                                                              |
| [<span data-ttu-id="26ab1-161">**UIA \_ исконтентелементпропертид**</span><span class="sxs-lookup"><span data-stu-id="26ab1-161">**UIA\_IsContentElementPropertyId**</span></span>](uiauto-automation-element-propids.md)         | <span data-ttu-id="26ab1-162">true</span><span class="sxs-lookup"><span data-stu-id="26ab1-162">TRUE</span></span>        | <span data-ttu-id="26ab1-163">Элемент управления ToolBar всегда включается в представление содержимого дерева модели автоматизации пользовательского интерфейса.</span><span class="sxs-lookup"><span data-stu-id="26ab1-163">The toolbar control is always included in the content view of the UI Automation tree.</span></span>                                                                                                                      |
| [<span data-ttu-id="26ab1-164">**UIA \_ исконтролелементпропертид**</span><span class="sxs-lookup"><span data-stu-id="26ab1-164">**UIA\_IsControlElementPropertyId**</span></span>](uiauto-automation-element-propids.md)         | <span data-ttu-id="26ab1-165">true</span><span class="sxs-lookup"><span data-stu-id="26ab1-165">TRUE</span></span>        | <span data-ttu-id="26ab1-166">Элемент управления ToolBar всегда включается в представление элемента управления дерева модели автоматизации пользовательского интерфейса.</span><span class="sxs-lookup"><span data-stu-id="26ab1-166">The toolbar control is always included in the control view of the UI Automation tree.</span></span>                                                                                                                      |
| [<span data-ttu-id="26ab1-167">**UIA \_ искэйбоардфокусаблепропертид**</span><span class="sxs-lookup"><span data-stu-id="26ab1-167">**UIA\_IsKeyboardFocusablePropertyId**</span></span>](uiauto-automation-element-propids.md)   | <span data-ttu-id="26ab1-168">См. примечания.</span><span class="sxs-lookup"><span data-stu-id="26ab1-168">See notes.</span></span>  | <span data-ttu-id="26ab1-169">Если элемент управления может получать фокус клавиатуры, он должен поддерживать это свойство.</span><span class="sxs-lookup"><span data-stu-id="26ab1-169">If the control can receive keyboard focus, it must support this property.</span></span>                                                                                                                                  |
| [<span data-ttu-id="26ab1-170">**UIA \_ лабеледбипропертид**</span><span class="sxs-lookup"><span data-stu-id="26ab1-170">**UIA\_LabeledByPropertyId**</span></span>](uiauto-automation-element-propids.md)                       | <span data-ttu-id="26ab1-171">NULL</span><span class="sxs-lookup"><span data-stu-id="26ab1-171">NULL</span></span>        | <span data-ttu-id="26ab1-172">Элемент управления ToolBar никогда не имеет метки.</span><span class="sxs-lookup"><span data-stu-id="26ab1-172">A toolbar control never has a label.</span></span>                                                                                                                                                                       |
| [<span data-ttu-id="26ab1-173">**UIA \_ локализедконтролтипепропертид**</span><span class="sxs-lookup"><span data-stu-id="26ab1-173">**UIA\_LocalizedControlTypePropertyId**</span></span>](uiauto-automation-element-propids.md) | <span data-ttu-id="26ab1-174">См. примечания.</span><span class="sxs-lookup"><span data-stu-id="26ab1-174">See notes.</span></span>  | <span data-ttu-id="26ab1-175">Локализованная строка, соответствующая типу элемента управления **Toolbar** .</span><span class="sxs-lookup"><span data-stu-id="26ab1-175">Localized string corresponding to the **ToolBar** control type.</span></span> <span data-ttu-id="26ab1-176">Значение по умолчанию — "панель инструментов" для en-US или English (США).</span><span class="sxs-lookup"><span data-stu-id="26ab1-176">The default value is "tool bar" for en-US or English (United States).</span></span>                                                                      |
| [<span data-ttu-id="26ab1-177">**UIA \_ намепропертид**</span><span class="sxs-lookup"><span data-stu-id="26ab1-177">**UIA\_NamePropertyId**</span></span>](uiauto-automation-element-propids.md)                                 | <span data-ttu-id="26ab1-178">Зависит</span><span class="sxs-lookup"><span data-stu-id="26ab1-178">Depends</span></span>     | <span data-ttu-id="26ab1-179">Элементу управления ToolBar не требуется имя, если только в приложении не используется более одного элемента.</span><span class="sxs-lookup"><span data-stu-id="26ab1-179">The toolbar control does not need a name unless more than one is used within an application.</span></span> <span data-ttu-id="26ab1-180">Если имеется несколько, каждое из них должно иметь отличительное имя (например, "Форматирование" или "структурирование").</span><span class="sxs-lookup"><span data-stu-id="26ab1-180">If more than one is present, each must have a distinguishing name (for example, "Formatting" or "Outlining").</span></span> |



 

## <a name="required-control-patterns"></a><span data-ttu-id="26ab1-181">Обязательные шаблоны элементов управления</span><span class="sxs-lookup"><span data-stu-id="26ab1-181">Required Control Patterns</span></span>

<span data-ttu-id="26ab1-182">В следующей таблице перечислены шаблоны элементов управления модели автоматизации пользовательского интерфейса, которые должны поддерживаться элементами управления ToolBar.</span><span class="sxs-lookup"><span data-stu-id="26ab1-182">The following table lists the UI Automation control patterns required to be supported by toolbar controls.</span></span> <span data-ttu-id="26ab1-183">Дополнительные сведения о шаблонах элементов управления см. в разделе [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md).</span><span class="sxs-lookup"><span data-stu-id="26ab1-183">For more information on control patterns, see [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md).</span></span>



| <span data-ttu-id="26ab1-184">Шаблон элемента управления</span><span class="sxs-lookup"><span data-stu-id="26ab1-184">Control Pattern</span></span>                                                   | <span data-ttu-id="26ab1-185">Поддержка</span><span class="sxs-lookup"><span data-stu-id="26ab1-185">Support</span></span> | <span data-ttu-id="26ab1-186">Примечания</span><span class="sxs-lookup"><span data-stu-id="26ab1-186">Notes</span></span>                                                                                                                                                         |
|-------------------------------------------------------------------|---------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="26ab1-187">**IDockProvider**</span><span class="sxs-lookup"><span data-stu-id="26ab1-187">**IDockProvider**</span></span>](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-idockprovider)                     | <span data-ttu-id="26ab1-188">Зависит</span><span class="sxs-lookup"><span data-stu-id="26ab1-188">Depends</span></span> | <span data-ttu-id="26ab1-189">Если панель инструментов может быть закреплена на разных частях экрана, она должна поддерживать шаблон элемента управления [Dock](uiauto-implementingdock.md) .</span><span class="sxs-lookup"><span data-stu-id="26ab1-189">If the toolbar can be docked to different parts of the screen, it must support the [Dock](uiauto-implementingdock.md) control pattern.</span></span>                       |
| [<span data-ttu-id="26ab1-190">**IExpandCollapseProvider**</span><span class="sxs-lookup"><span data-stu-id="26ab1-190">**IExpandCollapseProvider**</span></span>](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iexpandcollapseprovider) | <span data-ttu-id="26ab1-191">Зависит</span><span class="sxs-lookup"><span data-stu-id="26ab1-191">Depends</span></span> | <span data-ttu-id="26ab1-192">Если панель инструментов может быть развернута и свернута для отображения дополнительных элементов, она должна поддерживать шаблон элемента управления [ExpandCollapse](uiauto-implementingexpandcollapse.md) .</span><span class="sxs-lookup"><span data-stu-id="26ab1-192">If the toolbar can be expanded and collapsed to show more items, it must support the [ExpandCollapse](uiauto-implementingexpandcollapse.md) control pattern.</span></span> |
| [<span data-ttu-id="26ab1-193">**ITransformProvider**</span><span class="sxs-lookup"><span data-stu-id="26ab1-193">**ITransformProvider**</span></span>](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itransformprovider)           | <span data-ttu-id="26ab1-194">Зависит</span><span class="sxs-lookup"><span data-stu-id="26ab1-194">Depends</span></span> | <span data-ttu-id="26ab1-195">Если размер панели инструментов можно изменить, повернуть или переместить, он должен поддерживать шаблон элемента управления [Transform](uiauto-implementingtransform.md) .</span><span class="sxs-lookup"><span data-stu-id="26ab1-195">If the toolbar can be resized, rotated, or moved, it must support the [Transform](uiauto-implementingtransform.md) control pattern.</span></span>                          |



 

## <a name="required-events"></a><span data-ttu-id="26ab1-196">Обязательные события</span><span class="sxs-lookup"><span data-stu-id="26ab1-196">Required Events</span></span>

<span data-ttu-id="26ab1-197">В следующей таблице перечислены события автоматизации пользовательского интерфейса, которые должны поддерживаться элементами управления ToolBar.</span><span class="sxs-lookup"><span data-stu-id="26ab1-197">The following table lists the UI Automation events that toolbar controls are required to support.</span></span> <span data-ttu-id="26ab1-198">Дополнительные сведения о событиях см. в разделе [UI Automation Events Overview](uiauto-eventsoverview.md).</span><span class="sxs-lookup"><span data-stu-id="26ab1-198">For more information on events, see [UI Automation Events Overview](uiauto-eventsoverview.md).</span></span>



| <span data-ttu-id="26ab1-199">Событие автоматизации пользовательского интерфейса</span><span class="sxs-lookup"><span data-stu-id="26ab1-199">UI Automation Event</span></span>                                                                                                                                                | <span data-ttu-id="26ab1-200">Примечания</span><span class="sxs-lookup"><span data-stu-id="26ab1-200">Notes</span></span>                                                                                                                            |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="26ab1-201">**UIA \_ аутоматионфокусчанжедевентид**</span><span class="sxs-lookup"><span data-stu-id="26ab1-201">**UIA\_AutomationFocusChangedEventId**</span></span>](uiauto-event-ids.md)                                                                   |                                                                                                                                  |
| <span data-ttu-id="26ab1-202">[**UIA \_**](uiauto-automation-element-propids.md) Событие изменения свойства баундингректанглепропертид.</span><span class="sxs-lookup"><span data-stu-id="26ab1-202">[**UIA\_BoundingRectanglePropertyId**](uiauto-automation-element-propids.md) property-changed event.</span></span>                              |                                                                                                                                  |
| <span data-ttu-id="26ab1-203">[**UIA \_**](uiauto-control-pattern-propids.md) Событие изменения свойства експандколлапсикспандколлапсестатепропертид.</span><span class="sxs-lookup"><span data-stu-id="26ab1-203">[**UIA\_ExpandCollapseExpandCollapseStatePropertyId**](uiauto-control-pattern-propids.md) property-changed event.</span></span> | <span data-ttu-id="26ab1-204">Если элемент управления поддерживает шаблон элемента управления [ExpandCollapse](uiauto-implementingexpandcollapse.md) , он должен поддерживать это событие.</span><span class="sxs-lookup"><span data-stu-id="26ab1-204">If the control supports the [ExpandCollapse](uiauto-implementingexpandcollapse.md) control pattern, it must support this event.</span></span> |
| <span data-ttu-id="26ab1-205">[**UIA \_**](uiauto-automation-element-propids.md) Событие изменения свойства исенабледпропертид.</span><span class="sxs-lookup"><span data-stu-id="26ab1-205">[**UIA\_IsEnabledPropertyId**](uiauto-automation-element-propids.md) property-changed event.</span></span>                                              | <span data-ttu-id="26ab1-206">Если элемент управления поддерживает свойство « [**включено**](uiauto-automation-element-propids.md) », оно должно поддерживать это событие.</span><span class="sxs-lookup"><span data-stu-id="26ab1-206">If the control supports the [**IsEnabled**](uiauto-automation-element-propids.md) property, it must support this event.</span></span>         |
| <span data-ttu-id="26ab1-207">[**UIA \_**](uiauto-automation-element-propids.md) Событие изменения свойства исоффскринпропертид.</span><span class="sxs-lookup"><span data-stu-id="26ab1-207">[**UIA\_IsOffscreenPropertyId**](uiauto-automation-element-propids.md) property-changed event.</span></span>                                          | <span data-ttu-id="26ab1-208">Если элемент управления поддерживает свойство [**исоффскрин**](uiauto-automation-element-propids.md) , он должен поддерживать это событие.</span><span class="sxs-lookup"><span data-stu-id="26ab1-208">If the control supports the [**IsOffscreen**](uiauto-automation-element-propids.md) property, it must support this event.</span></span>       |
| [<span data-ttu-id="26ab1-209">**UIA \_ структуречанжедевентид**</span><span class="sxs-lookup"><span data-stu-id="26ab1-209">**UIA\_StructureChangedEventId**</span></span>](uiauto-event-ids.md)                                                                               |                                                                                                                                  |



 

## <a name="related-topics"></a><span data-ttu-id="26ab1-210">См. также</span><span class="sxs-lookup"><span data-stu-id="26ab1-210">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="26ab1-211">**Зрения**</span><span class="sxs-lookup"><span data-stu-id="26ab1-211">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="26ab1-212">Общие сведения о типах элементов управления автоматизации пользовательского интерфейса</span><span class="sxs-lookup"><span data-stu-id="26ab1-212">UI Automation Control Types Overview</span></span>](uiauto-controltypesoverview.md)
</dt> <dt>

[<span data-ttu-id="26ab1-213">Общие сведения о модели автоматизации пользовательского интерфейса</span><span class="sxs-lookup"><span data-stu-id="26ab1-213">UI Automation Overview</span></span>](uiauto-uiautomationoverview.md)
</dt> </dl>

 

 




