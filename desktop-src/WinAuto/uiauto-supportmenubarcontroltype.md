---
title: Тип элемента управления MenuBar
description: В этом разделе содержатся сведения о поддержке автоматизации пользовательского интерфейса Майкрософт для типа элемента управления MenuBar.
ms.assetid: e93a92ce-7c98-4e8f-8a6a-a365ccb705d6
keywords:
- Модель автоматизации пользовательского интерфейса, поддержка типа элемента управления MenuBar
- Модель автоматизации пользовательского интерфейса, тип элемента управления MenuBar
- Модель автоматизации пользовательского интерфейса, древовидная структура для типа элемента управления MenuBar
- Модель автоматизации пользовательского интерфейса, свойства для типа элемента управления MenuBar
- Модель автоматизации пользовательского интерфейса, шаблоны элементов управления для типа элемента управления MenuBar
- Модель автоматизации пользовательского интерфейса, события для типа элемента управления MenuBar
- Древовидные структуры, тип элемента управления MenuBar
- свойства, тип элемента управления MenuBar
- шаблоны элементов управления, тип элемента управления MenuBar
- события, тип элемента управления MenuBar
- Поддержка типа элемента управления MenuBar
- Тип элемента управления MenuBar
- типы элементов управления, древовидная структура для типа элемента управления MenuBar
- типы элементов управления, шаблоны элементов управления для типа элемента управления MenuBar
- типы элементов управления, поддержка для MenuBar
- типы элементов управления, MenuBar
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b94bb60c13b5999bc8020eb70b84f6c932a2fb94
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "105691208"
---
# <a name="menubar-control-type"></a><span data-ttu-id="a41a2-119">Тип элемента управления MenuBar</span><span class="sxs-lookup"><span data-stu-id="a41a2-119">MenuBar Control Type</span></span>

<span data-ttu-id="a41a2-120">В этом разделе содержатся сведения о поддержке автоматизации пользовательского интерфейса Майкрософт для типа элемента управления **MenuBar** .</span><span class="sxs-lookup"><span data-stu-id="a41a2-120">This topic provides information about Microsoft UI Automation support for the **MenuBar** control type.</span></span>

<span data-ttu-id="a41a2-121">Элементы управления "строка меню" — это пример элементов управления, реализующих тип элемента управления **MenuBar** .</span><span class="sxs-lookup"><span data-stu-id="a41a2-121">Menu bar controls are an example of controls that implement the **MenuBar** control type.</span></span> <span data-ttu-id="a41a2-122">С помощью строк меню пользователи могут активировать команды и параметры, содержащиеся в приложении.</span><span class="sxs-lookup"><span data-stu-id="a41a2-122">Menu bars provide a means for users to activate commands and options contained in an application.</span></span>

<span data-ttu-id="a41a2-123">В следующих разделах определяется необходимая древовидная структура модели автоматизации пользовательского интерфейса, свойства, шаблоны элементов управления и события для типа элемента управления **MenuBar** .</span><span class="sxs-lookup"><span data-stu-id="a41a2-123">The following sections define the required UI Automation tree structure, properties, control patterns, and events for the **MenuBar** control type.</span></span> <span data-ttu-id="a41a2-124">Требования к автоматизации пользовательского интерфейса применяются ко всем элементам управления "строка меню", в которых платформа или платформа пользовательского интерфейса интегрирует поддержку автоматизации пользовательского интерфейса для типов элементов управления и шаблонов элементов управления.</span><span class="sxs-lookup"><span data-stu-id="a41a2-124">The UI Automation requirements apply to all menu bar controls where the UI framework/platform integrates UI Automation support for control types and control patterns.</span></span>

