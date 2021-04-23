---
title: Тип элемента управления Table
description: В этом разделе содержатся сведения о поддержке автоматизации пользовательского интерфейса Майкрософт для типа элемента управления Table.
ms.assetid: 508db2af-1ca3-4003-8e1f-6e225cf79b7a
keywords:
- Модель автоматизации пользовательского интерфейса, поддержка типа элемента управления Table
- Модель автоматизации пользовательского интерфейса, тип элемента управления Table
- Модель автоматизации пользовательского интерфейса, древовидная структура для типа элемента управления Table
- Модель автоматизации пользовательского интерфейса, свойства для типа элемента управления Table
- Модель автоматизации пользовательского интерфейса, шаблоны элементов управления для типа элемента управления Table
- Модель автоматизации пользовательского интерфейса, события для типа элемента управления Table
- Древовидные структуры, тип элемента управления Table
- свойства, тип элемента управления Table
- шаблоны элементов управления, тип элемента управления Table
- события, тип элемента управления Table
- Поддержка типа элемента управления Table
- Table - тип элемента управления
- типы элементов управления, древовидная структура для типа элемента управления Table
- типы элементов управления, шаблоны элементов управления для типа элемента управления Table
- типы элементов управления, поддержка таблиц
- типы элементов управления, таблица
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cb4ee709bd16156a62882aeee014b4744dab2214
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104532309"
---
# <a name="table-control-type"></a><span data-ttu-id="5dd80-119">Тип элемента управления Table</span><span class="sxs-lookup"><span data-stu-id="5dd80-119">Table Control Type</span></span>

<span data-ttu-id="5dd80-120">В этом разделе содержатся сведения о поддержке автоматизации пользовательского интерфейса Майкрософт для типа элемента управления **Table** .</span><span class="sxs-lookup"><span data-stu-id="5dd80-120">This topic provides information about Microsoft UI Automation support for the **Table** control type.</span></span>

<span data-ttu-id="5dd80-121">Элементы управления "Таблица" содержат строки и столбцы текста и, при необходимости, заголовки строк и заголовки столбцов.</span><span class="sxs-lookup"><span data-stu-id="5dd80-121">Table controls contain rows and columns of text and, optionally, row headers and column headers.</span></span>

<span data-ttu-id="5dd80-122">В следующих разделах определяется необходимая древовидная структура модели автоматизации пользовательского интерфейса, свойства, шаблоны элементов управления и события для типа элемента управления **Table** .</span><span class="sxs-lookup"><span data-stu-id="5dd80-122">The following sections define the required UI Automation tree structure, properties, control patterns, and events for the **Table** control type.</span></span> <span data-ttu-id="5dd80-123">Требования к автоматизации пользовательского интерфейса применяются ко всем элементам управления "Таблица", в которых платформа или платформа пользовательского интерфейса интегрирует поддержку модели автоматизации пользовательского интерфейса для типов элементов управления и шаблонов элементов управления.</span><span class="sxs-lookup"><span data-stu-id="5dd80-123">The UI Automation requirements apply to all table controls where the UI framework/platform integrates UI Automation support for control types and control patterns.</span></span>

