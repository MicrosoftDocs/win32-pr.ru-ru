---
title: Тип элемента управления DataGrid
description: В этом разделе содержатся сведения о поддержке автоматизации пользовательского интерфейса Майкрософт для типа элемента управления DataGrid.
ms.assetid: 2381b302-37d6-4159-bb7d-862ae41af695
keywords:
- Модель автоматизации пользовательского интерфейса, поддержка типа элемента управления DataGrid
- Модель автоматизации пользовательского интерфейса, тип элемента управления DataGrid
- Модель автоматизации пользовательского интерфейса, древовидная структура для типа элемента управления DataGrid
- Модель автоматизации пользовательского интерфейса, свойства для типа элемента управления DataGrid
- Модель автоматизации пользовательского интерфейса, шаблоны элементов управления для типа элемента управления DataGrid
- Модель автоматизации пользовательского интерфейса, события для типа элемента управления DataGrid
- Древовидные структуры, тип элемента управления DataGrid
- свойства, тип элемента управления DataGrid
- шаблоны элементов управления, тип элемента управления DataGrid
- события, тип элемента управления DataGrid
- Поддержка типа элемента управления DataGrid
- Тип элемента управления DataGrid
- типы элементов управления, древовидная структура для типа элемента управления DataGrid
- типы элементов управления, шаблоны элементов управления для типа элемента управления DataGrid
- типы элементов управления, поддержка DataGrid
- типы элементов управления, DataGrid
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c8af1e35e062c778285d1cb7edcca9ac6192792b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103986411"
---
# <a name="datagrid-control-type"></a><span data-ttu-id="09a71-119">Тип элемента управления DataGrid</span><span class="sxs-lookup"><span data-stu-id="09a71-119">DataGrid Control Type</span></span>

<span data-ttu-id="09a71-120">В этом разделе содержатся сведения о поддержке автоматизации пользовательского интерфейса Майкрософт для типа элемента управления **DataGrid** .</span><span class="sxs-lookup"><span data-stu-id="09a71-120">This topic provides information about Microsoft UI Automation support for the **DataGrid** control type.</span></span>

<span data-ttu-id="09a71-121">Тип элемента управления **DataGrid** позволяет пользователю легко работать с элементами, содержащими данные или элементы автоматизации, представленные в столбцах или строках.</span><span class="sxs-lookup"><span data-stu-id="09a71-121">The **DataGrid** control type lets a user easily work with items that contain data or automation elements presented in columns or rows.</span></span> <span data-ttu-id="09a71-122">Элементы управления DataGrid имеют строки элементов и столбцы сведений об этих элементах.</span><span class="sxs-lookup"><span data-stu-id="09a71-122">Data grid controls have rows of items and columns of information about those items.</span></span> <span data-ttu-id="09a71-123">Элемент управления "представление списка" в проводнике Windows Vista — это пример, который поддерживает тип элемента управления **DataGrid** .</span><span class="sxs-lookup"><span data-stu-id="09a71-123">A list-view control in Windows Vista Explorer is an example that supports the **DataGrid** control type.</span></span>

<span data-ttu-id="09a71-124">В следующих разделах определяется необходимая древовидная структура модели автоматизации пользовательского интерфейса, свойства, шаблоны элементов управления и события для типа элемента управления **DataGrid** .</span><span class="sxs-lookup"><span data-stu-id="09a71-124">The following sections define the required UI Automation tree structure, properties, control patterns, and events for the **DataGrid** control type.</span></span> <span data-ttu-id="09a71-125">Требования к автоматизации пользовательского интерфейса применяются ко всем элементам управления "Сетка данных", в которых платформа или платформа пользовательского интерфейса интегрирует поддержку автоматизации пользовательского интерфейса для типов элементов управления и шаблонов элементов управления.</span><span class="sxs-lookup"><span data-stu-id="09a71-125">The UI Automation requirements apply to all data grid controls where the UI framework/platform integrates UI Automation support for control types and control patterns.</span></span>

