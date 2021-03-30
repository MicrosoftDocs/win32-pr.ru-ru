---
title: Тип элемента управления "Счетчик"
description: В этом разделе содержатся сведения о поддержке автоматизации пользовательского интерфейса Майкрософт для типа элемента управления "Счетчик".
ms.assetid: 28673ad5-645d-4314-96c4-81a951226256
keywords:
- Модель автоматизации пользовательского интерфейса, поддержка типа элемента управления "Счетчик"
- Модель автоматизации пользовательского интерфейса, тип элемента управления "Счетчик"
- Модель автоматизации пользовательского интерфейса, древовидная структура для типа элемента управления "Счетчик"
- Модель автоматизации пользовательского интерфейса, свойства для типа элемента управления "Счетчик"
- Модель автоматизации пользовательского интерфейса, шаблоны элементов управления для типа элемента управления "Счетчик"
- Модель автоматизации пользовательского интерфейса, события для типа элемента управления "Счетчик"
- Древовидные структуры, тип элемента управления "Счетчик"
- свойства, тип элемента управления "Счетчик"
- шаблоны элементов управления, тип элемента управления "Счетчик"
- события, тип элемента управления "Счетчик"
- Поддержка типа элемента управления "Счетчик"
- Spinner - тип элемента управления
- типы элементов управления, древовидная структура для типа элемента управления "Счетчик"
- типы элементов управления, шаблоны элементов управления для типа элемента управления "Счетчик"
- типы элементов управления, поддержка счетчика
- типы элементов управления, счетчик
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9681160bf82c9a541412bb6dde8958c603fcfe22
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103778236"
---
# <a name="spinner-control-type"></a><span data-ttu-id="d84fd-119">Тип элемента управления "Счетчик"</span><span class="sxs-lookup"><span data-stu-id="d84fd-119">Spinner Control Type</span></span>

<span data-ttu-id="d84fd-120">В этом разделе содержатся сведения о поддержке автоматизации пользовательского интерфейса Майкрософт для типа элемента управления " **Счетчик** ".</span><span class="sxs-lookup"><span data-stu-id="d84fd-120">This topic provides information about Microsoft UI Automation support for the **Spinner** control type.</span></span>

<span data-ttu-id="d84fd-121">Элементы управления "Счетчик" используются для выбора из домена элементов или диапазона чисел.</span><span class="sxs-lookup"><span data-stu-id="d84fd-121">Spinner controls are used to select from a domain of items or a range of numbers.</span></span>

<span data-ttu-id="d84fd-122">В следующих разделах определяется необходимая древовидная структура модели автоматизации пользовательского интерфейса, свойства, шаблоны элементов управления и события для типа элемента управления " **Счетчик** ".</span><span class="sxs-lookup"><span data-stu-id="d84fd-122">The following sections define the required UI Automation tree structure, properties, control patterns, and events for the **Spinner** control type.</span></span> <span data-ttu-id="d84fd-123">Требования к автоматизации пользовательского интерфейса применяются ко всем элементам управления "Счетчик", где платформа или платформа пользовательского интерфейса интегрирует поддержку автоматизации пользовательского интерфейса для типов элементов управления и шаблонов элементов управления.</span><span class="sxs-lookup"><span data-stu-id="d84fd-123">The UI Automation requirements apply to all spinner controls where the UI framework/platform integrates UI Automation support for control types and control patterns.</span></span>

