---
title: Тип элемента управления StatusBar
description: В этом разделе содержатся сведения о поддержке автоматизации пользовательского интерфейса Майкрософт для типа элемента управления StatusBar.
ms.assetid: a28df0a1-95a8-4941-a00d-1f5570589626
keywords:
- Модель автоматизации пользовательского интерфейса, поддержка типа элемента управления StatusBar
- Модель автоматизации пользовательского интерфейса, тип элемента управления StatusBar
- Модель автоматизации пользовательского интерфейса, структура дерева для типа элемента управления StatusBar
- Модель автоматизации пользовательского интерфейса, свойства для типа элемента управления StatusBar
- Модель автоматизации пользовательского интерфейса, шаблоны элементов управления для типа элемента управления StatusBar
- Модель автоматизации пользовательского интерфейса, события для типа элемента управления StatusBar
- Древовидные структуры, тип элемента управления StatusBar
- свойства, тип элемента управления StatusBar
- шаблоны элементов управления, тип элемента управления StatusBar
- события, тип элемента управления StatusBar
- Поддержка типа элемента управления StatusBar
- StatusBar - тип элемента управления
- типы элементов управления, древовидная структура для типа элемента управления StatusBar
- типы элементов управления, шаблоны элементов управления для типа элемента управления StatusBar
- типы элементов управления, поддержка StatusBar
- типы элементов управления, StatusBar
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 65ace64d34429a6d381dfdef2d99d82a3693fca2
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104331104"
---
# <a name="statusbar-control-type"></a><span data-ttu-id="ca480-119">Тип элемента управления StatusBar</span><span class="sxs-lookup"><span data-stu-id="ca480-119">StatusBar Control Type</span></span>

<span data-ttu-id="ca480-120">В этом разделе содержатся сведения о поддержке автоматизации пользовательского интерфейса Майкрософт для типа элемента управления **StatusBar** .</span><span class="sxs-lookup"><span data-stu-id="ca480-120">This topic provides information about Microsoft UI Automation support for the **StatusBar** control type.</span></span>

<span data-ttu-id="ca480-121">Элемент управления "Строка состояния" отображает сведения об объекте, который просматривается в окне приложения, сведения о компонентах этого объекта или контекстную информацию, относящуюся к работе объекта внутри приложения.</span><span class="sxs-lookup"><span data-stu-id="ca480-121">A status bar control displays information about an object being viewed in a window of an application, the object's component, or contextual information that relates to that object's operation within your application.</span></span>

<span data-ttu-id="ca480-122">В следующих разделах определяется необходимая древовидная структура модели автоматизации пользовательского интерфейса, свойства, шаблоны элементов управления и события для типа элемента управления **StatusBar** .</span><span class="sxs-lookup"><span data-stu-id="ca480-122">The following sections define the required UI Automation tree structure, properties, control patterns, and events for the **StatusBar** control type.</span></span> <span data-ttu-id="ca480-123">Требования к автоматизации пользовательского интерфейса применяются ко всем элементам управления "строка состояния", в которых платформа или платформа пользовательского интерфейса интегрирует поддержку автоматизации пользовательского интерфейса для типов элементов управления и шаблонов элементов управления.</span><span class="sxs-lookup"><span data-stu-id="ca480-123">The UI Automation requirements apply to all status bar controls where the UI framework/platform integrates UI Automation support for control types and control patterns.</span></span>

