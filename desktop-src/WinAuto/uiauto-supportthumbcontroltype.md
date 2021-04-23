---
title: Тип элемента управления Thumb
description: В этом разделе содержатся сведения о поддержке автоматизации пользовательского интерфейса Майкрософт для типа элемента управления Thumb.
ms.assetid: 3b1d6802-cfd4-4b07-80a0-2950ca7f4e96
keywords:
- Модель автоматизации пользовательского интерфейса, поддержка типа элемента управления Thumb
- Модель автоматизации пользовательского интерфейса, тип элемента управления Thumb
- Модель автоматизации пользовательского интерфейса, древовидная структура для типа элемента управления Thumb
- Модель автоматизации пользовательского интерфейса, свойства для типа элемента управления Thumb
- Модель автоматизации пользовательского интерфейса, шаблоны элементов управления для типа элемента управления Thumb
- Модель автоматизации пользовательского интерфейса, события для типа элемента управления Thumb
- Древовидные структуры, тип элемента управления Thumb
- свойства, тип элемента управления Thumb
- шаблоны элементов управления, тип элемента управления Thumb
- события, тип элемента управления Thumb
- Поддержка типа элемента управления Thumb
- Thumb - тип элемента управления
- типы элементов управления, древовидная структура для типа элемента управления Thumb
- типы элементов управления, шаблоны элементов управления для типа элемента управления Thumb
- типы элементов управления, поддержка Thumb
- типы элементов управления, Thumb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8faf60fab30f54d3ed3e4b5a9f49628a3a35be5b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104411330"
---
# <a name="thumb-control-type"></a><span data-ttu-id="2f3bb-119">Тип элемента управления Thumb</span><span class="sxs-lookup"><span data-stu-id="2f3bb-119">Thumb Control Type</span></span>

<span data-ttu-id="2f3bb-120">В этом разделе содержатся сведения о поддержке автоматизации пользовательского интерфейса Майкрософт для типа элемента управления **Thumb** .</span><span class="sxs-lookup"><span data-stu-id="2f3bb-120">This topic provides information about Microsoft UI Automation support for the **Thumb** control type.</span></span>

<span data-ttu-id="2f3bb-121">Элементы управления "Бегунок" предоставляют функциональность, позволяющую перемещать (или перетаскивать) элемент управления, например кнопка полосы прокрутки, или изменять его размер, например мини-приложение для изменения размера окна.</span><span class="sxs-lookup"><span data-stu-id="2f3bb-121">Thumb controls provide the functionality that enables a control to be moved (or dragged), such as a scroll bar button, or resized, such as a window resizing widget.</span></span> <span data-ttu-id="2f3bb-122">Обратите внимание, что элемент управления Thumb не обеспечивает функцию перетаскивания.</span><span class="sxs-lookup"><span data-stu-id="2f3bb-122">Note that a thumb control does not provide drag-and-drop functionality.</span></span> <span data-ttu-id="2f3bb-123">Элементы управления "бегунок" могут получать фокус мыши, но не фокус клавиатуры.</span><span class="sxs-lookup"><span data-stu-id="2f3bb-123">Thumb controls can receive mouse focus but not keyboard focus.</span></span> <span data-ttu-id="2f3bb-124">Разработчик элемента управления должен реализовать его так, чтобы он действовал соответствующим образом (поддерживал перетаскивание или изменение размера).</span><span class="sxs-lookup"><span data-stu-id="2f3bb-124">The control developer must implement the control so that it acts appropriately (can be dragged or resized).</span></span>

<span data-ttu-id="2f3bb-125">В следующих разделах определяется необходимая древовидная структура модели автоматизации пользовательского интерфейса, свойства, шаблоны элементов управления и события для типа элемента управления **Thumb** .</span><span class="sxs-lookup"><span data-stu-id="2f3bb-125">The following sections define the required UI Automation tree structure, properties, control patterns, and events for the **Thumb** control type.</span></span> <span data-ttu-id="2f3bb-126">Требования к автоматизации пользовательского интерфейса применяют все элементы управления Thumb, в которых платформа или платформа пользовательского интерфейса интегрирует поддержку автоматизации пользовательского интерфейса для типов элементов управления и шаблонов элементов управления.</span><span class="sxs-lookup"><span data-stu-id="2f3bb-126">The UI Automation requirements apply all thumb controls where the UI framework/platform integrates UI Automation support for control types and control patterns.</span></span>