<span data-ttu-id="a41a2-125">В этом разделе содержатся следующие подразделы.</span><span class="sxs-lookup"><span data-stu-id="a41a2-125">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="a41a2-126">Типичная древовидная структура</span><span class="sxs-lookup"><span data-stu-id="a41a2-126">Typical Tree Structure</span></span>](#typical-tree-structure)
-   [<span data-ttu-id="a41a2-127">Соответствующие свойства</span><span class="sxs-lookup"><span data-stu-id="a41a2-127">Relevant Properties</span></span>](#relevant-properties)
-   [<span data-ttu-id="a41a2-128">Обязательные шаблоны элементов управления</span><span class="sxs-lookup"><span data-stu-id="a41a2-128">Required Control Patterns</span></span>](#required-control-patterns)
-   [<span data-ttu-id="a41a2-129">Обязательные события</span><span class="sxs-lookup"><span data-stu-id="a41a2-129">Required Events</span></span>](#required-events)
-   [<span data-ttu-id="a41a2-130">См. также</span><span class="sxs-lookup"><span data-stu-id="a41a2-130">Related topics</span></span>](#related-topics)

## <a name="typical-tree-structure"></a><span data-ttu-id="a41a2-131">Типичная древовидная структура</span><span class="sxs-lookup"><span data-stu-id="a41a2-131">Typical Tree Structure</span></span>

<span data-ttu-id="a41a2-132">В следующей таблице описывается типичный элемент управления и представление содержимого дерева модели автоматизации пользовательского интерфейса, которое относится к элементам управления "строка меню" и описывает, что может содержаться в каждом представлении.</span><span class="sxs-lookup"><span data-stu-id="a41a2-132">The following table depicts a typical control and content view of the UI Automation tree that pertains to menu bar controls and describes what can be contained in each view.</span></span> <span data-ttu-id="a41a2-133">Дополнительные сведения о дереве автоматизации пользовательского интерфейса см. в разделе [Общие сведения о дереве модели автоматизации пользовательского интерфейса](uiauto-treeoverview.md).</span><span class="sxs-lookup"><span data-stu-id="a41a2-133">For more information about the UI Automation tree, see [UI Automation Tree Overview](uiauto-treeoverview.md).</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="a41a2-134">Представление элемента управления</span><span class="sxs-lookup"><span data-stu-id="a41a2-134">Control View</span></span></th>
<th><span data-ttu-id="a41a2-135">Представление содержимого</span><span class="sxs-lookup"><span data-stu-id="a41a2-135">Content View</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><ul>
<li><span data-ttu-id="a41a2-136">MenuBar</span><span class="sxs-lookup"><span data-stu-id="a41a2-136">MenuBar</span></span>
<ul>
<li><span data-ttu-id="a41a2-137">MenuItem (1 или более)</span><span class="sxs-lookup"><span data-stu-id="a41a2-137">MenuItem (1 or more)</span></span></li>
<li><span data-ttu-id="a41a2-138">Другие элементы управления (0 или более)</span><span class="sxs-lookup"><span data-stu-id="a41a2-138">Other controls (0 or many)</span></span></li>
</ul></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="a41a2-139">Неприменимо</span><span class="sxs-lookup"><span data-stu-id="a41a2-139">Not applicable</span></span>
<ul>
<li><span data-ttu-id="a41a2-140">MenuItem (1 или более)</span><span class="sxs-lookup"><span data-stu-id="a41a2-140">MenuItem (1 or more)</span></span></li>
<li><span data-ttu-id="a41a2-141">Другие элементы управления (0 или более)</span><span class="sxs-lookup"><span data-stu-id="a41a2-141">Other controls (0 or many)</span></span></li>
</ul></li>
</ul></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="a41a2-142">Элемент управления "строка меню" всегда отображается в представлении элемента управления, но не в представлении содержимого, так как обычно не передает пользователю значимую информацию (если приложение не содержит более одной строки меню).</span><span class="sxs-lookup"><span data-stu-id="a41a2-142">A menu bar control always appears in the control view, but not in content view because it usually does not convey meaningful information to the end user (unless the application contains more than one menu bar).</span></span>

<span data-ttu-id="a41a2-143">Клиенты автоматизации пользовательского интерфейса могут прослушивать событие [**UIA \_ менумодестартевентид**](uiauto-event-ids.md) , чтобы убедиться, что они постоянно уведомляются, когда пользовательский интерфейс переходит в режим меню.</span><span class="sxs-lookup"><span data-stu-id="a41a2-143">UI Automation clients can listen for the [**UIA\_MenuModeStartEventId**](uiauto-event-ids.md) event to ensure that they are consistently notified when the UI enters menu mode.</span></span> <span data-ttu-id="a41a2-144">Когда приложение находится в режиме меню, все вводимые с клавиатуры данные могут быть захвачены для навигации по меню (например, при вводе текста может вызываться меню **сохранить** вместо ввода символа в клиентской области приложения).</span><span class="sxs-lookup"><span data-stu-id="a41a2-144">When the application is in menu mode, all of the keyboard input may be captured for menu navigation (for example, typing 's' might invoke the **Save** menu instead of typing the character on the application client area).</span></span> <span data-ttu-id="a41a2-145">Событие **UIA \_ менумодестартевентид** должно предшествовать первому событию [**UIA \_ менуопенедевентид**](uiauto-event-ids.md) , чтобы обеспечить логическую согласованность.</span><span class="sxs-lookup"><span data-stu-id="a41a2-145">The **UIA\_MenuModeStartEventId** event must precede the first [**UIA\_MenuOpenedEventId**](uiauto-event-ids.md) event to ensure logical consistency.</span></span> <span data-ttu-id="a41a2-146">Событие [**UIA \_ менумодиндевентид**](uiauto-event-ids.md) следует за последним событием [**UIA \_ менуклоседевентид**](uiauto-event-ids.md) .</span><span class="sxs-lookup"><span data-stu-id="a41a2-146">The [**UIA\_MenuModeEndEventId**](uiauto-event-ids.md) event follows the last [**UIA\_MenuClosedEventId**](uiauto-event-ids.md) event.</span></span> <span data-ttu-id="a41a2-147">Если щелкнуть пункт меню, можно сразу же запустить событие **UIA \_ менумодестартевентид** , за которым следует событие **UIA \_ менуопенедевентид** .</span><span class="sxs-lookup"><span data-stu-id="a41a2-147">Clicking a menu item may also immediately trigger the **UIA\_MenuModeStartEventId** event, followed by a **UIA\_MenuOpenedEventId** event.</span></span>

<span data-ttu-id="a41a2-148">Элемент управления "строка меню" может содержать другие элементы управления, такие как элементы управления и поля со списком, в его структуре.</span><span class="sxs-lookup"><span data-stu-id="a41a2-148">A menu bar control can contain other controls, such as edit controls and combo boxes, within its structure.</span></span> <span data-ttu-id="a41a2-149">Эти дополнительные элементы управления соответствуют "другим элементам управления", перечисленным выше в представлениях элемента управления и содержимого.</span><span class="sxs-lookup"><span data-stu-id="a41a2-149">These additional controls correspond to the "other controls" listed above in the control and content views.</span></span>

## <a name="relevant-properties"></a><span data-ttu-id="a41a2-150">Соответствующие свойства</span><span class="sxs-lookup"><span data-stu-id="a41a2-150">Relevant Properties</span></span>

<span data-ttu-id="a41a2-151">В следующей таблице перечислены свойства модели автоматизации пользовательского интерфейса, значения или определения которых особенно важны для типа элемента управления **MenuBar** .</span><span class="sxs-lookup"><span data-stu-id="a41a2-151">The following table lists the UI Automation properties whose value or definition is especially relevant to the **MenuBar** control type.</span></span> <span data-ttu-id="a41a2-152">Дополнительные сведения о свойствах модели автоматизации пользовательского интерфейса см. в разделе [Получение свойств элементов модели автоматизации пользовательского интерфейса](uiauto-propertiesforclients.md).</span><span class="sxs-lookup"><span data-stu-id="a41a2-152">For more information about UI Automation properties, see [Retrieving Properties from UI Automation Elements](uiauto-propertiesforclients.md).</span></span>



| <span data-ttu-id="a41a2-153">Свойство модели автоматизации пользовательского интерфейса</span><span class="sxs-lookup"><span data-stu-id="a41a2-153">UI Automation Property</span></span>                                                                                              | <span data-ttu-id="a41a2-154">Значение</span><span class="sxs-lookup"><span data-stu-id="a41a2-154">Value</span></span>       | <span data-ttu-id="a41a2-155">Примечания</span><span class="sxs-lookup"><span data-stu-id="a41a2-155">Notes</span></span>                                                                                                                                                                                                                                    |
|---------------------------------------------------------------------------------------------------------------------|-------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="a41a2-156">**UIA \_ акцелераторкэйпропертид**</span><span class="sxs-lookup"><span data-stu-id="a41a2-156">**UIA\_AcceleratorKeyPropertyId**</span></span>](uiauto-automation-element-propids.md)             | <span data-ttu-id="a41a2-157">NULL</span><span class="sxs-lookup"><span data-stu-id="a41a2-157">NULL</span></span>        | <span data-ttu-id="a41a2-158">Строки меню обычно не имеют сочетаний клавиш.</span><span class="sxs-lookup"><span data-stu-id="a41a2-158">Menu bars usually do not have accelerator keys.</span></span>                                                                                                                                                                                          |
| [<span data-ttu-id="a41a2-159">**UIA \_ акцесскэйпропертид**</span><span class="sxs-lookup"><span data-stu-id="a41a2-159">**UIA\_AccessKeyPropertyId**</span></span>](uiauto-automation-element-propids.md)                       | <span data-ttu-id="a41a2-160">ALT</span><span class="sxs-lookup"><span data-stu-id="a41a2-160">"ALT"</span></span>       | <span data-ttu-id="a41a2-161">Нажатие клавиши ALT обычно помещает фокус на строку меню в приложении.</span><span class="sxs-lookup"><span data-stu-id="a41a2-161">Pressing the ALT key should usually bring focus to the menu bar within the application.</span></span>                                                                                                                                                  |
| [<span data-ttu-id="a41a2-162">**UIA \_ баундингректанглепропертид**</span><span class="sxs-lookup"><span data-stu-id="a41a2-162">**UIA\_BoundingRectanglePropertyId**</span></span>](uiauto-automation-element-propids.md)       | <span data-ttu-id="a41a2-163">См. примечания.</span><span class="sxs-lookup"><span data-stu-id="a41a2-163">See notes.</span></span>  | <span data-ttu-id="a41a2-164">Значение, представляемое этим свойством, должно включать все содержащиеся в нем элементы управления.</span><span class="sxs-lookup"><span data-stu-id="a41a2-164">The value exposed by this property must include all of the controls contained within it.</span></span>                                                                                                                                                 |
| [<span data-ttu-id="a41a2-165">**UIA \_ контролтипепропертид**</span><span class="sxs-lookup"><span data-stu-id="a41a2-165">**UIA\_ControlTypePropertyId**</span></span>](uiauto-automation-element-propids.md)                   | <span data-ttu-id="a41a2-166">**MenuBar**</span><span class="sxs-lookup"><span data-stu-id="a41a2-166">**MenuBar**</span></span> |                                                                                                                                                                                                                                          |
| [<span data-ttu-id="a41a2-167">**UIA \_ исконтентелементпропертид**</span><span class="sxs-lookup"><span data-stu-id="a41a2-167">**UIA\_IsContentElementPropertyId**</span></span>](uiauto-automation-element-propids.md)         | <span data-ttu-id="a41a2-168">FALSE</span><span class="sxs-lookup"><span data-stu-id="a41a2-168">FALSE</span></span>       | <span data-ttu-id="a41a2-169">Элемент управления "строка меню" не включен в представление содержимого дерева модели автоматизации пользовательского интерфейса.</span><span class="sxs-lookup"><span data-stu-id="a41a2-169">The menu bar control is not included in the content view of the UI Automation tree.</span></span>                                                                                                                                                      |
| [<span data-ttu-id="a41a2-170">**UIA \_ исконтролелементпропертид**</span><span class="sxs-lookup"><span data-stu-id="a41a2-170">**UIA\_IsControlElementPropertyId**</span></span>](uiauto-automation-element-propids.md)         | <span data-ttu-id="a41a2-171">true</span><span class="sxs-lookup"><span data-stu-id="a41a2-171">TRUE</span></span>        | <span data-ttu-id="a41a2-172">Элемент управления "строка меню" всегда включается в представление элемента управления дерева модели автоматизации пользовательского интерфейса.</span><span class="sxs-lookup"><span data-stu-id="a41a2-172">The menu bar control is always included in the control view of the UI Automation tree.</span></span>                                                                                                                                                   |
| [<span data-ttu-id="a41a2-173">**UIA \_ искэйбоардфокусаблепропертид**</span><span class="sxs-lookup"><span data-stu-id="a41a2-173">**UIA\_IsKeyboardFocusablePropertyId**</span></span>](uiauto-automation-element-propids.md)   | <span data-ttu-id="a41a2-174">true</span><span class="sxs-lookup"><span data-stu-id="a41a2-174">TRUE</span></span>        | <span data-ttu-id="a41a2-175">Элементы управления "Строка меню" являются фокусируемыми с помощью клавиатуры, так как элементы управления, содержащиеся в них, могут принимать фокус клавиатуры.</span><span class="sxs-lookup"><span data-stu-id="a41a2-175">Menu bar controls are keyboard-focusable because the controls they contain can take keyboard focus.</span></span>                                                                                                                                      |
| [<span data-ttu-id="a41a2-176">**UIA \_ исоффскринпропертид**</span><span class="sxs-lookup"><span data-stu-id="a41a2-176">**UIA\_IsOffscreenPropertyId**</span></span>](uiauto-automation-element-propids.md)                   | <span data-ttu-id="a41a2-177">См. примечания.</span><span class="sxs-lookup"><span data-stu-id="a41a2-177">See notes.</span></span>  | <span data-ttu-id="a41a2-178">Значение этого свойства зависит от того, можно ли видеть элемент управления на экране.</span><span class="sxs-lookup"><span data-stu-id="a41a2-178">The value of this property depends on whether the control is viewable on the screen.</span></span>                                                                                                                                                     |
| [<span data-ttu-id="a41a2-179">**UIA \_ лабеледбипропертид**</span><span class="sxs-lookup"><span data-stu-id="a41a2-179">**UIA\_LabeledByPropertyId**</span></span>](uiauto-automation-element-propids.md)                       | <span data-ttu-id="a41a2-180">NULL</span><span class="sxs-lookup"><span data-stu-id="a41a2-180">NULL</span></span>        | <span data-ttu-id="a41a2-181">Элементы управления "строка меню" обычно не имеют метки.</span><span class="sxs-lookup"><span data-stu-id="a41a2-181">Menu bar controls usually do not have a label.</span></span>                                                                                                                                                                                           |
| [<span data-ttu-id="a41a2-182">**UIA \_ локализедконтролтипепропертид**</span><span class="sxs-lookup"><span data-stu-id="a41a2-182">**UIA\_LocalizedControlTypePropertyId**</span></span>](uiauto-automation-element-propids.md) | <span data-ttu-id="a41a2-183">См. примечания.</span><span class="sxs-lookup"><span data-stu-id="a41a2-183">See notes.</span></span>  | <span data-ttu-id="a41a2-184">Локализованная строка, соответствующая типу элемента управления **MenuBar** .</span><span class="sxs-lookup"><span data-stu-id="a41a2-184">Localized string corresponding to the **MenuBar** control type.</span></span> <span data-ttu-id="a41a2-185">Значение по умолчанию — "строка меню" для en-US или English (США).</span><span class="sxs-lookup"><span data-stu-id="a41a2-185">The default value is "menu bar" for en-US or English (United States).</span></span>                                                                                                    |
| [<span data-ttu-id="a41a2-186">**UIA \_ намепропертид**</span><span class="sxs-lookup"><span data-stu-id="a41a2-186">**UIA\_NamePropertyId**</span></span>](uiauto-automation-element-propids.md)                                 | <span data-ttu-id="a41a2-187">См. примечания.</span><span class="sxs-lookup"><span data-stu-id="a41a2-187">See notes.</span></span>  | <span data-ttu-id="a41a2-188">Элементу управления "Строка меню" имя не требуется, кроме случая, когда в приложении имеется несколько строк меню.</span><span class="sxs-lookup"><span data-stu-id="a41a2-188">The menu bar control does not need a name unless an application has more than one menu bar.</span></span> <span data-ttu-id="a41a2-189">Если в приложении имеется несколько строк меню, используйте это свойство для различения имен, таких как "Форматирование" или "структурирование".</span><span class="sxs-lookup"><span data-stu-id="a41a2-189">If there is more than one menu bar in an application, use this property to expose distinguishing names, such as "Formatting" or "Outlining".</span></span> |
| [<span data-ttu-id="a41a2-190">**UIA \_ ориентатионпропертид**</span><span class="sxs-lookup"><span data-stu-id="a41a2-190">**UIA\_OrientationPropertyId**</span></span>](uiauto-automation-element-propids.md)                   | <span data-ttu-id="a41a2-191">Зависит</span><span class="sxs-lookup"><span data-stu-id="a41a2-191">Depends</span></span>     | <span data-ttu-id="a41a2-192">Это свойство показывает, является ли элемент управления "Строка меню" горизонтальным или вертикальным.</span><span class="sxs-lookup"><span data-stu-id="a41a2-192">This property exposes whether the menu bar control is horizontal or vertical.</span></span>                                                                                                                                                            |



 

## <a name="required-control-patterns"></a><span data-ttu-id="a41a2-193">Обязательные шаблоны элементов управления</span><span class="sxs-lookup"><span data-stu-id="a41a2-193">Required Control Patterns</span></span>

<span data-ttu-id="a41a2-194">В следующей таблице перечислены шаблоны элементов управления модели автоматизации пользовательского интерфейса, которые должны поддерживаться элементами управления "строка меню".</span><span class="sxs-lookup"><span data-stu-id="a41a2-194">The following table lists the UI Automation control patterns required to be supported by menu bar controls.</span></span> <span data-ttu-id="a41a2-195">Дополнительные сведения о шаблонах элементов управления см. в разделе [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md).</span><span class="sxs-lookup"><span data-stu-id="a41a2-195">For more information on control patterns, see [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md).</span></span>



| <span data-ttu-id="a41a2-196">Шаблон элемента управления</span><span class="sxs-lookup"><span data-stu-id="a41a2-196">Control Pattern</span></span>                                                   | <span data-ttu-id="a41a2-197">Поддержка</span><span class="sxs-lookup"><span data-stu-id="a41a2-197">Support</span></span> | <span data-ttu-id="a41a2-198">Примечания</span><span class="sxs-lookup"><span data-stu-id="a41a2-198">Notes</span></span>                                                                                                                                       |
|-------------------------------------------------------------------|---------|---------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="a41a2-199">**IExpandCollapseProvider**</span><span class="sxs-lookup"><span data-stu-id="a41a2-199">**IExpandCollapseProvider**</span></span>](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iexpandcollapseprovider) | <span data-ttu-id="a41a2-200">Зависит</span><span class="sxs-lookup"><span data-stu-id="a41a2-200">Depends</span></span> | <span data-ttu-id="a41a2-201">Если элемент управления можно развернуть или свернуть, он должен реализовать шаблон элемента управления [ExpandCollapse](uiauto-implementingexpandcollapse.md) .</span><span class="sxs-lookup"><span data-stu-id="a41a2-201">If the control can be expanded or collapsed, it must implement the [ExpandCollapse](uiauto-implementingexpandcollapse.md) control pattern.</span></span> |
| [<span data-ttu-id="a41a2-202">**IDockProvider**</span><span class="sxs-lookup"><span data-stu-id="a41a2-202">**IDockProvider**</span></span>](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-idockprovider)                     | <span data-ttu-id="a41a2-203">Зависит</span><span class="sxs-lookup"><span data-stu-id="a41a2-203">Depends</span></span> | <span data-ttu-id="a41a2-204">Если элемент управления можно закрепить в различных частях экрана, он должен реализовать шаблон элемента управления [Dock](uiauto-implementingdock.md) .</span><span class="sxs-lookup"><span data-stu-id="a41a2-204">If the control can be docked to different parts of the screen, it must implement the [Dock](uiauto-implementingdock.md) control pattern.</span></span>   |
| [<span data-ttu-id="a41a2-205">**ITransformProvider**</span><span class="sxs-lookup"><span data-stu-id="a41a2-205">**ITransformProvider**</span></span>](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itransformprovider)           | <span data-ttu-id="a41a2-206">Зависит</span><span class="sxs-lookup"><span data-stu-id="a41a2-206">Depends</span></span> | <span data-ttu-id="a41a2-207">Если размер элемента управления можно изменить, повернуть или переместить, он должен реализовать шаблон элемента управления [Transform](uiauto-implementingtransform.md) .</span><span class="sxs-lookup"><span data-stu-id="a41a2-207">If the control can be resized, rotated, or moved, it must implement the [Transform](uiauto-implementingtransform.md) control pattern.</span></span>      |



 

## <a name="required-events"></a><span data-ttu-id="a41a2-208">Обязательные события</span><span class="sxs-lookup"><span data-stu-id="a41a2-208">Required Events</span></span>

<span data-ttu-id="a41a2-209">В следующей таблице перечислены события модели автоматизации пользовательского интерфейса, которые должны поддерживаться элементами управления "строка меню".</span><span class="sxs-lookup"><span data-stu-id="a41a2-209">The following table lists the UI Automation events that menu bar controls are required to support.</span></span> <span data-ttu-id="a41a2-210">Дополнительные сведения о событиях см. в разделе [UI Automation Events Overview](uiauto-eventsoverview.md).</span><span class="sxs-lookup"><span data-stu-id="a41a2-210">For more information on events, see [UI Automation Events Overview](uiauto-eventsoverview.md).</span></span>



| <span data-ttu-id="a41a2-211">Событие автоматизации пользовательского интерфейса</span><span class="sxs-lookup"><span data-stu-id="a41a2-211">UI Automation Event</span></span>                                                                                                                                                | <span data-ttu-id="a41a2-212">Примечания</span><span class="sxs-lookup"><span data-stu-id="a41a2-212">Notes</span></span>                                                                                                                            |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="a41a2-213">**UIA \_ аутоматионфокусчанжедевентид**</span><span class="sxs-lookup"><span data-stu-id="a41a2-213">**UIA\_AutomationFocusChangedEventId**</span></span>](uiauto-event-ids.md)                                                                   |                                                                                                                                  |
| <span data-ttu-id="a41a2-214">[**UIA \_**](uiauto-automation-element-propids.md) Событие изменения свойства баундингректанглепропертид.</span><span class="sxs-lookup"><span data-stu-id="a41a2-214">[**UIA\_BoundingRectanglePropertyId**](uiauto-automation-element-propids.md) property-changed event.</span></span>                              |                                                                                                                                  |
| <span data-ttu-id="a41a2-215">[**UIA \_**](uiauto-control-pattern-propids.md) Событие изменения свойства експандколлапсикспандколлапсестатепропертид.</span><span class="sxs-lookup"><span data-stu-id="a41a2-215">[**UIA\_ExpandCollapseExpandCollapseStatePropertyId**](uiauto-control-pattern-propids.md) property-changed event.</span></span> | <span data-ttu-id="a41a2-216">Если элемент управления поддерживает шаблон элемента управления [ExpandCollapse](uiauto-implementingexpandcollapse.md) , он должен поддерживать это событие.</span><span class="sxs-lookup"><span data-stu-id="a41a2-216">If the control supports the [ExpandCollapse](uiauto-implementingexpandcollapse.md) control pattern, it must support this event.</span></span> |
| <span data-ttu-id="a41a2-217">[**UIA \_**](uiauto-automation-element-propids.md) Событие изменения свойства исенабледпропертид.</span><span class="sxs-lookup"><span data-stu-id="a41a2-217">[**UIA\_IsEnabledPropertyId**](uiauto-automation-element-propids.md) property-changed event.</span></span>                                              | <span data-ttu-id="a41a2-218">Если элемент управления поддерживает свойство « [**включено**](uiauto-automation-element-propids.md) », оно должно поддерживать это событие.</span><span class="sxs-lookup"><span data-stu-id="a41a2-218">If the control supports the [**IsEnabled**](uiauto-automation-element-propids.md) property, it must support this event.</span></span>         |
| <span data-ttu-id="a41a2-219">[**UIA \_**](uiauto-automation-element-propids.md) Событие изменения свойства исоффскринпропертид.</span><span class="sxs-lookup"><span data-stu-id="a41a2-219">[**UIA\_IsOffscreenPropertyId**](uiauto-automation-element-propids.md) property-changed event.</span></span>                                          | <span data-ttu-id="a41a2-220">Если элемент управления поддерживает свойство [**исоффскрин**](uiauto-automation-element-propids.md) , он должен поддерживать это событие.</span><span class="sxs-lookup"><span data-stu-id="a41a2-220">If the control supports the [**IsOffscreen**](uiauto-automation-element-propids.md) property, it must support this event.</span></span>       |
| [<span data-ttu-id="a41a2-221">**UIA \_ структуречанжедевентид**</span><span class="sxs-lookup"><span data-stu-id="a41a2-221">**UIA\_StructureChangedEventId**</span></span>](uiauto-event-ids.md)                                                                               |                                                                                                                                  |



 

## <a name="related-topics"></a><span data-ttu-id="a41a2-222">См. также</span><span class="sxs-lookup"><span data-stu-id="a41a2-222">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="a41a2-223">**Зрения**</span><span class="sxs-lookup"><span data-stu-id="a41a2-223">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="a41a2-224">Общие сведения о типах элементов управления автоматизации пользовательского интерфейса</span><span class="sxs-lookup"><span data-stu-id="a41a2-224">UI Automation Control Types Overview</span></span>](uiauto-controltypesoverview.md)
</dt> <dt>

[<span data-ttu-id="a41a2-225">Общие сведения о модели автоматизации пользовательского интерфейса</span><span class="sxs-lookup"><span data-stu-id="a41a2-225">UI Automation Overview</span></span>](uiauto-uiautomationoverview.md)
</dt> </dl>

 

 