<span data-ttu-id="09a71-126">В этом разделе содержатся следующие подразделы.</span><span class="sxs-lookup"><span data-stu-id="09a71-126">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="09a71-127">Типичная древовидная структура</span><span class="sxs-lookup"><span data-stu-id="09a71-127">Typical Tree Structure</span></span>](#typical-tree-structure)
-   [<span data-ttu-id="09a71-128">Соответствующие свойства</span><span class="sxs-lookup"><span data-stu-id="09a71-128">Relevant Properties</span></span>](#relevant-properties)
-   [<span data-ttu-id="09a71-129">Обязательные шаблоны элементов управления</span><span class="sxs-lookup"><span data-stu-id="09a71-129">Required Control Patterns</span></span>](#required-control-patterns)
-   [<span data-ttu-id="09a71-130">Обязательные события</span><span class="sxs-lookup"><span data-stu-id="09a71-130">Required Events</span></span>](#required-events)
-   [<span data-ttu-id="09a71-131">Пример типа элемента управления DataGrid</span><span class="sxs-lookup"><span data-stu-id="09a71-131">DataGrid Control Type Example</span></span>](#datagrid-control-type-example)
-   [<span data-ttu-id="09a71-132">См. также</span><span class="sxs-lookup"><span data-stu-id="09a71-132">Related topics</span></span>](#related-topics)

## <a name="typical-tree-structure"></a><span data-ttu-id="09a71-133">Типичная древовидная структура</span><span class="sxs-lookup"><span data-stu-id="09a71-133">Typical Tree Structure</span></span>

<span data-ttu-id="09a71-134">В следующей таблице описывается типичный элемент управления и представление содержимого дерева модели автоматизации пользовательского интерфейса, относящиеся к элементам управления "Сетка данных", и показывается, что может содержаться в каждом представлении.</span><span class="sxs-lookup"><span data-stu-id="09a71-134">The following table depicts a typical control and content view of the UI Automation tree that pertains to data grid controls and describes what can be contained in each view.</span></span> <span data-ttu-id="09a71-135">Дополнительные сведения о дереве автоматизации пользовательского интерфейса см. в разделе [Общие сведения о дереве модели автоматизации пользовательского интерфейса](uiauto-treeoverview.md).</span><span class="sxs-lookup"><span data-stu-id="09a71-135">For more information about the UI Automation tree, see [UI Automation Tree Overview](uiauto-treeoverview.md).</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="09a71-136">Представление элемента управления</span><span class="sxs-lookup"><span data-stu-id="09a71-136">Control View</span></span></th>
<th><span data-ttu-id="09a71-137">Представление содержимого</span><span class="sxs-lookup"><span data-stu-id="09a71-137">Content View</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><ul>
<li><span data-ttu-id="09a71-138">DataGrid</span><span class="sxs-lookup"><span data-stu-id="09a71-138">DataGrid</span></span>
<ul>
<li><span data-ttu-id="09a71-139">Заголовок {0, 1 или 2}</span><span class="sxs-lookup"><span data-stu-id="09a71-139">Header (0, 1, or 2)</span></span>
<ul>
<li><span data-ttu-id="09a71-140">HeaderItem (количество столбцов или строк)</span><span class="sxs-lookup"><span data-stu-id="09a71-140">HeaderItem (number of columns or rows)</span></span></li>
</ul></li>
<li><span data-ttu-id="09a71-141">DataItem (0 или более; может быть структурирован в иерархии)</span><span class="sxs-lookup"><span data-stu-id="09a71-141">DataItem (0 or more; can be structured in a hierarchy)</span></span></li>
</ul></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="09a71-142">DataGrid</span><span class="sxs-lookup"><span data-stu-id="09a71-142">DataGrid</span></span>
<ul>
<li><span data-ttu-id="09a71-143">DataItem (0 или более; может быть структурирован в иерархии)</span><span class="sxs-lookup"><span data-stu-id="09a71-143">DataItem (0 or more; can be structured in a hierarchy)</span></span></li>
</ul></li>
</ul></td>
</tr>
</tbody>
</table>



 

## <a name="relevant-properties"></a><span data-ttu-id="09a71-144">Соответствующие свойства</span><span class="sxs-lookup"><span data-stu-id="09a71-144">Relevant Properties</span></span>

<span data-ttu-id="09a71-145">В следующей таблице перечислены свойства модели автоматизации пользовательского интерфейса, значения или определения которых особенно важны для типа элемента управления **DataGrid** .</span><span class="sxs-lookup"><span data-stu-id="09a71-145">The following table lists the UI Automation properties whose value or definition is especially relevant to the **DataGrid** control type.</span></span> <span data-ttu-id="09a71-146">Дополнительные сведения о свойствах модели автоматизации пользовательского интерфейса см. в разделе [Получение свойств элементов модели автоматизации пользовательского интерфейса](uiauto-propertiesforclients.md).</span><span class="sxs-lookup"><span data-stu-id="09a71-146">For more information about UI Automation properties, see [Retrieving Properties from UI Automation Elements](uiauto-propertiesforclients.md).</span></span>



| <span data-ttu-id="09a71-147">Свойство модели автоматизации пользовательского интерфейса</span><span class="sxs-lookup"><span data-stu-id="09a71-147">UI Automation Property</span></span>                                                                                              | <span data-ttu-id="09a71-148">Значение</span><span class="sxs-lookup"><span data-stu-id="09a71-148">Value</span></span>        | <span data-ttu-id="09a71-149">Примечания</span><span class="sxs-lookup"><span data-stu-id="09a71-149">Notes</span></span>                                                                                                                                                                                                                                                                                                        |
|---------------------------------------------------------------------------------------------------------------------|--------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="09a71-150">**UIA \_ аутоматионидпропертид**</span><span class="sxs-lookup"><span data-stu-id="09a71-150">**UIA\_AutomationIdPropertyId**</span></span>](uiauto-automation-element-propids.md)                 | <span data-ttu-id="09a71-151">См. примечания.</span><span class="sxs-lookup"><span data-stu-id="09a71-151">See notes.</span></span>   | <span data-ttu-id="09a71-152">Значение этого свойства должно быть уникальным среди всех одноранговых элементов в необработанном представлении дерева модели автоматизации пользовательского интерфейса.</span><span class="sxs-lookup"><span data-stu-id="09a71-152">The value of this property must be unique among all peer elements in the raw view of the UI Automation tree.</span></span>                                                                                                                                                                                                 |
| [<span data-ttu-id="09a71-153">**UIA \_ баундингректанглепропертид**</span><span class="sxs-lookup"><span data-stu-id="09a71-153">**UIA\_BoundingRectanglePropertyId**</span></span>](uiauto-automation-element-propids.md)       | <span data-ttu-id="09a71-154">См. примечания.</span><span class="sxs-lookup"><span data-stu-id="09a71-154">See notes.</span></span>   | <span data-ttu-id="09a71-155">Внешний прямоугольник, содержащий весь элемент управления.</span><span class="sxs-lookup"><span data-stu-id="09a71-155">The outermost rectangle that contains the whole control.</span></span>                                                                                                                                                                                                                                                     |
| [<span data-ttu-id="09a71-156">**UIA \_ кликкаблепоинтпропертид**</span><span class="sxs-lookup"><span data-stu-id="09a71-156">**UIA\_ClickablePointPropertyId**</span></span>](uiauto-automation-element-propids.md)             | <span data-ttu-id="09a71-157">См. примечания.</span><span class="sxs-lookup"><span data-stu-id="09a71-157">See notes.</span></span>   | <span data-ttu-id="09a71-158">Поддерживается при наличии ограничивающего прямоугольника.</span><span class="sxs-lookup"><span data-stu-id="09a71-158">Supported if there is a bounding rectangle.</span></span> <span data-ttu-id="09a71-159">Если не все точки внутри ограничивающего прямоугольника являются щелчками, а элемент выполняет специализированное тестирование нажатия, переопределите и предоставьте точку для щелчка.</span><span class="sxs-lookup"><span data-stu-id="09a71-159">If not every point within the bounding rectangle is clickable, and the element performs specialized hit testing, override and provide a clickable point.</span></span>                                                                                                         |
| [<span data-ttu-id="09a71-160">**UIA \_ контролтипепропертид**</span><span class="sxs-lookup"><span data-stu-id="09a71-160">**UIA\_ControlTypePropertyId**</span></span>](uiauto-automation-element-propids.md)                   | <span data-ttu-id="09a71-161">**DataGrid**</span><span class="sxs-lookup"><span data-stu-id="09a71-161">**DataGrid**</span></span> |                                                                                                                                                                                                                                                                                                              |
| [<span data-ttu-id="09a71-162">**UIA \_ исконтентелементпропертид**</span><span class="sxs-lookup"><span data-stu-id="09a71-162">**UIA\_IsContentElementPropertyId**</span></span>](uiauto-automation-element-propids.md)         | <span data-ttu-id="09a71-163">true</span><span class="sxs-lookup"><span data-stu-id="09a71-163">TRUE</span></span>         | <span data-ttu-id="09a71-164">Значение этого свойства всегда должно быть **true**.</span><span class="sxs-lookup"><span data-stu-id="09a71-164">The value of this property must always be **TRUE**.</span></span> <span data-ttu-id="09a71-165">Это означает, что элемент управления "Сетка данных" всегда должен находиться в представлении содержимого дерева модели автоматизации пользовательского интерфейса.</span><span class="sxs-lookup"><span data-stu-id="09a71-165">This means that the data grid control must always be in the content view of the UI Automation tree.</span></span>                                                                                                                                                      |
| [<span data-ttu-id="09a71-166">**UIA \_ исконтролелементпропертид**</span><span class="sxs-lookup"><span data-stu-id="09a71-166">**UIA\_IsControlElementPropertyId**</span></span>](uiauto-automation-element-propids.md)         | <span data-ttu-id="09a71-167">true</span><span class="sxs-lookup"><span data-stu-id="09a71-167">TRUE</span></span>         | <span data-ttu-id="09a71-168">Значение этого свойства всегда должно быть **true**.</span><span class="sxs-lookup"><span data-stu-id="09a71-168">The value of this property must always **TRUE**.</span></span> <span data-ttu-id="09a71-169">Это означает, что элемент управления "Сетка данных" всегда должен включаться в представление элемента управления дерева модели автоматизации пользовательского интерфейса.</span><span class="sxs-lookup"><span data-stu-id="09a71-169">This means that the data grid control must always be included in the control view of the UI Automation tree.</span></span>                                                                                                                                                |
| [<span data-ttu-id="09a71-170">**UIA \_ искэйбоардфокусаблепропертид**</span><span class="sxs-lookup"><span data-stu-id="09a71-170">**UIA\_IsKeyboardFocusablePropertyId**</span></span>](uiauto-automation-element-propids.md)   | <span data-ttu-id="09a71-171">См. примечания.</span><span class="sxs-lookup"><span data-stu-id="09a71-171">See notes.</span></span>   | <span data-ttu-id="09a71-172">Если элемент управления может получать фокус клавиатуры, он должен поддерживать это свойство.</span><span class="sxs-lookup"><span data-stu-id="09a71-172">If the control can receive keyboard focus, it must support this property.</span></span>                                                                                                                                                                                                                                    |
| [<span data-ttu-id="09a71-173">**UIA \_ лабеледбипропертид**</span><span class="sxs-lookup"><span data-stu-id="09a71-173">**UIA\_LabeledByPropertyId**</span></span>](uiauto-automation-element-propids.md)                       | <span data-ttu-id="09a71-174">См. примечания.</span><span class="sxs-lookup"><span data-stu-id="09a71-174">See notes.</span></span>   | <span data-ttu-id="09a71-175">Если имеется статическая текстовая метка, это свойство должно предоставлять ссылку на этот элемент управления.</span><span class="sxs-lookup"><span data-stu-id="09a71-175">If there is a static text label, this property must expose a reference to that control.</span></span>                                                                                                                                                                                                                      |
| [<span data-ttu-id="09a71-176">**UIA \_ локализедконтролтипепропертид**</span><span class="sxs-lookup"><span data-stu-id="09a71-176">**UIA\_LocalizedControlTypePropertyId**</span></span>](uiauto-automation-element-propids.md) | <span data-ttu-id="09a71-177">См. примечания.</span><span class="sxs-lookup"><span data-stu-id="09a71-177">See notes.</span></span>   | <span data-ttu-id="09a71-178">Локализованная строка, соответствующая типу элемента управления **DataGrid** .</span><span class="sxs-lookup"><span data-stu-id="09a71-178">Localized string corresponding to the **DataGrid** control type.</span></span> <span data-ttu-id="09a71-179">Значение по умолчанию — "Сетка данных" для en-US или English (США).</span><span class="sxs-lookup"><span data-stu-id="09a71-179">The default value is "data grid" for en-US or English (United States).</span></span>                                                                                                                                                                      |
| [<span data-ttu-id="09a71-180">**UIA \_ намепропертид**</span><span class="sxs-lookup"><span data-stu-id="09a71-180">**UIA\_NamePropertyId**</span></span>](uiauto-automation-element-propids.md)                                 | <span data-ttu-id="09a71-181">См. примечания.</span><span class="sxs-lookup"><span data-stu-id="09a71-181">See notes.</span></span>   | <span data-ttu-id="09a71-182">Элемент управления "Сетка данных" обычно получает значение для свойства " **имя** " из статической текстовой метки.</span><span class="sxs-lookup"><span data-stu-id="09a71-182">The data grid control typically gets the value for its **Name** property from a static text label.</span></span> <span data-ttu-id="09a71-183">Если статическая текстовая метка не существует, разработчик приложения должен присвоить значение свойству **Name** .</span><span class="sxs-lookup"><span data-stu-id="09a71-183">If there is not a static text label an application developer must assign a value to for the **Name** property.</span></span> <span data-ttu-id="09a71-184">Значение свойства **Name** никогда не должно быть текстовым содержимым элемента управления "поле ввода".</span><span class="sxs-lookup"><span data-stu-id="09a71-184">The value of the **Name** property must never be the textual contents of the edit control.</span></span> |



 

## <a name="required-control-patterns"></a><span data-ttu-id="09a71-185">Обязательные шаблоны элементов управления</span><span class="sxs-lookup"><span data-stu-id="09a71-185">Required Control Patterns</span></span>

<span data-ttu-id="09a71-186">В следующей таблице перечислены шаблоны элементов управления модели автоматизации пользовательского интерфейса, которые должны поддерживаться всеми элементами управления "Сетка данных".</span><span class="sxs-lookup"><span data-stu-id="09a71-186">The following table lists the UI Automation control patterns required to be supported by all data grid controls.</span></span> <span data-ttu-id="09a71-187">Дополнительные сведения о шаблонах элементов управления см. в разделе [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md).</span><span class="sxs-lookup"><span data-stu-id="09a71-187">For more information on control patterns, see [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md).</span></span>



| <span data-ttu-id="09a71-188">Шаблон элемента управления</span><span class="sxs-lookup"><span data-stu-id="09a71-188">Control Pattern</span></span>                                         | <span data-ttu-id="09a71-189">Поддержка</span><span class="sxs-lookup"><span data-stu-id="09a71-189">Support</span></span>  | <span data-ttu-id="09a71-190">Примечания</span><span class="sxs-lookup"><span data-stu-id="09a71-190">Notes</span></span>                                                                                                                                                                             |
|---------------------------------------------------------|----------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="09a71-191">**IGridProvider**</span><span class="sxs-lookup"><span data-stu-id="09a71-191">**IGridProvider**</span></span>](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-igridprovider)           | <span data-ttu-id="09a71-192">Обязательно</span><span class="sxs-lookup"><span data-stu-id="09a71-192">Required</span></span> | <span data-ttu-id="09a71-193">Сам элемент управления "Сетка данных" всегда поддерживает шаблон элемента управления [Grid](uiauto-implementinggrid.md) , так как элементы, которые он содержит, имеют метаданные, которые располагаются в сетке.</span><span class="sxs-lookup"><span data-stu-id="09a71-193">The data grid control itself always supports the [Grid](uiauto-implementinggrid.md) control pattern because the items that it contains have metadata that is laid out in a grid.</span></span> |
| [<span data-ttu-id="09a71-194">**IScrollProvider**</span><span class="sxs-lookup"><span data-stu-id="09a71-194">**IScrollProvider**</span></span>](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iscrollprovider)       | <span data-ttu-id="09a71-195">Зависит</span><span class="sxs-lookup"><span data-stu-id="09a71-195">Depends</span></span>  | <span data-ttu-id="09a71-196">Возможность прокрутки сетки данных зависит от содержимого и наличия полос прокрутки.</span><span class="sxs-lookup"><span data-stu-id="09a71-196">The ability to scroll the data grid depends on content and whether scroll bars are present.</span></span>                                                                                       |
| [<span data-ttu-id="09a71-197">**ISelectionProvider**</span><span class="sxs-lookup"><span data-stu-id="09a71-197">**ISelectionProvider**</span></span>](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iselectionprovider) | <span data-ttu-id="09a71-198">Зависит</span><span class="sxs-lookup"><span data-stu-id="09a71-198">Depends</span></span>  | <span data-ttu-id="09a71-199">Возможность выбора сетки данных зависит от содержимого.</span><span class="sxs-lookup"><span data-stu-id="09a71-199">The ability to select the data grid depends on content.</span></span>                                                                                                                           |
| [<span data-ttu-id="09a71-200">**ITableProvider**</span><span class="sxs-lookup"><span data-stu-id="09a71-200">**ITableProvider**</span></span>](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itableprovider)         | <span data-ttu-id="09a71-201">Зависит</span><span class="sxs-lookup"><span data-stu-id="09a71-201">Depends</span></span>  | <span data-ttu-id="09a71-202">Элемент управления "Сетка данных" с заголовком должен поддерживать шаблон элемента управления [Table](uiauto-implementingtable.md) .</span><span class="sxs-lookup"><span data-stu-id="09a71-202">A data grid control that has a header should support the [Table](uiauto-implementingtable.md) control pattern.</span></span>                                                                   |



 

<span data-ttu-id="09a71-203">Элементы данных в контейнерах DataGrid будут поддерживать как минимум следующие шаблоны:</span><span class="sxs-lookup"><span data-stu-id="09a71-203">Data items within the data grid containers will support at a minimum:</span></span>

-   <span data-ttu-id="09a71-204">Шаблон элемента управления [SelectionItem](uiauto-implementingselectionitem.md) (если сетка данных доступна для выбора)</span><span class="sxs-lookup"><span data-stu-id="09a71-204">[SelectionItem](uiauto-implementingselectionitem.md) control pattern (if the data grid is selectable)</span></span>
-   <span data-ttu-id="09a71-205">Шаблон элемента управления [скроллитем](uiauto-implementingscrollitem.md) (если сетка данных доступна для прокрутки)</span><span class="sxs-lookup"><span data-stu-id="09a71-205">[ScrollItem](uiauto-implementingscrollitem.md) control pattern (if the data grid is scrollable)</span></span>
-   <span data-ttu-id="09a71-206">Шаблон элемента управления [GridItem](uiauto-implementinggriditem.md)</span><span class="sxs-lookup"><span data-stu-id="09a71-206">[GridItem](uiauto-implementinggriditem.md) control pattern</span></span>
-   <span data-ttu-id="09a71-207">Шаблон элемента управления [TableItem](uiauto-implementingtableitem.md) (если сетка данных имеет заголовок)</span><span class="sxs-lookup"><span data-stu-id="09a71-207">[TableItem](uiauto-implementingtableitem.md) control pattern (if the data grid has a header)</span></span>

## <a name="required-events"></a><span data-ttu-id="09a71-208">Обязательные события</span><span class="sxs-lookup"><span data-stu-id="09a71-208">Required Events</span></span>

<span data-ttu-id="09a71-209">В следующей таблице перечислены события автоматизации пользовательского интерфейса, которые должны поддерживаться элементами управления "Сетка данных".</span><span class="sxs-lookup"><span data-stu-id="09a71-209">The following table lists the UI Automation events that data grid controls are required to support.</span></span> <span data-ttu-id="09a71-210">Дополнительные сведения о событиях см. в разделе [UI Automation Events Overview](uiauto-eventsoverview.md).</span><span class="sxs-lookup"><span data-stu-id="09a71-210">For more information on events, see [UI Automation Events Overview](uiauto-eventsoverview.md).</span></span>



| <span data-ttu-id="09a71-211">Событие автоматизации пользовательского интерфейса</span><span class="sxs-lookup"><span data-stu-id="09a71-211">UI Automation Event</span></span>                                                                                                                                        | <span data-ttu-id="09a71-212">Примечания</span><span class="sxs-lookup"><span data-stu-id="09a71-212">Notes</span></span>                                                                                                                                                    |
|------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="09a71-213">**UIA \_ аутоматионфокусчанжедевентид**</span><span class="sxs-lookup"><span data-stu-id="09a71-213">**UIA\_AutomationFocusChangedEventId**</span></span>](uiauto-event-ids.md)                                                           |                                                                                                                                                          |
| <span data-ttu-id="09a71-214">[**UIA \_**](uiauto-automation-element-propids.md) Событие изменения свойства баундингректанглепропертид.</span><span class="sxs-lookup"><span data-stu-id="09a71-214">[**UIA\_BoundingRectanglePropertyId**](uiauto-automation-element-propids.md) property-changed event.</span></span>                      |                                                                                                                                                          |
| <span data-ttu-id="09a71-215">[**UIA \_**](uiauto-automation-element-propids.md) Событие изменения свойства исенабледпропертид.</span><span class="sxs-lookup"><span data-stu-id="09a71-215">[**UIA\_IsEnabledPropertyId**](uiauto-automation-element-propids.md) property-changed event.</span></span>                                      | <span data-ttu-id="09a71-216">Если элемент управления поддерживает свойство « [**включено**](uiauto-automation-element-propids.md) », оно должно поддерживать это событие.</span><span class="sxs-lookup"><span data-stu-id="09a71-216">If the control supports the [**IsEnabled**](uiauto-automation-element-propids.md) property, it must support this event.</span></span>                                 |
| <span data-ttu-id="09a71-217">[**UIA \_**](uiauto-automation-element-propids.md) Событие изменения свойства исоффскринпропертид.</span><span class="sxs-lookup"><span data-stu-id="09a71-217">[**UIA\_IsOffscreenPropertyId**](uiauto-automation-element-propids.md) property-changed event.</span></span>                                  | <span data-ttu-id="09a71-218">Если элемент управления поддерживает свойство [**исоффскрин**](uiauto-automation-element-propids.md) , он должен поддерживать это событие.</span><span class="sxs-lookup"><span data-stu-id="09a71-218">If the control supports the [**IsOffscreen**](uiauto-automation-element-propids.md) property, it must support this event.</span></span>                               |
| [<span data-ttu-id="09a71-219">**UIA \_ лайаутинвалидатедевентид**</span><span class="sxs-lookup"><span data-stu-id="09a71-219">**UIA\_LayoutInvalidatedEventId**</span></span>](uiauto-event-ids.md)                                                                     |                                                                                                                                                          |
| [<span data-ttu-id="09a71-220">**UIA \_ структуречанжедевентид**</span><span class="sxs-lookup"><span data-stu-id="09a71-220">**UIA\_StructureChangedEventId**</span></span>](uiauto-event-ids.md)                                                                       |                                                                                                                                                          |
| <span data-ttu-id="09a71-221">[**UIA \_**](uiauto-control-pattern-propids.md) Событие изменения свойства мултиплевиевкуррентвиевпропертид.</span><span class="sxs-lookup"><span data-stu-id="09a71-221">[**UIA\_MultipleViewCurrentViewPropertyId**](uiauto-control-pattern-propids.md) property-changed event.</span></span>             | <span data-ttu-id="09a71-222">Если элемент управления поддерживает свойство Куррентвиев шаблона элемента управления [мултиплевиев](uiauto-implementingmultipleview.md) , он должен поддерживать это событие.</span><span class="sxs-lookup"><span data-stu-id="09a71-222">If the control supports the CurrentView property of the [MultipleView](uiauto-implementingmultipleview.md) control pattern, it must support this event.</span></span> |
| <span data-ttu-id="09a71-223">[**UIA \_**](uiauto-control-pattern-propids.md) Событие изменения свойства скроллхоризонталлискроллаблепропертид.</span><span class="sxs-lookup"><span data-stu-id="09a71-223">[**UIA\_ScrollHorizontallyScrollablePropertyId**](uiauto-control-pattern-propids.md) property-changed event.</span></span>   | <span data-ttu-id="09a71-224">Если элемент управления поддерживает шаблон элемента управления [Scroll](uiauto-implementingscroll.md) , он должен поддерживать это событие.</span><span class="sxs-lookup"><span data-stu-id="09a71-224">If the control supports the [Scroll](uiauto-implementingscroll.md) control pattern, it must support this event.</span></span>                                         |
| <span data-ttu-id="09a71-225">[**UIA \_**](uiauto-control-pattern-propids.md) Событие изменения свойства скроллхоризонталскроллперцентпропертид.</span><span class="sxs-lookup"><span data-stu-id="09a71-225">[**UIA\_ScrollHorizontalScrollPercentPropertyId**](uiauto-control-pattern-propids.md) property-changed event.</span></span> | <span data-ttu-id="09a71-226">Если элемент управления поддерживает шаблон элемента управления [Scroll](uiauto-implementingscroll.md) , он должен поддерживать это событие.</span><span class="sxs-lookup"><span data-stu-id="09a71-226">If the control supports the [Scroll](uiauto-implementingscroll.md) control pattern, it must support this event.</span></span>                                         |
| <span data-ttu-id="09a71-227">[**UIA \_**](uiauto-control-pattern-propids.md) Событие изменения свойства скроллхоризонталвиевсизепропертид.</span><span class="sxs-lookup"><span data-stu-id="09a71-227">[**UIA\_ScrollHorizontalViewSizePropertyId**](uiauto-control-pattern-propids.md) property-changed event.</span></span>           | <span data-ttu-id="09a71-228">Если элемент управления поддерживает шаблон элемента управления [Scroll](uiauto-implementingscroll.md) , он должен поддерживать это событие.</span><span class="sxs-lookup"><span data-stu-id="09a71-228">If the control supports the [Scroll](uiauto-implementingscroll.md) control pattern, it must support this event.</span></span>                                         |
| <span data-ttu-id="09a71-229">[**UIA \_**](uiauto-control-pattern-propids.md) Событие изменения свойства скроллвертикалскроллперцентпропертид.</span><span class="sxs-lookup"><span data-stu-id="09a71-229">[**UIA\_ScrollVerticalScrollPercentPropertyId**](uiauto-control-pattern-propids.md) property-changed event.</span></span>     | <span data-ttu-id="09a71-230">Если элемент управления поддерживает шаблон элемента управления [Scroll](uiauto-implementingscroll.md) , он должен поддерживать это событие.</span><span class="sxs-lookup"><span data-stu-id="09a71-230">If the control supports the [Scroll](uiauto-implementingscroll.md) control pattern, it must support this event.</span></span>                                         |
| <span data-ttu-id="09a71-231">[**UIA \_**](uiauto-control-pattern-propids.md) Событие изменения свойства скроллвертикаллискроллаблепропертид.</span><span class="sxs-lookup"><span data-stu-id="09a71-231">[**UIA\_ScrollVerticallyScrollablePropertyId**](uiauto-control-pattern-propids.md) property-changed event.</span></span>       | <span data-ttu-id="09a71-232">Если элемент управления поддерживает шаблон элемента управления [Scroll](uiauto-implementingscroll.md) , он должен поддерживать это событие.</span><span class="sxs-lookup"><span data-stu-id="09a71-232">If the control supports the [Scroll](uiauto-implementingscroll.md) control pattern, it must support this event.</span></span>                                         |
| <span data-ttu-id="09a71-233">[**UIA \_**](uiauto-control-pattern-propids.md) Событие изменения свойства скроллвертикалвиевсизепропертид.</span><span class="sxs-lookup"><span data-stu-id="09a71-233">[**UIA\_ScrollVerticalViewSizePropertyId**](uiauto-control-pattern-propids.md) property-changed event.</span></span>               | <span data-ttu-id="09a71-234">Если элемент управления поддерживает шаблон элемента управления [Scroll](uiauto-implementingscroll.md) , он должен поддерживать это событие.</span><span class="sxs-lookup"><span data-stu-id="09a71-234">If the control supports the [Scroll](uiauto-implementingscroll.md) control pattern, it must support this event.</span></span>                                         |
| [<span data-ttu-id="09a71-235">**\_Выбор UIA \_ инвалидатедевентид**</span><span class="sxs-lookup"><span data-stu-id="09a71-235">**UIA\_Selection\_InvalidatedEventId**</span></span>](uiauto-event-ids.md)                                                            |                                                                                                                                                          |



 

## <a name="datagrid-control-type-example"></a><span data-ttu-id="09a71-236">Пример типа элемента управления DataGrid</span><span class="sxs-lookup"><span data-stu-id="09a71-236">DataGrid Control Type Example</span></span>

<span data-ttu-id="09a71-237">На следующем рисунке показан элемент управления "список-представление", реализующий тип элемента управления **DataGrid** .</span><span class="sxs-lookup"><span data-stu-id="09a71-237">The following image illustrates a list-view control that implements the **DataGrid** control type.</span></span>

![снимок экрана элемента управления "представление списка" с типом элемента управления DataGrid](images/datagridxmpl.jpg)

<span data-ttu-id="09a71-239">Ниже показано представление элемента управления и представление содержимого дерева модели автоматизации пользовательского интерфейса, относящиеся к элементу управления "представление списка".</span><span class="sxs-lookup"><span data-stu-id="09a71-239">The control view and the content view of the UI Automation tree that pertains to the list-view control is displayed below.</span></span> <span data-ttu-id="09a71-240">Шаблоны элементов управления для каждого элемента автоматизации отображаются в круглых скобках.</span><span class="sxs-lookup"><span data-stu-id="09a71-240">The control patterns for each automation element are shown in parentheses.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="09a71-241">Дерево модели автоматизации пользовательского интерфейса — представление элемента управления</span><span class="sxs-lookup"><span data-stu-id="09a71-241">UI Automation Tree - Control View</span></span></th>
<th><span data-ttu-id="09a71-242">Дерево модели автоматизации пользовательского интерфейса — представление содержимого</span><span class="sxs-lookup"><span data-stu-id="09a71-242">UI Automation Tree - Content View</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="09a71-243">DataGrid (сортировка, таблица, выбор, сетка)</span><span class="sxs-lookup"><span data-stu-id="09a71-243">DataGrid (Sort, Table, Selection, Grid)</span></span>
<ul>
<li><span data-ttu-id="09a71-244">Header</span><span class="sxs-lookup"><span data-stu-id="09a71-244">Header</span></span>
<ul>
<li><span data-ttu-id="09a71-245">&quot;Имя HeaderItem &quot; (Invoke)</span><span class="sxs-lookup"><span data-stu-id="09a71-245">HeaderItem &quot;Name&quot; (Invoke)</span></span></li>
<li><span data-ttu-id="09a71-246">HeaderItem &quot; Дата изменения &quot; (вызов)</span><span class="sxs-lookup"><span data-stu-id="09a71-246">HeaderItem &quot;Date Modified&quot; (Invoke)</span></span></li>
<li><span data-ttu-id="09a71-247">&quot;Размер HeaderItem &quot; (Invoke)</span><span class="sxs-lookup"><span data-stu-id="09a71-247">HeaderItem &quot;Size&quot; (Invoke)</span></span></li>
</ul></li>
<li><span data-ttu-id="09a71-248">Группа &quot; contoso &quot; (TableItem, GridItem, SelectionItem, таблица *, сетка*)</span><span class="sxs-lookup"><span data-stu-id="09a71-248">Group &quot;Contoso&quot; (TableItem, GridItem, SelectionItem, Table *, Grid*)</span></span>
<ul>
<li><span data-ttu-id="09a71-249">&quot;Receivable.docучетных записей DataItem &quot; (SelectionItem, Invoke, TableItem *, GridItem*)</span><span class="sxs-lookup"><span data-stu-id="09a71-249">DataItem &quot;Accounts Receivable.doc&quot; (SelectionItem, Invoke, TableItem *, GridItem*)</span></span></li>
<li><span data-ttu-id="09a71-250">&quot;Payable.docучетных записей DataItem &quot; (SelectionItem, Invoke, TableItem *, GridItem*)</span><span class="sxs-lookup"><span data-stu-id="09a71-250">DataItem &quot;Accounts Payable.doc&quot; (SelectionItem, Invoke, TableItem *, GridItem*)</span></span></li>
</ul></li>
</ul></td>
<td><span data-ttu-id="09a71-251">DataGrid (Table, Grid, Selection)</span><span class="sxs-lookup"><span data-stu-id="09a71-251">DataGrid (Table, Grid, Selection)</span></span>
<ul>
<li><span data-ttu-id="09a71-252">Группа &quot; contoso &quot; (TableItem, GridItem, SelectionItem, таблица *, сетка*)</span><span class="sxs-lookup"><span data-stu-id="09a71-252">Group &quot;Contoso&quot; (TableItem, GridItem, SelectionItem, Table *, Grid*)</span></span>
<ul>
<li><span data-ttu-id="09a71-253">&quot;Receivable.docучетных записей DataItem &quot; (SelectionItem, Invoke, TableItem *, GridItem*)</span><span class="sxs-lookup"><span data-stu-id="09a71-253">DataItem &quot;Accounts Receivable.doc&quot; (SelectionItem, Invoke, TableItem *, GridItem*)</span></span></li>
<li><span data-ttu-id="09a71-254">&quot;Payable.docучетных записей DataItem &quot; (SelectionItem, Invoke, TableItem *, GridItem*)</span><span class="sxs-lookup"><span data-stu-id="09a71-254">DataItem &quot;Accounts Payable.doc&quot; (SelectionItem, Invoke, TableItem *, GridItem*)</span></span></li>
</ul></li>
</ul></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="09a71-255">\*В предыдущем примере показана сетка данных, содержащая несколько уровней элементов управления.</span><span class="sxs-lookup"><span data-stu-id="09a71-255">\*The preceding example shows a data grid that contains multiple levels of controls.</span></span> <span data-ttu-id="09a71-256">Элемент управления **Group** ("contoso") содержит два элемента управления **DataItem** ("учетные записи Receivable.doc" и "учетные записи Payable.doc").</span><span class="sxs-lookup"><span data-stu-id="09a71-256">The **Group** ("Contoso") control contains two **DataItem** controls ("Accounts Receivable.doc" and "Accounts Payable.doc").</span></span> <span data-ttu-id="09a71-257">Пара элементов **управления DataGrid** /  не зависит от пары на другом уровне.</span><span class="sxs-lookup"><span data-stu-id="09a71-257">A **DataGrid**/**GridItem** pair is independent of a pair at another level.</span></span> <span data-ttu-id="09a71-258">Элементы управления **DataItem** в **группе** также могут быть представлены как тип элемента управления [ListItem](uiauto-supportlistitemcontroltype.md) , что позволяет более четко представить их как выбираемые объекты, а не как простые элементы данных.</span><span class="sxs-lookup"><span data-stu-id="09a71-258">The **DataItem** controls under a **Group** can also be exposed as a [ListItem](uiauto-supportlistitemcontroltype.md) control type, enabling them to be presented more clearly as selectable objects, rather than as simple data elements.</span></span> <span data-ttu-id="09a71-259">Этот пример не включает дочерние элементы сгруппированных элементов данных.</span><span class="sxs-lookup"><span data-stu-id="09a71-259">This example does not include the sub-elements of the grouped data items.</span></span> <span data-ttu-id="09a71-260">Еще один пример нескольких уровней элементов управления см. в разделе Тип элемента управления [DataItem](uiauto-supportdataitemcontroltype.md) .</span><span class="sxs-lookup"><span data-stu-id="09a71-260">For another example of multiple levels of controls, see the [DataItem](uiauto-supportdataitemcontroltype.md) control type.</span></span>

## <a name="related-topics"></a><span data-ttu-id="09a71-261">См. также</span><span class="sxs-lookup"><span data-stu-id="09a71-261">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="09a71-262">**Зрения**</span><span class="sxs-lookup"><span data-stu-id="09a71-262">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="09a71-263">Общие сведения о типах элементов управления автоматизации пользовательского интерфейса</span><span class="sxs-lookup"><span data-stu-id="09a71-263">UI Automation Control Types Overview</span></span>](uiauto-controltypesoverview.md)
</dt> <dt>

[<span data-ttu-id="09a71-264">Общие сведения о модели автоматизации пользовательского интерфейса</span><span class="sxs-lookup"><span data-stu-id="09a71-264">UI Automation Overview</span></span>](uiauto-uiautomationoverview.md)
</dt> </dl>

 

 