<span data-ttu-id="5dd80-124">В этом разделе содержатся следующие подразделы.</span><span class="sxs-lookup"><span data-stu-id="5dd80-124">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="5dd80-125">Типичная древовидная структура</span><span class="sxs-lookup"><span data-stu-id="5dd80-125">Typical Tree Structure</span></span>](#typical-tree-structure)
-   [<span data-ttu-id="5dd80-126">Соответствующие свойства</span><span class="sxs-lookup"><span data-stu-id="5dd80-126">Relevant Properties</span></span>](#relevant-properties)
-   [<span data-ttu-id="5dd80-127">Обязательные шаблоны элементов управления</span><span class="sxs-lookup"><span data-stu-id="5dd80-127">Required Control Patterns</span></span>](#required-control-patterns)
-   [<span data-ttu-id="5dd80-128">Обязательные события</span><span class="sxs-lookup"><span data-stu-id="5dd80-128">Required Events</span></span>](#required-events)
-   [<span data-ttu-id="5dd80-129">См. также</span><span class="sxs-lookup"><span data-stu-id="5dd80-129">Related topics</span></span>](#related-topics)

## <a name="typical-tree-structure"></a><span data-ttu-id="5dd80-130">Типичная древовидная структура</span><span class="sxs-lookup"><span data-stu-id="5dd80-130">Typical Tree Structure</span></span>

<span data-ttu-id="5dd80-131">В следующей таблице описывается типичный элемент управления и представление содержимого дерева модели автоматизации пользовательского интерфейса, которое относится к элементам управления "Таблица" и описывает, что может содержаться в каждом представлении.</span><span class="sxs-lookup"><span data-stu-id="5dd80-131">The following table depicts a typical control and content view of the UI Automation tree that pertains to table controls and describes what can be contained in each view.</span></span> <span data-ttu-id="5dd80-132">Дополнительные сведения о дереве автоматизации пользовательского интерфейса см. в разделе [Общие сведения о дереве модели автоматизации пользовательского интерфейса](uiauto-treeoverview.md).</span><span class="sxs-lookup"><span data-stu-id="5dd80-132">For more information about the UI Automation tree, see [UI Automation Tree Overview](uiauto-treeoverview.md).</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="5dd80-133">Представление элемента управления</span><span class="sxs-lookup"><span data-stu-id="5dd80-133">Control View</span></span></th>
<th><span data-ttu-id="5dd80-134">Представление содержимого</span><span class="sxs-lookup"><span data-stu-id="5dd80-134">Content View</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><ul>
<li><span data-ttu-id="5dd80-135">Таблица</span><span class="sxs-lookup"><span data-stu-id="5dd80-135">Table</span></span>
<ul>
<li><span data-ttu-id="5dd80-136">Text (0 или 1)</span><span class="sxs-lookup"><span data-stu-id="5dd80-136">Text (0 or 1)</span></span></li>
<li><span data-ttu-id="5dd80-137">Заголовок (0 или более)</span><span class="sxs-lookup"><span data-stu-id="5dd80-137">Header (0 or more)</span></span></li>
<li><span data-ttu-id="5dd80-138">Различные элементы управления (0 или более)</span><span class="sxs-lookup"><span data-stu-id="5dd80-138">Various controls (0 or more)</span></span></li>
</ul></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="5dd80-139">Таблица</span><span class="sxs-lookup"><span data-stu-id="5dd80-139">Table</span></span>
<ul>
<li><span data-ttu-id="5dd80-140">Текст (1 или более)</span><span class="sxs-lookup"><span data-stu-id="5dd80-140">Text (1 or more)</span></span></li>
<li><span data-ttu-id="5dd80-141">Различные элементы управления (0 или более)</span><span class="sxs-lookup"><span data-stu-id="5dd80-141">Various controls (0 or more)</span></span></li>
</ul></li>
</ul></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="5dd80-142">Если элемент управления "Таблица" содержит заголовки строк или столбцов, они должны быть представлены в представлении элемента управления дерева модели автоматизации пользовательского интерфейса.</span><span class="sxs-lookup"><span data-stu-id="5dd80-142">If a table control has row or column headers, they must be exposed in the control view of the UI Automation tree.</span></span> <span data-ttu-id="5dd80-143">Представлению содержимого не требуется предоставлять эти сведения, так как доступ к ним можно получить с помощью [**иуиаутоматионтаблепаттерн**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationtablepattern).</span><span class="sxs-lookup"><span data-stu-id="5dd80-143">The content view does not need to expose this information because it can be accessed using [**IUIAutomationTablePattern**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationtablepattern).</span></span>

## <a name="relevant-properties"></a><span data-ttu-id="5dd80-144">Соответствующие свойства</span><span class="sxs-lookup"><span data-stu-id="5dd80-144">Relevant Properties</span></span>

<span data-ttu-id="5dd80-145">В следующей таблице перечислены свойства модели автоматизации пользовательского интерфейса, значение или определение которых особенно важно для элементов управления таблицы.</span><span class="sxs-lookup"><span data-stu-id="5dd80-145">The following table lists the UI Automation properties whose value or definition is especially relevant to table controls.</span></span> <span data-ttu-id="5dd80-146">Дополнительные сведения о свойствах модели автоматизации пользовательского интерфейса см. в разделе [Получение свойств элементов модели автоматизации пользовательского интерфейса](uiauto-propertiesforclients.md).</span><span class="sxs-lookup"><span data-stu-id="5dd80-146">For more information about UI Automation properties, see [Retrieving Properties from UI Automation Elements](uiauto-propertiesforclients.md).</span></span>



| <span data-ttu-id="5dd80-147">Свойство модели автоматизации пользовательского интерфейса</span><span class="sxs-lookup"><span data-stu-id="5dd80-147">UI Automation Property</span></span>                                                                                              | <span data-ttu-id="5dd80-148">Значение</span><span class="sxs-lookup"><span data-stu-id="5dd80-148">Value</span></span>      | <span data-ttu-id="5dd80-149">Примечания</span><span class="sxs-lookup"><span data-stu-id="5dd80-149">Notes</span></span>                                                                                                                                                                                                                             |
|---------------------------------------------------------------------------------------------------------------------|------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="5dd80-150">**UIA \_ аутоматионидпропертид**</span><span class="sxs-lookup"><span data-stu-id="5dd80-150">**UIA\_AutomationIdPropertyId**</span></span>](uiauto-automation-element-propids.md)                 | <span data-ttu-id="5dd80-151">См. примечания.</span><span class="sxs-lookup"><span data-stu-id="5dd80-151">See notes.</span></span> | <span data-ttu-id="5dd80-152">Значение этого свойства должно быть уникальным среди всех одноранговых элементов в необработанном представлении дерева модели автоматизации пользовательского интерфейса.</span><span class="sxs-lookup"><span data-stu-id="5dd80-152">The value of this property must be unique among all peer elements in the raw view of the UI Automation tree.</span></span>                                                                                                                      |
| [<span data-ttu-id="5dd80-153">**UIA \_ баундингректанглепропертид**</span><span class="sxs-lookup"><span data-stu-id="5dd80-153">**UIA\_BoundingRectanglePropertyId**</span></span>](uiauto-automation-element-propids.md)       | <span data-ttu-id="5dd80-154">См. примечания.</span><span class="sxs-lookup"><span data-stu-id="5dd80-154">See notes.</span></span> | <span data-ttu-id="5dd80-155">Внешний прямоугольник, содержащий весь элемент управления.</span><span class="sxs-lookup"><span data-stu-id="5dd80-155">The outermost rectangle that contains the whole control.</span></span>                                                                                                                                                                          |
| [<span data-ttu-id="5dd80-156">**UIA \_ кликкаблепоинтпропертид**</span><span class="sxs-lookup"><span data-stu-id="5dd80-156">**UIA\_ClickablePointPropertyId**</span></span>](uiauto-automation-element-propids.md)             | <span data-ttu-id="5dd80-157">См. примечания.</span><span class="sxs-lookup"><span data-stu-id="5dd80-157">See notes.</span></span> | <span data-ttu-id="5dd80-158">Поддерживается при наличии ограничивающего прямоугольника.</span><span class="sxs-lookup"><span data-stu-id="5dd80-158">Supported if there is a bounding rectangle.</span></span> <span data-ttu-id="5dd80-159">Если не все точки внутри ограничивающего прямоугольника являются щелчками, а элемент выполняет специализированное тестирование нажатия, переопределите и предоставьте точку для щелчка.</span><span class="sxs-lookup"><span data-stu-id="5dd80-159">If not every point within the bounding rectangle is clickable, and the element performs specialized hit testing, override and provide a clickable point.</span></span>                              |
| [<span data-ttu-id="5dd80-160">**UIA \_ контролтипепропертид**</span><span class="sxs-lookup"><span data-stu-id="5dd80-160">**UIA\_ControlTypePropertyId**</span></span>](uiauto-automation-element-propids.md)                   | <span data-ttu-id="5dd80-161">**Таблица**</span><span class="sxs-lookup"><span data-stu-id="5dd80-161">**Table**</span></span>  |                                                                                                                                                                                                                                   |
| [<span data-ttu-id="5dd80-162">**UIA \_ дескрибедбипропертид**</span><span class="sxs-lookup"><span data-stu-id="5dd80-162">**UIA\_DescribedByPropertyId**</span></span>](uiauto-automation-element-propids.md)                   | <span data-ttu-id="5dd80-163">См. примечания.</span><span class="sxs-lookup"><span data-stu-id="5dd80-163">See notes.</span></span> | <span data-ttu-id="5dd80-164">Если у таблицы имеется заметка, предоставляемая другим элементом пользовательского интерфейса (например, текстовым элементом, содержащим описание таблицы), свойство DescribedBy должно предоставлять ссылку на элемент автоматизации элемента управления "Текст".</span><span class="sxs-lookup"><span data-stu-id="5dd80-164">If the table is annotated by other UI element (for example, a text element that holds the description for the table), the DescribedBy property should expose a reference to the automation element of the text control.</span></span>           |
| [<span data-ttu-id="5dd80-165">**UIA \_ хелптекстпропертид**</span><span class="sxs-lookup"><span data-stu-id="5dd80-165">**UIA\_HelpTextPropertyId**</span></span>](uiauto-automation-element-propids.md)                         | <span data-ttu-id="5dd80-166">См. примечания.</span><span class="sxs-lookup"><span data-stu-id="5dd80-166">See notes.</span></span> | <span data-ttu-id="5dd80-167">Дополнительные сведения о назначении таблицы должны предоставляться через это свойство, если оно недостаточно для объяснения свойством [**UIA \_ намепропертид**](uiauto-automation-element-propids.md) .</span><span class="sxs-lookup"><span data-stu-id="5dd80-167">More details about the purpose of the table should be exposed through this property if it is not sufficiently explained by the [**UIA\_NamePropertyId**](uiauto-automation-element-propids.md) property.</span></span>      |
| [<span data-ttu-id="5dd80-168">**UIA \_ исконтентелементпропертид**</span><span class="sxs-lookup"><span data-stu-id="5dd80-168">**UIA\_IsContentElementPropertyId**</span></span>](uiauto-automation-element-propids.md)         | <span data-ttu-id="5dd80-169">true</span><span class="sxs-lookup"><span data-stu-id="5dd80-169">TRUE</span></span>       | <span data-ttu-id="5dd80-170">Элемент управления "Таблица" всегда должен отображаться в представлении содержимого дерева модели автоматизации пользовательского интерфейса.</span><span class="sxs-lookup"><span data-stu-id="5dd80-170">The table control must always appear in the content view of the UI Automation tree.</span></span>                                                                                                                                               |
| [<span data-ttu-id="5dd80-171">**UIA \_ исконтролелементпропертид**</span><span class="sxs-lookup"><span data-stu-id="5dd80-171">**UIA\_IsControlElementPropertyId**</span></span>](uiauto-automation-element-propids.md)         | <span data-ttu-id="5dd80-172">true</span><span class="sxs-lookup"><span data-stu-id="5dd80-172">TRUE</span></span>       | <span data-ttu-id="5dd80-173">Элемент управления "Таблица" всегда должен отображаться в представлении элемента управления дерева модели автоматизации пользовательского интерфейса.</span><span class="sxs-lookup"><span data-stu-id="5dd80-173">The table control must always appear in the control view of the UI Automation tree.</span></span>                                                                                                                                               |
| [<span data-ttu-id="5dd80-174">**UIA \_ искэйбоардфокусаблепропертид**</span><span class="sxs-lookup"><span data-stu-id="5dd80-174">**UIA\_IsKeyboardFocusablePropertyId**</span></span>](uiauto-automation-element-propids.md)   | <span data-ttu-id="5dd80-175">См. примечания.</span><span class="sxs-lookup"><span data-stu-id="5dd80-175">See notes.</span></span> | <span data-ttu-id="5dd80-176">Если элемент управления может получать фокус клавиатуры, он должен поддерживать это свойство.</span><span class="sxs-lookup"><span data-stu-id="5dd80-176">If the control can receive keyboard focus, it must support this property.</span></span>                                                                                                                                                         |
| [<span data-ttu-id="5dd80-177">**UIA \_ лабеледбипропертид**</span><span class="sxs-lookup"><span data-stu-id="5dd80-177">**UIA\_LabeledByPropertyId**</span></span>](uiauto-automation-element-propids.md)                       | <span data-ttu-id="5dd80-178">См. примечания.</span><span class="sxs-lookup"><span data-stu-id="5dd80-178">See notes.</span></span> | <span data-ttu-id="5dd80-179">Если статическая текстовая метка присутствует, это свойство должно предоставлять ссылку на элемент автоматизации элемента управления.</span><span class="sxs-lookup"><span data-stu-id="5dd80-179">If there is a static text label, this property should expose a reference to the automation element of the control.</span></span>                                                                                                                |
| [<span data-ttu-id="5dd80-180">**UIA \_ локализедконтролтипепропертид**</span><span class="sxs-lookup"><span data-stu-id="5dd80-180">**UIA\_LocalizedControlTypePropertyId**</span></span>](uiauto-automation-element-propids.md) | <span data-ttu-id="5dd80-181">См. примечания.</span><span class="sxs-lookup"><span data-stu-id="5dd80-181">See notes.</span></span> | <span data-ttu-id="5dd80-182">Локализованная строка, соответствующая типу элемента управления **Table** .</span><span class="sxs-lookup"><span data-stu-id="5dd80-182">Localized string corresponding to the **Table** control type.</span></span> <span data-ttu-id="5dd80-183">Значение по умолчанию — "Table" для en-US или English (США).</span><span class="sxs-lookup"><span data-stu-id="5dd80-183">The default value is "table" for en-US or English (United States).</span></span>                                                                                                  |
| [<span data-ttu-id="5dd80-184">**UIA \_ намепропертид**</span><span class="sxs-lookup"><span data-stu-id="5dd80-184">**UIA\_NamePropertyId**</span></span>](uiauto-automation-element-propids.md)                                 | <span data-ttu-id="5dd80-185">См. примечания.</span><span class="sxs-lookup"><span data-stu-id="5dd80-185">See notes.</span></span> | <span data-ttu-id="5dd80-186">Элемент управления "Таблица" обычно получает значение имени из статической текстовой метки.</span><span class="sxs-lookup"><span data-stu-id="5dd80-186">The table control typically gets the value for its name from a static text label.</span></span> <span data-ttu-id="5dd80-187">Если статическая текстовая метка отсутствует, элемент должен назначить свойство Name, которое всегда должно быть доступно для объяснения назначения таблицы.</span><span class="sxs-lookup"><span data-stu-id="5dd80-187">If there is not a static text label, the element must assign a Name property that must always be available to explain the purpose of the table.</span></span> |



 

## <a name="required-control-patterns"></a><span data-ttu-id="5dd80-188">Обязательные шаблоны элементов управления</span><span class="sxs-lookup"><span data-stu-id="5dd80-188">Required Control Patterns</span></span>

<span data-ttu-id="5dd80-189">В следующей таблице перечислены шаблоны элементов управления модели автоматизации пользовательского интерфейса, которые должны поддерживаться всеми элементами управления "Таблица".</span><span class="sxs-lookup"><span data-stu-id="5dd80-189">The following table lists the UI Automation control patterns required to be supported by all table controls.</span></span> <span data-ttu-id="5dd80-190">Дополнительные сведения о шаблонах элементов управления см. в разделе [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md).</span><span class="sxs-lookup"><span data-stu-id="5dd80-190">For more information on control patterns, see [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md).</span></span>



| <span data-ttu-id="5dd80-191">Шаблон элемента управления</span><span class="sxs-lookup"><span data-stu-id="5dd80-191">Control Pattern</span></span>                                         | <span data-ttu-id="5dd80-192">Поддержка</span><span class="sxs-lookup"><span data-stu-id="5dd80-192">Support</span></span>                     | <span data-ttu-id="5dd80-193">Примечания</span><span class="sxs-lookup"><span data-stu-id="5dd80-193">Notes</span></span>                                                                                                                                                                                                                                                                                        |
|---------------------------------------------------------|-----------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="5dd80-194">**IGridProvider**</span><span class="sxs-lookup"><span data-stu-id="5dd80-194">**IGridProvider**</span></span>](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-igridprovider)           | <span data-ttu-id="5dd80-195">Обязательно</span><span class="sxs-lookup"><span data-stu-id="5dd80-195">Required</span></span>                    | <span data-ttu-id="5dd80-196">Поскольку элемент управления "Таблица" содержит элементы, представленные в сетке, он всегда поддерживает шаблон элемента управления [Grid](uiauto-implementinggrid.md) .</span><span class="sxs-lookup"><span data-stu-id="5dd80-196">Because the table control contains items presented in a grid, it always supports the [Grid](uiauto-implementinggrid.md) control pattern.</span></span>                                                                                                                                                    |
| [<span data-ttu-id="5dd80-197">**IGridItemProvider**</span><span class="sxs-lookup"><span data-stu-id="5dd80-197">**IGridItemProvider**</span></span>](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-igriditemprovider)   | <span data-ttu-id="5dd80-198">Требуется с дочерними объектами</span><span class="sxs-lookup"><span data-stu-id="5dd80-198">Required with child objects</span></span> | <span data-ttu-id="5dd80-199">Внутренние объекты таблицы должны поддерживать шаблоны элементов управления [GridItem](uiauto-implementinggriditem.md) и [TableItem](uiauto-implementingtableitem.md) .</span><span class="sxs-lookup"><span data-stu-id="5dd80-199">The inner objects of a table should support both the [GridItem](uiauto-implementinggriditem.md) and [TableItem](uiauto-implementingtableitem.md) control patterns.</span></span> <span data-ttu-id="5dd80-200">Сама таблица не должна поддерживать шаблон элемента управления GridItem или TableItem, если только таблица не является частью другой таблицы.</span><span class="sxs-lookup"><span data-stu-id="5dd80-200">The table itself need not support the GridItem or TableItem control pattern unless the table is part of another table.</span></span>  |
| [<span data-ttu-id="5dd80-201">**ITableProvider**</span><span class="sxs-lookup"><span data-stu-id="5dd80-201">**ITableProvider**</span></span>](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itableprovider)         | <span data-ttu-id="5dd80-202">Обязательно</span><span class="sxs-lookup"><span data-stu-id="5dd80-202">Required</span></span>                    | <span data-ttu-id="5dd80-203">Элемент управления "Таблица" всегда может иметь заголовки, связанные с содержимым.</span><span class="sxs-lookup"><span data-stu-id="5dd80-203">The table control can always have headers associated with the content.</span></span>                                                                                                                                                                                                                       |
| [<span data-ttu-id="5dd80-204">**ITableItemProvider**</span><span class="sxs-lookup"><span data-stu-id="5dd80-204">**ITableItemProvider**</span></span>](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itableitemprovider) | <span data-ttu-id="5dd80-205">Требуется с дочерними объектами</span><span class="sxs-lookup"><span data-stu-id="5dd80-205">Required with child objects</span></span> | <span data-ttu-id="5dd80-206">Внутренние объекты таблицы должны поддерживать шаблоны элементов управления [GridItem](uiauto-implementinggriditem.md) и [TableItem](uiauto-implementingtableitem.md) .</span><span class="sxs-lookup"><span data-stu-id="5dd80-206">The inner objects of a table should support both the [GridItem](uiauto-implementinggriditem.md) and [TableItem](uiauto-implementingtableitem.md) control patterns.</span></span> <span data-ttu-id="5dd80-207">Сама таблица не обязательно должна поддерживать шаблоны элементов управления GridItem или TableItem, если она не является частью другой таблицы.</span><span class="sxs-lookup"><span data-stu-id="5dd80-207">The table itself need not support the GridItem or TableItem control patterns unless the table is part of another table.</span></span> |



 

## <a name="required-events"></a><span data-ttu-id="5dd80-208">Обязательные события</span><span class="sxs-lookup"><span data-stu-id="5dd80-208">Required Events</span></span>

<span data-ttu-id="5dd80-209">В следующей таблице перечислены события автоматизации пользовательского интерфейса, которые должны поддерживаться элементами управления "Таблица".</span><span class="sxs-lookup"><span data-stu-id="5dd80-209">The following table lists the UI Automation events that table controls are required to support.</span></span> <span data-ttu-id="5dd80-210">Дополнительные сведения о событиях см. в разделе [UI Automation Events Overview](uiauto-eventsoverview.md).</span><span class="sxs-lookup"><span data-stu-id="5dd80-210">For more information on events, see [UI Automation Events Overview](uiauto-eventsoverview.md).</span></span>



| <span data-ttu-id="5dd80-211">Событие автоматизации пользовательского интерфейса</span><span class="sxs-lookup"><span data-stu-id="5dd80-211">UI Automation Event</span></span>                                                                                                                   | <span data-ttu-id="5dd80-212">Примечания</span><span class="sxs-lookup"><span data-stu-id="5dd80-212">Notes</span></span>                                                                                                                      |
|---------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="5dd80-213">**UIA \_ аутоматионфокусчанжедевентид**</span><span class="sxs-lookup"><span data-stu-id="5dd80-213">**UIA\_AutomationFocusChangedEventId**</span></span>](uiauto-event-ids.md)                                      |                                                                                                                            |
| <span data-ttu-id="5dd80-214">[**UIA \_**](uiauto-automation-element-propids.md) Событие изменения свойства баундингректанглепропертид.</span><span class="sxs-lookup"><span data-stu-id="5dd80-214">[**UIA\_BoundingRectanglePropertyId**](uiauto-automation-element-propids.md) property-changed event.</span></span> |                                                                                                                            |
| <span data-ttu-id="5dd80-215">[**UIA \_**](uiauto-automation-element-propids.md) Событие изменения свойства исенабледпропертид.</span><span class="sxs-lookup"><span data-stu-id="5dd80-215">[**UIA\_IsEnabledPropertyId**](uiauto-automation-element-propids.md) property-changed event.</span></span>                 | <span data-ttu-id="5dd80-216">Если элемент управления поддерживает свойство « [**включено**](uiauto-automation-element-propids.md) », оно должно поддерживать это событие.</span><span class="sxs-lookup"><span data-stu-id="5dd80-216">If the control supports the [**IsEnabled**](uiauto-automation-element-propids.md) property, it must support this event.</span></span>   |
| <span data-ttu-id="5dd80-217">[**UIA \_**](uiauto-automation-element-propids.md) Событие изменения свойства исоффскринпропертид.</span><span class="sxs-lookup"><span data-stu-id="5dd80-217">[**UIA\_IsOffscreenPropertyId**](uiauto-automation-element-propids.md) property-changed event.</span></span>             | <span data-ttu-id="5dd80-218">Если элемент управления поддерживает свойство [**исоффскрин**](uiauto-automation-element-propids.md) , он должен поддерживать это событие.</span><span class="sxs-lookup"><span data-stu-id="5dd80-218">If the control supports the [**IsOffscreen**](uiauto-automation-element-propids.md) property, it must support this event.</span></span> |
| [<span data-ttu-id="5dd80-219">**UIA \_ структуречанжедевентид**</span><span class="sxs-lookup"><span data-stu-id="5dd80-219">**UIA\_StructureChangedEventId**</span></span>](uiauto-event-ids.md)                                                  |                                                                                                                            |



 

## <a name="related-topics"></a><span data-ttu-id="5dd80-220">См. также</span><span class="sxs-lookup"><span data-stu-id="5dd80-220">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="5dd80-221">**Зрения**</span><span class="sxs-lookup"><span data-stu-id="5dd80-221">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="5dd80-222">Общие сведения о типах элементов управления автоматизации пользовательского интерфейса</span><span class="sxs-lookup"><span data-stu-id="5dd80-222">UI Automation Control Types Overview</span></span>](uiauto-controltypesoverview.md)
</dt> <dt>

[<span data-ttu-id="5dd80-223">Общие сведения о модели автоматизации пользовательского интерфейса</span><span class="sxs-lookup"><span data-stu-id="5dd80-223">UI Automation Overview</span></span>](uiauto-uiautomationoverview.md)
</dt> </dl>

 

 




