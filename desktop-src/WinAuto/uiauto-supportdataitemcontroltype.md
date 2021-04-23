---
title: Тип элемента управления DataItem
description: В этом разделе содержатся сведения о поддержке автоматизации пользовательского интерфейса Майкрософт для типа элемента управления DataItem.
ms.assetid: def52fe7-9f05-4cd0-8a46-af4e2e3ba03e
keywords:
- Модель автоматизации пользовательского интерфейса, поддержка типа элемента управления DataItem
- Модель автоматизации пользовательского интерфейса, тип элемента управления DataItem
- Модель автоматизации пользовательского интерфейса, древовидная структура для элемента управления DataItem
- Модель автоматизации пользовательского интерфейса, свойства для типа элемента управления DataItem
- Модель автоматизации пользовательского интерфейса, шаблоны элементов управления для типа DataItem
- Модель автоматизации пользовательского интерфейса, события для типа элемента управления DataItem
- Модель автоматизации пользовательского интерфейса, большие списки и тип элемента управления DataItem
- Древовидные структуры, тип элемента управления DataItem
- свойства, тип элемента управления DataItem
- шаблоны элементов управления, тип элемента управления DataItem
- события, тип элемента управления DataItem
- большие списки
- Поддержка типа элемента управления DataItem
- Тип элемента управления DataItem
- типы элементов управления, древовидная структура для элемента управления DataItem
- типы элементов управления, шаблоны элементов управления для типа DataItem
- типы элементов управления, большие списки и тип элемента управления DataItem
- типы элементов управления, поддержка DataItem
- типы элементов управления, DataItem
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f0902cc593ec7f9104ed27031caa2785b7cb9756
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104067869"
---
# <a name="dataitem-control-type"></a><span data-ttu-id="102d2-122">Тип элемента управления DataItem</span><span class="sxs-lookup"><span data-stu-id="102d2-122">DataItem Control Type</span></span>

<span data-ttu-id="102d2-123">В этом разделе содержатся сведения о поддержке автоматизации пользовательского интерфейса Майкрософт для типа элемента управления **DataItem** .</span><span class="sxs-lookup"><span data-stu-id="102d2-123">This topic provides information about Microsoft UI Automation support for the **DataItem** control type.</span></span>

<span data-ttu-id="102d2-124">Запись в списке контактов является примером элемента управления DataItem.</span><span class="sxs-lookup"><span data-stu-id="102d2-124">An entry in a Contacts list is an example of a data item control.</span></span> <span data-ttu-id="102d2-125">Элемент управления DataItem содержит сведения, представляющие интерес для конечного пользователя.</span><span class="sxs-lookup"><span data-stu-id="102d2-125">A data item control contains information that is of interest to an end user.</span></span> <span data-ttu-id="102d2-126">Он более сложный, чем обычный элемент списка, так как содержит более ценные сведения.</span><span class="sxs-lookup"><span data-stu-id="102d2-126">It is more complicated than the simple list item because it contains richer information.</span></span>

<span data-ttu-id="102d2-127">В следующих разделах определяется необходимая древовидная структура модели автоматизации пользовательского интерфейса, свойства, шаблоны элементов управления и события для типа элемента управления **DataItem** .</span><span class="sxs-lookup"><span data-stu-id="102d2-127">The following sections define the required UI Automation tree structure, properties, control patterns, and events for the **DataItem** control type.</span></span> <span data-ttu-id="102d2-128">Требования к автоматизации пользовательского интерфейса применяются ко всем элементам управления элементами данных, в которых платформа или платформа пользовательского интерфейса интегрирует поддержку автоматизации пользовательского интерфейса для типов элементов управления и шаблонов элементов управления.</span><span class="sxs-lookup"><span data-stu-id="102d2-128">The UI Automation requirements apply to all data item controls where the UI framework/platform integrates UI Automation support for control types and control patterns.</span></span>

