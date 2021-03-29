---
title: Тип элемента управления Button
description: В этом разделе содержатся сведения о поддержке автоматизации пользовательского интерфейса Майкрософт для типа элемента управления Button.
ms.assetid: a2942067-461c-4281-80cf-385e3c08c874
keywords:
- Модель автоматизации пользовательского интерфейса, поддержка типа элемента управления Button
- Модель автоматизации пользовательского интерфейса, тип элемента управления "Кнопка"
- Модель автоматизации пользовательского интерфейса, древовидная структура для типа элемента управления Button
- Модель автоматизации пользовательского интерфейса, свойства для типа элемента управления Button
- Модель автоматизации пользовательского интерфейса, шаблоны элементов управления для типа элемента управления Button
- Модель автоматизации пользовательского интерфейса, события для типа элемента управления Button
- Древовидные структуры, тип элемента управления Button
- свойства, тип элемента управления Button
- шаблоны элементов управления, тип элемента управления Button
- события, тип элемента управления Button
- Поддержка типа элемента управления Button
- тип элемента управления "Кнопка"
- типы элементов управления, древовидная структура для типа элемента управления Button
- типы элементов управления, шаблоны элементов управления для типа элемента управления Button
- типы элементов управления, поддержка кнопки
- типы элементов управления, кнопка
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: def18e7094e297303a70fc0980bfdd0cb4413c0c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104259096"
---
# <a name="button-control-type"></a><span data-ttu-id="8b1fb-119">Тип элемента управления Button</span><span class="sxs-lookup"><span data-stu-id="8b1fb-119">Button Control Type</span></span>

<span data-ttu-id="8b1fb-120">В этом разделе содержатся сведения о поддержке автоматизации пользовательского интерфейса Майкрософт для типа элемента управления **Button** .</span><span class="sxs-lookup"><span data-stu-id="8b1fb-120">This topic provides information about Microsoft UI Automation support for the **Button** control type.</span></span>

<span data-ttu-id="8b1fb-121">Кнопка является объектом, с которым пользователь взаимодействует для выполнения действия, таким как кнопки ОК и Отменить в диалоговом окне.</span><span class="sxs-lookup"><span data-stu-id="8b1fb-121">A button is an object that a user interacts with to perform an action such as the OK and Cancel buttons on a dialog box.</span></span> <span data-ttu-id="8b1fb-122">Кнопка является простым элементом управления, так как она сопоставляется с одной командой, которую пользователь хочет выполнить.</span><span class="sxs-lookup"><span data-stu-id="8b1fb-122">The button control is a simple control to expose because it maps to a single command that the user wishes to complete.</span></span>

<span data-ttu-id="8b1fb-123">В следующих разделах определяется необходимая древовидная структура модели автоматизации пользовательского интерфейса, свойства, шаблоны элементов управления и события для типа элемента управления **Button** .</span><span class="sxs-lookup"><span data-stu-id="8b1fb-123">The following sections define the required UI Automation tree structure, properties, control patterns, and events for the **Button** control type.</span></span> <span data-ttu-id="8b1fb-124">Требования к автоматизации пользовательского интерфейса применяются ко всем элементам управления "Кнопка", в которых платформа или платформа пользовательского интерфейса интегрирует поддержку модели автоматизации пользовательского интерфейса для типов элементов управления и шаблонов элементов управления.</span><span class="sxs-lookup"><span data-stu-id="8b1fb-124">The UI Automation requirements apply to all button controls where the UI framework/platform integrates UI Automation support for control types and control patterns.</span></span>

