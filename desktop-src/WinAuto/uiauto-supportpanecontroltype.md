---
title: Тип элемента управления панели
description: В этом разделе содержатся сведения о поддержке автоматизации пользовательского интерфейса Майкрософт для типа элемента управления Pane.
ms.assetid: 2a5d69dc-6880-4610-b481-4371637472ed
keywords:
- Модель автоматизации пользовательского интерфейса, поддержка типа элемента управления Pane
- Модель автоматизации пользовательского интерфейса, тип элемента управления Pane
- Модель автоматизации пользовательского интерфейса, древовидная структура для типа элемента управления Pane
- Модель автоматизации пользовательского интерфейса, свойства для типа элемента управления Pane
- Модель автоматизации пользовательского интерфейса, шаблоны элементов управления для типа элемента управления Pane
- Модель автоматизации пользовательского интерфейса, события для типа элемента управления Pane
- Древовидные структуры, тип элемента управления Pane
- свойства, тип элемента управления Pane
- шаблоны элементов управления, тип элемента управления Pane
- события, тип элемента управления Pane
- Поддержка типа элемента управления Pane
- Pane - тип элемента управления
- типы элементов управления, древовидная структура для типа элемента управления Pane
- типы элементов управления, шаблоны элементов управления для типа элемента управления Pane
- типы элементов управления, поддержка области
- типы элементов управления, область
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 51b7f22e6fb302ebb160a174c27c61119b8f09fe
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104566486"
---
# <a name="pane-control-type"></a><span data-ttu-id="3f452-119">Тип элемента управления панели</span><span class="sxs-lookup"><span data-stu-id="3f452-119">Pane Control Type</span></span>

<span data-ttu-id="3f452-120">В этом разделе содержатся сведения о поддержке автоматизации пользовательского интерфейса Майкрософт для типа элемента управления **Pane** .</span><span class="sxs-lookup"><span data-stu-id="3f452-120">This topic provides information about Microsoft UI Automation support for the **Pane** control type.</span></span>

<span data-ttu-id="3f452-121">Тип элемента управления " **панель** " предназначен для потенциально прокручиваемых областей, имеющих разнородное содержимое.</span><span class="sxs-lookup"><span data-stu-id="3f452-121">The **Pane** control type is for potentially scrollable regions that have disparate content.</span></span> <span data-ttu-id="3f452-122">Он используется для представления объекта внутри фрейма или окна документа.</span><span class="sxs-lookup"><span data-stu-id="3f452-122">It is used to represent an object within a frame or document window.</span></span> <span data-ttu-id="3f452-123">Пользователи могут перемещаться между элементами управления панели и содержимым текущей панели.</span><span class="sxs-lookup"><span data-stu-id="3f452-123">Users can navigate between pane controls and within the contents of the current pane.</span></span> <span data-ttu-id="3f452-124">Элементы управления "панель" представляют уровень группировки ниже окон или документов, но над отдельными элементами управления.</span><span class="sxs-lookup"><span data-stu-id="3f452-124">Pane controls represent a level of grouping lower than windows or documents, but above individual controls.</span></span> <span data-ttu-id="3f452-125">Пользователь переходит между панелями, нажимая клавишу TAB, F6 или CTRL+TAB, в зависимости от контекста.</span><span class="sxs-lookup"><span data-stu-id="3f452-125">The user navigates between panes by pressing TAB, F6, or CTRL+TAB, depending on the context.</span></span>

<span data-ttu-id="3f452-126">В следующих разделах определяется необходимая древовидная структура модели автоматизации пользовательского интерфейса, свойства, шаблоны элементов управления и события для типа элемента управления **Pane** .</span><span class="sxs-lookup"><span data-stu-id="3f452-126">The following sections define the required UI Automation tree structure, properties, control patterns, and events for the **Pane** control type.</span></span> <span data-ttu-id="3f452-127">Требования к автоматизации пользовательского интерфейса применяются ко всем элементам управления "панель", в которых платформа или платформа пользовательского интерфейса интегрирует поддержку автоматизации пользовательского интерфейса для типов элементов управления и шаблонов элементов управления.</span><span class="sxs-lookup"><span data-stu-id="3f452-127">The UI Automation requirements apply to all pane controls where the UI framework/platform integrates UI Automation support for control types and control patterns.</span></span>

