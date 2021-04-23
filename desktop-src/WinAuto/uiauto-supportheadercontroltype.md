---
title: Тип элемента управления "заголовок"
description: В этом разделе содержатся сведения о поддержке автоматизации пользовательского интерфейса Майкрософт для типа элемента управления "заголовок".
ms.assetid: 032fc3a1-f939-40db-abbb-532afe309ba3
keywords:
- Модель автоматизации пользовательского интерфейса, поддержка типа элемента управления Header
- Модель автоматизации пользовательского интерфейса, тип элемента управления "заголовок"
- Модель автоматизации пользовательского интерфейса, древовидная структура для типа элемента управления Header
- Модель автоматизации пользовательского интерфейса, свойства для типа элемента управления заголовков
- Модель автоматизации пользовательского интерфейса, шаблоны элементов управления для типа элемента управления Header
- Модель автоматизации пользовательского интерфейса, события для типа элемента управления заголовков
- Древовидные структуры, тип элемента управления "заголовок"
- свойства, тип элемента управления "заголовок"
- шаблоны элементов управления, тип элемента управления "заголовок"
- события, тип элемента управления "заголовок"
- Поддержка типа элемента управления "заголовок"
- Header - тип элемента управления
- типы элементов управления, древовидная структура для типа элемента управления Header
- типы элементов управления, шаблоны элементов управления для типа элемента управления заголовков
- типы элементов управления, поддержка заголовка
- типы элементов управления, заголовок
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c38ee0a00749888c624b627db247f2d01d24ff1c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104410885"
---
# <a name="header-control-type"></a><span data-ttu-id="84430-119">Тип элемента управления "заголовок"</span><span class="sxs-lookup"><span data-stu-id="84430-119">Header Control Type</span></span>

<span data-ttu-id="84430-120">В этом разделе содержатся сведения о поддержке автоматизации пользовательского интерфейса Майкрософт для типа элемента управления " **заголовок** ".</span><span class="sxs-lookup"><span data-stu-id="84430-120">This topic provides information about Microsoft UI Automation support for the **Header** control type.</span></span>

<span data-ttu-id="84430-121">Элемент управления "Заголовок" предоставляет визуальный контейнер для меток строк или столбцов данных.</span><span class="sxs-lookup"><span data-stu-id="84430-121">The header control provides a visual container for the labels for rows or columns of information.</span></span>

<span data-ttu-id="84430-122">В следующих разделах определяется необходимая древовидная структура модели автоматизации пользовательского интерфейса, свойства, шаблоны элементов управления и события для типа элемента управления **Header** .</span><span class="sxs-lookup"><span data-stu-id="84430-122">The following sections define the required UI Automation tree structure, properties, control patterns, and events for the **Header** control type.</span></span> <span data-ttu-id="84430-123">Требования к автоматизации пользовательского интерфейса применяются ко всем элементам управления "заголовок", в которых платформа или платформа пользовательского интерфейса интегрирует поддержку модели автоматизации пользовательского интерфейса для типов элементов управления и шаблонов элементов управления.</span><span class="sxs-lookup"><span data-stu-id="84430-123">The UI Automation requirements apply to all header controls where the UI framework/platform integrates UI Automation support for control types and control patterns.</span></span>