<span data-ttu-id="d84fd-124">В этом разделе содержатся следующие подразделы.</span><span class="sxs-lookup"><span data-stu-id="d84fd-124">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="d84fd-125">Типичная древовидная структура</span><span class="sxs-lookup"><span data-stu-id="d84fd-125">Typical Tree Structure</span></span>](#typical-tree-structure)
-   [<span data-ttu-id="d84fd-126">Соответствующие свойства</span><span class="sxs-lookup"><span data-stu-id="d84fd-126">Relevant Properties</span></span>](#relevant-properties)
-   [<span data-ttu-id="d84fd-127">Обязательные шаблоны элементов управления</span><span class="sxs-lookup"><span data-stu-id="d84fd-127">Required Control Patterns</span></span>](#required-control-patterns)
-   [<span data-ttu-id="d84fd-128">Обязательные события</span><span class="sxs-lookup"><span data-stu-id="d84fd-128">Required Events</span></span>](#required-events)
-   [<span data-ttu-id="d84fd-129">См. также</span><span class="sxs-lookup"><span data-stu-id="d84fd-129">Related topics</span></span>](#related-topics)

## <a name="typical-tree-structure"></a><span data-ttu-id="d84fd-130">Типичная древовидная структура</span><span class="sxs-lookup"><span data-stu-id="d84fd-130">Typical Tree Structure</span></span>

<span data-ttu-id="d84fd-131">В следующей таблице описывается типичный элемент управления и представление содержимого дерева модели автоматизации пользовательского интерфейса, которое относится к элементам управления "Счетчик", когда они поддерживают шаблоны элементов управления **RangeValue** и **Selection** , и описывает, что может содержаться в каждом представлении.</span><span class="sxs-lookup"><span data-stu-id="d84fd-131">The following table depicts a typical control and content view of the UI Automation tree that pertain to spinner controls when they support the **RangeValue** and **Selection** control patterns and describes what can be contained in each view.</span></span> <span data-ttu-id="d84fd-132">Дополнительные сведения о дереве автоматизации пользовательского интерфейса см. в разделе [Общие сведения о дереве модели автоматизации пользовательского интерфейса](uiauto-treeoverview.md).</span><span class="sxs-lookup"><span data-stu-id="d84fd-132">For more information about the UI Automation tree, see [UI Automation Tree Overview](uiauto-treeoverview.md).</span></span>

<span data-ttu-id="d84fd-133">**Шаблон элемента управления RangeValue**</span><span class="sxs-lookup"><span data-stu-id="d84fd-133">**RangeValue control pattern**</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="d84fd-134">Представление элемента управления</span><span class="sxs-lookup"><span data-stu-id="d84fd-134">Control View</span></span></th>
<th><span data-ttu-id="d84fd-135">Представление содержимого</span><span class="sxs-lookup"><span data-stu-id="d84fd-135">Content View</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><ul>
<li><span data-ttu-id="d84fd-136">Spinner</span><span class="sxs-lookup"><span data-stu-id="d84fd-136">Spinner</span></span>
<ul>
<li><span data-ttu-id="d84fd-137">Edit (0 или 1)</span><span class="sxs-lookup"><span data-stu-id="d84fd-137">Edit (0 or 1)</span></span></li>
<li><span data-ttu-id="d84fd-138">Button (2)</span><span class="sxs-lookup"><span data-stu-id="d84fd-138">Button (2)</span></span></li>
</ul></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="d84fd-139">Spinner</span><span class="sxs-lookup"><span data-stu-id="d84fd-139">Spinner</span></span></li>
</ul></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="d84fd-140">**Selection - шаблон элемента управления**</span><span class="sxs-lookup"><span data-stu-id="d84fd-140">**Selection control pattern**</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="d84fd-141">Представление элемента управления</span><span class="sxs-lookup"><span data-stu-id="d84fd-141">Control View</span></span></th>
<th><span data-ttu-id="d84fd-142">Представление содержимого</span><span class="sxs-lookup"><span data-stu-id="d84fd-142">Content View</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><ul>
<li><span data-ttu-id="d84fd-143">Spinner</span><span class="sxs-lookup"><span data-stu-id="d84fd-143">Spinner</span></span>
<ul>
<li><span data-ttu-id="d84fd-144">Edit (0 или 1)</span><span class="sxs-lookup"><span data-stu-id="d84fd-144">Edit (0 or 1)</span></span></li>
<li><span data-ttu-id="d84fd-145">Button (2)</span><span class="sxs-lookup"><span data-stu-id="d84fd-145">Button (2)</span></span></li>
<li><span data-ttu-id="d84fd-146">ListItem (0 или более)</span><span class="sxs-lookup"><span data-stu-id="d84fd-146">List Item (0 or more)</span></span></li>
</ul></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="d84fd-147">Spinner</span><span class="sxs-lookup"><span data-stu-id="d84fd-147">Spinner</span></span>
<ul>
<li><span data-ttu-id="d84fd-148">ListItem (0 или более)</span><span class="sxs-lookup"><span data-stu-id="d84fd-148">ListItem (0 or more)</span></span></li>
</ul></li>
</ul></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="d84fd-149">Чтобы убедиться, что две кнопки в поддереве представления элемента управления могут быть различны средствами автоматизированных тестов, назначьте значение **скролламаунт \_ Смаллинкремент** или [**Скролламаунт \_ смаллдекремент**](/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-scrollamount) свойству **AutomationId** соответствующим образом.</span><span class="sxs-lookup"><span data-stu-id="d84fd-149">To ensure that the two buttons in the control view subtree can be distinguished by automated test tools, assign the **ScrollAmount\_SmallIncrement** or [**ScrollAmount\_SmallDecrement**](/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-scrollamount) value to the **AutomationId** property as appropriate.</span></span> <span data-ttu-id="d84fd-150">Для некоторых реализаций связанный элемент управления "поле ввода" может быть одноранговым элементом элемента управления "Счетчик".</span><span class="sxs-lookup"><span data-stu-id="d84fd-150">For some implementations, the associated edit control may be a peer of the spinner control.</span></span>

## <a name="relevant-properties"></a><span data-ttu-id="d84fd-151">Соответствующие свойства</span><span class="sxs-lookup"><span data-stu-id="d84fd-151">Relevant Properties</span></span>

<span data-ttu-id="d84fd-152">В следующей таблице перечислены свойства модели автоматизации пользовательского интерфейса, значение или определение которых особенно важно для элементов управления "Счетчик".</span><span class="sxs-lookup"><span data-stu-id="d84fd-152">The following table lists the UI Automation properties whose value or definition is especially relevant to spinner controls.</span></span> <span data-ttu-id="d84fd-153">Дополнительные сведения о свойствах модели автоматизации пользовательского интерфейса см. в разделе [Получение свойств элементов модели автоматизации пользовательского интерфейса](uiauto-propertiesforclients.md).</span><span class="sxs-lookup"><span data-stu-id="d84fd-153">For more information about UI Automation properties, see [Retrieving Properties from UI Automation Elements](uiauto-propertiesforclients.md).</span></span>



| <span data-ttu-id="d84fd-154">Свойство модели автоматизации пользовательского интерфейса</span><span class="sxs-lookup"><span data-stu-id="d84fd-154">UI Automation Property</span></span>                                                                                              | <span data-ttu-id="d84fd-155">Значение</span><span class="sxs-lookup"><span data-stu-id="d84fd-155">Value</span></span>       | <span data-ttu-id="d84fd-156">Примечания</span><span class="sxs-lookup"><span data-stu-id="d84fd-156">Notes</span></span>                                                                                                                                                                                                                                                                                                                      |
|---------------------------------------------------------------------------------------------------------------------|-------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="d84fd-157">**UIA \_ аутоматионидпропертид**</span><span class="sxs-lookup"><span data-stu-id="d84fd-157">**UIA\_AutomationIdPropertyId**</span></span>](uiauto-automation-element-propids.md)                 | <span data-ttu-id="d84fd-158">См. примечания.</span><span class="sxs-lookup"><span data-stu-id="d84fd-158">See notes.</span></span>  | <span data-ttu-id="d84fd-159">Значение этого свойства должно быть уникальным среди всех одноранговых элементов в необработанном представлении дерева модели автоматизации пользовательского интерфейса.</span><span class="sxs-lookup"><span data-stu-id="d84fd-159">The value of this property must be unique among all peer elements in the raw view of the UI Automation tree.</span></span>                                                                                                                                                                                                               |
| [<span data-ttu-id="d84fd-160">**UIA \_ баундингректанглепропертид**</span><span class="sxs-lookup"><span data-stu-id="d84fd-160">**UIA\_BoundingRectanglePropertyId**</span></span>](uiauto-automation-element-propids.md)       | <span data-ttu-id="d84fd-161">См. примечания.</span><span class="sxs-lookup"><span data-stu-id="d84fd-161">See notes.</span></span>  | <span data-ttu-id="d84fd-162">Внешний прямоугольник, содержащий весь элемент управления.</span><span class="sxs-lookup"><span data-stu-id="d84fd-162">The outermost rectangle that contains the whole control.</span></span>                                                                                                                                                                                                                                                                   |
| [<span data-ttu-id="d84fd-163">**UIA \_ кликкаблепоинтпропертид**</span><span class="sxs-lookup"><span data-stu-id="d84fd-163">**UIA\_ClickablePointPropertyId**</span></span>](uiauto-automation-element-propids.md)             | <span data-ttu-id="d84fd-164">См. примечания.</span><span class="sxs-lookup"><span data-stu-id="d84fd-164">See notes.</span></span>  | <span data-ttu-id="d84fd-165">Активная точка управления "Счетчик" перемещает фокус в область редактирования элемента управления.</span><span class="sxs-lookup"><span data-stu-id="d84fd-165">The spinner control's clickable point gives focus to the edit portion of the control.</span></span>                                                                                                                                                                                                                                      |
| [<span data-ttu-id="d84fd-166">**UIA \_ контролтипепропертид**</span><span class="sxs-lookup"><span data-stu-id="d84fd-166">**UIA\_ControlTypePropertyId**</span></span>](uiauto-automation-element-propids.md)                   | <span data-ttu-id="d84fd-167">**Spinner**</span><span class="sxs-lookup"><span data-stu-id="d84fd-167">**Spinner**</span></span> | <span data-ttu-id="d84fd-168">Это значение одинаково для всех инфраструктур.</span><span class="sxs-lookup"><span data-stu-id="d84fd-168">This value is the same for all frameworks.</span></span>                                                                                                                                                                                                                                                                                 |
| [<span data-ttu-id="d84fd-169">**UIA \_ исконтентелементпропертид**</span><span class="sxs-lookup"><span data-stu-id="d84fd-169">**UIA\_IsContentElementPropertyId**</span></span>](uiauto-automation-element-propids.md)         | <span data-ttu-id="d84fd-170">true</span><span class="sxs-lookup"><span data-stu-id="d84fd-170">TRUE</span></span>        | <span data-ttu-id="d84fd-171">Элемент управления "Счетчик" всегда должен быть содержимым.</span><span class="sxs-lookup"><span data-stu-id="d84fd-171">The spinner control must always be content.</span></span>                                                                                                                                                                                                                                                                                |
| [<span data-ttu-id="d84fd-172">**UIA \_ исконтролелементпропертид**</span><span class="sxs-lookup"><span data-stu-id="d84fd-172">**UIA\_IsControlElementPropertyId**</span></span>](uiauto-automation-element-propids.md)         | <span data-ttu-id="d84fd-173">true</span><span class="sxs-lookup"><span data-stu-id="d84fd-173">TRUE</span></span>        | <span data-ttu-id="d84fd-174">Элемент управления "Счетчик" всегда должен быть элементом управления.</span><span class="sxs-lookup"><span data-stu-id="d84fd-174">The spinner control must always be a control.</span></span>                                                                                                                                                                                                                                                                              |
| [<span data-ttu-id="d84fd-175">**UIA \_ искэйбоардфокусаблепропертид**</span><span class="sxs-lookup"><span data-stu-id="d84fd-175">**UIA\_IsKeyboardFocusablePropertyId**</span></span>](uiauto-automation-element-propids.md)   | <span data-ttu-id="d84fd-176">См. примечания.</span><span class="sxs-lookup"><span data-stu-id="d84fd-176">See notes.</span></span>  | <span data-ttu-id="d84fd-177">Если элемент управления может получать фокус клавиатуры, он должен поддерживать это свойство.</span><span class="sxs-lookup"><span data-stu-id="d84fd-177">If the control can receive keyboard focus, it must support this property.</span></span> <span data-ttu-id="d84fd-178">Элемент управления "Счетчик" редко принимает фокус, но когда он выполняется, фокус должен оставаться на самом элементе управления "Счетчик", а не на дочерних кнопках.</span><span class="sxs-lookup"><span data-stu-id="d84fd-178">A spinner control rarely takes the focus, but when it does, the focus should remain on the spinner control itself, not on the child buttons.</span></span> <span data-ttu-id="d84fd-179">Пользователь должен иметь возможность выполнять все действия прокрутки с помощью клавиш стрелка вверх и стрелка вниз.</span><span class="sxs-lookup"><span data-stu-id="d84fd-179">The user should be able to perform all scrolling actions by using the UP ARROW and DOWN ARROW keys.</span></span> |
| [<span data-ttu-id="d84fd-180">**UIA \_ лабеледбипропертид**</span><span class="sxs-lookup"><span data-stu-id="d84fd-180">**UIA\_LabeledByPropertyId**</span></span>](uiauto-automation-element-propids.md)                       | <span data-ttu-id="d84fd-181">См. примечания.</span><span class="sxs-lookup"><span data-stu-id="d84fd-181">See notes.</span></span>  | <span data-ttu-id="d84fd-182">Элементы управления "Счетчик" имеют метку со статическим текстом.</span><span class="sxs-lookup"><span data-stu-id="d84fd-182">Spinner controls have a static text label.</span></span>                                                                                                                                                                                                                                                                                 |
| [<span data-ttu-id="d84fd-183">**UIA \_ локализедконтролтипепропертид**</span><span class="sxs-lookup"><span data-stu-id="d84fd-183">**UIA\_LocalizedControlTypePropertyId**</span></span>](uiauto-automation-element-propids.md) | <span data-ttu-id="d84fd-184">См. примечания.</span><span class="sxs-lookup"><span data-stu-id="d84fd-184">See notes.</span></span>  | <span data-ttu-id="d84fd-185">Локализованная строка, соответствующая типу элемента управления " **Счетчик** ".</span><span class="sxs-lookup"><span data-stu-id="d84fd-185">Localized string corresponding to the **Spinner** control type.</span></span> <span data-ttu-id="d84fd-186">Значение по умолчанию — "Счетчик" для en-US или English (США).</span><span class="sxs-lookup"><span data-stu-id="d84fd-186">The default value is "spinner" for en-US or English (United States).</span></span>                                                                                                                                                                                       |
| [<span data-ttu-id="d84fd-187">**UIA \_ намепропертид**</span><span class="sxs-lookup"><span data-stu-id="d84fd-187">**UIA\_NamePropertyId**</span></span>](uiauto-automation-element-propids.md)                                 | <span data-ttu-id="d84fd-188">См. примечания.</span><span class="sxs-lookup"><span data-stu-id="d84fd-188">See notes.</span></span>  | <span data-ttu-id="d84fd-189">Обычно элемент управления "Счетчик" получает имя из статической текстовой метки.</span><span class="sxs-lookup"><span data-stu-id="d84fd-189">The spinner control typically gets its name from a static text label.</span></span>                                                                                                                                                                                                                                                      |



 

## <a name="required-control-patterns"></a><span data-ttu-id="d84fd-190">Обязательные шаблоны элементов управления</span><span class="sxs-lookup"><span data-stu-id="d84fd-190">Required Control Patterns</span></span>

<span data-ttu-id="d84fd-191">В следующей таблице перечислены шаблоны элементов управления модели автоматизации пользовательского интерфейса, которые должны поддерживаться всеми элементами управления "Счетчик".</span><span class="sxs-lookup"><span data-stu-id="d84fd-191">The following table lists the UI Automation control patterns required to be supported by all spinner controls.</span></span> <span data-ttu-id="d84fd-192">Дополнительные сведения о шаблонах элементов управления см. в разделе [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md).</span><span class="sxs-lookup"><span data-stu-id="d84fd-192">For more information on control patterns, see [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md).</span></span>



| <span data-ttu-id="d84fd-193">Шаблон элемента управления/свойство шаблона</span><span class="sxs-lookup"><span data-stu-id="d84fd-193">Control Pattern/Pattern Property</span></span>                                         | <span data-ttu-id="d84fd-194">Поддержка/значение</span><span class="sxs-lookup"><span data-stu-id="d84fd-194">Support/Value</span></span> | <span data-ttu-id="d84fd-195">Примечания</span><span class="sxs-lookup"><span data-stu-id="d84fd-195">Notes</span></span>                                                                                                                                     |
|--------------------------------------------------------------------------|---------------|-------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="d84fd-196">**IRangeValueProvider**</span><span class="sxs-lookup"><span data-stu-id="d84fd-196">**IRangeValueProvider**</span></span>](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irangevalueprovider)                | <span data-ttu-id="d84fd-197">Зависит</span><span class="sxs-lookup"><span data-stu-id="d84fd-197">Depends</span></span>       | <span data-ttu-id="d84fd-198">Элементы управления "Счетчик", охватывающие числовой диапазон, могут поддерживать шаблон элемента управления [RangeValue](uiauto-implementingrangevalue.md) .</span><span class="sxs-lookup"><span data-stu-id="d84fd-198">Spinner controls that span a numeric range can support the [RangeValue](uiauto-implementingrangevalue.md) control pattern.</span></span>               |
| [<span data-ttu-id="d84fd-199">**ISelectionProvider**</span><span class="sxs-lookup"><span data-stu-id="d84fd-199">**ISelectionProvider**</span></span>](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iselectionprovider)                  | <span data-ttu-id="d84fd-200">Зависит</span><span class="sxs-lookup"><span data-stu-id="d84fd-200">Depends</span></span>       | <span data-ttu-id="d84fd-201">Элементы управления "Счетчик", имеющие список выбираемых элементов, должны поддерживать шаблон элемента управления [Selection](uiauto-implementingselection.md) .</span><span class="sxs-lookup"><span data-stu-id="d84fd-201">Spinner controls that have a list of items to be selected must support the [Selection](uiauto-implementingselection.md) control pattern.</span></span> |
| [<span data-ttu-id="d84fd-202">**канселектмултипле**</span><span class="sxs-lookup"><span data-stu-id="d84fd-202">**CanSelectMultiple**</span></span>](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iselectionprovider-get_canselectmultiple) | <span data-ttu-id="d84fd-203">FALSE</span><span class="sxs-lookup"><span data-stu-id="d84fd-203">FALSE</span></span>         | <span data-ttu-id="d84fd-204">Элементы управления "Счетчик" всегда являются контейнерами с возможностью выбора одного варианта.</span><span class="sxs-lookup"><span data-stu-id="d84fd-204">Spinner controls are always single selection containers.</span></span>                                                                                  |
| [<span data-ttu-id="d84fd-205">**IValueProvider**</span><span class="sxs-lookup"><span data-stu-id="d84fd-205">**IValueProvider**</span></span>](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-ivalueprovider)                          | <span data-ttu-id="d84fd-206">Зависит</span><span class="sxs-lookup"><span data-stu-id="d84fd-206">Depends</span></span>       | <span data-ttu-id="d84fd-207">Элементы управления "Счетчик", охватывающие дескрете набор параметров или чисел, могут поддерживать шаблон элемента управления [value](uiauto-implementingvalue.md) .</span><span class="sxs-lookup"><span data-stu-id="d84fd-207">Spinner controls that span a descrete set of options or numbers can support the [Value](uiauto-implementingvalue.md) control pattern.</span></span>    |



 

## <a name="required-events"></a><span data-ttu-id="d84fd-208">Обязательные события</span><span class="sxs-lookup"><span data-stu-id="d84fd-208">Required Events</span></span>

<span data-ttu-id="d84fd-209">В следующей таблице перечислены события автоматизации пользовательского интерфейса, которые требуются для поддержки элементов управления типа "Счетчик".</span><span class="sxs-lookup"><span data-stu-id="d84fd-209">The following table lists the UI Automation events that spinner controls are required to support.</span></span> <span data-ttu-id="d84fd-210">Дополнительные сведения о событиях см. в разделе [UI Automation Events Overview](uiauto-eventsoverview.md).</span><span class="sxs-lookup"><span data-stu-id="d84fd-210">For more information on events, see [UI Automation Events Overview](uiauto-eventsoverview.md).</span></span>



| <span data-ttu-id="d84fd-211">Событие автоматизации пользовательского интерфейса</span><span class="sxs-lookup"><span data-stu-id="d84fd-211">UI Automation Event</span></span>                                                                                                                   | <span data-ttu-id="d84fd-212">Примечания</span><span class="sxs-lookup"><span data-stu-id="d84fd-212">Notes</span></span>                                                                                                                      |
|---------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="d84fd-213">**UIA \_ аутоматионфокусчанжедевентид**</span><span class="sxs-lookup"><span data-stu-id="d84fd-213">**UIA\_AutomationFocusChangedEventId**</span></span>](uiauto-event-ids.md)                                      |                                                                                                                            |
| <span data-ttu-id="d84fd-214">[**UIA \_**](uiauto-automation-element-propids.md) Событие изменения свойства баундингректанглепропертид.</span><span class="sxs-lookup"><span data-stu-id="d84fd-214">[**UIA\_BoundingRectanglePropertyId**](uiauto-automation-element-propids.md) property-changed event.</span></span> |                                                                                                                            |
| <span data-ttu-id="d84fd-215">[**UIA \_**](uiauto-automation-element-propids.md) Событие изменения свойства исенабледпропертид.</span><span class="sxs-lookup"><span data-stu-id="d84fd-215">[**UIA\_IsEnabledPropertyId**](uiauto-automation-element-propids.md) property-changed event.</span></span>                 | <span data-ttu-id="d84fd-216">Если элемент управления поддерживает свойство « [**включено**](uiauto-automation-element-propids.md) », оно должно поддерживать это событие.</span><span class="sxs-lookup"><span data-stu-id="d84fd-216">If the control supports the [**IsEnabled**](uiauto-automation-element-propids.md) property, it must support this event.</span></span>   |
| <span data-ttu-id="d84fd-217">[**UIA \_**](uiauto-automation-element-propids.md) Событие изменения свойства исоффскринпропертид.</span><span class="sxs-lookup"><span data-stu-id="d84fd-217">[**UIA\_IsOffscreenPropertyId**](uiauto-automation-element-propids.md) property-changed event.</span></span>             | <span data-ttu-id="d84fd-218">Если элемент управления поддерживает свойство [**исоффскрин**](uiauto-automation-element-propids.md) , он должен поддерживать это событие.</span><span class="sxs-lookup"><span data-stu-id="d84fd-218">If the control supports the [**IsOffscreen**](uiauto-automation-element-propids.md) property, it must support this event.</span></span> |
| <span data-ttu-id="d84fd-219">[**UIA \_**](uiauto-control-pattern-propids.md) Событие изменения свойства ранжевалуевалуепропертид.</span><span class="sxs-lookup"><span data-stu-id="d84fd-219">[**UIA\_RangeValueValuePropertyId**](uiauto-control-pattern-propids.md) property-changed event.</span></span>        | <span data-ttu-id="d84fd-220">Если элемент управления поддерживает шаблон элемента управления [RangeValue](uiauto-implementingrangevalue.md) , он должен поддерживать это событие.</span><span class="sxs-lookup"><span data-stu-id="d84fd-220">If the control supports the [RangeValue](uiauto-implementingrangevalue.md) control pattern, it must support this event.</span></span>   |
| <span data-ttu-id="d84fd-221">[**UIA \_ Выбрано событие изменения свойства \_ инвалидатедевентид выделения**](uiauto-event-ids.md) .</span><span class="sxs-lookup"><span data-stu-id="d84fd-221">[**UIA\_Selection\_InvalidatedEventId**](uiauto-event-ids.md) property-changed event.</span></span>               | <span data-ttu-id="d84fd-222">Если элемент управления поддерживает шаблон элемента управления [Selection](uiauto-implementingselection.md) , он должен поддерживать это событие.</span><span class="sxs-lookup"><span data-stu-id="d84fd-222">If the control supports the [Selection](uiauto-implementingselection.md) control pattern, it must support this event.</span></span>     |
| [<span data-ttu-id="d84fd-223">**UIA \_ структуречанжедевентид**</span><span class="sxs-lookup"><span data-stu-id="d84fd-223">**UIA\_StructureChangedEventId**</span></span>](uiauto-event-ids.md)                                                  |                                                                                                                            |
| <span data-ttu-id="d84fd-224">[**UIA \_**](uiauto-control-pattern-propids.md) Событие изменения свойства валуевалуепропертид.</span><span class="sxs-lookup"><span data-stu-id="d84fd-224">[**UIA\_ValueValuePropertyId**](uiauto-control-pattern-propids.md) property-changed event.</span></span>                  | <span data-ttu-id="d84fd-225">Если элемент управления поддерживает шаблон элемента управления [value](uiauto-implementingvalue.md) , он должен поддерживать это событие.</span><span class="sxs-lookup"><span data-stu-id="d84fd-225">If the control supports the [Value](uiauto-implementingvalue.md) control pattern, it must support this event.</span></span>             |



 

## <a name="related-topics"></a><span data-ttu-id="d84fd-226">См. также</span><span class="sxs-lookup"><span data-stu-id="d84fd-226">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="d84fd-227">**Зрения**</span><span class="sxs-lookup"><span data-stu-id="d84fd-227">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="d84fd-228">Общие сведения о типах элементов управления автоматизации пользовательского интерфейса</span><span class="sxs-lookup"><span data-stu-id="d84fd-228">UI Automation Control Types Overview</span></span>](uiauto-controltypesoverview.md)
</dt> <dt>

[<span data-ttu-id="d84fd-229">Общие сведения о модели автоматизации пользовательского интерфейса</span><span class="sxs-lookup"><span data-stu-id="d84fd-229">UI Automation Overview</span></span>](uiauto-uiautomationoverview.md)
</dt> </dl>

 

 




