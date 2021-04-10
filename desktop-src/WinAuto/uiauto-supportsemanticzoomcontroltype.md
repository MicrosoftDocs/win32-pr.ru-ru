---
title: Тип элемента управления Семантикзум
description: В этом разделе содержатся сведения о поддержке модели автоматизации пользовательского интерфейса для типа элемента управления Семантикзум.
ms.assetid: 37C14610-431F-46BF-97B6-CB476EA1642D
keywords:
- Модель автоматизации пользовательского интерфейса, поддержка типа элемента управления Семантикзум
- Модель автоматизации пользовательского интерфейса, тип элемента управления Семантикзум
- Модель автоматизации пользовательского интерфейса, древовидная структура для типа элемента управления Семантикзум
- Модель автоматизации пользовательского интерфейса, свойства для типа элемента управления Семантикзум
- Модель автоматизации пользовательского интерфейса, шаблоны элементов управления для типа элемента управления Семантикзум
- Модель автоматизации пользовательского интерфейса, события для типа элемента управления Семантикзум
- Древовидные структуры, тип элемента управления Семантикзум
- свойства, тип элемента управления Семантикзум
- шаблоны элементов управления, тип элемента управления Семантикзум
- события, тип элемента управления Семантикзум
- Поддержка типа элемента управления Семантикзум
- Тип элемента управления Семантикзум
- типы элементов управления, древовидная структура для типа элемента управления Семантикзум
- типы элементов управления, шаблоны элементов управления для типа элемента управления Семантикзум
- типы элементов управления, поддержка Семантикзум
- типы элементов управления, Семантикзум
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b17d4712aa4f10489081b1b5d0f69fed849080bc
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104133915"
---
# <a name="semanticzoom-control-type"></a><span data-ttu-id="eac69-119">Тип элемента управления Семантикзум</span><span class="sxs-lookup"><span data-stu-id="eac69-119">SemanticZoom Control Type</span></span>

<span data-ttu-id="eac69-120">В этом разделе содержатся сведения о поддержке модели автоматизации пользовательского интерфейса для типа элемента управления **семантикзум** .</span><span class="sxs-lookup"><span data-stu-id="eac69-120">This topic provides information about UI Automation support for the **SemanticZoom** control type.</span></span>

<span data-ttu-id="eac69-121">Семантический масштаб — это метод, появившийся в Windows 8 для представления больших наборов связанных данных или содержимого в одном представлении, например фотоальбом, список приложений или адресная книга.</span><span class="sxs-lookup"><span data-stu-id="eac69-121">Semantic Zoom is a technique introduced in Windows 8 for presenting and navigating large sets of related data or content within a single view, such as a photo album, app list, or address book.</span></span> <span data-ttu-id="eac69-122">Для Организации и представления содержимого семантический масштаб использует два различных режима классификации или *масштабирования*.</span><span class="sxs-lookup"><span data-stu-id="eac69-122">Semantic Zoom uses two distinct modes of classification, or *zoom levels*, for organizing and presenting the content.</span></span> <span data-ttu-id="eac69-123">В режиме низкого уровня (или *с увеличенным масштабом*) элементы отображаются в виде плоской структуры «все». а высокоуровневый (или *уменьшенный*) режим отображает элементы в группах, позволяя пользователю быстро перемещаться по содержимому и просматривать его.</span><span class="sxs-lookup"><span data-stu-id="eac69-123">The low-level (or *zoomed in*) mode displays items in a flat, "all-up" structure; and the high-level (or *zoomed out*) mode displays items in groups, enabling the user to quickly navigate and browse through the content.</span></span> <span data-ttu-id="eac69-124">Например, изменение масштаба списка городов может привести к изменению списка Штатов, содержащих эти города.</span><span class="sxs-lookup"><span data-stu-id="eac69-124">For example, zooming a list of cities might change to a list of states containing those cities.</span></span> <span data-ttu-id="eac69-125">Изменение масштаба списка программ может привести к поссылке на список логических групп программ.</span><span class="sxs-lookup"><span data-stu-id="eac69-125">Zooming a list of programs might change to a list of logical program groups.</span></span>

