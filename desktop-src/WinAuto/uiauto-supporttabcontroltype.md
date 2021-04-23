---
title: Тип элемента управления Tab
description: В этом разделе содержатся сведения о поддержке автоматизации пользовательского интерфейса Майкрософт для типа элемента управления Tab.
ms.assetid: 49e3f025-f49b-44b1-90ca-09f40dce8f2a
keywords:
- Модель автоматизации пользовательского интерфейса, поддержка типа элемента управления Tab
- Модель автоматизации пользовательского интерфейса, тип элемента управления Tab
- Модель автоматизации пользовательского интерфейса, древовидная структура для типа элемента управления Tab
- Модель автоматизации пользовательского интерфейса, свойства для типа элемента управления Tab
- Модель автоматизации пользовательского интерфейса, шаблоны элементов управления для типа элемента управления Tab
- Модель автоматизации пользовательского интерфейса, события для типа элемента управления Tab
- Древовидные структуры, тип элемента управления Tab
- свойства, тип элемента управления Tab
- шаблоны элементов управления, тип элемента управления Tab
- события, тип элемента управления Tab
- Поддержка типа элемента управления Tab
- тип TabControl
- типы элементов управления, древовидная структура для типа элемента управления Tab
- типы элементов управления, шаблоны элементов управления для типа элемента управления Tab
- типы элементов управления, поддержка Tab
- типы элементов управления, вкладка
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 769a03617830c33fce4a8f64c594010b2120785b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103986604"
---
# <a name="tab-control-type"></a><span data-ttu-id="4a88f-119">Тип элемента управления Tab</span><span class="sxs-lookup"><span data-stu-id="4a88f-119">Tab Control Type</span></span>

<span data-ttu-id="4a88f-120">В этом разделе содержатся сведения о поддержке автоматизации пользовательского интерфейса Майкрософт для типа элемента управления **Tab** .</span><span class="sxs-lookup"><span data-stu-id="4a88f-120">This topic provides information about Microsoft UI Automation support for the **Tab** control type.</span></span>

<span data-ttu-id="4a88f-121">Элемент управления "Вкладка" является аналогом разделителей в записной книжке или меток в картотеке.</span><span class="sxs-lookup"><span data-stu-id="4a88f-121">A tab control is analogous to the dividers in a notebook or the labels in a file cabinet.</span></span> <span data-ttu-id="4a88f-122">С помощью элемента управления "Вкладка" приложение может определить несколько страниц для одной области окна или диалогового окна.</span><span class="sxs-lookup"><span data-stu-id="4a88f-122">By using a tab control, an application can define multiple pages for the same area of a window or dialog box.</span></span>

<span data-ttu-id="4a88f-123">В следующих разделах определяется необходимая древовидная структура модели автоматизации пользовательского интерфейса, свойства, шаблоны элементов управления и события для типа элемента управления **Tab** .</span><span class="sxs-lookup"><span data-stu-id="4a88f-123">The following sections define the required UI Automation tree structure, properties, control patterns, and events for the **Tab** control type.</span></span> <span data-ttu-id="4a88f-124">Требования к автоматизации пользовательского интерфейса применяются ко всем элементам управления "Вкладка", в которых платформа или платформа пользовательского интерфейса интегрирует поддержку модели автоматизации пользовательского интерфейса для типов элементов управления и шаблонов элементов управления.</span><span class="sxs-lookup"><span data-stu-id="4a88f-124">The UI Automation requirements apply to all tab controls where the UI framework/platform integrates UI Automation support for control types and control patterns.</span></span>

