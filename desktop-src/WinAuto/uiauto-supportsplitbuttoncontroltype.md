---
title: Тип элемента управления SplitButton
description: В этом разделе содержатся сведения о поддержке автоматизации пользовательского интерфейса Майкрософт для типа элемента управления SplitButton.
ms.assetid: ca4f8e45-7487-4a8b-9df5-edc2b0e56663
keywords:
- Модель автоматизации пользовательского интерфейса, поддержка типа элемента управления SplitButton
- Модель автоматизации пользовательского интерфейса, тип элемента управления SplitButton
- Модель автоматизации пользовательского интерфейса, древовидная структура для типа элемента управления SplitButton
- Модель автоматизации пользовательского интерфейса, свойства для типа элемента управления SplitButton
- Модель автоматизации пользовательского интерфейса, шаблоны элементов управления для типа элемента управления SplitButton
- Модель автоматизации пользовательского интерфейса, события для типа элемента управления SplitButton
- Древовидные структуры, тип элемента управления SplitButton
- свойства, тип элемента управления SplitButton
- шаблоны элементов управления, тип элемента управления SplitButton
- события, тип элемента управления SplitButton
- Поддержка типа элемента управления SplitButton
- Тип элемента управления SplitButton
- типы элементов управления, древовидная структура для типа элемента управления SplitButton
- типы элементов управления, шаблоны элементов управления для типа элемента управления SplitButton
- типы элементов управления, поддержка SplitButton
- типы элементов управления, SplitButton
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9c56cd6b22838dfa92ba25ce05e74d228f4173ac
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103778233"
---
# <a name="splitbutton-control-type"></a><span data-ttu-id="bc5fd-119">Тип элемента управления SplitButton</span><span class="sxs-lookup"><span data-stu-id="bc5fd-119">SplitButton Control Type</span></span>

<span data-ttu-id="bc5fd-120">В этом разделе содержатся сведения о поддержке автоматизации пользовательского интерфейса Майкрософт для типа элемента управления **SplitButton** .</span><span class="sxs-lookup"><span data-stu-id="bc5fd-120">This topic provides information about Microsoft UI Automation support for the **SplitButton** control type.</span></span>

<span data-ttu-id="bc5fd-121">Элемент управления "разворачивающаяся кнопка" позволяет выполнить действие над элементом управления и развернуть элемент управления, чтобы просмотреть список других возможных действий, которые можно выполнить.</span><span class="sxs-lookup"><span data-stu-id="bc5fd-121">The split button control enables an action to be performed on a control, and to expand the control to see a list of other possible actions that can be performed.</span></span>

<span data-ttu-id="bc5fd-122">В следующих разделах определяется необходимая древовидная структура модели автоматизации пользовательского интерфейса, свойства, шаблоны элементов управления и события для типа элемента управления **SplitButton** .</span><span class="sxs-lookup"><span data-stu-id="bc5fd-122">The following sections define the required UI Automation tree structure, properties, control patterns, and events for the **SplitButton** control type.</span></span> <span data-ttu-id="bc5fd-123">Требования к автоматизации пользовательского интерфейса применяются ко всем элементам управления "разворачивающаяся кнопка", в которых платформа или платформа пользовательского интерфейса интегрирует поддержку модели автоматизации пользовательского интерфейса для типов элементов управления и шаблонов элементов управления.</span><span class="sxs-lookup"><span data-stu-id="bc5fd-123">The UI Automation requirements apply to all split button controls where the UI framework/platform integrates UI Automation support for control types and control patterns.</span></span>

