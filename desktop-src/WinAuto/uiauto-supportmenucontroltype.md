---
title: Тип элемента управления Menu
description: В этом разделе содержатся сведения о поддержке автоматизации пользовательского интерфейса Майкрософт для типа элемента управления Menu.
ms.assetid: cdbb6db7-63d7-422e-952c-7b59779fefbe
keywords:
- Модель автоматизации пользовательского интерфейса, поддержка типа элемента управления Menu
- Модель автоматизации пользовательского интерфейса, тип элемента управления Menu
- Модель автоматизации пользовательского интерфейса, древовидная структура для типа элемента управления Menu
- Модель автоматизации пользовательского интерфейса, свойства для типа элемента управления Menu
- Модель автоматизации пользовательского интерфейса, шаблоны элементов управления для типа элемента управления Menu
- Модель автоматизации пользовательского интерфейса, события для типа элемента управления Menu
- Древовидные структуры, тип элемента управления Menu
- свойства, тип элемента управления Menu
- шаблоны элементов управления, тип элемента управления Menu
- события, тип элемента управления Menu
- Поддержка типа элемента управления Menu
- Меню - тип элемента управления
- типы элементов управления, древовидная структура для типа элемента управления Menu
- типы элементов управления, шаблоны элементов управления для типа элемента управления Menu
- типы элементов управления, поддержка меню
- типы элементов управления, меню
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: edee9f30f4d4cea123a2c7f5ff4dac235782faea
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104067866"
---
# <a name="menu-control-type"></a><span data-ttu-id="894ca-119">Тип элемента управления Menu</span><span class="sxs-lookup"><span data-stu-id="894ca-119">Menu Control Type</span></span>

<span data-ttu-id="894ca-120">В этом разделе содержатся сведения о поддержке автоматизации пользовательского интерфейса Майкрософт для типа элемента управления **Menu** .</span><span class="sxs-lookup"><span data-stu-id="894ca-120">This topic provides information about Microsoft UI Automation support for the **Menu** control type.</span></span>

<span data-ttu-id="894ca-121">Элемент управления "Меню" позволяет иерархически организовать элементы, связанные с командами и обработчиками событий.</span><span class="sxs-lookup"><span data-stu-id="894ca-121">A menu control allows hierarchal organization of elements associated with commands and event handlers.</span></span> <span data-ttu-id="894ca-122">В типичном приложении Microsoft Windows строка меню содержит несколько кнопок меню (например, **файл**, **Правка** и **окно**), и каждая кнопка меню отображает меню.</span><span class="sxs-lookup"><span data-stu-id="894ca-122">In a typical Microsoft Windows application, a menu bar contains several menu buttons (such as **File**, **Edit**, and **Window**), and each menu button displays a menu.</span></span> <span data-ttu-id="894ca-123">Меню содержит набор пунктов меню (таких как **Создать**, **Открыть** и **Закрыть**), которые можно развернуть, чтобы отобразить дополнительные пункты меню или выполнить определенное действие, нажав соответствующий пункт.</span><span class="sxs-lookup"><span data-stu-id="894ca-123">A menu contains a collection of menu items (such as **New**, **Open**, and **Close**), which can be expanded to display additional menu items or to perform a specific action when clicked.</span></span>

<span data-ttu-id="894ca-124">В следующих разделах определяется необходимая древовидная структура модели автоматизации пользовательского интерфейса, свойства, шаблоны элементов управления и события для типа элемента управления **Menu** .</span><span class="sxs-lookup"><span data-stu-id="894ca-124">The following sections define the required UI Automation tree structure, properties, control patterns, and events for the **Menu** control type.</span></span> <span data-ttu-id="894ca-125">Требования к автоматизации пользовательского интерфейса применяются ко всем элементам управления "меню", в которых платформа или платформа пользовательского интерфейса интегрирует поддержку модели автоматизации пользовательского интерфейса для типов элементов управления и шаблонов элементов управления.</span><span class="sxs-lookup"><span data-stu-id="894ca-125">The UI Automation requirements apply to all menu controls where the UI framework/platform integrates UI Automation support for control types and control patterns.</span></span>