<span data-ttu-id="2f3bb-127">В этом разделе содержатся следующие подразделы.</span><span class="sxs-lookup"><span data-stu-id="2f3bb-127">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="2f3bb-128">Типичная древовидная структура</span><span class="sxs-lookup"><span data-stu-id="2f3bb-128">Typical Tree Structure</span></span>](#typical-tree-structure)
-   [<span data-ttu-id="2f3bb-129">Соответствующие свойства</span><span class="sxs-lookup"><span data-stu-id="2f3bb-129">Relevant Properties</span></span>](#relevant-properties)
-   [<span data-ttu-id="2f3bb-130">Обязательные шаблоны элементов управления</span><span class="sxs-lookup"><span data-stu-id="2f3bb-130">Required Control Patterns</span></span>](#required-control-patterns)
-   [<span data-ttu-id="2f3bb-131">Обязательные события</span><span class="sxs-lookup"><span data-stu-id="2f3bb-131">Required Events</span></span>](#required-events)
-   [<span data-ttu-id="2f3bb-132">См. также</span><span class="sxs-lookup"><span data-stu-id="2f3bb-132">Related topics</span></span>](#related-topics)

## <a name="typical-tree-structure"></a><span data-ttu-id="2f3bb-133">Типичная древовидная структура</span><span class="sxs-lookup"><span data-stu-id="2f3bb-133">Typical Tree Structure</span></span>

<span data-ttu-id="2f3bb-134">В следующей таблице описывается типичный элемент управления и представление содержимого дерева модели автоматизации пользовательского интерфейса, которое относится к элементам управления "бегунок" и описывает, что может содержаться в каждом представлении.</span><span class="sxs-lookup"><span data-stu-id="2f3bb-134">The following table depicts a typical control and content view of the UI Automation tree that pertains to thumb controls and describes what can be contained in each view.</span></span> <span data-ttu-id="2f3bb-135">Дополнительные сведения о дереве автоматизации пользовательского интерфейса см. в разделе [Общие сведения о дереве модели автоматизации пользовательского интерфейса](uiauto-treeoverview.md).</span><span class="sxs-lookup"><span data-stu-id="2f3bb-135">For more information about the UI Automation tree, see [UI Automation Tree Overview](uiauto-treeoverview.md).</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="2f3bb-136">Представление элемента управления</span><span class="sxs-lookup"><span data-stu-id="2f3bb-136">Control View</span></span></th>
<th><span data-ttu-id="2f3bb-137">Представление содержимого</span><span class="sxs-lookup"><span data-stu-id="2f3bb-137">Content View</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><ul>
<li><span data-ttu-id="2f3bb-138">Бегунок</span><span class="sxs-lookup"><span data-stu-id="2f3bb-138">Thumb</span></span></li>
</ul></td>
<td><span data-ttu-id="2f3bb-139">(Неприменимо)</span><span class="sxs-lookup"><span data-stu-id="2f3bb-139">(Not applicable)</span></span></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="2f3bb-140">Элементы управления "бегунок" никогда не отображаются в представлении содержимого, так как они существуют только для управления с помощью мыши.</span><span class="sxs-lookup"><span data-stu-id="2f3bb-140">Thumb controls never appear in the content view because they exist only to be manipulated with a mouse.</span></span> <span data-ttu-id="2f3bb-141">Они представляют собой другой шаблон элемента управления, например шаблон элемента управления [Scroll](uiauto-implementingscroll.md) , шаблон элемента [Transform](uiauto-implementingtransform.md) или шаблон элемента управления [RangeValue](uiauto-implementingrangevalue.md) , который поддерживается в контейнере элемента управления Thumb.</span><span class="sxs-lookup"><span data-stu-id="2f3bb-141">They are exposed though another control pattern, such as the [Scroll](uiauto-implementingscroll.md) control pattern, [Transform](uiauto-implementingtransform.md) control pattern, or [RangeValue](uiauto-implementingrangevalue.md) control pattern, being supported on the thumb control's container.</span></span>

## <a name="relevant-properties"></a><span data-ttu-id="2f3bb-142">Соответствующие свойства</span><span class="sxs-lookup"><span data-stu-id="2f3bb-142">Relevant Properties</span></span>

<span data-ttu-id="2f3bb-143">В следующей таблице перечислены свойства модели автоматизации пользовательского интерфейса, значения или определения которых особенно важны для элементов управления "бегунок".</span><span class="sxs-lookup"><span data-stu-id="2f3bb-143">The following table lists the UI Automation properties whose value or definition is especially relevant to thumb controls.</span></span> <span data-ttu-id="2f3bb-144">Дополнительные сведения о свойствах модели автоматизации пользовательского интерфейса см. в разделе [Получение свойств элементов модели автоматизации пользовательского интерфейса](uiauto-propertiesforclients.md).</span><span class="sxs-lookup"><span data-stu-id="2f3bb-144">For more information about UI Automation properties, see [Retrieving Properties from UI Automation Elements](uiauto-propertiesforclients.md).</span></span>



| <span data-ttu-id="2f3bb-145">Свойство модели автоматизации пользовательского интерфейса</span><span class="sxs-lookup"><span data-stu-id="2f3bb-145">UI Automation Property</span></span>                                                                                              | <span data-ttu-id="2f3bb-146">Значение</span><span class="sxs-lookup"><span data-stu-id="2f3bb-146">Value</span></span>      | <span data-ttu-id="2f3bb-147">Примечания</span><span class="sxs-lookup"><span data-stu-id="2f3bb-147">Notes</span></span>                                                                                                                                                                                                                                                        |
|---------------------------------------------------------------------------------------------------------------------|------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="2f3bb-148">**UIA \_ аутоматионидпропертид**</span><span class="sxs-lookup"><span data-stu-id="2f3bb-148">**UIA\_AutomationIdPropertyId**</span></span>](uiauto-automation-element-propids.md)                 | <span data-ttu-id="2f3bb-149">См. примечания.</span><span class="sxs-lookup"><span data-stu-id="2f3bb-149">See notes.</span></span> | <span data-ttu-id="2f3bb-150">Значение этого свойства должно быть уникальным среди всех одноранговых элементов в необработанном представлении дерева модели автоматизации пользовательского интерфейса.</span><span class="sxs-lookup"><span data-stu-id="2f3bb-150">The value of this property must be unique among all peer elements in the raw view of the UI Automation tree.</span></span>                                                                                                                                                 |
| [<span data-ttu-id="2f3bb-151">**UIA \_ баундингректанглепропертид**</span><span class="sxs-lookup"><span data-stu-id="2f3bb-151">**UIA\_BoundingRectanglePropertyId**</span></span>](uiauto-automation-element-propids.md)       | <span data-ttu-id="2f3bb-152">См. примечания.</span><span class="sxs-lookup"><span data-stu-id="2f3bb-152">See notes.</span></span> | <span data-ttu-id="2f3bb-153">Внешний прямоугольник, содержащий весь элемент управления.</span><span class="sxs-lookup"><span data-stu-id="2f3bb-153">The outermost rectangle that contains the whole control.</span></span>                                                                                                                                                                                                     |
| [<span data-ttu-id="2f3bb-154">**UIA \_ кликкаблепоинтпропертид**</span><span class="sxs-lookup"><span data-stu-id="2f3bb-154">**UIA\_ClickablePointPropertyId**</span></span>](uiauto-automation-element-propids.md)             | <span data-ttu-id="2f3bb-155">См. примечания.</span><span class="sxs-lookup"><span data-stu-id="2f3bb-155">See notes.</span></span> | <span data-ttu-id="2f3bb-156">Точка в видимой клиентской области элемента управления Thumb.</span><span class="sxs-lookup"><span data-stu-id="2f3bb-156">A point within the visible client area of the thumb control.</span></span>                                                                                                                                                                                                 |
| [<span data-ttu-id="2f3bb-157">**UIA \_ контролтипепропертид**</span><span class="sxs-lookup"><span data-stu-id="2f3bb-157">**UIA\_ControlTypePropertyId**</span></span>](uiauto-automation-element-propids.md)                   | <span data-ttu-id="2f3bb-158">**Типа**</span><span class="sxs-lookup"><span data-stu-id="2f3bb-158">**Thumb**</span></span>  |                                                                                                                                                                                                                                                              |
| [<span data-ttu-id="2f3bb-159">**UIA \_ исконтентелементпропертид**</span><span class="sxs-lookup"><span data-stu-id="2f3bb-159">**UIA\_IsContentElementPropertyId**</span></span>](uiauto-automation-element-propids.md)         | <span data-ttu-id="2f3bb-160">FALSE</span><span class="sxs-lookup"><span data-stu-id="2f3bb-160">FALSE</span></span>      | <span data-ttu-id="2f3bb-161">Элемент управления Thumb никогда не включается в представление содержимого дерева модели автоматизации пользовательского интерфейса.</span><span class="sxs-lookup"><span data-stu-id="2f3bb-161">The thumb control is never included in the content view of the UI Automation tree.</span></span>                                                                                                                                                                           |
| [<span data-ttu-id="2f3bb-162">**UIA \_ исконтролелементпропертид**</span><span class="sxs-lookup"><span data-stu-id="2f3bb-162">**UIA\_IsControlElementPropertyId**</span></span>](uiauto-automation-element-propids.md)         | <span data-ttu-id="2f3bb-163">true</span><span class="sxs-lookup"><span data-stu-id="2f3bb-163">TRUE</span></span>       | <span data-ttu-id="2f3bb-164">Элемент управления Thumb всегда включается в представление элемента управления дерева модели автоматизации пользовательского интерфейса.</span><span class="sxs-lookup"><span data-stu-id="2f3bb-164">The thumb control is always included in the control view of the UI Automation tree.</span></span>                                                                                                                                                                          |
| [<span data-ttu-id="2f3bb-165">**UIA \_ искэйбоардфокусаблепропертид**</span><span class="sxs-lookup"><span data-stu-id="2f3bb-165">**UIA\_IsKeyboardFocusablePropertyId**</span></span>](uiauto-automation-element-propids.md)   | <span data-ttu-id="2f3bb-166">См. примечания.</span><span class="sxs-lookup"><span data-stu-id="2f3bb-166">See notes.</span></span> | <span data-ttu-id="2f3bb-167">Если элемент управления может получать фокус клавиатуры, он должен поддерживать это свойство.</span><span class="sxs-lookup"><span data-stu-id="2f3bb-167">If the control can receive keyboard focus, it must support this property.</span></span> <span data-ttu-id="2f3bb-168">Элемент управления Thumb может получать фокус, если он используется как объект "захвата" для изменения размера окна или панели.</span><span class="sxs-lookup"><span data-stu-id="2f3bb-168">A thumb control can receive the focus if it is used as a "gripper" object for sizing a window or a pane.</span></span> <span data-ttu-id="2f3bb-169">Элемент управления Thumb в ползунке или полосе прокрутки не должен получать фокус.</span><span class="sxs-lookup"><span data-stu-id="2f3bb-169">A thumb control in a slider or scroll bar should never receive the focus.</span></span> |
| [<span data-ttu-id="2f3bb-170">**UIA \_ лабеледбипропертид**</span><span class="sxs-lookup"><span data-stu-id="2f3bb-170">**UIA\_LabeledByPropertyId**</span></span>](uiauto-automation-element-propids.md)                       | <span data-ttu-id="2f3bb-171">NULL</span><span class="sxs-lookup"><span data-stu-id="2f3bb-171">NULL</span></span>       | <span data-ttu-id="2f3bb-172">Бегунки никогда не имеют меток.</span><span class="sxs-lookup"><span data-stu-id="2f3bb-172">Thumb controls never have a label.</span></span>                                                                                                                                                                                                                           |
| [<span data-ttu-id="2f3bb-173">**UIA \_ локализедконтролтипепропертид**</span><span class="sxs-lookup"><span data-stu-id="2f3bb-173">**UIA\_LocalizedControlTypePropertyId**</span></span>](uiauto-automation-element-propids.md) | <span data-ttu-id="2f3bb-174">См. примечания.</span><span class="sxs-lookup"><span data-stu-id="2f3bb-174">See notes.</span></span> | <span data-ttu-id="2f3bb-175">Локализованная строка, соответствующая типу элемента управления **Thumb** .</span><span class="sxs-lookup"><span data-stu-id="2f3bb-175">Localized string corresponding to the **Thumb** control type.</span></span> <span data-ttu-id="2f3bb-176">Значение по умолчанию — "Thumb" для en-US или English (США).</span><span class="sxs-lookup"><span data-stu-id="2f3bb-176">The default value is "thumb" for en-US or English (United States).</span></span>                                                                                                                             |
| [<span data-ttu-id="2f3bb-177">**UIA \_ намепропертид**</span><span class="sxs-lookup"><span data-stu-id="2f3bb-177">**UIA\_NamePropertyId**</span></span>](uiauto-automation-element-propids.md)                                 | <span data-ttu-id="2f3bb-178">NULL</span><span class="sxs-lookup"><span data-stu-id="2f3bb-178">NULL</span></span>       | <span data-ttu-id="2f3bb-179">Так как элемент управления Thumb недоступен в представлении содержимого дерева модели автоматизации пользовательского интерфейса, имя не требуется.</span><span class="sxs-lookup"><span data-stu-id="2f3bb-179">Because the thumb control is not available in the content view of the UI Automation tree, it does not require a name.</span></span>                                                                                                                                        |



 

## <a name="required-control-patterns"></a><span data-ttu-id="2f3bb-180">Обязательные шаблоны элементов управления</span><span class="sxs-lookup"><span data-stu-id="2f3bb-180">Required Control Patterns</span></span>

<span data-ttu-id="2f3bb-181">В следующей таблице перечислены шаблоны элементов управления модели автоматизации пользовательского интерфейса, которые должны поддерживаться элементами управления "Thumb".</span><span class="sxs-lookup"><span data-stu-id="2f3bb-181">The following table lists the UI Automation control patterns required to be supported by thumb controls.</span></span> <span data-ttu-id="2f3bb-182">Дополнительные сведения о шаблонах элементов управления см. в разделе [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md).</span><span class="sxs-lookup"><span data-stu-id="2f3bb-182">For more information on control patterns, see [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md).</span></span>



| <span data-ttu-id="2f3bb-183">Шаблон элемента управления</span><span class="sxs-lookup"><span data-stu-id="2f3bb-183">Control Pattern</span></span>                                         | <span data-ttu-id="2f3bb-184">Поддержка</span><span class="sxs-lookup"><span data-stu-id="2f3bb-184">Support</span></span>  | <span data-ttu-id="2f3bb-185">Примечания</span><span class="sxs-lookup"><span data-stu-id="2f3bb-185">Notes</span></span>                                                                                                                                                                                                                                                                    |
|---------------------------------------------------------|----------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="2f3bb-186">**ITransformProvider**</span><span class="sxs-lookup"><span data-stu-id="2f3bb-186">**ITransformProvider**</span></span>](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itransformprovider) | <span data-ttu-id="2f3bb-187">Обязательно</span><span class="sxs-lookup"><span data-stu-id="2f3bb-187">Required</span></span> | <span data-ttu-id="2f3bb-188">Разрешает перемещение бегунка на экране.</span><span class="sxs-lookup"><span data-stu-id="2f3bb-188">Enables the thumb control to be moved on the screen.</span></span> <span data-ttu-id="2f3bb-189">Поскольку элемент управления Thumb обычно не может быть перемещен или изменен, шаблон элемента управления [Transform](uiauto-implementingtransform.md) в основном поддерживает функцию [**Move**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itransformprovider-move) .</span><span class="sxs-lookup"><span data-stu-id="2f3bb-189">Because the thumb control typically cannot be resized or rotated, the [Transform](uiauto-implementingtransform.md) control pattern primarily supports the [**Move**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itransformprovider-move) function.</span></span> |



 

## <a name="required-events"></a><span data-ttu-id="2f3bb-190">Обязательные события</span><span class="sxs-lookup"><span data-stu-id="2f3bb-190">Required Events</span></span>

<span data-ttu-id="2f3bb-191">В следующей таблице перечислены события автоматизации пользовательского интерфейса, которые должны поддерживаться элементами управления "Thumbs".</span><span class="sxs-lookup"><span data-stu-id="2f3bb-191">The following table lists the UI Automation events that thumb controls are required to support.</span></span> <span data-ttu-id="2f3bb-192">Дополнительные сведения о событиях см. в разделе [UI Automation Events Overview](uiauto-eventsoverview.md).</span><span class="sxs-lookup"><span data-stu-id="2f3bb-192">For more information on events, see [UI Automation Events Overview](uiauto-eventsoverview.md).</span></span>



| <span data-ttu-id="2f3bb-193">Событие автоматизации пользовательского интерфейса</span><span class="sxs-lookup"><span data-stu-id="2f3bb-193">UI Automation Event</span></span>                                                                                                                   | <span data-ttu-id="2f3bb-194">Примечания</span><span class="sxs-lookup"><span data-stu-id="2f3bb-194">Notes</span></span>                                                                                                                      |
|---------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="2f3bb-195">**UIA \_ аутоматионфокусчанжедевентид**</span><span class="sxs-lookup"><span data-stu-id="2f3bb-195">**UIA\_AutomationFocusChangedEventId**</span></span>](uiauto-event-ids.md)                                      |                                                                                                                            |
| <span data-ttu-id="2f3bb-196">[**UIA \_**](uiauto-automation-element-propids.md) Событие изменения свойства баундингректанглепропертид.</span><span class="sxs-lookup"><span data-stu-id="2f3bb-196">[**UIA\_BoundingRectanglePropertyId**](uiauto-automation-element-propids.md) property-changed event.</span></span> |                                                                                                                            |
| <span data-ttu-id="2f3bb-197">[**UIA \_**](uiauto-automation-element-propids.md) Событие изменения свойства исенабледпропертид.</span><span class="sxs-lookup"><span data-stu-id="2f3bb-197">[**UIA\_IsEnabledPropertyId**](uiauto-automation-element-propids.md) property-changed event.</span></span>                 | <span data-ttu-id="2f3bb-198">Если элемент управления поддерживает свойство « [**включено**](uiauto-automation-element-propids.md) », оно должно поддерживать это событие.</span><span class="sxs-lookup"><span data-stu-id="2f3bb-198">If the control supports the [**IsEnabled**](uiauto-automation-element-propids.md) property, it must support this event.</span></span>   |
| <span data-ttu-id="2f3bb-199">[**UIA \_**](uiauto-automation-element-propids.md) Событие изменения свойства исоффскринпропертид.</span><span class="sxs-lookup"><span data-stu-id="2f3bb-199">[**UIA\_IsOffscreenPropertyId**](uiauto-automation-element-propids.md) property-changed event.</span></span>             | <span data-ttu-id="2f3bb-200">Если элемент управления поддерживает свойство [**исоффскрин**](uiauto-automation-element-propids.md) , он должен поддерживать это событие.</span><span class="sxs-lookup"><span data-stu-id="2f3bb-200">If the control supports the [**IsOffscreen**](uiauto-automation-element-propids.md) property, it must support this event.</span></span> |
| [<span data-ttu-id="2f3bb-201">**UIA \_ структуречанжедевентид**</span><span class="sxs-lookup"><span data-stu-id="2f3bb-201">**UIA\_StructureChangedEventId**</span></span>](uiauto-event-ids.md)                                                  |                                                                                                                            |



 

## <a name="related-topics"></a><span data-ttu-id="2f3bb-202">См. также</span><span class="sxs-lookup"><span data-stu-id="2f3bb-202">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="2f3bb-203">**Зрения**</span><span class="sxs-lookup"><span data-stu-id="2f3bb-203">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="2f3bb-204">Общие сведения о типах элементов управления автоматизации пользовательского интерфейса</span><span class="sxs-lookup"><span data-stu-id="2f3bb-204">UI Automation Control Types Overview</span></span>](uiauto-controltypesoverview.md)
</dt> <dt>

[<span data-ttu-id="2f3bb-205">Общие сведения о модели автоматизации пользовательского интерфейса</span><span class="sxs-lookup"><span data-stu-id="2f3bb-205">UI Automation Overview</span></span>](uiauto-uiautomationoverview.md)
</dt> </dl>

 

 




