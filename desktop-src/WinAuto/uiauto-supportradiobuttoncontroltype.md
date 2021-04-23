---
title: Тип элемента управления RadioButton
description: В этом разделе содержатся сведения о поддержке автоматизации пользовательского интерфейса Майкрософт для типа элемента управления RadioButton.
ms.assetid: 6fc4a6a3-f5c0-402b-b9e7-870dfaa3370d
keywords:
- Модель автоматизации пользовательского интерфейса, поддержка типа элемента управления RadioButton
- Модель автоматизации пользовательского интерфейса, тип элемента управления RadioButton
- Модель автоматизации пользовательского интерфейса, древовидная структура для типа элемента управления RadioButton
- Модель автоматизации пользовательского интерфейса, свойства для типа элемента управления RadioButton
- Модель автоматизации пользовательского интерфейса, шаблоны элементов управления для типа элемента управления RadioButton
- Модель автоматизации пользовательского интерфейса, события для типа элемента управления RadioButton
- Древовидные структуры, тип элемента управления RadioButton
- свойства, тип элемента управления RadioButton
- шаблоны элементов управления, тип элемента управления RadioButton
- события, тип элемента управления RadioButton
- Поддержка типа элемента управления RadioButton
- RadioButton - тип элемента управления
- типы элементов управления, древовидная структура для типа элемента управления RadioButton
- типы элементов управления, шаблоны элементов управления для типа элемента управления RadioButton
- типы элементов управления, поддержка RadioButton
- типы элементов управления, RadioButton
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4702a2227a5164ff694378c82fa3b7cde33f9823
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103778239"
---
# <a name="radiobutton-control-type"></a><span data-ttu-id="bb8de-119">Тип элемента управления RadioButton</span><span class="sxs-lookup"><span data-stu-id="bb8de-119">RadioButton Control Type</span></span>

<span data-ttu-id="bb8de-120">В этом разделе содержатся сведения о поддержке автоматизации пользовательского интерфейса Майкрософт для типа элемента управления **RadioButton** .</span><span class="sxs-lookup"><span data-stu-id="bb8de-120">This topic provides information about Microsoft UI Automation support for the **RadioButton** control type.</span></span>

<span data-ttu-id="bb8de-121">Переключатель состоит из круглой кнопки и определяемого приложением текста (метки), значка или растрового изображения, указывающего выбор, который может сделать пользователь, нажав кнопку.</span><span class="sxs-lookup"><span data-stu-id="bb8de-121">A radio button consists of a round button and application-defined text (a label), an icon, or a bitmap that indicates a choice the user can make by selecting the button.</span></span> <span data-ttu-id="bb8de-122">Обычно в приложениях переключатели объединяются в группу, чтобы пользователь мог выбирать из набора связанных, но взаимоисключающих вариантов.</span><span class="sxs-lookup"><span data-stu-id="bb8de-122">An application typically uses radio buttons in a group box to permit the user to choose from a set of related, but mutually exclusive options.</span></span> <span data-ttu-id="bb8de-123">Например, приложение может представлять группу переключателей, из которых пользователь может выбрать вариант форматирования текста, выделенного в клиентской области текста.</span><span class="sxs-lookup"><span data-stu-id="bb8de-123">For example, the application might present a group of radio buttons from which the user can select a format preference for text selected in the client area.</span></span> <span data-ttu-id="bb8de-124">Пользователь может выбрать выравнивание по левому краю, по правому краю или по центру, выбрав соответствующий переключатель.</span><span class="sxs-lookup"><span data-stu-id="bb8de-124">The user could select a left-aligned, right-aligned, or centered format by selecting the corresponding radio button.</span></span> <span data-ttu-id="bb8de-125">Обычно пользователь может за один раз выбрать только один вариант в наборе переключателей.</span><span class="sxs-lookup"><span data-stu-id="bb8de-125">Typically, the user can select only one option at a time from a set of radio buttons.</span></span>

> [!Note]  
> <span data-ttu-id="bb8de-126">Другим обобщением элементов управления для кнопок, где может быть выбрано только одно в группе, является содержимое выключателя.</span><span class="sxs-lookup"><span data-stu-id="bb8de-126">Another control generalization for buttons where only one in a group can be selected is the content of a toggle button.</span></span> <span data-ttu-id="bb8de-127">Некоторые платформы пользовательского интерфейса рассматривайте переключатель как специализированный выключатель.</span><span class="sxs-lookup"><span data-stu-id="bb8de-127">Some UI frameworks consider a radio button to be a specialized toggle button.</span></span>

 