<span data-ttu-id="8b1fb-125">В этом разделе содержатся следующие подразделы.</span><span class="sxs-lookup"><span data-stu-id="8b1fb-125">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="8b1fb-126">Типичная древовидная структура</span><span class="sxs-lookup"><span data-stu-id="8b1fb-126">Typical Tree Structure</span></span>](#typical-tree-structure)
-   [<span data-ttu-id="8b1fb-127">Соответствующие свойства</span><span class="sxs-lookup"><span data-stu-id="8b1fb-127">Relevant Properties</span></span>](#relevant-properties)
-   [<span data-ttu-id="8b1fb-128">Обязательные шаблоны элементов управления</span><span class="sxs-lookup"><span data-stu-id="8b1fb-128">Required Control Patterns</span></span>](#required-control-patterns)
-   [<span data-ttu-id="8b1fb-129">Обязательные события</span><span class="sxs-lookup"><span data-stu-id="8b1fb-129">Required Events</span></span>](#required-events)
-   [<span data-ttu-id="8b1fb-130">См. также</span><span class="sxs-lookup"><span data-stu-id="8b1fb-130">Related topics</span></span>](#related-topics)

## <a name="typical-tree-structure"></a><span data-ttu-id="8b1fb-131">Типичная древовидная структура</span><span class="sxs-lookup"><span data-stu-id="8b1fb-131">Typical Tree Structure</span></span>

<span data-ttu-id="8b1fb-132">В следующей таблице описывается типичный элемент управления и представление содержимого дерева модели автоматизации пользовательского интерфейса, которое относится к элементам управления "Кнопка" и описывает, что может содержаться в каждом представлении.</span><span class="sxs-lookup"><span data-stu-id="8b1fb-132">The following table depicts a typical control and content view of the UI Automation tree that pertains to button controls and describes what can be contained in each view.</span></span> <span data-ttu-id="8b1fb-133">Дополнительные сведения о дереве автоматизации пользовательского интерфейса см. в разделе [Общие сведения о дереве модели автоматизации пользовательского интерфейса](uiauto-treeoverview.md).</span><span class="sxs-lookup"><span data-stu-id="8b1fb-133">For more information about the UI Automation tree, see [UI Automation Tree Overview](uiauto-treeoverview.md).</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="8b1fb-134">Представление элемента управления</span><span class="sxs-lookup"><span data-stu-id="8b1fb-134">Control View</span></span></th>
<th><span data-ttu-id="8b1fb-135">Представление содержимого</span><span class="sxs-lookup"><span data-stu-id="8b1fb-135">Content View</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><ul>
<li><span data-ttu-id="8b1fb-136">Кнопка</span><span class="sxs-lookup"><span data-stu-id="8b1fb-136">Button</span></span>
<ul>
<li><span data-ttu-id="8b1fb-137">Image (0 или более)</span><span class="sxs-lookup"><span data-stu-id="8b1fb-137">Image (0 or more)</span></span></li>
<li><span data-ttu-id="8b1fb-138">Text (0 или более)</span><span class="sxs-lookup"><span data-stu-id="8b1fb-138">Text (0 or more)</span></span></li>
</ul></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="8b1fb-139">Кнопка</span><span class="sxs-lookup"><span data-stu-id="8b1fb-139">Button</span></span></li>
</ul></td>
</tr>
</tbody>
</table>



 

## <a name="relevant-properties"></a><span data-ttu-id="8b1fb-140">Соответствующие свойства</span><span class="sxs-lookup"><span data-stu-id="8b1fb-140">Relevant Properties</span></span>

<span data-ttu-id="8b1fb-141">В следующей таблице перечислены свойства модели автоматизации пользовательского интерфейса, значение или определение которых особенно релевантно для элементов управления, реализующих тип элемента управления **Button** (например, элементы управления "Кнопка").</span><span class="sxs-lookup"><span data-stu-id="8b1fb-141">The following table lists the UI Automation properties whose value or definition is especially relevant to the controls that implement the **Button** control type (such as button controls).</span></span> <span data-ttu-id="8b1fb-142">Дополнительные сведения о свойствах модели автоматизации пользовательского интерфейса см. в разделе [Получение свойств элементов модели автоматизации пользовательского интерфейса](uiauto-propertiesforclients.md).</span><span class="sxs-lookup"><span data-stu-id="8b1fb-142">For more information about UI Automation properties, see [Retrieving Properties from UI Automation Elements](uiauto-propertiesforclients.md).</span></span>



| <span data-ttu-id="8b1fb-143">Свойство модели автоматизации пользовательского интерфейса</span><span class="sxs-lookup"><span data-stu-id="8b1fb-143">UI Automation Property</span></span>                                                                                              | <span data-ttu-id="8b1fb-144">Значение</span><span class="sxs-lookup"><span data-stu-id="8b1fb-144">Value</span></span>      | <span data-ttu-id="8b1fb-145">Примечания</span><span class="sxs-lookup"><span data-stu-id="8b1fb-145">Notes</span></span>                                                                                                                                                                                                |
|---------------------------------------------------------------------------------------------------------------------|------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="8b1fb-146">**UIA \_ акцелераторкэйпропертид**</span><span class="sxs-lookup"><span data-stu-id="8b1fb-146">**UIA\_AcceleratorKeyPropertyId**</span></span>](uiauto-automation-element-propids.md)             | <span data-ttu-id="8b1fb-147">См. примечания.</span><span class="sxs-lookup"><span data-stu-id="8b1fb-147">See notes.</span></span> | <span data-ttu-id="8b1fb-148">Элемент управления "Кнопка" обычно поддерживает сочетание клавиш, чтобы позволить пользователю быстро выполнить действие, представленное кнопкой с клавиатуры.</span><span class="sxs-lookup"><span data-stu-id="8b1fb-148">A button control typically supports an accelerator key to enable the end user to quickly perform the action represented by the button from the keyboard.</span></span>                                             |
| [<span data-ttu-id="8b1fb-149">**UIA \_ аутоматионидпропертид**</span><span class="sxs-lookup"><span data-stu-id="8b1fb-149">**UIA\_AutomationIdPropertyId**</span></span>](uiauto-automation-element-propids.md)                 | <span data-ttu-id="8b1fb-150">См. примечания.</span><span class="sxs-lookup"><span data-stu-id="8b1fb-150">See notes.</span></span> | <span data-ttu-id="8b1fb-151">Значение этого свойства должно быть уникальным среди всех одноранговых элементов в необработанном представлении дерева модели автоматизации пользовательского интерфейса.</span><span class="sxs-lookup"><span data-stu-id="8b1fb-151">The value of this property must be unique among all peer elements in the raw view of the UI Automation tree.</span></span>                                                                                         |
| [<span data-ttu-id="8b1fb-152">**UIA \_ баундингректанглепропертид**</span><span class="sxs-lookup"><span data-stu-id="8b1fb-152">**UIA\_BoundingRectanglePropertyId**</span></span>](uiauto-automation-element-propids.md)       | <span data-ttu-id="8b1fb-153">См. примечания.</span><span class="sxs-lookup"><span data-stu-id="8b1fb-153">See notes.</span></span> | <span data-ttu-id="8b1fb-154">Внешний прямоугольник, содержащий весь элемент управления.</span><span class="sxs-lookup"><span data-stu-id="8b1fb-154">The outermost rectangle that contains the whole control.</span></span>                                                                                                                                             |
| [<span data-ttu-id="8b1fb-155">**UIA \_ кликкаблепоинтпропертид**</span><span class="sxs-lookup"><span data-stu-id="8b1fb-155">**UIA\_ClickablePointPropertyId**</span></span>](uiauto-automation-element-propids.md)             | <span data-ttu-id="8b1fb-156">См. примечания.</span><span class="sxs-lookup"><span data-stu-id="8b1fb-156">See notes.</span></span> | <span data-ttu-id="8b1fb-157">Поддерживается при наличии ограничивающего прямоугольника.</span><span class="sxs-lookup"><span data-stu-id="8b1fb-157">Supported if there is a bounding rectangle.</span></span> <span data-ttu-id="8b1fb-158">Если не все точки внутри ограничивающего прямоугольника являются щелчками, а элемент выполняет специализированное тестирование нажатия, переопределите и предоставьте точку для щелчка.</span><span class="sxs-lookup"><span data-stu-id="8b1fb-158">If not every point within the bounding rectangle is clickable, and the element performs specialized hit testing, override and provide a clickable point.</span></span> |
| [<span data-ttu-id="8b1fb-159">**UIA \_ контролтипепропертид**</span><span class="sxs-lookup"><span data-stu-id="8b1fb-159">**UIA\_ControlTypePropertyId**</span></span>](uiauto-automation-element-propids.md)                   | <span data-ttu-id="8b1fb-160">**Кнопка**</span><span class="sxs-lookup"><span data-stu-id="8b1fb-160">**Button**</span></span> |                                                                                                                                                                                                      |
| [<span data-ttu-id="8b1fb-161">**UIA \_ хелптекстпропертид**</span><span class="sxs-lookup"><span data-stu-id="8b1fb-161">**UIA\_HelpTextPropertyId**</span></span>](uiauto-automation-element-propids.md)                         | <span data-ttu-id="8b1fb-162">См. примечания.</span><span class="sxs-lookup"><span data-stu-id="8b1fb-162">See notes.</span></span> | <span data-ttu-id="8b1fb-163">Текст справки должен указывать на результат активации кнопки.</span><span class="sxs-lookup"><span data-stu-id="8b1fb-163">The help text should indicate what the end result of activating the button will be.</span></span> <span data-ttu-id="8b1fb-164">Обычно это один и тот же тип информации, представленной в подсказке.</span><span class="sxs-lookup"><span data-stu-id="8b1fb-164">This is typically the same type of information presented through a tooltip.</span></span>                                      |
| [<span data-ttu-id="8b1fb-165">**UIA \_ исконтентелементпропертид**</span><span class="sxs-lookup"><span data-stu-id="8b1fb-165">**UIA\_IsContentElementPropertyId**</span></span>](uiauto-automation-element-propids.md)         | <span data-ttu-id="8b1fb-166">true</span><span class="sxs-lookup"><span data-stu-id="8b1fb-166">TRUE</span></span>       | <span data-ttu-id="8b1fb-167">Элемент управления "Кнопка" всегда должен быть содержимым.</span><span class="sxs-lookup"><span data-stu-id="8b1fb-167">The button control must always be content.</span></span>                                                                                                                                                           |
| [<span data-ttu-id="8b1fb-168">**UIA \_ исконтролелементпропертид**</span><span class="sxs-lookup"><span data-stu-id="8b1fb-168">**UIA\_IsControlElementPropertyId**</span></span>](uiauto-automation-element-propids.md)         | <span data-ttu-id="8b1fb-169">true</span><span class="sxs-lookup"><span data-stu-id="8b1fb-169">TRUE</span></span>       | <span data-ttu-id="8b1fb-170">Элемент управления "Кнопка" всегда должен быть элементом управления.</span><span class="sxs-lookup"><span data-stu-id="8b1fb-170">The button control must always be a control.</span></span>                                                                                                                                                         |
| [<span data-ttu-id="8b1fb-171">**UIA \_ искэйбоардфокусаблепропертид**</span><span class="sxs-lookup"><span data-stu-id="8b1fb-171">**UIA\_IsKeyboardFocusablePropertyId**</span></span>](uiauto-automation-element-propids.md)   | <span data-ttu-id="8b1fb-172">См. примечания.</span><span class="sxs-lookup"><span data-stu-id="8b1fb-172">See notes.</span></span> | <span data-ttu-id="8b1fb-173">Если элемент управления может получать фокус клавиатуры, он должен поддерживать это свойство.</span><span class="sxs-lookup"><span data-stu-id="8b1fb-173">If the control can receive keyboard focus, it must support this property.</span></span>                                                                                                                            |
| [<span data-ttu-id="8b1fb-174">**UIA \_ лабеледбипропертид**</span><span class="sxs-lookup"><span data-stu-id="8b1fb-174">**UIA\_LabeledByPropertyId**</span></span>](uiauto-automation-element-propids.md)                       | <span data-ttu-id="8b1fb-175">NULL</span><span class="sxs-lookup"><span data-stu-id="8b1fb-175">Null</span></span>       | <span data-ttu-id="8b1fb-176">Элементы управления "Кнопка" помечаются автоматически по их содержимому.</span><span class="sxs-lookup"><span data-stu-id="8b1fb-176">Button controls are self-labeled by their contents.</span></span>                                                                                                                                                  |
| [<span data-ttu-id="8b1fb-177">**UIA \_ локализедконтролтипепропертид**</span><span class="sxs-lookup"><span data-stu-id="8b1fb-177">**UIA\_LocalizedControlTypePropertyId**</span></span>](uiauto-automation-element-propids.md) | <span data-ttu-id="8b1fb-178">См. примечания.</span><span class="sxs-lookup"><span data-stu-id="8b1fb-178">See notes.</span></span> | <span data-ttu-id="8b1fb-179">Локализованная строка, соответствующая типу элемента управления **"Кнопка"** .</span><span class="sxs-lookup"><span data-stu-id="8b1fb-179">Localized string corresponding to the **Button** control type.</span></span> <span data-ttu-id="8b1fb-180">Значение по умолчанию — "Кнопка" для en-US или English (США).</span><span class="sxs-lookup"><span data-stu-id="8b1fb-180">The default value is "button" for en-US or English (United States).</span></span>                                                                   |
| [<span data-ttu-id="8b1fb-181">**UIA \_ намепропертид**</span><span class="sxs-lookup"><span data-stu-id="8b1fb-181">**UIA\_NamePropertyId**</span></span>](uiauto-automation-element-propids.md)                                 | <span data-ttu-id="8b1fb-182">См. примечания.</span><span class="sxs-lookup"><span data-stu-id="8b1fb-182">See notes.</span></span> | <span data-ttu-id="8b1fb-183">Имя элемента управления "Кнопка" — это текст, который используется для подписи.</span><span class="sxs-lookup"><span data-stu-id="8b1fb-183">The name of the button control is the text used to label it.</span></span> <span data-ttu-id="8b1fb-184">Каждый раз, когда изображение используется для обозначения кнопки, для свойства **имени** кнопки должен быть указан альтернативный текст.</span><span class="sxs-lookup"><span data-stu-id="8b1fb-184">Whenever an image is used to label a button, alternate text must be supplied for the button's **Name** property.</span></span>                        |



 

## <a name="required-control-patterns"></a><span data-ttu-id="8b1fb-185">Обязательные шаблоны элементов управления</span><span class="sxs-lookup"><span data-stu-id="8b1fb-185">Required Control Patterns</span></span>

<span data-ttu-id="8b1fb-186">В следующей таблице перечислены шаблоны элементов управления модели автоматизации пользовательского интерфейса, которые должны поддерживаться всеми элементами управления "Кнопка".</span><span class="sxs-lookup"><span data-stu-id="8b1fb-186">The following table lists the UI Automation control patterns required to be supported by all button controls.</span></span> <span data-ttu-id="8b1fb-187">Дополнительные сведения о шаблонах элементов управления см. в разделе [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md).</span><span class="sxs-lookup"><span data-stu-id="8b1fb-187">For more information on control patterns, see [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md).</span></span>



| <span data-ttu-id="8b1fb-188">Шаблон элемента управления/свойство шаблона</span><span class="sxs-lookup"><span data-stu-id="8b1fb-188">Control Pattern/Pattern Property</span></span>                                  | <span data-ttu-id="8b1fb-189">Поддержка/значение</span><span class="sxs-lookup"><span data-stu-id="8b1fb-189">Support/Value</span></span> | <span data-ttu-id="8b1fb-190">Примечания</span><span class="sxs-lookup"><span data-stu-id="8b1fb-190">Notes</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                     |
|-------------------------------------------------------------------|---------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="8b1fb-191">**IExpandCollapseProvider**</span><span class="sxs-lookup"><span data-stu-id="8b1fb-191">**IExpandCollapseProvider**</span></span>](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iexpandcollapseprovider) | <span data-ttu-id="8b1fb-192">См. примечания.</span><span class="sxs-lookup"><span data-stu-id="8b1fb-192">See notes.</span></span>    | <span data-ttu-id="8b1fb-193">Если кнопка размещается как дочерняя кнопка разворачивающейся кнопки, дочерняя кнопка может поддерживать шаблон элемента управления [ExpandCollapse](uiauto-implementingexpandcollapse.md) вместо шаблона элемента управления [Invoke](uiauto-implementinginvoke.md) или [Toggle](uiauto-implementingtoggle.md) .</span><span class="sxs-lookup"><span data-stu-id="8b1fb-193">When a button is hosted as a child of a split button, the child button can support the [ExpandCollapse](uiauto-implementingexpandcollapse.md) control pattern instead of the [Invoke](uiauto-implementinginvoke.md) or [Toggle](uiauto-implementingtoggle.md) control pattern.</span></span> <span data-ttu-id="8b1fb-194">Шаблон элемента управления ExpandCollapse можно использовать для открытия или закрытия меню или другой вложенной структуры, связанной с элементом Button.</span><span class="sxs-lookup"><span data-stu-id="8b1fb-194">The ExpandCollapse control pattern can be used for opening or closing a menu or other sub-structure associated with the button element.</span></span> |
| [<span data-ttu-id="8b1fb-195">**IInvokeProvider**</span><span class="sxs-lookup"><span data-stu-id="8b1fb-195">**IInvokeProvider**</span></span>](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iinvokeprovider)                 | <span data-ttu-id="8b1fb-196">См. примечания.</span><span class="sxs-lookup"><span data-stu-id="8b1fb-196">See notes.</span></span>    | <span data-ttu-id="8b1fb-197">Все кнопки должны поддерживать шаблон элемента управления [Invoke](uiauto-implementinginvoke.md) или шаблон элемента управления [Toggle](uiauto-implementingtoggle.md) , но не оба значения.</span><span class="sxs-lookup"><span data-stu-id="8b1fb-197">All buttons should support the [Invoke](uiauto-implementinginvoke.md) control pattern or the [Toggle](uiauto-implementingtoggle.md) control pattern but not both.</span></span> <span data-ttu-id="8b1fb-198">Шаблон элемента управления Invoke должен поддерживаться, когда кнопка выполняет команду по запросу пользователя.</span><span class="sxs-lookup"><span data-stu-id="8b1fb-198">The Invoke control pattern must be supported when the button performs a command at the request of the user.</span></span> <span data-ttu-id="8b1fb-199">Эта команда сопоставляется с одной операцией, например операцией вырезания, копирования, вставки или удаления.</span><span class="sxs-lookup"><span data-stu-id="8b1fb-199">This command maps to a single operation such as Cut, Copy, Paste, or Delete.</span></span>                                                              |
| [<span data-ttu-id="8b1fb-200">**IToggleProvider**</span><span class="sxs-lookup"><span data-stu-id="8b1fb-200">**IToggleProvider**</span></span>](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itoggleprovider)                 | <span data-ttu-id="8b1fb-201">См. примечания.</span><span class="sxs-lookup"><span data-stu-id="8b1fb-201">See notes.</span></span>    | <span data-ttu-id="8b1fb-202">Все кнопки должны поддерживать шаблон элемента управления [Invoke](uiauto-implementinginvoke.md) или шаблон элемента управления [Toggle](uiauto-implementingtoggle.md) , но не оба значения.</span><span class="sxs-lookup"><span data-stu-id="8b1fb-202">All buttons should support the [Invoke](uiauto-implementinginvoke.md) control pattern or the [Toggle](uiauto-implementingtoggle.md) control pattern but not both.</span></span> <span data-ttu-id="8b1fb-203">Шаблон элемента управления Toggle должен поддерживаться, если кнопка может циклически проходить до трех состояний.</span><span class="sxs-lookup"><span data-stu-id="8b1fb-203">The Toggle control pattern must be supported if the button can cycle through a series of up to three states.</span></span> <span data-ttu-id="8b1fb-204">Обычно это выглядит как переключатель "Вкл./Выкл." для конкретных функций.</span><span class="sxs-lookup"><span data-stu-id="8b1fb-204">Typically this is seen as an on/off switch for specific features.</span></span>                                                                        |



 

## <a name="required-events"></a><span data-ttu-id="8b1fb-205">Обязательные события</span><span class="sxs-lookup"><span data-stu-id="8b1fb-205">Required Events</span></span>

<span data-ttu-id="8b1fb-206">В следующей таблице перечислены события автоматизации пользовательского интерфейса, которые должны поддерживаться элементами управления "Кнопка".</span><span class="sxs-lookup"><span data-stu-id="8b1fb-206">The following table lists the UI Automation events that button controls are required to support.</span></span> <span data-ttu-id="8b1fb-207">Дополнительные сведения о событиях см. в разделе [UI Automation Events Overview](uiauto-eventsoverview.md).</span><span class="sxs-lookup"><span data-stu-id="8b1fb-207">For more information on events, see [UI Automation Events Overview](uiauto-eventsoverview.md).</span></span>



| <span data-ttu-id="8b1fb-208">Событие автоматизации пользовательского интерфейса</span><span class="sxs-lookup"><span data-stu-id="8b1fb-208">UI Automation Event</span></span>                                                                                                                   | <span data-ttu-id="8b1fb-209">Примечания</span><span class="sxs-lookup"><span data-stu-id="8b1fb-209">Notes</span></span>                                                                                                                      |
|---------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="8b1fb-210">**UIA \_ аутоматионфокусчанжедевентид**</span><span class="sxs-lookup"><span data-stu-id="8b1fb-210">**UIA\_AutomationFocusChangedEventId**</span></span>](uiauto-event-ids.md)                                      |                                                                                                                            |
| <span data-ttu-id="8b1fb-211">[**UIA \_**](uiauto-automation-element-propids.md) Событие изменения свойства баундингректанглепропертид.</span><span class="sxs-lookup"><span data-stu-id="8b1fb-211">[**UIA\_BoundingRectanglePropertyId**](uiauto-automation-element-propids.md) property-changed event.</span></span> |                                                                                                                            |
| [<span data-ttu-id="8b1fb-212">**UIA \_ Invoke \_ инвокедевентид**</span><span class="sxs-lookup"><span data-stu-id="8b1fb-212">**UIA\_Invoke\_InvokedEventId**</span></span>](uiauto-event-ids.md)                                                     | <span data-ttu-id="8b1fb-213">Если элемент управления поддерживает шаблон элемента управления [Invoke](uiauto-implementinginvoke.md) , он должен поддерживать это событие.</span><span class="sxs-lookup"><span data-stu-id="8b1fb-213">If the control supports the [Invoke](uiauto-implementinginvoke.md) control pattern, it must support this event.</span></span>           |
| <span data-ttu-id="8b1fb-214">[**UIA \_**](uiauto-automation-element-propids.md) Событие изменения свойства исенабледпропертид.</span><span class="sxs-lookup"><span data-stu-id="8b1fb-214">[**UIA\_IsEnabledPropertyId**](uiauto-automation-element-propids.md) property-changed event.</span></span>                 | <span data-ttu-id="8b1fb-215">Если элемент управления поддерживает свойство « [**включено**](uiauto-automation-element-propids.md) », оно должно поддерживать это событие.</span><span class="sxs-lookup"><span data-stu-id="8b1fb-215">If the control supports the [**IsEnabled**](uiauto-automation-element-propids.md) property, it must support this event.</span></span>   |
| <span data-ttu-id="8b1fb-216">[**UIA \_**](uiauto-automation-element-propids.md) Событие изменения свойства исоффскринпропертид.</span><span class="sxs-lookup"><span data-stu-id="8b1fb-216">[**UIA\_IsOffscreenPropertyId**](uiauto-automation-element-propids.md) property-changed event.</span></span>             | <span data-ttu-id="8b1fb-217">Если элемент управления поддерживает свойство [**исоффскрин**](uiauto-automation-element-propids.md) , он должен поддерживать это событие.</span><span class="sxs-lookup"><span data-stu-id="8b1fb-217">If the control supports the [**IsOffscreen**](uiauto-automation-element-propids.md) property, it must support this event.</span></span> |
| <span data-ttu-id="8b1fb-218">[**UIA \_**](uiauto-automation-element-propids.md) Событие изменения свойства намепропертид.</span><span class="sxs-lookup"><span data-stu-id="8b1fb-218">[**UIA\_NamePropertyId**](uiauto-automation-element-propids.md) property-changed event.</span></span>                           |                                                                                                                            |
| [<span data-ttu-id="8b1fb-219">**UIA \_ структуречанжедевентид**</span><span class="sxs-lookup"><span data-stu-id="8b1fb-219">**UIA\_StructureChangedEventId**</span></span>](uiauto-event-ids.md)                                                  |                                                                                                                            |
| <span data-ttu-id="8b1fb-220">[**UIA \_**](uiauto-control-pattern-propids.md) Событие изменения свойства тогглетогглестатепропертид.</span><span class="sxs-lookup"><span data-stu-id="8b1fb-220">[**UIA\_ToggleToggleStatePropertyId**](uiauto-control-pattern-propids.md) property-changed event.</span></span>    | <span data-ttu-id="8b1fb-221">Если элемент управления поддерживает шаблон элемента управления [Toggle](uiauto-implementingtoggle.md) , он должен поддерживать это событие.</span><span class="sxs-lookup"><span data-stu-id="8b1fb-221">If the control supports the [Toggle](uiauto-implementingtoggle.md) control pattern, it must support this event.</span></span>           |



 

## <a name="related-topics"></a><span data-ttu-id="8b1fb-222">См. также</span><span class="sxs-lookup"><span data-stu-id="8b1fb-222">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="8b1fb-223">**Зрения**</span><span class="sxs-lookup"><span data-stu-id="8b1fb-223">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="8b1fb-224">Общие сведения о типах элементов управления автоматизации пользовательского интерфейса</span><span class="sxs-lookup"><span data-stu-id="8b1fb-224">UI Automation Control Types Overview</span></span>](uiauto-controltypesoverview.md)
</dt> <dt>

[<span data-ttu-id="8b1fb-225">Общие сведения о модели автоматизации пользовательского интерфейса</span><span class="sxs-lookup"><span data-stu-id="8b1fb-225">UI Automation Overview</span></span>](uiauto-uiautomationoverview.md)
</dt> </dl>

 

 