<span data-ttu-id="4a88f-125">В этом разделе содержатся следующие подразделы.</span><span class="sxs-lookup"><span data-stu-id="4a88f-125">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="4a88f-126">Типичная древовидная структура</span><span class="sxs-lookup"><span data-stu-id="4a88f-126">Typical Tree Structure</span></span>](#typical-tree-structure)
-   [<span data-ttu-id="4a88f-127">Соответствующие свойства</span><span class="sxs-lookup"><span data-stu-id="4a88f-127">Relevant Properties</span></span>](#relevant-properties)
-   [<span data-ttu-id="4a88f-128">Обязательные шаблоны элементов управления</span><span class="sxs-lookup"><span data-stu-id="4a88f-128">Required Control Patterns</span></span>](#required-control-patterns)
-   [<span data-ttu-id="4a88f-129">Обязательные события</span><span class="sxs-lookup"><span data-stu-id="4a88f-129">Required Events</span></span>](#required-events)
-   [<span data-ttu-id="4a88f-130">См. также</span><span class="sxs-lookup"><span data-stu-id="4a88f-130">Related topics</span></span>](#related-topics)

## <a name="typical-tree-structure"></a><span data-ttu-id="4a88f-131">Типичная древовидная структура</span><span class="sxs-lookup"><span data-stu-id="4a88f-131">Typical Tree Structure</span></span>

<span data-ttu-id="4a88f-132">В следующей таблице описывается типичный элемент управления и представление содержимого дерева модели автоматизации пользовательского интерфейса, которое относится к элементам управления "Вкладка" и описывает, что может содержаться в каждом представлении.</span><span class="sxs-lookup"><span data-stu-id="4a88f-132">The following table depicts a typical control and content view of the UI Automation tree that pertains to tab controls and describes what can be contained in each view.</span></span> <span data-ttu-id="4a88f-133">Дополнительные сведения о дереве автоматизации пользовательского интерфейса см. в разделе [Общие сведения о дереве модели автоматизации пользовательского интерфейса](uiauto-treeoverview.md).</span><span class="sxs-lookup"><span data-stu-id="4a88f-133">For more information about the UI Automation tree, see [UI Automation Tree Overview](uiauto-treeoverview.md).</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="4a88f-134">Представление элемента управления</span><span class="sxs-lookup"><span data-stu-id="4a88f-134">Control View</span></span></th>
<th><span data-ttu-id="4a88f-135">Представление содержимого</span><span class="sxs-lookup"><span data-stu-id="4a88f-135">Content View</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><ul>
<li><span data-ttu-id="4a88f-136">Вкладка</span><span class="sxs-lookup"><span data-stu-id="4a88f-136">Tab</span></span>
<ul>
<li><span data-ttu-id="4a88f-137">TabItem (1 или более)</span><span class="sxs-lookup"><span data-stu-id="4a88f-137">TabItem (1 or more)</span></span></li>
<li><span data-ttu-id="4a88f-138">ScrollBar (0 или 1)</span><span class="sxs-lookup"><span data-stu-id="4a88f-138">ScrollBar (0 or 1)</span></span>
<ul>
<li><span data-ttu-id="4a88f-139">Button (0 или 2)</span><span class="sxs-lookup"><span data-stu-id="4a88f-139">Button (0 or 2)</span></span></li>
</ul></li>
</ul></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="4a88f-140">Вкладка</span><span class="sxs-lookup"><span data-stu-id="4a88f-140">Tab</span></span>
<ul>
<li><span data-ttu-id="4a88f-141">TabItem (1 или более)</span><span class="sxs-lookup"><span data-stu-id="4a88f-141">TabItem (1 or more)</span></span></li>
</ul></li>
</ul></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="4a88f-142">Элементы управления "Вкладка" имеют дочерние элементы автоматизации пользовательского интерфейса, основанные на типе элемента управления [TabItem](uiauto-supporttabitemcontroltype.md) .</span><span class="sxs-lookup"><span data-stu-id="4a88f-142">Tab controls have child UI Automation elements based on the [TabItem](uiauto-supporttabitemcontroltype.md) control type.</span></span> <span data-ttu-id="4a88f-143">При группировании элементов вкладки (например, как в Microsoft Office приложениях) тип элемента управления **Tab** может также размещать типы элементов управления **группы** для элементов сгруппированной вкладки, как показано в следующей древовидной структуре.</span><span class="sxs-lookup"><span data-stu-id="4a88f-143">When tab items are grouped (for example, as in Microsoft Office applications) the **Tab** control type can also host **Groups** control types for the grouped tab items, as the following tree structure shows.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="4a88f-144">Представление элемента управления</span><span class="sxs-lookup"><span data-stu-id="4a88f-144">Control View</span></span></th>
<th><span data-ttu-id="4a88f-145">Представление содержимого</span><span class="sxs-lookup"><span data-stu-id="4a88f-145">Content View</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><ul>
<li><span data-ttu-id="4a88f-146">Вкладка</span><span class="sxs-lookup"><span data-stu-id="4a88f-146">Tab</span></span>
<ul>
<li><span data-ttu-id="4a88f-147">TabItem (1 или более)</span><span class="sxs-lookup"><span data-stu-id="4a88f-147">TabItem (1 or more)</span></span></li>
<li><span data-ttu-id="4a88f-148">Group (0 или более)</span><span class="sxs-lookup"><span data-stu-id="4a88f-148">Group (0 or more)</span></span>
<ul>
<li><span data-ttu-id="4a88f-149">TabItem (0 или более)</span><span class="sxs-lookup"><span data-stu-id="4a88f-149">TabItem (0 or more)</span></span></li>
</ul></li>
<li><span data-ttu-id="4a88f-150">ScrollBar (0 или 1)</span><span class="sxs-lookup"><span data-stu-id="4a88f-150">ScrollBar (0 or 1)</span></span>
<ul>
<li><span data-ttu-id="4a88f-151">Button (0 или 2)</span><span class="sxs-lookup"><span data-stu-id="4a88f-151">Button (0 or 2)</span></span></li>
</ul></li>
</ul></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="4a88f-152">Вкладка</span><span class="sxs-lookup"><span data-stu-id="4a88f-152">Tab</span></span>
<ul>
<li><span data-ttu-id="4a88f-153">TabItem (1 или более)</span><span class="sxs-lookup"><span data-stu-id="4a88f-153">TabItem (1 or more)</span></span></li>
<li><span data-ttu-id="4a88f-154">Group (0 или более)</span><span class="sxs-lookup"><span data-stu-id="4a88f-154">Group (0 or more)</span></span>
<ul>
<li><span data-ttu-id="4a88f-155">TabItem (0 или более)</span><span class="sxs-lookup"><span data-stu-id="4a88f-155">TabItem (0 or more)</span></span></li>
</ul></li>
</ul></li>
</ul></td>
</tr>
</tbody>
</table>



 

## <a name="relevant-properties"></a><span data-ttu-id="4a88f-156">Соответствующие свойства</span><span class="sxs-lookup"><span data-stu-id="4a88f-156">Relevant Properties</span></span>

<span data-ttu-id="4a88f-157">В следующей таблице перечислены свойства модели автоматизации пользовательского интерфейса, значения или определения которых особенно важны для элементов управления "Вкладка".</span><span class="sxs-lookup"><span data-stu-id="4a88f-157">The following table lists the UI Automation properties whose value or definition is especially relevant to tab controls.</span></span> <span data-ttu-id="4a88f-158">Дополнительные сведения о свойствах модели автоматизации пользовательского интерфейса см. в разделе [Получение свойств элементов модели автоматизации пользовательского интерфейса](uiauto-propertiesforclients.md).</span><span class="sxs-lookup"><span data-stu-id="4a88f-158">For more information about UI Automation properties, see [Retrieving Properties from UI Automation Elements](uiauto-propertiesforclients.md).</span></span>



| <span data-ttu-id="4a88f-159">Свойство модели автоматизации пользовательского интерфейса</span><span class="sxs-lookup"><span data-stu-id="4a88f-159">UI Automation Property</span></span>                                                                                              | <span data-ttu-id="4a88f-160">Значение</span><span class="sxs-lookup"><span data-stu-id="4a88f-160">Value</span></span>      | <span data-ttu-id="4a88f-161">Примечания</span><span class="sxs-lookup"><span data-stu-id="4a88f-161">Notes</span></span>                                                                                                                                                                                                                                                                                                                                                                         |
|---------------------------------------------------------------------------------------------------------------------|------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="4a88f-162">**UIA \_ аутоматионидпропертид**</span><span class="sxs-lookup"><span data-stu-id="4a88f-162">**UIA\_AutomationIdPropertyId**</span></span>](uiauto-automation-element-propids.md)                 | <span data-ttu-id="4a88f-163">См. примечания.</span><span class="sxs-lookup"><span data-stu-id="4a88f-163">See notes.</span></span> | <span data-ttu-id="4a88f-164">Значение этого свойства должно быть уникальным среди всех одноранговых элементов в необработанном представлении дерева модели автоматизации пользовательского интерфейса.</span><span class="sxs-lookup"><span data-stu-id="4a88f-164">The value of this property must be unique among all peer elements in the raw view of the UI Automation tree.</span></span>                                                                                                                                                                                                                                                                  |
| [<span data-ttu-id="4a88f-165">**UIA \_ баундингректанглепропертид**</span><span class="sxs-lookup"><span data-stu-id="4a88f-165">**UIA\_BoundingRectanglePropertyId**</span></span>](uiauto-automation-element-propids.md)       | <span data-ttu-id="4a88f-166">См. примечания.</span><span class="sxs-lookup"><span data-stu-id="4a88f-166">See notes.</span></span> | <span data-ttu-id="4a88f-167">Внешний прямоугольник, содержащий весь элемент управления.</span><span class="sxs-lookup"><span data-stu-id="4a88f-167">The outermost rectangle that contains the whole control.</span></span>                                                                                                                                                                                                                                                                                                                      |
| [<span data-ttu-id="4a88f-168">**UIA \_ кликкаблепоинтпропертид**</span><span class="sxs-lookup"><span data-stu-id="4a88f-168">**UIA\_ClickablePointPropertyId**</span></span>](uiauto-automation-element-propids.md)             | <span data-ttu-id="4a88f-169">Нет</span><span class="sxs-lookup"><span data-stu-id="4a88f-169">No</span></span>         | <span data-ttu-id="4a88f-170">Элемент управления "Вкладка" не имеет точек, подуправляющих щелчками.</span><span class="sxs-lookup"><span data-stu-id="4a88f-170">The tab control does not have clickable points.</span></span>                                                                                                                                                                                                                                                                                                                               |
| [<span data-ttu-id="4a88f-171">**UIA \_ контролтипепропертид**</span><span class="sxs-lookup"><span data-stu-id="4a88f-171">**UIA\_ControlTypePropertyId**</span></span>](uiauto-automation-element-propids.md)                   | <span data-ttu-id="4a88f-172">**TAB**</span><span class="sxs-lookup"><span data-stu-id="4a88f-172">**Tab**</span></span>    |                                                                                                                                                                                                                                                                                                                                                                               |
| [<span data-ttu-id="4a88f-173">**UIA \_ исконтентелементпропертид**</span><span class="sxs-lookup"><span data-stu-id="4a88f-173">**UIA\_IsContentElementPropertyId**</span></span>](uiauto-automation-element-propids.md)         | <span data-ttu-id="4a88f-174">true</span><span class="sxs-lookup"><span data-stu-id="4a88f-174">TRUE</span></span>       | <span data-ttu-id="4a88f-175">Элемент управления "Вкладка" всегда включается в представление содержимого дерева модели автоматизации пользовательского интерфейса.</span><span class="sxs-lookup"><span data-stu-id="4a88f-175">The tab control is always included in the content view of the UI Automation tree.</span></span>                                                                                                                                                                                                                                                                                             |
| [<span data-ttu-id="4a88f-176">**UIA \_ исконтролелементпропертид**</span><span class="sxs-lookup"><span data-stu-id="4a88f-176">**UIA\_IsControlElementPropertyId**</span></span>](uiauto-automation-element-propids.md)         | <span data-ttu-id="4a88f-177">true</span><span class="sxs-lookup"><span data-stu-id="4a88f-177">TRUE</span></span>       | <span data-ttu-id="4a88f-178">Элемент управления "Вкладка" всегда включается в представление элемента управления дерева модели автоматизации пользовательского интерфейса.</span><span class="sxs-lookup"><span data-stu-id="4a88f-178">The tab control is always included in the control view of the UI Automation tree.</span></span>                                                                                                                                                                                                                                                                                             |
| [<span data-ttu-id="4a88f-179">**UIA \_ искэйбоардфокусаблепропертид**</span><span class="sxs-lookup"><span data-stu-id="4a88f-179">**UIA\_IsKeyboardFocusablePropertyId**</span></span>](uiauto-automation-element-propids.md)   | <span data-ttu-id="4a88f-180">true</span><span class="sxs-lookup"><span data-stu-id="4a88f-180">TRUE</span></span>       | <span data-ttu-id="4a88f-181">Тип элемента управления Tab должен иметь возможность получать фокус клавиатуры.</span><span class="sxs-lookup"><span data-stu-id="4a88f-181">The Tab control type must be able to receive keyboard focus.</span></span> <span data-ttu-id="4a88f-182">Как правило, клиент автоматизации пользовательского интерфейса вызывает [**иуиаутоматионелемент:: SetFocus**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-setfocus) на элементе управления Tab, и один из его элементов перемещает фокус клавиатуры на элемент управления Tab.</span><span class="sxs-lookup"><span data-stu-id="4a88f-182">Typically, a UI Automation client calls [**IUIAutomationElement::SetFocus**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-setfocus) on a tab control and one of its items will forward the keyboard focus to the tab control.</span></span> <span data-ttu-id="4a88f-183">Некоторые контейнеры вкладок могут получать фокус без установки фокуса в одном из их элементов.</span><span class="sxs-lookup"><span data-stu-id="4a88f-183">It is possible for some tab containers to take focus without setting focus to one of its items.</span></span> |
| [<span data-ttu-id="4a88f-184">**UIA \_ лабеледбипропертид**</span><span class="sxs-lookup"><span data-stu-id="4a88f-184">**UIA\_LabeledByPropertyId**</span></span>](uiauto-automation-element-propids.md)                       | <span data-ttu-id="4a88f-185">См. примечания.</span><span class="sxs-lookup"><span data-stu-id="4a88f-185">See notes.</span></span> | <span data-ttu-id="4a88f-186">Элементы управления "Вкладка" обычно имеют метку со статическим текстом, на который ссылается это свойство.</span><span class="sxs-lookup"><span data-stu-id="4a88f-186">Tab controls typically have a static text label that is exposed through this property.</span></span>                                                                                                                                                                                                                                                                                        |
| [<span data-ttu-id="4a88f-187">**UIA \_ локализедконтролтипепропертид**</span><span class="sxs-lookup"><span data-stu-id="4a88f-187">**UIA\_LocalizedControlTypePropertyId**</span></span>](uiauto-automation-element-propids.md) | <span data-ttu-id="4a88f-188">См. примечания.</span><span class="sxs-lookup"><span data-stu-id="4a88f-188">See notes.</span></span> | <span data-ttu-id="4a88f-189">Локализованная строка, соответствующая типу элемента управления **Tab** .</span><span class="sxs-lookup"><span data-stu-id="4a88f-189">Localized string corresponding to the **Tab** control type.</span></span> <span data-ttu-id="4a88f-190">Значение по умолчанию — "Tab" для en-US или English (США).</span><span class="sxs-lookup"><span data-stu-id="4a88f-190">The default value is "tab" for en-US or English (United States).</span></span>                                                                                                                                                                                                                                                  |
| [<span data-ttu-id="4a88f-191">**UIA \_ намепропертид**</span><span class="sxs-lookup"><span data-stu-id="4a88f-191">**UIA\_NamePropertyId**</span></span>](uiauto-automation-element-propids.md)                                 | <span data-ttu-id="4a88f-192">См. примечания.</span><span class="sxs-lookup"><span data-stu-id="4a88f-192">See notes.</span></span> | <span data-ttu-id="4a88f-193">Элементу управления "Вкладка" редко требуется свойство **Name** .</span><span class="sxs-lookup"><span data-stu-id="4a88f-193">The tab control rarely requires a **Name** property.</span></span>                                                                                                                                                                                                                                                                                                                          |
| [<span data-ttu-id="4a88f-194">**UIA \_ ориентатионпропертид**</span><span class="sxs-lookup"><span data-stu-id="4a88f-194">**UIA\_OrientationPropertyId**</span></span>](uiauto-automation-element-propids.md)                   | <span data-ttu-id="4a88f-195">См. примечания.</span><span class="sxs-lookup"><span data-stu-id="4a88f-195">See notes.</span></span> | <span data-ttu-id="4a88f-196">Элемент управления "Вкладка" должен всегда указывать, располагается ли он горизонтально или вертикально.</span><span class="sxs-lookup"><span data-stu-id="4a88f-196">The tab control must always indicate whether it is positioned horizontally or vertically.</span></span>                                                                                                                                                                                                                                                                                     |



 

## <a name="required-control-patterns"></a><span data-ttu-id="4a88f-197">Обязательные шаблоны элементов управления</span><span class="sxs-lookup"><span data-stu-id="4a88f-197">Required Control Patterns</span></span>

<span data-ttu-id="4a88f-198">В следующей таблице перечислены шаблоны элементов управления модели автоматизации пользовательского интерфейса, которые должны поддерживаться всеми элементами управления "Вкладка".</span><span class="sxs-lookup"><span data-stu-id="4a88f-198">The following table lists the UI Automation control patterns required to be supported by all tab controls.</span></span> <span data-ttu-id="4a88f-199">Дополнительные сведения о шаблонах элементов управления см. в разделе [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md).</span><span class="sxs-lookup"><span data-stu-id="4a88f-199">For more information on control patterns, see [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md).</span></span>



| <span data-ttu-id="4a88f-200">Шаблон элемента управления/свойство шаблона</span><span class="sxs-lookup"><span data-stu-id="4a88f-200">Control Pattern/Pattern Property</span></span>                                             | <span data-ttu-id="4a88f-201">Поддержка/значение</span><span class="sxs-lookup"><span data-stu-id="4a88f-201">Support/Value</span></span> | <span data-ttu-id="4a88f-202">Примечания</span><span class="sxs-lookup"><span data-stu-id="4a88f-202">Notes</span></span>                                                                                                                                                                  |
|------------------------------------------------------------------------------|---------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="4a88f-203">**ISelectionProvider**</span><span class="sxs-lookup"><span data-stu-id="4a88f-203">**ISelectionProvider**</span></span>](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iselectionprovider)                      | <span data-ttu-id="4a88f-204">Обязательно</span><span class="sxs-lookup"><span data-stu-id="4a88f-204">Required</span></span>      | <span data-ttu-id="4a88f-205">Все элементы управления "Вкладка" должны поддерживать шаблон элемента управления [Selection](uiauto-implementingselection.md) .</span><span class="sxs-lookup"><span data-stu-id="4a88f-205">All tab controls must support the [Selection](uiauto-implementingselection.md) control pattern.</span></span>                                                                       |
| [<span data-ttu-id="4a88f-206">**исселектионрекуиред**</span><span class="sxs-lookup"><span data-stu-id="4a88f-206">**IsSelectionRequired**</span></span>](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iselectionprovider-get_isselectionrequired) | <span data-ttu-id="4a88f-207">true</span><span class="sxs-lookup"><span data-stu-id="4a88f-207">TRUE</span></span>          | <span data-ttu-id="4a88f-208">Элементы управления "Вкладка" всегда требуют, чтобы был сделан выбор.</span><span class="sxs-lookup"><span data-stu-id="4a88f-208">Tab controls always require that a selection be made.</span></span>                                                                                                                  |
| [<span data-ttu-id="4a88f-209">**канселектмултипле**</span><span class="sxs-lookup"><span data-stu-id="4a88f-209">**CanSelectMultiple**</span></span>](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iselectionprovider-get_canselectmultiple)     | <span data-ttu-id="4a88f-210">FALSE</span><span class="sxs-lookup"><span data-stu-id="4a88f-210">FALSE</span></span>         | <span data-ttu-id="4a88f-211">Элементы управления "Вкладка" всегда являются контейнерами с возможностью выбора одного варианта.</span><span class="sxs-lookup"><span data-stu-id="4a88f-211">Tab controls are always single-selection containers.</span></span>                                                                                                                   |
| [<span data-ttu-id="4a88f-212">**IScrollProvider**</span><span class="sxs-lookup"><span data-stu-id="4a88f-212">**IScrollProvider**</span></span>](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iscrollprovider)                            | <span data-ttu-id="4a88f-213">Зависит</span><span class="sxs-lookup"><span data-stu-id="4a88f-213">Depends</span></span>       | <span data-ttu-id="4a88f-214">Шаблон элемента управления [Scroll](uiauto-implementingscroll.md) должен поддерживаться, если элемент управления "Вкладка" содержит мини-приложения, позволяющие выполнять прокрутку набора элементов вкладки.</span><span class="sxs-lookup"><span data-stu-id="4a88f-214">The [Scroll](uiauto-implementingscroll.md) control pattern must be supported if the tab control has widgets that allow for a set of tab items to be scrolled through.</span></span> |



 

## <a name="required-events"></a><span data-ttu-id="4a88f-215">Обязательные события</span><span class="sxs-lookup"><span data-stu-id="4a88f-215">Required Events</span></span>

<span data-ttu-id="4a88f-216">В следующей таблице перечислены события автоматизации пользовательского интерфейса, которые должны поддерживаться элементами управления "Вкладка".</span><span class="sxs-lookup"><span data-stu-id="4a88f-216">The following table lists the UI Automation events that tab controls are required to support.</span></span> <span data-ttu-id="4a88f-217">Дополнительные сведения о событиях см. в разделе [UI Automation Events Overview](uiauto-eventsoverview.md).</span><span class="sxs-lookup"><span data-stu-id="4a88f-217">For more information on events, see [UI Automation Events Overview](uiauto-eventsoverview.md).</span></span>



| <span data-ttu-id="4a88f-218">Событие автоматизации пользовательского интерфейса</span><span class="sxs-lookup"><span data-stu-id="4a88f-218">UI Automation Event</span></span>                                                                                                                                        | <span data-ttu-id="4a88f-219">Примечания</span><span class="sxs-lookup"><span data-stu-id="4a88f-219">Notes</span></span>                                                                                                                      |
|------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="4a88f-220">**UIA \_ аутоматионфокусчанжедевентид**</span><span class="sxs-lookup"><span data-stu-id="4a88f-220">**UIA\_AutomationFocusChangedEventId**</span></span>](uiauto-event-ids.md)                                                           |                                                                                                                            |
| <span data-ttu-id="4a88f-221">[**UIA \_**](uiauto-automation-element-propids.md) Событие изменения свойства баундингректанглепропертид.</span><span class="sxs-lookup"><span data-stu-id="4a88f-221">[**UIA\_BoundingRectanglePropertyId**](uiauto-automation-element-propids.md) property-changed event.</span></span>                      |                                                                                                                            |
| <span data-ttu-id="4a88f-222">[**UIA \_**](uiauto-automation-element-propids.md) Событие изменения свойства исенабледпропертид.</span><span class="sxs-lookup"><span data-stu-id="4a88f-222">[**UIA\_IsEnabledPropertyId**](uiauto-automation-element-propids.md) property-changed event.</span></span>                                      | <span data-ttu-id="4a88f-223">Если элемент управления поддерживает свойство « [**включено**](uiauto-automation-element-propids.md) », оно должно поддерживать это событие.</span><span class="sxs-lookup"><span data-stu-id="4a88f-223">If the control supports the [**IsEnabled**](uiauto-automation-element-propids.md) property, it must support this event.</span></span>   |
| <span data-ttu-id="4a88f-224">[**UIA \_**](uiauto-automation-element-propids.md) Событие изменения свойства исоффскринпропертид.</span><span class="sxs-lookup"><span data-stu-id="4a88f-224">[**UIA\_IsOffscreenPropertyId**](uiauto-automation-element-propids.md) property-changed event.</span></span>                                  | <span data-ttu-id="4a88f-225">Если элемент управления поддерживает свойство [**исоффскрин**](uiauto-automation-element-propids.md) , он должен поддерживать это событие.</span><span class="sxs-lookup"><span data-stu-id="4a88f-225">If the control supports the [**IsOffscreen**](uiauto-automation-element-propids.md) property, it must support this event.</span></span> |
| <span data-ttu-id="4a88f-226">[**UIA \_**](uiauto-control-pattern-propids.md) Событие изменения свойства скроллхоризонталлискроллаблепропертид.</span><span class="sxs-lookup"><span data-stu-id="4a88f-226">[**UIA\_ScrollHorizontallyScrollablePropertyId**](uiauto-control-pattern-propids.md) property-changed event.</span></span>   | <span data-ttu-id="4a88f-227">Если элемент управления поддерживает шаблон элемента управления [Scroll](uiauto-implementingscroll.md) , он должен поддерживать это событие.</span><span class="sxs-lookup"><span data-stu-id="4a88f-227">If the control supports the [Scroll](uiauto-implementingscroll.md) control pattern, it must support this event.</span></span>           |
| <span data-ttu-id="4a88f-228">[**UIA \_**](uiauto-control-pattern-propids.md) Событие изменения свойства скроллхоризонталскроллперцентпропертид.</span><span class="sxs-lookup"><span data-stu-id="4a88f-228">[**UIA\_ScrollHorizontalScrollPercentPropertyId**](uiauto-control-pattern-propids.md) property-changed event.</span></span> | <span data-ttu-id="4a88f-229">Если элемент управления поддерживает шаблон элемента управления [Scroll](uiauto-implementingscroll.md) , он должен поддерживать это событие.</span><span class="sxs-lookup"><span data-stu-id="4a88f-229">If the control supports the [Scroll](uiauto-implementingscroll.md) control pattern, it must support this event.</span></span>           |
| <span data-ttu-id="4a88f-230">[**UIA \_**](uiauto-control-pattern-propids.md) Событие изменения свойства скроллхоризонталвиевсизепропертид.</span><span class="sxs-lookup"><span data-stu-id="4a88f-230">[**UIA\_ScrollHorizontalViewSizePropertyId**](uiauto-control-pattern-propids.md) property-changed event.</span></span>           | <span data-ttu-id="4a88f-231">Если элемент управления поддерживает шаблон элемента управления [Scroll](uiauto-implementingscroll.md) , он должен поддерживать это событие.</span><span class="sxs-lookup"><span data-stu-id="4a88f-231">If the control supports the [Scroll](uiauto-implementingscroll.md) control pattern, it must support this event.</span></span>           |
| <span data-ttu-id="4a88f-232">[**UIA \_**](uiauto-control-pattern-propids.md) Событие изменения свойства скроллвертикаллискроллаблепропертид.</span><span class="sxs-lookup"><span data-stu-id="4a88f-232">[**UIA\_ScrollVerticallyScrollablePropertyId**](uiauto-control-pattern-propids.md) property-changed event.</span></span>       | <span data-ttu-id="4a88f-233">Если элемент управления поддерживает шаблон элемента управления [Scroll](uiauto-implementingscroll.md) , он должен поддерживать это событие.</span><span class="sxs-lookup"><span data-stu-id="4a88f-233">If the control supports the [Scroll](uiauto-implementingscroll.md) control pattern, it must support this event.</span></span>           |
| <span data-ttu-id="4a88f-234">[**UIA \_**](uiauto-control-pattern-propids.md) Событие изменения свойства скроллвертикалскроллперцентпропертид.</span><span class="sxs-lookup"><span data-stu-id="4a88f-234">[**UIA\_ScrollVerticalScrollPercentPropertyId**](uiauto-control-pattern-propids.md) property-changed event.</span></span>     | <span data-ttu-id="4a88f-235">Если элемент управления поддерживает шаблон элемента управления [Scroll](uiauto-implementingscroll.md) , он должен поддерживать это событие.</span><span class="sxs-lookup"><span data-stu-id="4a88f-235">If the control supports the [Scroll](uiauto-implementingscroll.md) control pattern, it must support this event.</span></span>           |
| <span data-ttu-id="4a88f-236">[**UIA \_**](uiauto-control-pattern-propids.md) Событие изменения свойства скроллвертикалвиевсизепропертид.</span><span class="sxs-lookup"><span data-stu-id="4a88f-236">[**UIA\_ScrollVerticalViewSizePropertyId**](uiauto-control-pattern-propids.md) property-changed event.</span></span>               | <span data-ttu-id="4a88f-237">Если элемент управления поддерживает шаблон элемента управления [Scroll](uiauto-implementingscroll.md) , он должен поддерживать это событие.</span><span class="sxs-lookup"><span data-stu-id="4a88f-237">If the control supports the [Scroll](uiauto-implementingscroll.md) control pattern, it must support this event.</span></span>           |
| [<span data-ttu-id="4a88f-238">**UIA \_ структуречанжедевентид**</span><span class="sxs-lookup"><span data-stu-id="4a88f-238">**UIA\_StructureChangedEventId**</span></span>](uiauto-event-ids.md)                                                                       |                                                                                                                            |



 

## <a name="related-topics"></a><span data-ttu-id="4a88f-239">См. также</span><span class="sxs-lookup"><span data-stu-id="4a88f-239">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="4a88f-240">**Зрения**</span><span class="sxs-lookup"><span data-stu-id="4a88f-240">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="4a88f-241">Общие сведения о типах элементов управления автоматизации пользовательского интерфейса</span><span class="sxs-lookup"><span data-stu-id="4a88f-241">UI Automation Control Types Overview</span></span>](uiauto-controltypesoverview.md)
</dt> <dt>

[<span data-ttu-id="4a88f-242">Общие сведения о модели автоматизации пользовательского интерфейса</span><span class="sxs-lookup"><span data-stu-id="4a88f-242">UI Automation Overview</span></span>](uiauto-uiautomationoverview.md)
</dt> </dl>

 

 