<span data-ttu-id="102d2-129">В этом разделе содержатся следующие подразделы.</span><span class="sxs-lookup"><span data-stu-id="102d2-129">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="102d2-130">Типичная древовидная структура</span><span class="sxs-lookup"><span data-stu-id="102d2-130">Typical Tree Structure</span></span>](#typical-tree-structure)
-   [<span data-ttu-id="102d2-131">Соответствующие свойства</span><span class="sxs-lookup"><span data-stu-id="102d2-131">Relevant Properties</span></span>](#relevant-properties)
-   [<span data-ttu-id="102d2-132">Обязательные шаблоны элементов управления</span><span class="sxs-lookup"><span data-stu-id="102d2-132">Required Control Patterns</span></span>](#required-control-patterns)
-   [<span data-ttu-id="102d2-133">Работа с элементами в больших списках</span><span class="sxs-lookup"><span data-stu-id="102d2-133">Working with DataItems in Large Lists</span></span>](#working-with-dataitems-in-large-lists)
-   [<span data-ttu-id="102d2-134">Обязательные события</span><span class="sxs-lookup"><span data-stu-id="102d2-134">Required Events</span></span>](#required-events)
-   [<span data-ttu-id="102d2-135">Пример элемента управления DataItem</span><span class="sxs-lookup"><span data-stu-id="102d2-135">DataItem Control Type Example</span></span>](#dataitem-control-type-example)
-   [<span data-ttu-id="102d2-136">См. также</span><span class="sxs-lookup"><span data-stu-id="102d2-136">Related topics</span></span>](#related-topics)

## <a name="typical-tree-structure"></a><span data-ttu-id="102d2-137">Типичная древовидная структура</span><span class="sxs-lookup"><span data-stu-id="102d2-137">Typical Tree Structure</span></span>

<span data-ttu-id="102d2-138">В следующей таблице представлен типичный элемент управления и представление содержимого дерева модели автоматизации пользовательского интерфейса, которое относится к элементам управления DataItem и описывает, что может содержаться в каждом представлении.</span><span class="sxs-lookup"><span data-stu-id="102d2-138">The following table depicts a typical control and content view of the UI Automation tree that pertains to data item controls and describes what can be contained in each view.</span></span> <span data-ttu-id="102d2-139">Дополнительные сведения о дереве автоматизации пользовательского интерфейса см. в разделе [Общие сведения о дереве модели автоматизации пользовательского интерфейса](uiauto-treeoverview.md).</span><span class="sxs-lookup"><span data-stu-id="102d2-139">For more information about the UI Automation tree, see [UI Automation Tree Overview](uiauto-treeoverview.md).</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="102d2-140">Представление элемента управления</span><span class="sxs-lookup"><span data-stu-id="102d2-140">Control View</span></span></th>
<th><span data-ttu-id="102d2-141">Представление содержимого</span><span class="sxs-lookup"><span data-stu-id="102d2-141">Content View</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><ul>
<li><span data-ttu-id="102d2-142">DataItem</span><span class="sxs-lookup"><span data-stu-id="102d2-142">DataItem</span></span>
<ul>
<li><span data-ttu-id="102d2-143">Изменяется (0 и более; возможна иерархическая структуризация)</span><span class="sxs-lookup"><span data-stu-id="102d2-143">Varies (0 or more; can be structured in hierarchy)</span></span></li>
</ul></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="102d2-144">DataItem</span><span class="sxs-lookup"><span data-stu-id="102d2-144">DataItem</span></span>
<ul>
<li><span data-ttu-id="102d2-145">Изменяется (0 и более; возможна иерархическая структуризация)</span><span class="sxs-lookup"><span data-stu-id="102d2-145">Varies (0 or more; can be structured in hierarchy)</span></span></li>
</ul></li>
</ul></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="102d2-146">Элемент данных в сетке данных может поддерживать множество объектов, в том числе еще один уровень элементов данных или определенные элементы сетки, такие как текст, изображения или элементы управления "Поле ввода".</span><span class="sxs-lookup"><span data-stu-id="102d2-146">A data item element in a data grid can host a variety of objects, including another layer of data items, or specific grid elements such as text, images, or edit controls.</span></span> <span data-ttu-id="102d2-147">Если элемент данных имеет определенную роль объекта, элемент должен быть представлен как конкретный тип элемента управления. Например, тип элемента управления [ListItem](uiauto-supportlistitemcontroltype.md) для выбираемого элемента данных в сетке.</span><span class="sxs-lookup"><span data-stu-id="102d2-147">If the data item element has a specific object role, the element should be exposed as a specific control type; for example, a [ListItem](uiauto-supportlistitemcontroltype.md) control type for a selectable data item in the grid.</span></span>

## <a name="relevant-properties"></a><span data-ttu-id="102d2-148">Соответствующие свойства</span><span class="sxs-lookup"><span data-stu-id="102d2-148">Relevant Properties</span></span>

<span data-ttu-id="102d2-149">В следующей таблице перечислены свойства модели автоматизации пользовательского интерфейса, значения или определения которых особенно важны для типа элемента управления DataItem.</span><span class="sxs-lookup"><span data-stu-id="102d2-149">The following table lists the UI Automation properties whose value or definition is especially relevant to the DataItem control type.</span></span> <span data-ttu-id="102d2-150">Дополнительные сведения о свойствах модели автоматизации пользовательского интерфейса см. в разделе [Получение свойств элементов модели автоматизации пользовательского интерфейса](uiauto-propertiesforclients.md).</span><span class="sxs-lookup"><span data-stu-id="102d2-150">For more information about UI Automation properties, see [Retrieving Properties from UI Automation Elements](uiauto-propertiesforclients.md).</span></span>



| <span data-ttu-id="102d2-151">Свойство модели автоматизации пользовательского интерфейса</span><span class="sxs-lookup"><span data-stu-id="102d2-151">UI Automation Property</span></span>                                                                                              | <span data-ttu-id="102d2-152">Значение</span><span class="sxs-lookup"><span data-stu-id="102d2-152">Value</span></span>        | <span data-ttu-id="102d2-153">Примечания</span><span class="sxs-lookup"><span data-stu-id="102d2-153">Notes</span></span>                                                                                                                                                                                                |
|---------------------------------------------------------------------------------------------------------------------|--------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="102d2-154">**UIA \_ аутоматионидпропертид**</span><span class="sxs-lookup"><span data-stu-id="102d2-154">**UIA\_AutomationIdPropertyId**</span></span>](uiauto-automation-element-propids.md)                 | <span data-ttu-id="102d2-155">См. примечания.</span><span class="sxs-lookup"><span data-stu-id="102d2-155">See notes.</span></span>   | <span data-ttu-id="102d2-156">Значение этого свойства должно быть уникальным среди всех одноранговых элементов в необработанном представлении дерева модели автоматизации пользовательского интерфейса.</span><span class="sxs-lookup"><span data-stu-id="102d2-156">The value of this property must be unique among all peer elements in the raw view of the UI Automation tree.</span></span>                                                                                         |
| [<span data-ttu-id="102d2-157">**UIA \_ баундингректанглепропертид**</span><span class="sxs-lookup"><span data-stu-id="102d2-157">**UIA\_BoundingRectanglePropertyId**</span></span>](uiauto-automation-element-propids.md)       | <span data-ttu-id="102d2-158">См. примечания.</span><span class="sxs-lookup"><span data-stu-id="102d2-158">See notes.</span></span>   | <span data-ttu-id="102d2-159">Внешний прямоугольник, содержащий весь элемент управления.</span><span class="sxs-lookup"><span data-stu-id="102d2-159">The outermost rectangle that contains the whole control.</span></span>                                                                                                                                             |
| [<span data-ttu-id="102d2-160">**UIA \_ кликкаблепоинтпропертид**</span><span class="sxs-lookup"><span data-stu-id="102d2-160">**UIA\_ClickablePointPropertyId**</span></span>](uiauto-automation-element-propids.md)             | <span data-ttu-id="102d2-161">См. примечания.</span><span class="sxs-lookup"><span data-stu-id="102d2-161">See notes.</span></span>   | <span data-ttu-id="102d2-162">Поддерживается при наличии ограничивающего прямоугольника.</span><span class="sxs-lookup"><span data-stu-id="102d2-162">Supported if there is a bounding rectangle.</span></span> <span data-ttu-id="102d2-163">Если не все точки внутри ограничивающего прямоугольника являются щелчками, а элемент выполняет специализированное тестирование нажатия, переопределите и предоставьте точку для щелчка.</span><span class="sxs-lookup"><span data-stu-id="102d2-163">If not every point within the bounding rectangle is clickable, and the element performs specialized hit testing, override and provide a clickable point.</span></span> |
| [<span data-ttu-id="102d2-164">**UIA \_ контролтипепропертид**</span><span class="sxs-lookup"><span data-stu-id="102d2-164">**UIA\_ControlTypePropertyId**</span></span>](uiauto-automation-element-propids.md)                   | <span data-ttu-id="102d2-165">**DataItem**</span><span class="sxs-lookup"><span data-stu-id="102d2-165">**DataItem**</span></span> |                                                                                                                                                                                                      |
| [<span data-ttu-id="102d2-166">**UIA \_ исконтентелементпропертид**</span><span class="sxs-lookup"><span data-stu-id="102d2-166">**UIA\_IsContentElementPropertyId**</span></span>](uiauto-automation-element-propids.md)         | <span data-ttu-id="102d2-167">true</span><span class="sxs-lookup"><span data-stu-id="102d2-167">TRUE</span></span>         | <span data-ttu-id="102d2-168">Элемент управления DataItem всегда должен быть содержимым.</span><span class="sxs-lookup"><span data-stu-id="102d2-168">The data item control must always be content.</span></span>                                                                                                                                                        |
| [<span data-ttu-id="102d2-169">**UIA \_ исконтролелементпропертид**</span><span class="sxs-lookup"><span data-stu-id="102d2-169">**UIA\_IsControlElementPropertyId**</span></span>](uiauto-automation-element-propids.md)         | <span data-ttu-id="102d2-170">true</span><span class="sxs-lookup"><span data-stu-id="102d2-170">TRUE</span></span>         | <span data-ttu-id="102d2-171">Элемент управления DataItem всегда должен быть элементом управления.</span><span class="sxs-lookup"><span data-stu-id="102d2-171">The data item control must always be a control.</span></span>                                                                                                                                                      |
| [<span data-ttu-id="102d2-172">**UIA \_ искэйбоардфокусаблепропертид**</span><span class="sxs-lookup"><span data-stu-id="102d2-172">**UIA\_IsKeyboardFocusablePropertyId**</span></span>](uiauto-automation-element-propids.md)   | <span data-ttu-id="102d2-173">См. примечания.</span><span class="sxs-lookup"><span data-stu-id="102d2-173">See notes.</span></span>   | <span data-ttu-id="102d2-174">Если элемент управления может получать фокус клавиатуры, он должен поддерживать это свойство.</span><span class="sxs-lookup"><span data-stu-id="102d2-174">If the control can receive keyboard focus, it must support this property.</span></span>                                                                                                                            |
| [<span data-ttu-id="102d2-175">**UIA \_ итемстатуспропертид**</span><span class="sxs-lookup"><span data-stu-id="102d2-175">**UIA\_ItemStatusPropertyId**</span></span>](uiauto-automation-element-propids.md)                     | <span data-ttu-id="102d2-176">См. примечания.</span><span class="sxs-lookup"><span data-stu-id="102d2-176">See notes.</span></span>   | <span data-ttu-id="102d2-177">Если элемент управления содержит состояние, которое обновляется динамически, это свойство должно поддерживаться таким образом, чтобы технология поддержки могла получать обновления при изменении состояния элемента.</span><span class="sxs-lookup"><span data-stu-id="102d2-177">If the control contains status that is being updated dynamically, this property must be supported so that an assistive technology can receive updates when the status of the element changes.</span></span>        |
| [<span data-ttu-id="102d2-178">**UIA \_ итемтипепропертид**</span><span class="sxs-lookup"><span data-stu-id="102d2-178">**UIA\_ItemTypePropertyId**</span></span>](uiauto-automation-element-propids.md)                         | <span data-ttu-id="102d2-179">См. примечания.</span><span class="sxs-lookup"><span data-stu-id="102d2-179">See notes.</span></span>   | <span data-ttu-id="102d2-180">Это строковое значение, передающее конечному пользователю базовый объект, который этот элемент представляет.</span><span class="sxs-lookup"><span data-stu-id="102d2-180">This is the string value that conveys to the end user the underlying object that the item represents.</span></span> <span data-ttu-id="102d2-181">Примеры: "файл мультимедиа" и "Contact".</span><span class="sxs-lookup"><span data-stu-id="102d2-181">Examples include "Media File" and "Contact".</span></span>                                                   |
| [<span data-ttu-id="102d2-182">**UIA \_ лабеледбипропертид**</span><span class="sxs-lookup"><span data-stu-id="102d2-182">**UIA\_LabeledByPropertyId**</span></span>](uiauto-automation-element-propids.md)                       | <span data-ttu-id="102d2-183">NULL</span><span class="sxs-lookup"><span data-stu-id="102d2-183">Null</span></span>         | <span data-ttu-id="102d2-184">Элементы управления DataItem не имеют меток со статическим текстом.</span><span class="sxs-lookup"><span data-stu-id="102d2-184">Data item controls do not have a static text label.</span></span>                                                                                                                                                  |
| [<span data-ttu-id="102d2-185">**UIA \_ локализедконтролтипепропертид**</span><span class="sxs-lookup"><span data-stu-id="102d2-185">**UIA\_LocalizedControlTypePropertyId**</span></span>](uiauto-automation-element-propids.md) | <span data-ttu-id="102d2-186">См. примечания.</span><span class="sxs-lookup"><span data-stu-id="102d2-186">See notes.</span></span>   | <span data-ttu-id="102d2-187">Локализованная строка, соответствующая типу элемента управления **DataItem** .</span><span class="sxs-lookup"><span data-stu-id="102d2-187">Localized string corresponding to the **DataItem** control type.</span></span> <span data-ttu-id="102d2-188">Значение по умолчанию — "элемент данных" для en-US или English (США).</span><span class="sxs-lookup"><span data-stu-id="102d2-188">The default value is "data item" for en-US or English (United States).</span></span>                                                              |
| [<span data-ttu-id="102d2-189">**UIA \_ намепропертид**</span><span class="sxs-lookup"><span data-stu-id="102d2-189">**UIA\_NamePropertyId**</span></span>](uiauto-automation-element-propids.md)                                 | <span data-ttu-id="102d2-190">См. примечания.</span><span class="sxs-lookup"><span data-stu-id="102d2-190">See notes.</span></span>   | <span data-ttu-id="102d2-191">Элемент управления DataItem всегда содержит основной текстовый элемент, который пользователь распознает как идентификатор элемента.</span><span class="sxs-lookup"><span data-stu-id="102d2-191">The data item control always contains a primary text element that the user would recognize as the identifier for the item.</span></span>                                                                           |



 

## <a name="required-control-patterns"></a><span data-ttu-id="102d2-192">Обязательные шаблоны элементов управления</span><span class="sxs-lookup"><span data-stu-id="102d2-192">Required Control Patterns</span></span>

<span data-ttu-id="102d2-193">В следующей таблице перечислены шаблоны элементов управления модели автоматизации пользовательского интерфейса, которые должны поддерживаться всеми элементами управления "элемент данных".</span><span class="sxs-lookup"><span data-stu-id="102d2-193">The following table lists the UI Automation control patterns required to be supported by all data item controls.</span></span> <span data-ttu-id="102d2-194">Дополнительные сведения о шаблонах элементов управления см. в разделе [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md).</span><span class="sxs-lookup"><span data-stu-id="102d2-194">For more information on control patterns, see [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md).</span></span>



| <span data-ttu-id="102d2-195">Шаблон элемента управления</span><span class="sxs-lookup"><span data-stu-id="102d2-195">Control Pattern</span></span>                                                   | <span data-ttu-id="102d2-196">Поддержка</span><span class="sxs-lookup"><span data-stu-id="102d2-196">Support</span></span> | <span data-ttu-id="102d2-197">Примечания</span><span class="sxs-lookup"><span data-stu-id="102d2-197">Notes</span></span>                                                                                                                                                                                                                 |
|-------------------------------------------------------------------|---------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="102d2-198">**IExpandCollapseProvider**</span><span class="sxs-lookup"><span data-stu-id="102d2-198">**IExpandCollapseProvider**</span></span>](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iexpandcollapseprovider) | <span data-ttu-id="102d2-199">Зависит</span><span class="sxs-lookup"><span data-stu-id="102d2-199">Depends</span></span> | <span data-ttu-id="102d2-200">Если элемент данных может быть развернут или свернут для отображения и скрытия информации, должен поддерживаться шаблон элемента управления [ExpandCollapse](uiauto-implementingexpandcollapse.md) .</span><span class="sxs-lookup"><span data-stu-id="102d2-200">If the data item can be expanded or collapsed to show and hide information, the [ExpandCollapse](uiauto-implementingexpandcollapse.md) control pattern must be supported.</span></span>                                            |
| [<span data-ttu-id="102d2-201">**IGridItemProvider**</span><span class="sxs-lookup"><span data-stu-id="102d2-201">**IGridItemProvider**</span></span>](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-igriditemprovider)             | <span data-ttu-id="102d2-202">Зависит</span><span class="sxs-lookup"><span data-stu-id="102d2-202">Depends</span></span> | <span data-ttu-id="102d2-203">Элементы данных будут поддерживать шаблон элемента управления [GridItem](uiauto-implementinggriditem.md) , если коллекция элементов данных доступна в контейнере, к которому можно выполнить пространственное перемещение элемента в элемент.</span><span class="sxs-lookup"><span data-stu-id="102d2-203">Data items will support the [GridItem](uiauto-implementinggriditem.md) control pattern when a collection of data items is available within a container that can be spatially navigated item-to-item.</span></span>                 |
| [<span data-ttu-id="102d2-204">**IScrollItemProvider**</span><span class="sxs-lookup"><span data-stu-id="102d2-204">**IScrollItemProvider**</span></span>](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iscrollitemprovider)         | <span data-ttu-id="102d2-205">Зависит</span><span class="sxs-lookup"><span data-stu-id="102d2-205">Depends</span></span> | <span data-ttu-id="102d2-206">Все элементы данных поддерживают возможность прокрутки на представление с помощью шаблона элемента управления [скроллитем](uiauto-implementingscrollitem.md) , если их контейнер данных содержит больше элементов, чем может уместиться на экране.</span><span class="sxs-lookup"><span data-stu-id="102d2-206">All data items support the ability to be scrolled into view with the [ScrollItem](uiauto-implementingscrollitem.md) control pattern when their data container has more items than can fit on the screen.</span></span>             |
| [<span data-ttu-id="102d2-207">**ISelectionItemProvider**</span><span class="sxs-lookup"><span data-stu-id="102d2-207">**ISelectionItemProvider**</span></span>](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iselectionitemprovider)   | <span data-ttu-id="102d2-208">Зависит</span><span class="sxs-lookup"><span data-stu-id="102d2-208">Depends</span></span> | <span data-ttu-id="102d2-209">Возможность выбора элементов данных зависит от содержимого.</span><span class="sxs-lookup"><span data-stu-id="102d2-209">The ability to select the data items depends on the content.</span></span>                                                                                                                                                          |
| [<span data-ttu-id="102d2-210">**ITableItemProvider**</span><span class="sxs-lookup"><span data-stu-id="102d2-210">**ITableItemProvider**</span></span>](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itableitemprovider)           | <span data-ttu-id="102d2-211">Зависит</span><span class="sxs-lookup"><span data-stu-id="102d2-211">Depends</span></span> | <span data-ttu-id="102d2-212">Если элемент данных содержится в типе элемента управления [DataGrid](uiauto-supportdatagridcontroltype.md) с элементом Header, он должен поддерживать шаблон элемента управления [TableItem](uiauto-implementingtableitem.md) .</span><span class="sxs-lookup"><span data-stu-id="102d2-212">If the data item is contained within a [DataGrid](uiauto-supportdatagridcontroltype.md) control type that has a header element, it should support the [TableItem](uiauto-implementingtableitem.md) control pattern.</span></span> |
| [<span data-ttu-id="102d2-213">**IToggleProvider**</span><span class="sxs-lookup"><span data-stu-id="102d2-213">**IToggleProvider**</span></span>](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itoggleprovider)                 | <span data-ttu-id="102d2-214">Зависит</span><span class="sxs-lookup"><span data-stu-id="102d2-214">Depends</span></span> | <span data-ttu-id="102d2-215">Если элемент данных содержит состояние, которое может быть циклическим, оно должно поддерживать шаблон элемента управления [Toggle](uiauto-implementingtoggle.md) .</span><span class="sxs-lookup"><span data-stu-id="102d2-215">If the data item contains a state that can be cycled through, it should support the [Toggle](uiauto-implementingtoggle.md) control pattern.</span></span>                                                                          |
| [<span data-ttu-id="102d2-216">**IValueProvider**</span><span class="sxs-lookup"><span data-stu-id="102d2-216">**IValueProvider**</span></span>](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-ivalueprovider)                   | <span data-ttu-id="102d2-217">Зависит</span><span class="sxs-lookup"><span data-stu-id="102d2-217">Depends</span></span> | <span data-ttu-id="102d2-218">Если основной текст элемента данных является редактируемым, шаблон элемента управления [value](uiauto-implementingvalue.md) должен поддерживаться.</span><span class="sxs-lookup"><span data-stu-id="102d2-218">If the data item's primary text is editable, the [Value](uiauto-implementingvalue.md) control pattern must be supported.</span></span>                                                                                             |



 

## <a name="working-with-dataitems-in-large-lists"></a><span data-ttu-id="102d2-219">Работа с элементами в больших списках</span><span class="sxs-lookup"><span data-stu-id="102d2-219">Working with DataItems in Large Lists</span></span>

<span data-ttu-id="102d2-220">Так как большие списки часто виртуализованы в платформах пользовательского интерфейса для повышения производительности, клиент автоматизации пользовательского интерфейса не может использовать функцию запросов UI Automation для поиска содержимого полного дерева так же, как и в других контейнерах элементов.</span><span class="sxs-lookup"><span data-stu-id="102d2-220">Because large lists are often virtualized within UI frameworks to assist in performance, a UI Automation client cannot use the UI Automation query feature to search the contents of the full tree in the same way that it can in other item containers.</span></span> <span data-ttu-id="102d2-221">Перед доступом к полному набору сведений из элемента данных клиент должен прокручивать элемент в представление (или развернуть элемент управления, чтобы показать все доступные параметры).</span><span class="sxs-lookup"><span data-stu-id="102d2-221">A client should scroll the item into view (or expand the control to show all available options) prior to accessing the full set of information from the data item.</span></span>

<span data-ttu-id="102d2-222">При вызове [**SetFocus**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-setfocus) в элементе модели автоматизации пользовательского интерфейса для элемента данных обозреватель Microsoft Windows Explorer возвращается успешно и заставляет фокус быть установленным элементом управления редактирования в поддереве элемента данных.</span><span class="sxs-lookup"><span data-stu-id="102d2-222">When calling [**SetFocus**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-setfocus) on the UI Automation element for the data item, Microsoft Windows Explorer returns successfully and causes focus to be set to the Edit control within the data item subtree.</span></span>

## <a name="required-events"></a><span data-ttu-id="102d2-223">Обязательные события</span><span class="sxs-lookup"><span data-stu-id="102d2-223">Required Events</span></span>

<span data-ttu-id="102d2-224">В следующей таблице перечислены события автоматизации пользовательского интерфейса, которые должны поддерживаться элементами управления "элемент данных".</span><span class="sxs-lookup"><span data-stu-id="102d2-224">The following table lists the UI Automation events that data item controls are required to support.</span></span> <span data-ttu-id="102d2-225">Дополнительные сведения о событиях см. в разделе [UI Automation Events Overview](uiauto-eventsoverview.md).</span><span class="sxs-lookup"><span data-stu-id="102d2-225">For more information on events, see [UI Automation Events Overview](uiauto-eventsoverview.md).</span></span>



| <span data-ttu-id="102d2-226">Событие автоматизации пользовательского интерфейса</span><span class="sxs-lookup"><span data-stu-id="102d2-226">UI Automation Event</span></span>                                                                                                                                                | <span data-ttu-id="102d2-227">Примечания</span><span class="sxs-lookup"><span data-stu-id="102d2-227">Notes</span></span>                                                                                                                            |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="102d2-228">**UIA \_ аутоматионфокусчанжедевентид**</span><span class="sxs-lookup"><span data-stu-id="102d2-228">**UIA\_AutomationFocusChangedEventId**</span></span>](uiauto-event-ids.md)                                                                   |                                                                                                                                  |
| <span data-ttu-id="102d2-229">[**UIA \_**](uiauto-automation-element-propids.md) Событие изменения свойства баундингректанглепропертид.</span><span class="sxs-lookup"><span data-stu-id="102d2-229">[**UIA\_BoundingRectanglePropertyId**](uiauto-automation-element-propids.md) property-changed event.</span></span>                              |                                                                                                                                  |
| <span data-ttu-id="102d2-230">[**UIA \_**](uiauto-control-pattern-propids.md) Событие изменения свойства експандколлапсикспандколлапсестатепропертид.</span><span class="sxs-lookup"><span data-stu-id="102d2-230">[**UIA\_ExpandCollapseExpandCollapseStatePropertyId**](uiauto-control-pattern-propids.md) property-changed event.</span></span> | <span data-ttu-id="102d2-231">Если элемент управления поддерживает шаблон элемента управления [ExpandCollapse](uiauto-implementingexpandcollapse.md) , он должен поддерживать это событие.</span><span class="sxs-lookup"><span data-stu-id="102d2-231">If the control supports the [ExpandCollapse](uiauto-implementingexpandcollapse.md) control pattern, it must support this event.</span></span> |
| [<span data-ttu-id="102d2-232">**UIA \_ Invoke \_ инвокедевентид**</span><span class="sxs-lookup"><span data-stu-id="102d2-232">**UIA\_Invoke\_InvokedEventId**</span></span>](uiauto-event-ids.md)                                                                                  | <span data-ttu-id="102d2-233">Если элемент управления поддерживает шаблон элемента управления [Invoke](uiauto-implementinginvoke.md) , он должен поддерживать это событие.</span><span class="sxs-lookup"><span data-stu-id="102d2-233">If the control supports the [Invoke](uiauto-implementinginvoke.md) control pattern, it must support this event.</span></span>                 |
| <span data-ttu-id="102d2-234">[**UIA \_**](uiauto-automation-element-propids.md) Событие изменения свойства исенабледпропертид.</span><span class="sxs-lookup"><span data-stu-id="102d2-234">[**UIA\_IsEnabledPropertyId**](uiauto-automation-element-propids.md) property-changed event.</span></span>                                              | <span data-ttu-id="102d2-235">Если элемент управления поддерживает свойство « [**включено**](uiauto-automation-element-propids.md) », оно должно поддерживать это событие.</span><span class="sxs-lookup"><span data-stu-id="102d2-235">If the control supports the [**IsEnabled**](uiauto-automation-element-propids.md) property, it must support this event.</span></span>         |
| <span data-ttu-id="102d2-236">[**UIA \_**](uiauto-automation-element-propids.md) Событие изменения свойства исоффскринпропертид.</span><span class="sxs-lookup"><span data-stu-id="102d2-236">[**UIA\_IsOffscreenPropertyId**](uiauto-automation-element-propids.md) property-changed event.</span></span>                                          | <span data-ttu-id="102d2-237">Если элемент управления поддерживает свойство [**исоффскрин**](uiauto-automation-element-propids.md) , он должен поддерживать это событие.</span><span class="sxs-lookup"><span data-stu-id="102d2-237">If the control supports the [**IsOffscreen**](uiauto-automation-element-propids.md) property, it must support this event.</span></span>       |
| <span data-ttu-id="102d2-238">[**UIA \_**](uiauto-automation-element-propids.md) Событие изменения свойства итемстатуспропертид.</span><span class="sxs-lookup"><span data-stu-id="102d2-238">[**UIA\_ItemStatusPropertyId**](uiauto-automation-element-propids.md) property-changed event.</span></span>                                            | <span data-ttu-id="102d2-239">Если элемент управления поддерживает свойство [**итемстатус**](uiauto-automation-element-propids.md) , он должен поддерживать это событие.</span><span class="sxs-lookup"><span data-stu-id="102d2-239">If the control supports the [**ItemStatus**](uiauto-automation-element-propids.md) property, it must support this event.</span></span>        |
| <span data-ttu-id="102d2-240">[**UIA \_**](uiauto-automation-element-propids.md) Событие изменения свойства намепропертид.</span><span class="sxs-lookup"><span data-stu-id="102d2-240">[**UIA\_NamePropertyId**](uiauto-automation-element-propids.md) property-changed event.</span></span>                                                        |                                                                                                                                  |
| [<span data-ttu-id="102d2-241">**UIA \_ SelectionItem \_ елементаддедтоселектионевентид**</span><span class="sxs-lookup"><span data-stu-id="102d2-241">**UIA\_SelectionItem\_ElementAddedToSelectionEventId**</span></span>](uiauto-event-ids.md)                                    | <span data-ttu-id="102d2-242">Если элемент управления поддерживает шаблон элемента управления [SelectionItem](uiauto-implementingselectionitem.md) , он должен поддерживать это событие.</span><span class="sxs-lookup"><span data-stu-id="102d2-242">If the control supports the [SelectionItem](uiauto-implementingselectionitem.md) control pattern, it must support this event.</span></span>   |
| [<span data-ttu-id="102d2-243">**UIA \_ SelectionItem \_ елементремоведфромселектионевентид**</span><span class="sxs-lookup"><span data-stu-id="102d2-243">**UIA\_SelectionItem\_ElementRemovedFromSelectionEventId**</span></span>](uiauto-event-ids.md)                            | <span data-ttu-id="102d2-244">Если элемент управления поддерживает шаблон элемента управления [SelectionItem](uiauto-implementingselectionitem.md) , он должен поддерживать это событие.</span><span class="sxs-lookup"><span data-stu-id="102d2-244">If the control supports the [SelectionItem](uiauto-implementingselectionitem.md) control pattern, it must support this event.</span></span>   |
| [<span data-ttu-id="102d2-245">**UIA \_ SelectionItem \_ елементселектедевентид**</span><span class="sxs-lookup"><span data-stu-id="102d2-245">**UIA\_SelectionItem\_ElementSelectedEventId**</span></span>](uiauto-event-ids.md)                                                    | <span data-ttu-id="102d2-246">Если элемент управления поддерживает шаблон элемента управления [SelectionItem](uiauto-implementingselectionitem.md) , он должен поддерживать это событие.</span><span class="sxs-lookup"><span data-stu-id="102d2-246">If the control supports the [SelectionItem](uiauto-implementingselectionitem.md) control pattern, it must support this event.</span></span>   |
| [<span data-ttu-id="102d2-247">**UIA \_ структуречанжедевентид**</span><span class="sxs-lookup"><span data-stu-id="102d2-247">**UIA\_StructureChangedEventId**</span></span>](uiauto-event-ids.md)                                                                               |                                                                                                                                  |
| <span data-ttu-id="102d2-248">[**UIA \_**](uiauto-control-pattern-propids.md) Событие изменения свойства тогглетогглестатепропертид.</span><span class="sxs-lookup"><span data-stu-id="102d2-248">[**UIA\_ToggleToggleStatePropertyId**](uiauto-control-pattern-propids.md) property-changed event.</span></span>                                 | <span data-ttu-id="102d2-249">Если элемент управления поддерживает шаблон элемента управления [Toggle](uiauto-implementingtoggle.md) , он должен поддерживать это событие.</span><span class="sxs-lookup"><span data-stu-id="102d2-249">If the control supports the [Toggle](uiauto-implementingtoggle.md) control pattern, it must support this event.</span></span>                 |
| <span data-ttu-id="102d2-250">[**UIA \_**](uiauto-control-pattern-propids.md) Событие изменения свойства валуевалуепропертид.</span><span class="sxs-lookup"><span data-stu-id="102d2-250">[**UIA\_ValueValuePropertyId**](uiauto-control-pattern-propids.md) property-changed event.</span></span>                                               | <span data-ttu-id="102d2-251">Если элемент управления поддерживает шаблон элемента управления [value](uiauto-implementingvalue.md) , он должен поддерживать это событие.</span><span class="sxs-lookup"><span data-stu-id="102d2-251">If the control supports the [Value](uiauto-implementingvalue.md) control pattern, it must support this event.</span></span>                   |



 

## <a name="dataitem-control-type-example"></a><span data-ttu-id="102d2-252">Пример элемента управления DataItem</span><span class="sxs-lookup"><span data-stu-id="102d2-252">DataItem Control Type Example</span></span>

<span data-ttu-id="102d2-253">На следующем рисунке показан тип элемента управления DataItem в элементе управления "представление списка".</span><span class="sxs-lookup"><span data-stu-id="102d2-253">The following image illustrates a DataItem control type in a list-view control.</span></span>

![снимок экрана элемента управления "представление списка" с типом элемента управления DataItem](images/dataitemxmpl.jpg)

<span data-ttu-id="102d2-255">Ниже показано представление элемента управления и представление содержимого дерева модели автоматизации пользовательского интерфейса, относящегося к элементу управления элементом данных.</span><span class="sxs-lookup"><span data-stu-id="102d2-255">The control view and the content view of the UI Automation tree that pertains to the data item control is displayed below.</span></span> <span data-ttu-id="102d2-256">Шаблоны элементов управления для каждого элемента автоматизации отображаются в круглых скобках.</span><span class="sxs-lookup"><span data-stu-id="102d2-256">The control patterns for each automation element are shown in parentheses.</span></span> <span data-ttu-id="102d2-257">**Группа** Contoso также является частью сетки элемента управления узла сетки данных.</span><span class="sxs-lookup"><span data-stu-id="102d2-257">The **Group** "Contoso" is also part of the grid of the data grid host control.</span></span> <span data-ttu-id="102d2-258">Пример структуры сетки более высокого уровня см. в разделе [тип элемента управления DataGrid](uiauto-supportdatagridcontroltype.md).</span><span class="sxs-lookup"><span data-stu-id="102d2-258">For an example of a higher level grid structure, see [DataGrid Control Type](uiauto-supportdatagridcontroltype.md).</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="102d2-259">Дерево модели автоматизации пользовательского интерфейса — представление элемента управления</span><span class="sxs-lookup"><span data-stu-id="102d2-259">UI Automation Tree - Control View</span></span></th>
<th><span data-ttu-id="102d2-260">Дерево модели автоматизации пользовательского интерфейса — представление содержимого</span><span class="sxs-lookup"><span data-stu-id="102d2-260">UI Automation Tree - Content View</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><ul>
<li><span data-ttu-id="102d2-261">Группа &quot; contoso &quot; (таблица, сетка)</span><span class="sxs-lookup"><span data-stu-id="102d2-261">Group &quot;Contoso&quot; (Table, Grid)</span></span>
<ul>
<li><span data-ttu-id="102d2-262">&quot;Receivable.docучетных записей DataItem &quot; (TableItem, GridItem, SelectionItem, Invoke)</span><span class="sxs-lookup"><span data-stu-id="102d2-262">DataItem &quot;Accounts Receivable.doc&quot; (TableItem, GridItem, SelectionItem, Invoke)</span></span>
<ul>
<li><span data-ttu-id="102d2-263">&quot;Учетные записи изображений Receivable.doc&quot;</span><span class="sxs-lookup"><span data-stu-id="102d2-263">Image &quot;Accounts Receivable.doc&quot;</span></span></li>
<li><span data-ttu-id="102d2-264">Изменить &quot; имя &quot; (TableItem, GridItem, &quot; учетные записи Receivable.doc&quot; )</span><span class="sxs-lookup"><span data-stu-id="102d2-264">Edit &quot;Name&quot; (TableItem, GridItem, Value &quot;Accounts Receivable.doc&quot;)</span></span></li>
<li><span data-ttu-id="102d2-265">Изменение &quot; даты изменения &quot; (TableItem, GridItem, value &quot; 8/25/2006 3:29 PM &quot; )</span><span class="sxs-lookup"><span data-stu-id="102d2-265">Edit &quot;Date modified&quot; (TableItem, GridItem, Value &quot;8/25/2006 3:29 PM&quot;)</span></span></li>
<li><span data-ttu-id="102d2-266">Изменение &quot; размера &quot; (GridItem, TableItem, value &quot; 11,0 КБ &quot; )</span><span class="sxs-lookup"><span data-stu-id="102d2-266">Edit &quot;Size&quot; (GridItem, TableItem, Value &quot;11.0 KB&quot;)</span></span></li>
</ul></li>
<li><span data-ttu-id="102d2-267">&quot;Payable.docучетных записей DataItem &quot; (TableItem, GridItem, SelectionItem, Invoke)</span><span class="sxs-lookup"><span data-stu-id="102d2-267">DataItem &quot;Accounts Payable.doc&quot; (TableItem, GridItem, SelectionItem, Invoke)</span></span>
<ul>
<li><span data-ttu-id="102d2-268">...</span><span class="sxs-lookup"><span data-stu-id="102d2-268">...</span></span></li>
</ul></li>
</ul></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="102d2-269">Группа &quot; contoso &quot; (таблица, сетка)</span><span class="sxs-lookup"><span data-stu-id="102d2-269">Group &quot;Contoso&quot; (Table, Grid)</span></span>
<ul>
<li><span data-ttu-id="102d2-270">&quot;Receivable.docучетных записей DataItem &quot; (TableItem, GridItem, SelectionItem, Invoke)</span><span class="sxs-lookup"><span data-stu-id="102d2-270">DataItem &quot;Accounts Receivable.doc&quot; (TableItem, GridItem, SelectionItem, Invoke)</span></span>
<ul>
<li><span data-ttu-id="102d2-271">&quot;Учетные записи изображений Receivable.doc&quot;</span><span class="sxs-lookup"><span data-stu-id="102d2-271">Image &quot;Accounts Receivable.doc&quot;</span></span></li>
<li><span data-ttu-id="102d2-272">Изменить &quot; имя &quot; (TableItem, GridItem, &quot; учетные записи Receivable.doc&quot; )</span><span class="sxs-lookup"><span data-stu-id="102d2-272">Edit &quot;Name&quot; (TableItem, GridItem, Value &quot;Accounts Receivable.doc&quot;)</span></span></li>
<li><span data-ttu-id="102d2-273">Изменение &quot; даты изменения &quot; (TableItem, GridItem, value &quot; 8/25/2006 3:29 PM &quot; )</span><span class="sxs-lookup"><span data-stu-id="102d2-273">Edit &quot;Date modified&quot; (TableItem, GridItem, Value &quot;8/25/2006 3:29 PM&quot;)</span></span></li>
<li><span data-ttu-id="102d2-274">Изменение &quot; размера &quot; (GridItem, TableItem, value &quot; 11,0 КБ &quot; )</span><span class="sxs-lookup"><span data-stu-id="102d2-274">Edit &quot;Size&quot; (GridItem, TableItem, Value &quot;11.0 KB&quot;)</span></span></li>
</ul></li>
<li><span data-ttu-id="102d2-275">&quot;Payable.docучетных записей DataItem &quot; (TableItem, GridItem, SelectionItem, Invoke)</span><span class="sxs-lookup"><span data-stu-id="102d2-275">DataItem &quot;Accounts Payable.doc&quot; (TableItem, GridItem, SelectionItem, Invoke)</span></span>
<ul>
<li><span data-ttu-id="102d2-276">...</span><span class="sxs-lookup"><span data-stu-id="102d2-276">...</span></span></li>
</ul></li>
</ul></li>
</ul></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="102d2-277">Если сетка представляет список выбираемых элементов, соответствующие выбираемые элементы пользовательского интерфейса могут быть представлены с типом элемента управления [ListItem](uiauto-supportlistitemcontroltype.md) , а не с типом элемента управления DataItem.</span><span class="sxs-lookup"><span data-stu-id="102d2-277">If a grid represents a list of selectable items, the corresponding selectable UI elements can be exposed with the [ListItem](uiauto-supportlistitemcontroltype.md) control type instead of the DataItem control type.</span></span> <span data-ttu-id="102d2-278">В предыдущем примере элементы **DataItem** ("accounts Receivable.doc" и "accounts Payable.doc") в **группе** ("contoso") можно улучшить, предоставив их как типы элементов управления ListItem, так как этот тип уже поддерживает шаблон элемента управления [SelectionItem](uiauto-implementingselectionitem.md) .</span><span class="sxs-lookup"><span data-stu-id="102d2-278">In the preceding example, the **DataItem** elements ("Accounts Receivable.doc" and "Accounts Payable.doc") under **Group** ("Contoso") can be improved by exposing them as ListItem control types because that type already supports the [SelectionItem](uiauto-implementingselectionitem.md) control pattern.</span></span>

## <a name="related-topics"></a><span data-ttu-id="102d2-279">См. также</span><span class="sxs-lookup"><span data-stu-id="102d2-279">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="102d2-280">**Зрения**</span><span class="sxs-lookup"><span data-stu-id="102d2-280">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="102d2-281">Общие сведения о типах элементов управления автоматизации пользовательского интерфейса</span><span class="sxs-lookup"><span data-stu-id="102d2-281">UI Automation Control Types Overview</span></span>](uiauto-controltypesoverview.md)
</dt> <dt>

[<span data-ttu-id="102d2-282">Общие сведения о модели автоматизации пользовательского интерфейса</span><span class="sxs-lookup"><span data-stu-id="102d2-282">UI Automation Overview</span></span>](uiauto-uiautomationoverview.md)
</dt> </dl>

 

 