<span data-ttu-id="eac69-126">Дополнительные сведения о семантическом масштабе, специально используемом для приложений Магазина Windows, см. в разделе [рекомендации по семантическому масштабу](/windows/uwp/controls-and-patterns/semantic-zoom).</span><span class="sxs-lookup"><span data-stu-id="eac69-126">For more information about Semantic Zoom specifically as used for Windows Store apps, see [Guidelines for Semantic Zoom](/windows/uwp/controls-and-patterns/semantic-zoom).</span></span>

<span data-ttu-id="eac69-127">Модель использования для типа элемента управления **семантикзум** необычна в том, что она существует в основном для программного доступа.</span><span class="sxs-lookup"><span data-stu-id="eac69-127">The usage model for the **SemanticZoom** control type is unusual in that it exists mainly for programmatic access.</span></span> <span data-ttu-id="eac69-128">Клиенты автоматизации пользовательского интерфейса Майкрософт могут отслеживать контроль семантического масштабирования и управлять им, чтобы управлять состоянием списка.</span><span class="sxs-lookup"><span data-stu-id="eac69-128">Microsoft UI Automation clients can monitor and manipulate the Semantic Zoom control to control the zoomed-in state of the list.</span></span> <span data-ttu-id="eac69-129">Пользователи, не использующие специальные технологии, обычно управляют семантическим контролем масштаба непосредственно через сенсорные жесты или сочетания клавиш.</span><span class="sxs-lookup"><span data-stu-id="eac69-129">Users who are not using assistive technology would typically manipulate the Semantic Zoom control directly through touch gestures or keyboard shortcuts.</span></span>

<span data-ttu-id="eac69-130">В следующих разделах определяется необходимая древовидная структура модели автоматизации пользовательского интерфейса, свойства, шаблоны элементов управления и события для типа элемента управления **семантикзум** .</span><span class="sxs-lookup"><span data-stu-id="eac69-130">The following sections define the required UI Automation tree structure, properties, control patterns, and events for the **SemanticZoom** control type.</span></span> <span data-ttu-id="eac69-131">Требования к автоматизации пользовательского интерфейса применяются ко всем элементам управления семантического масштабирования, в которых платформа или платформа пользовательского интерфейса интегрирует поддержку автоматизации пользовательского интерфейса для типов элементов управления и шаблонов элементов управления.</span><span class="sxs-lookup"><span data-stu-id="eac69-131">The UI Automation requirements apply to all Semantic Zoom controls where the UI framework/platform integrates UI Automation support for control types and control patterns.</span></span>