<span data-ttu-id="3f452-128">В этом разделе содержатся следующие подразделы.</span><span class="sxs-lookup"><span data-stu-id="3f452-128">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="3f452-129">Типичная древовидная структура</span><span class="sxs-lookup"><span data-stu-id="3f452-129">Typical Tree Structure</span></span>](#typical-tree-structure)
-   [<span data-ttu-id="3f452-130">Соответствующие свойства</span><span class="sxs-lookup"><span data-stu-id="3f452-130">Relevant Properties</span></span>](#relevant-properties)
-   [<span data-ttu-id="3f452-131">Обязательные шаблоны элементов управления</span><span class="sxs-lookup"><span data-stu-id="3f452-131">Required Control Patterns</span></span>](#required-control-patterns)
-   [<span data-ttu-id="3f452-132">Обязательные события</span><span class="sxs-lookup"><span data-stu-id="3f452-132">Required Events</span></span>](#required-events)
-   [<span data-ttu-id="3f452-133">Пример типа элемента управления Pane</span><span class="sxs-lookup"><span data-stu-id="3f452-133">Pane Control Type Example</span></span>](#pane-control-type-example)
-   [<span data-ttu-id="3f452-134">См. также</span><span class="sxs-lookup"><span data-stu-id="3f452-134">Related topics</span></span>](#related-topics)

## <a name="typical-tree-structure"></a><span data-ttu-id="3f452-135">Типичная древовидная структура</span><span class="sxs-lookup"><span data-stu-id="3f452-135">Typical Tree Structure</span></span>

<span data-ttu-id="3f452-136">В следующей таблице описывается типичный элемент управления и представление содержимого дерева модели автоматизации пользовательского интерфейса, которое относится к элементам управления "панель" и описывает, что может содержаться в каждом представлении.</span><span class="sxs-lookup"><span data-stu-id="3f452-136">The following table depicts a typical control and content view of the UI Automation tree that pertains to pane controls and describes what can be contained in each view.</span></span> <span data-ttu-id="3f452-137">Дополнительные сведения о дереве автоматизации пользовательского интерфейса см. в разделе [Общие сведения о дереве модели автоматизации пользовательского интерфейса](uiauto-treeoverview.md).</span><span class="sxs-lookup"><span data-stu-id="3f452-137">For more information about the UI Automation tree, see [UI Automation Tree Overview](uiauto-treeoverview.md).</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="3f452-138">Представление элемента управления</span><span class="sxs-lookup"><span data-stu-id="3f452-138">Control View</span></span></th>
<th><span data-ttu-id="3f452-139">Представление содержимого</span><span class="sxs-lookup"><span data-stu-id="3f452-139">Content View</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><ul>
<li><span data-ttu-id="3f452-140">Панель</span><span class="sxs-lookup"><span data-stu-id="3f452-140">Pane</span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="3f452-141">Панель</span><span class="sxs-lookup"><span data-stu-id="3f452-141">Pane</span></span></li>
</ul></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="3f452-142">Элемент управления "панель" всегда отображается в представлениях элемента управления и содержимого.</span><span class="sxs-lookup"><span data-stu-id="3f452-142">A pane control always appears in the control and content views.</span></span> <span data-ttu-id="3f452-143">Не предоставляйте объект макета в виде области в представлении элемента управления или содержимого, если объект используется только для визуального представления.</span><span class="sxs-lookup"><span data-stu-id="3f452-143">Do not expose a layout object as a pane in either the control or content view if the object is used only for visual presentation.</span></span>

## <a name="relevant-properties"></a><span data-ttu-id="3f452-144">Соответствующие свойства</span><span class="sxs-lookup"><span data-stu-id="3f452-144">Relevant Properties</span></span>

<span data-ttu-id="3f452-145">В следующей таблице перечислены свойства модели автоматизации пользовательского интерфейса, значения или определения которых особенно актуальны для элементов управления "панель".</span><span class="sxs-lookup"><span data-stu-id="3f452-145">The following table lists the UI Automation properties whose value or definition is especially relevant to pane controls.</span></span> <span data-ttu-id="3f452-146">Дополнительные сведения о свойствах модели автоматизации пользовательского интерфейса см. в разделе [Получение свойств элементов модели автоматизации пользовательского интерфейса](uiauto-propertiesforclients.md).</span><span class="sxs-lookup"><span data-stu-id="3f452-146">For more information about UI Automation properties, see [Retrieving Properties from UI Automation Elements](uiauto-propertiesforclients.md).</span></span>



| <span data-ttu-id="3f452-147">Свойство модели автоматизации пользовательского интерфейса</span><span class="sxs-lookup"><span data-stu-id="3f452-147">UI Automation Property</span></span>                                                                                              | <span data-ttu-id="3f452-148">Значение</span><span class="sxs-lookup"><span data-stu-id="3f452-148">Value</span></span>      | <span data-ttu-id="3f452-149">Примечания</span><span class="sxs-lookup"><span data-stu-id="3f452-149">Notes</span></span>                                                                                                                                                                                                                                                                                                                 |
|---------------------------------------------------------------------------------------------------------------------|------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="3f452-150">**UIA \_ акцесскэйпропертид**</span><span class="sxs-lookup"><span data-stu-id="3f452-150">**UIA\_AccessKeyPropertyId**</span></span>](uiauto-automation-element-propids.md)                       | <span data-ttu-id="3f452-151">См. примечания.</span><span class="sxs-lookup"><span data-stu-id="3f452-151">See notes.</span></span> | <span data-ttu-id="3f452-152">Если определенное сочетание клавиш переводит фокус на область, эта информация должна предоставляться через это свойство.</span><span class="sxs-lookup"><span data-stu-id="3f452-152">If a specific key combination gives focus to the pane, that information should be exposed through this property.</span></span>                                                                                                                                                                                                      |
| [<span data-ttu-id="3f452-153">**UIA \_ аутоматионидпропертид**</span><span class="sxs-lookup"><span data-stu-id="3f452-153">**UIA\_AutomationIdPropertyId**</span></span>](uiauto-automation-element-propids.md)                 | <span data-ttu-id="3f452-154">См. примечания.</span><span class="sxs-lookup"><span data-stu-id="3f452-154">See notes.</span></span> | <span data-ttu-id="3f452-155">Значение этого свойства должно быть уникальным среди всех одноранговых элементов в необработанном представлении дерева модели автоматизации пользовательского интерфейса.</span><span class="sxs-lookup"><span data-stu-id="3f452-155">The value of this property must be unique among all peer elements in the raw view of the UI Automation tree.</span></span>                                                                                                                                                                                                          |
| [<span data-ttu-id="3f452-156">**UIA \_ баундингректанглепропертид**</span><span class="sxs-lookup"><span data-stu-id="3f452-156">**UIA\_BoundingRectanglePropertyId**</span></span>](uiauto-automation-element-propids.md)       | <span data-ttu-id="3f452-157">См. примечания.</span><span class="sxs-lookup"><span data-stu-id="3f452-157">See notes.</span></span> | <span data-ttu-id="3f452-158">Внешний прямоугольник, содержащий весь элемент управления.</span><span class="sxs-lookup"><span data-stu-id="3f452-158">The outermost rectangle that contains the whole control.</span></span>                                                                                                                                                                                                                                                              |
| [<span data-ttu-id="3f452-159">**UIA \_ кликкаблепоинтпропертид**</span><span class="sxs-lookup"><span data-stu-id="3f452-159">**UIA\_ClickablePointPropertyId**</span></span>](uiauto-automation-element-propids.md)             | <span data-ttu-id="3f452-160">См. примечания.</span><span class="sxs-lookup"><span data-stu-id="3f452-160">See notes.</span></span> | <span data-ttu-id="3f452-161">Это свойство предоставляет активную точку элемента управления "Панель", при щелчке в которой эта панель получает фокус.</span><span class="sxs-lookup"><span data-stu-id="3f452-161">This property exposes a clickable point of the pane control that causes the pane to become focused when it is clicked.</span></span>                                                                                                                                                                                                |
| [<span data-ttu-id="3f452-162">**UIA \_ контролтипепропертид**</span><span class="sxs-lookup"><span data-stu-id="3f452-162">**UIA\_ControlTypePropertyId**</span></span>](uiauto-automation-element-propids.md)                   | <span data-ttu-id="3f452-163">**Панель**</span><span class="sxs-lookup"><span data-stu-id="3f452-163">**Pane**</span></span>   |                                                                                                                                                                                                                                                                                                                       |
| [<span data-ttu-id="3f452-164">**UIA \_ хелптекстпропертид**</span><span class="sxs-lookup"><span data-stu-id="3f452-164">**UIA\_HelpTextPropertyId**</span></span>](uiauto-automation-element-propids.md)                         | <span data-ttu-id="3f452-165">См. примечания.</span><span class="sxs-lookup"><span data-stu-id="3f452-165">See notes.</span></span> | <span data-ttu-id="3f452-166">Текст справки для элементов управления "панель" должен объяснить назначение кадра и его связь с другими кадрами.</span><span class="sxs-lookup"><span data-stu-id="3f452-166">The help text for pane controls should explain the purpose of the frame and how it relates to other frames.</span></span> <span data-ttu-id="3f452-167">Описание необходимо, если назначение и связь между кадрами не ясно из значения свойства [**UIA \_ намепропертид**](uiauto-automation-element-propids.md) .</span><span class="sxs-lookup"><span data-stu-id="3f452-167">A description is necessary if the purpose and relationship of the frames is not clear from the value of the [**UIA\_NamePropertyId**](uiauto-automation-element-propids.md) property.</span></span> |
| [<span data-ttu-id="3f452-168">**UIA \_ исконтентелементпропертид**</span><span class="sxs-lookup"><span data-stu-id="3f452-168">**UIA\_IsContentElementPropertyId**</span></span>](uiauto-automation-element-propids.md)         | <span data-ttu-id="3f452-169">true</span><span class="sxs-lookup"><span data-stu-id="3f452-169">TRUE</span></span>       | <span data-ttu-id="3f452-170">Элемент управления "панель" всегда включается в представление содержимого дерева модели автоматизации пользовательского интерфейса.</span><span class="sxs-lookup"><span data-stu-id="3f452-170">The pane control is always included in the content view of the UI Automation tree.</span></span>                                                                                                                                                                                                                                    |
| [<span data-ttu-id="3f452-171">**UIA \_ исконтролелементпропертид**</span><span class="sxs-lookup"><span data-stu-id="3f452-171">**UIA\_IsControlElementPropertyId**</span></span>](uiauto-automation-element-propids.md)         | <span data-ttu-id="3f452-172">true</span><span class="sxs-lookup"><span data-stu-id="3f452-172">TRUE</span></span>       | <span data-ttu-id="3f452-173">Элемент управления "панель" всегда включается в представление элемента управления дерева модели автоматизации пользовательского интерфейса.</span><span class="sxs-lookup"><span data-stu-id="3f452-173">The pane control is always included in the control view of the UI Automation tree.</span></span>                                                                                                                                                                                                                                    |
| [<span data-ttu-id="3f452-174">**UIA \_ искэйбоардфокусаблепропертид**</span><span class="sxs-lookup"><span data-stu-id="3f452-174">**UIA\_IsKeyboardFocusablePropertyId**</span></span>](uiauto-automation-element-propids.md)   | <span data-ttu-id="3f452-175">См. примечания.</span><span class="sxs-lookup"><span data-stu-id="3f452-175">See notes.</span></span> | <span data-ttu-id="3f452-176">Если элемент управления может получать фокус клавиатуры, он должен поддерживать это свойство.</span><span class="sxs-lookup"><span data-stu-id="3f452-176">If the control can receive keyboard focus, it must support this property.</span></span>                                                                                                                                                                                                                                             |
| [<span data-ttu-id="3f452-177">**UIA \_ лабеледбипропертид**</span><span class="sxs-lookup"><span data-stu-id="3f452-177">**UIA\_LabeledByPropertyId**</span></span>](uiauto-automation-element-propids.md)                       | <span data-ttu-id="3f452-178">См. примечания.</span><span class="sxs-lookup"><span data-stu-id="3f452-178">See notes.</span></span> | <span data-ttu-id="3f452-179">Элементы управления "Панель" обычно не имеют статических меток.</span><span class="sxs-lookup"><span data-stu-id="3f452-179">Pane controls typically do not have a static label.</span></span> <span data-ttu-id="3f452-180">Если метка со статическим текстом присутствует, она должна предоставляться через это свойство.</span><span class="sxs-lookup"><span data-stu-id="3f452-180">If there is a static text label, it should be exposed through this property.</span></span>                                                                                                                                                                                      |
| [<span data-ttu-id="3f452-181">**UIA \_ локализедконтролтипепропертид**</span><span class="sxs-lookup"><span data-stu-id="3f452-181">**UIA\_LocalizedControlTypePropertyId**</span></span>](uiauto-automation-element-propids.md) | <span data-ttu-id="3f452-182">См. примечания.</span><span class="sxs-lookup"><span data-stu-id="3f452-182">See notes.</span></span> | <span data-ttu-id="3f452-183">Локализованная строка, соответствующая типу элемента управления **Pane** .</span><span class="sxs-lookup"><span data-stu-id="3f452-183">Localized string corresponding to the **Pane** control type.</span></span> <span data-ttu-id="3f452-184">Значение по умолчанию — "область" для en-US или English (США).</span><span class="sxs-lookup"><span data-stu-id="3f452-184">The default value is "pane" for en-US or English (United States).</span></span>                                                                                                                                                                                        |
| [<span data-ttu-id="3f452-185">**UIA \_ намепропертид**</span><span class="sxs-lookup"><span data-stu-id="3f452-185">**UIA\_NamePropertyId**</span></span>](uiauto-automation-element-propids.md)                                 | <span data-ttu-id="3f452-186">См. примечания.</span><span class="sxs-lookup"><span data-stu-id="3f452-186">See notes.</span></span> | <span data-ttu-id="3f452-187">Значение этого свойства всегда должно быть четким, кратким и понятным заголовком.</span><span class="sxs-lookup"><span data-stu-id="3f452-187">The value for this property must always be a clear, concise and meaningful title.</span></span>                                                                                                                                                                                                                                     |



 

## <a name="required-control-patterns"></a><span data-ttu-id="3f452-188">Обязательные шаблоны элементов управления</span><span class="sxs-lookup"><span data-stu-id="3f452-188">Required Control Patterns</span></span>

<span data-ttu-id="3f452-189">В следующей таблице перечислены шаблоны элементов управления модели автоматизации пользовательского интерфейса, которые должны поддерживаться элементами управления "панель".</span><span class="sxs-lookup"><span data-stu-id="3f452-189">The following table lists the UI Automation control patterns required to be supported by pane controls.</span></span> <span data-ttu-id="3f452-190">Дополнительные сведения о шаблонах элементов управления см. в разделе [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md).</span><span class="sxs-lookup"><span data-stu-id="3f452-190">For more information on control patterns, see [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md).</span></span>



| <span data-ttu-id="3f452-191">Шаблон элемента управления</span><span class="sxs-lookup"><span data-stu-id="3f452-191">Control Pattern</span></span>                                         | <span data-ttu-id="3f452-192">Поддержка</span><span class="sxs-lookup"><span data-stu-id="3f452-192">Support</span></span> | <span data-ttu-id="3f452-193">Примечания</span><span class="sxs-lookup"><span data-stu-id="3f452-193">Notes</span></span>                                                                                                                                                                                         |
|---------------------------------------------------------|---------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="3f452-194">**IDockProvider**</span><span class="sxs-lookup"><span data-stu-id="3f452-194">**IDockProvider**</span></span>](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-idockprovider)           | <span data-ttu-id="3f452-195">Зависит</span><span class="sxs-lookup"><span data-stu-id="3f452-195">Depends</span></span> | <span data-ttu-id="3f452-196">Реализуйте шаблон элемента управления [Dock](uiauto-implementingdock.md) , если элемент управления "панель" можно закрепить.</span><span class="sxs-lookup"><span data-stu-id="3f452-196">Implement the [Dock](uiauto-implementingdock.md) control pattern if the pane control can be docked.</span></span>                                                                                          |
| [<span data-ttu-id="3f452-197">**IScrollProvider**</span><span class="sxs-lookup"><span data-stu-id="3f452-197">**IScrollProvider**</span></span>](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iscrollprovider)       | <span data-ttu-id="3f452-198">Зависит</span><span class="sxs-lookup"><span data-stu-id="3f452-198">Depends</span></span> | <span data-ttu-id="3f452-199">Реализуйте шаблон элемента управления [Scroll](uiauto-implementingscroll.md) , если элемент управления "панель" можно прокручивать.</span><span class="sxs-lookup"><span data-stu-id="3f452-199">Implement the [Scroll](uiauto-implementingscroll.md) control pattern if the pane control can be scrolled.</span></span>                                                                                    |
| [<span data-ttu-id="3f452-200">**ITransformProvider**</span><span class="sxs-lookup"><span data-stu-id="3f452-200">**ITransformProvider**</span></span>](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itransformprovider) | <span data-ttu-id="3f452-201">Зависит</span><span class="sxs-lookup"><span data-stu-id="3f452-201">Depends</span></span> | <span data-ttu-id="3f452-202">Реализуйте шаблон элемента [Transform](uiauto-implementingtransform.md) , если элемент управления "панель" можно перемещать, изменять его размер или поворачивать на экране.</span><span class="sxs-lookup"><span data-stu-id="3f452-202">Implement the [Transform](uiauto-implementingtransform.md) control pattern if the pane control can be moved, resized, or rotated on the screen.</span></span>                                              |
| [<span data-ttu-id="3f452-203">**IWindowProvider**</span><span class="sxs-lookup"><span data-stu-id="3f452-203">**IWindowProvider**</span></span>](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iwindowprovider)       | <span data-ttu-id="3f452-204">Никогда</span><span class="sxs-lookup"><span data-stu-id="3f452-204">Never</span></span>   | <span data-ttu-id="3f452-205">Если элементу требуется реализовать шаблон элемента управления [Window](uiauto-implementingwindow.md) , элемент управления должен основываться на типе элемента управления [Window](uiauto-supportwindowcontroltype.md) .</span><span class="sxs-lookup"><span data-stu-id="3f452-205">If the element needs to implement the [Window](uiauto-implementingwindow.md) control pattern, the control should be based on the [Window](uiauto-supportwindowcontroltype.md) control type.</span></span> |



 

## <a name="required-events"></a><span data-ttu-id="3f452-206">Обязательные события</span><span class="sxs-lookup"><span data-stu-id="3f452-206">Required Events</span></span>

<span data-ttu-id="3f452-207">В следующей таблице перечислены события автоматизации пользовательского интерфейса, которые должны поддерживаться элементами управления "панель".</span><span class="sxs-lookup"><span data-stu-id="3f452-207">The following table lists the UI Automation events that pane controls are required to support.</span></span> <span data-ttu-id="3f452-208">Дополнительные сведения о событиях см. в разделе [UI Automation Events Overview](uiauto-eventsoverview.md).</span><span class="sxs-lookup"><span data-stu-id="3f452-208">For more information on events, see [UI Automation Events Overview](uiauto-eventsoverview.md).</span></span>



| <span data-ttu-id="3f452-209">Событие автоматизации пользовательского интерфейса</span><span class="sxs-lookup"><span data-stu-id="3f452-209">UI Automation Event</span></span>                                                                                                                                        | <span data-ttu-id="3f452-210">Примечания</span><span class="sxs-lookup"><span data-stu-id="3f452-210">Notes</span></span>                                                                                                                      |
|------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="3f452-211">**UIA \_ асинкконтентлоадедевентид**</span><span class="sxs-lookup"><span data-stu-id="3f452-211">**UIA\_AsyncContentLoadedEventId**</span></span>](uiauto-event-ids.md)                                                                   |                                                                                                                            |
| [<span data-ttu-id="3f452-212">**UIA \_ аутоматионфокусчанжедевентид**</span><span class="sxs-lookup"><span data-stu-id="3f452-212">**UIA\_AutomationFocusChangedEventId**</span></span>](uiauto-event-ids.md)                                                           |                                                                                                                            |
| <span data-ttu-id="3f452-213">[**UIA \_**](uiauto-automation-element-propids.md) Событие изменения свойства баундингректанглепропертид.</span><span class="sxs-lookup"><span data-stu-id="3f452-213">[**UIA\_BoundingRectanglePropertyId**](uiauto-automation-element-propids.md) property-changed event.</span></span>                      |                                                                                                                            |
| <span data-ttu-id="3f452-214">[**UIA \_**](uiauto-automation-element-propids.md) Событие изменения свойства исоффскринпропертид.</span><span class="sxs-lookup"><span data-stu-id="3f452-214">[**UIA\_IsOffscreenPropertyId**](uiauto-automation-element-propids.md) property-changed event.</span></span>                                  | <span data-ttu-id="3f452-215">Если элемент управления поддерживает свойство [**исоффскрин**](uiauto-automation-element-propids.md) , он должен поддерживать это событие.</span><span class="sxs-lookup"><span data-stu-id="3f452-215">If the control supports the [**IsOffscreen**](uiauto-automation-element-propids.md) property, it must support this event.</span></span> |
| <span data-ttu-id="3f452-216">[**UIA \_**](uiauto-control-pattern-propids.md) Событие изменения свойства скроллхоризонталлискроллаблепропертид.</span><span class="sxs-lookup"><span data-stu-id="3f452-216">[**UIA\_ScrollHorizontallyScrollablePropertyId**](uiauto-control-pattern-propids.md) property-changed event.</span></span>   | <span data-ttu-id="3f452-217">Если элемент управления поддерживает шаблон элемента управления [Scroll](uiauto-implementingscroll.md) , он должен поддерживать это событие.</span><span class="sxs-lookup"><span data-stu-id="3f452-217">If the control supports the [Scroll](uiauto-implementingscroll.md) control pattern, it must support this event.</span></span>           |
| <span data-ttu-id="3f452-218">[**UIA \_**](uiauto-control-pattern-propids.md) Событие изменения свойства скроллхоризонталскроллперцентпропертид.</span><span class="sxs-lookup"><span data-stu-id="3f452-218">[**UIA\_ScrollHorizontalScrollPercentPropertyId**](uiauto-control-pattern-propids.md) property-changed event.</span></span> | <span data-ttu-id="3f452-219">Если элемент управления поддерживает шаблон элемента управления [Scroll](uiauto-implementingscroll.md) , он должен поддерживать это событие.</span><span class="sxs-lookup"><span data-stu-id="3f452-219">If the control supports the [Scroll](uiauto-implementingscroll.md) control pattern, it must support this event.</span></span>           |
| <span data-ttu-id="3f452-220">[**UIA \_**](uiauto-control-pattern-propids.md) Событие изменения свойства скроллхоризонталвиевсизепропертид.</span><span class="sxs-lookup"><span data-stu-id="3f452-220">[**UIA\_ScrollHorizontalViewSizePropertyId**](uiauto-control-pattern-propids.md) property-changed event.</span></span>           | <span data-ttu-id="3f452-221">Если элемент управления поддерживает шаблон элемента управления [Scroll](uiauto-implementingscroll.md) , он должен поддерживать это событие.</span><span class="sxs-lookup"><span data-stu-id="3f452-221">If the control supports the [Scroll](uiauto-implementingscroll.md) control pattern, it must support this event.</span></span>           |
| <span data-ttu-id="3f452-222">[**UIA \_**](uiauto-control-pattern-propids.md) Событие изменения свойства скроллвертикаллискроллаблепропертид.</span><span class="sxs-lookup"><span data-stu-id="3f452-222">[**UIA\_ScrollVerticallyScrollablePropertyId**](uiauto-control-pattern-propids.md) property-changed event.</span></span>       | <span data-ttu-id="3f452-223">Если элемент управления поддерживает шаблон элемента управления [Scroll](uiauto-implementingscroll.md) , он должен поддерживать это событие.</span><span class="sxs-lookup"><span data-stu-id="3f452-223">If the control supports the [Scroll](uiauto-implementingscroll.md) control pattern, it must support this event.</span></span>           |
| <span data-ttu-id="3f452-224">[**UIA \_**](uiauto-control-pattern-propids.md) Событие изменения свойства скроллвертикалскроллперцентпропертид.</span><span class="sxs-lookup"><span data-stu-id="3f452-224">[**UIA\_ScrollVerticalScrollPercentPropertyId**](uiauto-control-pattern-propids.md) property-changed event.</span></span>     | <span data-ttu-id="3f452-225">Если элемент управления поддерживает шаблон элемента управления [Scroll](uiauto-implementingscroll.md) , он должен поддерживать это событие.</span><span class="sxs-lookup"><span data-stu-id="3f452-225">If the control supports the [Scroll](uiauto-implementingscroll.md) control pattern, it must support this event.</span></span>           |
| <span data-ttu-id="3f452-226">[**UIA \_**](uiauto-control-pattern-propids.md) Событие изменения свойства скроллвертикалвиевсизепропертид.</span><span class="sxs-lookup"><span data-stu-id="3f452-226">[**UIA\_ScrollVerticalViewSizePropertyId**](uiauto-control-pattern-propids.md) property-changed event.</span></span>               | <span data-ttu-id="3f452-227">Если элемент управления поддерживает шаблон элемента управления [Scroll](uiauto-implementingscroll.md) , он должен поддерживать это событие.</span><span class="sxs-lookup"><span data-stu-id="3f452-227">If the control supports the [Scroll](uiauto-implementingscroll.md) control pattern, it must support this event.</span></span>           |
| [<span data-ttu-id="3f452-228">**UIA \_ структуречанжедевентид**</span><span class="sxs-lookup"><span data-stu-id="3f452-228">**UIA\_StructureChangedEventId**</span></span>](uiauto-event-ids.md)                                                                       |                                                                                                                            |



 

## <a name="pane-control-type-example"></a><span data-ttu-id="3f452-229">Пример типа элемента управления Pane</span><span class="sxs-lookup"><span data-stu-id="3f452-229">Pane Control Type Example</span></span>

<span data-ttu-id="3f452-230">На следующем рисунке показан элемент управления, реализующий тип элемента управления **Pane** .</span><span class="sxs-lookup"><span data-stu-id="3f452-230">The following image illustrates a control that implements the **Pane** control type.</span></span>

![снимок экрана, демонстрирующий пример элемента управления "панель"](images/panexmpl.jpg)



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="3f452-232">Дерево модели автоматизации пользовательского интерфейса — представление элемента управления</span><span class="sxs-lookup"><span data-stu-id="3f452-232">UI Automation Tree—Control View</span></span></th>
<th><span data-ttu-id="3f452-233">Дерево модели автоматизации пользовательского интерфейса — представление содержимого</span><span class="sxs-lookup"><span data-stu-id="3f452-233">UI Automation Tree—Content View</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><ul>
<li><span data-ttu-id="3f452-234">Панель</span><span class="sxs-lookup"><span data-stu-id="3f452-234">Pane</span></span>
<ul>
<li><span data-ttu-id="3f452-235">Tree (шаблон Scroll)</span><span class="sxs-lookup"><span data-stu-id="3f452-235">Tree (Scroll Pattern)</span></span>
<ul>
<li><span data-ttu-id="3f452-236">TreeItem</span><span class="sxs-lookup"><span data-stu-id="3f452-236">TreeItem</span></span></li>
<li><span data-ttu-id="3f452-237">...</span><span class="sxs-lookup"><span data-stu-id="3f452-237">...</span></span></li>
</ul></li>
</ul></li>
<li><span data-ttu-id="3f452-238">Панель</span><span class="sxs-lookup"><span data-stu-id="3f452-238">Pane</span></span>
<ul>
<li><span data-ttu-id="3f452-239">Изменить (шаблон прокрутки)</span><span class="sxs-lookup"><span data-stu-id="3f452-239">Edit (Scroll Pattern)</span></span></li>
</ul></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="3f452-240">Панель</span><span class="sxs-lookup"><span data-stu-id="3f452-240">Pane</span></span>
<ul>
<li><span data-ttu-id="3f452-241">Tree (шаблон Scroll)</span><span class="sxs-lookup"><span data-stu-id="3f452-241">Tree (Scroll Pattern)</span></span>
<ul>
<li><span data-ttu-id="3f452-242">TreeItem</span><span class="sxs-lookup"><span data-stu-id="3f452-242">TreeItem</span></span></li>
<li><span data-ttu-id="3f452-243">...</span><span class="sxs-lookup"><span data-stu-id="3f452-243">...</span></span></li>
</ul></li>
<li><span data-ttu-id="3f452-244">Панель</span><span class="sxs-lookup"><span data-stu-id="3f452-244">Pane</span></span>
<ul>
<li><span data-ttu-id="3f452-245">Изменить (шаблон прокрутки)</span><span class="sxs-lookup"><span data-stu-id="3f452-245">Edit (Scroll Pattern)</span></span></li>
</ul></li>
</ul></li>
</ul></td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a><span data-ttu-id="3f452-246">См. также</span><span class="sxs-lookup"><span data-stu-id="3f452-246">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="3f452-247">**Зрения**</span><span class="sxs-lookup"><span data-stu-id="3f452-247">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="3f452-248">Общие сведения о типах элементов управления автоматизации пользовательского интерфейса</span><span class="sxs-lookup"><span data-stu-id="3f452-248">UI Automation Control Types Overview</span></span>](uiauto-controltypesoverview.md)
</dt> <dt>

[<span data-ttu-id="3f452-249">Общие сведения о модели автоматизации пользовательского интерфейса</span><span class="sxs-lookup"><span data-stu-id="3f452-249">UI Automation Overview</span></span>](uiauto-uiautomationoverview.md)
</dt> </dl>

 

 