<span data-ttu-id="bc5fd-124">В этом разделе содержатся следующие подразделы.</span><span class="sxs-lookup"><span data-stu-id="bc5fd-124">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="bc5fd-125">Типичная древовидная структура</span><span class="sxs-lookup"><span data-stu-id="bc5fd-125">Typical Tree Structure</span></span>](#typical-tree-structure)
-   [<span data-ttu-id="bc5fd-126">Соответствующие свойства</span><span class="sxs-lookup"><span data-stu-id="bc5fd-126">Relevant Properties</span></span>](#relevant-properties)
-   [<span data-ttu-id="bc5fd-127">Обязательные шаблоны элементов управления</span><span class="sxs-lookup"><span data-stu-id="bc5fd-127">Required Control Patterns</span></span>](#required-control-patterns)
-   [<span data-ttu-id="bc5fd-128">Обязательные события</span><span class="sxs-lookup"><span data-stu-id="bc5fd-128">Required Events</span></span>](#required-events)
-   [<span data-ttu-id="bc5fd-129">Пример типа элемента управления SplitButton</span><span class="sxs-lookup"><span data-stu-id="bc5fd-129">SplitButton Control Type Example</span></span>](#splitbutton-control-type-example)
-   [<span data-ttu-id="bc5fd-130">См. также</span><span class="sxs-lookup"><span data-stu-id="bc5fd-130">Related topics</span></span>](#related-topics)

## <a name="typical-tree-structure"></a><span data-ttu-id="bc5fd-131">Типичная древовидная структура</span><span class="sxs-lookup"><span data-stu-id="bc5fd-131">Typical Tree Structure</span></span>

<span data-ttu-id="bc5fd-132">В следующей таблице представлен типичный элемент управления и представление содержимого дерева модели автоматизации пользовательского интерфейса, которое относится к элементам управления "разворачивающаяся кнопка" и описывает, что может содержаться в каждом представлении.</span><span class="sxs-lookup"><span data-stu-id="bc5fd-132">The following table depicts a typical control and content view of the UI Automation tree that pertains to split button controls and describes what can be contained in each view.</span></span> <span data-ttu-id="bc5fd-133">Дополнительные сведения о дереве автоматизации пользовательского интерфейса см. в разделе [Общие сведения о дереве модели автоматизации пользовательского интерфейса](uiauto-treeoverview.md).</span><span class="sxs-lookup"><span data-stu-id="bc5fd-133">For more information about the UI Automation tree, see [UI Automation Tree Overview](uiauto-treeoverview.md).</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="bc5fd-134">Представление элемента управления</span><span class="sxs-lookup"><span data-stu-id="bc5fd-134">Control View</span></span></th>
<th><span data-ttu-id="bc5fd-135">Представление содержимого</span><span class="sxs-lookup"><span data-stu-id="bc5fd-135">Content View</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><ul>
<li><span data-ttu-id="bc5fd-136">SplitButton</span><span class="sxs-lookup"><span data-stu-id="bc5fd-136">SplitButton</span></span>
<ul>
<li><span data-ttu-id="bc5fd-137">Image (0 или 1)</span><span class="sxs-lookup"><span data-stu-id="bc5fd-137">Image (0 or 1)</span></span></li>
<li><span data-ttu-id="bc5fd-138">Text (0 или 1)</span><span class="sxs-lookup"><span data-stu-id="bc5fd-138">Text (0 or 1)</span></span></li>
<li><span data-ttu-id="bc5fd-139">Button (1 или 2)</span><span class="sxs-lookup"><span data-stu-id="bc5fd-139">Button (1 or 2)</span></span>
<ul>
<li><span data-ttu-id="bc5fd-140">Меню (0 или 1; отображается как дочерний элемент вложенной кнопки, поддерживающей шаблон ExpandCollapse)</span><span class="sxs-lookup"><span data-stu-id="bc5fd-140">Menu (0 or 1; appears as a child of a sub-button that supports the ExpandCollapse pattern)</span></span>
<ul>
<li><span data-ttu-id="bc5fd-141">MenuItem (1 или более)</span><span class="sxs-lookup"><span data-stu-id="bc5fd-141">MenuItem (1 to many)</span></span></li>
</ul></li>
</ul></li>
</ul></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="bc5fd-142">SplitButton</span><span class="sxs-lookup"><span data-stu-id="bc5fd-142">SplitButton</span></span>
<ul>
<li><span data-ttu-id="bc5fd-143">Button (1 или 2)</span><span class="sxs-lookup"><span data-stu-id="bc5fd-143">Button (1 or 2)</span></span>
<ul>
<li><span data-ttu-id="bc5fd-144">MenuItem (1 или более)</span><span class="sxs-lookup"><span data-stu-id="bc5fd-144">MenuItem (1 to many)</span></span></li>
</ul></li>
</ul></li>
</ul></td>
</tr>
</tbody>
</table>



 

## <a name="relevant-properties"></a><span data-ttu-id="bc5fd-145">Соответствующие свойства</span><span class="sxs-lookup"><span data-stu-id="bc5fd-145">Relevant Properties</span></span>

<span data-ttu-id="bc5fd-146">В следующей таблице перечислены свойства модели автоматизации пользовательского интерфейса, значения или определения которых особенно важны для типа элемента управления **SplitButton** .</span><span class="sxs-lookup"><span data-stu-id="bc5fd-146">The following table lists the UI Automation properties whose value or definition is especially relevant to the **SplitButton** control type.</span></span> <span data-ttu-id="bc5fd-147">Дополнительные сведения о свойствах модели автоматизации пользовательского интерфейса см. в разделе [Получение свойств элементов модели автоматизации пользовательского интерфейса](uiauto-propertiesforclients.md).</span><span class="sxs-lookup"><span data-stu-id="bc5fd-147">For more information about UI Automation properties, see [Retrieving Properties from UI Automation Elements](uiauto-propertiesforclients.md).</span></span>



| <span data-ttu-id="bc5fd-148">Свойство модели автоматизации пользовательского интерфейса</span><span class="sxs-lookup"><span data-stu-id="bc5fd-148">UI Automation Property</span></span>                                                                                              | <span data-ttu-id="bc5fd-149">Значение</span><span class="sxs-lookup"><span data-stu-id="bc5fd-149">Value</span></span>           | <span data-ttu-id="bc5fd-150">Примечания</span><span class="sxs-lookup"><span data-stu-id="bc5fd-150">Notes</span></span>                                                                                                                                                                                                |
|---------------------------------------------------------------------------------------------------------------------|-----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="bc5fd-151">**UIA \_ аутоматионидпропертид**</span><span class="sxs-lookup"><span data-stu-id="bc5fd-151">**UIA\_AutomationIdPropertyId**</span></span>](uiauto-automation-element-propids.md)                 | <span data-ttu-id="bc5fd-152">См. примечания.</span><span class="sxs-lookup"><span data-stu-id="bc5fd-152">See notes.</span></span>      | <span data-ttu-id="bc5fd-153">Значение этого свойства должно быть уникальным среди всех одноранговых элементов в необработанном представлении дерева модели автоматизации пользовательского интерфейса.</span><span class="sxs-lookup"><span data-stu-id="bc5fd-153">The value of this property must be unique among all peer elements in the raw view of the UI Automation tree.</span></span>                                                                                         |
| [<span data-ttu-id="bc5fd-154">**UIA \_ баундингректанглепропертид**</span><span class="sxs-lookup"><span data-stu-id="bc5fd-154">**UIA\_BoundingRectanglePropertyId**</span></span>](uiauto-automation-element-propids.md)       | <span data-ttu-id="bc5fd-155">См. примечания.</span><span class="sxs-lookup"><span data-stu-id="bc5fd-155">See notes.</span></span>      | <span data-ttu-id="bc5fd-156">Внешний прямоугольник, содержащий весь элемент управления.</span><span class="sxs-lookup"><span data-stu-id="bc5fd-156">The outermost rectangle that contains the whole control.</span></span>                                                                                                                                             |
| [<span data-ttu-id="bc5fd-157">**UIA \_ кликкаблепоинтпропертид**</span><span class="sxs-lookup"><span data-stu-id="bc5fd-157">**UIA\_ClickablePointPropertyId**</span></span>](uiauto-automation-element-propids.md)             | <span data-ttu-id="bc5fd-158">См. примечания.</span><span class="sxs-lookup"><span data-stu-id="bc5fd-158">See notes.</span></span>      | <span data-ttu-id="bc5fd-159">Поддерживается при наличии ограничивающего прямоугольника.</span><span class="sxs-lookup"><span data-stu-id="bc5fd-159">Supported if there is a bounding rectangle.</span></span> <span data-ttu-id="bc5fd-160">Если не все точки внутри ограничивающего прямоугольника являются щелчками, а элемент выполняет специализированное тестирование нажатия, переопределите и предоставьте точку для щелчка.</span><span class="sxs-lookup"><span data-stu-id="bc5fd-160">If not every point within the bounding rectangle is clickable, and the element performs specialized hit testing, override and provide a clickable point.</span></span> |
| [<span data-ttu-id="bc5fd-161">**UIA \_ контролтипепропертид**</span><span class="sxs-lookup"><span data-stu-id="bc5fd-161">**UIA\_ControlTypePropertyId**</span></span>](uiauto-automation-element-propids.md)                   | <span data-ttu-id="bc5fd-162">**SplitButton**</span><span class="sxs-lookup"><span data-stu-id="bc5fd-162">**SplitButton**</span></span> | <span data-ttu-id="bc5fd-163">Это значение одинаково для всех инфраструктур пользовательского интерфейса.</span><span class="sxs-lookup"><span data-stu-id="bc5fd-163">This value is the same for all UI frameworks.</span></span>                                                                                                                                                        |
| [<span data-ttu-id="bc5fd-164">**UIA \_ хелптекстпропертид**</span><span class="sxs-lookup"><span data-stu-id="bc5fd-164">**UIA\_HelpTextPropertyId**</span></span>](uiauto-automation-element-propids.md)                         | <span data-ttu-id="bc5fd-165">См. примечания.</span><span class="sxs-lookup"><span data-stu-id="bc5fd-165">See notes.</span></span>      | <span data-ttu-id="bc5fd-166">Текст справки может указывать результат активации разворачивающейся кнопки и обычно предоставляет тот же тип сведений, что и подсказка.</span><span class="sxs-lookup"><span data-stu-id="bc5fd-166">The help text can indicate the result of activating the split button, which is typically the same type of information presented through a tooltip.</span></span>                                                   |
| [<span data-ttu-id="bc5fd-167">**UIA \_ исконтентелементпропертид**</span><span class="sxs-lookup"><span data-stu-id="bc5fd-167">**UIA\_IsContentElementPropertyId**</span></span>](uiauto-automation-element-propids.md)         | <span data-ttu-id="bc5fd-168">true</span><span class="sxs-lookup"><span data-stu-id="bc5fd-168">TRUE</span></span>            | <span data-ttu-id="bc5fd-169">Элемент управления "Разворачивающаяся кнопка" содержит сведения для конечного пользователя.</span><span class="sxs-lookup"><span data-stu-id="bc5fd-169">The split button control contains information for the end user.</span></span>                                                                                                                                      |
| [<span data-ttu-id="bc5fd-170">**UIA \_ исконтролелементпропертид**</span><span class="sxs-lookup"><span data-stu-id="bc5fd-170">**UIA\_IsControlElementPropertyId**</span></span>](uiauto-automation-element-propids.md)         | <span data-ttu-id="bc5fd-171">true</span><span class="sxs-lookup"><span data-stu-id="bc5fd-171">TRUE</span></span>            | <span data-ttu-id="bc5fd-172">Элемент управления "Разворачивающаяся кнопка" является видимым для конечного пользователя.</span><span class="sxs-lookup"><span data-stu-id="bc5fd-172">The split button control is visible to the end user.</span></span>                                                                                                                                                 |
| [<span data-ttu-id="bc5fd-173">**UIA \_ искэйбоардфокусаблепропертид**</span><span class="sxs-lookup"><span data-stu-id="bc5fd-173">**UIA\_IsKeyboardFocusablePropertyId**</span></span>](uiauto-automation-element-propids.md)   | <span data-ttu-id="bc5fd-174">См. примечания.</span><span class="sxs-lookup"><span data-stu-id="bc5fd-174">See notes.</span></span>      | <span data-ttu-id="bc5fd-175">Если элемент управления может получать фокус клавиатуры, он должен поддерживать это свойство.</span><span class="sxs-lookup"><span data-stu-id="bc5fd-175">If the control can receive keyboard focus, it must support this property.</span></span>                                                                                                                            |
| [<span data-ttu-id="bc5fd-176">**UIA \_ лабеледбипропертид**</span><span class="sxs-lookup"><span data-stu-id="bc5fd-176">**UIA\_LabeledByPropertyId**</span></span>](uiauto-automation-element-propids.md)                       | <span data-ttu-id="bc5fd-177">NULL</span><span class="sxs-lookup"><span data-stu-id="bc5fd-177">NULL</span></span>            | <span data-ttu-id="bc5fd-178">Элементы управления "Разворачивающаяся кнопка" не имеют меток со статическим текстом.</span><span class="sxs-lookup"><span data-stu-id="bc5fd-178">Split button controls do not have a static text label.</span></span>                                                                                                                                               |
| [<span data-ttu-id="bc5fd-179">**UIA \_ локализедконтролтипепропертид**</span><span class="sxs-lookup"><span data-stu-id="bc5fd-179">**UIA\_LocalizedControlTypePropertyId**</span></span>](uiauto-automation-element-propids.md) | <span data-ttu-id="bc5fd-180">См. примечания.</span><span class="sxs-lookup"><span data-stu-id="bc5fd-180">See notes.</span></span>      | <span data-ttu-id="bc5fd-181">Локализованная строка, соответствующая типу элемента управления **SplitButton** .</span><span class="sxs-lookup"><span data-stu-id="bc5fd-181">Localized string corresponding to the **SplitButton** control type.</span></span> <span data-ttu-id="bc5fd-182">Значение по умолчанию — "разворачивающаяся кнопка" для en-US или English (США).</span><span class="sxs-lookup"><span data-stu-id="bc5fd-182">The default value is "split button" for en-US or English (United States).</span></span>                                                        |
| [<span data-ttu-id="bc5fd-183">**UIA \_ намепропертид**</span><span class="sxs-lookup"><span data-stu-id="bc5fd-183">**UIA\_NamePropertyId**</span></span>](uiauto-automation-element-propids.md)                                 | <span data-ttu-id="bc5fd-184">См. примечания.</span><span class="sxs-lookup"><span data-stu-id="bc5fd-184">See notes.</span></span>      | <span data-ttu-id="bc5fd-185">Текст, который используется для добавления метки к разворачивающейся кнопке.</span><span class="sxs-lookup"><span data-stu-id="bc5fd-185">The text that is used to label the split button.</span></span> <span data-ttu-id="bc5fd-186">Каждый раз, когда изображение используется для обозначения разворачивающейся кнопки, для свойства имя разворачивающейся кнопки должен быть указан альтернативный текст.</span><span class="sxs-lookup"><span data-stu-id="bc5fd-186">Whenever an image is used to label a split button, alternate text must be supplied for the split button Name property.</span></span>                              |



 

## <a name="required-control-patterns"></a><span data-ttu-id="bc5fd-187">Обязательные шаблоны элементов управления</span><span class="sxs-lookup"><span data-stu-id="bc5fd-187">Required Control Patterns</span></span>

<span data-ttu-id="bc5fd-188">В следующей таблице перечислены шаблоны элементов управления модели автоматизации пользовательского интерфейса, которые должны поддерживаться всеми элементами управления "разворачивающаяся кнопка".</span><span class="sxs-lookup"><span data-stu-id="bc5fd-188">The following table lists the UI Automation control patterns required to be supported by all split button controls.</span></span> <span data-ttu-id="bc5fd-189">Дополнительные сведения о шаблонах элементов управления см. в разделе [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md).</span><span class="sxs-lookup"><span data-stu-id="bc5fd-189">For more information on control patterns, see [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md).</span></span>



| <span data-ttu-id="bc5fd-190">Шаблон элемента управления</span><span class="sxs-lookup"><span data-stu-id="bc5fd-190">Control Pattern</span></span>                                                   | <span data-ttu-id="bc5fd-191">Поддержка</span><span class="sxs-lookup"><span data-stu-id="bc5fd-191">Support</span></span>  | <span data-ttu-id="bc5fd-192">Примечания</span><span class="sxs-lookup"><span data-stu-id="bc5fd-192">Notes</span></span>                                                                                                                                                                                                                          |
|-------------------------------------------------------------------|----------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="bc5fd-193">**IExpandCollapseProvider**</span><span class="sxs-lookup"><span data-stu-id="bc5fd-193">**IExpandCollapseProvider**</span></span>](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iexpandcollapseprovider) | <span data-ttu-id="bc5fd-194">Обязательно</span><span class="sxs-lookup"><span data-stu-id="bc5fd-194">Required</span></span> | <span data-ttu-id="bc5fd-195">Поскольку у кнопок разбиения всегда есть возможность развернуть список параметров, они должны поддерживать шаблон элемента управления [ExpandCollapse](uiauto-implementingexpandcollapse.md) .</span><span class="sxs-lookup"><span data-stu-id="bc5fd-195">Because split buttons always have the ability to expand a list of options, they must support the [ExpandCollapse](uiauto-implementingexpandcollapse.md) control pattern.</span></span>                                                      |
| [<span data-ttu-id="bc5fd-196">**IInvokeProvider**</span><span class="sxs-lookup"><span data-stu-id="bc5fd-196">**IInvokeProvider**</span></span>](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iinvokeprovider)                 | <span data-ttu-id="bc5fd-197">Обязательно</span><span class="sxs-lookup"><span data-stu-id="bc5fd-197">Required</span></span> | <span data-ttu-id="bc5fd-198">Поскольку у кнопок разбиения всегда есть действие по умолчанию, связанное с методом [**IInvokeProvider:: Invoke**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iinvokeprovider-invoke) , они должны поддерживать шаблон элемента управления [Invoke](uiauto-implementinginvoke.md) .</span><span class="sxs-lookup"><span data-stu-id="bc5fd-198">Because split buttons always have a default action associated with the [**IInvokeProvider::Invoke**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iinvokeprovider-invoke) method, they must support the [Invoke](uiauto-implementinginvoke.md) control pattern.</span></span> |



 

## <a name="required-events"></a><span data-ttu-id="bc5fd-199">Обязательные события</span><span class="sxs-lookup"><span data-stu-id="bc5fd-199">Required Events</span></span>

<span data-ttu-id="bc5fd-200">В следующей таблице перечислены события автоматизации пользовательского интерфейса, которые должны поддерживаться разворачивающимися элементами управления "Кнопка".</span><span class="sxs-lookup"><span data-stu-id="bc5fd-200">The following table lists the UI Automation events that split button controls are required to support.</span></span> <span data-ttu-id="bc5fd-201">Дополнительные сведения о событиях см. в разделе [UI Automation Events Overview](uiauto-eventsoverview.md).</span><span class="sxs-lookup"><span data-stu-id="bc5fd-201">For more information on events, see [UI Automation Events Overview](uiauto-eventsoverview.md).</span></span>



| <span data-ttu-id="bc5fd-202">Событие автоматизации пользовательского интерфейса</span><span class="sxs-lookup"><span data-stu-id="bc5fd-202">UI Automation Event</span></span>                                                                                                                                                | <span data-ttu-id="bc5fd-203">Примечания</span><span class="sxs-lookup"><span data-stu-id="bc5fd-203">Notes</span></span>                                                                                                                      |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="bc5fd-204">**UIA \_ аутоматионфокусчанжедевентид**</span><span class="sxs-lookup"><span data-stu-id="bc5fd-204">**UIA\_AutomationFocusChangedEventId**</span></span>](uiauto-event-ids.md)                                                                   |                                                                                                                            |
| <span data-ttu-id="bc5fd-205">[**UIA \_**](uiauto-automation-element-propids.md) Событие изменения свойства баундингректанглепропертид.</span><span class="sxs-lookup"><span data-stu-id="bc5fd-205">[**UIA\_BoundingRectanglePropertyId**](uiauto-automation-element-propids.md) property-changed event.</span></span>                              |                                                                                                                            |
| <span data-ttu-id="bc5fd-206">[**UIA \_**](uiauto-control-pattern-propids.md) Событие изменения свойства експандколлапсикспандколлапсестатепропертид.</span><span class="sxs-lookup"><span data-stu-id="bc5fd-206">[**UIA\_ExpandCollapseExpandCollapseStatePropertyId**](uiauto-control-pattern-propids.md) property-changed event.</span></span> |                                                                                                                            |
| [<span data-ttu-id="bc5fd-207">**UIA \_ Invoke \_ инвокедевентид**</span><span class="sxs-lookup"><span data-stu-id="bc5fd-207">**UIA\_Invoke\_InvokedEventId**</span></span>](uiauto-event-ids.md)                                                                                  |                                                                                                                            |
| <span data-ttu-id="bc5fd-208">[**UIA \_**](uiauto-automation-element-propids.md) Событие изменения свойства исенабледпропертид.</span><span class="sxs-lookup"><span data-stu-id="bc5fd-208">[**UIA\_IsEnabledPropertyId**](uiauto-automation-element-propids.md) property-changed event.</span></span>                                              | <span data-ttu-id="bc5fd-209">Если элемент управления поддерживает свойство « [**включено**](uiauto-automation-element-propids.md) », оно должно поддерживать это событие.</span><span class="sxs-lookup"><span data-stu-id="bc5fd-209">If the control supports the [**IsEnabled**](uiauto-automation-element-propids.md) property, it must support this event.</span></span>   |
| <span data-ttu-id="bc5fd-210">[**UIA \_**](uiauto-automation-element-propids.md) Событие изменения свойства исоффскринпропертид.</span><span class="sxs-lookup"><span data-stu-id="bc5fd-210">[**UIA\_IsOffscreenPropertyId**](uiauto-automation-element-propids.md) property-changed event.</span></span>                                          | <span data-ttu-id="bc5fd-211">Если элемент управления поддерживает свойство [**исоффскрин**](uiauto-automation-element-propids.md) , он должен поддерживать это событие.</span><span class="sxs-lookup"><span data-stu-id="bc5fd-211">If the control supports the [**IsOffscreen**](uiauto-automation-element-propids.md) property, it must support this event.</span></span> |
| [<span data-ttu-id="bc5fd-212">**UIA \_ структуречанжедевентид**</span><span class="sxs-lookup"><span data-stu-id="bc5fd-212">**UIA\_StructureChangedEventId**</span></span>](uiauto-event-ids.md)                                                                               |                                                                                                                            |



 

## <a name="splitbutton-control-type-example"></a><span data-ttu-id="bc5fd-213">Пример типа элемента управления SplitButton</span><span class="sxs-lookup"><span data-stu-id="bc5fd-213">SplitButton Control Type Example</span></span>

<span data-ttu-id="bc5fd-214">На следующем рисунке показан элемент управления, реализующий тип элемента управления **SplitButton** .</span><span class="sxs-lookup"><span data-stu-id="bc5fd-214">The following image illustrates a control that implements the **SplitButton** control type.</span></span>

![снимок экрана, демонстрирующий пример элемента управления SplitButton](images/splitbuttonxmpl.jpg)



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="bc5fd-216">Дерево модели автоматизации пользовательского интерфейса — представление элемента управления</span><span class="sxs-lookup"><span data-stu-id="bc5fd-216">UI Automation Tree—Control View</span></span></th>
<th><span data-ttu-id="bc5fd-217">Дерево модели автоматизации пользовательского интерфейса — представление содержимого</span><span class="sxs-lookup"><span data-stu-id="bc5fd-217">UI Automation Tree—Content View</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><ul>
<li><span data-ttu-id="bc5fd-218">&quot;Имя SplitButton &quot; (Invoke, ExpandCollapse)</span><span class="sxs-lookup"><span data-stu-id="bc5fd-218">SplitButton &quot;Name&quot; (Invoke, ExpandCollapse)</span></span>
<ul>
<li><span data-ttu-id="bc5fd-219">Кнопка " &quot; Дополнительно" &quot; (Invoke)</span><span class="sxs-lookup"><span data-stu-id="bc5fd-219">Button &quot;More option&quot; (Invoke)</span></span>
<ul>
<li><span data-ttu-id="bc5fd-220">Меню</span><span class="sxs-lookup"><span data-stu-id="bc5fd-220">Menu</span></span>
<ul>
<li><span data-ttu-id="bc5fd-221">MenuItem</span><span class="sxs-lookup"><span data-stu-id="bc5fd-221">MenuItem</span></span></li>
<li><span data-ttu-id="bc5fd-222">...</span><span class="sxs-lookup"><span data-stu-id="bc5fd-222">...</span></span></li>
</ul></li>
</ul></li>
</ul></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="bc5fd-223">&quot;Имя SplitButton &quot; (Invoke, ExpandCollapse)</span><span class="sxs-lookup"><span data-stu-id="bc5fd-223">SplitButton &quot;Name&quot; (Invoke, ExpandCollapse)</span></span>
<ul>
<li><span data-ttu-id="bc5fd-224">Кнопка " &quot; Дополнительно" &quot; (Invoke)</span><span class="sxs-lookup"><span data-stu-id="bc5fd-224">Button &quot;More option&quot; (Invoke)</span></span>
<ul>
<li><span data-ttu-id="bc5fd-225">Меню</span><span class="sxs-lookup"><span data-stu-id="bc5fd-225">Menu</span></span>
<ul>
<li><span data-ttu-id="bc5fd-226">MenuItem</span><span class="sxs-lookup"><span data-stu-id="bc5fd-226">MenuItem</span></span></li>
<li><span data-ttu-id="bc5fd-227">...</span><span class="sxs-lookup"><span data-stu-id="bc5fd-227">...</span></span></li>
</ul></li>
</ul></li>
</ul></li>
</ul></td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a><span data-ttu-id="bc5fd-228">См. также</span><span class="sxs-lookup"><span data-stu-id="bc5fd-228">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="bc5fd-229">**Зрения**</span><span class="sxs-lookup"><span data-stu-id="bc5fd-229">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="bc5fd-230">Общие сведения о типах элементов управления автоматизации пользовательского интерфейса</span><span class="sxs-lookup"><span data-stu-id="bc5fd-230">UI Automation Control Types Overview</span></span>](uiauto-controltypesoverview.md)
</dt> <dt>

[<span data-ttu-id="bc5fd-231">Общие сведения о модели автоматизации пользовательского интерфейса</span><span class="sxs-lookup"><span data-stu-id="bc5fd-231">UI Automation Overview</span></span>](uiauto-uiautomationoverview.md)
</dt> </dl>

 

 