<span data-ttu-id="eac69-132">В этом разделе содержатся следующие подразделы.</span><span class="sxs-lookup"><span data-stu-id="eac69-132">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="eac69-133">Типичная древовидная структура</span><span class="sxs-lookup"><span data-stu-id="eac69-133">Typical Tree Structure</span></span>](#typical-tree-structure)
-   [<span data-ttu-id="eac69-134">Соответствующие свойства</span><span class="sxs-lookup"><span data-stu-id="eac69-134">Relevant Properties</span></span>](#relevant-properties)
-   [<span data-ttu-id="eac69-135">Обязательные шаблоны элементов управления и свойства</span><span class="sxs-lookup"><span data-stu-id="eac69-135">Required Control Patterns and Properties</span></span>](#required-control-patterns-and-properties)
-   [<span data-ttu-id="eac69-136">Обязательные события</span><span class="sxs-lookup"><span data-stu-id="eac69-136">Required Events</span></span>](#required-events)
-   [<span data-ttu-id="eac69-137">Замечания</span><span class="sxs-lookup"><span data-stu-id="eac69-137">Remarks</span></span>](#remarks)
-   [<span data-ttu-id="eac69-138">См. также</span><span class="sxs-lookup"><span data-stu-id="eac69-138">Related topics</span></span>](#related-topics)

## <a name="typical-tree-structure"></a><span data-ttu-id="eac69-139">Типичная древовидная структура</span><span class="sxs-lookup"><span data-stu-id="eac69-139">Typical Tree Structure</span></span>

<span data-ttu-id="eac69-140">В следующей таблице описывается типичный элемент управления и представление содержимого дерева модели автоматизации пользовательского интерфейса, относящиеся к типу элемента управления **семантикзум** , и показывается, что может содержаться в каждом представлении.</span><span class="sxs-lookup"><span data-stu-id="eac69-140">The following table depicts a typical control and content view of the UI Automation tree that pertains to the **SemanticZoom** control type and describes what can be contained in each view.</span></span> <span data-ttu-id="eac69-141">Дополнительные сведения о дереве автоматизации пользовательского интерфейса см. в разделе [Общие сведения о дереве модели автоматизации пользовательского интерфейса](uiauto-treeoverview.md).</span><span class="sxs-lookup"><span data-stu-id="eac69-141">For more information about the UI Automation tree, see [UI Automation Tree Overview](uiauto-treeoverview.md).</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="eac69-142">Представление элемента управления</span><span class="sxs-lookup"><span data-stu-id="eac69-142">Control View</span></span></th>
<th><span data-ttu-id="eac69-143">Представление содержимого</span><span class="sxs-lookup"><span data-stu-id="eac69-143">Content View</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><ul>
<li><span data-ttu-id="eac69-144">Список</span><span class="sxs-lookup"><span data-stu-id="eac69-144">List</span></span>
<ul>
<li><span data-ttu-id="eac69-145">[Семантикзум]</span><span class="sxs-lookup"><span data-stu-id="eac69-145">[SemanticZoom]</span></span>
<ul>
<li><span data-ttu-id="eac69-146">ListItem (0 или более)</span><span class="sxs-lookup"><span data-stu-id="eac69-146">ListItem (0 or more)</span></span></li>
</ul></li>
</ul></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="eac69-147">Список</span><span class="sxs-lookup"><span data-stu-id="eac69-147">List</span></span>
<ul>
<li><span data-ttu-id="eac69-148">ListItem (0 или более)</span><span class="sxs-lookup"><span data-stu-id="eac69-148">ListItem (0 or more)</span></span></li>
</ul></li>
</ul></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="eac69-149">Или сделайте так:</span><span class="sxs-lookup"><span data-stu-id="eac69-149">Or:</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="eac69-150">Представление элемента управления</span><span class="sxs-lookup"><span data-stu-id="eac69-150">Control View</span></span></th>
<th><span data-ttu-id="eac69-151">Представление содержимого</span><span class="sxs-lookup"><span data-stu-id="eac69-151">Content View</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><ul>
<li><span data-ttu-id="eac69-152">[Семантикзум]</span><span class="sxs-lookup"><span data-stu-id="eac69-152">[SemanticZoom]</span></span>
<ul>
<li><span data-ttu-id="eac69-153">Список</span><span class="sxs-lookup"><span data-stu-id="eac69-153">List</span></span>
<ul>
<li><span data-ttu-id="eac69-154">ListItem (0 или более)</span><span class="sxs-lookup"><span data-stu-id="eac69-154">ListItem (0 or more)</span></span></li>
</ul></li>
</ul></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="eac69-155">Список</span><span class="sxs-lookup"><span data-stu-id="eac69-155">List</span></span>
<ul>
<li><span data-ttu-id="eac69-156">ListItem (0 или более)</span><span class="sxs-lookup"><span data-stu-id="eac69-156">ListItem (0 or more)</span></span></li>
</ul></li>
</ul></td>
</tr>
</tbody>
</table>



 

## <a name="relevant-properties"></a><span data-ttu-id="eac69-157">Соответствующие свойства</span><span class="sxs-lookup"><span data-stu-id="eac69-157">Relevant Properties</span></span>

<span data-ttu-id="eac69-158">В следующей таблице перечислены свойства модели автоматизации пользовательского интерфейса, значения или определения которых особенно важны для элементов управления, реализующих тип элемента управления **семантикзум** .</span><span class="sxs-lookup"><span data-stu-id="eac69-158">The following table lists the UI Automation properties whose value or definition is especially relevant to the controls that implement the **SemanticZoom** control type.</span></span> <span data-ttu-id="eac69-159">Дополнительные сведения о свойствах модели автоматизации пользовательского интерфейса см. в разделе [Получение свойств элементов модели автоматизации пользовательского интерфейса](uiauto-propertiesforclients.md).</span><span class="sxs-lookup"><span data-stu-id="eac69-159">For more information about UI Automation properties, see [Retrieving Properties from UI Automation Elements](uiauto-propertiesforclients.md).</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="eac69-160">Свойство модели автоматизации пользовательского интерфейса</span><span class="sxs-lookup"><span data-stu-id="eac69-160">UI Automation Property</span></span></th>
<th><span data-ttu-id="eac69-161">Значение</span><span class="sxs-lookup"><span data-stu-id="eac69-161">Value</span></span></th>
<th><span data-ttu-id="eac69-162">Примечания</span><span class="sxs-lookup"><span data-stu-id="eac69-162">Notes</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="eac69-163"><a href="uiauto-automation-element-propids.md"><strong>UIA_AutomationIdPropertyId</strong></a></span><span class="sxs-lookup"><span data-stu-id="eac69-163"><a href="uiauto-automation-element-propids.md"><strong>UIA_AutomationIdPropertyId</strong></a></span></span></td>
<td><span data-ttu-id="eac69-164">См. примечания.</span><span class="sxs-lookup"><span data-stu-id="eac69-164">See notes.</span></span></td>
<td><span data-ttu-id="eac69-165">Значение этого свойства должно быть уникальным среди всех одноранговых элементов в необработанном представлении дерева модели автоматизации пользовательского интерфейса.</span><span class="sxs-lookup"><span data-stu-id="eac69-165">The value of this property must be unique among all peer elements in the raw view of the UI Automation tree.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="eac69-166"><a href="uiauto-automation-element-propids.md"><strong>UIA_BoundingRectanglePropertyId</strong></a></span><span class="sxs-lookup"><span data-stu-id="eac69-166"><a href="uiauto-automation-element-propids.md"><strong>UIA_BoundingRectanglePropertyId</strong></a></span></span></td>
<td><span data-ttu-id="eac69-167">См. примечания.</span><span class="sxs-lookup"><span data-stu-id="eac69-167">See notes.</span></span></td>
<td><span data-ttu-id="eac69-168">Внешний прямоугольник, содержащий весь элемент управления.</span><span class="sxs-lookup"><span data-stu-id="eac69-168">The outermost rectangle that contains the whole control.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="eac69-169"><a href="uiauto-automation-element-propids.md"><strong>UIA_ClickablePointPropertyId</strong></a></span><span class="sxs-lookup"><span data-stu-id="eac69-169"><a href="uiauto-automation-element-propids.md"><strong>UIA_ClickablePointPropertyId</strong></a></span></span></td>
<td><span data-ttu-id="eac69-170">См. примечания.</span><span class="sxs-lookup"><span data-stu-id="eac69-170">See notes.</span></span></td>
<td><span data-ttu-id="eac69-171">Если элемент управления "список" имеет точку щелчка (точка, которую можно щелкнуть, чтобы перестать фокусом списка), эта точка должна предоставляться через это свойство.</span><span class="sxs-lookup"><span data-stu-id="eac69-171">If the list control has a clickable point (a point that can be clicked to cause the list to take focus), that point must be exposed through this property.</span></span> <span data-ttu-id="eac69-172">Если значение свойства <a href="uiauto-automation-element-propids.md"><strong>UIA_IsOffscreenPropertyId</strong></a> равно <strong>true</strong>, попытка получить это свойство приводит к ошибке <a href="uiauto-error-codes.md"><strong>UIA_E_NOCLICKABLEPOINT</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="eac69-172">If the value of the <a href="uiauto-automation-element-propids.md"><strong>UIA_IsOffscreenPropertyId</strong></a> property is <strong>TRUE</strong>, attempting to retrieve this property results in the <a href="uiauto-error-codes.md"><strong>UIA_E_NOCLICKABLEPOINT</strong></a> error.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="eac69-173"><a href="uiauto-automation-element-propids.md"><strong>UIA_ControlTypePropertyId</strong></a></span><span class="sxs-lookup"><span data-stu-id="eac69-173"><a href="uiauto-automation-element-propids.md"><strong>UIA_ControlTypePropertyId</strong></a></span></span></td>
<td><span data-ttu-id="eac69-174"><strong>SemanticZoom</strong></span><span class="sxs-lookup"><span data-stu-id="eac69-174"><strong>SemanticZoom</strong></span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="eac69-175"><a href="uiauto-automation-element-propids.md"><strong>UIA_IsContentElementPropertyId</strong></a></span><span class="sxs-lookup"><span data-stu-id="eac69-175"><a href="uiauto-automation-element-propids.md"><strong>UIA_IsContentElementPropertyId</strong></a></span></span></td>
<td><span data-ttu-id="eac69-176">true</span><span class="sxs-lookup"><span data-stu-id="eac69-176">TRUE</span></span></td>

</tr>
<tr class="even">
<td><span data-ttu-id="eac69-177"><a href="uiauto-automation-element-propids.md"><strong>UIA_IsControlElementPropertyId</strong></a></span><span class="sxs-lookup"><span data-stu-id="eac69-177"><a href="uiauto-automation-element-propids.md"><strong>UIA_IsControlElementPropertyId</strong></a></span></span></td>
<td><span data-ttu-id="eac69-178">true</span><span class="sxs-lookup"><span data-stu-id="eac69-178">TRUE</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="eac69-179"><a href="uiauto-automation-element-propids.md"><strong>UIA_IsKeyboardFocusablePropertyId</strong></a></span><span class="sxs-lookup"><span data-stu-id="eac69-179"><a href="uiauto-automation-element-propids.md"><strong>UIA_IsKeyboardFocusablePropertyId</strong></a></span></span></td>
<td><span data-ttu-id="eac69-180">FALSE</span><span class="sxs-lookup"><span data-stu-id="eac69-180">FALSE</span></span></td>

</tr>
<tr class="even">
<td><span data-ttu-id="eac69-181"><a href="uiauto-automation-element-propids.md"><strong>UIA_LabeledByPropertyId</strong></a></span><span class="sxs-lookup"><span data-stu-id="eac69-181"><a href="uiauto-automation-element-propids.md"><strong>UIA_LabeledByPropertyId</strong></a></span></span></td>
<td><span data-ttu-id="eac69-182">См. примечания.</span><span class="sxs-lookup"><span data-stu-id="eac69-182">See notes.</span></span></td>
<td><span data-ttu-id="eac69-183">Если имеется статическая текстовая метка, это свойство должно предоставлять ссылку на этот элемент управления.</span><span class="sxs-lookup"><span data-stu-id="eac69-183">If there is a static text label, this property must expose a reference to that control.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="eac69-184"><a href="uiauto-automation-element-propids.md"><strong>UIA_LocalizedControlTypePropertyId</strong></a></span><span class="sxs-lookup"><span data-stu-id="eac69-184"><a href="uiauto-automation-element-propids.md"><strong>UIA_LocalizedControlTypePropertyId</strong></a></span></span></td>
<td><span data-ttu-id="eac69-185">См. примечания.</span><span class="sxs-lookup"><span data-stu-id="eac69-185">See notes.</span></span></td>
<td><span data-ttu-id="eac69-186">Локализованная строка, соответствующая типу элемента управления <strong>семантикзум</strong> .</span><span class="sxs-lookup"><span data-stu-id="eac69-186">A localized string corresponding to the <strong>SemanticZoom</strong> control type.</span></span> <span data-ttu-id="eac69-187">По умолчанию используется значение &quot; семантического масштабирования &quot; для en-US или English (США).</span><span class="sxs-lookup"><span data-stu-id="eac69-187">The default value is &quot;semantic zoom&quot; for en-US or English (United States).</span></span>
<blockquote>
[!Note]<br />
<span data-ttu-id="eac69-188">Некоторые платформы сцепляются это как &quot; семантикзум &quot; .</span><span class="sxs-lookup"><span data-stu-id="eac69-188">Some frameworks concatenated this as &quot;semanticzoom&quot;.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="eac69-189"><a href="uiauto-automation-element-propids.md"><strong>UIA_NamePropertyId</strong></a></span><span class="sxs-lookup"><span data-stu-id="eac69-189"><a href="uiauto-automation-element-propids.md"><strong>UIA_NamePropertyId</strong></a></span></span></td>
<td><span data-ttu-id="eac69-190">См. примечания.</span><span class="sxs-lookup"><span data-stu-id="eac69-190">See notes.</span></span></td>
<td><span data-ttu-id="eac69-191">Допустима пустая строка, или может быть предоставлено более полезное имя, если оно не содержит термина семантического масштабирования, что сделает сочетание типа элемента управления и имени незапутанным.</span><span class="sxs-lookup"><span data-stu-id="eac69-191">An empty string is acceptable, or a more useful name could be provided, as long as it does not contain the term  semantic zoom , which would make the combination of control type and name confusing.</span></span></td>
</tr>
</tbody>
</table>



 

## <a name="required-control-patterns-and-properties"></a><span data-ttu-id="eac69-192">Обязательные шаблоны элементов управления и свойства</span><span class="sxs-lookup"><span data-stu-id="eac69-192">Required Control Patterns and Properties</span></span>

<span data-ttu-id="eac69-193">В следующей таблице перечислены шаблоны элементов управления модели автоматизации пользовательского интерфейса, которые должны поддерживаться всеми элементами управления семантического масштабирования.</span><span class="sxs-lookup"><span data-stu-id="eac69-193">The following table lists the UI Automation control patterns required to be supported by all Semantic Zoom controls.</span></span> <span data-ttu-id="eac69-194">Дополнительные сведения о шаблонах элементов управления см. в разделе [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md).</span><span class="sxs-lookup"><span data-stu-id="eac69-194">For more information on control patterns, see [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md).</span></span>



| <span data-ttu-id="eac69-195">Шаблон элемента управления/свойство шаблона</span><span class="sxs-lookup"><span data-stu-id="eac69-195">Control Pattern/Pattern Property</span></span>                  | <span data-ttu-id="eac69-196">Поддержка/значение</span><span class="sxs-lookup"><span data-stu-id="eac69-196">Support/Value</span></span> | <span data-ttu-id="eac69-197">Примечания</span><span class="sxs-lookup"><span data-stu-id="eac69-197">Notes</span></span>                                                                                                                                                                                                                                                                                                                                                          |
|---------------------------------------------------|---------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="eac69-198">**IToggleProvider**</span><span class="sxs-lookup"><span data-stu-id="eac69-198">**IToggleProvider**</span></span>](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itoggleprovider) | <span data-ttu-id="eac69-199">Зависит</span><span class="sxs-lookup"><span data-stu-id="eac69-199">Depends</span></span>       | <span data-ttu-id="eac69-200">Элементы управления семантического масштабирования поддерживают шаблон элемента управления [Toggle](uiauto-implementingtoggle.md) , чтобы разрешить включение или отключение масштабирования.</span><span class="sxs-lookup"><span data-stu-id="eac69-200">Semantic Zoom controls support the [Toggle](uiauto-implementingtoggle.md) control pattern to allow the zoom to be enabled or disabled.</span></span> <span data-ttu-id="eac69-201">[**Тогглестате \_ Off**](/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-togglestate) соответствует неструктурированному состоянию, и [**тогглестате \_ On**](/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-togglestate) соответствует высокоуровневой, масштабному представлению.</span><span class="sxs-lookup"><span data-stu-id="eac69-201">[**ToggleState\_Off**](/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-togglestate) corresponds to the flat, all-up state, and [**ToggleState\_On**](/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-togglestate) corresponds to the high level, zoomed-out view.</span></span> |



 

## <a name="required-events"></a><span data-ttu-id="eac69-202">Обязательные события</span><span class="sxs-lookup"><span data-stu-id="eac69-202">Required Events</span></span>

<span data-ttu-id="eac69-203">В следующей таблице перечислены события автоматизации пользовательского интерфейса, которые требуются для поддержки элементов управления семантического масштаба.</span><span class="sxs-lookup"><span data-stu-id="eac69-203">The following table lists the UI Automation events that Semantic Zoom controls are required to support.</span></span> <span data-ttu-id="eac69-204">Дополнительные сведения о событиях см. в разделе [UI Automation Events Overview](uiauto-eventsoverview.md).</span><span class="sxs-lookup"><span data-stu-id="eac69-204">For more information on events, see [UI Automation Events Overview](uiauto-eventsoverview.md).</span></span>



| <span data-ttu-id="eac69-205">Событие автоматизации пользовательского интерфейса</span><span class="sxs-lookup"><span data-stu-id="eac69-205">UI Automation Event</span></span>                                                                                                                   | <span data-ttu-id="eac69-206">Примечания</span><span class="sxs-lookup"><span data-stu-id="eac69-206">Notes</span></span>                                                                                                                      |
|---------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="eac69-207">[**UIA \_**](uiauto-automation-element-propids.md) Событие изменения свойства баундингректанглепропертид.</span><span class="sxs-lookup"><span data-stu-id="eac69-207">[**UIA\_BoundingRectanglePropertyId**](uiauto-automation-element-propids.md) property-changed event.</span></span> |                                                                                                                            |
| <span data-ttu-id="eac69-208">[**UIA \_**](uiauto-automation-element-propids.md) Событие изменения свойства исенабледпропертид.</span><span class="sxs-lookup"><span data-stu-id="eac69-208">[**UIA\_IsEnabledPropertyId**](uiauto-automation-element-propids.md) property-changed event.</span></span>                 | <span data-ttu-id="eac69-209">Если элемент управления поддерживает свойство « [**включено**](uiauto-automation-element-propids.md) », оно должно поддерживать это событие.</span><span class="sxs-lookup"><span data-stu-id="eac69-209">If the control supports the [**IsEnabled**](uiauto-automation-element-propids.md) property, it must support this event.</span></span>   |
| <span data-ttu-id="eac69-210">[**UIA \_**](uiauto-automation-element-propids.md) Событие изменения свойства исоффскринпропертид.</span><span class="sxs-lookup"><span data-stu-id="eac69-210">[**UIA\_IsOffscreenPropertyId**](uiauto-automation-element-propids.md) property-changed event.</span></span>             | <span data-ttu-id="eac69-211">Если элемент управления поддерживает свойство [**исоффскрин**](uiauto-automation-element-propids.md) , он должен поддерживать это событие.</span><span class="sxs-lookup"><span data-stu-id="eac69-211">If the control supports the [**IsOffscreen**](uiauto-automation-element-propids.md) property, it must support this event.</span></span> |
| <span data-ttu-id="eac69-212">[**UIA \_**](uiauto-control-pattern-propids.md) Событие изменения свойства тогглетогглестатепропертид.</span><span class="sxs-lookup"><span data-stu-id="eac69-212">[**UIA\_ToggleToggleStatePropertyId**](uiauto-control-pattern-propids.md) property-changed event.</span></span>    |                                                                                                                            |



 

## <a name="remarks"></a><span data-ttu-id="eac69-213">Комментарии</span><span class="sxs-lookup"><span data-stu-id="eac69-213">Remarks</span></span>

<span data-ttu-id="eac69-214">Если в пользовательском интерфейсе есть видимая кнопка для переключения режима управления семантическим масштабом, эта кнопка не должна иметь тип элемента управления **семантикзум** .</span><span class="sxs-lookup"><span data-stu-id="eac69-214">If a UI has a visible button to toggle Semantic Zoom control behavior, this button should not have a **SemanticZoom** control type.</span></span> <span data-ttu-id="eac69-215">Это интуитивно понятный счетчик, но тип элемента управления **семантикзум** характеризует контейнер масштабирования содержимого, а не кнопку, управляющую масштабом.</span><span class="sxs-lookup"><span data-stu-id="eac69-215">This is counter-intuitive, but the **SemanticZoom** control type characterizes the container of the zooming content, not a button that controls the zoom.</span></span> <span data-ttu-id="eac69-216">(Такую кнопку можно представить просто как тип элемента управления [кнопки](uiauto-supportbuttoncontroltype.md) с шаблоном элемента управления [Toggle](uiauto-implementingtoggle.md) .)</span><span class="sxs-lookup"><span data-stu-id="eac69-216">(Such a button could be represented simply as a [Button](uiauto-supportbuttoncontroltype.md) control type with the [Toggle](uiauto-implementingtoggle.md) control pattern.)</span></span>

## <a name="related-topics"></a><span data-ttu-id="eac69-217">См. также</span><span class="sxs-lookup"><span data-stu-id="eac69-217">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="eac69-218">Общие сведения о типах элементов управления автоматизации пользовательского интерфейса</span><span class="sxs-lookup"><span data-stu-id="eac69-218">UI Automation Control Types Overview</span></span>](uiauto-controltypesoverview.md)
</dt> <dt>

[<span data-ttu-id="eac69-219">Общие сведения о модели автоматизации пользовательского интерфейса</span><span class="sxs-lookup"><span data-stu-id="eac69-219">UI Automation Overview</span></span>](uiauto-uiautomationoverview.md)
</dt> </dl>

 