<span data-ttu-id="ca480-124">В этом разделе содержатся следующие подразделы.</span><span class="sxs-lookup"><span data-stu-id="ca480-124">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="ca480-125">Типичная древовидная структура</span><span class="sxs-lookup"><span data-stu-id="ca480-125">Typical Tree Structure</span></span>](#typical-tree-structure)
-   [<span data-ttu-id="ca480-126">Соответствующие свойства</span><span class="sxs-lookup"><span data-stu-id="ca480-126">Relevant Properties</span></span>](#relevant-properties)
-   [<span data-ttu-id="ca480-127">Обязательные шаблоны элементов управления</span><span class="sxs-lookup"><span data-stu-id="ca480-127">Required Control Patterns</span></span>](#required-control-patterns)
-   [<span data-ttu-id="ca480-128">Обязательные события</span><span class="sxs-lookup"><span data-stu-id="ca480-128">Required Events</span></span>](#required-events)
-   [<span data-ttu-id="ca480-129">Замечания</span><span class="sxs-lookup"><span data-stu-id="ca480-129">Remarks</span></span>](#remarks)
-   [<span data-ttu-id="ca480-130">См. также</span><span class="sxs-lookup"><span data-stu-id="ca480-130">Related topics</span></span>](#related-topics)

## <a name="typical-tree-structure"></a><span data-ttu-id="ca480-131">Типичная древовидная структура</span><span class="sxs-lookup"><span data-stu-id="ca480-131">Typical Tree Structure</span></span>

<span data-ttu-id="ca480-132">В следующей таблице описывается типичный элемент управления и представление содержимого дерева модели автоматизации пользовательского интерфейса, которое относится к элементам управления "строка состояния" и описывает, что может содержаться в каждом представлении.</span><span class="sxs-lookup"><span data-stu-id="ca480-132">The following table depicts a typical control and content view of the UI Automation tree that pertains to status bar controls and describes what can be contained in each view.</span></span> <span data-ttu-id="ca480-133">Дополнительные сведения о дереве автоматизации пользовательского интерфейса см. в разделе [Общие сведения о дереве модели автоматизации пользовательского интерфейса](uiauto-treeoverview.md).</span><span class="sxs-lookup"><span data-stu-id="ca480-133">For more information about the UI Automation tree, see [UI Automation Tree Overview](uiauto-treeoverview.md).</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="ca480-134">Представление элемента управления</span><span class="sxs-lookup"><span data-stu-id="ca480-134">Control View</span></span></th>
<th><span data-ttu-id="ca480-135">Представление содержимого</span><span class="sxs-lookup"><span data-stu-id="ca480-135">Content View</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><ul>
<li><span data-ttu-id="ca480-136">StatusBar</span><span class="sxs-lookup"><span data-stu-id="ca480-136">StatusBar</span></span>
<ul>
<li><span data-ttu-id="ca480-137">Edit (0 или более)</span><span class="sxs-lookup"><span data-stu-id="ca480-137">Edit (0 or more)</span></span></li>
<li><span data-ttu-id="ca480-138">ProgressBar (0 или более)</span><span class="sxs-lookup"><span data-stu-id="ca480-138">ProgressBar (0 or many)</span></span></li>
<li><span data-ttu-id="ca480-139">Image (0 или более)</span><span class="sxs-lookup"><span data-stu-id="ca480-139">Image (0 or many)</span></span></li>
<li><span data-ttu-id="ca480-140">Button (0 или более)</span><span class="sxs-lookup"><span data-stu-id="ca480-140">Button (0 or many)</span></span></li>
</ul></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="ca480-141">StatusBar</span><span class="sxs-lookup"><span data-stu-id="ca480-141">StatusBar</span></span>
<ul>
<li><span data-ttu-id="ca480-142">Edit (0 или более)</span><span class="sxs-lookup"><span data-stu-id="ca480-142">Edit (0 or more)</span></span></li>
<li><span data-ttu-id="ca480-143">ProgressBar (0 или более)</span><span class="sxs-lookup"><span data-stu-id="ca480-143">ProgressBar (0 or many)</span></span></li>
<li><span data-ttu-id="ca480-144">Image (0 или более)</span><span class="sxs-lookup"><span data-stu-id="ca480-144">Image (0 or many)</span></span></li>
<li><span data-ttu-id="ca480-145">Button (0 или более)</span><span class="sxs-lookup"><span data-stu-id="ca480-145">Button (0 or many)</span></span></li>
</ul></li>
</ul></td>
</tr>
</tbody>
</table>



 

## <a name="relevant-properties"></a><span data-ttu-id="ca480-146">Соответствующие свойства</span><span class="sxs-lookup"><span data-stu-id="ca480-146">Relevant Properties</span></span>

<span data-ttu-id="ca480-147">В следующей таблице перечислены свойства модели автоматизации пользовательского интерфейса, значения или определения которых особенно важны для элементов управления "строка состояния".</span><span class="sxs-lookup"><span data-stu-id="ca480-147">The following table lists the UI Automation properties whose value or definition is especially relevant to the status bar controls.</span></span> <span data-ttu-id="ca480-148">Дополнительные сведения о свойствах модели автоматизации пользовательского интерфейса см. в разделе [Получение свойств элементов модели автоматизации пользовательского интерфейса](uiauto-propertiesforclients.md).</span><span class="sxs-lookup"><span data-stu-id="ca480-148">For more information about UI Automation properties, see [Retrieving Properties from UI Automation Elements](uiauto-propertiesforclients.md).</span></span>



| <span data-ttu-id="ca480-149">Свойство модели автоматизации пользовательского интерфейса</span><span class="sxs-lookup"><span data-stu-id="ca480-149">UI Automation Property</span></span>                                                                                              | <span data-ttu-id="ca480-150">Значение</span><span class="sxs-lookup"><span data-stu-id="ca480-150">Value</span></span>         | <span data-ttu-id="ca480-151">Примечания</span><span class="sxs-lookup"><span data-stu-id="ca480-151">Notes</span></span>                                                                                                                                                                                                               |
|---------------------------------------------------------------------------------------------------------------------|---------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="ca480-152">**UIA \_ аутоматионидпропертид**</span><span class="sxs-lookup"><span data-stu-id="ca480-152">**UIA\_AutomationIdPropertyId**</span></span>](uiauto-automation-element-propids.md)                 | <span data-ttu-id="ca480-153">См. примечания.</span><span class="sxs-lookup"><span data-stu-id="ca480-153">See notes.</span></span>    | <span data-ttu-id="ca480-154">Значение этого свойства должно быть уникальным среди всех одноранговых элементов в необработанном представлении дерева модели автоматизации пользовательского интерфейса.</span><span class="sxs-lookup"><span data-stu-id="ca480-154">The value of this property must be unique among all peer elements in the raw view of the UI Automation tree.</span></span>                                                                                                        |
| [<span data-ttu-id="ca480-155">**UIA \_ баундингректанглепропертид**</span><span class="sxs-lookup"><span data-stu-id="ca480-155">**UIA\_BoundingRectanglePropertyId**</span></span>](uiauto-automation-element-propids.md)       | <span data-ttu-id="ca480-156">См. примечания.</span><span class="sxs-lookup"><span data-stu-id="ca480-156">See notes.</span></span>    | <span data-ttu-id="ca480-157">Ограничивающий прямоугольник строки состояния должен охватывать все элементы управления, содержащиеся в ней.</span><span class="sxs-lookup"><span data-stu-id="ca480-157">The bounding rectangle of a status bar must encompass all of the controls contained within it.</span></span>                                                                                                                      |
| [<span data-ttu-id="ca480-158">**UIA \_ кликкаблепоинтпропертид**</span><span class="sxs-lookup"><span data-stu-id="ca480-158">**UIA\_ClickablePointPropertyId**</span></span>](uiauto-automation-element-propids.md)             | <span data-ttu-id="ca480-159">См. примечания.</span><span class="sxs-lookup"><span data-stu-id="ca480-159">See notes.</span></span>    | <span data-ttu-id="ca480-160">Поддерживается при наличии ограничивающего прямоугольника.</span><span class="sxs-lookup"><span data-stu-id="ca480-160">Supported if there is a bounding rectangle.</span></span> <span data-ttu-id="ca480-161">Если в ограничивающем прямоугольнике есть области, которые не могут быть выбраны, а элемент выполняет специализированное тестирование нажатия, Переопределите это и предоставьте точку для щелчка.</span><span class="sxs-lookup"><span data-stu-id="ca480-161">If there are areas within the bounding rectangle that are not clickable, and the element performs specialized hit testing, override this and provide a clickable point.</span></span> |
| [<span data-ttu-id="ca480-162">**UIA \_ контролтипепропертид**</span><span class="sxs-lookup"><span data-stu-id="ca480-162">**UIA\_ControlTypePropertyId**</span></span>](uiauto-automation-element-propids.md)                   | <span data-ttu-id="ca480-163">**StatusBar**</span><span class="sxs-lookup"><span data-stu-id="ca480-163">**StatusBar**</span></span> |                                                                                                                                                                                                                     |
| [<span data-ttu-id="ca480-164">**UIA \_ исконтентелементпропертид**</span><span class="sxs-lookup"><span data-stu-id="ca480-164">**UIA\_IsContentElementPropertyId**</span></span>](uiauto-automation-element-propids.md)         | <span data-ttu-id="ca480-165">true</span><span class="sxs-lookup"><span data-stu-id="ca480-165">TRUE</span></span>          | <span data-ttu-id="ca480-166">Элемент управления "строка состояния" всегда включается в представление содержимого дерева модели автоматизации пользовательского интерфейса.</span><span class="sxs-lookup"><span data-stu-id="ca480-166">The status bar control is always included in the content view of the UI Automation tree.</span></span>                                                                                                                            |
| [<span data-ttu-id="ca480-167">**UIA \_ исконтролелементпропертид**</span><span class="sxs-lookup"><span data-stu-id="ca480-167">**UIA\_IsControlElementPropertyId**</span></span>](uiauto-automation-element-propids.md)         | <span data-ttu-id="ca480-168">true</span><span class="sxs-lookup"><span data-stu-id="ca480-168">TRUE</span></span>          | <span data-ttu-id="ca480-169">Элемент управления "строка состояния" всегда включается в представление элемента управления дерева модели автоматизации пользовательского интерфейса.</span><span class="sxs-lookup"><span data-stu-id="ca480-169">The status bar control is always included in the control view of the UI Automation tree.</span></span>                                                                                                                            |
| [<span data-ttu-id="ca480-170">**UIA \_ искэйбоардфокусаблепропертид**</span><span class="sxs-lookup"><span data-stu-id="ca480-170">**UIA\_IsKeyboardFocusablePropertyId**</span></span>](uiauto-automation-element-propids.md)   | <span data-ttu-id="ca480-171">Зависит</span><span class="sxs-lookup"><span data-stu-id="ca480-171">Depends</span></span>       | <span data-ttu-id="ca480-172">Если элемент управления может получать фокус клавиатуры, он должен поддерживать это свойство.</span><span class="sxs-lookup"><span data-stu-id="ca480-172">If the control can receive keyboard focus, it must support this property.</span></span>                                                                                                                                           |
| [<span data-ttu-id="ca480-173">**UIA \_ исоффскринпропертид**</span><span class="sxs-lookup"><span data-stu-id="ca480-173">**UIA\_IsOffscreenPropertyId**</span></span>](uiauto-automation-element-propids.md)                   | <span data-ttu-id="ca480-174">Зависит</span><span class="sxs-lookup"><span data-stu-id="ca480-174">Depends</span></span>       | <span data-ttu-id="ca480-175">Если элемент управления "строка состояния" в настоящее время не виден, он возвратит значение TRUE для этого свойства.</span><span class="sxs-lookup"><span data-stu-id="ca480-175">If a status bar control is not currently visible, it will return TRUE for this property.</span></span>                                                                                                                            |
| [<span data-ttu-id="ca480-176">**UIA \_ лабеледбипропертид**</span><span class="sxs-lookup"><span data-stu-id="ca480-176">**UIA\_LabeledByPropertyId**</span></span>](uiauto-automation-element-propids.md)                       | <span data-ttu-id="ca480-177">NULL</span><span class="sxs-lookup"><span data-stu-id="ca480-177">NULL</span></span>          | <span data-ttu-id="ca480-178">Элемент управления "строка состояния" обычно не имеет метки.</span><span class="sxs-lookup"><span data-stu-id="ca480-178">The status bar control typically does not have a label.</span></span>                                                                                                                                                             |
| [<span data-ttu-id="ca480-179">**UIA \_ локализедконтролтипепропертид**</span><span class="sxs-lookup"><span data-stu-id="ca480-179">**UIA\_LocalizedControlTypePropertyId**</span></span>](uiauto-automation-element-propids.md) | <span data-ttu-id="ca480-180">См. примечания.</span><span class="sxs-lookup"><span data-stu-id="ca480-180">See notes.</span></span>    | <span data-ttu-id="ca480-181">Локализованная строка, соответствующая типу элемента управления **StatusBar** .</span><span class="sxs-lookup"><span data-stu-id="ca480-181">Localized string corresponding to the **StatusBar** control type.</span></span> <span data-ttu-id="ca480-182">По умолчанию используется значение "строка состояния" для en-US или English (США).</span><span class="sxs-lookup"><span data-stu-id="ca480-182">The default value is "status bar" for en-US or English (United States).</span></span>                                                                           |
| [<span data-ttu-id="ca480-183">**UIA \_ намепропертид**</span><span class="sxs-lookup"><span data-stu-id="ca480-183">**UIA\_NamePropertyId**</span></span>](uiauto-automation-element-propids.md)                                 | <span data-ttu-id="ca480-184">См. примечания.</span><span class="sxs-lookup"><span data-stu-id="ca480-184">See notes.</span></span>    | <span data-ttu-id="ca480-185">Элементу управления "Строка состояния" имя не требуется, кроме случая, когда в приложении используется несколько строк состояния.</span><span class="sxs-lookup"><span data-stu-id="ca480-185">The status bar control does not need a name unless more than one is used within an application.</span></span> <span data-ttu-id="ca480-186">В этом случае каждую строку следует отличать такими именами, как "состояние Интернета" или "состояние приложения".</span><span class="sxs-lookup"><span data-stu-id="ca480-186">In this case, distinguish each bar with names such as "Internet Status" or "Application Status".</span></span>                    |
| [<span data-ttu-id="ca480-187">**UIA \_ ориентатионпропертид**</span><span class="sxs-lookup"><span data-stu-id="ca480-187">**UIA\_OrientationPropertyId**</span></span>](uiauto-automation-element-propids.md)                   | <span data-ttu-id="ca480-188">Зависит</span><span class="sxs-lookup"><span data-stu-id="ca480-188">Depends</span></span>       | <span data-ttu-id="ca480-189">Значение, указывающее ориентацию элемента управления: по горизонтали или по вертикали.</span><span class="sxs-lookup"><span data-stu-id="ca480-189">A value indicating the control's orientation: horizontal or vertical.</span></span>                                                                                                                                               |



 

## <a name="required-control-patterns"></a><span data-ttu-id="ca480-190">Обязательные шаблоны элементов управления</span><span class="sxs-lookup"><span data-stu-id="ca480-190">Required Control Patterns</span></span>

<span data-ttu-id="ca480-191">В следующей таблице перечислены шаблоны элементов управления модели автоматизации пользовательского интерфейса, которые должны поддерживаться для элементов управления "строка состояния".</span><span class="sxs-lookup"><span data-stu-id="ca480-191">The following table lists the UI Automation control patterns required to be supported for status bar controls.</span></span> <span data-ttu-id="ca480-192">Дополнительные сведения о шаблонах элементов управления см. в разделе [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md).</span><span class="sxs-lookup"><span data-stu-id="ca480-192">For more information on control patterns, see [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md).</span></span>



| <span data-ttu-id="ca480-193">Шаблон элемента управления</span><span class="sxs-lookup"><span data-stu-id="ca480-193">Control Pattern</span></span>                               | <span data-ttu-id="ca480-194">Поддержка</span><span class="sxs-lookup"><span data-stu-id="ca480-194">Support</span></span>  | <span data-ttu-id="ca480-195">Примечания</span><span class="sxs-lookup"><span data-stu-id="ca480-195">Notes</span></span>                                                                                                                                                                        |
|-----------------------------------------------|----------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="ca480-196">**IGridProvider**</span><span class="sxs-lookup"><span data-stu-id="ca480-196">**IGridProvider**</span></span>](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-igridprovider) | <span data-ttu-id="ca480-197">Необязательно</span><span class="sxs-lookup"><span data-stu-id="ca480-197">Optional</span></span> | <span data-ttu-id="ca480-198">Элементы управления "строка состояния" должны поддерживать шаблон элемента управления [Grid](uiauto-implementinggrid.md) , чтобы отдельные элементы можно было отслеживать и легко ссылаться на них.</span><span class="sxs-lookup"><span data-stu-id="ca480-198">Status bar controls should support the [Grid](uiauto-implementinggrid.md) control pattern so that individual pieces can be monitored and easily referenced for information.</span></span> |



 

## <a name="required-events"></a><span data-ttu-id="ca480-199">Обязательные события</span><span class="sxs-lookup"><span data-stu-id="ca480-199">Required Events</span></span>

<span data-ttu-id="ca480-200">В следующей таблице перечислены события автоматизации пользовательского интерфейса, которые должны поддерживаться элементами управления "строка состояния".</span><span class="sxs-lookup"><span data-stu-id="ca480-200">The following table lists the UI Automation events that status bar controls are required to support.</span></span> <span data-ttu-id="ca480-201">Дополнительные сведения о событиях см. в разделе [UI Automation Events Overview](uiauto-eventsoverview.md).</span><span class="sxs-lookup"><span data-stu-id="ca480-201">For more information on events, see [UI Automation Events Overview](uiauto-eventsoverview.md).</span></span>



| <span data-ttu-id="ca480-202">Событие автоматизации пользовательского интерфейса</span><span class="sxs-lookup"><span data-stu-id="ca480-202">UI Automation Event</span></span>                                                                                                                   | <span data-ttu-id="ca480-203">Примечания</span><span class="sxs-lookup"><span data-stu-id="ca480-203">Notes</span></span>                                                                             |
|---------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------|
| [<span data-ttu-id="ca480-204">**UIA \_ аутоматионфокусчанжедевентид**</span><span class="sxs-lookup"><span data-stu-id="ca480-204">**UIA\_AutomationFocusChangedEventId**</span></span>](uiauto-event-ids.md)                                      |                                                                                   |
| <span data-ttu-id="ca480-205">[**UIA \_**](uiauto-automation-element-propids.md) Событие изменения свойства баундингректанглепропертид.</span><span class="sxs-lookup"><span data-stu-id="ca480-205">[**UIA\_BoundingRectanglePropertyId**](uiauto-automation-element-propids.md) property-changed event.</span></span> |                                                                                   |
| <span data-ttu-id="ca480-206">[**UIA \_**](uiauto-automation-element-propids.md) Событие изменения свойства исенабледпропертид.</span><span class="sxs-lookup"><span data-stu-id="ca480-206">[**UIA\_IsEnabledPropertyId**](uiauto-automation-element-propids.md) property-changed event.</span></span>                 | <span data-ttu-id="ca480-207">Если элемент управления поддерживает свойство « **включено** », оно должно поддерживать это событие.</span><span class="sxs-lookup"><span data-stu-id="ca480-207">If the control supports the **IsEnabled** property, it must support this event.</span></span>   |
| <span data-ttu-id="ca480-208">[**UIA \_**](uiauto-automation-element-propids.md) Событие изменения свойства исоффскринпропертид.</span><span class="sxs-lookup"><span data-stu-id="ca480-208">[**UIA\_IsOffscreenPropertyId**](uiauto-automation-element-propids.md) property-changed event.</span></span>             | <span data-ttu-id="ca480-209">Если элемент управления поддерживает свойство **исоффскрин** , он должен поддерживать это событие.</span><span class="sxs-lookup"><span data-stu-id="ca480-209">If the control supports the **IsOffscreen** property, it must support this event.</span></span> |
| [<span data-ttu-id="ca480-210">**UIA \_ структуречанжедевентид**</span><span class="sxs-lookup"><span data-stu-id="ca480-210">**UIA\_StructureChangedEventId**</span></span>](uiauto-event-ids.md)                                                  |                                                                                   |



 

## <a name="remarks"></a><span data-ttu-id="ca480-211">Комментарии</span><span class="sxs-lookup"><span data-stu-id="ca480-211">Remarks</span></span>

<span data-ttu-id="ca480-212">Рекомендуется использовать элементы управления "Правка" в качестве дочерних элементов сетки в строке состояния.</span><span class="sxs-lookup"><span data-stu-id="ca480-212">We recommend that edit controls be used as child grid elements in a status bar.</span></span> <span data-ttu-id="ca480-213">Использование элементов управления "поле ввода" упрощает связывание назначения поля состояния с его значением с помощью свойства "имя элемента" и "значение".</span><span class="sxs-lookup"><span data-stu-id="ca480-213">Using edit controls makes it easier to associate the purpose of the status field with its value by using the element name and value property.</span></span> <span data-ttu-id="ca480-214">Поскольку элементы управления "текст" не должны поддерживать шаблон элемента управления **value** , они не должны использоваться как дочерние элементы сетки.</span><span class="sxs-lookup"><span data-stu-id="ca480-214">Because text controls should not support the **Value** control pattern, they should not be used as child grid elements.</span></span>

## <a name="related-topics"></a><span data-ttu-id="ca480-215">См. также</span><span class="sxs-lookup"><span data-stu-id="ca480-215">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="ca480-216">**Зрения**</span><span class="sxs-lookup"><span data-stu-id="ca480-216">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="ca480-217">Общие сведения о типах элементов управления автоматизации пользовательского интерфейса</span><span class="sxs-lookup"><span data-stu-id="ca480-217">UI Automation Control Types Overview</span></span>](uiauto-controltypesoverview.md)
</dt> <dt>

[<span data-ttu-id="ca480-218">Общие сведения о модели автоматизации пользовательского интерфейса</span><span class="sxs-lookup"><span data-stu-id="ca480-218">UI Automation Overview</span></span>](uiauto-uiautomationoverview.md)
</dt> </dl>

 

 