<span data-ttu-id="894ca-126">В этом разделе содержатся следующие подразделы.</span><span class="sxs-lookup"><span data-stu-id="894ca-126">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="894ca-127">Типичная древовидная структура</span><span class="sxs-lookup"><span data-stu-id="894ca-127">Typical Tree Structure</span></span>](#typical-tree-structure)
-   [<span data-ttu-id="894ca-128">Соответствующие свойства</span><span class="sxs-lookup"><span data-stu-id="894ca-128">Relevant Properties</span></span>](#relevant-properties)
-   [<span data-ttu-id="894ca-129">Обязательные шаблоны элементов управления</span><span class="sxs-lookup"><span data-stu-id="894ca-129">Required Control Patterns</span></span>](#required-control-patterns)
-   [<span data-ttu-id="894ca-130">Обязательные события</span><span class="sxs-lookup"><span data-stu-id="894ca-130">Required Events</span></span>](#required-events)
-   [<span data-ttu-id="894ca-131">См. также</span><span class="sxs-lookup"><span data-stu-id="894ca-131">Related topics</span></span>](#related-topics)

## <a name="typical-tree-structure"></a><span data-ttu-id="894ca-132">Типичная древовидная структура</span><span class="sxs-lookup"><span data-stu-id="894ca-132">Typical Tree Structure</span></span>

<span data-ttu-id="894ca-133">В следующей таблице описывается типичный элемент управления и представление содержимого дерева модели автоматизации пользовательского интерфейса, которое относится к элементам управления "меню" и описывает, что может содержаться в каждом представлении.</span><span class="sxs-lookup"><span data-stu-id="894ca-133">The following table depicts a typical control and content view of the UI Automation tree that pertains to menu controls and describes what can be contained in each view.</span></span> <span data-ttu-id="894ca-134">Дополнительные сведения о дереве автоматизации пользовательского интерфейса см. в разделе [Общие сведения о дереве модели автоматизации пользовательского интерфейса](uiauto-treeoverview.md).</span><span class="sxs-lookup"><span data-stu-id="894ca-134">For more information about the UI Automation tree, see [UI Automation Tree Overview](uiauto-treeoverview.md).</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="894ca-135">Представление элемента управления</span><span class="sxs-lookup"><span data-stu-id="894ca-135">Control View</span></span></th>
<th><span data-ttu-id="894ca-136">Представление содержимого</span><span class="sxs-lookup"><span data-stu-id="894ca-136">Content View</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><ul>
<li><span data-ttu-id="894ca-137">Меню</span><span class="sxs-lookup"><span data-stu-id="894ca-137">Menu</span></span>
<ul>
<li><span data-ttu-id="894ca-138">MenuItem (1 или более)</span><span class="sxs-lookup"><span data-stu-id="894ca-138">MenuItem (1 or many)</span></span></li>
</ul>
<ul>
<li><span data-ttu-id="894ca-139">Другие элементы управления (0 или более)</span><span class="sxs-lookup"><span data-stu-id="894ca-139">Other controls (0 or many)</span></span></li>
</ul></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="894ca-140">Меню</span><span class="sxs-lookup"><span data-stu-id="894ca-140">Menu</span></span>
<ul>
<li><span data-ttu-id="894ca-141">MenuItem (1 или более)</span><span class="sxs-lookup"><span data-stu-id="894ca-141">MenuItem (1 or many)</span></span></li>
</ul>
<ul>
<li><span data-ttu-id="894ca-142">Другие элементы управления (0 или более)</span><span class="sxs-lookup"><span data-stu-id="894ca-142">Other controls (0 or many)</span></span></li>
</ul></li>
</ul></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="894ca-143">Элементы управления "меню" всегда отображаются в представлении элемента управления и представлении содержимого дерева модели автоматизации пользовательского интерфейса.</span><span class="sxs-lookup"><span data-stu-id="894ca-143">Menu controls always appear in the control view and the content view of the UI Automation tree.</span></span> <span data-ttu-id="894ca-144">Элементы управления "меню" должны отображаться под элементом управления, на который ссылаются их сведения.</span><span class="sxs-lookup"><span data-stu-id="894ca-144">Menu controls should appear under the control that their information is referring to.</span></span> <span data-ttu-id="894ca-145">Клиенты автоматизации пользовательского интерфейса могут прослушивать [**UIA \_ менуопенедевентид**](uiauto-event-ids.md) , чтобы убедиться, что они постоянно получают сведения, передаваемые элементами управления Menu.</span><span class="sxs-lookup"><span data-stu-id="894ca-145">UI Automation clients can listen for [**UIA\_MenuOpenedEventId**](uiauto-event-ids.md) to ensure that they consistently obtain information conveyed by menu controls.</span></span> <span data-ttu-id="894ca-146">Особым случаем являются элементы управления "Контекстное меню".</span><span class="sxs-lookup"><span data-stu-id="894ca-146">Context menu controls are a special case.</span></span> <span data-ttu-id="894ca-147">Они могут отображаться как дочерние элементы рабочего стола или окна приложения верхнего уровня.</span><span class="sxs-lookup"><span data-stu-id="894ca-147">They may appear as children of the desktop or of a top level application window.</span></span>

<span data-ttu-id="894ca-148">Элемент управления Menu может содержать другие элементы управления, такие как поля редактирования и поля со списком, в структуре.</span><span class="sxs-lookup"><span data-stu-id="894ca-148">A menu control can contain other controls, such as edit controls and combo boxes, within its structure.</span></span> <span data-ttu-id="894ca-149">Эти дополнительные элементы управления соответствуют "другим элементам управления", перечисленным в предыдущей таблице в представлениях элемента управления и содержимого.</span><span class="sxs-lookup"><span data-stu-id="894ca-149">These additional controls correspond to the "other controls" listed in the previous table in the control and content views.</span></span>

## <a name="relevant-properties"></a><span data-ttu-id="894ca-150">Соответствующие свойства</span><span class="sxs-lookup"><span data-stu-id="894ca-150">Relevant Properties</span></span>

<span data-ttu-id="894ca-151">В следующей таблице перечислены свойства модели автоматизации пользовательского интерфейса, значения или определения которых особенно важны для типа элемента управления **Menu** .</span><span class="sxs-lookup"><span data-stu-id="894ca-151">The following table lists the UI Automation properties whose value or definition is especially relevant to the **Menu** control type.</span></span> <span data-ttu-id="894ca-152">Дополнительные сведения о свойствах модели автоматизации пользовательского интерфейса см. в разделе [Получение свойств элементов модели автоматизации пользовательского интерфейса](uiauto-propertiesforclients.md).</span><span class="sxs-lookup"><span data-stu-id="894ca-152">For more information about UI Automation properties, see [Retrieving Properties from UI Automation Elements](uiauto-propertiesforclients.md).</span></span>



| <span data-ttu-id="894ca-153">Свойство модели автоматизации пользовательского интерфейса</span><span class="sxs-lookup"><span data-stu-id="894ca-153">UI Automation Property</span></span>                                                                                      | <span data-ttu-id="894ca-154">Значение</span><span class="sxs-lookup"><span data-stu-id="894ca-154">Value</span></span>      | <span data-ttu-id="894ca-155">Примечания</span><span class="sxs-lookup"><span data-stu-id="894ca-155">Notes</span></span>                                                                                                                                                                   |
|-------------------------------------------------------------------------------------------------------------|------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="894ca-156">**UIA \_ контролтипепропертид**</span><span class="sxs-lookup"><span data-stu-id="894ca-156">**UIA\_ControlTypePropertyId**</span></span>](uiauto-automation-element-propids.md)           | <span data-ttu-id="894ca-157">**Меню**</span><span class="sxs-lookup"><span data-stu-id="894ca-157">**Menu**</span></span>   |                                                                                                                                                                         |
| [<span data-ttu-id="894ca-158">**UIA \_ исконтентелементпропертид**</span><span class="sxs-lookup"><span data-stu-id="894ca-158">**UIA\_IsContentElementPropertyId**</span></span>](uiauto-automation-element-propids.md) | <span data-ttu-id="894ca-159">true</span><span class="sxs-lookup"><span data-stu-id="894ca-159">TRUE</span></span>       | <span data-ttu-id="894ca-160">Элемент управления "меню" всегда включается в представление содержимого дерева модели автоматизации пользовательского интерфейса.</span><span class="sxs-lookup"><span data-stu-id="894ca-160">The menu control is always included in the content view of the UI Automation tree.</span></span>                                                                                      |
| [<span data-ttu-id="894ca-161">**UIA \_ исконтролелементпропертид**</span><span class="sxs-lookup"><span data-stu-id="894ca-161">**UIA\_IsControlElementPropertyId**</span></span>](uiauto-automation-element-propids.md) | <span data-ttu-id="894ca-162">true</span><span class="sxs-lookup"><span data-stu-id="894ca-162">TRUE</span></span>       | <span data-ttu-id="894ca-163">Элемент управления "меню" всегда включается в представление элемента управления дерева модели автоматизации пользовательского интерфейса.</span><span class="sxs-lookup"><span data-stu-id="894ca-163">The menu control is always included in the control view of the UI Automation tree.</span></span>                                                                                      |
| [<span data-ttu-id="894ca-164">**UIA \_ лабеледбипропертид**</span><span class="sxs-lookup"><span data-stu-id="894ca-164">**UIA\_LabeledByPropertyId**</span></span>](uiauto-automation-element-propids.md)               | <span data-ttu-id="894ca-165">NULL</span><span class="sxs-lookup"><span data-stu-id="894ca-165">NULL</span></span>       | <span data-ttu-id="894ca-166">С обычным элементом управления "Меню" не ожидается никаких меток.</span><span class="sxs-lookup"><span data-stu-id="894ca-166">No label is anticipated with a typical menu control.</span></span>                                                                                                                    |
| [<span data-ttu-id="894ca-167">**UIA \_ намепропертид**</span><span class="sxs-lookup"><span data-stu-id="894ca-167">**UIA\_NamePropertyId**</span></span>](uiauto-automation-element-propids.md)                         | <span data-ttu-id="894ca-168">См. примечания.</span><span class="sxs-lookup"><span data-stu-id="894ca-168">See notes.</span></span> | <span data-ttu-id="894ca-169">Элементу управления "меню" не требуется задавать свойство **Name** или имя, совпадающее с именем связанного элемента управления, например, пункт меню, открывший подменю.</span><span class="sxs-lookup"><span data-stu-id="894ca-169">The menu control does not require a **Name** property to be set, or it could have the same name as the associated control, such as a menu item that opened the submenu.</span></span> |



 

## <a name="required-control-patterns"></a><span data-ttu-id="894ca-170">Обязательные шаблоны элементов управления</span><span class="sxs-lookup"><span data-stu-id="894ca-170">Required Control Patterns</span></span>

<span data-ttu-id="894ca-171">Для типа элемента управления Menu отсутствуют обязательные шаблоны элементов управления.</span><span class="sxs-lookup"><span data-stu-id="894ca-171">There are no required control patterns for the Menu control type.</span></span>

## <a name="required-events"></a><span data-ttu-id="894ca-172">Обязательные события</span><span class="sxs-lookup"><span data-stu-id="894ca-172">Required Events</span></span>

<span data-ttu-id="894ca-173">Элементы управления "меню" должны вызывать событие [**UIA \_ менуопенедевентид**](uiauto-event-ids.md) , когда они появляются на экране.</span><span class="sxs-lookup"><span data-stu-id="894ca-173">Menu controls must raise the [**UIA\_MenuOpenedEventId**](uiauto-event-ids.md) event when they appear on the screen.</span></span> <span data-ttu-id="894ca-174">Событие **UIA \_ менуопенедевентид** будет включать текст элемента управления.</span><span class="sxs-lookup"><span data-stu-id="894ca-174">The **UIA\_MenuOpenedEventId** event will include the text of the control.</span></span> <span data-ttu-id="894ca-175">Событие [**UIA \_ менуклоседевентид**](uiauto-event-ids.md) должно вызываться при исчезновении меню с экрана.</span><span class="sxs-lookup"><span data-stu-id="894ca-175">The [**UIA\_MenuClosedEventId**](uiauto-event-ids.md) event must be raised when a menu disappears from the screen.</span></span>

<span data-ttu-id="894ca-176">В следующей таблице перечислены события модели автоматизации пользовательского интерфейса, которые должны поддерживаться элементами управления "меню".</span><span class="sxs-lookup"><span data-stu-id="894ca-176">The following table lists the UI Automation events that menu controls are required to support.</span></span> <span data-ttu-id="894ca-177">Дополнительные сведения о событиях см. в разделе [UI Automation Events Overview](uiauto-eventsoverview.md).</span><span class="sxs-lookup"><span data-stu-id="894ca-177">For more information on events, see [UI Automation Events Overview](uiauto-eventsoverview.md).</span></span>



| <span data-ttu-id="894ca-178">Событие автоматизации пользовательского интерфейса</span><span class="sxs-lookup"><span data-stu-id="894ca-178">UI Automation Event</span></span>                                                                                                                   | <span data-ttu-id="894ca-179">Примечания</span><span class="sxs-lookup"><span data-stu-id="894ca-179">Notes</span></span>                                                                                                                      |
|---------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="894ca-180">**UIA \_ аутоматионфокусчанжедевентид**</span><span class="sxs-lookup"><span data-stu-id="894ca-180">**UIA\_AutomationFocusChangedEventId**</span></span>](uiauto-event-ids.md)                                      |                                                                                                                            |
| <span data-ttu-id="894ca-181">[**UIA \_**](uiauto-automation-element-propids.md) Событие изменения свойства баундингректанглепропертид.</span><span class="sxs-lookup"><span data-stu-id="894ca-181">[**UIA\_BoundingRectanglePropertyId**](uiauto-automation-element-propids.md) property-changed event.</span></span> |                                                                                                                            |
| <span data-ttu-id="894ca-182">[**UIA \_**](uiauto-automation-element-propids.md) Событие изменения свойства исенабледпропертид.</span><span class="sxs-lookup"><span data-stu-id="894ca-182">[**UIA\_IsEnabledPropertyId**](uiauto-automation-element-propids.md) property-changed event.</span></span>                 | <span data-ttu-id="894ca-183">Если элемент управления поддерживает свойство « [**включено**](uiauto-automation-element-propids.md) », оно должно поддерживать это событие.</span><span class="sxs-lookup"><span data-stu-id="894ca-183">If the control supports the [**IsEnabled**](uiauto-automation-element-propids.md) property, it must support this event.</span></span>   |
| <span data-ttu-id="894ca-184">[**UIA \_**](uiauto-automation-element-propids.md) Событие изменения свойства исоффскринпропертид.</span><span class="sxs-lookup"><span data-stu-id="894ca-184">[**UIA\_IsOffscreenPropertyId**](uiauto-automation-element-propids.md) property-changed event.</span></span>             | <span data-ttu-id="894ca-185">Если элемент управления поддерживает свойство [**исоффскрин**](uiauto-automation-element-propids.md) , он должен поддерживать это событие.</span><span class="sxs-lookup"><span data-stu-id="894ca-185">If the control supports the [**IsOffscreen**](uiauto-automation-element-propids.md) property, it must support this event.</span></span> |
| [<span data-ttu-id="894ca-186">**UIA \_ менуклоседевентид**</span><span class="sxs-lookup"><span data-stu-id="894ca-186">**UIA\_MenuClosedEventId**</span></span>](uiauto-event-ids.md)                                                              |                                                                                                                            |
| [<span data-ttu-id="894ca-187">**UIA \_ менуопенедевентид**</span><span class="sxs-lookup"><span data-stu-id="894ca-187">**UIA\_MenuOpenedEventId**</span></span>](uiauto-event-ids.md)                                                              |                                                                                                                            |
| [<span data-ttu-id="894ca-188">**UIA \_ структуречанжедевентид**</span><span class="sxs-lookup"><span data-stu-id="894ca-188">**UIA\_StructureChangedEventId**</span></span>](uiauto-event-ids.md)                                                  |                                                                                                                            |



 

## <a name="related-topics"></a><span data-ttu-id="894ca-189">См. также</span><span class="sxs-lookup"><span data-stu-id="894ca-189">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="894ca-190">**Зрения**</span><span class="sxs-lookup"><span data-stu-id="894ca-190">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="894ca-191">Общие сведения о типах элементов управления автоматизации пользовательского интерфейса</span><span class="sxs-lookup"><span data-stu-id="894ca-191">UI Automation Control Types Overview</span></span>](uiauto-controltypesoverview.md)
</dt> <dt>

[<span data-ttu-id="894ca-192">Общие сведения о модели автоматизации пользовательского интерфейса</span><span class="sxs-lookup"><span data-stu-id="894ca-192">UI Automation Overview</span></span>](uiauto-uiautomationoverview.md)
</dt> </dl>

 

 