<span data-ttu-id="84430-124">В этом разделе содержатся следующие подразделы.</span><span class="sxs-lookup"><span data-stu-id="84430-124">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="84430-125">Типичная древовидная структура</span><span class="sxs-lookup"><span data-stu-id="84430-125">Typical Tree Structure</span></span>](#typical-tree-structure)
-   [<span data-ttu-id="84430-126">Соответствующие свойства</span><span class="sxs-lookup"><span data-stu-id="84430-126">Relevant Properties</span></span>](#relevant-properties)
-   [<span data-ttu-id="84430-127">Обязательные шаблоны элементов управления</span><span class="sxs-lookup"><span data-stu-id="84430-127">Required Control Patterns</span></span>](#required-control-patterns)
-   [<span data-ttu-id="84430-128">Обязательные события</span><span class="sxs-lookup"><span data-stu-id="84430-128">Required Events</span></span>](#required-events)
-   [<span data-ttu-id="84430-129">См. также</span><span class="sxs-lookup"><span data-stu-id="84430-129">Related topics</span></span>](#related-topics)

## <a name="typical-tree-structure"></a><span data-ttu-id="84430-130">Типичная древовидная структура</span><span class="sxs-lookup"><span data-stu-id="84430-130">Typical Tree Structure</span></span>

<span data-ttu-id="84430-131">В следующей таблице описывается типичный элемент управления и представление содержимого дерева модели автоматизации пользовательского интерфейса, которое относится к элементам управления "заголовок" и описывает, что может содержаться в каждом представлении.</span><span class="sxs-lookup"><span data-stu-id="84430-131">The following table depicts a typical control and content view of the UI Automation tree that pertains to header controls and describes what can be contained in each view.</span></span> <span data-ttu-id="84430-132">Дополнительные сведения о дереве автоматизации пользовательского интерфейса см. в разделе [Общие сведения о дереве модели автоматизации пользовательского интерфейса](uiauto-treeoverview.md).</span><span class="sxs-lookup"><span data-stu-id="84430-132">For more information about the UI Automation tree, see [UI Automation Tree Overview](uiauto-treeoverview.md).</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="84430-133">Представление элемента управления</span><span class="sxs-lookup"><span data-stu-id="84430-133">Control View</span></span></th>
<th><span data-ttu-id="84430-134">Представление содержимого</span><span class="sxs-lookup"><span data-stu-id="84430-134">Content View</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><ul>
<li><span data-ttu-id="84430-135">Header</span><span class="sxs-lookup"><span data-stu-id="84430-135">Header</span></span>
<ul>
<li><span data-ttu-id="84430-136">HeaderItem (1 или более)</span><span class="sxs-lookup"><span data-stu-id="84430-136">HeaderItem (1 or more)</span></span></li>
</ul></li>
</ul></td>
<td><span data-ttu-id="84430-137">(Неприменимо)</span><span class="sxs-lookup"><span data-stu-id="84430-137">(Not applicable)</span></span></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="84430-138">Элементы управления "заголовок" всегда имеют один или несколько дочерних элементов в представлении элемента управления дерева модели автоматизации пользовательского интерфейса.</span><span class="sxs-lookup"><span data-stu-id="84430-138">Header controls always have one or more children in the control view of the UI Automation tree.</span></span>

<span data-ttu-id="84430-139">Элементы управления "заголовок" в представлении содержимого дерева модели автоматизации пользовательского интерфейса имеют нулевые дочерние элементы.</span><span class="sxs-lookup"><span data-stu-id="84430-139">Header controls have zero children in the content view of the UI Automation tree.</span></span>

## <a name="relevant-properties"></a><span data-ttu-id="84430-140">Соответствующие свойства</span><span class="sxs-lookup"><span data-stu-id="84430-140">Relevant Properties</span></span>

<span data-ttu-id="84430-141">В следующей таблице перечислены свойства модели автоматизации пользовательского интерфейса, значение или определение которых особенно важно для элементов управления "заголовок".</span><span class="sxs-lookup"><span data-stu-id="84430-141">The following table lists the UI Automation properties whose value or definition is especially relevant to header controls.</span></span> <span data-ttu-id="84430-142">Дополнительные сведения о свойствах модели автоматизации пользовательского интерфейса см. в разделе [Получение свойств элементов модели автоматизации пользовательского интерфейса](uiauto-propertiesforclients.md).</span><span class="sxs-lookup"><span data-stu-id="84430-142">For more information about UI Automation properties, see [Retrieving Properties from UI Automation Elements](uiauto-propertiesforclients.md).</span></span>



| <span data-ttu-id="84430-143">Свойство модели автоматизации пользовательского интерфейса</span><span class="sxs-lookup"><span data-stu-id="84430-143">UI Automation Property</span></span>                                                                                              | <span data-ttu-id="84430-144">Значение</span><span class="sxs-lookup"><span data-stu-id="84430-144">Value</span></span>                                                            | <span data-ttu-id="84430-145">Примечания</span><span class="sxs-lookup"><span data-stu-id="84430-145">Notes</span></span>                                                                                                                                                                                                |
|---------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="84430-146">**UIA \_ аутоматионидпропертид**</span><span class="sxs-lookup"><span data-stu-id="84430-146">**UIA\_AutomationIdPropertyId**</span></span>](uiauto-automation-element-propids.md)                 | <span data-ttu-id="84430-147">См. примечания.</span><span class="sxs-lookup"><span data-stu-id="84430-147">See notes.</span></span>                                                       | <span data-ttu-id="84430-148">Значение этого свойства должно быть уникальным для всех элементов управления в приложении.</span><span class="sxs-lookup"><span data-stu-id="84430-148">The value of this property must be unique across all controls in an application.</span></span>                                                                                                                     |
| [<span data-ttu-id="84430-149">**UIA \_ баундингректанглепропертид**</span><span class="sxs-lookup"><span data-stu-id="84430-149">**UIA\_BoundingRectanglePropertyId**</span></span>](uiauto-automation-element-propids.md)       | <span data-ttu-id="84430-150">См. примечания.</span><span class="sxs-lookup"><span data-stu-id="84430-150">See notes.</span></span>                                                       | <span data-ttu-id="84430-151">Внешний прямоугольник, содержащий весь элемент управления.</span><span class="sxs-lookup"><span data-stu-id="84430-151">The outermost rectangle that contains the whole control.</span></span>                                                                                                                                             |
| [<span data-ttu-id="84430-152">**UIA \_ кликкаблепоинтпропертид**</span><span class="sxs-lookup"><span data-stu-id="84430-152">**UIA\_ClickablePointPropertyId**</span></span>](uiauto-automation-element-propids.md)             | <span data-ttu-id="84430-153">См. примечания.</span><span class="sxs-lookup"><span data-stu-id="84430-153">See notes.</span></span>                                                       | <span data-ttu-id="84430-154">Поддерживается при наличии ограничивающего прямоугольника.</span><span class="sxs-lookup"><span data-stu-id="84430-154">Supported if there is a bounding rectangle.</span></span> <span data-ttu-id="84430-155">Если не все точки внутри ограничивающего прямоугольника являются щелчками, а элемент выполняет специализированное тестирование нажатия, переопределите и предоставьте точку для щелчка.</span><span class="sxs-lookup"><span data-stu-id="84430-155">If not every point within the bounding rectangle is clickable, and the element performs specialized hit testing, override and provide a clickable point.</span></span> |
| [<span data-ttu-id="84430-156">**UIA \_ контролтипепропертид**</span><span class="sxs-lookup"><span data-stu-id="84430-156">**UIA\_ControlTypePropertyId**</span></span>](uiauto-automation-element-propids.md)                   | <span data-ttu-id="84430-157">**Header**</span><span class="sxs-lookup"><span data-stu-id="84430-157">**Header**</span></span>                                                       |                                                                                                                                                                                                      |
| [<span data-ttu-id="84430-158">**UIA \_ исконтентелементпропертид**</span><span class="sxs-lookup"><span data-stu-id="84430-158">**UIA\_IsContentElementPropertyId**</span></span>](uiauto-automation-element-propids.md)         | <span data-ttu-id="84430-159">FALSE</span><span class="sxs-lookup"><span data-stu-id="84430-159">FALSE</span></span>                                                            | <span data-ttu-id="84430-160">Элемент управления "заголовок" не включен в представление содержимого дерева модели автоматизации пользовательского интерфейса.</span><span class="sxs-lookup"><span data-stu-id="84430-160">The header control is not included in the content view of the UI Automation tree.</span></span>                                                                                                                    |
| [<span data-ttu-id="84430-161">**UIA \_ исконтролелементпропертид**</span><span class="sxs-lookup"><span data-stu-id="84430-161">**UIA\_IsControlElementPropertyId**</span></span>](uiauto-automation-element-propids.md)         | <span data-ttu-id="84430-162">true</span><span class="sxs-lookup"><span data-stu-id="84430-162">TRUE</span></span>                                                             | <span data-ttu-id="84430-163">Элемент управления "заголовок" всегда включается в представление элемента управления дерева модели автоматизации пользовательского интерфейса.</span><span class="sxs-lookup"><span data-stu-id="84430-163">The header control is always included in the control view of the UI Automation tree.</span></span>                                                                                                                 |
| [<span data-ttu-id="84430-164">**UIA \_ искэйбоардфокусаблепропертид**</span><span class="sxs-lookup"><span data-stu-id="84430-164">**UIA\_IsKeyboardFocusablePropertyId**</span></span>](uiauto-automation-element-propids.md)   | <span data-ttu-id="84430-165">См. примечания.</span><span class="sxs-lookup"><span data-stu-id="84430-165">See notes.</span></span>                                                       | <span data-ttu-id="84430-166">Если элемент управления может получать фокус клавиатуры, он должен поддерживать это свойство.</span><span class="sxs-lookup"><span data-stu-id="84430-166">If the control can receive keyboard focus, it must support this property.</span></span>                                                                                                                            |
| [<span data-ttu-id="84430-167">**UIA \_ лабеледбипропертид**</span><span class="sxs-lookup"><span data-stu-id="84430-167">**UIA\_LabeledByPropertyId**</span></span>](uiauto-automation-element-propids.md)                       | <span data-ttu-id="84430-168">NULL</span><span class="sxs-lookup"><span data-stu-id="84430-168">NULL</span></span>                                                             | <span data-ttu-id="84430-169">Элементы управления "Заголовок" не имеют меток со статическим текстом.</span><span class="sxs-lookup"><span data-stu-id="84430-169">Header controls do not have a static label.</span></span>                                                                                                                                                          |
| [<span data-ttu-id="84430-170">**UIA \_ локализедконтролтипепропертид**</span><span class="sxs-lookup"><span data-stu-id="84430-170">**UIA\_LocalizedControlTypePropertyId**</span></span>](uiauto-automation-element-propids.md) | <span data-ttu-id="84430-171">См. примечания.</span><span class="sxs-lookup"><span data-stu-id="84430-171">See notes.</span></span>                                                       | <span data-ttu-id="84430-172">Значение по умолчанию — "заголовок" для en-US или English (США).</span><span class="sxs-lookup"><span data-stu-id="84430-172">The default value is "header" for en-US or English (United States).</span></span>                                                                                                                                  |
| [<span data-ttu-id="84430-173">**UIA \_ намепропертид**</span><span class="sxs-lookup"><span data-stu-id="84430-173">**UIA\_NamePropertyId**</span></span>](uiauto-automation-element-propids.md)                                 | <span data-ttu-id="84430-174">См. примечания.</span><span class="sxs-lookup"><span data-stu-id="84430-174">See notes.</span></span>                                                       | <span data-ttu-id="84430-175">Элемент управления "Заголовок" должен иметь имя, если существует несколько заголовков строк или несколько заголовков столбцов.</span><span class="sxs-lookup"><span data-stu-id="84430-175">The header control needs a name if there is more than one row header or more than one column header.</span></span> <span data-ttu-id="84430-176">Оно определяет сведения в заголовке.</span><span class="sxs-lookup"><span data-stu-id="84430-176">This identifies the information within the header.</span></span>                                              |
| [<span data-ttu-id="84430-177">**UIA \_ ориентатионпропертид**</span><span class="sxs-lookup"><span data-stu-id="84430-177">**UIA\_OrientationPropertyId**</span></span>](uiauto-automation-element-propids.md)                   | <span data-ttu-id="84430-178">**Ориентатионтипе \_ Горизонтальная** или **\_ вертикально ориентатионтипе**</span><span class="sxs-lookup"><span data-stu-id="84430-178">**OrientationType\_Horizontal** or **OrientationType\_Vertical**</span></span> | <span data-ttu-id="84430-179">Значение этого свойства представляет собой расположение элемента управления "заголовок", будь то заголовок строки (**\_ горизонтально ориентатионтипе**) или заголовок столбца (**ориентатионтипе \_ Vertical**).</span><span class="sxs-lookup"><span data-stu-id="84430-179">The value of this property exposes the position of the header control—whether it is a row header (**OrientationType\_Horizontal**) or column header (**OrientationType\_Vertical**).</span></span>                 |



 

## <a name="required-control-patterns"></a><span data-ttu-id="84430-180">Обязательные шаблоны элементов управления</span><span class="sxs-lookup"><span data-stu-id="84430-180">Required Control Patterns</span></span>

<span data-ttu-id="84430-181">В следующей таблице перечислены шаблоны элементов управления модели автоматизации пользовательского интерфейса, которые должны поддерживаться для элементов управления "заголовок".</span><span class="sxs-lookup"><span data-stu-id="84430-181">The following table lists the UI Automation control patterns required to be supported for header controls.</span></span> <span data-ttu-id="84430-182">Дополнительные сведения о шаблонах элементов управления см. в разделе [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md).</span><span class="sxs-lookup"><span data-stu-id="84430-182">For more information on control patterns, see [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md).</span></span>



| <span data-ttu-id="84430-183">Шаблон элемента управления</span><span class="sxs-lookup"><span data-stu-id="84430-183">Control Pattern</span></span>                                         | <span data-ttu-id="84430-184">Поддержка</span><span class="sxs-lookup"><span data-stu-id="84430-184">Support</span></span> | <span data-ttu-id="84430-185">Примечания</span><span class="sxs-lookup"><span data-stu-id="84430-185">Notes</span></span>                                                                                                             |
|---------------------------------------------------------|---------|-------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="84430-186">**ITransformProvider**</span><span class="sxs-lookup"><span data-stu-id="84430-186">**ITransformProvider**</span></span>](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itransformprovider) | <span data-ttu-id="84430-187">Зависит</span><span class="sxs-lookup"><span data-stu-id="84430-187">Depends</span></span> | <span data-ttu-id="84430-188">Реализуйте шаблон элемента [Transform](uiauto-implementingtransform.md) , если размер элемента управления заголовка может быть изменен.</span><span class="sxs-lookup"><span data-stu-id="84430-188">Implement the [Transform](uiauto-implementingtransform.md) control pattern if the header control can be resized.</span></span> |



 

## <a name="required-events"></a><span data-ttu-id="84430-189">Обязательные события</span><span class="sxs-lookup"><span data-stu-id="84430-189">Required Events</span></span>

<span data-ttu-id="84430-190">В следующей таблице перечислены события автоматизации пользовательского интерфейса, которые должны поддерживаться элементами управления "заголовок".</span><span class="sxs-lookup"><span data-stu-id="84430-190">The following table lists the UI Automation events that header controls are required to support.</span></span> <span data-ttu-id="84430-191">Дополнительные сведения о событиях см. в разделе [UI Automation Events Overview](uiauto-eventsoverview.md).</span><span class="sxs-lookup"><span data-stu-id="84430-191">For more information on events, see [UI Automation Events Overview](uiauto-eventsoverview.md).</span></span>



| <span data-ttu-id="84430-192">Событие автоматизации пользовательского интерфейса</span><span class="sxs-lookup"><span data-stu-id="84430-192">UI Automation Event</span></span>                                                                                                                   | <span data-ttu-id="84430-193">Примечания</span><span class="sxs-lookup"><span data-stu-id="84430-193">Notes</span></span>                                                                                                                      |
|---------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="84430-194">**UIA \_ аутоматионфокусчанжедевентид**</span><span class="sxs-lookup"><span data-stu-id="84430-194">**UIA\_AutomationFocusChangedEventId**</span></span>](uiauto-event-ids.md)                                      |                                                                                                                            |
| <span data-ttu-id="84430-195">[**UIA \_**](uiauto-automation-element-propids.md) Событие изменения свойства баундингректанглепропертид.</span><span class="sxs-lookup"><span data-stu-id="84430-195">[**UIA\_BoundingRectanglePropertyId**](uiauto-automation-element-propids.md) property-changed event.</span></span> |                                                                                                                            |
| <span data-ttu-id="84430-196">[**UIA \_**](uiauto-automation-element-propids.md) Событие изменения свойства исенабледпропертид.</span><span class="sxs-lookup"><span data-stu-id="84430-196">[**UIA\_IsEnabledPropertyId**](uiauto-automation-element-propids.md) property-changed event.</span></span>                 | <span data-ttu-id="84430-197">Если элемент управления поддерживает свойство « [**включено**](uiauto-automation-element-propids.md) », оно должно поддерживать это событие.</span><span class="sxs-lookup"><span data-stu-id="84430-197">If the control supports the [**IsEnabled**](uiauto-automation-element-propids.md) property, it must support this event.</span></span>   |
| <span data-ttu-id="84430-198">[**UIA \_**](uiauto-automation-element-propids.md) Событие изменения свойства исоффскринпропертид.</span><span class="sxs-lookup"><span data-stu-id="84430-198">[**UIA\_IsOffscreenPropertyId**](uiauto-automation-element-propids.md) property-changed event.</span></span>             | <span data-ttu-id="84430-199">Если элемент управления поддерживает свойство [**исоффскрин**](uiauto-automation-element-propids.md) , он должен поддерживать это событие.</span><span class="sxs-lookup"><span data-stu-id="84430-199">If the control supports the [**IsOffscreen**](uiauto-automation-element-propids.md) property, it must support this event.</span></span> |
| [<span data-ttu-id="84430-200">**UIA \_ структуречанжедевентид**</span><span class="sxs-lookup"><span data-stu-id="84430-200">**UIA\_StructureChangedEventId**</span></span>](uiauto-event-ids.md)                                                  |                                                                                                                            |



 

## <a name="related-topics"></a><span data-ttu-id="84430-201">См. также</span><span class="sxs-lookup"><span data-stu-id="84430-201">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="84430-202">**Зрения**</span><span class="sxs-lookup"><span data-stu-id="84430-202">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="84430-203">Общие сведения о типах элементов управления автоматизации пользовательского интерфейса</span><span class="sxs-lookup"><span data-stu-id="84430-203">UI Automation Control Types Overview</span></span>](uiauto-controltypesoverview.md)
</dt> <dt>

[<span data-ttu-id="84430-204">Общие сведения о модели автоматизации пользовательского интерфейса</span><span class="sxs-lookup"><span data-stu-id="84430-204">UI Automation Overview</span></span>](uiauto-uiautomationoverview.md)
</dt> </dl>

 

 