<span data-ttu-id="bb8de-128">В следующих разделах определяется необходимая древовидная структура модели автоматизации пользовательского интерфейса, свойства, шаблоны элементов управления и события для типа элемента управления **RadioButton** .</span><span class="sxs-lookup"><span data-stu-id="bb8de-128">The following sections define the required UI Automation tree structure, properties, control patterns, and events for the **RadioButton** control type.</span></span> <span data-ttu-id="bb8de-129">Требования к автоматизации пользовательского интерфейса применяются ко всем элементам управления "Кнопка", в которых платформа или платформа пользовательского интерфейса интегрирует поддержку модели автоматизации пользовательского интерфейса для типов элементов управления и шаблонов элементов управления.</span><span class="sxs-lookup"><span data-stu-id="bb8de-129">The UI Automation requirements apply to all button controls where the UI framework/platform integrates UI Automation support for control types and control patterns.</span></span>

<span data-ttu-id="bb8de-130">В этом разделе содержатся следующие подразделы.</span><span class="sxs-lookup"><span data-stu-id="bb8de-130">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="bb8de-131">Типичная древовидная структура</span><span class="sxs-lookup"><span data-stu-id="bb8de-131">Typical Tree Structure</span></span>](#typical-tree-structure)
-   [<span data-ttu-id="bb8de-132">Соответствующие свойства</span><span class="sxs-lookup"><span data-stu-id="bb8de-132">Relevant Properties</span></span>](#relevant-properties)
-   [<span data-ttu-id="bb8de-133">Обязательные шаблоны элементов управления</span><span class="sxs-lookup"><span data-stu-id="bb8de-133">Required Control Patterns</span></span>](#required-control-patterns)
-   [<span data-ttu-id="bb8de-134">Обязательные события</span><span class="sxs-lookup"><span data-stu-id="bb8de-134">Required Events</span></span>](#required-events)
-   [<span data-ttu-id="bb8de-135">Замечания</span><span class="sxs-lookup"><span data-stu-id="bb8de-135">Remarks</span></span>](#remarks)
-   [<span data-ttu-id="bb8de-136">См. также</span><span class="sxs-lookup"><span data-stu-id="bb8de-136">Related topics</span></span>](#related-topics)

## <a name="typical-tree-structure"></a><span data-ttu-id="bb8de-137">Типичная древовидная структура</span><span class="sxs-lookup"><span data-stu-id="bb8de-137">Typical Tree Structure</span></span>

<span data-ttu-id="bb8de-138">В следующей таблице описывается типичный элемент управления и представление содержимого дерева модели автоматизации пользовательского интерфейса, которое относится к элементам управления "переключатель" и описывает, что может содержаться в каждом представлении.</span><span class="sxs-lookup"><span data-stu-id="bb8de-138">The following table depicts a typical control and content view of the UI Automation tree that pertains to radio button controls and describes what can be contained in each view.</span></span> <span data-ttu-id="bb8de-139">Дополнительные сведения о дереве автоматизации пользовательского интерфейса см. в разделе [Общие сведения о дереве модели автоматизации пользовательского интерфейса](uiauto-treeoverview.md).</span><span class="sxs-lookup"><span data-stu-id="bb8de-139">For more information about the UI Automation tree, see [UI Automation Tree Overview](uiauto-treeoverview.md).</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="bb8de-140">Представление элемента управления</span><span class="sxs-lookup"><span data-stu-id="bb8de-140">Control View</span></span></th>
<th><span data-ttu-id="bb8de-141">Представление содержимого</span><span class="sxs-lookup"><span data-stu-id="bb8de-141">Content View</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><ul>
<li><span data-ttu-id="bb8de-142">RadioButton</span><span class="sxs-lookup"><span data-stu-id="bb8de-142">RadioButton</span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="bb8de-143">RadioButton</span><span class="sxs-lookup"><span data-stu-id="bb8de-143">RadioButton</span></span></li>
</ul></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="bb8de-144">Дочерние элементы в представлении элемента управления или представлении содержимого отсутствуют.</span><span class="sxs-lookup"><span data-stu-id="bb8de-144">There are no children in the control view or the content view.</span></span>

## <a name="relevant-properties"></a><span data-ttu-id="bb8de-145">Соответствующие свойства</span><span class="sxs-lookup"><span data-stu-id="bb8de-145">Relevant Properties</span></span>

<span data-ttu-id="bb8de-146">В следующей таблице перечислены свойства модели автоматизации пользовательского интерфейса, значения или определения которых особенно важны для элементов управления, реализующих тип элемента управления **RadioButton** (например, элементы управления "Кнопка").</span><span class="sxs-lookup"><span data-stu-id="bb8de-146">The following table lists the UI Automation properties whose value or definition is especially relevant to the controls that implement the **RadioButton** control type (such as button controls).</span></span> <span data-ttu-id="bb8de-147">Дополнительные сведения о свойствах модели автоматизации пользовательского интерфейса см. в разделе [Получение свойств элементов модели автоматизации пользовательского интерфейса](uiauto-propertiesforclients.md).</span><span class="sxs-lookup"><span data-stu-id="bb8de-147">For more information about UI Automation properties, see [Retrieving Properties from UI Automation Elements](uiauto-propertiesforclients.md).</span></span>



| <span data-ttu-id="bb8de-148">Свойство модели автоматизации пользовательского интерфейса</span><span class="sxs-lookup"><span data-stu-id="bb8de-148">UI Automation Property</span></span>                                                                                              | <span data-ttu-id="bb8de-149">Значение</span><span class="sxs-lookup"><span data-stu-id="bb8de-149">Value</span></span>           | <span data-ttu-id="bb8de-150">Примечания</span><span class="sxs-lookup"><span data-stu-id="bb8de-150">Notes</span></span>                                                                                                                                         |
|---------------------------------------------------------------------------------------------------------------------|-----------------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="bb8de-151">**UIA \_ аутоматионидпропертид**</span><span class="sxs-lookup"><span data-stu-id="bb8de-151">**UIA\_AutomationIdPropertyId**</span></span>](uiauto-automation-element-propids.md)                 | <span data-ttu-id="bb8de-152">См. примечания.</span><span class="sxs-lookup"><span data-stu-id="bb8de-152">See notes.</span></span>      | <span data-ttu-id="bb8de-153">Значение этого свойства должно быть уникальным среди всех одноранговых элементов в необработанном представлении дерева модели автоматизации пользовательского интерфейса.</span><span class="sxs-lookup"><span data-stu-id="bb8de-153">The value of this property must be unique among all peer elements in the raw view of the UI Automation tree.</span></span>                                  |
| [<span data-ttu-id="bb8de-154">**UIA \_ баундингректанглепропертид**</span><span class="sxs-lookup"><span data-stu-id="bb8de-154">**UIA\_BoundingRectanglePropertyId**</span></span>](uiauto-automation-element-propids.md)       | <span data-ttu-id="bb8de-155">См. примечания.</span><span class="sxs-lookup"><span data-stu-id="bb8de-155">See notes.</span></span>      | <span data-ttu-id="bb8de-156">Внешний прямоугольник, содержащий весь элемент управления.</span><span class="sxs-lookup"><span data-stu-id="bb8de-156">The outermost rectangle that contains the whole control.</span></span>                                                                                      |
| [<span data-ttu-id="bb8de-157">**UIA \_ кликкаблепоинтпропертид**</span><span class="sxs-lookup"><span data-stu-id="bb8de-157">**UIA\_ClickablePointPropertyId**</span></span>](uiauto-automation-element-propids.md)             | <span data-ttu-id="bb8de-158">См. примечания.</span><span class="sxs-lookup"><span data-stu-id="bb8de-158">See notes.</span></span>      | <span data-ttu-id="bb8de-159">Точка, которую можно щелкнуть, должна быть точкой, при нажатии которой будет выбран переключатель.</span><span class="sxs-lookup"><span data-stu-id="bb8de-159">The clickable point must be a point that, when clicked, selects the radio button.</span></span>                                                             |
| [<span data-ttu-id="bb8de-160">**UIA \_ контролтипепропертид**</span><span class="sxs-lookup"><span data-stu-id="bb8de-160">**UIA\_ControlTypePropertyId**</span></span>](uiauto-automation-element-propids.md)                   | <span data-ttu-id="bb8de-161">**RadioButton**</span><span class="sxs-lookup"><span data-stu-id="bb8de-161">**RadioButton**</span></span> |                                                                                                                                               |
| [<span data-ttu-id="bb8de-162">**UIA \_ исконтентелементпропертид**</span><span class="sxs-lookup"><span data-stu-id="bb8de-162">**UIA\_IsContentElementPropertyId**</span></span>](uiauto-automation-element-propids.md)         | <span data-ttu-id="bb8de-163">true</span><span class="sxs-lookup"><span data-stu-id="bb8de-163">TRUE</span></span>            | <span data-ttu-id="bb8de-164">Элемент управления "переключатель" всегда включается в представление содержимого дерева модели автоматизации пользовательского интерфейса.</span><span class="sxs-lookup"><span data-stu-id="bb8de-164">The radio button control is always included in the content view of the UI Automation tree.</span></span>                                                    |
| [<span data-ttu-id="bb8de-165">**UIA \_ исконтролелементпропертид**</span><span class="sxs-lookup"><span data-stu-id="bb8de-165">**UIA\_IsControlElementPropertyId**</span></span>](uiauto-automation-element-propids.md)         | <span data-ttu-id="bb8de-166">true</span><span class="sxs-lookup"><span data-stu-id="bb8de-166">TRUE</span></span>            | <span data-ttu-id="bb8de-167">Элемент управления "переключатель" всегда включается в представление элемента управления дерева модели автоматизации пользовательского интерфейса.</span><span class="sxs-lookup"><span data-stu-id="bb8de-167">The radio button control is always included in the control view of the UI Automation tree.</span></span>                                                    |
| [<span data-ttu-id="bb8de-168">**UIA \_ искэйбоардфокусаблепропертид**</span><span class="sxs-lookup"><span data-stu-id="bb8de-168">**UIA\_IsKeyboardFocusablePropertyId**</span></span>](uiauto-automation-element-propids.md)   | <span data-ttu-id="bb8de-169">См. примечания.</span><span class="sxs-lookup"><span data-stu-id="bb8de-169">See notes.</span></span>      | <span data-ttu-id="bb8de-170">Если элемент управления может получать фокус клавиатуры, он должен поддерживать это свойство.</span><span class="sxs-lookup"><span data-stu-id="bb8de-170">If the control can receive keyboard focus, it must support this property.</span></span>                                                                     |
| [<span data-ttu-id="bb8de-171">**UIA \_ лабеледбипропертид**</span><span class="sxs-lookup"><span data-stu-id="bb8de-171">**UIA\_LabeledByPropertyId**</span></span>](uiauto-automation-element-propids.md)                       | <span data-ttu-id="bb8de-172">NULL</span><span class="sxs-lookup"><span data-stu-id="bb8de-172">NULL</span></span>            | <span data-ttu-id="bb8de-173">Элементы управления "переключатель" снабжены собственным содержимым.</span><span class="sxs-lookup"><span data-stu-id="bb8de-173">Radio button controls are self-labeled by their contents.</span></span>                                                                                     |
| [<span data-ttu-id="bb8de-174">**UIA \_ локализедконтролтипепропертид**</span><span class="sxs-lookup"><span data-stu-id="bb8de-174">**UIA\_LocalizedControlTypePropertyId**</span></span>](uiauto-automation-element-propids.md) | <span data-ttu-id="bb8de-175">См. примечания.</span><span class="sxs-lookup"><span data-stu-id="bb8de-175">See notes.</span></span>      | <span data-ttu-id="bb8de-176">Локализованная строка, соответствующая типу элемента управления **RadioButton** .</span><span class="sxs-lookup"><span data-stu-id="bb8de-176">Localized string corresponding to the **RadioButton** control type.</span></span> <span data-ttu-id="bb8de-177">Значение по умолчанию — "переключатель" для en-US или English (США).</span><span class="sxs-lookup"><span data-stu-id="bb8de-177">The default value is "radio button" for en-US or English (United States).</span></span> |
| [<span data-ttu-id="bb8de-178">**UIA \_ намепропертид**</span><span class="sxs-lookup"><span data-stu-id="bb8de-178">**UIA\_NamePropertyId**</span></span>](uiauto-automation-element-propids.md)                                 | <span data-ttu-id="bb8de-179">См. примечания.</span><span class="sxs-lookup"><span data-stu-id="bb8de-179">See notes.</span></span>      | <span data-ttu-id="bb8de-180">Имя элемента управления "переключатель" — это текст, отображаемый рядом с кнопкой, которая поддерживает состояние выбора.</span><span class="sxs-lookup"><span data-stu-id="bb8de-180">The name of the radio button control is the text that is displayed beside the button that maintains the selection state.</span></span>                      |



 

## <a name="required-control-patterns"></a><span data-ttu-id="bb8de-181">Обязательные шаблоны элементов управления</span><span class="sxs-lookup"><span data-stu-id="bb8de-181">Required Control Patterns</span></span>

<span data-ttu-id="bb8de-182">В следующей таблице перечислены шаблоны элементов управления модели автоматизации пользовательского интерфейса, которые должны поддерживаться всеми элементами управления "переключатель".</span><span class="sxs-lookup"><span data-stu-id="bb8de-182">The following table lists the UI Automation control patterns required to be supported by all radio button controls.</span></span> <span data-ttu-id="bb8de-183">Дополнительные сведения о шаблонах элементов управления см. в разделе [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md).</span><span class="sxs-lookup"><span data-stu-id="bb8de-183">For more information on control patterns, see [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md).</span></span>



| <span data-ttu-id="bb8de-184">Шаблон элемента управления/свойство шаблона</span><span class="sxs-lookup"><span data-stu-id="bb8de-184">Control Pattern/Pattern Property</span></span>                                               | <span data-ttu-id="bb8de-185">Поддержка/значение</span><span class="sxs-lookup"><span data-stu-id="bb8de-185">Support/Value</span></span> | <span data-ttu-id="bb8de-186">Примечания</span><span class="sxs-lookup"><span data-stu-id="bb8de-186">Notes</span></span>                                                                                                                                                                                                                                                                                                                                                                                                             |
|--------------------------------------------------------------------------------|---------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="bb8de-187">**ISelectionItemProvider**</span><span class="sxs-lookup"><span data-stu-id="bb8de-187">**ISelectionItemProvider**</span></span>](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iselectionitemprovider)                | <span data-ttu-id="bb8de-188">Обязательно</span><span class="sxs-lookup"><span data-stu-id="bb8de-188">Required</span></span>      | <span data-ttu-id="bb8de-189">Все элементы управления "переключатель" должны поддерживать шаблон элемента управления [SelectionItem](uiauto-implementingselectionitem.md) , чтобы обеспечить возможность выбора.</span><span class="sxs-lookup"><span data-stu-id="bb8de-189">All radio button controls must support the [SelectionItem](uiauto-implementingselectionitem.md) control pattern to enable themselves to be selected.</span></span>                                                                                                                                                                                                                                                             |
| [<span data-ttu-id="bb8de-190">**селектионконтаинер**</span><span class="sxs-lookup"><span data-stu-id="bb8de-190">**SelectionContainer**</span></span>](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iselectionitemprovider-get_selectioncontainer) | <span data-ttu-id="bb8de-191">См. примечания.</span><span class="sxs-lookup"><span data-stu-id="bb8de-191">See notes.</span></span>    | <span data-ttu-id="bb8de-192">Свойство [**селектионконтаинер**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iselectionitemprovider-get_selectioncontainer) должно всегда быть завершено, чтобы клиент автоматизации пользовательского интерфейса мог определить, какие другие переключатели в определенном контексте связаны друг с другом.</span><span class="sxs-lookup"><span data-stu-id="bb8de-192">The [**SelectionContainer**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iselectionitemprovider-get_selectioncontainer) property must always be completed so that a UI Automation client can determine what other radio buttons within a specific context relate to one another.</span></span> <span data-ttu-id="bb8de-193">Для версии Microsoft Win32 переключателя не поддерживается это свойство, так как невозможно получить эти сведения из этой устаревшей платформы.</span><span class="sxs-lookup"><span data-stu-id="bb8de-193">For the Microsoft Win32 version of the radio button, this property is not supported because it is not possible to obtain this information from that legacy framework.</span></span> |
| [<span data-ttu-id="bb8de-194">**IToggleProvider**</span><span class="sxs-lookup"><span data-stu-id="bb8de-194">**IToggleProvider**</span></span>](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itoggleprovider)                              | <span data-ttu-id="bb8de-195">Никогда</span><span class="sxs-lookup"><span data-stu-id="bb8de-195">Never</span></span>         | <span data-ttu-id="bb8de-196">Переключатель не может циклически проходить свое состояние после его установки.</span><span class="sxs-lookup"><span data-stu-id="bb8de-196">The radio button cannot cycle through its state once it has been set.</span></span> <span data-ttu-id="bb8de-197">Шаблон [элемента управления "переключатель"](uiauto-implementingtoggle.md) никогда не должен поддерживаться переключателем.</span><span class="sxs-lookup"><span data-stu-id="bb8de-197">The [Toggle](uiauto-implementingtoggle.md) control pattern must never be supported on a radio button.</span></span>                                                                                                                                                                                                                                      |



 

## <a name="required-events"></a><span data-ttu-id="bb8de-198">Обязательные события</span><span class="sxs-lookup"><span data-stu-id="bb8de-198">Required Events</span></span>

<span data-ttu-id="bb8de-199">В следующей таблице перечислены события автоматизации пользовательского интерфейса, которые должны поддерживаться элементами управления "Кнопка".</span><span class="sxs-lookup"><span data-stu-id="bb8de-199">The following table lists the UI Automation events that button controls are required to support.</span></span> <span data-ttu-id="bb8de-200">Дополнительные сведения о событиях см. в разделе [UI Automation Events Overview](uiauto-eventsoverview.md).</span><span class="sxs-lookup"><span data-stu-id="bb8de-200">For more information on events, see [UI Automation Events Overview](uiauto-eventsoverview.md).</span></span>



| <span data-ttu-id="bb8de-201">Событие автоматизации пользовательского интерфейса</span><span class="sxs-lookup"><span data-stu-id="bb8de-201">UI Automation Event</span></span>                                                                                                                     | <span data-ttu-id="bb8de-202">Примечания</span><span class="sxs-lookup"><span data-stu-id="bb8de-202">Notes</span></span>                                                                                                                          |
|-----------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="bb8de-203">**UIA \_ аутоматионфокусчанжедевентид**</span><span class="sxs-lookup"><span data-stu-id="bb8de-203">**UIA\_AutomationFocusChangedEventId**</span></span>](uiauto-event-ids.md)                                        |                                                                                                                                |
| <span data-ttu-id="bb8de-204">[**UIA \_**](uiauto-automation-element-propids.md) Событие изменения свойства баундингректанглепропертид.</span><span class="sxs-lookup"><span data-stu-id="bb8de-204">[**UIA\_BoundingRectanglePropertyId**](uiauto-automation-element-propids.md) property-changed event.</span></span>   |                                                                                                                                |
| <span data-ttu-id="bb8de-205">[**UIA \_**](uiauto-automation-element-propids.md) Событие изменения свойства исенабледпропертид.</span><span class="sxs-lookup"><span data-stu-id="bb8de-205">[**UIA\_IsEnabledPropertyId**](uiauto-automation-element-propids.md) property-changed event.</span></span>                   | <span data-ttu-id="bb8de-206">Если элемент управления поддерживает свойство « [**включено**](uiauto-automation-element-propids.md) », оно должно поддерживать это событие.</span><span class="sxs-lookup"><span data-stu-id="bb8de-206">If the control supports the [**IsEnabled**](uiauto-automation-element-propids.md) property, it must support this event.</span></span>       |
| <span data-ttu-id="bb8de-207">[**UIA \_**](uiauto-automation-element-propids.md) Событие изменения свойства исоффскринпропертид.</span><span class="sxs-lookup"><span data-stu-id="bb8de-207">[**UIA\_IsOffscreenPropertyId**](uiauto-automation-element-propids.md) property-changed event.</span></span>               | <span data-ttu-id="bb8de-208">Если элемент управления поддерживает свойство [**исоффскрин**](uiauto-automation-element-propids.md) , он должен поддерживать это событие.</span><span class="sxs-lookup"><span data-stu-id="bb8de-208">If the control supports the [**IsOffscreen**](uiauto-automation-element-propids.md) property, it must support this event.</span></span>     |
| [<span data-ttu-id="bb8de-209">**UIA \_ SelectionItem \_ елементремоведфромселектионевентид**</span><span class="sxs-lookup"><span data-stu-id="bb8de-209">**UIA\_SelectionItem\_ElementRemovedFromSelectionEventId**</span></span>](uiauto-event-ids.md) | <span data-ttu-id="bb8de-210">Если элемент управления поддерживает шаблон элемента управления [SelectionItem](uiauto-implementingselectionitem.md) , он должен поддерживать это событие.</span><span class="sxs-lookup"><span data-stu-id="bb8de-210">If the control supports the [SelectionItem](uiauto-implementingselectionitem.md) control pattern, it must support this event.</span></span> |
| [<span data-ttu-id="bb8de-211">**UIA \_ SelectionItem \_ елементселектедевентид**</span><span class="sxs-lookup"><span data-stu-id="bb8de-211">**UIA\_SelectionItem\_ElementSelectedEventId**</span></span>](uiauto-event-ids.md)                         | <span data-ttu-id="bb8de-212">Если элемент управления поддерживает шаблон элемента управления [SelectionItem](uiauto-implementingselectionitem.md) , он должен поддерживать это событие.</span><span class="sxs-lookup"><span data-stu-id="bb8de-212">If the control supports the [SelectionItem](uiauto-implementingselectionitem.md) control pattern, it must support this event.</span></span> |
| [<span data-ttu-id="bb8de-213">**UIA \_ структуречанжедевентид**</span><span class="sxs-lookup"><span data-stu-id="bb8de-213">**UIA\_StructureChangedEventId**</span></span>](uiauto-event-ids.md)                                                    |                                                                                                                                |



 

## <a name="remarks"></a><span data-ttu-id="bb8de-214">Комментарии</span><span class="sxs-lookup"><span data-stu-id="bb8de-214">Remarks</span></span>

<span data-ttu-id="bb8de-215">Переключатель представляет единственный Выбираемый параметр среди групп одноранговых переключателей.</span><span class="sxs-lookup"><span data-stu-id="bb8de-215">A radio button represents a single selectable option among a group of peer radio buttons.</span></span> <span data-ttu-id="bb8de-216">В идеале переключатели должны иметь элемент grouping, поясняющий границы одноранговых переключателей.</span><span class="sxs-lookup"><span data-stu-id="bb8de-216">Ideally, radio buttons should have a grouping element that clarifies the boundaries of the peer radio buttons.</span></span> <span data-ttu-id="bb8de-217">Однако часто граница подразумевается структурой элементов пользовательского интерфейса.</span><span class="sxs-lookup"><span data-stu-id="bb8de-217">Often, however, the boundary is implied by the UI element structure.</span></span> <span data-ttu-id="bb8de-218">Например, меню может содержать набор последовательных переключателей вместо пунктов меню или набор переключателей, которые появляются после метки группы, но перед элементом, который может быть членом действия, таким как Button.</span><span class="sxs-lookup"><span data-stu-id="bb8de-218">For example, a menu might contain a set of consecutive radio buttons instead of menu items, or a set of radio buttons that occur after a group label, but before an actionable element such as button.</span></span>

## <a name="related-topics"></a><span data-ttu-id="bb8de-219">См. также</span><span class="sxs-lookup"><span data-stu-id="bb8de-219">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="bb8de-220">**Зрения**</span><span class="sxs-lookup"><span data-stu-id="bb8de-220">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="bb8de-221">Общие сведения о типах элементов управления автоматизации пользовательского интерфейса</span><span class="sxs-lookup"><span data-stu-id="bb8de-221">UI Automation Control Types Overview</span></span>](uiauto-controltypesoverview.md)
</dt> <dt>

[<span data-ttu-id="bb8de-222">Общие сведения о модели автоматизации пользовательского интерфейса</span><span class="sxs-lookup"><span data-stu-id="bb8de-222">UI Automation Overview</span></span>](uiauto-uiautomationoverview.md)
</dt> </dl>

 

 




